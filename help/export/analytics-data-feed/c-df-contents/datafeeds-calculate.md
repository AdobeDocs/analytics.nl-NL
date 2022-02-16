---
description: Beschrijft hoe te om gemeenschappelijke metriek te berekenen gebruikend gegevensvoer.
keywords: Gegevensfeed;taak;metriek;pre-kolom;post kolom;bots;datum filteren;gebeurtenistekenreeks;common;formules
title: Metrische gegevens berekenen
feature: Data Feeds
exl-id: f9b0d637-7a6e-416a-adff-3c7e533bfac7
source-git-commit: 4daa5c8bdbcb483f23a3b8f75dde9eeb48516db8
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---

# Gegevensfeeds gebruiken om algemene metriek te berekenen

Beschrijft hoe te om gemeenschappelijke metriek te berekenen gebruikend gegevensvoer.

>[!IMPORTANT]
>
>Hits die normaal gesproken van Adobe Analytics worden uitgesloten, worden opgenomen in gegevensfeeds. Gebruiken `exclude_hit > 0` om uitgesloten klappen uit vragen over ruwe gegevens te verwijderen. Gegevensbronnen worden ook opgenomen in gegevensfeeds. Als u gegevensbronnen wilt uitsluiten, sluit dan alle rijen uit met `hit_source = 5,7,8,9`.

## Paginaweergaven

1. Telt het aantal rijen waarin een waarde zich bevindt `post_pagename` of `post_page_url`.

## Bezoeken

1. Samenvoegen `post_visid_high`, `post_visid_low`, `visit_num`, en `visit_start_time_gmt`.
1. Telt het unieke aantal waarden.

>[!NOTE]
>
>Onregelmatigheden op internet, systeemonregelmatigheden of het gebruik van aangepaste bezoeker-id&#39;s kunnen zelden hetzelfde gebruiken `visit_num` waarden voor verschillende bezoeken. Gebruiken `visit_start_time_gmt` bij het tellen van bezoeken om ervoor te zorgen dat deze bezoeken worden geteld.

## Bezoekers

Alle methoden die Adobe gebruikt om unieke bezoekers te identificeren (aangepaste bezoeker-id, Experience Cloud-id-service, enz.) worden uiteindelijk allemaal berekend als een waarde in `post_visid_high` en `post_visid_low`. De samenvoeging van deze twee kolommen kan worden gebruikt als standaard voor het identificeren van unieke bezoekers, ongeacht hoe zij als unieke bezoeker zijn geïdentificeerd. Als u wilt begrijpen welke methode Adobe wordt gebruikt om een unieke bezoeker te identificeren, gebruikt u de kolom `post_visid_type`.

1. Samenvoegen `post_visid_high` en `post_visid_low`.
2. Telt het unieke aantal waarden.

## Koppelingen aanpassen, downloaden of afsluiten

1. Telt het aantal rijen waarin:
   * `post_page_event = 100` voor aangepaste koppelingen
   * `post_page_event = 101` voor downloadkoppelingen
   * `post_page_event = 102` voor exit-koppelingen

## Aangepaste gebeurtenissen

Alle metriek worden geteld in de `post_event_list` kolom als door komma&#39;s gescheiden gehele getallen. Gebruiken `event.tsv` om numerieke waarden aan te passen aan de gewenste gebeurtenis. Bijvoorbeeld: `post_event_list = 1,200` geeft aan dat de hit een aankoopgebeurtenis en een aangepaste gebeurtenis 1 bevatte.

1. Tellen hoe vaak de opzoekwaarde van de gebeurtenis wordt weergegeven in `post_event_list`.

## Tijd besteed

De bezoekers moeten eerst per bezoek worden gegroepeerd en vervolgens worden besteld op basis van het nummer van de treffer tijdens het bezoek.

1. Samenvoegen `post_visid_high`, `post_visid_low`, `visit_num`, en `visit_start_time_gmt`.
2. Sorteren op deze samengevoegde waarde en vervolgens een secundaire sortering toepassen op `visit_page_num`.
3. Als een treffer niet de laatste in een bezoek is, trekt u de opdracht `post_cust_hit_time` waarde van de volgende treffer `post_cust_hit_time` waarde.
4. Dit getal is de hoeveelheid tijd (in seconden) die voor de treffer is doorgebracht. Filters kunnen worden toegepast om de focus op dimensiepunten of gebeurtenissen te verplaatsen.

## Orders, eenheden en inkomsten

Als een hit `currency` De waarde komt niet overeen met de valuta van een rapportsuite. De waarde wordt omgezet met de conversiekoers van die dag. De kolom `post_product_list` gebruikt de omgezette valutawaarde, zodat alle treffers dezelfde valuta in deze kolom gebruiken.

1. Alle rijen uitsluiten waar `duplicate_purchase = 1`.
2. Alleen rijen opnemen waarin `event_list` bevat de aankoopgebeurtenis.
3. Parseren `post_product_list` kolom om alle prijsgegevens te extraheren. De `post_product_list` kolom is op dezelfde manier opgemaakt als de kolom `s.products` variabele.
4. Bereken de gewenste metrische waarde:
   * Aantal rijen tellen om Orden te berekenen
   * Som het aantal van `quantity` in de productreeks om Eenheden te berekenen
   * Som het aantal van `price` in de productreeks om opbrengst te berekenen
