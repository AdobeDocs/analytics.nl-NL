---
title: US DMA
description: Het aangewezen marktgebied van de hit.
exl-id: 156d5755-2e93-4240-bde3-1d537422b7bf
source-git-commit: 9770f8e04089ff339d912d1787679257c87c7caa
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# US DMA

De dimensie &quot;DMA van de VS&quot; rapporteert het aangewezen marktgebied (DMA) van de bezoeker. Het is gebaseerd op mediamarkten gecompileerd door [Nielsen](https://www.nielsen.com/us/en/intl-campaigns/dma-maps/).

## Deze dimensie vullen met gegevens

Deze afmeting verwijst raadplegingsregels intern aan Adobe. De raadplegingswaarde is gebaseerd op het IP adres dat met de klap wordt verzonden. Adobe partners met Nielsen om raadplegingen tussen IP adres en DMA te handhaven. Deze dimensie werkt uit de doos voor alle implementaties.

## Dimension-items

Dimension-items omvatten de DMA- en DMA-code van de bezoeker. De 3-cijfercode is geen postcode, maar de DMA-code van Nielsen. Voorbeelden van waarden zijn `"Dallas-Ft. Worth (623)"`, `"New York (501)"` of `"Los Angeles (803)"`. Het dimensie-item `"No Metro (0)"` omvat alle internationale verkeer buiten de Verenigde Staten.

## Verschillen tussen gerapporteerde en werkelijke locatie

Aangezien deze dimensie op IP adres gebaseerd is, kunnen sommige scenario&#39;s een verschil tussen gemelde plaats en daadwerkelijke plaats tonen:

* **IP adressen die collectieve volmachten** vertegenwoordigen: Deze bezoekers kunnen als verkeer verschijnen dat door het collectieve netwerk van de gebruiker komt, dat een verschillende plaats kan zijn als de gebruiker ver werkt.
* **Mobiele IP-adressen**: Het mobiele IP richten werkt op variërende niveaus afhankelijk van de plaats en het netwerk. Een aantal vervoerders backhaul IP verkeer door gecentraliseerde of regionale plaatsen van aanwezigheid.
* **ISP-gebruikers** satelliet: Het is moeilijk de specifieke locatie van deze gebruikers te identificeren, omdat ze doorgaans van de opstraallocatie afkomstig lijken te zijn.
* **IP&#39;s van militaire en overheidsinstellingen**: Vertegenwoordigt personeel dat over de hele wereld reist en door hun huisplaats ingaat, eerder dan de basis of het bureau waar zij momenteel zijn gestationeerd.
