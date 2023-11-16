---
description: Documentatie waarin wordt beschreven hoe tabellen in Analysis Workspace worden gefilterd en gesorteerd.
title: Vrije-vormtabellen filteren en sorteren
feature: Freeform Tables
role: User, Admin
exl-id: 15fea9e2-f8d8-4489-9a44-e74a351b8f36
source-git-commit: e5f67042fce223f2998e4031962193b1c0154557
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 2%

---

# Vrije-vormtabellen filteren en sorteren

Vrije-vormtabellen in Analysis Workspace vormen de basis voor interactieve gegevensanalyse. Als zodanig kunnen ze duizenden rijen informatie bevatten. Het filteren en sorteren van de gegevens kan een essentieel onderdeel zijn van het efficiënt opzoeken van de belangrijkste informatie.

## Filtertabellen

Met filters in Analysis Workspace kunt u de belangrijkste informatie doornemen.

>[!NOTE]
>
> Alleen items met een dynamische dimensie kunnen worden gefilterd zoals in deze sectie wordt beschreven. Statische dimensie-items kunnen niet worden gefilterd. Zie voor meer informatie [Dynamische versus statische dimensie-items in vrije-vormtabellen](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/manual-vs-dynamic-rows.md).

## Rijen vrije-vormtabellen filteren

U kunt verschillende methoden gebruiken om rijen vanuit een vrije-vormtabel te filteren. 

- Klik op de X in de rij
- Klik met de rechtermuisknop > Geselecteerde rijen verwijderen
- Tabelfilters
- Segmentatie

