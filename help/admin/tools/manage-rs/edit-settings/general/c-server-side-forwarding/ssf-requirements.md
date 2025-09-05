---
description: U moet deze oplossing van Experience Cloud, de dienst, en codevereisten ontmoeten om server-zijhet door:sturen uit te voeren. Deze vereisten omvatten ook instructies over hoe te om codeversies te controleren en waar te om de recentste codebibliotheken te krijgen.
solution: Analytics
title: Vereisten voor server-side door:sturen
feature: Report Suite Settings
exl-id: af0cf85a-381e-46d2-a4fd-9a5b073c8a8d
role: Admin
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---

# Vereisten voor server-side door:sturen

U moet deze oplossing van Experience Cloud, de dienst, en codevereisten ontmoeten om server-zijhet door:sturen uit te voeren. Deze vereisten omvatten ook instructies over hoe te om codeversies te controleren en waar te om de recentste codebibliotheken te krijgen.

## Oplossingsvereisten

Server-kant het door:sturen werkt met [ Analytics ](https://www.adobe.com/data-analytics-cloud/analytics.html) en [ Audience Manager ](https://www.adobe.com/data-analytics-cloud/audience-manager.html) en/of [ Soorten publiek ](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Servicevereisten

Server-kant het door:sturen vereist de [ Dienst van de Identiteit ](https://experienceleague.adobe.com/docs/id-service/using/home.html). De Identity Service biedt een universele id die bezoekers van de site identificeert voor alle oplossingen in de Experience Cloud. U moet de dienst van identiteitskaart uitvoeren alvorens server-kant het door:sturen zal werken.

## Codeversies

Voor het doorsturen aan de serverzijde is versie 1.5 (of hoger) van de hieronder vermelde codebibliotheken vereist. We raden u aan de nieuwste versies te gebruiken in plaats van deze minimale versies.

* `AppMeasurement.js`
* `AppMeasurement_Module_AudienceManagement.js`
* `VistorAPI.js`

### De versie van uw codebibliotheek bepalen

Om het even welk hulpmiddel dat de HTTP- verzoeken controleert die door browser worden gemaakt kan u het versieaantal voor uw AppMeasurement en bezoeker API code tonen. De `AppMeasurement_Module_AudienceManagement.js` bevat geen versie-id of retourneert deze niet. In de volgende voorbeelden ziet u hoe de versie-id&#39;s voor `AppMeasurement.js` - en `VisitorAPI.js` -code eruit zien.

* `AppMeasurement.js`: [ Adobe Debugger ](/help/implement/validate/debugger.md) keert de versie van AppMeasurement als dit terug: `Version of Code | JS-1.5.1`. Andere gereedschappen kunnen een ander label gebruiken, maar de waarde volgt altijd het patroon `JS-X.X.X` , waarbij `X` een versienummer is.
* `VisitorAPI.js`: zoek naar de parameter `d_visid_ver` . U ziet hier de service Bezoeker-id als volgt: `d_visid_ver: 1.5.5` . Bezoeker-API-code ouder dan versie 1.5.2 bevat geen versienummer. U gebruikt waarschijnlijk een oudere codebibliotheek (en moet bevorderen) als uw controleresultaten geen versieaantal terugkeren.
