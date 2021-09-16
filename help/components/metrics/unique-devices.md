---
title: Unieke apparaten
description: Het aantal unieke apparaten.
exl-id: fa5c860f-bea7-4d03-9632-fa6e025647bf
source-git-commit: 407111f6016fe8595f1d5c3464e36dfd4d314630
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# Unieke apparaten

De metrische waarde &#39;Unieke apparaten&#39; is een [Analyse van verschillende apparaten](../cda/overview.md) die het aantal unieke, niet-geïdentificeerde apparaten en unieke virtuele apparaten telt. Niet-geïdentificeerde apparaten zijn apparaten die anonieme hits hebben gegenereerd. Unieke virtuele apparaten zijn verschillende personen die per apparaat worden geïdentificeerd.

## Hoe deze metrische waarde wordt berekend

Voor elk apparaat, som alle verschillende mensen verbonden aan het (met inbegrip van anoniem als het apparaat niet-gestippelde klappen bevat).

Merk op dat deze metrische waarde niet aan [Unieke Bezoekers](unique-visitors.md) in niet-CDA rapportreeksen gelijk is. Een apparaat wordt bijvoorbeeld gedeeld door drie verschillende accounts. Als alle drie accounts uw site in een rapportagevenster bezoeken, wordt in het resulterende rapport 3 Unique Devices in CDA weergegeven. Dezelfde gegevens buiten de CDA zouden 1 Unieke Bezoeker tonen.

## Voorbeeld

1. Bob arriveert via een advertentie naar uw site op zijn telefoon, maar is niet aangemeld.
1. Bob wil een aankoop doen, maar wil dit liever doen op de familiecomputer omdat hij daar al is aangemeld. Op de gezinscomputer koopt hij.
1. De volgende dag controleert hij zijn bestelling aan zijn telefoon en verifieert hij daar.
1. De vrouw van Bob, Alice, bladert door uw site terwijl u zich aanmeldt bij haar account op de familiecomputer.
1. De broer van Bob, Charles, bladert ook door uw site terwijl hij zich bij zijn account op de familiecomputer heeft aangemeld.

![Aantal unieke apparaten](/help/components/metrics/assets/Unique_Devices_Count.png)

Het bekijken van deze gegevens in een virtuele CDA rapportreeks alvorens [Replay](/help/components/cda/replay.md) zou tonen:

* **5 unieke apparaten**: 1 voor niet-geverifieerd Bob + 2 voor Bob + 1 voor Alice + 1 voor Charles
* **4  [Personen](people.md)**: 1  [Niet-geïdentificeerde personen](unidentified-people.md) + 3  [geïdentificeerde personen](identified-people.md).

