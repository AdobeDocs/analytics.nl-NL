---
description: Verklaart de noodzakelijke voorbereidingen om componenten en projecten van Adobe Analytics aan Customer Journey Analytics voor te bereiden.
title: Migratie van onderdelen en projecten van Adobe Analytics naar Customer Journey Analytics voorbereiden
feature: Admin Tools
exl-id: a9ff98dc-6568-428d-a8a8-faca5bc76a29
source-git-commit: ca84a5f807545d7196e2e0e90d3209c32d3fd789
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 1%

---

# Migratie van onderdelen en projecten van Adobe Analytics naar Customer Journey Analytics voorbereiden

Alvorens iedereen in uw organisatie begint migrerend projecten zoals die in [ worden beschreven componenten en projecten van Adobe Analytics aan Customer Journey Analytics ](/help/admin/tools/component-migration/component-migration.md) migreren, voltooi de volgende secties.

## Vereisten

Alvorens uw projecten en hun bijbehorende componenten klaar zijn om te migreren, moet u eerst de stappen in [ Evolutie van Adobe Analytics ](https://experienceleague.adobe.com/docs/analytics-platform/using/compare-aa-cja/aa-to-cja.html) in de Gids van Adobe Customer Journey Analytics volgen. Deze stappen omvatten:

1. Gebruik een van de volgende methoden om gegevens in te voeren in Adobe Experience Platform om Adobe Analytics-rapportsuite-gegevens in Customer Journey Analytics weer te geven:

   >[!NOTE]
   >
   >  Wanneer u WebSDK gebruikt om gegevens in te voeren, moeten alle schemagebieden manueel in kaart worden gebracht. (Voor meer informatie over het kaartproces, zie [ componenten en projecten van Adobe Analytics aan Customer Journey Analytics migreren ](/help/admin/tools/component-migration/component-migration.md))


   * Als u de Adobe Analytics-bronconnector wilt gebruiken, moet u:

      1. [ de reeksen van het opstellingsrapport voor opname in Adobe Experience Platform en Customer Journey Analytics ](https://experienceleague.adobe.com/docs/analytics-platform/using/compare-aa-cja/cja-aa-comparison/aa-data-in-cja.html#set-up-report-suites-for-ingestion-into-the-adobe-experience-platform-and-customer-journey-analytics)

      1. [ Samenvatten en gebruiken de gegevens ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/analytics.html)

   * Om WebSDK te gebruiken, moet u:

      1. [ de reeksen van het opstellingsrapport voor opname in Adobe Experience Platform en Customer Journey Analytics ](https://experienceleague.adobe.com/docs/analytics-platform/using/compare-aa-cja/cja-aa-comparison/aa-data-in-cja.html#set-up-report-suites-for-ingestion-into-the-adobe-experience-platform-and-customer-journey-analytics)

      1. [ Ingest gegevens via het Web SDK van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk.html)

1. Creeer a [ verbinding ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/overview.html) en [ gegevensmening ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html) met de opgenomen gegevens.

1. Zorg ervoor dat gebruikers in Customer Journey Analytics zijn ingericht voor de gegevensweergaven waarin gegevens worden toegewezen.

   Voor meer informatie, zie {de toestemmingen van 0} Customer Journey Analytics in Admin Console [ in ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-admin/cja-access-control.html#customer-journey-analytics-permissions-in-admin-console) de toegangscontrole van Customer Journey Analytics [.](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-admin/cja-access-control.html)

   Het tabblad Machtigingen maakt deel uit van elk productprofiel in Admin Console. U kunt gebruikers toevoegen aan specifieke productprofielen. Vervolgens wijst u rechten toe aan specifieke gegevensweergaven en geeft u op welke machtigingen de gebruikers in een productprofiel hebben.

1. Bepaal als organisatie hoe u componenten in kaart zult brengen.

   Voor meer informatie, zie de sectie hieronder, [ besluit als organisatie hoe u componenten ](#decide-as-an-organization-how-you-will-map-components) in kaart zult brengen.

## Begrijpen wat er in een migratie is opgenomen

In de volgende tabellen wordt aangegeven welke elementen van een project en component in een migratie zijn opgenomen:

### Componentelementen die worden gemigreerd

De afmetingen en de metriek worden gemigreerd als deel van het kaartproces dat in [ wordt beschreven migreren de projecten van Adobe Analytics aan Customer Journey Analytics ](#migrate-adobe-analytics-projects-to-customer-journey-analytics).

De segmenten, de datumwaaiers, en de berekende metriek die niet reeds in Customer Journey Analytics bestaan worden daar opnieuw gecreeerd gebaseerd op de afmetingen en de metriek die in kaart worden gebracht.

|  | Gegigreerd |
|---------|---------|
| **[Eigenaar](/help/components/calculated-metrics/workflow/cm-manager.md)** | Afmetingen en metingen: geen<p>Segmenten en datumwaaiers: ![ vinkje ](assets/Smock_Checkmark_18_N.svg)</p> |
| **[het Delen](/help/analyze/analysis-workspace/components/analysis-workspace-components.md)** | Afmetingen en metingen: geen<p>Segmenten en datumbereiken: Nee</p> |
| **[Beschrijvingen](/help/analyze/analysis-workspace/components/add-component-descriptions.md)** | Afmetingen en metingen: geen<p>Segmenten en datumwaaiers: ![ vinkje ](assets/Smock_Checkmark_18_N.svg)</p> |
| **[Markeringen](/help/analyze/analysis-workspace/components/analysis-workspace-components.md)** | Afmetingen en metingen: geen<p>Segmenten en datumbereiken: Nee</p> |
| **[Attributie (op afmetingen)](/help/analyze/analysis-workspace/attribution/overview.md)** | Afmetingen en metingen: geen<p>Segmenten en datumbereiken: Nee</p> |

{style="table-layout:auto"}

### Projectelementen die worden gemigreerd

|  | Gegigreerd |
|---------|----------|
| **[waaiers van de Datum](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md)** | ![ vinkje ](assets/Smock_Checkmark_18_N.svg) |
| **[Segmenten](/help/components/segmentation/seg-overview.md)** | ![ vinkje ](assets/Smock_Checkmark_18_N.svg) |
| **[Snelle segmenten](/help/analyze/analysis-workspace/components/segments/quick-segments.md)** | ![ vinkje ](assets/Smock_Checkmark_18_N.svg) |
| **[Dimensies](/help/components/dimensions/overview.md)** | ![ vinkje ](assets/Smock_Checkmark_18_N.svg) die automatisch of manueel in kaart wordt gebracht |
| **[Cijfers](/help/components/metrics/overview.md)** | ![ vinkje ](assets/Smock_Checkmark_18_N.svg) die automatisch of manueel in kaart wordt gebracht |
| **[Panelen](/help/analyze/analysis-workspace/c-panels/panels.md)** | ![ vinkje ](assets/Smock_Checkmark_18_N.svg) |
| **[Visualisaties](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md)** | ![ vinkje ](assets/Smock_Checkmark_18_N.svg) |
| **[Eigenaar](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md)** | ![ vinkje ](assets/Smock_Checkmark_18_N.svg) Gedefinieerd door gebruiker die de migratie doet |
| **[Kromming](/help/analyze/analysis-workspace/curate-share/curate.md)** | Nee |
| **[het Delen](/help/analyze/analysis-workspace/curate-share/share-projects.md)** | Nee |
| **[Annotaties](/help/analyze/analysis-workspace/components/annotations/overview.md)** | Nee |
| **[de structuur van de Omslag](/help/analyze/analysis-workspace/build-workspace-project/workspace-folders/about-folders.md)** | Nee |
| **[Beschrijvingen](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md)** | ![ vinkje ](assets/Smock_Checkmark_18_N.svg) |
| **[Markeringen](/help/analyze/landing.md)** | Nee |
| **[Favorieten](/help/analyze/landing.md)** | Nee |
| **[Programma&#39;s](/help/components/scheduled-projects-manager.md)** | Nee |
| **[Anomaliedetectie](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md)** | ![ vinkje ](assets/Smock_Checkmark_18_N.svg) |

{style="table-layout:auto"}

## Niet-ondersteunde elementen begrijpen die fouten veroorzaken

De volgende visualisaties en deelvensters worden niet ondersteund in Customer Journey Analytics. Wanneer deze elementen in een project vóór migratie zijn opgenomen, kunnen ze ervoor zorgen dat de migratie mislukt of dat er fouten optreden nadat het project is gemigreerd.

Verwijder deze elementen uit het Adobe Analytics-project voordat u het project naar Customer Journey Analytics migreert. Als een migratie mislukt, verwijdert u deze elementen voordat u de migratie opnieuw probeert.

### Niet-ondersteunde deelvensters

* [Analyses voor doel (A4T)](/help/analyze/analysis-workspace/c-panels/a4t-panel.md)

* [Segmentvergelijking](/help/analyze/analysis-workspace/c-panels/c-segment-comparison/segment-comparison.md)

* [Gemiddelde mediumgeluid](/help/analyze/analysis-workspace/c-panels/average-minute-audience-panel.md)

* [Volgende of vorige item](/help/analyze/analysis-workspace/c-panels/next-previous.md)

* [Overzicht van pagina](/help/analyze/analysis-workspace/c-panels/page-summary.md)

* [Contributieanalyse](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md#contribution-analysis)

## Besluit als organisatie hoe u componenten in kaart zult brengen

>[!NOTE]
>
>Tijdens het migratieproces worden componenten in uw Adobe Analytics-project geïdentificeerd die niet automatisch kunnen worden toegewezen aan componenten in Customer Journey Analytics. U kunt deze componenten dan handmatig toewijzen.
>
>**om het even welke die afbeeldingen op één project worden gemaakt is op alle toekomstige projecten over uw volledige IMS org van toepassing, ongeacht welke gebruiker de migratie uitvoert. Deze toewijzingen kunnen worden bijgewerkt wanneer het migreren van toekomstige projecten.**
>
>Het is belangrijk dat uw organisatie bepaalt hoe dimensies en metriek zullen worden in kaart gebracht alvorens om het even welke projecten worden gemigreerd. Als u dit doet, voorkomt u dat afzonderlijke beheerders beslissingen nemen in een silo wanneer u slechts één project overweegt.
>
>Hier volgt een lijst met afmetingen en metriek die u handmatig moet toewijzen als deze in uw project bestaan. We raden u aan deze lijst vóór uw migratie te herzien. Als een van deze componenten in uw project aanwezig is, bepaalt u nu aan welke Customer Journey Analytics-componenten u ze wilt toewijzen.


### Afmetingen die handmatig moeten worden toegewezen

* averagepagetime
* pagetimeseconds
* singlepagevisits
* bezoeker
* tijdvoorafgaande
* tijdsbestek
* categorie
* connectiontype
* klantentrouw
* customlink
* downloadlink
* exitlink
* hitte
* hittype
* padlengte
* daysbefore firstpurchase
* dayssincelastaankoop
* dayssincelastbezoek
* identificatiestaat
* optoverraad
* aanhoudend cookie
* retourfrequentie
* zoekmachine
* searchenginenaturaltrefwoord
* mobiel
* monitorresolutie
* landmeter
* mcaudiëntie
* tntbase
* doelwit


### Metrisch die handmatig moeten worden toegewezen

* timespentbezoek
* timespentbezoeker
* herladen
* golven
* bouncering
* pageevents
* pageviewspervisit
* orderspervisje
* averagePageDepent
* averagetimespentonsite
* exitlinkinstanties
* customlinkinstances
* downloadlinkinstanties
* darkbezoekers
* singlepagevisits
* singlevaluatie
* bezoekerhomepage
* bezoekersmcvisus
* pagesnotfound
* newengaals
* time_granularity
* gelijktijdige_viewers_bezoekers
* concurrent_viewers_occurrences
* apparaten
* schatten
* playback_time_used_seconds
* playback_time_used_minutes
* average_minute_publiek_time_based
* average_minute_publiek_media_time
* average_minute_publiek_content_time
* video_length
* doelconversie
* doelgerichtheid
