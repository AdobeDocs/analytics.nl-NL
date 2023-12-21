---
description: Stappen die beschrijven hoe te om een verzoek van de Data Warehouse tot stand te brengen.
title: Vorm een rapportbestemming voor een verzoek van de Data Warehouse
feature: Data Warehouse
exl-id: e5f8acaa-156f-41fb-a0fc-bc5475f1f3b7
source-git-commit: 1bd46f104c5ebcca78d624b49c56b2992c3d62cb
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 2%

---

# Configureer de planningsopties voor een Data Warehouse-verzoek

Er zijn diverse configuratieopties beschikbaar wanneer het creëren van een verzoek van de Data Warehouse. De volgende informatie beschrijft hoe te om het plannen opties voor het verzoek te vormen.

Voor informatie over hoe te beginnen creërend een verzoek, evenals verbindingen aan andere belangrijke configuratieopties, zie [Een Data Warehouse-aanvraag maken](/help/export/data-warehouse/create-request/t-dw-create-request.md).

Om het plannen opties voor een verzoek van de Data Warehouse te vormen:

1. Begin met het maken van een aanvraag in Adobe Analytics door **[!UICONTROL Tools]** > **[!UICONTROL Data Warehouse]** > [!UICONTROL **Toevoegen**].

   Zie voor meer informatie [Een Data Warehouse-aanvraag maken](/help/export/data-warehouse/create-request/t-dw-create-request.md).

1. Selecteer op de aanvraagpagina Nieuwe Data Warehouse de optie [!UICONTROL **Planningsopties**] tab.

   ![Tabblad Doel rapporteren](assets/dw-scheduling-options.png) <!-- update screenshot -->

1. Vul de volgende velden in:

   | Optie | Functie |
   |---------|----------|
   | [!UICONTROL **Rapport nu verzenden**] | Verzendt het rapport als een eenmalig rapport. Als deze optie is geselecteerd, worden alle planningsopties verborgen. |
   | [!UICONTROL **Plan voor later**] | Verstrekt opties voor het plannen van rapportlevering. Alle opties worden hieronder beschreven. |
   | [!UICONTROL **Rapportfrequentie**] | De frequentie waarmee rapporten worden geleverd. <p>De volgende opties zijn beschikbaar:</p><ul><li>Uurlijks</li><p>[!UICONTROL **Uur**] is alleen beschikbaar als de [!UICONTROL **Datumbereiken**] de optie [!UICONTROL **Algemene instellingen**] tab is ingesteld op [!UICONTROL **Laatste uur**].</p><li>Dagelijks</li><li>Wekelijks</li><li>Maandelijks</li><li>Jaarlijks</li></ul><p>Afhankelijk van de frequentie die u selecteert, worden aanvullende opties weergegeven.</p> |
   | [!UICONTROL **Starten bij**] | De datum waarop het nieuwe schema zou moeten beginnen. |
   | [!UICONTROL **Tijd van dag**] | Het tijdstip waarop het verslag moet worden verzonden. |
   | [!UICONTROL **Opties voor eindlevering**] | Kies wanneer de geplande leveringen moeten worden beëindigd. U kunt ervoor kiezen nooit te beëindigen, na een bepaald aantal exemplaren te beëindigen of op een bepaalde datum te eindigen. |

   {style="table-layout:auto"}

1. Ga door met het configureren van uw verzoek voor Data Warehouse op de [!UICONTROL **Bericht**] tab. Zie voor meer informatie [Een e-mailbericht configureren voor een aanvraag van een Data Warehouse](/help/export/data-warehouse/create-request/dw-request-email.md).
