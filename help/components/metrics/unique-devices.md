---
title: Unieke apparaten
description: Het aantal unieke apparaten.
feature: Metrics
exl-id: fa5c860f-bea7-4d03-9632-fa6e025647bf
source-git-commit: 7d5383e1ee3bee189d3dd48bc6b899f4108f7ba8
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# Unieke apparaten

De metrische waarde &#39;Unieke apparaten&#39; is een [Apparaatanalyse](../cda/overview.md) metrisch die het aantal unieke niet-geïdentificeerde apparaten en unieke virtuele apparaten telt. Niet-geïdentificeerde apparaten zijn apparaten die anonieme hits hebben gegenereerd. Unieke virtuele apparaten zijn verschillende personen die per apparaat worden geïdentificeerd.

## Hoe deze metrische waarde wordt berekend

Voor elk apparaat, som alle verschillende mensen verbonden aan het (met inbegrip van anoniem als het apparaat niet-gestippelde klappen bevat).

Deze metrische waarde is niet gelijk aan [Unieke bezoekers](unique-visitors.md) in niet-CDA-rapportensuites. Een apparaat wordt bijvoorbeeld gedeeld door drie verschillende accounts. Als alle drie accounts uw site in een rapportagevenster bezoeken, wordt in het resulterende rapport 3 Unique Devices in CDA weergegeven. Dezelfde gegevens buiten de CDA zouden 1 Unieke Bezoeker tonen.

## Voorbeeld

1. Sally komt aan uw plaats op zijn telefoon door een advertentie aan, maar het programma wordt niet geopend.
1. Sally wil een aankoop doen, maar wil dit liever doen op de familiecomputer omdat ze daar al is aangemeld. Op de gezinscomputer koopt ze.
1. De volgende dag controleert ze zijn bestelling op zijn telefoon en verifieert ze daar.
1. De vrouw van Bob, Alice, bladert door uw site terwijl u zich aanmeldt bij haar account op de familiecomputer.
1. De broer van Bob, Charles, bladert ook door uw site terwijl hij zich bij zijn account op de familiecomputer heeft aangemeld.

![Aantal unieke apparaten](/help/components/metrics/assets/Unique_Devices_Count.png)

Deze gegevens weergeven in een virtuele CDA-rapportenpakket voordat [Opnieuw afspelen](/help/components/cda/replay.md) potentieel stitches unauthenticate hits zouden laten zien :

* **5 unieke apparaten**: 1 voor niet-geverifieerd Bob + 2 voor Bob + 1 voor Alice + 1 voor Charles
* **4 [Mensen](people.md)**: 1 [Niet-geïdentificeerde personen](unidentified-people.md) + 3 [Geïdentificeerde personen](identified-people.md).
