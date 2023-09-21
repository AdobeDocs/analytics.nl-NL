---
title: US DMA
description: Het aangewezen marktgebied van de hit.
feature: Dimensions
exl-id: 156d5755-2e93-4240-bde3-1d537422b7bf
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# US DMA

De &#39;US DMA&#39; [dimensie](overview.md) meldt het aangewezen marktgebied (DMA) van de bezoeker. Het is gebaseerd op mediamarkten die zijn samengesteld door [Nielsen](https://markets.nielsen.com/us/en/contact-us/intl-campaigns/dma-maps/).

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar raadplegingsregels intern aan Adobe. De raadplegingswaarde is gebaseerd op het IP adres dat met de klap wordt verzonden. De partners van de Adobe met Nielsen om raadplegingen tussen IP adres en DMA te handhaven. Deze dimensie werkt uit de doos voor alle implementaties.

## Dimension-items

Items van het Dimension zijn onder andere de DMA- en DMA-code van de bezoeker. De 3-cijfercode is geen postcode, maar de DMA-code van Nielsen. Voorbeelden van waarden zijn `"Dallas-Ft. Worth (623)"`, `"New York (501)"`, of `"Los Angeles (803)"`. Dimensie-item `"No Metro (0)"` omvat het gehele internationale verkeer buiten de Verenigde Staten.

## Verschillen tussen gerapporteerde en werkelijke locatie

Aangezien deze dimensie op IP adres gebaseerd is, kunnen sommige scenario&#39;s een verschil tussen gemelde plaats en daadwerkelijke plaats tonen:

* **IP adressen die collectieve volmachten vertegenwoordigen**: Deze bezoekers kunnen als verkeer verschijnen dat door het collectieve netwerk van de gebruiker komt, dat een verschillende plaats kan zijn als de gebruiker ver werkt.
* **Mobiele IP-adressen**: Mobiele IP die werken richt op variërende niveaus afhankelijk van de plaats en het netwerk. Een aantal vervoerders backhaul IP verkeer door gecentraliseerde of regionale plaatsen van aanwezigheid.
* **ISP-gebruikers satelliet**: Het is moeilijk de specifieke locatie van deze gebruikers te identificeren, omdat ze doorgaans van de opstraallocatie afkomstig lijken te zijn.
* **IP&#39;s van militaire en overheidsinstellingen**: Vertegenwoordigt personeel dat over de hele wereld reist en door hun thuislocatie komt, in plaats van de basis of het kantoor waar zij momenteel zijn gestationeerd.
* **Proxy&#39;s die IP-adressen om privacyredenen verbergen**: De diensten zoals het Privé Relais van Apple verbergen het ware IP adres door gegevens door een tussenpersoon of een volmacht willekeurig te verzenden. Deze volmacht vervangt dan een verschillend IP adres alvorens aan Adobe door:sturen.
