---
description: Beschrijft hoe te om gemeenschappelijke metriek te berekenen gebruikend gegevensvoer.
keywords: Data Feed;job;metrics;pre column;post column;bots;date filtering;event string;common;formulas
title: Metrische gegevens berekenen
topic: Reports and analytics
uuid: a45ea5bb-7c83-468f-b94a-63add78931d7
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Gegevensfeeds gebruiken om algemene metriek te berekenen

Beschrijft hoe te om gemeenschappelijke metriek te berekenen gebruikend gegevensvoer.

> [!IMPORTANT] Deze normaal gesproken niet opgenomen in Adobe Analytics, worden opgenomen in gegevensfeeds. Gebruik deze optie `exclude_hit > 0` om uitgesloten hits te verwijderen van query&#39;s op onbewerkte gegevens. Gegevensbronnen worden ook opgenomen in gegevensfeeds. Als u gegevensbronnen wilt uitsluiten, sluit u alle rijen met `hit_source = 5,7,8,9`.

## Paginaweergaven

1. Telt het aantal rijen waarin een waarde zich bevindt `post_pagename` of `post_page_url`.

## Bezoeken

1. Samenvoegen `post_visid_high`, `post_visid_low`, `visit_num`en `visit_start_time_gmt`.
1. Telt het unieke aantal waarden.

> [!NOTE] Onregelmatigheden op internet, systeemonregelmatigheden of het gebruik van aangepaste bezoeker-id&#39;s kunnen zelden dezelfde `visit_num` waarden gebruiken voor verschillende bezoeken. Gebruik deze optie `visit_start_time_gmt` bij het tellen van bezoeken om ervoor te zorgen dat deze bezoeken worden geteld.

## Bezoekers

Alle methoden die Adobe gebruikt om unieke bezoekers te identificeren (aangepaste bezoeker-id, Experience Cloud ID-service, enz.) worden uiteindelijk allemaal berekend als een waarde in `post_visid_high` en `post_visid_low`. De samenvoeging van deze twee kolommen kan worden gebruikt als standaard voor het identificeren van unieke bezoekers, ongeacht hoe zij als unieke bezoeker zijn geïdentificeerd. Als u wilt weten welke methode Adobe heeft gebruikt om een unieke bezoeker te identificeren, gebruikt u de kolom `post_visid_type`.

1. Samenvoegen `post_visid_high` en `post_visid_low`.
2. Telt het unieke aantal waarden.

## Koppelingen aanpassen, downloaden of afsluiten

1. Telt het aantal rijen waarin:
   * `post_page_event = 100` voor aangepaste koppelingen
   * `post_page_event = 101` voor downloadkoppelingen
   * `post_page_event = 102` voor exit-koppelingen

## Aangepaste gebeurtenissen

Alle metriek worden in de `post_event_list` kolom geteld als door komma&#39;s gescheiden gehele getallen. Kies deze optie `event.tsv` om numerieke waarden te laten overeenkomen met de gewenste gebeurtenis. Hiermee wordt bijvoorbeeld `post_event_list = 1,200` aangegeven dat de hit een aankoopgebeurtenis en een aangepaste gebeurtenis 1 bevatte.

1. Telt het aantal keren dat de opzoekwaarde van de gebeurtenis wordt weergegeven `post_event_list`.

## Tijd besteed

De bezoekers moeten eerst per bezoek worden gegroepeerd en vervolgens worden besteld volgens het nummer van de treffer tijdens het bezoek.

1. Samenvoegen `post_visid_high`, `post_visid_low`, `visit_num`en `visit_start_time_gmt`.
2. Sorteer op deze samengevoegde waarde en pas vervolgens een secundaire sortering op toe `visit_page_num`.
3. Als een treffer niet de laatste in een bezoek is, trekt u de `post_cust_hit_time` waarde van de `post_cust_hit_time` waarde van de volgende treffer af.
4. Dit getal is de hoeveelheid tijd (in seconden) die voor de treffer is doorgebracht. U kunt filters toepassen om de focus op waarden of gebeurtenissen van dimensies te vestigen.

## Orders, eenheden en inkomsten

Als de `currency` waarde van een hit niet overeenkomt met de valuta van een rapportsuite, wordt deze geconverteerd met de conversiekoers van die dag. De kolom `post_product_list` gebruikt de omgezette valutawaarde, zodat gebruiken alle treffers de zelfde munt in deze kolom.

1. Sluit alle rijen waar `duplicate_purchase = 1`.
2. Neem alleen rijen op waarin de aankoopgebeurtenis `event_list` zich bevindt.
3. Parseer de `post_product_list` kolom om alle prijsgegevens te extraheren. De `post_product_list` kolom heeft dezelfde opmaak als de `s.products` variabele.
4. Bereken de gewenste metrische waarde:
   * Aantal rijen tellen om Orden te berekenen
   * Som het aantal `quantity` in de productreeks om Eenheden te berekenen
   * Som het aantal `price` in de productreeks om opbrengst te berekenen
