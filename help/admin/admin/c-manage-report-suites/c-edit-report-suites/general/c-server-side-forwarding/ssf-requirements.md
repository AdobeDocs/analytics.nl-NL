---
description: U moet deze oplossing van het Experience Cloud, de dienst, en codevereisten ontmoeten om server-zij het door:sturen uit te voeren. Deze vereisten omvatten ook instructies over hoe te om codeversies te controleren en waar te om de recentste codebibliotheken te krijgen.
solution: Analytics
title: Vereisten voor server-side door:sturen
feature: Server-Side Forwarding
exl-id: af0cf85a-381e-46d2-a4fd-9a5b073c8a8d
role: Admin
source-git-commit: def7d071de1765acf524a638a8f8d13ae69e1a1f
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---

# Vereisten voor server-side door:sturen

U moet deze oplossing van het Experience Cloud, de dienst, en codevereisten ontmoeten om server-zij het door:sturen uit te voeren. Deze vereisten omvatten ook instructies over hoe te om codeversies te controleren en waar te om de recentste codebibliotheken te krijgen.

## Oplossingsvereisten

Het door:sturen van de server werkt met [Analyse](https://www.adobe.com/data-analytics-cloud/analytics.html) en [Audience Manager](https://www.adobe.com/data-analytics-cloud/audience-manager.html) en/of [Soorten publiek](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=nl-NL).

## Servicevereisten

Voor het doorsturen op de server is de [Identiteitsservice](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=nl-NL). De identiteitsservice biedt een universele id waarmee bezoekers van de site op alle oplossingen in het Experience Cloud kunnen worden geïdentificeerd. U moet de dienst van identiteitskaart uitvoeren alvorens server-kant het door:sturen zal werken.

## Codeversies

Voor het doorsturen aan de serverzijde is versie 1.5 (of hoger) van de hieronder vermelde codebibliotheken vereist. We raden u aan de nieuwste versies te gebruiken in plaats van deze minimale versies.

* `AppMeasurement.js`
* `AppMeasurement_Module_AudienceManagement.js`
* `VistorAPI.js`

### De versie van uw codebibliotheek bepalen

Om het even welk hulpmiddel dat de HTTP- verzoeken controleert die door browser worden gemaakt kan u het versieaantal voor uw AppMeasurement en de code van de BezoekerAPI tonen. De `AppMeasurement_Module_AudienceManagement.js` bevat geen versie-id of retourneert deze. In de volgende voorbeelden ziet u hoe de versie-id&#39;s eruit zien `AppMeasurement.js` en `VisitorAPI.js` code.

* `AppMeasurement.js`: De [Adobe Debugger](https://experienceleague.adobe.com/docs/analytics/implementation/validate/debugger.html?lang=nl-NL) retourneert de versie van het AppMeasurement als volgt: `Version of Code | JS-1.5.1`. Andere gereedschappen kunnen een ander label gebruiken, maar de waarde volgt altijd het patroon `JS-X.X.X`, waarbij `X` is een versienummer.
* `VisitorAPI.js`: Zoek naar de `d_visid_ver` parameter. De bezoeker-id-service wordt als volgt weergegeven: `d_visid_ver: 1.5.5`. Bezoeker-API-code ouder dan versie 1.5.2 bevat geen versienummer. U gebruikt waarschijnlijk een oudere codebibliotheek (en moet bevorderen) als uw controleresultaten geen versieaantal terugkeren.
