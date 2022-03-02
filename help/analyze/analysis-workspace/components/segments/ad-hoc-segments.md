---
description: Gebruik ad-hocsegmenten in Analysis Workspace.
title: Ad-hocsegmenten
feature: Segmentation
role: User, Admin
exl-id: 1c189abc-ab9f-413c-9be6-0d2fc457230e
source-git-commit: f50e3d9a1d3c1705c55a14af0e42a0da3ac00955
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 1%

---

# Ad-hocprojectsegmenten

Met ad-hocprojectsegmenten kunt u een component rechtstreeks naar de neerzetzone van het deelvenster slepen om een segment te maken. Het segment wordt een [segment op projectniveau](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/segments/quick-segments.html?#what-are-project-only-segments%3F) lokaal aan het huidige project.

Hier volgt een video over het maken van ad-hocprojectsegmenten:

>[!VIDEO](https://video.tv.adobe.com/v/23978/?quality=12)

1. Zet om het even welk componenttype (afmeting, afmeting punt, gebeurtenis, metrisch, segment, segmentmalplaatje, datumwaaier) in de segment dalingsstreek bij de bovenkant van een paneel neer. Componenttypen worden automatisch omgezet in ad-hocsegmenten of [Snelle segmenten](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/segments/quick-segments.html) indien compatibel.
Hier ziet u hoe u een segment voor het Twitter-verwijzende domein kunt maken:

   ![](assets/ad-hoc1.png)

   Dit segment wordt automatisch toegepast in uw deelvenster en u kunt de resultaten direct zien.

1. U kunt een onbeperkt aantal segmenten aan een deelvenster toevoegen.
1. Raadpleeg de onderstaande sectie als u besluit dat u dit segment wilt opslaan.

Houd rekening met het volgende:

* U **kan** Zet de volgende componenttypen neer in de segmentzone: berekende metriek en afmetingen/metriek waarvan u geen segmenten kunt bouwen.
* Voor volledige afmetingen en gebeurtenissen maakt Analysis Workspace &#39;bestaande&#39; raaksegmenten. Voorbeelden: `Hit where eVar1 exists` of `Hit where event1 exists`.
* Als &quot;niet gespecificeerd&quot;of &quot;niets&quot;in de segment dalingsstreek wordt gelaten vallen, wordt het automatisch omgezet in een &quot;bestaat niet&quot;segment zodat het correct in segmentatie wordt behandeld.

Voor een vergelijking van de verschillende segmenten die u binnen een project kunt maken en toepassen, gaat u [hier](/help/analyze/analysis-workspace/components/segments/t-freeform-project-segment.md).

## Ad-hocsegmenten opslaan {#ad-hoc-save}

Ad-hocsegmenten kunnen beschikbaar worden gesteld aan andere projecten door ze op te slaan.

1. Houd de cursor boven het segment in de neerzetzone en klik op het pictogram &quot;i&quot;.
1. Klik het uitgeven potlood om naar de Bouwer van het Segment te gaan.
1. Controleren **[!UICONTROL Make available to all projects and add to your component list]**.
1. Klik op **[!UICONTROL SAVE]**.

Zodra bewaard, is het segment beschikbaar in uw linkerspoorcomponentenlijst en kan met andere gebruikers van de Manager van het Segment worden gedeeld.
