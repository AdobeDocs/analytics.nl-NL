---
title: Implementatiemethoden vergelijken
description: Zie de voordelen van elke methode die gegevens naar Adobe Analytics verzendt.
source-git-commit: 96a5daaf9d8358e4a5222a20f64c381cb8340ab1
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# Implementatiemethoden vergelijken

Zie hoe elke methode om Adobe Analytics uit te voeren met elkaar vergelijkt. U kunt deze lijst gebruiken om uw organisatie te helpen de meest ideale manier bepalen om gegevens naar Adobe te verzenden.

|  | AppMeasurement | Adobe Analytics-extensie | Web SDK | Web SDK-extensie |
| --- | --- | --- | --- | --- |
| Implementatievereisten | Referentie `AppMeasurement.js` op elke pagina variabelen definiëren, gegevens verzenden met `s.t()` | De markeringslader van de verwijzing op elke pagina, gebruik UI van de Inzameling van Gegevens om variabelen te bepalen en gegevens naar Adobe te verzenden | Referentie `Alloy.js` op elke pagina, gebruik `alloy("sendEvent",{})` om een JSON-object te verzenden dat de gewenste gegevens bevat | De markeringslader van de verwijzing op elke pagina, gebruik de UI van de Inzameling van Gegevens om het JSON voorwerp tot stand te brengen om gegevens te verzenden |
| Gegevensbestemming | Direct verzonden naar Adobe Analytics | Direct verzonden naar Adobe Analytics | Verzonden naar Adobe Experience Platform Edge, die gegevens doorstuurt naar Adobe Analytics | Verzonden naar Adobe Experience Platform Edge, die gegevens doorstuurt naar Adobe Analytics |
| Probleem bij het aanbrengen van aanpassingen in de implementatie | Vereist toegang tot websitecode voor elke implementatiewijziging | De code van de website hoeft slechts eenmaal te worden gewijzigd om de loader-tag te installeren. alle verdere implementatie-updates kunnen worden uitgevoerd in de gebruikersinterface voor gegevensverzameling | Vereist toegang tot websitecode voor elke implementatiewijziging | De code van de website hoeft slechts eenmaal te worden gewijzigd om de loader-tag te installeren. alle verdere implementatie-updates kunnen worden uitgevoerd in de gebruikersinterface voor gegevensverzameling |
| Hoe A4T wordt behandeld | A4T vraag omvat in klappen die naar Adobe worden verzonden | A4T vraag omvat in klappen die naar Adobe worden verzonden | A4T-aanroepen worden verzonden als afzonderlijke treffers | A4T-aanroepen worden verzonden als afzonderlijke treffers |
| Hoe de verwijzer wordt behandeld |