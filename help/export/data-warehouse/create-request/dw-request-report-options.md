---
description: Stappen die beschrijven hoe te om een verzoek van de Data Warehouse tot stand te brengen.
title: Configureer rapportopties voor een Data Warehouse-verzoek
feature: Data Warehouse
source-git-commit: 0abf0c76f38b481c0b72d113fe49e0da03ddd8cd
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# Configureer rapportopties voor een Data Warehouse-verzoek

>[!AVAILABILITY]
>
>Sommige functies voor Data Warehouse die in dit artikel worden beschreven (en andere artikelen voor Data Warehouse in deze sectie) zijn alleen beschikbaar in de beperkte testfase van de release en zijn mogelijk nog niet beschikbaar in uw omgeving.
>
>Voor informatie over welke functies nog niet voor alle klanten beschikbaar zijn, en voor informatie over de releasetijdlijn van deze functies, raadpleegt u de [releaseopmerkingen](/help/release-notes/latest.md).
>
>Deze notitie wordt verwijderd wanneer de functionaliteit algemeen beschikbaar is. Voor informatie over het evaluatieproces Analytics raadpleegt u [Adobe Analytics-functiereleases](/help/release-notes/releases.md).

Er zijn diverse configuratieopties beschikbaar wanneer het creëren van een verzoek van de Data Warehouse. De volgende informatie beschrijft hoe te om rapportopties voor het verzoek te vormen.

Voor informatie over hoe te beginnen creërend een verzoek, evenals verbindingen aan andere belangrijke configuratieopties, zie [Een Data Warehouse-aanvraag maken](/help/export/data-warehouse/create-request/t-dw-create-request.md).

Om rapportopties voor een verzoek van de Data Warehouse te vormen:

1. Begin met het maken van een aanvraag in Adobe Analytics door **[!UICONTROL Tools]** > **[!UICONTROL Data Warehouse]** > [!UICONTROL **Toevoegen**].

   Zie voor meer informatie [Een Data Warehouse-aanvraag maken](/help/export/data-warehouse/create-request/t-dw-create-request.md).

1. Selecteer op de aanvraagpagina Nieuwe Data Warehouse de optie [!UICONTROL **Rapportopties**] tab.

   ![Tabblad Doel rapporteren](assets/dw-report-options.png) <!-- update screenshot to include Sort by metrics -->

1. Vul de volgende velden in:

   | Optie | -functie |
   |---------|----------|
   | Bestandsnaam | Identificeert het rapport. |
   | Datumbereik van rapport toevoegen aan bestandsnaam | Hiermee voegt u het datumbereik toe aan de naam van het rapportbestand. <p>Als u bijvoorbeeld gegevens aanvraagt van 1 mei 2024 tot en met 7 mei 2024, bevat de bestandsnaam het datumbereik 20240501 - 20240507.</p> |
   | CSV | Levert rapporten in een CSV-bestandsindeling voor het weergeven van gegevens in een spreadsheet. |
   | Tableau (TDE) | Levert rapporten in een het dossierformaat van de Uitvoer van Gegevens van Tableau (TDE), dat kan worden gebruikt om gegevens en laag in extra gegevens binnen Tableau te visualiseren. |
   | Rapport verzenden als gecomprimeerd bestand (ZIP) | Levert rapporten in een gecomprimeerde (ZIP) dossierformaat. We raden u aan deze optie in te schakelen als u e-mail gebruikt als de [rapportbestemming](/help/export/data-warehouse/create-request/dw-request-report-destinations.md). |
   | Aantal rijen in de tabel | Het aantal rijen dat in het rapport kan worden omvat. Gebruik 0 om alle rijen op te nemen (dit is de standaardselectie). <!-- when would you want to limit the rows? To improve performance? Do we have recommendations? --> |
   | Opmerkingen | Voeg eventuele opmerkingen toe die u in het rapport wilt opnemen. De commentaren verschijnen aan het begin van het rapport. |
   | Sorteren op metriek | Verstrekt gerangschikte verdelingsrapporten in Data Warehouse, die door dalende metrische waarde wordt gesorteerd. Sorteren op metrisch maakt de rapporten van de Data Warehouse voor u gemakkelijker te interpreteren, en maakt deze rapporten gemakkelijker om met andere Analytics te vergelijken de mening van de het verdelingsrapporten van de Analyse.<p>Zie voor meer informatie [Sorteren op metrisch](/help/export/data-warehouse/sorting-by-metric.md).</p> |
   | Manifestbestand verzenden | Omvat meta-gegevens over de dossiers inbegrepen in het rapport.<!-- What kind of metadata is included in the manifest file? --> |
   | Digitaal handtekeningbestand verzenden | Staat rapportontvangers toe om te verifiëren dat het dossier uit Adobe kwam en dat het niet is veranderd. |
   | Een leeg bestand verzenden als het rapport geen gegevens bevat | Verzendt een rapport zelfs wanneer het rapport geen gegevens bevat. |

   {style="table-layout:auto"}

1. Ga door met het configureren van uw verzoek voor Data Warehouse op de [!UICONTROL **Planningsopties**] tab. Zie voor meer informatie [Configureer de planningsopties voor een Data Warehouse-verzoek](/help/export/data-warehouse/create-request/dw-request-scheduling.md).