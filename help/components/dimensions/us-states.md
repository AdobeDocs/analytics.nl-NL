---
title: VS-staten
description: De Amerikaanse staat van de bezoeker.
feature: Dimensions
exl-id: d4506e59-c1ff-4348-912d-c1ad73278f56
source-git-commit: 146d622f370fd7469a8e5f0f2fe68cb31fa91844
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Amerikaanse staat

De dimensie &#39;Amerikaanse staat&#39; meldt de staat van de bezoeker in de Verenigde Staten van Amerika. Het lijkt op het [Regio&#39;s](regions.md) dimensie, behalve dat deze dimensie specifiek is voor de Verenigde Staten. Het gebruiken van deze dimensie is waardevol als u inzicht meer korrelig wilt dan [Landen](countries.md) maar niet zo korrelig als [Plaatsen](cities.md).

## Deze dimensie vullen met gegevens

Deze afmeting verwijst raadplegingsregels intern aan Adobe. De raadplegingswaarde is gebaseerd op het IP adres dat met de klap wordt verzonden. Adobe partners met [Digitaal element](https://www.digitalelement.com/) om raadplegingen tussen IP adres en land te handhaven. Deze dimensie werkt uit de doos voor alle implementaties.

## Dimension-items

Tot de Dimension-items behoren regio&#39;s en het land waarin de regio woont. Voorbeelden van waarden zijn `"California"`, `"Texas"`, of `"Virginia"`. Dimensie-item `"Unspecified"` omvat het gehele internationale verkeer buiten de Verenigde Staten.

Deze dimensie kan `"AOL"`, een inbelverbinding voor internetservices. De abonnees aan deze dienst worden toegewezen een toegangspunt. De gebruikers van AOL gebruiken het IP adres van dit toegangspunt. Aangezien deze afmeting op IP adres gebaseerd is, wordt de geolocatie van het toegangspunt gebruikt in plaats van de daadwerkelijke plaats van de bezoeker.

## Verschillen tussen gerapporteerde en werkelijke locatie

Aangezien deze dimensie op IP adres gebaseerd is, kunnen sommige scenario&#39;s een verschil tussen gemelde plaats en daadwerkelijke plaats tonen:

* **IP adressen die collectieve volmachten vertegenwoordigen**: Deze bezoekers kunnen als verkeer verschijnen dat door het collectieve netwerk van de gebruiker komt, dat een verschillende plaats kan zijn als de gebruiker ver werkt.
* **Mobiele IP-adressen**: Het mobiele IP richten werkt op variërende niveaus afhankelijk van de plaats en het netwerk. Een aantal vervoerders backhaul IP verkeer door gecentraliseerde of regionale plaatsen van aanwezigheid.
* **ISP-gebruikers satelliet**: Het is moeilijk de specifieke locatie van deze gebruikers te identificeren, omdat ze doorgaans van de opstraallocatie afkomstig lijken te zijn.
* **IP&#39;s van militaire en overheidsinstellingen**: Vertegenwoordigt personeel dat over de hele wereld reist en door hun huisplaats ingaat, eerder dan de basis of het bureau waar zij momenteel zijn gestationeerd.
* **Proxy&#39;s die IP-adressen om privacyredenen verbergen**: De diensten zoals het Privé Relais van Apple verbergen het ware IP adres door gegevens door een tussenpersoon of een volmacht willekeurig te verzenden. Deze volmacht vervangt dan een verschillend IP adres alvorens aan Adobe door:sturen.
