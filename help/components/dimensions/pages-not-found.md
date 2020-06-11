---
title: Pagina's niet gevonden
description: URL's die een fout op uw site hebben geretourneerd.
translation-type: tm+mt
source-git-commit: 54aeaa35fea8f725c87030936fa24f415064e333
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---


# Pagina&#39;s niet gevonden

*Deze Help-pagina beschrijft hoe &#39;Pagina&#39;s niet gevonden&#39; werkt als een dimensie. Zie de[Pagina&#39;s niet metrisch voor meer informatie gevonden](../metrics/pages-not-found.md).*

De dimensie &#39;Pagina&#39;s niet gevonden&#39; toont URL&#39;s die een fout bevatten. Deze dimensie is handig als u het aantal fouten dat bezoekers op uw site krijgen, wilt verminderen.

* U kunt deze dimensie in een [stroomvisualisatie](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) gebruiken om te zien welke pagina&#39;s bezoekers door klikken om de fout te bereiken. U kunt dan met ontwikkelingsteams in uw organisatie werken om de verbinding op elke pagina te bevestigen.
* U kunt deze dimensie met de dimensie [&#39;Referrer&#39;](referrer.md) gebruiken om te zien waar de bezoekers aan uw plaats van externe verbindingen aankomen. U kunt of omleidingen aan de gewenste plaats uitvoeren, of met de derde werken om de verbinding te herstellen.

## Deze dimensie vullen met gegevens

Deze dimensie wint gegevens van de [`pageType` en `g` vraagkoorden](/help/implement/validate/query-parameters.md) in beeldverzoeken terug. Als de `pageType` querytekenreeks gelijk is `errorPage`, wordt de `g` querytekenreeks (pagina-URL) opgenomen. AppMeturement verzamelt deze gegevens met behulp van de [`pageType`](/help/implement/vars/page-vars/pagetype.md) variabele. Als de `pageType` variabele niet is gedefinieerd of op iets anders is ingesteld dan `errorPage`, worden geen gegevens voor deze dimensie verzameld.

## Dimensiewaarden

Tot de waarden voor dimensies behoren de URL&#39;s van pagina&#39;s op uw site waar een fout is opgetreden.
