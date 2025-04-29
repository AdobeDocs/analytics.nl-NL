---
title: Pagina's niet gevonden (afmetingen)
description: URL's die een fout op uw site hebben geretourneerd.
feature: Dimensions
exl-id: 28c22565-7fcf-49f1-8876-0db88f12a182
source-git-commit: 828f41bf45c1954c3b68ad71a7746e24626b9eed
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# Pagina&#39;s niet gevonden

*Deze hulppagina beschrijft hoe de &quot;Pagina&#39;s niet gevonden&quot;werken als a [ dimensie ](overview.md). Zie de [ Pagina&#39;s niet gevonden ](../metrics/pages-not-found.md) metrische pagina voor informatie over hoe het als metrisch werkt.*

De dimensie &#39;Pagina&#39;s niet gevonden&#39; toont URL&#39;s die een fout bevatten. Deze dimensie is handig als u het aantal fouten dat bezoekers op uw site krijgen, wilt verminderen.

* U kunt deze afmeting in a [ Stroomvisualisatie ](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) gebruiken om te zien welke paginabezoekers door klikken om de fout te bereiken. U kunt dan met ontwikkelingsteams in uw organisatie werken om de verbinding op elke pagina te bevestigen.
* U kunt deze afmeting met de [ &quot;Verwijzer&quot;](referrer.md) afmeting gebruiken om te zien waar de bezoekers aan uw plaats van externe verbindingen aankomen. U kunt of omleidingen aan de gewenste plaats uitvoeren, of met de derde werken om de verbinding te herstellen.

## Deze dimensie vullen met gegevens

Deze dimensie wint gegevens van [`pageType` en `g` vraagkoorden ](/help/implement/validate/query-parameters.md) in beeldverzoeken terug. Als de `pageType` querytekenreeks gelijk is aan `errorPage` , wordt de `g` querytekenreeks (pagina-URL) opgenomen. AppMeasurement verzamelt deze gegevens met behulp van de variabele [`pageType`](/help/implement/vars/page-vars/pagetype.md) . Wanneer de variabele `pageType` niet is gedefinieerd of op iets anders is ingesteld dan `errorPage` , worden geen gegevens voor deze dimensie verzameld.

## Dimension-objecten

Dimension-items bevatten de URL&#39;s van de pagina&#39;s op uw site waarop een fout is opgetreden.
