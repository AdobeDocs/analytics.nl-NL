---
description: Stappen die beschrijven hoe te om een verzoek van de Data Warehouse tot stand te brengen.
title: Vorm een rapportbestemming voor een verzoek van de Data Warehouse
feature: Data Warehouse
source-git-commit: 0abf0c76f38b481c0b72d113fe49e0da03ddd8cd
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 1%

---

# Configureer de planningsopties voor een Data Warehouse-verzoek

>[!AVAILABILITY]
>
>Sommige functies voor Data Warehouse die in dit artikel worden beschreven (en andere artikelen voor Data Warehouse in deze sectie) zijn alleen beschikbaar in de beperkte testfase van de release en zijn mogelijk nog niet beschikbaar in uw omgeving.
>
>Voor informatie over welke functies nog niet voor alle klanten beschikbaar zijn, en voor informatie over de releasetijdlijn van deze functies, raadpleegt u de [releaseopmerkingen](/help/release-notes/latest.md).
>
>Deze notitie wordt verwijderd wanneer de functionaliteit algemeen beschikbaar is. Voor informatie over het evaluatieproces Analytics raadpleegt u [Adobe Analytics-functiereleases](/help/release-notes/releases.md).

Er zijn diverse configuratieopties beschikbaar wanneer het creëren van een verzoek van de Data Warehouse. De volgende informatie beschrijft hoe te om het plannen opties voor het verzoek te vormen.

Voor informatie over hoe te beginnen creërend een verzoek, evenals verbindingen aan andere belangrijke configuratieopties, zie [Een Data Warehouse-aanvraag maken](/help/export/data-warehouse/create-request/t-dw-create-request.md).

Om het plannen opties voor een verzoek van de Data Warehouse te vormen:

1. Begin met het maken van een aanvraag in Adobe Analytics door **[!UICONTROL Tools]** > **[!UICONTROL Data Warehouse]** > [!UICONTROL **Toevoegen**].

   Zie voor meer informatie [Een Data Warehouse-aanvraag maken](/help/export/data-warehouse/create-request/t-dw-create-request.md).

1. Selecteer op de aanvraagpagina Nieuwe Data Warehouse de optie [!UICONTROL **Planningsopties**] tab.

   ![Tabblad Doel rapporteren](assets/dw-scheduling-options.png) <!-- update screenshot -->

1. Vul de volgende velden in:

   | Optie | -functie |
   |---------|----------|
   | Rapport nu verzenden | Verzendt het rapport als een eenmalig rapport. Als deze optie is geselecteerd, worden alle planningsopties verborgen. |
   | Plan voor later | Verstrekt opties voor het plannen van rapportlevering. Alle opties worden hieronder beschreven. |
   | Rapportfrequentie | De frequentie waarmee rapporten worden geleverd. <p>De volgende opties zijn beschikbaar:</p><ul><li>Uurlijks</li><p>[!UICONTROL **Uur**] is alleen beschikbaar als de [!UICONTROL **Datumbereiken**] de optie [!UICONTROL **Algemene instellingen**] tab is ingesteld op [!UICONTROL **Laatste uur**].</p><li>Dagelijks</li><li>Wekelijks</li><li>Maandelijks</li><li>Jaarlijks</li></ul>  <!-- Is this valid? Was in the old docs: "To schedule Data Warehouse requests for Daily, Weekly, Monthly, or Yearly, make sure *Preset* is correctly selected" --> |
   | Maandelijkse herhaling | Het interval tussen maanden wanneer het rapport wordt verzonden. |
   | Dag van de maand | De datum elke maand wanneer het rapport wordt verzonden.<p>Wanneer deze optie beschikbaar is, [!UICONTROL **Week van de maand**] en [!UICONTROL **Dag van de week**] zijn niet mogelijk. Selecteer de [!UICONTROL **Alternatieve indeling**] om heen en weer te schakelen. </p> |
   | Week van de maand | De week van elke maand waarin het verslag moet worden verzonden. <p>De volgende opties zijn beschikbaar:</p><ul><li>Eerste</li><li>Seconde</li><li>Derde</li><li>Vierde</li><p>Stuur het rapport over de vierde week, zelfs over maanden met 5 weken. Kies [!UICONTROL **Laatste**] als u het rapport wilt verzenden over de laatste week van elke maand.</p><li>Laatste</li></ul><p>Wanneer deze optie beschikbaar is, [!UICONTROL **Dag van de maand**] is niet mogelijk. Selecteer de [!UICONTROL **Alternatieve indeling**] om heen en weer te schakelen. </p> |
   | Dag van de week | De dag van de week waarop het verslag moet worden verzonden. <p>Wanneer deze optie beschikbaar is, [!UICONTROL **Dag van de maand**] is niet mogelijk. Selecteer de [!UICONTROL **Alternatieve indeling**] om heen en weer te schakelen. </p> |
   | Starten bij | De datum waarop het nieuwe schema zou moeten beginnen. |
   | Tijd van dag | Het tijdstip waarop het verslag moet worden verzonden. |
   | Opties voor eindlevering | Kies wanneer de geplande leveringen moeten worden beëindigd. U kunt ervoor kiezen nooit te beëindigen, na een bepaald aantal exemplaren te beëindigen of op een bepaalde datum te eindigen. |

   {style="table-layout:auto"}

1. Ga door met het configureren van uw verzoek voor Data Warehouse op de [!UICONTROL **Bericht**] tab. Zie voor meer informatie [Een e-mailbericht configureren voor een aanvraag van een Data Warehouse](/help/export/data-warehouse/create-request/dw-request-email.md).

