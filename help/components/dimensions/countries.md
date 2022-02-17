---
title: Landen
description: Het land waar de treffer vandaan kwam.
feature: Dimensions
exl-id: 47704b08-215d-4d2d-bcd4-1789e308c1c6
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---

# Landen

De dimensie &#39;Landen&#39; meldt het land waar de slachtoffers vandaan komen. Deze dimensie is handig om te bepalen uit welke populairste landen bezoekers uw site bezoeken. U kunt deze gegevens gebruiken om u te concentreren op marketingactiviteiten in deze landen, of ervoor te zorgen dat uw site optimaal werkt in landen met verschillende primaire talen.

## Deze dimensie vullen met gegevens

Deze afmeting verwijst raadplegingsregels intern aan Adobe. De raadplegingswaarde is gebaseerd op het IP adres dat met de klap wordt verzonden. Adobe partners met [Digitaal element](https://www.digitalelement.com/) om raadplegingen tussen IP adres en land te handhaven. Deze dimensie werkt uit de doos voor alle implementaties.

## Dimension-items

Dimension-objecten omvatten landen over de hele wereld. Voorbeelden van waarden zijn `"United States"`, `"United Kingdom"`, of `"India"`.

## Verschillen tussen gerapporteerde en werkelijke locatie

Aangezien deze dimensie op IP adres gebaseerd is, kunnen sommige scenario&#39;s een verschil tussen gemelde plaats en daadwerkelijke plaats tonen:

* **IP adressen die collectieve volmachten vertegenwoordigen**: Deze bezoekers kunnen als verkeer verschijnen dat door het collectieve netwerk van de gebruiker komt, dat een verschillende plaats kan zijn als de gebruiker ver werkt.
* **Mobiele IP-adressen**: Het mobiele IP richten werkt op variërende niveaus afhankelijk van de plaats en het netwerk. Een aantal vervoerders backhaul IP verkeer door gecentraliseerde of regionale plaatsen van aanwezigheid.
* **ISP-gebruikers satelliet**: Het is moeilijk de specifieke locatie van deze gebruikers te identificeren, omdat ze doorgaans van de opstraallocatie afkomstig lijken te zijn.
* **IP&#39;s van militaire en overheidsinstellingen**: Vertegenwoordigt personeel dat over de hele wereld reist en door hun huisplaats ingaat, eerder dan de basis of het bureau waar zij momenteel zijn gestationeerd.
