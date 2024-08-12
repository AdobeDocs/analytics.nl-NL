---
title: Unieke apparaten
description: Het aantal unieke apparaten.
feature: Metrics
exl-id: fa5c860f-bea7-4d03-9632-fa6e025647bf
source-git-commit: 16a9c9a2b6692b9b1944cfdb9b5b0411d48db666
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Unieke apparaten

De &quot;Unieke apparaten&#39; [ metrische ](overview.md) is metrische a [ dwars-apparaat analyse ](../cda/overview.md) die het aantal unieke niet geïdentificeerde apparaten en unieke virtuele apparaten telt. Niet-geïdentificeerde apparaten zijn apparaten die anonieme hits hebben gegenereerd. Unieke virtuele apparaten zijn verschillende personen die per apparaat worden geïdentificeerd.

## Hoe deze metrische waarde wordt berekend

Voor elk apparaat, som alle verschillende mensen verbonden aan het (met inbegrip van anoniem als het apparaat niet-gestippelde klappen bevat).

Merk op dat dit metrisch niet aan [ Unieke Bezoekers ](unique-visitors.md) in niet-CDA rapportsuites gelijk is. Een apparaat wordt bijvoorbeeld gedeeld door drie verschillende accounts. Als alle drie accounts uw site in een rapportagevenster bezoeken, worden in het resulterende rapport drie unieke apparaten in CDA weergegeven. Dezelfde gegevens buiten de CDA zouden 1 Unieke Bezoeker tonen.

## Voorbeeld

1. Sally arrives to your site by phone through an advertence, but is not registered in.
1. Sally wil een aankoop doen, maar wil dit liever doen op de familiecomputer omdat ze daar al is aangemeld. Op de gezinscomputer koopt ze.
1. De volgende dag controleert ze haar bestelling op haar telefoon en verifieert ze daar.
1. De vrouw van Bob, Alice, bladert door uw site terwijl u zich aanmeldt bij haar account op de familiecomputer.
1. De broer van Bob, Charles, bladert ook door uw site terwijl hij zich bij zijn account op de familiecomputer heeft aangemeld.

![ de Unieke Telling van Apparaten ](/help/components/metrics/assets/Unique_Devices_Count.png)

Het bekijken van dit gegeven in een CDA virtuele rapportreeks alvorens [ Replay ](/help/components/cda/replay.md) potentieel stitches unauthenticated klappen zouden tonen:

* **5 unieke apparaten**: 1 voor niet voor authentiek verklaard Loodje + 2 voor Loodje + 1 voor Alice + 1 voor Charles
* **4 [ Mensen](people.md)**: 1 [ Niet geïdentificeerde Mensen ](unidentified-people.md) + 3 [ Geïdentificeerde Mensen ](identified-people.md).
