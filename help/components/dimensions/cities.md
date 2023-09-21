---
title: Plaatsen
description: De stad waar de treffer vandaan kwam.
feature: Dimensions
exl-id: c04525bb-50d6-4d28-b5dc-335d089e184b
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---

# Plaatsen

De steden [dimensie](overview.md) meldt de stad waar de treffer vandaan komt . Deze dimensie is handig om te bepalen van waaruit de populairste bezoekers van steden afkomstig zijn wanneer ze uw site bezoeken. U kunt deze gegevens gebruiken om de aandacht te richten op lokale reclame in deze steden, zoals billboards of reclamespots.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar raadplegingsregels intern aan Adobe. De raadplegingswaarde is gebaseerd op het IP adres dat met de klap wordt verzonden. Adobe partners met [Digitaal element](https://www.digitalelement.com/) om raadplegingen tussen IP adres en stad te handhaven. Deze dimensie werkt uit de doos voor alle implementaties.

## Dimension-items

Dimension-items omvatten steden over de hele wereld. Voorbeelden van waarden zijn `"New York (New York, United States)"`, `"Bangalore (Karnataka, India)"`, of `"London (London, United Kingdom)"`.

Sommige dimensie-items kunnen `"AOL"`, een inbelverbinding voor internetservices. Abonnees op deze service krijgen een toegangspunt toegewezen op basis van het land waar hun accountnummer is gevestigd. De gebruikers van AOL gebruiken het IP adres van dit toegangspunt. Aangezien deze afmeting op IP adres gebaseerd is, wordt de geolocatie van het toegangspunt gebruikt in plaats van de daadwerkelijke plaats van de bezoeker.

## Verschillen tussen gerapporteerde en werkelijke locatie

Aangezien deze dimensie op IP adres gebaseerd is, kunnen sommige scenario&#39;s een verschil tussen gemelde plaats en daadwerkelijke plaats tonen:

* **IP adressen die collectieve volmachten vertegenwoordigen**: Deze bezoekers kunnen als verkeer verschijnen dat door het collectieve netwerk van de gebruiker komt, dat een verschillende plaats kan zijn als de gebruiker ver werkt.
* **Mobiele IP-adressen**: Mobiele IP die werken richt op variërende niveaus afhankelijk van de plaats en het netwerk. Een aantal vervoerders backhaul IP verkeer door gecentraliseerde of regionale plaatsen van aanwezigheid.
* **ISP-gebruikers satelliet**: Het is moeilijk de specifieke locatie van deze gebruikers te identificeren, omdat ze doorgaans van de opstraallocatie afkomstig lijken te zijn.
* **IP&#39;s van militaire en overheidsinstellingen**: Vertegenwoordigt personeel dat over de hele wereld reist en door hun thuislocatie komt, in plaats van de basis of het kantoor waar zij momenteel zijn gestationeerd.
* **Proxy&#39;s die IP-adressen om privacyredenen verbergen**: De diensten zoals het Privé Relais van Apple verbergen het ware IP adres door gegevens door een tussenpersoon of een volmacht willekeurig te verzenden. Deze volmacht vervangt dan een verschillend IP adres alvorens aan Adobe door:sturen.
