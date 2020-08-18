---
title: Regio's
description: De geografische regio van de bezoeker.
translation-type: tm+mt
source-git-commit: fdc77997c8aea07cc7db1d06c5c0c2cd2f2abbd9
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---


# Regio&#39;s

De dimensie &quot;Regio&#39;s&quot; rapporteert de geografische regio van de bezoeker. Het is een geografisch gebied dat kleiner is dan een land, maar groter dan een stad. In sommige landen is een regio een staat, provincie of prefectuur. In andere gebieden is het een deelland, afdeling of metropolitane regio. Het gebruik van deze dimensie is waardevol als u meer inzicht wilt dan [landen](countries.md) maar niet zo korrelig als [steden](cities.md).

## Deze dimensie vullen met gegevens

Deze afmeting verwijst raadplegingsregels intern aan Adobe. De raadplegingswaarde is gebaseerd op het IP adres dat met de klap wordt verzonden. Adobe werkt met [Digitaal Element](https://www.digitalelement.com/) samen om raadplegingen tussen IP adres en land te handhaven. Deze dimensie werkt uit de doos voor alle implementaties.

>[!TIP]
>
>Als uw organisatie strenge privacyverordeningen volgt waar het [verduisteren van IP adres](/help/admin/admin/general-acct-settings-admin.md) niet genoeg is, kunt u verzoeken om geolocatiegegevens volledig onbruikbaar te maken. Neem contact op met de klantenservice met de id van de rapportsuite en verzoek &#39;Geography&#39; uit te schakelen voor de rapportsuite.

## Dimension-items

Tot de Dimension-items behoren regio&#39;s en het land waarin de regio woont. Voorbeelden hiervan zijn `"California (United States)"`, `"Tokyo (Japan)"`of `"Sao Paulo (Brazil)"`.

Sommige dimensie-items kunnen `"AOL"`een inbelverbinding voor internetservices zijn. Abonnees op deze service krijgen een toegangspunt toegewezen op basis van het land waar hun accountnummer is gevestigd. De gebruikers van AOL gebruiken het IP adres van dit toegangspunt. Aangezien deze afmeting op IP adres gebaseerd is, wordt de geolocatie van het toegangspunt gebruikt in plaats van de daadwerkelijke plaats van de bezoeker.

## Verschillen tussen gerapporteerde en werkelijke locatie

Aangezien deze dimensie op IP adres gebaseerd is, kunnen sommige scenario&#39;s een verschil tussen gemelde plaats en daadwerkelijke plaats tonen:

* **IP adressen die collectieve volmachten** vertegenwoordigen: Deze bezoekers kunnen als verkeer verschijnen dat door het collectieve netwerk van de gebruiker komt, dat een verschillende plaats kan zijn als de gebruiker ver werkt.
* **Mobiele IP-adressen**: Het mobiele IP richten werkt op variërende niveaus afhankelijk van de plaats en het netwerk. Een aantal vervoerders backhaul IP verkeer door gecentraliseerde of regionale plaatsen van aanwezigheid.
* **ISP-gebruikers** satelliet: Het is moeilijk de specifieke locatie van deze gebruikers te identificeren, omdat ze doorgaans van de opstraallocatie afkomstig lijken te zijn.
* **IP&#39;s van militaire en overheidsinstellingen**: Vertegenwoordigt personeel dat over de hele wereld reist en door hun huisplaats ingaat, eerder dan de basis of het bureau waar zij momenteel zijn gestationeerd.
