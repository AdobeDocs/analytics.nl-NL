---
title: Enkelvoudige toegang
description: Het aantal keren dat een dimensie-item niet is gewijzigd tijdens een bezoek.
feature: Metrics
exl-id: 973ce835-9d6f-4ead-90c9-0b80aac82cc0
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 0%

---

# Enkelvoudige toegang

De &#39;enkele toegang&#39; [metrisch](overview.md) toont het aantal bezoeken waar het afmetingspunt slechts één enkele unieke waarde voor het volledige bezoek bevatte. Deze metrische waarde is handig voor elke dimensie waarin u wilt zien welke elementen tijdens een bezoek stagneren.

## Hoe deze metrische waarde wordt berekend

Deze metrische tellingen bezoeken waar het afmetingspunt één enkele unieke waarde bevatte. U kunt het afmetingspunt plaatsen veelvoudige tijden of het hebben voortbestaan en nog tellen als één enkele toegang. Zodra een dimensie-item verandert in een tweede unieke waarde, komt het bezoek niet meer in aanmerking als één enkele toegang.

## Verschil tussen &#39;Eén enkele toegang&#39; en &#39;Bezoek één pagina&#39;

In het kader van de [Pagina](../dimensions/page.md) Dimensies, &#39;Enkelvoudige toegang&#39; en &#39;Bezoeken op één pagina&#39; zijn exact identiek. Hun verschillen komen naar voren wanneer je andere dimensies gebruikt.

* **Enkelvoudige toegang**: Geeft het aantal bezoeken weer, waarbij het gegeven item Dimensie niet is gewijzigd voor het volledige bezoek. Het is contextueel aan de dimensie die u in uw project gebruikt.
* **Bezoek één pagina**: Geeft het aantal bezoeken weer waarbij de dimensie Pagina niet is gewijzigd voor het volledige bezoek. Alhoewel u een andere dimensie in uw rapport gebruikt, telt het nog bezoeken die één enkel uniek punt van de &quot;Pagina&quot;dimensie bevatten.

Neem bijvoorbeeld het volgende voorbeeld van twee aanraakbezoeken. De dimensie in uw rapport is [Sectie Site](../dimensions/site-section.md).

* Een bezoeker slaat twee pagina&#39;s aan, maar ze bevinden zich allebei in dezelfde sitesectie. Aangezien de sectie van de plaats door het bezoek het zelfde bleef, telt het als Één enkele toegang. Het telt niet als een Bezoek van één pagina omdat het bezoek meer dan één uniek pagina-afmetingsitem bevat.
* Een bezoeker raakt twee pagina&#39;s in verschillende sitesecties, maar beide pagina&#39;s worden toevallig het zelfde genoemd. Het bezoek telt niet als één enkele toegang omdat er twee unieke waarden van de plaatssectie waren. Het telt als een bezoek van één pagina omdat er één enkel uniek punt van de Pagina afmeting was.
