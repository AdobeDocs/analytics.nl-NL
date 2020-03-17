---
description: U moet aan deze oplossing van de Wolk van Ervaring, de dienst, en codevereisten voldoen om server-zijhet door:sturen uit te voeren. Deze vereisten omvatten ook instructies over hoe te om codeversies te controleren en waar te om de recentste codebibliotheken te krijgen.
solution: Audience Manager
title: Vereisten voor server-side door:sturen
uuid: e52c9292-b2ed-4782-9594-c813e4f894e1
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Vereisten voor server-side door:sturen

U moet aan deze oplossing van de Wolk van Ervaring, de dienst, en codevereisten voldoen om server-zijhet door:sturen uit te voeren. Deze vereisten omvatten ook instructies over hoe te om codeversies te controleren en waar te om de recentste codebibliotheken te krijgen.

## Oplossingsvereisten

Server-kant het door:sturen werkt met [Analytics](https://www.adobe.com/data-analytics-cloud/analytics.html) en de Manager [van het](https://www.adobe.com/data-analytics-cloud/audience-manager.html) Publiek en/of [Publiek](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html).

## Servicevereisten

Voor server-side doorsturen is de [Identity Service](https://marketing.adobe.com/resources/help/en_US/mcvid/)vereist. De Identity Service biedt een universele id die bezoekers van de site identificeert voor alle oplossingen in de Experience Cloud. U moet de dienst van identiteitskaart uitvoeren alvorens server-kant het door:sturen zal werken.

## Codeversies

Voor het doorsturen aan de serverzijde is versie 1.5 (of hoger) van de hieronder vermelde codebibliotheken vereist. We raden u aan de nieuwste versies te gebruiken in plaats van deze minimale versies.

* `AppMeasurement.js`
* `AppMeasurement_Module_AudienceManagement.js`
* `VistorAPI.js`

### De versie van uw codebibliotheek bepalen

Om het even welk hulpmiddel dat de HTTP- verzoeken controleert die door browser worden gemaakt kan u het versieaantal voor uw code van AppMeasurement en van de Bezoeker API tonen. De id `AppMeasurement_Module_AudienceManagement.js` bevat geen versie-id of retourneert deze niet. In de volgende voorbeelden ziet u hoe de versie-id&#39;s eruit zien voor `AppMeasurement.js` en `VisitorAPI.js` code.

* `AppMeasurement.js`: De [foutopsporing](https://marketing.adobe.com/resources/help/en_US/sc/implement/debugger.html) van Adobe retourneert de versie AppMeasurement als volgt: `Version of Code | JS-1.5.1`. Andere gereedschappen kunnen een ander label gebruiken, maar de waarde volgt altijd het patroon, `JS-X.X.X`waarbij `X` een versienummer wordt gebruikt.
* `VisitorAPI.js`: Zoek de `d_visid_ver` parameter. De bezoeker-id-service wordt als volgt weergegeven: `d_visid_ver: 1.5.5`. Bezoeker-API-code ouder dan versie 1.5.2 bevat geen versienummer. U gebruikt waarschijnlijk een oudere codebibliotheek (en moet bevorderen) als uw controleresultaten geen versieaantal terugkeren.
