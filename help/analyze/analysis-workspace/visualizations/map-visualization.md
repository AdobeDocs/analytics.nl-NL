---
description: Gebruik de kaartvisualisatie in een Workspace-project.
title: Kaart
uuid: 6038f336-62a3-4efa-8316-4d7792468db3
feature: Visualizations
role: User, Admin
exl-id: a60544b4-27b6-413a-96ce-ab9487594422
source-git-commit: de489dda1c2627ccb263ac496f8abb2794854856
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 2%

---

# Kaart {#map}

<!-- markdownlint-disable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_map_button"
>title="Kaart"
>abstract="Deze visualisatie vertegenwoordigt metriek door hen op een kaart te bedekken. Dit is handig voor het identificeren van gegevens in verschillende geografische gebieden."

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

*dit artikel documenteert de visualisatie van de Kaart in **Adobe Analytics**.<br/> Er is momenteel geen visualisatie van de Kaart beschikbaar in **Customer Journey Analytics**.*

>[!ENDSHADEBOX]

## Overzicht {#section_19F740FAF08D47B1AF1EF239A74FC75C}

Visualisatie op de kaart in Analysis Workspace

* Hiermee kunt u een visuele kaart van elke metrische waarde (inclusief berekende metriek) maken.
* Is nuttig om metrische gegevens over verschillende geografische gebieden te identificeren en te vergelijken.
* Biedt ondersteuning voor twee gegevensbronnen: breedte/lengte van mobiel gebruik of geografische afmeting voor webgebruik.
* Ondersteunt PDF-export.
* Gebruikt WebGL voor beeldvertoning. Als uw grafische stuurprogramma&#39;s geen ondersteuning bieden voor WebGL-rendering, moet u de stuurprogramma&#39;s mogelijk bijwerken.

Hier volgt een video-overzicht:

>[!VIDEO](https://video.tv.adobe.com/v/23559/?quality=12)

## Een kaart visualiseren {#section_61BBFA3A7BFD48DA8D305A69D9416299}

1. Sleep **[!UICONTROL Map]** vanuit de lijst met visualisaties naar een deelvenster Vrije vorm:

   ![](assets/map-viz1.png)

1. Sleep in metrische vorm vanuit de lijst met metriek (inclusief berekende metriek).
1. Geef de gegevensbron op waaruit u wilt tekenen. (Dit dialoogvenster wordt alleen weergegeven als u locatie-tracking hebt ingeschakeld voor gegevens van mobiele apps.)

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL Mobile Lat/Long] | Deze optie vertegenwoordigt gegevens van mobiele apps. U ziet deze optie alleen als u deze voor uw rapportsuite hebt ingeschakeld in [!UICONTROL Analytics] > [!UICONTROL Admin] > [!UICONTROL Report Suites] > (selecteer rapportsuite) > [!UICONTROL Edit Settings] > [!UICONTROL Mobile Management] > [!UICONTROL Enable Location Tracking] . Dit is de standaardinstelling (als locatie bijhouden is ingeschakeld). |
| [!UICONTROL Geographic Dimension] | Deze optie vertegenwoordigt geo segmentatiegegevens over bezoekersplaats die op het IP van de bezoeker adres wordt gebaseerd. Deze gegevens worden omgezet in [!UICONTROL Country] , [!UICONTROL Region] en [!UICONTROL City] . Merk op dat het niet naar het niveau van de Code DMA of van het Postcode gaat. Bijna alle rapportsuites hebben deze toegelaten dimensie. Als u dat niet doet, neemt u contact op met de klantenservice van de Adobe om geografische rapporten ingeschakeld te laten. |

1. Klik op **[!UICONTROL Build]**.

   De eerste weergave die je zult zien is een World View met een bubble map, vergelijkbaar met deze.

   ![](assets/bubble-world-view.png)

1. U kunt nu

   * **Gezoem** in deze kaart om bepaalde gebieden te vergroten door de kaart tweemaal te klikken of door uw rolwiel te gebruiken. De kaart zoomt naar waar u de cursor hebt geplaatst. Via zoominteractie wordt de vereiste afmeting (land > land > plaats) automatisch bijgewerkt op basis van het zoomniveau.
   * **vergelijk** twee of meer kaartvisualisaties in het zelfde project door hen naast elkaar te plaatsen.
   * **toon periode-over-periode (zoals, jaar-over-jaar) vergelijkingen**:

      * Negatieve getallen tonen: als u bijvoorbeeld een metrisch getal uitzet dat jaar in jaar doorloopt, kan de kaart -33% weergeven ten opzichte van New York.
      * Met metrics van het type percentage, wordt het gemiddelde van de geclusterde percentages getoond.
      * Een groen/rood kleurenschema: positief/negatief

   * **roteer** de kaart in 2D of 3D door de [!UICONTROL Ctrl] sleutel te houden en de kaart te bewegen.

   * **knevel** aan een verschillende mening, zoals de warmtekaart, gebruikend de [ hieronder beschreven montages ](/help/analyze/analysis-workspace/visualizations/map-visualization.md#section_5F89C620A6AA42BC8E0955478B3A427E). De bellenweergave is de standaardinstelling.

1. **sparen** het project om alle kaartmontages (coördinaten, gezoem, omwenteling) te bewaren.
1. De vrije-vormlijst, onder visualisatie, kan worden bevolkt door in plaatsdimensies en metriek van de linkerspoorstaaf te slepen:

   ![](assets/location-dimensions.png)

## Visualisatie-instellingen toewijzen {#section_5F89C620A6AA42BC8E0955478B3A427E}

Er zijn twee sets instellingen voor Kaart:

Het **moersleutelpictogram** bij het hoogste recht brengt de aanvankelijke dialoog terug waar u metrisch en gegevensbron kunt veranderen:

![](assets/map-wrench.png)

Het klikken van het **tandwielpictogram** openbaart deze visualiseringsmontages:

| Instelling | Beschrijving |
|--- |--- |
| Luchtbellen | Hiermee worden gebeurtenissen geplakt met behulp van bellen. Een bubbelgrafiek is een multi-variabelegrafiek die een kruis tussen een spreidplot en een proportioneel gebiedsgrafiek is. Dit is de standaardweergave. |
| Heatmap | Hiermee worden gebeurtenissen geplakt met een heatmap. Een heatmap is een grafische voorstelling van gegevens waarbij de afzonderlijke waarden in een matrix als kleuren worden weergegeven. |
| Stijlen: kleurthema | Hiermee geeft u het kleurenschema voor de warmtekaart en luchtbellen weer. U kunt kiezen uit Koraal, Rode tinten, Groene tinten of Vervagen. Standaard is Coral. |
| Stijlen: Stijl toewijzen | U kunt kiezen uit Standaard, Streets, Helder, Licht, Donker en Satelliet. |
| Clusterstraal | Hiermee groepeert u gegevenspunten die binnen het opgegeven aantal pixels liggen. De standaardwaarde is 50. |
| Aangepaste maximale waarde | Hiermee kunt u de drempelwaarde voor de maximale waarde voor de kaart wijzigen. Als u deze waarde aanpast, wordt de schaal voor de waarden voor luchtbellen/heatmap (kleur en grootte) aangepast ten opzichte van de aangepaste maximale waarde die is ingesteld. |

## Een geparseerde heatmap maken

Hier volgt een video over het onderwerp:

>[!VIDEO](https://video.tv.adobe.com/v/26991/?quality=12)
