---
description: Gebruik snelle segmenten in Analysis Workspace.
title: Snelle segmenten
feature: Workspace Basics
role: User, Admin
source-git-commit: ef232d1227430bb2430ca1da09756f5dd5106b1f
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 0%

---


# Snelle segmenten

U kunt snelle segmenten binnen een project tot stand brengen om de ingewikkeldheid van volledige [segmentbouwer](/help/components/segmentation/segmentation-workflow/seg-build.md) te mijden. Voor een vergelijking van wat de snelle segmenten versus volledig-afgewerkte component-lijst segmenten kunnen doen, ga [hier](/help/analyze/analysis-workspace/components/segments/t-freeform-project-segment.md). De snelle segmenten staan voor maximaal 3 regels toe en passen geen genestelde containers, of opeenvolgende segmenten aan.

>[!IMPORTANT]
> Snelle segmenten worden momenteel beperkt getest en zijn nog niet algemeen beschikbaar.

## Snelle segmenten maken

Klik in een tabel voor vrije vorm op het pictogram filter+ in de koptekst van het deelvenster:

![](assets/quick-seg1.png)

| Instelling | Beschrijving |
| --- | --- |
| Naam | De standaardnaam van een segment is een combinatie van de regels in het segment. U kunt de naam van het segment wijzigen. |
| Opnemen/uitsluiten | U kunt componenten in uw segmentdefinitie omvatten of uitsluiten, maar niet allebei. |
| Handje/Bezoek/Bezoeker container | De snelle segmenten omvatten één [segmentcontainer](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-overview.html?lang=en#section_AF2A28BE92474DB386AE85743C71B2D6) slechts die u een afmeting/metrisch/datumwaaier in (of het van) het segment laat uitsluiten. [!UICONTROL Visitor] bevat overkoepelende gegevens die specifiek zijn voor de bezoeker in verschillende bezoeken en paginaweergaven. Met een container [!UICONTROL Visit] kunt u regels instellen om de gegevens van de bezoeker op basis van bezoeken af te splitsen. Met een container [!UICONTROL Hit] kunt u bezoekersinformatie afsplitsen op basis van afzonderlijke paginaweergaven. De standaardcontainer is [!UICONTROL Hit]. |
| Onderdelen (Dimension/metrisch/datumbereik) | Definieer maximaal 3 regels door de afmetingen van componenten en/of metriek en/of datumbereiken toe te voegen. Er zijn drie manieren om de juiste component te vinden:<ul><li>Begin het typen en [!UICONTROL Quick Segment] bouwer vindt automatisch de aangewezen component.</li><li>Gebruik de vervolgkeuzelijst om de component te zoeken.</li><li>Sleep componenten vanuit de linkerspoorstaaf.</li></ul> |
| Operator | Gebruik het vervolgkeuzemenu om standaardoperatoren zoals `contains` en [!UICONTROL Distinct Count] te zoeken. |
| plusteken (+) | Een andere regel toevoegen |
| en/of kwalificaties | U kunt &quot;EN&quot;of &quot;OF&quot;bepalende eigenschappen aan de regels toevoegen, maar u kunt &quot;EN&quot;en &quot;OF&quot;in één enkele segmentdefinitie niet mengen. |
| Toepassen | Pas dit segment toe op het deelvenster. |
| Opbouwfunctie openen | Opent de Segment Builder. |
| Annuleren | Annuleer dit snelle segment - pas het niet toe. |
| Datumbereik | De validator gebruikt het datumbereik van het deelvenster voor het opzoeken van de gegevens. Maar elk datumbereik dat in een snel segment wordt toegepast, overschrijft het datumbereik van het deelvenster boven in het deelvenster. |
| Voorvertoning (rechtsboven) | Hiermee kunt u zien of u een geldig segment hebt en hoe breed het segment is. Geeft de uitsplitsing aan van de gegevensset die u kunt verwachten wanneer u dit segment toepast. |

Hier is een voorbeeld van een segment waarin afmetingen en metriek worden gecombineerd:

![](assets/quick-seg2.png)

Het segment wordt bovenaan weergegeven. Let op de grijze zijbalk in tegenstelling tot de blauwe zijbalk voor segmenten op componentniveau in de segmentbibliotheek aan de linkerkant.

![](assets/quick-seg3.png)

## Snel segmenten bewerken

1. Houd de cursor boven het snelle segment en selecteer het potloodpictogram.
1. Bewerk de segmentdefinitie of de segmentnaam.

## Snelle segmenten opslaan

U kunt snelle segmenten opslaan in de constructor Quick Segments of door deze stappen uit te voeren.

>[!IMPORTANT]
>Zodra u sparen of het segment toepast, kunt u het niet meer uitgeven in de Snelle Bouwer van het Segment, slechts in de regelmatige Bouwer van het Segment.

1. Houd de muisaanwijzer boven het snelsegment en selecteer het pictogram Info (&quot;i&quot;).
1. **[!UICONTROL Save segment]** selecteren

   ![](assets/save-quick-seg.png)

1. Laat de naam ongewijzigd of wijzig de naam van het segment.

   Ga terug naar Workspace en zie hoe het segment nu een blauw zijpaneel heeft. Dit geeft aan dat het bestand niet langer kan worden bewerkt of geopend in de Quick Segment Builder. En door het op te slaan, wordt het onderdeel van de componentenlijst.

   ![](assets/quick-seg4.png)

Nadat u het segment hebt toegepast, kunt u verkiezen om het aan uw lijst van de segmentcomponent toe te voegen en het ter beschikking te stellen van al uw projecten.

1. Houd de cursor boven het opgeslagen segment en selecteer het potloodpictogram.

1. Boven aan de Segment Builder ziet u dit dialoogvenster:

   ![](assets/project-only.png)

1. Selecteren naast **[!UICONTROL Make this segment available to all your projects and add it to your component list.]**
1. Klik op **[!UICONTROL Save]**.
1. Het segment verschijnt nu in uw lijst van de segmentcomponent voor al uw projecten.
1. U kunt ook [het segment](/help/components/segmentation/segmentation-workflow/t-seg-share.md) met andere mensen in uw organisatie delen.

## Wat zijn projectgebonden segmenten?

De project-enige segmenten zijn of snelle segmenten of de projectsegmenten van de ad-hoc Werkruimte. Wanneer het uitgeven van/het openen van hen in de segmentbouwer dan zal het project-enige vakje verschijnen. Als ze een snel segment toepassen in de builder maar het selectievakje voor het beschikbaar stellen niet inschakelen, is het segment nog steeds een segment dat alleen in het project kan worden geopend, maar niet meer in de builder voor kwaliteitscontrole. Als zij de doos controleren en OPSLAAN is het nu een component-lijst segment.