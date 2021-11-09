---
description: Gebruik de kaartvisualisatie in een project van de Werkruimte.
title: Kaart
uuid: 6038f336-62a3-4efa-8316-4d7792468db3
feature: Visualizations
role: User, Admin
exl-id: a60544b4-27b6-413a-96ce-ab9487594422
source-git-commit: f7853f81c6f7d036b35e1d88ac8b5eb2bf84646d
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 3%

---

# Kaart

## Overzicht {#section_19F740FAF08D47B1AF1EF239A74FC75C}

Visualisatie op de kaart in Analysis Workspace

* Hiermee kunt u een visuele kaart van elke metrische waarde (inclusief berekende metriek) maken.
* Is nuttig om metrische gegevens over verschillende geografische gebieden te identificeren en te vergelijken.
* Biedt ondersteuning voor twee gegevensbronnen: breedtegraad/lengtegraad van mobiel gebruik of geografische afmeting voor webgebruik.
* Ondersteunt PDF-export.
* Gebruikt WebGL voor beeldvertoning. Als uw grafische stuurprogramma&#39;s geen ondersteuning bieden voor WebGL-rendering, moet u de stuurprogramma&#39;s mogelijk bijwerken.

Hier volgt een video-overzicht:

>[!VIDEO](https://video.tv.adobe.com/v/23559/?quality=12)

## Een kaart visualiseren {#section_61BBFA3A7BFD48DA8D305A69D9416299}

1. Sleep vanuit de lijst met visualisaties **[!UICONTROL Map]** in een deelvenster Vrije vorm:

   ![](assets/map-viz1.png)

1. Sleep in metrische vorm vanuit de lijst met metriek (inclusief berekende metriek).
1. Geef de gegevensbron op waaruit u wilt tekenen. (Dit dialoogvenster wordt alleen weergegeven als u locatie-tracking hebt ingeschakeld voor gegevens van mobiele apps.)

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL Mobile Lat/Long] | Deze optie vertegenwoordigt gegevens van mobiele apps. U ziet deze optie alleen als u deze voor uw rapportsuite hebt ingeschakeld in [!UICONTROL Analytics] > [!UICONTROL Admin] > [!UICONTROL Report Suites] > (selecteer rapportsuite) > [!UICONTROL Edit Settings] >  [!UICONTROL Mobile Management] > [!UICONTROL Enable Location Tracking]. Dit is de standaardinstelling (als locatie bijhouden is ingeschakeld). |
| [!UICONTROL Geographic Dimension] | Deze optie vertegenwoordigt geo segmentatiegegevens over bezoekersplaats die op het IP van de bezoeker adres wordt gebaseerd. Deze gegevens worden omgezet in [!UICONTROL Country], [!UICONTROL Region], en [!UICONTROL City]. Merk op dat het niet naar het niveau van de Code DMA of van het Postcode gaat. Bijna alle rapportsuites hebben deze toegelaten dimensie. Als u dat niet doet, neemt u contact op met de klantenservice van Adobe om geografische rapporten ingeschakeld te laten. |

1. Klik op **[!UICONTROL Build]**.

   De eerste weergave die je zult zien is een World View met een bubble map, vergelijkbaar met deze.

   ![](assets/bubble-world-view.png)

1. U kunt nu

   * **Zoomen** in deze kaart om bepaalde gebieden te vergroten door te dubbelklikken op de kaart of door uw schuifwiel te gebruiken. De kaart zoomt naar waar u de cursor hebt geplaatst. Via zoominteractie wordt de vereiste afmeting (land > land > plaats) automatisch bijgewerkt op basis van het zoomniveau.
   * **Vergelijken** twee of meer kaartvisualisaties in het zelfde project door hen naast elkaar te plaatsen.
   * **Vergelijkingen tussen perioden waarin een periode is overgelopen (zoals jaar-overjaar) weergeven**:

      * Negatieve getallen tonen: Als u bijvoorbeeld een metrische waarde uitzet die elk jaar wordt overschreden, kan de kaart -33% weergeven ten opzichte van New York.
      * Met metrics van het type percentage, wordt het gemiddelde van de geclusterde percentages getoond.
      * Een groen/rood kleurenschema: Positief/negatief
   * **Roteren** de kaart in 2D of 3D door de [!UICONTROL Ctrl] en de kaart verplaatsen.

   * **Schakelen** naar een andere weergave, zoals de warmtekaart, met behulp van de [instellingen](/help/analyze/analysis-workspace/visualizations/map-visualization.md#section_5F89C620A6AA42BC8E0955478B3A427E) hieronder beschreven. De bellenweergave is de standaardinstelling.


1. **Opslaan** het project om alle kaartmontages (coördinaten, gezoem, omwenteling) te bewaren.
1. De vrije-vormlijst, onder visualisatie, kan worden bevolkt door in plaatsdimensies en metriek van de linkerspoorstaaf te slepen:

   ![](assets/location-dimensions.png)

## Visualisatie-instellingen toewijzen {#section_5F89C620A6AA42BC8E0955478B3A427E}

Er zijn twee sets instellingen voor Kaart:

De **moersleutelpictogram** rechtsboven wordt het eerste dialoogvenster weergegeven waarin u de metrische waarde en de gegevensbron kunt wijzigen:

![](assets/map-wrench.png)

Klik op de knop **tandwielpictogram** onthult deze visualisatie-instellingen:

| Instelling | Beschrijving |
|--- |--- |
| Luchtbellen | Hiermee worden gebeurtenissen geplakt met behulp van bellen. Een bubbelgrafiek is een multi-variabelegrafiek die een kruis tussen een spreidplot en een proportioneel gebiedsgrafiek is. Dit is de standaardweergave. |
| Heatmap | Hiermee worden gebeurtenissen geplakt met een heatmap. Een heatmap is een grafische voorstelling van gegevens waarbij de afzonderlijke waarden in een matrix als kleuren worden weergegeven. |
| Stijlen: Kleurthema | Hiermee geeft u het kleurenschema voor de warmtekaart en luchtbellen weer. U kunt kiezen uit Koraal, Rode tinten, Groene tinten of Vervagen. Standaard is Coral. |
| Stijlen: Type kaart | U kunt kiezen uit Standaard, Streets, Helder, Licht, Donker en Satelliet. |
| Clusterstraal | Hiermee groepeert u gegevenspunten die binnen het opgegeven aantal pixels liggen. De standaardwaarde is 50. |
| Aangepaste maximale waarde | Hiermee kunt u de drempelwaarde voor de maximale waarde voor de kaart wijzigen. Als u deze waarde aanpast, wordt de schaal voor de waarden voor luchtbellen/heatmap (kleur en grootte) aangepast ten opzichte van de aangepaste maximale waarde die is ingesteld. |

## Een geparseerde heatmap maken

Hier volgt een video over het onderwerp:

>[!VIDEO](https://video.tv.adobe.com/v/26991/?quality=12)
