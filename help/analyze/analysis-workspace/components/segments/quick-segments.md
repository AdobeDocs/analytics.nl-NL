---
description: Gebruik snelle segmenten in Analysis Workspace.
title: Snelle segmenten
feature: Workspace Basics
role: User, Admin
source-git-commit: 34824daca188119bfe366fea101053f2547a2f6d
workflow-type: tm+mt
source-wordcount: '741'
ht-degree: 1%

---


# Snelle segmenten

U kunt snelle segmenten binnen een project tot stand brengen om de ingewikkeldheid van volledige [segmentbouwer](/help/components/segmentation/segmentation-workflow/seg-build.md) te mijden. Snelle segmenten

* Alleen van toepassing op projecten waarin ze zijn gemaakt (u kunt dit wijzigen).
* Sta voor maximaal 3 regels toe.
* Plaats geen geneste containers of opeenvolgende regels.
* Werken in projecten met meerdere rapportsuites.

Voor een vergelijking van wat de snelle segmenten versus volledig-afgewerkte component-lijst segmenten kunnen doen, ga [hier](/help/analyze/analysis-workspace/components/segments/t-freeform-project-segment.md).

>[!IMPORTANT]
> Snelle segmenten worden momenteel beperkt getest en zijn nog niet algemeen beschikbaar.

## Vereisten

Iedereen kan een [!UICONTROL Quick Segment] creëren. Nochtans, hebt u [!UICONTROL Segment Creation] toestemming in [Adobe Admin Console](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/permissions/summary-tables.html?lang=en#analytics-tools) nodig om een snelle segmenten te kunnen bewaren of het in [!UICONTROL Segment Builder] te openen.

## Snelle segmenten maken

Klik in een tabel voor vrije vorm op het pictogram filter+ in de koptekst van het deelvenster:

![](assets/quick-seg1.png)

| Instelling | Beschrijving |
| --- | --- |
| Naam | De standaardnaam van een segment is een combinatie van de regelnamen in het segment. U kunt de naam van het segment wijzigen. |
| Opnemen/uitsluiten | U kunt of componenten in uw segmentdefinitie omvatten of uitsluiten, maar niet allebei. |
| Handje/Bezoek/Bezoeker container | De snelle segmenten omvatten één [segmentcontainer](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-overview.html?lang=en#section_AF2A28BE92474DB386AE85743C71B2D6) slechts die u een afmeting/metrisch/datumwaaier in (of het van) het segment laat uitsluiten. [!UICONTROL Visitor] bevat overkoepelende gegevens die specifiek zijn voor de bezoeker in verschillende bezoeken en paginaweergaven. Met een container [!UICONTROL Visit] kunt u regels instellen om de gegevens van de bezoeker op basis van bezoeken af te splitsen. Met een container [!UICONTROL Hit] kunt u bezoekersinformatie afsplitsen op basis van afzonderlijke paginaweergaven. De standaardcontainer is [!UICONTROL Hit]. |
| Onderdelen (Dimension/metrisch/datumbereik) | Definieer maximaal 3 regels door de afmetingen en/of metriek en/of datumbereiken en hun waarden toe te voegen. Er zijn drie manieren om de juiste component te vinden:<ul><li>Begin het typen en [!UICONTROL Quick Segment] bouwer vindt automatisch de aangewezen component.</li><li>Gebruik de vervolgkeuzelijst om de component te zoeken.</li><li>Sleep componenten vanuit de linkerspoorstaaf.</li></ul> |
| Operator | Gebruik het vervolgkeuzemenu om standaardoperatoren en [!UICONTROL Distinct Count]-operatoren te zoeken. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segment-reference/seg-operators.html?lang=en) |
| plusteken (+) | Een andere regel toevoegen |
| EN/OF kwalificatietekens | U kunt &quot;EN&quot;of &quot;OF&quot;bepalende eigenschappen aan de regels toevoegen, maar u kunt &quot;EN&quot;en &quot;OF&quot;in één enkele segmentdefinitie niet mengen. |
| Toepassen | Pas dit segment toe op het deelvenster. Als het segment geen gegevens bevat, wordt u gevraagd of u wilt doorgaan. |
| Opbouwfunctie openen | Opent de Segment Builder. Zodra u het segment in de Bouwer van het Segment opslaat, wordt het niet meer beschouwd als een &quot;Snel Segment&quot;. Het wordt deel van de component-lijst segmentbibliotheek. |
| Annuleren | Annuleer dit snelle segment - pas het niet toe. |
| Datumbereik | De validator gebruikt het datumbereik van het deelvenster voor het opzoeken van de gegevens. Maar elk datumbereik dat in een snel segment wordt toegepast, overschrijft het datumbereik van het deelvenster boven in het deelvenster. |
| Voorvertoning (rechtsboven) | Hiermee kunt u zien of u een geldig segment hebt en hoe breed het segment is. Geeft de uitsplitsing aan van de gegevensset die u kunt verwachten wanneer u dit segment toepast. u zou een bericht kunnen krijgen dat erop wijst dat dit segment geen gegevens heeft. U kunt doorgaan of de segmentdefinitie wijzigen. |

Hier is een voorbeeld van een segment waarin afmetingen en metriek worden gecombineerd:

![](assets/quick-seg2.png)

Het segment wordt bovenaan weergegeven. Let op de zijbalk met een blauw streepjespatroon, in tegenstelling tot de blauwe zijbalk voor segmenten op componentniveau in de segmentbibliotheek aan de linkerkant.

![](assets/quick-seg5.png)

## Snel segmenten bewerken

1. Houd de cursor boven het snelle segment en selecteer het potloodpictogram.
1. Bewerk de segmentdefinitie en/of de segmentnaam.
1. Klik op [!UICONTROL Apply].

## Snelle segmenten opslaan

>[!IMPORTANT]
>Zodra u sparen of het segment toepast, kunt u het niet meer uitgeven in de Snelle Bouwer van het Segment, slechts in de regelmatige Bouwer van het Segment.

1. Zodra u het snelle segment hebt toegepast, houdt u de muisaanwijzer boven het segment en selecteert u het pictogram Info (&quot;i&quot;).

   ![](assets/quick-seg6.png)

1. Klik op **[!UICONTROL Make available to all projects and add to your component list]**.
1. (Optioneel) Wijzig de naam van het segment.
1. Klik op **[!UICONTROL Save]**.

U ziet hoe de zijbalk van het segment verandert van gestreept blauw in blauw. Het wordt nu weergegeven in uw lijst met componenten in de linkerrails.

## Wat zijn projectgebonden segmenten?

De project-enige segmenten zijn of snelle segmenten of de projectsegmenten van de ad-hoc Werkruimte. Wanneer het uitgeven van/het openen van hen in [!UICONTROL Segment Builder], zal het project-enige vakje verschijnen. Als u een snel segment toepast in de builder maar niet het vakje ter beschikking stellen controleert, dan is het nog een project-slechts segment maar het kan niet meer in [!UICONTROL Quick Segment Builder] worden geopend. Als u het vakje controleert en **[!UICONTROL SAVE]** klikt, is het nu een component-lijst segment.