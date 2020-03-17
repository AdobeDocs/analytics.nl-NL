---
title: purchaseID
description: Gededupliceerde hits op basis van een unieke aankoop-id.
translation-type: tm+mt
source-git-commit: c7d596be4f70c820039725be6a5fddc8572156d9

---


# purchaseID

Met de `purchaseID` variabele voorkomt u dat hits met dezelfde aankoop rapporten opblazen. Als een bezoeker bijvoorbeeld de pagina bereikt waarop uw aankoop wordt bevestigd, verzendt u doorgaans gegevens over de opbrengsten van de transactie naar Adobe. Als de gebruiker deze pagina meerdere keren vernieuwt of als bladwijzers op de pagina worden weergegeven om later te bezoeken, kunnen deze controles rapporten opblazen. De `purchaseID` variabele dedupliceert metriek wanneer meer dan één klap de zelfde aankoop ID heeft.

Wanneer Adobe een hit herkent als een dubbele aankoop, worden niet alle conversiegegevens (zoals eVars en gebeurtenissen) weergegeven in de rapportage. In gegevensfeeds wordt de `duplicate_purchase` kolom ingesteld op `1`.

De aankoop-id&#39;s gelden voor alle bezoekers en verlopen niet. Als een bezoeker een bepaalde aankoop-id instelt, stelt een andere bezoeker die aankoop-id een jaar later in, dan wordt de tweede aankoop gedupliceerd.

## Aankoop-id in Adobe Experience Platform Starten

Er is geen specifiek veld in Launch om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.purchaseID in AppMeasurement en Launch, aangepaste code-editor

De `s.purchaseID` variabele is een tekenreeks die een unieke id voor een aankoop bevat. Deze wordt ingesteld op hetzelfde resultaat als een aankoopgebeurtenis. Gebruik alleen alfanumerieke tekens om deze variabele te vullen.

Deze variabele kan maximaal 20 bytes opslaan; waarden langer dan 20 bytes zijn afgebroken. Als deze ingekorte waarde overeenkomt met de volgende ingekorte waarden, worden deze volgende treffers gededupliceerd.

```js
s.purchaseID = "ABC123";
```

> [!NOTE] Gebruik geen randomisatiefunctie om een aankoop-id te genereren. Adobe raadt u aan een [gegevenslaag](../../prepare/data-layer.md) te gebruiken om een bepaalde aankoop-id op te slaan.
