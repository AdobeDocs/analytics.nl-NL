---
description: Beschrijft hoe te om gemeenschappelijke metriek te berekenen gebruikend gegevensvoer.
keywords: Gegevensfeed;taak;metriek;pre-kolom;post kolom;bots;datum filteren;gebeurtenistekenreeks;common;formules
title: Metrische gegevens berekenen
feature: Data Feeds
exl-id: f9b0d637-7a6e-416a-adff-3c7e533bfac7
source-git-commit: adee2f1013cfd2ae231e3133b5a5327b8792bd16
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---

# Gegevensfeeds gebruiken om algemene metriek te berekenen

Beschrijft hoe te om gemeenschappelijke metriek te berekenen gebruikend gegevensvoer.

>[!NOTE]
>
>Hits die normaal gesproken van Analysis Workspace worden uitgesloten, worden opgenomen in gegevensfeeds. Overweeg de volgende voorwaarden aan uw vragen toe te voegen als zij relevant zijn:
>
>* **`exclude_hit`**: Analysis Workspace bevat alleen gegevens waarbij `exclude_hit = 0` wordt gebruikt.
>* **`customer_perspective`**: Analysis Workspace bevat alleen gegevens waar `customer_perspective = 0` voorkomt, tenzij u een virtuele rapportsuite gebruikt die raakt op de mobiele achtergrond.
>* **`hit_source`**: gegevens uit gegevensbronnen kunnen verschillen bevatten tussen onbewerkte gegevens en Analysis Workspace. Als u hits van gegevensbronnen wilt uitsluiten, sluit u alle rijen uit waarin `hit_source = 5,7,8,9` voorkomt.

## Paginaweergaven

1. Telt het aantal rijen waar een waarde in `post_pagename` of `post_page_url` staat.

## Voorvallen

1. Telt het totale aantal rijen.

## Bezoeken

1. Samenvoegen `post_visid_high`, `post_visid_low`, `visit_num` en `visit_start_time_gmt` .
1. Telt het unieke aantal waarden.

>[!TIP]
>
>Onregelmatigheden op internet, systeemonregelmatigheden of het gebruik van aangepaste bezoeker-id&#39;s kunnen zelden dezelfde `visit_num` -waarden gebruiken voor verschillende bezoeken. Gebruik, hoewel optioneel, `visit_start_time_gmt` bij het tellen van bezoeken om ervoor te zorgen dat deze bezoeken worden geteld.

## Bezoekers

Alle methoden die Adobe gebruikt om unieke bezoekers te identificeren (aangepaste bezoeker-id, Experience Cloud ID-service, enz.) worden uiteindelijk allemaal berekend als een waarde in `post_visid_high` en `post_visid_low` . De samenvoeging van deze twee kolommen kan worden gebruikt als standaard voor het identificeren van unieke bezoekers, ongeacht hoe zij als unieke bezoeker zijn geïdentificeerd. Als u wilt weten welke methode Adobe heeft gebruikt om een unieke bezoeker te identificeren, gebruikt u de kolom `post_visid_type` .

1. Samenvoegen `post_visid_high` en `post_visid_low` .
2. Telt het unieke aantal waarden.

## Koppelingen aanpassen, downloaden of afsluiten

1. Telt het aantal rijen waarin:
   * `post_page_event = 100` voor aangepaste koppelingen
   * `post_page_event = 101` voor downloadkoppelingen
   * `post_page_event = 102` voor afsluitkoppelingen

## Aangepaste gebeurtenissen

Alle metriek worden in de kolom `post_event_list` geteld als door komma&#39;s gescheiden gehele getallen. Gebruik `event.tsv` om numerieke waarden te laten overeenkomen met de gewenste gebeurtenis. `post_event_list = 1,200` geeft bijvoorbeeld aan dat de hit een aankoopgebeurtenis en een aangepaste gebeurtenis 1 bevatte.

1. Telt het aantal keren dat de opzoekwaarde van de gebeurtenis in `post_event_list` wordt weergegeven.

## Tijd besteed

De bezoekers moeten eerst per bezoek worden gegroepeerd en vervolgens worden besteld op basis van het nummer van de treffer tijdens het bezoek.

1. Samenvoegen `post_visid_high`, `post_visid_low`, `visit_num` en `visit_start_time_gmt` .
2. Sorteer op deze samengevoegde waarde en pas vervolgens een secundaire sortering op `visit_page_num` toe.
3. Als een treffer niet de laatste in een bezoek is, trekt u de `post_cust_hit_time` -waarde van de `post_cust_hit_time` -waarde van de volgende treffer af.
4. Dit getal is de hoeveelheid tijd (in seconden) die voor de treffer is doorgebracht. Filters kunnen worden toegepast om de focus op dimensiepunten of gebeurtenissen te verplaatsen.

## Orders, eenheden en inkomsten

Als de `currency` -waarde van een hit niet overeenkomt met de valuta van een rapportsuite, wordt deze omgezet met de conversiekoers van die dag. De kolom `post_product_list` gebruikt de omgezette valutawaarde, zodat alle treffers dezelfde valuta in deze kolom gebruiken.

1. Sluit alle rijen waar `duplicate_purchase = 1` staat uit.
2. Neem alleen rijen op waarin `event_list` de aankoopgebeurtenis bevat.
3. Analyseer de kolom `post_product_list` om alle prijsgegevens te extraheren. De kolom `post_product_list` heeft dezelfde opmaak als de variabele `s.products` .
4. Bereken de gewenste metrische waarde:
   * Aantal rijen tellen om Orden te berekenen
   * Som het aantal `quantity` in de productreeks om Eenheden te berekenen
   * Som het aantal `price` in de productreeks om opbrengst te berekenen
