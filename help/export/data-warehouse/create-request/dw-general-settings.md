---
description: Stappen die beschrijven hoe te om een verzoek van de Data Warehouse tot stand te brengen.
title: Algemene instellingen voor verzoek om Data Warehouse
feature: Data Warehouse
exl-id: f564d5a9-78a2-431e-987a-78c4b0b9d31e
source-git-commit: 1e1a26b8595ca026fb049322125a6f91d9d5513c
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 1%

---

# Algemene instellingen voor verzoek om Data Warehouse

Er zijn diverse configuratieopties beschikbaar wanneer het creëren van een verzoek van de Data Warehouse. De volgende informatie beschrijft hoe te om algemene montages voor het verzoek te vormen.

Voor informatie over hoe te beginnen creërend een verzoek, evenals verbindingen aan andere belangrijke configuratieopties, zie [&#x200B; een verzoek van de Data Warehouse &#x200B;](/help/export/data-warehouse/create-request/t-dw-create-request.md) creëren.

Algemene instellingen configureren voor een verzoek om Data Warehouse:

1. Begin creërend een verzoek van de Data Warehouse in Adobe Analytics door **[!UICONTROL Tools]** te selecteren > **[!UICONTROL Data Warehouse]** > [!UICONTROL **voeg**] toe.

   Voor extra details, zie [&#x200B; een verzoek van de Data Warehouse &#x200B;](/help/export/data-warehouse/create-request/t-dw-create-request.md) creëren.

1. Voor de Nieuwe pagina van het de verzoekverzoek van de Data Warehouse, selecteer de [!UICONTROL **Algemene montages**] tabel.

   ![&#x200B; de bestemmingslusje van het Rapport &#x200B;](assets/dw-general-settings.png)

1. Vul de volgende velden in:

   | Optie | Functie |
   |---------|----------|
   | Naam aanvraag | Deze naam wordt op de hoofdpagina van de Data Warehouse weergegeven wanneer u aanvragen beheert. |
   | Datumbereiken | Selecteer het datumbereik dat u wilt opnemen in het rapport. <p>U kunt aangepaste datums of een vooraf ingesteld datumbereik kiezen. De vooraf ingestelde waaiers zijn met betrekking tot de datum het rapport wordt verzonden.</p><p>De volgende voorinstellingsopties zijn beschikbaar:</p><ul><li>Vandaag</li><li>Gisteren</li><li>Laatste 7 dagen</li><li>Laatste 30 dagen</li><li>Deze week</li><li>Vorige week</li><li>Afgelopen 2 weken</li><li>Afgelopen 3 weken</li><li>Afgelopen 4 weken</li><li>Deze maand</li><li>Vorige maand</li><li>Laatste uur</li></ul> |
   | Granulariteit | De tijdsgranulariteit. Geldige waarden zijn None, Hour, Day, Week, Month, Quarter en Year.<p>Het melden van granulariteit vereist extra verwerkingstijd. Als u maandelijks granulariteit voor een volledig jaar rapporteert, verwerkt uw rapporten veel sneller als u een rapportverzoek voor elke maand indient.</p><p>**Nota:** wanneer het toepassen van granulariteit in een verzoek van de Data Warehouse, wordt de kolom van de &quot;Datum&quot;toegevoegd aan het rapport. Afhankelijk van de geselecteerde granulariteit wordt de datumnotatie als volgt gewijzigd:</p><ul><li>**Uur granulariteit**:<ul> <li>**Formaat**: `mmmm d, yyyy` Uur `H`</li><li>**Voorbeeld**: 1 Januari, 20XX, Uur 0 </li></ul><li>**Dagelijkse granulariteit**:<ul> <li>**Formaat**: `mmmm d, yyyy`</li><li>**Voorbeeld**: 1 Januari, 20XX</li></ul><li>**Wekelijkse granulariteit**:<ul> <li>**Formaat**: Week `w, yyyy`</li><li>**Voorbeeld**: Week 1, 20XX </li></ul><li>**Maandelijkse granulariteit**:<ul> <li>**Formaat**: `mmmm yyyy`</li><li>**Voorbeeld**: 20XX Januari </li></ul><li>**Kwartaalgranulariteit**:<ul> <li>**Formaat**: `q` Kwartaal `yyyy`</li><li>**Voorbeeld**: 1ste Kwartaal 20XX </li></ul><li>**jaarlijkse granulariteit**:<ul> <li>**Formaat**: `yyyy`</li><li>**Voorbeeld**: 20XX</li></ul> |
   | Beschikbaar maken voor gebruikers in uw organisatie | Alle verzoeken van het gegevenspakhuis zijn zichtbaar slechts aan u en om het even welke systeembeheerders. Schakel deze optie in als u het verzoek zichtbaar wilt maken voor iedereen in uw organisatie. <p>Het is handig deze optie in te schakelen als u wilt dat andere gebruikers in uw organisatie de aanvraag kunnen maken of bijwerken.</p> |

   {style="table-layout:auto"}

1. Ga verder vormend uw verzoek van de Data Warehouse op [!UICONTROL **bouwt uw rapport**] tabel. Voor meer informatie, zie [&#x200B; een rapport voor een verzoek van de Data Warehouse &#x200B;](/help/export/data-warehouse/create-request/dw-request-build-report.md) bouwen.
