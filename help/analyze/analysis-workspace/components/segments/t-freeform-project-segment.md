---
description: Gebruik segmenten in Analysis Workspace.
title: Segmenten
feature: Segmentation
role: User, Admin
exl-id: 67112e13-4d0a-4d77-be50-496c3d28779c
source-git-commit: d7a6867796f97f8a14cd8a3cfad115923b329c7c
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 1%

---


# Segmenten {#topic_DC2917A2E8FD4B62816572F3F6EDA58A}

U kunt verschillende typen segmenten maken in Workspace, afhankelijk van de complexiteit die ze moeten hebben, of ze alleen op dit project moeten worden toegepast, enzovoort. Hier volgt een overzicht van segmenttypen:

| Segmenttype | Waar gemaakt? | Waar van toepassing? | Wanneer gebruiken |
| --- | --- | --- | --- |
| Segment op lijst met componenten | Klik +, die u aan de [ Bouwer van het Segment ](/help/components/segmentation/segmentation-workflow/seg-build.md) neemt | Alle Workspace-projecten | Voor complexere segmenten, opeenvolgende segmenten |
| Snel segment | [ Snelle segmentbouwer ](/help/analyze/analysis-workspace/components/segments/quick-segments.md) | Alleen project, maar u kunt het segment opslaan en toevoegen aan uw segmentlijst. | Kan worden gebruikt voor ad-hocsegmenten met één regel (met slepen en neerzetten) of om meerdere regels toe te voegen/te bewerken (door op het pictogram Segment te klikken) |
| Op cijfers gebaseerd segment | [ Berekende metrische bouwer ](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/metrics-with-segments.html) | Op berekende individuele metrieke waarde | Segment/s toepassen binnen uw metrische definitie |
| Op suite gebaseerd segment van virtueel rapport | [ de Virtuele bouwer van de rapportsuite ](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-workflow/vrs-create.html) | Naar afzonderlijke virtuele rapportsuite | Segment/segmenten toepassen binnen de definitie van uw virtuele rapportsuite |

## Video&#39;s

>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Gebruikend segmenten in Analysis Workspace ](https://video.tv.adobe.com/v/23977?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Vindend en creërend segmenten ](https://video.tv.adobe.com/v/334092?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Rolling datumwaaiers in segment ](https://video.tv.adobe.com/v/25403?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


## Segmenten maken {#section_693CFADA668B4542B982446C2B4CF0F5}

In Analysis Workspace kunt u verschillende typen segmenten maken:

* [Snelle segmenten](/help/analyze/analysis-workspace/components/segments/quick-segments.md)
* Regelmatige component-lijst segmenten die u in de Bouwer van het Segment creeert en die omhoog in de segmentbibliotheek (zie hieronder) beëindigen

### Segmenten maken voor lijsten met componenten {#section_3B07D458C43E42FDAF242BB3ACAF3E90}

De segmentrail onder het menu Componenten toont

* Segmenten die u of uw bedrijf heeft gemaakt
* De malplaatjes van het segment, zoals die door het Adobe ![ worden ondertekend AdobeLogoSmall ](/help/assets/icons/AdobeLogoSmall.svg) pictogram:


Als u een segment van dit type wilt maken, hebt u twee opties. Beide nemen u aan de [ Bouwer van het Segment ](/help/components/segmentation/segmentation-workflow/seg-build.md) in Adobe Analytics, waar u verdere instructies kunt vinden.

* Klik in de linkertrack op het plusteken (+) naast [!UICONTROL Segments] :

![](assets/create-seg.png)

of

* Ga naar [!UICONTROL Components] > [!UICONTROL Segments] en klik vervolgens op [!UICONTROL + Add] .


### Andere methoden voor het toepassen van segmenten {#section_10FF2E309BA84618990EA5B473015894}


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Andere methodes om segmenten ](https://video.tv.adobe.com/v/30994?quality=12&learn=on){target="_blank"} voor een demo video toe te passen.

>[!ENDSHADEBOX]

Er bestaan verschillende andere methoden voor het toepassen van segmenten op een vrije-vormproject.

| Handeling | Beschrijving |
|--- |--- |
| Segment maken van selectie | Maak een inline-segment. Dit segment is alleen van toepassing op het geopende project en wordt niet opgeslagen als een analysesegment. 1. Selecteer rijen.  2. Klik met de rechtermuisknop op de selectie.  3. Klik *creeer segment van selectie*. |
| Componenten > Nieuw segment | Toont de Bouwer van het Segment. Zie {de Bouwer van het 0} Segment ](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) voor meer informatie over segmentatie.[ |
| Delen > Project delen of Delen > Projectgegevens krommen | In [ Kromme en Aandeel ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/curate.html#concept_4A9726927E7C44AFA260E2BB2721AFC6), leer hoe de segmenten die u op het project toepast in gedeelde analyse voor de ontvanger beschikbaar zijn. |
| Segmenten gebruiken als Dimensionen | Video: [ Gebruikend Segmenten als Dimensionen in Analysis Workspace ](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/applying-segments/using-segments-as-dimensions-in-analysis-workspace.html) |

## Segment-IQ

Segment-IQ (ook wel Segment Comparison genoemd) omvat de volgende kenmerken:

* [ de vergelijkingspaneel van het Segment:](/help/analyze/analysis-workspace/c-panels/c-segment-comparison/segment-comparison.md) de kerneigenschap in IQ van het Segment. Sleep twee segmenten naar het deelvenster en bekijk een uitgebreid rapport met statistisch significante verschillen en overlappingen tussen de twee soorten publiek.
* [ het Vergelijken van segmenten in reserve:](/help/analyze/analysis-workspace/visualizations/fallout/compare-segments-fallout.md) zie hoe de verschillende soorten publiek met elkaar in verband met een fallout visualisatie vergelijken.

## Meer informatie

Voor een diepgaande bespreking van segmentatie in Adobe Analytics, ga [ hier ](/help/components/segmentation/seg-overview.md).
