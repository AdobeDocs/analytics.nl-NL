---
title: Pagina's niet gevonden
description: URL's die een fout op uw site hebben geretourneerd.
feature: Dimensions
exl-id: 28c22565-7fcf-49f1-8876-0db88f12a182
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# Pagina&#39;s niet gevonden

*Deze Help-pagina beschrijft hoe &#39;Pagina&#39;s niet gevonden&#39; werkt als een dimensie. Zie de [Pagina&#39;s niet gevonden](../metrics/pages-not-found.md) metrisch voor meer informatie.*

De dimensie &#39;Pagina&#39;s niet gevonden&#39; toont URL&#39;s die een fout bevatten. Deze dimensie is handig als u het aantal fouten dat bezoekers op uw site krijgen, wilt verminderen.

* U kunt deze dimensie gebruiken in een [Stroomvisualisatie](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) om te zien welke pagina&#39;s bezoekers door klikken om de fout te bereiken. U kunt dan met ontwikkelingsteams in uw organisatie werken om de verbinding op elke pagina te bevestigen.
* U kunt deze dimensie gebruiken met de [&#39;Referrer&#39;](referrer.md) dimensie om te zien waar bezoekers via externe koppelingen naar uw site aankomen. U kunt of omleidingen aan de gewenste plaats uitvoeren, of met de derde werken om de verbinding te herstellen.

## Deze dimensie vullen met gegevens

Deze dimensie haalt gegevens van terug [`pageType` en `g` querytekenreeksen](/help/implement/validate/query-parameters.md) in afbeeldingsaanvragen. Als de `pageType` queryreeks is gelijk `errorPage`de `g` querytekenreeks (pagina-URL) wordt opgenomen. AppMeturement verzamelt deze gegevens met de [`pageType`](/help/implement/vars/page-vars/pagetype.md) variabele. Als de `pageType` variabele is niet gedefinieerd of ingesteld op iets anders dan `errorPage`Er worden geen gegevens voor deze dimensie verzameld.

## Dimension-items

Tot de Dimension-items behoren de URL&#39;s van de pagina&#39;s op uw site waarop een fout is opgetreden.
