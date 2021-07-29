---
title: purchaseID
description: Gededupliceerde hits op basis van een unieke aankoop-id.
exl-id: 7a4d7f08-65ae-4541-a94e-cc6c445c01db
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# purchaseID

Met de variabele `purchaseID` voorkomt u dat hits met dezelfde aankoop rapporten opblazen. Als een bezoeker bijvoorbeeld de pagina bereikt waarop uw aankoop wordt bevestigd, verzendt u doorgaans gegevens over de opbrengsten van de transactie naar Adobe. Als de gebruiker deze pagina meerdere keren vernieuwt of als bladwijzers op de pagina worden weergegeven om later te bezoeken, kunnen deze controles rapporten opblazen. De variabele `purchaseID` dedupliceert metriek wanneer meer dan één klap zelfde aankoop identiteitskaart heeft

Wanneer Adobe een hit herkent als een dubbele aankoop, worden alle conversiegegevens (zoals eVars en gebeurtenissen) niet weergegeven in de rapportage. In gegevensfeeds wordt de kolom `duplicate_purchase` ingesteld op `1`.

De aankoop-id&#39;s gelden voor alle bezoekers en verlopen niet. Als een bezoeker een bepaalde aankoop-id instelt, stelt een andere bezoeker die aankoop-id een jaar later in, dan wordt de tweede aankoop gedupliceerd.

## ID aanschaffen met tags in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.purchaseID in AppMeasurement en aangepaste code-editor

De variabele `s.purchaseID` is een tekenreeks die een unieke id voor een aankoop bevat. Deze wordt ingesteld op hetzelfde resultaat als een aankoopgebeurtenis. Gebruik alleen alfanumerieke tekens om deze variabele te vullen.

Deze variabele kan maximaal 20 bytes opslaan; waarden langer dan 20 bytes zijn afgebroken. Als deze ingekorte waarde overeenkomt met de volgende ingekorte waarden, worden deze volgende treffers gededupliceerd.

```js
s.purchaseID = "ABC123";
```

Bij gebruik van de `digitalData` [gegevenslaag](../../prepare/data-layer.md):

```js
s.purchaseID = digitalData.transaction.transactionID;
```

>[!CAUTION]
>
>Gebruik geen randomisatiefunctie om een aankoop-id te genereren.