Zorg ervoor dat u leest wat de invloed van elke methode is [Tabeltotalen voor vrije vorm](https://docs.adobe.com/content/help/nl-NL/analytics/analyze/analysis-workspace/build-workspace-project/workspace-totals.html).

### Snel specifieke rijen uitsluiten van een tabel

U kunt snel specifieke rijen van de lijst uitsluiten zonder het nodig hebben om de dialoog van de Filter te openen.

>[!NOTE]
>
>Wanneer u rijen zoals beschreven in deze sectie uitsluit, [!UICONTROL **Items altijd uitsluiten**] wordt automatisch toegepast in het dialoogvenster met geavanceerde filters. (U kunt de toegepaste regel weergeven door het pictogram Filter te selecteren en vervolgens [**[!UICONTROL Show advanced]**](#apply-a-simple-or-advanced-filter-to-a-table).)

Om specifieke rijen van een lijst van de Vrije vorm snel uit te sluiten:

1. Houd de cursor boven de rij die u wilt uitsluiten en selecteer vervolgens het x-pictogram.

   Houd Shift ingedrukt om een reeks rijen te selecteren of houd Command (in Mac) of Ctrl (in Windows) ingedrukt om meerdere rijen te selecteren.

### Klik met de rechtermuisknop > Geselecteerde rijen verwijderen

1. Selecteer 1 of meer rijen.
1. Klik met de rechtermuisknop en selecteer **[!UICONTROL Delete Selected Rows]**.

   Met deze actie verwijdert u de rijen uit de tabel en past u een tabelfilter toe.

### Een eenvoudig of geavanceerd filter toepassen op een tabel

Gegevens filteren in Freeform-tabellen:

1. Houd de muisaanwijzer boven de kolom met de gegevens die u wilt filteren. <!--only some types of columns show the filter... Which? Just Dimensions?-->

1. Selecteer de **Filter** wanneer deze wordt weergegeven.

   ![Filterpictogram in een tabel](assets/table-filter-icon.png)

   De volgende opties zijn beschikbaar:

   | Optie | -functie |
   |---------|----------|
   | [!UICONTROL **Woord of woordgroep zoeken**] | Geef een woord of woordgroep op waarop u wilt filteren. Alleen rijen die het opgegeven woord of de exacte woordgroep bevatten, worden weergegeven. |
   | [!UICONTROL **Inclusief niet-opgegeven (geen)**] | Selecteer deze optie om gegevens in de tabel weer te geven die niet in een van de afmetingen van de tabel vallen. <!--what is this?--> |

1. (Optioneel) Als u op verschillende criteria of op meerdere criteria wilt filteren, selecteert u [!UICONTROL **Geavanceerd tonen**].

   De volgende geavanceerde filteropties zijn beschikbaar:

   | Optie | -functie |
   |---------|----------|
   | [!UICONTROL **Inclusief niet-opgegeven (geen)**] | Selecteer deze optie om gegevens in de tabel weer te geven die niet in een van de afmetingen van de tabel vallen. <!--what is this?--> |
   | [!UICONTROL **Overeenkomst**] | <p>Kies [!UICONTROL **Als aan alle criteria is voldaan**] om alleen gegevens weer te geven die voldoen aan alle criteria die u opgeeft. Deze optie resulteert doorgaans in meer verfijnde gegevens.</p> <p>Kies [!UICONTROL **Als aan bepaalde criteria is voldaan**] om gegevens weer te geven die voldoen aan een van de filtercriteria die u opgeeft. Deze optie resulteert doorgaans in minder verfijnde gegevens.</p> |
   | [!UICONTROL **Criteria**] | <p>Selecteer een van de volgende filteropties:</p><p>(Selecteer [!UICONTROL **Rij toevoegen**] meerdere filtercriteria toevoegen. De optie die u selecteert in het dialoogvenster [!UICONTROL **Overeenkomst**] bepaalt of aan alle criteria die u toevoegt of aan alle criteria moet worden voldaan.)</p><ul><li><p>[!UICONTROL **Bevat de woordgroep**]: Alleen gegevens met de exacte woordgroep die u opgeeft, worden opgenomen in de gefilterde resultaten. Woorden moeten in de volgorde staan die is opgegeven in de [!UICONTROL **Woord- of woordveld zoeken**].<p>Dit is de standaardinstelling bij een eenvoudige zoekopdracht.</p></p></li><li><p>[!UICONTROL **Bevat een term**]: Alleen gegevens die een of meer woorden uit de opgegeven woordgroep bevatten, worden opgenomen in de gefilterde resultaten. </p></li><li><p>[!UICONTROL **Bevat alle termen**]: Alleen gegevens die alle woorden bevatten van de woordgroep die u opgeeft, worden opgenomen in de gefilterde resultaten. Woorden hoeven niet in de volgorde te staan die in de [!UICONTROL **Woord- of woordveld zoeken**].</p></li><li><p>[!UICONTROL **Bevat geen term**]: Alleen gegevens die geen woorden bevatten uit de woordgroep die u opgeeft, worden opgenomen in de gefilterde resultaten. </p></li><li><p>[!UICONTROL **Bevat niet de uitdrukking**]: Alleen gegevens die niet de exacte woordgroep bevatten die u opgeeft, worden opgenomen in de gefilterde resultaten. Woorden moeten in de volgorde staan die is opgegeven in de [!UICONTROL **Woord- of woordveld zoeken**].</p></li><li><p>[!UICONTROL **Gelijk**]: Alleen gegevens die exact overeenkomen met de woordgroep die u opgeeft, worden opgenomen in de gefilterde resultaten. </p></li><li><p>[!UICONTROL **Is niet gelijk aan**]: Alleen gegevens die niet exact overeenkomen met de woordgroep die u opgeeft, worden opgenomen in de gefilterde resultaten. </p></li><li><p>[!UICONTROL **Begint met**]: Alleen gegevens die beginnen met het woord of de exacte woordgroep die u opgeeft, worden opgenomen in de gefilterde resultaten. </p></li><li><p>[!UICONTROL **Eindigt met**]: Alleen gegevens die eindigen met het woord of de exacte woordgroep die u opgeeft, worden opgenomen in de gefilterde resultaten. </p></li></ul> |
   | [!UICONTROL **Items altijd uitsluiten**] | Geef de naam op van de items die u wilt uitsluiten van de gefilterde gegevens. |

1. Selecteren [!UICONTROL **Toepassen**] om de gegevens te filteren.

   De **Filter** pictogram ![Blauw filterpictogram gefilterde tabel](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Filter_18_N.svg) wordt blauw wanneer een filter op de lijst wordt toegepast.

### Segmentatie

Zie onze [Segmenteringsdocumentatie](https://docs.adobe.com/help/en/analytics/components/segmentation/seg-home.html) voor meer informatie .

## Tabellen sorteren

U kunt de gegevens van een lijst Freeform door om het even welke kolom in Analysis Workspace sorteren die metrisch is.

Pijl-omlaag ![Pijl-omlaag - pictogram gesorteerde tabelkolom](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ArrowDown_18_N.svg) is zichtbaar in de koptekst van de kolom waarop de gegevens momenteel worden gesorteerd.

De gegevens in een tabel voor vrije vorm sorteren op een bepaalde kolom:

1. Houd de muisaanwijzer boven de kolomtitel waarmee u de gegevens wilt sorteren.

2. Selecteer het pictogram Pijl-omlaag wanneer dit wordt weergegeven.

   ![Pijl-omlaag - pictogram gesorteerde tabelkolom](assets/table-sort.png)

   Tabelgegevens worden gesorteerd op de kolom die u hebt geselecteerd.
