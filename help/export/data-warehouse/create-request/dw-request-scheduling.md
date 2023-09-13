---
description: Stappen die beschrijven hoe te om een verzoek van de Data Warehouse tot stand te brengen.
title: Vorm een rapportbestemming voor een verzoek van de Data Warehouse
feature: Data Warehouse
source-git-commit: 3b116cb8d0d3f3eb86b512d712f37b29876f2b22
workflow-type: tm+mt
source-wordcount: '372'
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
   | [!UICONTROL **Rapport nu verzenden**] | Verzendt het rapport als een eenmalig rapport. Als deze optie is geselecteerd, worden alle planningsopties verborgen. |
   | [!UICONTROL **Plan voor later**] | Verstrekt opties voor het plannen van rapportlevering. Alle opties worden hieronder beschreven. |
   | [!UICONTROL **Rapportfrequentie**] | De frequentie waarmee rapporten worden geleverd. <p>De volgende opties zijn beschikbaar:</p><ul><li>Uurlijks</li><p>[!UICONTROL **Uur**] is alleen beschikbaar als de [!UICONTROL **Datumbereiken**] de optie [!UICONTROL **Algemene instellingen**] tab is ingesteld op [!UICONTROL **Laatste uur**].</p><li>Dagelijks</li><li>Wekelijks</li><li>Maandelijks</li><li>Jaarlijks</li></ul><p>Afhankelijk van de frequentie die u selecteert, worden aanvullende opties weergegeven.</p> |
   | [!UICONTROL **Starten bij**] | De datum waarop het nieuwe schema zou moeten beginnen. |
   | [!UICONTROL **Tijd van dag**] | Het tijdstip waarop het verslag moet worden verzonden. |
   | [!UICONTROL **Opties voor eindlevering**] | Kies wanneer de geplande leveringen moeten worden beëindigd. U kunt ervoor kiezen nooit te beëindigen, na een bepaald aantal exemplaren te beëindigen of op een bepaalde datum te eindigen. |

   {style="table-layout:auto"}

1. Ga door met het configureren van uw verzoek voor Data Warehouse op de [!UICONTROL **Bericht**] tab. Zie voor meer informatie [Een e-mailbericht configureren voor een aanvraag van een Data Warehouse](/help/export/data-warehouse/create-request/dw-request-email.md).

