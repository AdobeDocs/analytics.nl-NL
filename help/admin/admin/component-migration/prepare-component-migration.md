---
description: Verklaart de noodzakelijke voorbereidingen om componenten en projecten van Adobe Analytics aan Customer Journey Analytics voor te bereiden.
title: Migratie van onderdelen en projecten van Adobe Analytics naar Customer Journey Analytics voorbereiden
feature: Admin Tools
exl-id: a9ff98dc-6568-428d-a8a8-faca5bc76a29
source-git-commit: 03120156e1ba70e50b265da788fa5997fd31c93e
workflow-type: tm+mt
source-wordcount: '939'
ht-degree: 2%

---

# Migratie van onderdelen en projecten van Adobe Analytics naar Customer Journey Analytics voorbereiden

Voordat iemand in uw organisatie begint met het migreren van projecten zoals beschreven in [Componenten en projecten migreren van Adobe Analytics naar Customer Journey Analytics](/help/admin/admin/component-migration/component-migration.md), vult u de volgende secties in.

## Vereisten

Voordat uw projecten en de bijbehorende componenten kunnen worden gemigreerd, moet u eerst het volgende doen:

* Gebruik een van de volgende methoden om gegevens in te voeren in Adobe Experience Platform om Adobe Analytics-gegevens van rapportsuite in Customer Journey Analytics weer te geven:

  >[!NOTE]
  >
  >  Wanneer u WebSDK gebruikt om gegevens in te voeren, moeten alle schemagebieden manueel in kaart worden gebracht. (Zie voor meer informatie over het toewijzingsproces [Componenten en projecten migreren van Adobe Analytics naar Customer Journey Analytics](/help/admin/admin/component-migration/component-migration.md))


   * Als u de Adobe Analytics-bronconnector wilt gebruiken, moet u:

      * [Rapportagesuites instellen voor opname in Adobe Experience Platform en Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/compare-aa-cja/cja-aa-comparison/aa-data-in-cja.html?lang=en#set-up-report-suites-for-ingestion-into-the-adobe-experience-platform-and-customer-journey-analytics)

      * [Gegevens opnemen en gebruiken](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/analytics.html)

   * Om WebSDK te gebruiken, moet u:

      * [Rapportagesuites instellen voor opname in Adobe Experience Platform en Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/compare-aa-cja/cja-aa-comparison/aa-data-in-cja.html?lang=en#set-up-report-suites-for-ingestion-into-the-adobe-experience-platform-and-customer-journey-analytics)

      * [Gegevens invoeren via de Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk.html)

* Een [verbinding](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/overview.html) en [gegevensweergave](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html) met de opgenomen gegevens.

* Zorg ervoor dat gebruikers in de Customer Journey Analytics zijn ingericht voor de gegevensweergaven waarin gegevens worden toegewezen.

  Zie voor meer informatie [De toestemmingen van de Customer Journey Analytics in de Admin Console](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-admin/cja-access-control.html?lang=en#customer-journey-analytics-permissions-in-admin-console) in [Toegangsbeheer Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-admin/cja-access-control.html).

  Het tabblad Machtigingen maakt deel uit van elk productprofiel in Admin Console. U kunt gebruikers toevoegen aan specifieke productprofielen. Vervolgens wijst u rechten toe aan specifieke gegevensweergaven en geeft u op welke machtigingen de gebruikers in een productprofiel hebben.

* Bepaal als organisatie hoe u componenten in kaart zult brengen.

  Zie de volgende sectie voor meer informatie: [Besluit als organisatie hoe u componenten in kaart zult brengen](#decide-as-an-organization-how-you-will-map-components).

## Begrijpen wat er in een migratie is opgenomen

In de volgende tabellen wordt aangegeven welke elementen van een project en component zijn opgenomen in een migratie:

### Componentelementen die worden gemigreerd

Dimensionen en maateenheden worden gemigreerd als onderdeel van het toewijzingsproces dat wordt beschreven in [Adobe Analytics-projecten migreren naar Customer Journey Analytics](#migrate-adobe-analytics-projects-to-customer-journey-analytics).

De segmenten, de datumwaaiers, en de berekende metriek die niet reeds in Customer Journey Analytics bestaan worden daar opnieuw gecreeerd gebaseerd op de afmetingen en de metriek die in kaart worden gebracht.

|  | Gegigreerd |
|---------|---------|
| **[Eigenaar](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-manager.md)** | Dimensionen en maatstaven: Nee<p>Segmenten en datumbereiken: ![vinkje](assets/Smock_Checkmark_18_N.svg)</p> |
| **[Delen](/help/analyze/analysis-workspace/components/analysis-workspace-components.md)** | Dimensionen en maatstaven: Nee<p>Segmenten en datumbereiken: Nee</p> |
| **[Beschrijvingen](/help/analyze/analysis-workspace/components/add-component-descriptions.md)** | Dimensionen en maatstaven: Nee<p>Segmenten en datumbereiken: ![vinkje](assets/Smock_Checkmark_18_N.svg)</p> |
| **[Tags](/help/analyze/analysis-workspace/components/analysis-workspace-components.md)** | Dimensionen en maatstaven: Nee<p>Segmenten en datumbereiken: Nee</p> |
| **[Attributie (op afmetingen)](/help/analyze/analysis-workspace/attribution/overview.md)** | Dimensionen en maatstaven: Nee<p>Segmenten en datumbereiken: Nee</p> |

{style="table-layout:auto"}

### Projectelementen die worden gemigreerd

|  | Gegigreerd |
|---------|----------|
| **[Datumbereiken](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md)** | ![vinkje](assets/Smock_Checkmark_18_N.svg) |
| **[Segmenten](/help/components/segmentation/seg-overview.md)** | ![vinkje](assets/Smock_Checkmark_18_N.svg) |
| **[Snelle segmenten](/help/analyze/analysis-workspace/components/segments/quick-segments.md)** | ![vinkje](assets/Smock_Checkmark_18_N.svg) |
| **[Dimensies](/help/components/dimensions/overview.md)** | ![vinkje](assets/Smock_Checkmark_18_N.svg) Automatisch of handmatig toegewezen |
| **[Cijfers](/help/components/metrics/overview.md)** | ![vinkje](assets/Smock_Checkmark_18_N.svg) Automatisch of handmatig toegewezen |
| **[Deelvensters](/help/analyze/analysis-workspace/c-panels/panels.md)** | ![vinkje](assets/Smock_Checkmark_18_N.svg) |
| **[Visualisaties](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md)** | ![vinkje](assets/Smock_Checkmark_18_N.svg) |
| **[Eigenaar](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md)** | ![vinkje](assets/Smock_Checkmark_18_N.svg) Gedefinieerd door gebruiker die de migratie uitvoert |
| **[Curation](/help/analyze/analysis-workspace/curate-share/curate.md)** | Nee |
| **[Delen](/help/analyze/analysis-workspace/curate-share/share-projects.md)** | Nee |
| **[Annotaties](/help/analyze/analysis-workspace/components/annotations/overview.md)** | Nee |
| **[Mapstructuur](/help/analyze/analysis-workspace/build-workspace-project/workspace-folders/about-folders.md)** | Nee |
| **[Beschrijvingen](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md)** | ![vinkje](assets/Smock_Checkmark_18_N.svg) |
| **[Tags](/help/analyze/landing.md)** | Nee |
| **[Favorieten](/help/analyze/landing.md)** | Nee |
| **[Planningen](/help/components/scheduled-projects-manager.md)** | Nee |
| **[Anomaliedetectie](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md)** | ![vinkje](assets/Smock_Checkmark_18_N.svg) |

{style="table-layout:auto"}

## Niet-ondersteunde elementen begrijpen die fouten veroorzaken

De volgende visualisaties en deelvensters worden niet ondersteund in Customer Journey Analytics. Wanneer deze elementen in een project vóór migratie zijn opgenomen, kunnen ze ervoor zorgen dat de migratie mislukt of dat er fouten optreden nadat het project is gemigreerd.

Verwijder deze elementen uit het Adobe Analytics-project voordat u het project naar de Customer Journey Analytics migreert. Als een migratie mislukt, verwijdert u deze elementen voordat u de migratie opnieuw probeert.

### Niet-ondersteunde visualisaties

* [Kaart](/help/analyze/analysis-workspace/visualizations/map-visualization.md)

### Niet-ondersteunde deelvensters

* [Analyses voor doel (A4T)](/help/analyze/analysis-workspace/c-panels/a4t-panel.md)

* [Segmentvergelijking](/help/analyze/analysis-workspace/c-panels/c-segment-comparison/segment-comparison.md)

* [Gemiddelde mediumgeluid](/help/analyze/analysis-workspace/c-panels/average-minute-audience-panel.md)

* [Volgende of vorige item](/help/analyze/analysis-workspace/c-panels/next-previous.md)

* [Overzicht van pagina](/help/analyze/analysis-workspace/c-panels/page-summary.md)

* [Contributieanalyse](/help/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.md)

## Besluit als organisatie hoe u componenten in kaart zult brengen

>[!IMPORTANT]
>
>Het migratieproces identificeert componenten in uw Adobe Analytics-project die niet automatisch aan componenten in Customer Journey Analytics kunnen worden toegewezen, en het staat u toe om hen manueel in kaart te brengen.
>
>**Om het even welke afbeeldingen die op één project worden gemaakt zijn op alle toekomstige projecten over uw volledige organisatie van toepassing, ongeacht welke gebruiker de migratie uitvoert. Deze toewijzingen kunnen alleen worden gewijzigd of ongedaan gemaakt door contact op te nemen met de klantenservice.**
>
>Daarom is het belangrijk dat uw organisatie bepaalt hoe dimensies en metriek worden toegewezen voordat projecten worden gemigreerd. Als u dit doet, voorkomt u dat afzonderlijke beheerders beslissingen nemen in een silo wanneer u slechts één project overweegt.
>
>Hier volgt een lijst met afmetingen en metriek die u handmatig moet toewijzen als deze in uw project bestaan. We raden u aan deze lijst vóór uw migratie te herzien. Als om het even welk van deze componenten in uw project bestaan, besluit nu welke componenten van de Customer Journey Analytics u hen aan in kaart zult brengen.


### Dimensionen die handmatig moeten worden toegewezen

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
