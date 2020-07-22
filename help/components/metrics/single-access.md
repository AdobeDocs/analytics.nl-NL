---
title: Enkelvoudige toegang
description: Het aantal keren dat een dimensie-item niet is gewijzigd tijdens een bezoek.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 0%

---


# Enkelvoudige toegang

De metrische waarde &#39;Enkelvoudige toegang&#39; toont het aantal bezoeken waar het dimensie-item slechts één unieke waarde voor het volledige bezoek bevatte. Deze metrische waarde is handig voor elke dimensie waarin u wilt zien welke elementen tijdens een bezoek stagneren.

## Hoe deze metrische waarde wordt berekend

Deze metrische tellingen bezoeken waar het afmetingspunt één enkele unieke waarde bevatte. U kunt het afmetingspunt plaatsen veelvoudige tijden of het hebben voortbestaan en nog tellen als één enkele toegang. Zodra een dimensie-item verandert in een tweede unieke waarde, komt het bezoek niet meer in aanmerking als één enkele toegang.

## Verschil tussen &#39;Eén enkele toegang&#39; en &#39;Bezoek één pagina&#39;

In het kader van de [pagina](../dimensions/page.md) -dimensie zijn &#39;Eén enkele toegang&#39; en &#39;Bezoeken op één pagina&#39; exact hetzelfde. Hun verschillen komen naar voren wanneer je andere dimensies gebruikt.

* **Enkelvoudige toegang**: Toont het aantal bezoeken waar het bepaalde afmetingspunt niet voor het volledige bezoek veranderde. Het is contextueel aan de dimensie die u in uw project gebruikt.
* **Bezoek**&#x200B;één pagina: Hier ziet u het aantal bezoeken waarbij de dimensie Pagina niet is gewijzigd voor het volledige bezoek. Alhoewel u een andere dimensie in uw rapport gebruikt, telt het nog bezoeken die één enkel uniek punt van de &quot;Pagina&quot;dimensie bevatten.

Neem bijvoorbeeld het volgende voorbeeld van twee aanraakbezoeken. De dimensie in uw rapport is de sectie [van de](../dimensions/site-section.md)Plaats.

* Een bezoeker slaat twee pagina&#39;s aan, maar ze bevinden zich allebei in dezelfde sitesectie. Aangezien de sectie van de plaats door het bezoek het zelfde bleef, telt het als Één enkele toegang. Het telt niet als een Bezoek van één pagina omdat het bezoek meer dan één uniek pagina-afmetingsitem bevat.
* Een bezoeker raakt twee pagina&#39;s in verschillende sitesecties, maar beide pagina&#39;s worden toevallig het zelfde genoemd. Het bezoek telt niet als één enkele toegang omdat er twee unieke waarden van de plaatssectie waren. Het telt als een bezoek van één pagina omdat er één enkel uniek punt van de Pagina afmeting was.
