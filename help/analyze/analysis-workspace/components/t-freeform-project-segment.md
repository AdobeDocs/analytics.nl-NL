---
description: Gebruik segmenten in Analysis Workspace.
title: Segmenten
uuid: 677f6030-5b3e-4dfa-bb79-9f27f3382fb1
feature: Workspace Basics
role: User, Admin
exl-id: 67112e13-4d0a-4d77-be50-496c3d28779c
source-git-commit: 76072b45114a15d9b366657ea81872035965e5b6
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 1%

---

# Segmenten {#topic_DC2917A2E8FD4B62816572F3F6EDA58A}

## Segment per spoor {#section_3B07D458C43E42FDAF242BB3ACAF3E90}

Het segmentspoor onder het menu van Componenten toont segmenten evenals segmentmalplaatjes, zoals die door deze pictogrammen worden bedoeld:

![](assets/segment_icons.png)

[Segmenten gebruiken in Analysis Workspace](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/applying-segments/using-segments-in-analysis-workspace.html) (6:46)

## Segmenten maken {#section_693CFADA668B4542B982446C2B4CF0F5}

U kunt onmiddellijke segmenten tot stand brengen door om het even welk componententype (afmeting, afmetingpunt, gebeurtenis, metrisch, segment, segmentmalplaatje, datumwaaier) in de segment dalingsstreek bij de bovenkant van een paneel te laten vallen.

Componenttypen worden automatisch omgezet in segmenten. U kunt ook op het plusteken (+) klikken in de vervolgkeuzelijst Segment toevoegen.

Houd er rekening mee dat:

* U **kunt niet** de volgende componenttypen in de segmentzone laten vallen: berekende metriek en afmetingen/metriek waarvan u geen segmenten kunt bouwen.
* Voor volledige afmetingen en gebeurtenissen maakt Analysis Workspace &#39;bestaande&#39; raaksegmenten. Voorbeelden: &quot;Druk op de plaats waar eVar1 bestaat&quot; of &quot;druk op de plaats waar event1 bestaat&quot;.
* Als &quot;niet gespecificeerd&quot;of &quot;niets&quot;in de segment dalingsstreek wordt gelaten vallen, wordt het automatisch omgezet in een &quot;bestaat niet&quot;segment zodat het correct in segmentatie wordt behandeld.

![](assets/segment-dropzone.png)

>[!NOTE]
>
>Segmenten die op deze manier worden gemaakt, bevinden zich intern in het project.

U kunt ervoor kiezen om deze segmenten openbaar (algemeen) te maken door de volgende stappen uit te voeren:

1. Houd de cursor boven het segment in de neerzetzone en klik op het pictogram &quot;i&quot;.
1. Klik in het informatievenster dat wordt weergegeven op **[!UICONTROL Make public]**.

   ![](assets/segment-info.png)

## Andere methoden voor het toepassen van segmenten {#section_10FF2E309BA84618990EA5B473015894}

>[!VIDEO](https://video.tv.adobe.com/v/30994/?quality=12)

Er bestaan verschillende andere methoden voor het toepassen van segmenten op een vrije-vormproject.

| Handeling | Beschrijving |
|--- |--- |
| Segment maken van selectie | Maak een inline-segment. Selecteer rijen, klik met de rechtermuisknop op de selectie en maak vervolgens een inline-segment. Dit segment is alleen van toepassing op het geopende project en wordt niet opgeslagen als een analysesegment. 1. Selecteer rijen.  2. Klik met de rechtermuisknop op de selectie.  3. Klik *Segment maken van selectie*. |
| Componenten > Nieuw segment | Toont de Bouwer van het Segment. Zie [Segment Builder](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) voor meer informatie over segmentatie. |
| Delen > Project delen of Delen > Projectgegevens krommen | In [Curate en Aandeel](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/curate.html#concept_4A9726927E7C44AFA260E2BB2721AFC6), leer hoe de segmenten die u op het project toepast in gedeelde analyse voor de ontvanger beschikbaar zijn. |
| Segmenten gebruiken als Dimension | Video: [Segmenten gebruiken als Dimension in Analysis Workspace](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/applying-segments/using-segments-as-dimensions-in-analysis-workspace.html?lang=en) |

## Ad-hocsegmenten (tijdelijk) in Analysis Workspace

Hier volgt een video over ad-hocsegmenten:

>[!VIDEO](https://video.tv.adobe.com/v/23978/?quality=12)
