---
description: Voordat u virtuele rapportsuites gaat maken, moet u rekening houden met een aantal zaken.
keywords: Virtuele rapportsuite
title: Virtuele rapportsuites maken
feature: VRS
exl-id: 5ff6ff1a-5b99-41cc-a3a7-928197ec9ef9
source-git-commit: fcc165536d77284e002cb2ba6b7856be1fdb3e14
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 2%

---

# Virtuele rapportsuites maken

Voordat u virtuele rapportsuites gaat maken, moet u rekening houden met een aantal zaken.

* Gebruikers die geen beheerder zijn, kunnen het beheerprogramma voor virtuele rapportpakken niet zien.
* Virtuele rapportsuites kunnen niet worden gedeeld. &quot;Delen&quot; wordt uitgevoerd via groepen/machtigingen.
* In de Virtuele manager van de rapportreeksen, kunt u slechts uw eigen virtuele rapportreeksen zien. U moet op Alles tonen klikken om iedereen te zien.

1. Ga naar **[!UICONTROL Components]** > **[!UICONTROL Virtual report suites]**.
1. Klik op **[!UICONTROL Add +]**.

   ![](assets/new_vrs.png)

## Instellingen definiëren

Definieer deze instellingen op het tabblad [!UICONTROL Settings] en klik op **[!UICONTROL Continue]** .

| Element | Beschrijving |
| --- |--- |
| Naam | De naam van de virtuele rapportreeks wordt niet geërft van de ouderrapportreeks en zou verschillend moeten zijn. |
| Beschrijving | Voeg een goede beschrijving toe ten behoeve van uw zakelijke gebruikers. |
| Tags | U kunt codes toevoegen om uw rapportsuites te organiseren. |
| Bron | De rapportsuite waarvan deze virtuele rapportsuite de volgende instellingen overneemt. De meeste serviceniveaus en -functies (zoals eVar-instellingen, Verwerkingsregels, Classificaties, enzovoort) worden overgeërfd. Als u wijzigingen wilt aanbrengen in deze overgeërfde instellingen in een virtuele-rapportsuite, moet u de bovenliggende rapportsuite bewerken ( Admin > Report Suites). |
| Tijdzone | Een tijdzone kiezen is optioneel. Als u een tijdzone kiest, wordt deze samen met de Virtual Report-suite opgeslagen. Als u niet kiest, wordt de tijdzone van de ouderrapportreeks gebruikt.  Als u een virtuele rapportsuite bewerkt, wordt de tijdzone die is opgeslagen met de Virtual Report-suite weergegeven in de vervolgkeuzelijst. Als de Virtuele rapportreeks werd gecreeerd alvorens de steun van de tijdzone werd toegevoegd, wordt de de tijdzone van de reeks van het ouderrapport getoond in de drop-down selecteur. |
| Segmenten | U kunt slechts één segment toevoegen of segmenten stapelen.   Nota: Wanneer het stapelen van twee segmenten, worden zij aangesloten bij door een EN verklaring. Dit kan niet in een OF verklaring worden veranderd. Wanneer u probeert om een segment te schrappen of te wijzigen dat momenteel in een virtuele rapportreeks wordt gebruikt, toont een waarschuwing. |

## Definitie van bezoek definiëren

Definieer deze instellingen op het tabblad [!UICONTROL Visit Definition] en klik op **[!UICONTROL Continue]** .

![](assets/visit-definition.png)


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ een bezoekdefinitie ](https://video.tv.adobe.com/v/23545?quality=12&learn=on){target="_blank"} voor een demo video aanpassen.

>[!ENDSHADEBOX]

| Element | Beschrijving |
| --- |--- |
| **vorm de definitie van het bezoek** |  |
| Tijdverwerking rapport inschakelen | De verwerking van de rapporttijd van het gebruik om de standaardonderbrekingslengte van het bezoek te veranderen. Deze instellingen zijn niet-destructief en zijn alleen van toepassing in Analysis Workspace. [Meer informatie](/help/components/vrs/vrs-report-time-processing.md) |
| Time-out bij bezoek | Hiermee bepaalt u de mate van inactiviteit die een unieke bezoeker moet hebben voordat een nieuw bezoek automatisch wordt gestart. Dit zal metrische bezoeken, de container van het bezoekensegment, en eVars beïnvloeden die op bezoek verlopen. |
| Nieuw bezoek starten met gebeurtenis | Hiermee wordt een nieuwe sessie gestart wanneer een van de opgegeven gebeurtenissen wordt gestart, ongeacht of er een time-out voor een sessie is opgetreden. |
| **Mobiele montages van het toepassingsbezoek** | Wijzig de manier waarop bezoeken worden gedefinieerd voor hits in mobiele apps die worden verzameld door Adobe Mobile-SDK&#39;s. Deze instellingen zijn niet-destructief en zijn alleen van toepassing in Analysis Workspace. |
| Voorkomen dat achtergrondhits een nieuw bezoek beginnen | Hiermee voorkomt u dat achtergrondopdrachten beginnen en dat bezoekers en unieke bezoekersstatistieken opblazen. |
| Een nieuw bezoek starten bij elke keer dat de app wordt gestart | Hiermee wordt een nieuwe sessie gestart wanneer een app wordt gestart. [Meer informatie](/help/components/vrs/vrs-mobile-visit-processing.md) |

## Componenten opnemen en hernoemen

![](assets/components.png)

1. Schakel op het tabblad [!UICONTROL Components] het selectievakje in om de curatie toe te passen voor het opnemen, uitsluiten en hernoemen van componenten voor deze virtuele rapportsuite in Analysis Workspace.
Voor meer informatie over de virtuele cursus van de rapportreeks, zie [ Virtuele de componentencuratie van de rapportreeks ](/help/components/vrs/vrs-components.md).

1. Sleep componenten (afmetingen, metriek, segmenten, of datumwaaiers) die u in de Virtuele rapportreeks in de [!UICONTROL Included Components] sectie wilt omvatten.

1. Klik op **[!UICONTROL Save]** als u klaar bent.

## Gegevens voorvertonen

Aan de rechterkant van elk tabblad kunt u een voorvertoning weergeven van het totale aantal treffers, het totale aantal bezoeken en het totale aantal bezoekers in deze virtuele rapportsuite, in vergelijking met de oorspronkelijke rapportsuite.

## Productcompatibiliteit weergeven

Sommige functies van virtuele rapportsuites worden niet door alle Adobe Analytics-producten ondersteund. Met de lijst met productcompatibiliteit kunt u zien welke producten in Adobe Analytics worden ondersteund op basis van de instellingen van uw huidige virtuele rapportsuite.
