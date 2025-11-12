---
description: Stappen die beschrijven hoe u een Data Warehouse-aanvraag maakt.
title: Algemene instellingen Data Warehouse-verzoek
feature: Data Warehouse
exl-id: f564d5a9-78a2-431e-987a-78c4b0b9d31e
source-git-commit: ca84a5f807545d7196e2e0e90d3209c32d3fd789
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 1%

---

# Algemene instellingen Data Warehouse-verzoek

Er zijn verschillende configuratieopties beschikbaar wanneer u een Data Warehouse-aanvraag maakt. De volgende informatie beschrijft hoe te om algemene montages voor het verzoek te vormen.

Voor informatie over hoe te beginnen creërend een verzoek, evenals verbindingen aan andere belangrijke configuratieopties, zie [&#x200B; een verzoek van Data Warehouse &#x200B;](/help/export/data-warehouse/create-request/t-dw-create-request.md) creëren.

Algemene instellingen configureren voor een Data Warehouse-aanvraag:

1. Begin creërend een verzoek van Data Warehouse in Adobe Analytics door te selecteren **[!UICONTROL Tools]** > **[!UICONTROL Data Warehouse]** > [!UICONTROL **voeg**] toe.

   Voor extra details, zie [&#x200B; een verzoek van Data Warehouse &#x200B;](/help/export/data-warehouse/create-request/t-dw-create-request.md) creëren.

1. Voor de Nieuwe Data Warehouse verzoekpagina, selecteer de [!UICONTROL **Algemene montages**] tabel.

   ![&#x200B; de bestemmingslusje van het Rapport &#x200B;](assets/dw-general-settings.png)

1. Vul de volgende velden in:

   | Optie | Functie |
   |---------|----------|
   | Naam aanvraag | Deze naam wordt weergegeven op de Data Warehouse-hoofdpagina wanneer u aanvragen beheert. |
   | Datumbereiken | Selecteer het datumbereik dat u wilt opnemen in het rapport. <p>U kunt aangepaste datums of een vooraf ingesteld datumbereik kiezen. De vooraf ingestelde waaiers zijn met betrekking tot de datum het rapport wordt verzonden.</p><p>De volgende voorinstellingsopties zijn beschikbaar:</p><ul><li>Vandaag</li><li>Gisteren</li><li>Laatste 7 dagen</li><li>Laatste 30 dagen</li><li>Deze week</li><li>Vorige week</li><li>Afgelopen 2 weken</li><li>Afgelopen 3 weken</li><li>Afgelopen 4 weken</li><li>Deze maand</li><li>Vorige maand</li><li>Laatste uur</li></ul> |
   | Granulariteit | De tijdsgranulariteit. Geldige waarden zijn None, Hour, Day, Week, Month, Quarter en Year.<p>Het melden van granulariteit vereist extra verwerkingstijd. Als u maandelijks granulariteit voor een volledig jaar rapporteert, verwerkt uw rapporten veel sneller als u een rapportverzoek voor elke maand indient.</p><p>**Nota:** wanneer het toepassen van granulariteit in een verzoek van Data Warehouse, wordt de kolom van de &quot;Datum&quot;toegevoegd aan het rapport. Afhankelijk van de geselecteerde granulariteit wordt de datumnotatie als volgt gewijzigd:</p><ul><li>**Uur granulariteit**:<ul> <li>**Formaat**: `mmmm d, yyyy` Uur `H`</li><li>**Voorbeeld**: 1 Januari, 20XX, Uur 0 </li></ul><li>**Dagelijkse granulariteit**:<ul> <li>**Formaat**: `mmmm d, yyyy`</li><li>**Voorbeeld**: 1 Januari, 20XX</li></ul><li>**Wekelijkse granulariteit**:<ul> <li>**Formaat**: Week `w, yyyy`</li><li>**Voorbeeld**: Week 1, 20XX </li></ul><li>**Maandelijkse granulariteit**:<ul> <li>**Formaat**: `mmmm yyyy`</li><li>**Voorbeeld**: 20XX Januari </li></ul><li>**Kwartaalgranulariteit**:<ul> <li>**Formaat**: `q` Kwartaal `yyyy`</li><li>**Voorbeeld**: 1ste Kwartaal 20XX </li></ul><li>**jaarlijkse granulariteit**:<ul> <li>**Formaat**: `yyyy`</li><li>**Voorbeeld**: 20XX</li></ul> |
   | Beschikbaar maken voor gebruikers in uw organisatie | Alle verzoeken van het gegevenspakhuis zijn zichtbaar slechts aan u en om het even welke systeembeheerders. Schakel deze optie in als u het verzoek zichtbaar wilt maken voor iedereen in uw organisatie. <p>Het is handig deze optie in te schakelen als u wilt dat andere gebruikers in uw organisatie de aanvraag kunnen maken of bijwerken.</p> |

   {style="table-layout:auto"}

1. Ga door uw verzoek van Data Warehouse op [!UICONTROL **vormen uw rapport**] tabel. Voor meer informatie, zie [&#x200B; een rapport voor een verzoek van Data Warehouse &#x200B;](/help/export/data-warehouse/create-request/dw-request-build-report.md) bouwen.
