---
description: Gebruik snelle segmenten in Analysis Workspace.
title: Snelle segmenten
feature: Workspace Basics
role: User, Admin
source-git-commit: f3185f1ee341348fb7bdbaab8b68d421e7c79076
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---


# Snelle segmenten

U kunt snelle segmenten binnen een project tot stand brengen om de ingewikkeldheid van volledige [segmentbouwer](/help/components/segmentation/segmentation-workflow/seg-build.md) te mijden. Voor een vergelijking van wat de snelle segmenten versus volledig-afgewerkte component-lijst segmenten kunnen doen, ga [hier](/help/analyze/analysis-workspace/components/segments/t-freeform-project-segment.md).

>[!IMPORTANT]
> Snelle segmenten worden momenteel beperkt getest en zijn nog niet algemeen beschikbaar.

## Snelle segmenten maken

1. Klik in een tabel voor vrije vorm op het pictogram filter+ in de koptekst van het deelvenster:

   ![](assets/quick-seg1.png)

   Let op:

   - Er is één segmentcontainer slechts die u een afmeting/metrisch/datumwaaier in (of het van) het segment laat uitsluiten laat omvatten.
   - U kunt de container instellen op Actief, Bezoek of Bezoekerniveau. Standaard is Actief.

1. Voeg op drie manieren een dimensie/metrisch/datumbereik toe:

   - Begin te typen en [!UICONTROL Quick Segment builder] vindt automatisch de aangewezen component.
   - Gebruik de vervolgkeuzelijst om de component te zoeken.
   - Sleep componenten vanuit de linkerspoorstaaf.

1. Geef de eerste regel op, bijvoorbeeld `Page equals workspace`. U kunt tot drie regels in een segmentdefinities hebben. Klik op het plusteken (+) om een andere regel toe te voegen. U kunt &quot;EN&quot;of &quot;OF&quot;bepalende eigenschappen aan de regels toevoegen, maar u kunt &quot;EN&quot;en &quot;OF&quot;in één enkele segmentdefinitie niet mengen.

   Hier is een voorbeeld van een segment waarin afmetingen en metriek worden gecombineerd:

   ![](assets/quick-seg2.png)

1. Klik **[!UICONTROL Apply]** om dit segment op het paneel toe te passen.
Het segment wordt bovenaan weergegeven. Let op de grijze zijbalk in tegenstelling tot de blauwe zijbalk voor segmenten op componentniveau in de segmentbibliotheek aan de linkerkant.

   ![](assets/quick-seg3.png)

## Snel segmenten bewerken

1. Houd de cursor boven het snelle segment en selecteer het potloodpictogram.
1. Bewerk de segmentdefinitie of de segmentnaam.

## Snelle segmenten opslaan

U kunt snelle segmenten opslaan door deze stappen te volgen.

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