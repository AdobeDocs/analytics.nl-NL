---
title: API voor data-invoer in bulk
description: BDIA (Bulk Data Insertion API) is een Adobe Analytics-functie waarmee u gegevens van serveroproepen in batches bestanden kunt uploaden in plaats van bibliotheken op de client, zoals AppMeasurement. De serveraanroepen in deze batchbestanden kunnen actuele (live) gegevens of historische gegevens zijn. Het is een meer schaalbare opvolger van de API voor het invoegen van gegevens in eerdere versies van de Adobe Analytics API.
solution: Analytics
feature: API
source-git-commit: d8603ddd6cee2ccc930281003d9ff1befa15c95c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# API voor data-invoer in bulk

De toevoeging van bulkgegevens lost verscheidene gebruiksgevallen op, zoals:

* Historische gegevens uit een vorig analysesysteem verzamelen

* Een intern analysesysteem dat het onuitvoerbaar maakt om AppMeasurement te gebruiken. Met de ETL-processen (Extract-Transform-Load) kunt u gegevens in batchbestanden plaatsen. Vervolgens gebruikt u BDIA om deze te uploaden naar Adobe Analytics.

* Gegevensverzameling van apparaten die slechts intermitterende connectiviteit met internet hebben. Deze apparaten slaan de interacties op tot zij een verbinding ontvangen. Het apparaat kan de gegevens vervolgens allemaal tegelijk uploaden via BDIA.

API voor gegevensinvoeging en [API voor het invoegen van bulkgegevens](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md)zijn beide methoden om gegevens van verzamelingen op de server naar Adobe Analytics te verzenden. API-aanroepen voor het invoegen van gegevens worden één gebeurtenis tegelijk uitgevoerd. De API voor het invoegen van bulkgegevens accepteert CSV-bestanden met gebeurtenisgegevens, één gebeurtenis per rij. Als u aan een nieuwe implementatie van server-zijinzameling werkt, adviseren wij gebruikend de Invoeging API van de Gegevens van het Bulk.