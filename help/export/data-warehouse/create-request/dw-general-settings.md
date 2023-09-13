---
description: Stappen die beschrijven hoe te om een verzoek van de Data Warehouse tot stand te brengen.
title: Algemene instellingen voor verzoek om Data Warehouse
feature: Data Warehouse
source-git-commit: ea4c1ae21f2c83bad92723e6ffd2e706fac5e1e8
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 1%

---

# Algemene instellingen voor verzoek om Data Warehouse

>[!AVAILABILITY]
>
>Sommige functies voor Data Warehouse die in dit artikel worden beschreven (en andere artikelen voor Data Warehouse in deze sectie) zijn alleen beschikbaar in de beperkte testfase van de release en zijn mogelijk nog niet beschikbaar in uw omgeving.
>
>Voor informatie over welke functies nog niet voor alle klanten beschikbaar zijn, en voor informatie over de releasetijdlijn van deze functies, raadpleegt u de [releaseopmerkingen](/help/release-notes/latest.md).
>
>Deze notitie wordt verwijderd wanneer de functionaliteit algemeen beschikbaar is. Voor informatie over het evaluatieproces Analytics raadpleegt u [Adobe Analytics-functiereleases](/help/release-notes/releases.md).

Er zijn diverse configuratieopties beschikbaar wanneer het creëren van een verzoek van de Data Warehouse. De volgende informatie beschrijft hoe te om algemene montages voor het verzoek te vormen.

Voor informatie over hoe te beginnen creërend een verzoek, evenals verbindingen aan andere belangrijke configuratieopties, zie [Een Data Warehouse-aanvraag maken](/help/export/data-warehouse/create-request/t-dw-create-request.md).

Algemene instellingen configureren voor een verzoek om Data Warehouse:

1. Begin met het maken van een Data Warehouse-aanvraag in Adobe Analytics door **[!UICONTROL Tools]** > **[!UICONTROL Data Warehouse]** > [!UICONTROL **Toevoegen**].

   Zie voor meer informatie [Een Data Warehouse-aanvraag maken](/help/export/data-warehouse/create-request/t-dw-create-request.md).

1. Selecteer op de aanvraagpagina Nieuwe Data Warehouse de optie [!UICONTROL **Algemene instellingen**] tab.

   ![Tabblad Doel rapporteren](assets/dw-general-settings.png)

1. Vul de volgende velden in:

   | Optie | -functie |
   |---------|----------|
   | Naam aanvraag | Deze naam wordt op de hoofdpagina van de Data Warehouse weergegeven wanneer u aanvragen beheert. |
   | Datumbereiken | Selecteer het datumbereik dat u wilt opnemen in het rapport. <p>U kunt aangepaste datums of een vooraf ingesteld datumbereik kiezen. De vooraf ingestelde waaiers zijn met betrekking tot de datum het rapport wordt verzonden.</p><p>De volgende voorinstellingsopties zijn beschikbaar:</p><ul><li>Vandaag</li><li>Gisteren</li><li>Laatste 7 dagen</li><li>Laatste 30 dagen</li><li>Deze week</li><li>Vorige week</li><li>Afgelopen 2 weken</li><li>Afgelopen 3 weken</li><li>Afgelopen 4 weken</li><li>Deze maand</li><li>Vorige maand</li><li>Laatste uur</li></ul> |
   | Granulariteit | <!--what does this setting do? It's not the schedule/frequency... --> De tijdsgranulariteit. Geldige waarden zijn None, Hour, Day, Week, Month, Quarter en Year.<p>Het melden van granulariteit vereist extra verwerkingstijd. Als u maandelijks granulariteit voor een volledig jaar rapporteert, verwerkt uw rapporten veel sneller als u een rapportverzoek voor elke maand indient.</p> |

   {style="table-layout:auto"}

1. Ga door met het configureren van uw verzoek voor Data Warehouse op de [!UICONTROL **Uw rapport samenstellen**] tab. Zie voor meer informatie [Bouw een rapport voor een verzoek van de Data Warehouse](/help/export/data-warehouse/create-request/dw-request-build-report.md).