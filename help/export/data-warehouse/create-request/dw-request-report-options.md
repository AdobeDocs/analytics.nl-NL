---
description: Stappen die beschrijven hoe u een Data Warehouse-aanvraag maakt.
title: Rapportopties configureren voor een Data Warehouse-aanvraag
feature: Data Warehouse
exl-id: b273bddb-431c-44d9-82a5-cb088829b3a3
source-git-commit: ca84a5f807545d7196e2e0e90d3209c32d3fd789
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# Rapportopties configureren voor een Data Warehouse-aanvraag

Er zijn verschillende configuratieopties beschikbaar wanneer u een Data Warehouse-aanvraag maakt. De volgende informatie beschrijft hoe te om rapportopties voor het verzoek te vormen.

Voor informatie over hoe te beginnen creërend een verzoek, evenals verbindingen aan andere belangrijke configuratieopties, zie [ een verzoek van Data Warehouse ](/help/export/data-warehouse/create-request/t-dw-create-request.md) creëren.

Om rapportopties voor een Data Warehouse verzoek te vormen:

1. Als u niet reeds hebt, begin creërend een verzoek in Adobe Analytics door te selecteren **[!UICONTROL Tools]** > **[!UICONTROL Data Warehouse]** > [!UICONTROL **voeg**] toe.

   Voor extra details, zie [ een verzoek van Data Warehouse ](/help/export/data-warehouse/create-request/t-dw-create-request.md) creëren.

1. Voor de Nieuwe Data Warehouse verzoekpagina, selecteer de [!UICONTROL **opties van het Rapport**] tabel.

   ![ het bestemmingslusje van het Rapport ](assets/dw-report-options.png) <!-- update screenshot to include Sort by metrics -->

1. Vul de volgende velden in:

   | Optie | Functie |
   |---------|----------|
   | [!UICONTROL **de naam van het Dossier**] | Identificeert het rapport. <p>Als een van de volgende speciale tekens in de bestandsnaam wordt gebruikt, kan de aanvraag niet worden opgeslagen: <code>! &quot; # $ &amp; &#39; ( ) * + , / : ; > = &lt; ? @ [ ] \ ^ ` { } \| ~</code> </p><p>Het teken % kan alleen worden gebruikt als het wordt gevolgd door &quot;R&quot;, &quot;rsid&quot; of &quot;id&quot;, als volgt: <code>%R</code>, <code>%rsid</code>en <code>%id</code>.</p> |
   | [!UICONTROL **voeg de waaier van de rapportdatum aan dossier toe - noem**] | Hiermee voegt u het datumbereik toe aan de naam van het rapportbestand. <p>Als u bijvoorbeeld gegevens aanvraagt van 1 mei 2024 tot en met 7 mei 2024, bevat de bestandsnaam het datumbereik 20240501 - 20240507.</p> |
   | [!UICONTROL **CSV**] | Levert rapporten in een CSV-bestandsindeling voor het weergeven van gegevens in een spreadsheet. |
   | [!UICONTROL **Tableau (TDE)**] | Levert rapporten in een het dossierformaat van de Uitvoer van Gegevens van Tableau (TDE), dat kan worden gebruikt om gegevens en laag in extra gegevens binnen Tableau te visualiseren. |
   | [!UICONTROL **verzendt rapport als samengeperst dossier (ZIP)**] | Levert rapporten in een gecomprimeerde (ZIP) dossierformaat. Wij adviseren toelatend deze optie wanneer het gebruiken van e-mail als [ rapportbestemming ](/help/export/data-warehouse/create-request/dw-request-report-destinations.md). |
   | [!UICONTROL **terugkeer alle rijen**] | Wanneer toegelaten, zijn alle rijen inbegrepen in het rapport. Schakel deze optie uit om het aantal rijen op te geven dat u wilt opnemen. |
   | [!UICONTROL **Begin van rapportcommentaren**] | Voeg eventuele opmerkingen toe die u in het rapport wilt opnemen. De commentaren verschijnen aan het begin van het rapport. |
   | [!UICONTROL **Soort door metriek**] | Verstrekt gerangschikte verdelingsrapporten in Data Warehouse, die door dalende metrische waarde wordt gesorteerd. Sorteren op metrische waarde maakt Data Warehouse-rapporten gemakkelijker voor u te interpreteren en maakt deze rapporten gemakkelijker te vergelijken met andere analytische rapportage-weergaven.<p>Voor meer informatie, zie [ Soort door metrisch ](/help/export/data-warehouse/sorting-by-metric.md).</p> |
   | [!UICONTROL **verzend een manifestdossier**] | Omvat meta-gegevens over de dossiers inbegrepen in het rapport.<!-- What kind of metadata is included in the manifest file? --> |
   | [!UICONTROL **verzend een digitaal handtekeningsdossier**] | Hiermee kunnen ontvangers van rapporten controleren of het bestand uit Adobe afkomstig is en of het niet is gewijzigd. |
   | [!UICONTROL **verzend een leeg dossier wanneer er geen gegevens in het rapport**] zijn | Verzendt een rapport zelfs wanneer het rapport geen gegevens bevat. |

   {style="table-layout:auto"}

1. Ga door het vormen van uw verzoek van Data Warehouse op het [!UICONTROL **Plannende opties**] tabel. Voor meer informatie, zie [ het plannen opties voor een verzoek van Data Warehouse ](/help/export/data-warehouse/create-request/dw-request-scheduling.md) vormen.
