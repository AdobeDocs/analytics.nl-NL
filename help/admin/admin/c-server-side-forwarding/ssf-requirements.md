---
description: U moet deze oplossing van Experience Cloud, de dienst, en codevereisten ontmoeten om server-zij het door:sturen uit te voeren. Deze vereisten omvatten ook instructies over hoe te om codeversies te controleren en waar te om de recentste codebibliotheken te krijgen.
solution: Audience Manager
title: Vereisten voor server-side doorsturen
uuid: e52c9292-b2ed-4782-9594-c813e4f894e1
exl-id: af0cf85a-381e-46d2-a4fd-9a5b073c8a8d
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 2%

---

# Vereisten voor server-side doorsturen

U moet deze oplossing van Experience Cloud, de dienst, en codevereisten ontmoeten om server-zij het door:sturen uit te voeren. Deze vereisten omvatten ook instructies over hoe te om codeversies te controleren en waar te om de recentste codebibliotheken te krijgen.

## Oplossingsvereisten

Het doorsturen aan de serverzijde werkt met [Analytics](https://www.adobe.com/data-analytics-cloud/analytics.html) en [Audience Manager](https://www.adobe.com/data-analytics-cloud/audience-manager.html) en/of [Soorten publiek](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Servicevereisten

Voor server-side verzending is [Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) vereist. De identiteitsservice biedt een universele id die bezoekers van de site identificeert voor alle oplossingen in de Experience Cloud. U moet de dienst van identiteitskaart uitvoeren alvorens server-kant het door:sturen zal werken.

## Codeversies

Voor het doorsturen aan de serverzijde is versie 1.5 (of hoger) van de hieronder vermelde codebibliotheken vereist. We raden u aan de nieuwste versies te gebruiken in plaats van deze minimale versies.

* `AppMeasurement.js`
* `AppMeasurement_Module_AudienceManagement.js`
* `VistorAPI.js`

### De versie van uw codebibliotheek bepalen

Om het even welk hulpmiddel dat de HTTP- verzoeken controleert die door browser worden gemaakt kan u het versieaantal voor uw code van AppMeasurement en van de Bezoeker API tonen. De `AppMeasurement_Module_AudienceManagement.js` bevat geen versie-id of retourneert deze niet. De volgende voorbeelden tonen u hoe versie IDs voor `AppMeasurement.js` en `VisitorAPI.js` code kijkt.

* `AppMeasurement.js`: De  [Adobe ](https://experienceleague.adobe.com/docs/analytics/implementation/validate/debugger.html) Foutopsporing keert de versie AppMeasurement als dit terug:  `Version of Code | JS-1.5.1`. Andere gereedschappen kunnen een ander label gebruiken, maar de waarde volgt altijd het patroon `JS-X.X.X`, waarbij `X` een versienummer is.
* `VisitorAPI.js`: Zoek de  `d_visid_ver` parameter. De bezoeker-id-service wordt als volgt weergegeven: `d_visid_ver: 1.5.5`. Bezoeker-API-code ouder dan versie 1.5.2 bevat geen versienummer. U gebruikt waarschijnlijk een oudere codebibliotheek (en moet bevorderen) als uw controleresultaten geen versieaantal terugkeren.
