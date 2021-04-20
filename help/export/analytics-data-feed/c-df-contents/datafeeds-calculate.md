---
description: Beschrijft hoe te om gemeenschappelijke metriek te berekenen gebruikend gegevensvoer.
keywords: Gegevensfeed;taak;metriek;pre-kolom;post kolom;bots;datum filteren;gebeurtenistekenreeks;common;formules
title: Metrische gegevens berekenen
feature: Reports & Analytics Basics & Analytics Basics
uuid: a45ea5bb-7c83-468f-b94a-63add78931d7
exl-id: f9b0d637-7a6e-416a-adff-3c7e533bfac7
translation-type: tm+mt
source-git-commit: f9b5380cfb2cdfe1827b8ee70f60c65ff5004b48
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 0%

---

# Gegevensfeeds gebruiken om algemene metriek te berekenen

Beschrijft hoe te om gemeenschappelijke metriek te berekenen gebruikend gegevensvoer.

>[!IMPORTANT]
>
>Hits die normaal gesproken van Adobe Analytics worden uitgesloten, worden opgenomen in gegevensfeeds. Gebruik `exclude_hit > 0` om uitgesloten klappen uit vragen over ruwe gegevens te verwijderen. Gegevensbronnen worden ook opgenomen in gegevensfeeds. Als u gegevensbronnen wilt uitsluiten, sluit dan alle rijen met `hit_source = 5,7,8,9` uit.

## Paginaweergaven

1. Telt het aantal rijen waarin een waarde `post_pagename` of `post_page_url` is.

## Bezoeken

1. Samenvoegen `post_visid_high`, `post_visid_low`, `visit_num` en `visit_start_time_gmt`.
1. Telt het unieke aantal waarden.

>[!NOTE]
>
>Onregelmatigheden op internet, systeemonregelmatigheden of het gebruik van aangepaste bezoeker-id&#39;s kunnen zelden dezelfde `visit_num`-waarden gebruiken voor verschillende bezoeken. Gebruik `visit_start_time_gmt` bij het tellen van bezoeken om ervoor te zorgen dat deze bezoeken worden geteld.

## Bezoekers

Alle methoden die Adobe gebruikt om unieke bezoekers te identificeren (aangepaste bezoeker-id, Experience Cloud-id-service, enz.) worden uiteindelijk allemaal berekend als een waarde in `post_visid_high` en `post_visid_low`. De samenvoeging van deze twee kolommen kan worden gebruikt als standaard voor het identificeren van unieke bezoekers, ongeacht hoe zij als unieke bezoeker zijn geïdentificeerd. Als u wilt begrijpen welke methode Adobe wordt gebruikt om een unieke bezoeker te identificeren, gebruikt u de kolom `post_visid_type`.

1. Verbind `post_visid_high` en `post_visid_low`.
2. Telt het unieke aantal waarden.

## Koppelingen aanpassen, downloaden of afsluiten

1. Telt het aantal rijen waarin:
   * `post_page_event = 100` voor aangepaste koppelingen
   * `post_page_event = 101` voor downloadkoppelingen
   * `post_page_event = 102` voor exit-koppelingen

## Aangepaste gebeurtenissen

Alle metriek worden in de `post_event_list` kolom geteld als door komma&#39;s gescheiden gehele getallen. Gebruik `event.tsv` om numerieke waarden aan te passen aan de gewenste gebeurtenis. `post_event_list = 1,200` geeft bijvoorbeeld aan dat de hit een aankoopgebeurtenis en een aangepaste gebeurtenis 1 bevatte.

1. Telt het aantal keren dat de opzoekwaarde van de gebeurtenis wordt weergegeven in `post_event_list`.

## Tijd besteed

De bezoekers moeten eerst per bezoek worden gegroepeerd en vervolgens worden besteld op basis van het nummer van de treffer tijdens het bezoek.

1. Samenvoegen `post_visid_high`, `post_visid_low`, `visit_num` en `visit_start_time_gmt`.
2. Sorteren op deze samengevoegde waarde en vervolgens een secundaire sortering op `visit_page_num` toepassen.
3. Als een hit niet de laatste in een bezoek is, trekt u de waarde `post_cust_hit_time` van de waarde `post_cust_hit_time` van de volgende hit af.
4. Dit getal is de hoeveelheid tijd (in seconden) die voor de treffer is doorgebracht. Filters kunnen worden toegepast om de focus op dimensiepunten of gebeurtenissen te verplaatsen.

## Orders, eenheden en inkomsten

Als de waarde `currency` van een treffer niet de munt van een rapportreeks aanpast, wordt het omgezet gebruikend de omrekeningskoers van die dag. De kolom `post_product_list` gebruikt de omgezette valutawaarde, zodat gebruiken alle treffers de zelfde munt in deze kolom.

1. Sluit alle rijen uit waarin `duplicate_purchase = 1`.
2. Neem alleen rijen op waarin `event_list` de aankoopgebeurtenis bevat.
3. Parseer de kolom `post_product_list` om alle prijsgegevens te extraheren. De kolom `post_product_list` is op dezelfde manier opgemaakt als de variabele `s.products`.
4. Bereken de gewenste metrische waarde:
   * Aantal rijen tellen om Orden te berekenen
   * Som het aantal `quantity` in het productkoord om Eenheden te berekenen
   * Som het aantal `price` in het productkoord om opbrengst te berekenen
