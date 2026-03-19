---
title: Enkelvoudige toegang
description: Het aantal keren dat een dimensie-item niet is gewijzigd tijdens een bezoek.
feature: Metrics
exl-id: 973ce835-9d6f-4ead-90c9-0b80aac82cc0
source-git-commit: 6d2c278c5525c89b73c39bbfcedbe644806bf989
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# Enkelvoudige toegang

**[!UICONTROL Single access]** [ metrisch ](overview.md) toont het aantal bezoeken waar de toepasselijke het melden afmeting slechts één enkele waarde voor een volledig bezoek bevatte. Het is de bredere, dimensiespecifieke versie van [[!UICONTROL Single page visits]](single-page-visits.md). Deze metrische waarde is handig voor elke dimensie waarin u de waarde van een dimensie wilt zien wanneer deze slechts eenmaal is ingesteld tijdens een bezoek.

## Hoe deze metrische waarde wordt berekend

De definitie van deze metrische waarde is afhankelijk van de projectinstelling [[!UICONTROL Count repeat instances]](/help/analyze/analysis-workspace/build-workspace-project/create-projects.md#project-info-settings) :

* **toegelaten de herhalingsinstanties van de Telling**: Telt bezoeken waar de dimensie precies één waarde in een bezoek bevat. Als de afmeting voortduurt, dan kwalificeert het niet meer als één enkele toegang.
* **de herhalingsinstanties van de Telling gehandicapt**: Telt bezoeken waar de dimensie één enkele unieke waarde bevat. U kunt het afmetingspunt aan de zelfde waarde veelvoudige tijden plaatsen of het hebben aanhoudt en het nog telt als één enkele toegang.

Ongeacht &quot;[!UICONTROL Count repeat instances]&quot;, kwalificeert het bezoek niet meer als één enkele toegang als de afmeting in een tweede unieke waarde verandert. De volgende vraag van de verbinding is inbegrepen in deze berekening als de afmeting in hen wordt geplaatst.

## Verschil tussen &#39;[!UICONTROL Single access]&#39; en &#39;[!UICONTROL Single page visit]&#39;

In context van de [[!UICONTROL Page]](../dimensions/page.md) dimensie, &quot;[!UICONTROL Single access]&quot;en &quot;[!UICONTROL Single page visits]&quot;zijn altijd precies identiek ongeacht &quot;[!UICONTROL Count repeat instances]&quot;project het plaatsen. Hun verschillen komen naar voren wanneer je andere dimensies gebruikt.

* **[!UICONTROL Single access]**: geeft het aantal bezoeken weer waar het opgegeven dimensie-item aanwezig was voor één hit. Het is contextueel aan de dimensie die u in uw project gebruikt.
* **[!UICONTROL Single page visit]**: toont het aantal bezoeken waar de &quot;[!UICONTROL Page]&quot;dimensie voor één enkele klap aanwezig was. Alhoewel u een andere dimensie in uw rapport gebruikt, telt het nog bezoeken die één enkel uniek ([!UICONTROL Page]&quot;dimensie punt bevatten.

Wanneer [[!UICONTROL Count repeat instances]](/help/analyze/analysis-workspace/build-workspace-project/create-projects.md#project-info-settings) is uitgeschakeld, veranderen de metrische definities iets:

* **Enige toegang**: Toont het aantal bezoeken waar het bepaalde afmetingspunt niet voor het volledige bezoek veranderde.
* **Enige paginabezoek**: Toont het aantal bezoeken waar de &#39;[!UICONTROL Page]&#39; dimensie niet voor het volledige bezoek veranderde.

Neem bijvoorbeeld het volgende voorbeeld van twee-raakbezoeken. De dimensie in uw rapport is [[!UICONTROL Site section]](../dimensions/site-section.md) en &quot;[!UICONTROL Count repeat instances]&quot;is gehandicapt.

* Een bezoeker slaat twee pagina&#39;s aan, maar ze bevinden zich allebei in dezelfde sitesectie. Aangezien de sectie van de plaats door het bezoek het zelfde bleef, telt het als één enkele toegang. Het telt niet als een bezoek van één pagina omdat het bezoek meer dan één uniek [!UICONTROL Page] dimensie-item bevat.
* Een bezoeker raakt twee pagina&#39;s in verschillende sitesecties, maar beide pagina&#39;s worden toevallig het zelfde genoemd. Het bezoek telt niet als één enkele toegang omdat er twee unieke waarden van de plaatssectie waren. Het telt als een bezoek van één pagina omdat er één uniek [!UICONTROL Page] dimensie-item was.
