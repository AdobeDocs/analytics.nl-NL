---
title: purchaseID
description: Gededupliceerde hits op basis van een unieke aankoop-id.
feature: Variables
exl-id: 7a4d7f08-65ae-4541-a94e-cc6c445c01db
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# purchaseID

De `purchaseID` variabele helpt voorkomen dat hits met dezelfde aankoop rapporten opblazen. Als een bezoeker bijvoorbeeld de pagina bereikt waarop uw aankoop wordt bevestigd, verzendt u doorgaans gegevens over de opbrengsten van de transactie naar Adobe. Als de gebruiker deze pagina meerdere keren vernieuwt of als bladwijzers op de pagina worden weergegeven om later te bezoeken, kunnen deze controles rapporten opblazen. De `purchaseID` variabele de-dupliceert metriek wanneer meer dan één klap de zelfde aankoop ID heeft.

Wanneer Adobe een hit herkent als een dubbele aankoop, worden alle conversiegegevens (zoals eVars en gebeurtenissen) niet weergegeven in de rapportage. In gegevensfeeds wordt de `duplicate_purchase` kolom is ingesteld op `1`.

De aankoop-id&#39;s gelden voor alle bezoekers en verlopen niet. Als een bezoeker een bepaalde aankoop-id instelt, stelt een andere bezoeker die aankoop-id een jaar later in, dan wordt de tweede aankoop gedupliceerd.

## Aankoop-id met de web SDK

Aankoop-id is [toegewezen voor Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) onder het XDM-veld `commerce.order.purchaseID`.

## Aankoop-id met Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.purchaseID in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De `s.purchaseID` variable is a string that contains a unique identifier to a purchase. Deze wordt ingesteld op hetzelfde resultaat als een aankoopgebeurtenis. Gebruik alleen alfanumerieke tekens om deze variabele te vullen.

Deze variabele kan maximaal 20 bytes opslaan; waarden langer dan 20 bytes zijn afgebroken. Als deze ingekorte waarde overeenkomt met de volgende ingekorte waarden, worden deze volgende treffers gededupliceerd.

```js
s.purchaseID = "ABC123";
```

Als u de `digitalData` [gegevenslaag](../../prepare/data-layer.md):

```js
s.purchaseID = digitalData.transaction.transactionID;
```

>[!CAUTION]
>
>Gebruik geen randomisatiefunctie om een aankoop-id te genereren.
