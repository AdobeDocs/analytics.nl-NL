---
title: Plaatsen
description: De stad waar de treffer vandaan kwam.
feature: Dimensions
exl-id: c04525bb-50d6-4d28-b5dc-335d089e184b
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Plaatsen

De dimensie &#39;Steden&#39; meldt de stad waar de aanslag vandaan komt. Deze dimensie is handig om te bepalen van waaruit de populairste bezoekers van steden afkomstig zijn wanneer ze uw site bezoeken. U kunt deze gegevens gebruiken om de aandacht te richten op lokale reclame in deze steden, zoals billboards of reclamespots.

## Deze dimensie vullen met gegevens

Deze afmeting verwijst raadplegingsregels intern aan Adobe. De raadplegingswaarde is gebaseerd op het IP adres dat met de klap wordt verzonden. Adobe partners met [Digitaal element](https://www.digitalelement.com/) om raadplegingen tussen IP adres en stad te handhaven. Deze dimensie werkt uit de doos voor alle implementaties.

## Dimension-items

Dimension-objecten omvatten steden over de hele wereld. Voorbeelden van waarden zijn `"New York (New York, United States)"`, `"Bangalore (Karnataka, India)"`, of `"London (London, United Kingdom)"`.

Sommige dimensie-items kunnen `"AOL"`, een inbelverbinding voor internetservices. Abonnees op deze service krijgen een toegangspunt toegewezen op basis van het land waar hun accountnummer is gevestigd. De gebruikers van AOL gebruiken het IP adres van dit toegangspunt. Aangezien deze afmeting op IP adres gebaseerd is, wordt de geolocatie van het toegangspunt gebruikt in plaats van de daadwerkelijke plaats van de bezoeker.

## Verschillen tussen gerapporteerde en werkelijke locatie

Aangezien deze dimensie op IP adres gebaseerd is, kunnen sommige scenario&#39;s een verschil tussen gemelde plaats en daadwerkelijke plaats tonen:

* **IP adressen die collectieve volmachten vertegenwoordigen**: Deze bezoekers kunnen als verkeer verschijnen dat door het collectieve netwerk van de gebruiker komt, dat een verschillende plaats kan zijn als de gebruiker ver werkt.
* **Mobiele IP-adressen**: Het mobiele IP richten werkt op variërende niveaus afhankelijk van de plaats en het netwerk. Een aantal vervoerders backhaul IP verkeer door gecentraliseerde of regionale plaatsen van aanwezigheid.
* **ISP-gebruikers satelliet**: Het is moeilijk de specifieke locatie van deze gebruikers te identificeren, omdat ze doorgaans van de opstraallocatie afkomstig lijken te zijn.
* **IP&#39;s van militaire en overheidsinstellingen**: Vertegenwoordigt personeel dat over de hele wereld reist en door hun huisplaats ingaat, eerder dan de basis of het bureau waar zij momenteel zijn gestationeerd.
