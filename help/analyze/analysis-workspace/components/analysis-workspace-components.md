---
description: Componenten in Analysis Workspace bestaan uit afmetingen, metriek, segmenten en datumbereiken die u naar een project kunt slepen en neerzetten.
title: Overzicht van onderdelen
feature: Components
role: User, Admin
exl-id: e2c98c77-64ee-4349-956a-3ab092e36017
source-git-commit: c64b4199d93443b14e2012459a4d33fdd847eca1
workflow-type: tm+mt
source-wordcount: '1143'
ht-degree: 3%

---

# Overzicht van onderdelen

Componenten in Analysis Workspace bestaan uit afmetingen, metriek, segmenten en datumbereiken die u naar een project kunt slepen en neerzetten.

Als u het menu Componenten wilt openen, klikt u op de knop **[!UICONTROL Components]** in de linkerspoorstaaf. U kunt schakelen tussen [Deelvensters](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html), [Visualisaties](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html)en componenten van de linkerspoorpictogrammen of met behulp van [sneltoetsen](/help/analyze/analysis-workspace/build-workspace-project/fa-shortcut-keys.md).

![](assets/component-overview.png)

U kunt ook de [Dichtheidsinstellingen weergeven](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/view-density.html) voor het project kunnen in één keer meer waarden in het linkerspoor worden opgetekend door naar **[!UICONTROL Project > Project Info & Settings > View Density]**.

## Dimensies {#dimensions}

