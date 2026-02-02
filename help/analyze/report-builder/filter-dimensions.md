---
title: Filterafmetingen in Report Builder
description: Leer hoe u afmetingen filtert in Report Builder.
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: 43f48abf-951d-4fd1-afd4-58304ee5247b
source-git-commit: ba4fe682d717e8a90d87eaa5244a269f49a4a00a
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 1%

---

# Filterafmetingen


Door gebrek, keert elk afmetingspunt in de lijst top 10 punten voor die afmeting terug.

Om de afmetingspunten te veranderen die voor elke afmeting worden teruggekeerd:

1. Selecteer een cel in het gegevensblok.

1. Selecteer ![&#x200B; uitgeven &#x200B;](/help/assets/icons/Edit.svg) **[!UICONTROL Edit data block]** in het **[!UICONTROL Commands]** paneel.

1. Selecteer **[!UICONTROL Next]** om de tab **[!UICONTROL Dimensions]** weer te geven.

1. Selecteer ![&#x200B; MoreSmall &#x200B;](/help/assets/icons/MoreSmall.svg) naast een componentennaam in de lijst.

   ![&#x200B; de pictogramopties van de ellips.](./assets/image27.png){zoomable="yes"}

1. Selecteer **[!UICONTROL Filter dimension]** in het pop-upmenu om het deelvenster **[!UICONTROL Filter dimension]** weer te geven.

1. Selecteer **populairste** of **Specifiek** als **[!UICONTROL Type]**.

   ![&#x200B; de specifieke optie die in de ruit van de afmeting van de Filter wordt geselecteerd.](./assets/image28.png){zoomable="yes"}

1. Selecteer aangewezen die opties op het [&#x200B; worden gebaseerd gekozen filtertype &#x200B;](#filter-type).

1. Selecteer **[!UICONTROL Apply]** om het filter toe te voegen.

1. Report Builder geeft een melding weer ter bevestiging van het toegevoegde filter.

Houd de muisaanwijzer boven een dimensie om toegepaste filters weer te geven. De afmetingen met toegepaste filters tonen a ![&#x200B; filter &#x200B;](/help/assets/icons/Filter.svg) filterpictogram naast de afmetingsnaam.

## Het filter en de sorteervolgorde wijzigen

A ![&#x200B; ArrowUp &#x200B;](/help/assets/icons/ArrowUp.svg) of ![&#x200B; ArrowDown &#x200B;](/help/assets/icons/ArrowDown.svg) verschijnt naast metrisch die wordt gebruikt om het gegevensblok te filtreren en te sorteren. De richting van de pijl geeft aan of de metrische waarde in oplopende of aflopende volgorde wordt gesorteerd.

De sorteervolgorde wijzigen:

- Selecteer ![&#x200B; ArrowUp &#x200B;](/help/assets/icons/ArrowUp.svg) of ![&#x200B; ArrowDown &#x200B;](/help/assets/icons/ArrowDown.svg) naast metrisch om de soortorde van een knevel te voorzien.

U wijzigt als volgt de metrische waarde die wordt gebruikt voor het filteren en sorteren van het gegevensblok:

1. Houd de muisaanwijzer boven de gewenste metrische component in de Tabelbouwer om aanvullende opties weer te geven.

2. Selecteer ![&#x200B; ArrowDown &#x200B;](/help/assets/icons/ArrowDown.svg) voor aangewezen metrisch.

   ![&#x200B; de bouwer en metriek van de Lijst.](./assets/image30.png){zoomable="yes"}



## Filtertype

Er zijn twee manieren om afmetingspunten te filtreren: [&#x200B; populairste &#x200B;](#most-popular) en [&#x200B; Specifieke &#x200B;](#specific-filtering)

### **[!UICONTROL Most popular]**

Met de optie **[!UICONTROL Most popular]** kunt u dimensie-items dynamisch filteren op basis van metrische waarden. De populairste winst de hoogste gerangschikte afmetingspunten die op metrische waarden worden gebaseerd. Standaard worden de eerste 10 dimensies weergegeven, gesorteerd op de eerste metrische waarde die aan het gegevensblok is toegevoegd.

![&#x200B; de populairste optie.](./assets/image29.png){zoomable="yes"}


#### Opties voor Pagina en Rijen

Gebruik de velden **[!UICONTROL Page]** en **[!UICONTROL Rows]** om gegevens te verdelen in opeenvolgende groepen of pagina&#39;s. Met deze functie kunt u gerangschikte rijwaarden buiten de bovenste waarden in uw rapport opnemen. En is vooral nuttig om gegevens voorbij de 50.000 rijgrens te trekken.

De standaardwaarde voor Pagina is `1` en voor Rijen is `10` . Deze standaardinstellingen impliceren dat elke pagina 10 rijen gegevens heeft. Pagina 1 retourneert de bovenste 10 items, pagina 2 retourneert de volgende 10 items, enzovoort.

In de onderstaande tabel staan voorbeelden van pagina- en rijwaarden en de resulterende uitvoer.

| Pagina | Rij | Uitvoer |
|------|--------|----------------------|
| 1 | 10 | Meest 10 items |
| 2 | 10 | Punten 11-20 |
| 1 | 100 | Top 100 van items |
| 2 | 100 | Items 101-200 |
| 2 | 50.000 | Items 50.001-100.000 |

In de onderstaande tabel worden de minimum- en maximumwaarden voor pagina en rijen weergegeven.

|       | Minimumwaarden | Maximumwaarden |
|-------|---------------:|---------------:|
| Beginpagina | 1 | 50 miljoen |
| Aantal rijen | 1 | 50.000 |


#### Inclusief &quot;Geen waarde&quot;

In Customer Journey Analytics, verzamelen sommige dimensies a *geen waarde* ingang. Met de instelling **[!UICONTROL Include "No value"]** kunt u deze waarden uitsluiten van rapporten. U kunt bijvoorbeeld een classificatie maken, zoals de classificatie Productnaam op basis van de sleutel Product SKU. Als een specifiek productSKU niet opstelling met zijn specifieke classificatie van de Naam van het Product is geweest, wordt zijn waarde van de Naam van het Product geplaatst aan *Geen waarde*.

**[!UICONTROL Include "No value"]** is standaard geselecteerd. Schakel deze optie uit als u items zonder waarde wilt uitsluiten.

#### Filteren op criteria

U kunt dimensie-items filteren op basis van de vraag of aan alle criteria is voldaan of aan alle criteria is voldaan.

Filtercriteria instellen:

1. Selecteer een operator in de vervolgkeuzelijst met operatoren. Standaard is **[!UICONTROL Contains the phrase]** geselecteerd

   ![&#x200B; de exploitantlijst.](./assets/image31.png){zoomable="yes"}

1. Voer een zoekterm in.

1. Selecteer ![&#x200B; toevoegen &#x200B;](/help/assets/icons/Add.svg) **[!UICONTROL Add row]** om de selectie te bevestigen en een ander criterium punt toe te voegen.

1. Selecteer ![&#x200B; CrossSize75 &#x200B;](/help/assets/icons/CrossSize75.svg) om een criterium punt te verwijderen.

U kunt maximaal 10 criteria toevoegen.

### **[!UICONTROL &#x200B; Specific]**

Met de optie **[!UICONTROL Specific]** kunt u een vaste lijst met dimensie-items maken voor elke dimensie. Gebruik het filtertype **[!UICONTROL Specific]** om de exacte afmetingen op te geven die u in het filter wilt opnemen. U kunt items in een lijst of uit een reeks cellen selecteren.

![&#x200B; de Specifieke opties en de geselecteerde punten.](./assets/image32.png){zoomable="yes"}

#### Van lijst

1. Selecteer de optie **[!UICONTROL From list]** om te zoeken naar dimensie-items en deze te selecteren.

   Wanneer u **van lijst** optie selecteert, wordt de **[!UICONTROL Dimension items]** lijst bevolkt met afmetingspunten die door aantal gebeurtenissen worden bevolen.

   ![&#x200B; Van lijstoptie en beschikbare punten.](./assets/image33.png){zoomable="yes"}

1. Ga een onderzoekstermijn in het ![&#x200B; Onderzoek &#x200B;](/help/assets/icons/Search.svg) in **[!UICONTROL _voeg punt_]** toe om de lijst te zoeken.

1. Als u wilt zoeken naar een item dat niet in de laatste 90 dagen aan gegevens is opgenomen, selecteert u **[!UICONTROL Show items for the last 6 months]** om de zoekopdracht uit te breiden. Wanneer gegevens van de afgelopen 6 maanden zijn geladen, werkt Report Builder de koppeling naar **[!UICONTROL Show items for last 18 months]** bij.

1. Om een punt van de **[!UICONTROL Selected items]** lijst te schrappen, selecteer ![&#x200B; CrossSize75 &#x200B;](/help/assets/icons/CrossSize75.svg).

1. Om een punt in de **[!UICONTROL Selected items]** lijst te bewegen, sleep en laat vallen het punt of selecteer ![&#x200B; MoreSmall &#x200B;](/help/assets/icons/MoreSmall.svg) om het contextmenu te tonen en van de verplaatsingsopties te selecteren.

1. Selecteer **[!UICONTROL Apply]**.

Report Builder werkt de lijst bij om het specifieke filter te tonen u toepaste.

#### Uit celbereik

Selecteer **van waaier van cellen** optie om een waaier van cel te kiezen die de lijst van dimensiepunten bevat om aan te passen.

![&#x200B; Van waaier van cellen optie en gebied om één waaier van cellen te selecteren.](./assets/image37.png){zoomable="yes"}

Houd rekening met de volgende beperkingen wanneer u een bereik cellen selecteert:

- Het bereik moet ten minste één cel bevatten.
- Het bereik kan niet meer dan 50.000 cellen bevatten.
- Het bereik moet in één ononderbroken rij of kolom staan.

Uw selectie kan lege cellen of cellen met waarden bevatten die niet met een specifiek afmetingspunt aanpassen.


### Snel een dimensie filteren

Een dimensie filteren waarvoor momenteel geen filter wordt toegepast:

1. Selecteer ![&#x200B; ChevronRight &#x200B;](/help/assets/icons/ChevronRight.svg) voor een afmeting. Bijvoorbeeld **[!UICONTROL Interaction channel]** .

1. Selecteer een dimensie-items die u aan het filter wilt toevoegen. Alternatief, selecteer één of meerdere afmetingspunten en sleep en laat vallen de selectie op ![&#x200B; TableSelectRow &#x200B;](/help/assets/icons/TableSelectRow.svg) **[!UICONTROL Row]** sectie.

   ![&#x200B; het lusje van Dimensies en de lijst van dimensies.](./assets/quickly-filter.png){zoomable="yes"}


<!--

By default, each dimension item in the table returns the top 10 items for that dimension.

To change the dimension items returned for each dimension

1. Click **[!UICONTROL Manage]** and select a data block from the list.

   ![Manage > Edit data block](./assets/manage-edit.png)

1. Click **[!UICONTROL Edit data block]** in the COMMANDS panel.

1. Click **[!UICONTROL Next]** to display the Dimensions tab.

1. Click the **...** icon next to a component name in the table.

    ![The ellipsis icon options.](./assets/image27.png)

1. Select **[!UICONTROL Filter dimension]** in the pop-up menu to display the **[!UICONTROL Filter dimension]** pane.

1. Select **[!UICONTROL Most popular]** or **[!UICONTROL Specific]**.

    ![The specific option selected in the Filter dimension pane.](./assets/image28.png)

1. Select appropriate options based on the filter type chosen.

1. Click **[!UICONTROL Apply]** to add the filter.

    Report Builder displays a notification to confirm the added filter.

To display applied filters, hover over a dimension. Dimensions with applied filters display a filter icon to the right of the Dimension name.

## Filter Type

There are two ways to filter dimension items: Most popular and Specific.

## Most popular

The [!UICONTROL Most popular] option allows you to dynamically filter dimension items based on metric values. [!UICONTROL Most popular] filtering returns the highest ranked dimension items based on metric values. By default, the first 10 dimensions items are listed, sorted by the first metric added to the data block.

 ![The Most popular option.](./assets/image29.png)


### Page and Rows options

Use the **Page** and **Rows** fields to divide data into sequential groups or pages. This allows you to pull ranked row values other than the top-most values into your report. This feature is especially useful for pulling data beyond the 50,000 row limit.

#### Page and Rows defaults

- Page = 1
- Rows = 10

The Page and Rows default settings identify that each page has 10 rows of data. Page 1 returns the top 10 items, page 2 returns the next 10 items, and so on.

The table below lists examples of page and row values and the resulting output.

| Page | Row    | Output               |
|------|--------|----------------------|
| 1    | 10     | Top 10 items         |
| 2    | 10     | Items 11-20          |
| 1    | 100    | Top 100 items        |
| 2    | 100    | Items 101-200        |
| 2    | 50,000 | Items 50,001-100,000 |

#### Minimum and maximum values

- Starting page: Min = 1, Max: 50 million
- Number of rows: Min = 1, Max: 50,000

### Include "No value"

In Adobe Analytics, some dimensions collect a "no value" entry. This filter allows you to exclude these values from reports. For example, you can create a classification such as the Product Name classification based on the Product SKU key. If a specific product SKU has not been set up with its specific Product Name classification, its Product Name value is set to "no value".

Include "**No value**" is selected by default. Deselect this option to exclude entries with no value.

### Filter by Criteria

You can filter dimension items based on whether all criteria are met or if any criteria are met.

To set filtering criteria

1. Select an operator from the drop-down list.

    ![The operator list.](./assets/image31.png)

1. Enter a value into the search field.

1. Click **[!UICONTROL Add row]** to confirm the selection and add another criteria item.

1. Click the delete icon to remove a criteria item.

    You can include up to 10 criteria items.

### Change the filter and sort order

An arrow appears next to the metric used to filter and sort the data block. The direction of the arrow indicates whether the metric is sorted greatest to least or least to greatest.

To change the sort direction, click the arrow next to the metric.

To change the metric used to filter and sort the data block,

1. Hover over the desired metric component in the Table builder to display additional options.

2. Click the arrow on the preferred metric.

   ![The Table builder and metrics.](./assets/image30.png)


## Specific filtering

The Specific option allows you to create a fixed list of dimension items for each dimension. Use the **[!UICONTROL Specific]** filtering type to specify the exact dimension items to include in your filter. You can select items from a list or from a range of cells.

![The Specific options and selected items.](./assets/image32.png)

### From list

1. Select the **[!UICONTROL From list]** option to search for and select dimension items.

    When you select the **[!UICONTROL From list]** option, the list is populated with dimension items with the most events first.

    ![The From list option and available items.](./assets/image33.png)

    The **[!UICONTROL Available items]** list is ordered from dimension items with the most events to those with the least.

1. Enter a search term in the **[!UICONTROL Add item]** field to search the list.

1. To search for an item not included in the last 90 days of data, click **[!UICONTROL Show items for the last 6 months]** to extend the search.

    ![The Show items from the last 6 months list.](./assets/image34.png)

    After data from the past 6 months loads, Report Builder updates the link to **[!UICONTROL Show items for last 18 months]**.

1. Select a dimension item.

    Selected dimension items are automatically added to the **[!UICONTROL Selected items]** list.

    ![](./assets/image35.png)

    To delete an item from the list, click the delete icon to remove the item from the list.

    To move an item in the list, drag and drop the item or click ... to display the move menu.

    ![The dimension items list.](./assets/image36.png)

1. Click **[!UICONTROL Apply]**

    Report Builder updates the list to show the specific filtering you applied.

### From range of cells

Select the **[!UICONTROL From range of cells]** option to choose a range of cell that contain the list of dimensions items to match.

 ![The From range of cells option and field to select one range of cells.](./assets/image37.png)

When you select a range of cells, consider the following restrictions:

- The range must have at least one cell.
- The range can't have more than 50,000 cells.
- The range must be in a single uninterrupted row, or column.

Your selection can contain empty cells or cells with values that don't match with a specific dimension item.

### From the Dimensions tab in the Table builder

From the **[!UICONTROL Dimensions]** tab, click the chevron icon next to a dimension name to view the list of dimension items.

 ![The Dimensions tab and the list of dimensions.](./assets/dimensions_chevron.png)

You can drag and drop items onto the **[!UICONTROL Table]** or double-click an item name to add it to the **[!UICONTROL Table]** builder.

-->