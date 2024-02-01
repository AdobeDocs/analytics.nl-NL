---
title: API voor data-invoer in bulk
description: BDIA (Bulk Data Insertion API) is een Adobe Analytics-functie waarmee u gegevens van serveroproepen in batches bestanden kunt uploaden in plaats van bibliotheken op de client, zoals AppMeasurement.
solution: Analytics
feature: API
exl-id: c9d23fae-2800-42bb-8f8d-adf915cadc62
role: Admin
source-git-commit: 27bcbd638848650c842ad8d8aaa7ab59e27e900e
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 4%

---

# API voor data-invoer in bulk

De toevoeging van bulkgegevens lost verscheidene gebruiksgevallen op, zoals:

* Historische gegevens uit een vorig analysesysteem verzamelen

* Een intern analysesysteem dat het gebruik van AppMeasurement onmogelijk maakt. Met de ETL-processen (Extract-Transform-Load) kunt u gegevens in batchbestanden plaatsen. Vervolgens gebruikt u BDIA om deze te uploaden naar Adobe Analytics.

* Gegevensverzameling van apparaten die slechts intermitterende connectiviteit met internet hebben. Deze apparaten slaan de interacties op tot zij een verbinding ontvangen. Het apparaat kan de gegevens vervolgens allemaal tegelijk uploaden via BDIA.

API voor gegevensinvoeging en [API voor het invoegen van bulkgegevens](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md)zijn beide methoden om gegevens van verzamelingen op de server naar Adobe Analytics te verzenden. API-aanroepen voor het invoegen van gegevens worden één gebeurtenis tegelijk uitgevoerd. De API voor het invoegen van bulkgegevens accepteert CSV-bestanden met gebeurtenisgegevens, één gebeurtenis per rij. Als u aan een nieuwe implementatie van server-zijinzameling werkt, adviseren wij gebruikend de Invoeging API van de Gegevens van het Bulk.