[**Dimension**](https://experienceleague.adobe.com/docs/analytics/components/dimensions/overview.html) Dit zijn tekstkenmerken die het gedrag van de bezoeker beschrijven en die u in uw analyse kunt bekijken, splitsen en vergelijken. Ze zijn te vinden in de linkercomponentrails (oranje sectie) en worden doorgaans toegepast als rijen van een tabel.

Voorbeelden van afmetingen zijn [!UICONTROL Page Name], [!UICONTROL Marketing Channels], [!UICONTROL Device Type], en [!UICONTROL Products]. Dimension worden geleverd door Adobe en worden vastgelegd via uw aangepaste implementatie (eVar, Props, classificaties, enz.).

Elke dimensie bevat ook **dimensieitems** erin. U vindt Dimension-items in de linkercomponentrails door op de pijl naar rechts naast de naam van een willekeurige dimensie te klikken (de items zijn geel).

Voorbeelden van dimensie-items zijn [!UICONTROL Homepage] (binnen de [!UICONTROL Page] dimensie), [!UICONTROL Paid Search] (binnen de [!UICONTROL Marketing Channel] dimensie), [!UICONTROL Tablet] (binnen de [!UICONTROL Mobile Device Type] dimensie), enzovoort.

![](assets/dimensions.png)

## Metrics {#metrics}

[**Metrisch**](https://experienceleague.adobe.com/docs/analytics/components/metrics/overview.html) zijn kwantitatieve maatstaven voor het gedrag van bezoekers. Ze zijn te vinden in het linkerspoor van de component (groene sectie) en worden doorgaans toegepast als kolommen van een tabel.

Voorbeelden van metriek zijn: [!UICONTROL Page views], [!UICONTROL Visits], [!UICONTROL Orders], [!UICONTROL Average Time spent], en [!UICONTROL Revenue/Order]. Metriek worden geleverd door Adobe of vastgelegd via uw aangepaste implementatie ([!UICONTROL Success events]), of gemaakt met de [Berekende metrische builder](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-build-metrics.html).

![](assets/metrics.png)

## Segmenten {#segments}

[**Segmenten**](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/segments/t-freeform-project-segment.html) Dit zijn publieksfilters die worden toegepast op uw analyse. Ze zijn te vinden in de linkercomponentrails (blauw gedeelte) en worden doorgaans toegepast boven aan een deelvenster of boven metrische kolommen in een tabel.

Voorbeelden van segmenten zijn [!UICONTROL Mobile Device Visitors], [!UICONTROL Visits from Email], en [!UICONTROL Authenticated Hits]. Segmenten worden geleverd door Adobe of gemaakt in het dialoogvenster [dropzone van deelvenster](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html)of gemaakt met de [Segment builder](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html).

![](assets/segments.png)

## Datumbereik {#date-ranges}

[**Datumbereik**](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/calendar-date-ranges/calendar.html) Dit zijn de datums waarop u de analyse uitvoert. Ze zijn te vinden in de linkercomponentrails (paarse sectie) en worden doorgaans toegepast in de kalender van elk deelvenster.

U kunt de componenten van het datumbereik relatief maken ten opzichte van de deelvensterkalender. Zie voor meer informatie [Over datumbereiken in het relatieve deelvenster](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md#relative-panel-dates).

Voorbeelden van datumbereiken zijn juli 2019. [!UICONTROL Last 4 weeks], en [!UICONTROL This month]. Datumbereiken worden opgegeven door Adobe, toegepast in het dialoogvenster [paneelkalender](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html)of gemaakt met de [Bouwer van datumbereik](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.html).

![](assets/date-ranges.png)


## Componenten beheren {#actions}

U kunt componenten rechtstreeks in de linkerspoorstaaf beheren.

1. Klik met de rechtermuisknop op een component.

   of

   Selecteer een component en selecteer vervolgens de **Handeling** (3 punten) boven aan de lijst met componenten.

   >[!TIP]
   >
   >   U kunt meerdere componenten selecteren door Shift ingedrukt te houden of door Command (in Mac) of Ctrl (in Windows) ingedrukt te houden.


   ![](assets/component-actions.png)

   | Component, actie | Beschrijving |
   |--- |--- |
   | [!UICONTROL **Tag**] | U kunt componenten ordenen of beheren door er tags op toe te passen. U kunt vervolgens zoeken op tag in de linkertrack door op het filter te klikken of # te typen. Tags fungeren ook als filters in de componentmanagers. |
   | [!UICONTROL **Favorieten**] | Voeg de component toe aan de lijst met favorieten. Net als tags kunt u zoeken op Favorieten in het linkerspoor en deze filteren in de componentmanagers. |
   | [!UICONTROL **Goedkeuren**] | Markeer componenten zoals Goedgekeurd om aan uw gebruikers te laten weten dat de component door de organisatie is goedgekeurd. Net als tags kunt u zoeken op Goedgekeurd in de linkertrack en door hen filteren in de componentmanagers. |
   | [!UICONTROL **Delen**] | Delen van componenten naar gebruikers in uw organisatie. Deze optie is alleen beschikbaar voor aangepaste componenten, zoals segmenten of berekende maateenheden. |
   | [!UICONTROL **Verwijderen**] | Verwijder componenten die u niet meer nodig hebt. Deze optie is alleen beschikbaar voor aangepaste componenten, zoals segmenten of berekende maateenheden. |

De componenten van de douane kunnen ook door hun respectieve managers van de Component worden beheerd. De [Segmentbeheer](/help/components/segmentation/segmentation-workflow/seg-manage.md).

## De componentenlijst zoeken, filteren en sorteren

U kunt zoeken, filteren en sorteren de componentenlijst in de linkerspoor van Analysis Workspace om van een bepaalde component snel de plaats te bepalen.

### De componentenlijst doorzoeken

1. Selecteer **Componenten** pictogram ![Pictogram Componenten](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Curate_18_N.svg) in het linkerspoor.

2. Typ in het zoekveld de naam van de component die u in het project wilt gebruiken.

   Het type component kan door zowel kleur als pictogram worden geïdentificeerd. **Dimension** ![Dimension-pictogram](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Data_18_N.svg) oranje zijn, **Segmenten** ![Segmentpictogram](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Segmentation_18_N.svg) blauw zijn, **Datumbereiken** ![Pictogram Datumbereik](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calendar_18_N.svg) paars zijn, en **Metrisch** ![Metrisch pictogram](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Event_18_N.svg) zijn groen. Het Adobe-pictogram geeft een berekende metrische sjabloon of een segmentsjabloon aan en het rekenatorpictogram ![Pictogram Rekenmachine](assets/calculated-metric-icon-created.png) wees op berekende metrisch die door een beheerder van Analytics in uw organisatie werd gecreeerd.

3. Selecteer de component wanneer deze in de vervolgkeuzelijst wordt weergegeven.

### De componentlijst filteren

1. Selecteer **Componenten** pictogram ![Pictogram Componenten](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Curate_18_N.svg) in het linkerspoor.

2. Selecteer **Filter** pictogram ![Filter gegevenswoordenboek, pictogram](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Filter_18_N.svg).

   of

   Typ het hekje (#) in het zoekveld.

3. Selecteer een van de volgende filteropties om de lijst met componenten te filteren:

   | Optie | -functie |
   |---------|----------|
   | [!UICONTROL **Goedgekeurd**] | Alleen componenten tonen die zijn gemarkeerd als goedgekeurd door een beheerder. |
   | [!UICONTROL **Favorieten**] | Alleen componenten tonen die zich in de lijst Favorieten bevinden. Voor informatie over het toevoegen van componenten aan uw lijst van favorieten, zie [Overzicht van componenten](/help/analyze/analysis-workspace/components/analysis-workspace-components.md). |
   | [!UICONTROL **Dimensies**] | Alleen componenten weergeven die Dimension zijn. |
   | [!UICONTROL **Cijfers**] | Alleen componenten weergeven die Metrisch zijn. |
   | [!UICONTROL **Segmenten**] | Alleen componenten tonen die Segmenten zijn. <!--this is Filters in CJA--> |
   | [!UICONTROL **Datumbereiken**] | Alleen componenten tonen die Datumbereik hebben. |
   | [!UICONTROL **Alles tonen**] | Alle componenten tonen. Deze optie is alleen beschikbaar voor beheerders. |
   | [!UICONTROL **Niet goedgekeurd**] | Alleen componenten tonen die nog niet zijn gemarkeerd als goedgekeurd door een beheerder. Als beheerder, is dit nuttig wanneer het identificeren van componenten die uw overzicht en goedkeuring vereisen. Deze optie is alleen beschikbaar voor beheerders. |

4. (Optioneel) Als u de lijst verder wilt uitlijnen, kunt u de lijst met componenten sorteren, zoals beschreven in [De componentlijst sorteren](#sort-the-component-list).

### De componentlijst sorteren

{{release-limited-testing-section}}

1. (Optioneel) Pas filters toe op de lijst met componenten, zoals beschreven in [De componentlijst filteren](#filter-the-component-list).

2. Selecteer **Componenten** pictogram ![Pictogram Componenten](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Curate_18_N.svg) in het linkerspoor.

3. Selecteer **Sorteren** pictogram ![Pictogram Componenten sorteren](https://spectrum.adobe.com/static/icons/workflow_18/Smock_SortOrderDown_18_N.svg)Selecteer vervolgens een van de volgende filteropties om de lijst met componenten te sorteren:

   {{components-sort-options}}
