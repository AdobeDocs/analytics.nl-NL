---
title: US DMA
description: Het aangewezen marktgebied van de hit.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---


# US DMA

De dimensie &quot;DMA van de VS&quot; rapporteert het aangewezen marktgebied (DMA) van de bezoeker. Het is gebaseerd op de mediamarkten die door [Nielsen](https://www.nielsen.com/us/en/intl-campaigns/dma-maps/)zijn samengesteld.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar interne opzoekregels van Adobe. De raadplegingswaarde is gebaseerd op het IP adres dat met de klap wordt verzonden. Adobe werkt samen met Nielsen om raadplegingen tussen IP adres en DMA te handhaven. Deze dimensie werkt uit de doos voor alle implementaties.

>[!TIP]
>
>Als uw organisatie strenge privacyverordeningen volgt waar het [verduisteren van IP adres](/help/admin/admin/general-acct-settings-admin.md) niet genoeg is, kunt u verzoeken om geolocatiegegevens volledig onbruikbaar te maken. Neem contact op met de klantenservice met de id van de rapportsuite en verzoek &#39;Geography&#39; uit te schakelen voor de rapportsuite.

## Dimensiewaarden

Dimensiewaarden zijn onder andere de DMA- en DMA-code van de bezoeker. De 3-cijfercode is geen postcode, maar de DMA-code van Nielsen. Voorbeelden hiervan zijn `"Dallas-Ft. Worth (623)"`, `"New York (501)"`of `"Los Angeles (803)"`. De waarde van de dimensie `"No Metro (0)"` omvat al internationaal verkeer buiten de Verenigde Staten.

## Verschillen tussen gerapporteerde en werkelijke locatie

Aangezien deze dimensie op IP adres gebaseerd is, kunnen sommige scenario&#39;s een verschil tussen gemelde plaats en daadwerkelijke plaats tonen:

* **IP adressen die collectieve volmachten** vertegenwoordigen: Deze bezoekers kunnen als verkeer verschijnen dat door het collectieve netwerk van de gebruiker komt, dat een verschillende plaats kan zijn als de gebruiker ver werkt.
* **Mobiele IP-adressen**: Het mobiele IP richten werkt op variërende niveaus afhankelijk van de plaats en het netwerk. Een aantal vervoerders backhaul IP verkeer door gecentraliseerde of regionale plaatsen van aanwezigheid.
* **ISP-gebruikers** satelliet: Het is moeilijk de specifieke locatie van deze gebruikers te identificeren, omdat ze doorgaans van de opstraallocatie afkomstig lijken te zijn.
* **IP&#39;s van militaire en overheidsinstellingen**: Vertegenwoordigt personeel dat over de hele wereld reist en door hun huisplaats ingaat, eerder dan de basis of het bureau waar zij momenteel zijn gestationeerd.
