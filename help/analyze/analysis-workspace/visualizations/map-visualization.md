---
description: Gebruik de kaartvisualisatie om gegevens op een geografische kaartvisualisatie te plotten.
title: Kaart
uuid: 6038f336-62a3-4efa-8316-4d7792468db3
feature: Visualizations
role: User, Admin
exl-id: a60544b4-27b6-413a-96ce-ab9487594422
source-git-commit: 8b1e25b9633b6db3e49da079f7014e6b7b595474
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# Kaart {#map}

<!-- markdownlint-disable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_map_button"
>title="Kaart"
>abstract="Deze visualisatie vertegenwoordigt metriek door hen op een kaart te bedekken. Deze visualisatie is handig voor het identificeren van gegevens in verschillende geografische gebieden."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_map_bubbles"
>title="Luchtbellen"
>abstract="Plot gebeurtenissen using bubbles."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_map_heatmap"
>title="Heatmap"
>abstract="Plotten met behulp van een warmtekaart."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_dit artikel documenteert de visualisatie van de Kaart in_ ![&#x200B; AdobeAnalytics &#x200B;](/help/assets/icons/AdobeAnalytics.svg) _&#x200B;**Adobe Analytics**._<br/>_zie [&#x200B; Kaart &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-workspace/visualizations/map) voor_ ![&#x200B; CustomerJourneyAnalytics &#x200B;](/help/assets/icons/CustomerJourneyAnalytics.svg) _&#x200B;**Customer Journey Analytics** versie van dit artikel._

>[!ENDSHADEBOX]



De ![&#x200B; Globe &#x200B;](/help/assets/icons/Globe.svg) **[!UICONTROL Map]** visualisatie in Analysis Workspace

* kunt u een visuele kaart van om het even welke metrisch (met inbegrip van berekende metriek) bouwen;
* nuttig is voor het identificeren en vergelijken van metrische gegevens over verschillende geografische regio&#39;s;
* twee gegevensbronnen kunnen ondersteunen: lengte-/breedtegraad van mobiel gebruik of geografische afmeting voor webgebruik;
* ondersteunt PDF-export, en
* Gebruikt WebGL voor beeldvertoning. Als uw grafische stuurprogramma&#39;s geen ondersteuning bieden voor WebGL-rendering, moet u de stuurprogramma&#39;s mogelijk bijwerken.


>[!BEGINSHADEBOX]

Zie ![&#x200B; VideoCheckedOut &#x200B;](/help/assets/icons/VideoCheckedOut.svg) [&#x200B; visualisatie van de Kaart in Analysis Workspace &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics-learn/tutorials/analysis-workspace/visualizations/map-visualization){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


## Gebruiken

1. Voeg a ![&#x200B; Kaart &#x200B;](/help/assets/icons/Globe.svg) [!UICONTROL Map] visualisatie toe. Zie [&#x200B; een visualisatie aan een paneel &#x200B;](freeform-analysis-visualizations.md#add-visualizations-to-a-panel) toevoegen. U kunt een Kaartweergave alleen boven op een tabel voor vrije vorm slepen.

   ![&#x200B; configuratie van de Kaart &#x200B;](assets/map-configuration.png){width="50%"}

1. Selecteer een metrische waarde in de vervolgkeuzelijst. Of sleep in metrische vorm vanuit de lijst met metriek (inclusief berekende metriek).
1. Geef de gegevensbron op waaruit u wilt tekenen. Dit dialoogvenster wordt alleen weergegeven als u locatie-tracking hebt ingeschakeld voor gegevens van mobiele apps.

   | Bron | Beschrijving |
   | --- | --- |
   | **[!UICONTROL Mobile Lat/Long]** | Deze optie vertegenwoordigt gegevens van mobiele apps. U ziet deze optie alleen als u deze voor uw rapportsuite hebt ingeschakeld in [!UICONTROL Analytics] > [!UICONTROL Admin] > [!UICONTROL Report Suites] > (selecteer rapportsuite) > [!UICONTROL Edit Settings] > [!UICONTROL Mobile Management] > [!UICONTROL Enable Location Tracking] . Dit zijn de standaardinstellingen (als locatietracering is ingeschakeld). |
   | **[!UICONTROL Geographic Dimension]** | Deze optie vertegenwoordigt geo segmentatiegegevens over bezoekersplaats die op het IP van de bezoeker adres wordt gebaseerd. Deze gegevens worden omgezet in [!UICONTROL Country] , [!UICONTROL Region] en [!UICONTROL City] . Merk op dat het niet naar het niveau van de Code DMA of van het Postcode gaat. Bijna alle rapportsuites hebben deze toegelaten dimensie. Als dat niet het geval is, neemt u contact op met de klantenservice van Adobe om geografische rapporten in te schakelen. |

1. Selecteer **[!UICONTROL Build]**.

   Er wordt een &#39;world map visualization&#39; met bubbels gegenereerd.

   ![](assets/bubble-world-view.png)

1. U kunt nu:

   * **Gezoem** in deze kaart om bepaalde gebieden te vergroten door de kaart tweemaal te klikken of door uw rolwiel te gebruiken. De kaart zoomt naar waar u de cursor hebt geplaatst. Via zoominteractie wordt de vereiste afmeting (land > land > plaats) automatisch bijgewerkt op basis van het zoomniveau.
   * **vergelijk** twee of meer kaartvisualisaties in het zelfde project door hen naast elkaar te plaatsen.
   * **toon periode-over-periode (zoals, jaar-over-jaar) vergelijkingen**:

      * Negatieve getallen tonen: als u bijvoorbeeld een metrisch getal uitzet dat jaar in jaar doorloopt, kan de kaart -33% weergeven ten opzichte van New York.
      * Met metriek die van type *percenten* zijn, groeperen zich gemiddelden samen de percentages.
      * Een groen/rood kleurenschema: positief/negatief

   * **roteer** de kaart in 2D of 3D door de [!UICONTROL Ctrl] sleutel te houden en de kaart te bewegen.

   * **knevel** aan een verschillende mening, zoals de warmtekaart, gebruikend de [&#x200B; hieronder beschreven montages &#x200B;](/help/analyze/analysis-workspace/visualizations/map-visualization.md#section_5F89C620A6AA42BC8E0955478B3A427E). De bellenweergave is de standaardinstelling.

1. **sparen** het project om alle kaartmontages (coördinaten, gezoem, omwenteling) te bewaren.
1. De vrije-vormlijst, onder visualisatie, kan worden bevolkt door in plaatsdimensies en metriek van de linkerspoorstaaf te slepen.



## Configureren

Om de visualisatie van de Kaart aan te passen, uitgezocht ![&#x200B; geef &#x200B;](/help/assets/icons/Edit.svg) uit.


## Instellingen

Om montages voor visualisatie te bepalen, uitgezochte ![&#x200B; Plaatsend &#x200B;](/help/assets/icons/Setting.svg).

| Instelling | Beschrijving |
|--- |--- |
| **[!UICONTROL Map type]** | |
| **[!UICONTROL Bubbles] | Hiermee worden gebeurtenissen geplakt met behulp van bellen. Een bubbelgrafiek is een multi-variabelegrafiek die een kruis tussen een spreidplot en een proportioneel gebiedsgrafiek is. Dit is de standaardweergave. |
| [!UICONTROL Heatmap] | Hiermee worden gebeurtenissen geplakt met een heatmap. Een heatmap is een grafische voorstelling van gegevens waarbij de afzonderlijke waarden in een matrix als kleuren worden weergegeven. |
| **[!UICONTROL Styles]** | |
| [!UICONTROL Color theme] | Hiermee geeft u het kleurenschema voor de warmtekaart en luchtbellen weer. U kunt kiezen uit Koraal, Rode tinten, Groene tinten of Vervagen. De standaardinstelling is Coral. |
| [!UICONTROL Map style] | U kunt kiezen uit Standaard, Streets, Helder, Licht, Donker en Satelliet. |
| **[!UICONTROL Cluster Radius]** | Hiermee groepeert u gegevenspunten die binnen het opgegeven aantal pixels liggen. De standaardwaarde is 50. |
| **[!UICONTROL Custom Max Value]** | Hiermee kunt u de drempelwaarde voor de maximale waarde voor de kaart wijzigen. Als u deze waarde aanpast, wordt de schaal voor de waarden voor luchtbellen/heatmap (kleur en grootte) aangepast ten opzichte van de aangepaste maximale waarde die is ingesteld. |

<!--
## Build a time-parting heatmap

Here is a video on the topic:

>[!VIDEO](https://experienceleague.adobe.com/nl/docs/analytics-learn/tutorials/analysis-workspace/visualizations/build-a-time-parting-heatmap)

-->

