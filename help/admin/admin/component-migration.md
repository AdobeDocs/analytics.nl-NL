---
description: Verklaart hoe te om componenten en projecten van Adobe Analytics aan Customer Journey Analytics te migreren.
title: Componenten en projecten migreren van Adobe Analytics naar Customer Journey Analytics
feature: Admin Tools
hide: true
hidefromtoc: true
source-git-commit: 792b2171c5535fcd3920b5cbb100b2fb7c642db8
workflow-type: tm+mt
source-wordcount: '1784'
ht-degree: 1%

---

# Componenten en projecten migreren van Adobe Analytics naar Customer Journey Analytics

Adobe Analytics-beheerders kunnen Adobe Analytics-projecten en de bijbehorende onderdelen migreren naar Customer Journey Analytics.

Het migratieproces omvat:

* Adobe Analytics-projecten opnieuw maken in Customer Journey Analytics.

* De dimensies en metriek van de afbeelding van Adobe Analytics melden reeksen aan dimensies en metriek in de mening van de gegevens van de Customer Journey Analytics.

  Sommige dimensies en metriek worden automatisch toegewezen; andere moet u handmatig toewijzen als onderdeel van het migratieproces. Segmenten worden ook gemigreerd, maar hoeven niet in kaart te worden gebracht als onderdeel van het migratieproces.

  Alle gemigreerde componenten worden in het migratiesamenvatting weergegeven wanneer de migratie is voltooid.

## Een migratie voorbereiden

Voordat iemand in uw organisatie met het migreren van projecten begint, moet u de volgende secties voltooien.

### Vereisten

Voordat uw projecten en de bijbehorende componenten kunnen worden gemigreerd, moet u eerst het volgende doen:

* Gebruik de bronschakelaar van de Analyse om de gegevens van de het rapportreeks van Adobe Analytics in Customer Journey Analytics te bekijken. Om dat te doen, moet u:

   * [Rapportagesuites instellen voor opname in Adobe Experience Platform en Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/compare-aa-cja/cja-aa-comparison/aa-data-in-cja.html?lang=en#set-up-report-suites-for-ingestion-into-the-adobe-experience-platform-and-customer-journey-analytics)

   * [Gegevens opnemen en gebruiken](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/analytics.html)

* Zorg ervoor dat gebruikers in de Customer Journey Analytics zijn ingericht voor de gegevensweergaven waarin gegevens worden toegewezen.

  Zie voor meer informatie [De toestemmingen van de Customer Journey Analytics in de Admin Console](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-admin/cja-access-control.html?lang=en#customer-journey-analytics-permissions-in-admin-console) in [Toegangsbeheer Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-admin/cja-access-control.html).

  Het tabblad Machtigingen maakt deel uit van elk productprofiel in Admin Console. U kunt gebruikers toevoegen aan specifieke productprofielen. Vervolgens wijst u rechten toe aan specifieke gegevensweergaven en geeft u op welke machtigingen de gebruikers in een productprofiel hebben.

* Maak een migratieplan, zoals beschreven in de onderstaande sectie; [Een migratieplan maken als organisatie](#create-a-migration-plan-as-an-organization).

### Begrijpen wat er in een migratie is opgenomen

In de volgende tabellen wordt aangegeven welke elementen van een project en component zijn opgenomen in een migratie:

#### Componentelementen die worden gemigreerd

|  | Gegigreerd |
|---------|---------|
| **[Eigenaar](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-manager.md)** | ![vinkje](assets/Smock_Checkmark_18_N.svg) |
| **[Delen](/help/analyze/analysis-workspace/components/analysis-workspace-components.md)** | Nee |
| **[Beschrijvingen](/help/analyze/analysis-workspace/components/add-component-descriptions.md)** | ? |
| **[Tags](/help/analyze/analysis-workspace/components/analysis-workspace-components.md)** | Nee |
| **[Attributie (op afmetingen)](/help/analyze/analysis-workspace/attribution/overview.md)** | ? |

{style="table-layout:auto"}

#### Projectelementen die worden gemigreerd

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
| **[Delen (projectrollen)](/help/analyze/analysis-workspace/curate-share/share-projects.md)** | Nee |
| **[Delen (delen met een willekeurige koppeling)](/help/analyze/analysis-workspace/curate-share/share-projects.md)** | ? <!-- if no, combine with the above and just call it sharing? What about sharing links?--> |
| **[Annotaties](/help/analyze/analysis-workspace/components/annotations/overview.md)** | Nee |
| **[Mapstructuur](/help/analyze/analysis-workspace/build-workspace-project/workspace-folders/about-folders.md)** | Nee |
| **[Beschrijvingen](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md)** | ![vinkje](assets/Smock_Checkmark_18_N.svg) |
| **[Tags](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md)** | Nee |
| **[Planningen](/help/components/scheduled-projects-manager.md)** | Nee |
| **[Anomaliedetectie](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md)** | ? |
| **[Favorieten](/help/analyze/landing.md)** | ? |

{style="table-layout:auto"}

### Niet-ondersteunde elementen begrijpen die fouten veroorzaken

De volgende visualisaties, deelvensters en functies worden niet ondersteund in Customer Journey Analytics. Wanneer deze elementen in een project vóór migratie zijn opgenomen, kunnen ze ervoor zorgen dat de migratie mislukt of dat er fouten optreden nadat het project is gemigreerd.

Verwijder deze elementen uit het Adobe Analytics-project voordat u het project naar de Customer Journey Analytics migreert. Als een migratie mislukt, verwijdert u deze elementen voordat u de migratie opnieuw probeert.

#### Niet-ondersteunde visualisaties

* [Kaart](/help/analyze/analysis-workspace/visualizations/map-visualization.md)

#### Niet-ondersteunde deelvensters

* [Analyses voor doel (A4T)](/help/analyze/analysis-workspace/c-panels/a4t-panel.md)

* [Segmentvergelijking](/help/analyze/analysis-workspace/c-panels/c-segment-comparison/segment-comparison.md)

* [Gemiddelde mediumgeluid](/help/analyze/analysis-workspace/c-panels/average-minute-audience-panel.md)

* [Volgende of vorige item](/help/analyze/analysis-workspace/c-panels/next-previous.md)

* [Overzicht van pagina](/help/analyze/analysis-workspace/c-panels/page-summary.md)

#### Niet-ondersteunde functies

* [Contributieanalyse](/help/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.md)

* [Waarschuwingen](/help/components/c-alerts/intellligent-alerts.md)

### Een migratieplan maken als organisatie

Omdat om het even welke componenten die voor een bepaalde projectmigratie in kaart worden gebracht op om het even welke toekomstige projectmigraties voor de volledige organisatie van toepassing zijn, is het belangrijk dat uw organisatie alle projectmigraties vooraf plant.

Als organisatie moet u bepalen hoe dimensies en metriek worden toegewezen. Als u dit doet, voorkomt u dat afzonderlijke beheerders beslissingen nemen in een silo wanneer u slechts één project overweegt.

## Adobe Analytics-projecten migreren naar Customer Journey Analytics

>[!IMPORTANT]
>
>Voordat u projecten migreert naar Customer Journey Analytics, zoals wordt beschreven in deze sectie, moet u meer weten over migrerende projecten in het deelvenster [De migratie plannen](#plan-the-migration) hierboven.
>
>Alle dimensies of metriek die u toewijst, zijn permanent, zowel voor dit project als voor alle toekomstige projecten die door uw volledige organisatie worden gemigreerd. Toewijzingen die u maakt, kunnen niet worden gewijzigd nadat de migratie is voltooid.

1. Selecteer in Adobe Analytics de optie [!UICONTROL **Beheerder**] tab, dan selecteren [!UICONTROL **Alle beheerders**].

1. Onder [!UICONTROL **Gegevensconfiguratie en -verzameling**], selecteert u [!UICONTROL **Componentmigratie**].

1. Zoek het project dat u wilt migreren. U kunt de projectlijst filteren, sorteren of doorzoeken.

   Door gebrek, slechts worden de projecten die met u worden gedeeld getoond. Om alle projecten in uw organisatie te bekijken, selecteer **Filter** pictogram, vervolgens uitvouwen [!UICONTROL **Overige filters**] en selecteert u [!UICONTROL **Alles tonen**]. (Voor meer informatie over het filtreren, het sorteren, en het zoeken van de projectlijst, zie [De lijst met projecten filteren, sorteren en doorzoeken](#filter-sort-and-search-the-list-of-projects).)

1. Plaats de muis boven het project dat u wilt migreren en selecteer vervolgens de knop **Migreren** pictogram ![Project migreren](assets/migrate.svg).

   of

   Selecteer het project dat u wilt migreren en selecteer vervolgens [!UICONTROL **Migreren naar Customer Journey Analytics**].

   U kunt slechts één project tegelijk selecteren voor migratie.

   De [!UICONTROL **Project_name migreren naar Customer Journey Analytics**] wordt weergegeven.

   <!-- add screenshot -->

1. In de [!UICONTROL **Projecteigenaar**] veld, typt u de naam van de gebruiker die u als eigenaar van het project in de Customer Journey Analytics wilt instellen en selecteert u vervolgens de naam van de gebruiker in het keuzemenu.

   De eigenaar die u specificeert heeft volledige beheersrechten aan het project.

1. In de [!UICONTROL **Kaartschema voor rapportsuites**] , selecteert u een rapportsuite.

1. In de [!UICONTROL **Gegevens, weergave**] drop-down menu, selecteer de de gegevensmening van de Customer Journey Analytics waar u het project en de componenten wilt worden gemigreerd.

1. Selecteren [!UICONTROL **Toewijzingsschema**].

1. In de [!UICONTROL **Toewijzingsschema**] sectie, breid de [!UICONTROL **Dimensionen**] en [!UICONTROL **Metrisch**] secties.

   Sommige dimensies en metriek in Adobe Analytics worden automatisch toegewezen aan een dimensie of metrisch in Customer Journey Analytics. Andere moeten handmatig worden toegewezen.

   **Automatisch dimensies en metriek toewijzen**

   Sommige dimensies en metriek in Adobe Analytics worden automatisch toegewezen aan een dimensie of metrisch in Customer Journey Analytics. U kunt geen toewijzingsbeslissingen maken voor deze dimensies en metriek.

   Bijvoorbeeld de **Bezoeken** De metrische waarde in Adobe Analytics wordt automatisch toegewezen aan de **Sessies** metrisch in Customer Journey Analytics.

   U kunt om het even welke afmeting of metrisch selecteren om hun bijbehorende IDs te bekijken.

   <!-- update screenshot after I can see the Status column -->

   ![Projectmigratieschema](assets/project-migration-schema.png)

   **Afmetingen en metingen handmatig toewijzen**

   Sommige dimensies en metriek in Adobe Analytics kunnen niet automatisch worden toegewezen aan een dimensie of metrisch in Customer Journey Analytics.

   Wanneer een afmeting of metrisch niet automatisch in kaart kan worden gebracht, verschijnt een oranje teller naast [!UICONTROL **Dimensionen**] of [!UICONTROL **Metrisch**] sectiekoptekst, die het aantal afmetingen of metriek aangeeft dat handmatig moet worden toegewezen. In de tabel verschijnt een waarschuwingspictogram ![waarschuwingspictogram](assets/schema-warning.png) wordt weergegeven naast elke dimensie of metrische waarde die handmatig moet worden toegewezen.

   Bovendien [!UICONTROL **Status**] column: [!UICONTROL **Niet toegewezen**].

   <!-- update screenshot after I can see the Status column -->

   ![Handmatige toewijzing van het migratieschema](assets/schema-manual-map.png)

1. Als u de afmetingen en metriek handmatig wilt toewijzen, selecteert u een dimensie of metrische waarde die een waarschuwingspictogram bevat ![waarschuwingspictogram](assets/schema-warning.png)en vervolgens in de [!UICONTROL **Metrisch met toegewezen Customer Journey Analytics**] (of de [!UICONTROL **Dimensie toegewezen Customer Journey Analytics**] (als u een dimensie in kaart brengt), selecteer de afmeting of metrisch in Customer Journey Analytics die u aan de afmeting of metrisch wilt in kaart brengen u selecteerde.

   ![kaartafmetingen en maatstaven](assets/schema-manual-map-drop-down.png)

   Nadat een dimensie of metrisch in kaart is gebracht, verdwijnt het waarschuwingspictogram en [!UICONTROL **Status**] kolomwijzigingen in [!UICONTROL **Toegewezen**] met een groene stip. (Een status van [!UICONTROL **Toegewezen**] met een grijze stip geeft aan dat de dimensie of de metrische waarde is toegewezen tijdens een vorige migratie; eventuele vorige toewijzingen kunnen niet worden bijgewerkt.)

   Herhaal dit proces voor elke afmeting of metrisch die het waarschuwingspictogram bevat.

   Nadat alle dimensies en metriek in de het rapportreeks van Adobe Analytics aan een afmeting of metrisch in de mening van de gegevens van de Customer Journey Analytics in kaart worden gebracht, een groen vinkje ![vinkje](assets/report-suite-check.png) wordt weergegeven naast de naam van de rapportsuite in het dialoogvenster [!UICONTROL **Kaartschema voor rapportsuites**] sectie.

1. (Voorwaardelijk) als het project u migreert meer dan één rapportreeks bevat, selecteer een andere rapportreeks in het [!UICONTROL **Kaartschema voor rapportsuites**] en herhaal vervolgens stap 6 tot en met stap 10. <!-- double-check that the step numbers are still correct -->

1. Selecteren [!UICONTROL **Migreren**].

   >[!WARNING]
   >
   >   Er verschijnt een waarschuwingsbericht op het scherm nadat u [!UICONTROL **Migreren**]. Alvorens u verkiest om verder te gaan, begrijp dat om het even welke dimensies of metriek u in kaart brengt, zowel voor dit project als voor alle toekomstige projecten die door uw volledige organisatie worden gemigreerd. Als u doorgaat, kunnen de toewijzingen die u maakt, niet worden gewijzigd.

   Nadat een migratie is voltooid, worden de [!UICONTROL **Migratiestatus**] bevat een overzicht van wat er is gemigreerd.

   Als de migratie mislukt, raadpleegt u de [Een mislukte migratie opnieuw proberen](#retry-a-failed-migration) zie hieronder voor meer informatie .

## Een mislukte migratie opnieuw proberen

Als een migratie mislukt, kunt u de migratie opnieuw proberen.

U kunt een mislukte migratie op een van de volgende manieren opnieuw proberen:

>[!NOTE]
>
>Als de migratie na het opnieuw proberen blijft mislukken, neemt u contact op met de klantenservice met de project-id. U kunt projectidentiteitskaart op de de statuspagina van de Migratie vinden. <!-- when does this page display? How can they get there -->

1. Selecteer in Adobe Analytics de optie [!UICONTROL **Beheerder**] tab, dan selecteren [!UICONTROL **Alle beheerders**].

1. Onder [!UICONTROL **Gegevensconfiguratie en -verzameling**], selecteert u [!UICONTROL **Componentmigratie**].

1. Selecteren [!UICONTROL **Mislukt**] in de [!UICONTROL **Migratiestatus**] kolom naast het project dat u wilt opnieuw proberen.

   ![migratiestatus kolom mislukt](assets/migration-failed.png)

   De [!UICONTROL **Migratiestatus**] wordt weergegeven.

   Deze pagina wordt ook direct weergegeven nadat de in de sectie beschreven migratiestappen zijn voltooid [Adobe Analytics-projecten migreren naar Customer Journey Analytics](#migrate-adobe-analytics-projects-to-customer-journey-analytics) hierboven.

1. Selecteren [!UICONTROL **Migratie opnieuw proberen**].

## De lijst met projecten filteren, sorteren en doorzoeken

U kunt filteren, sorteren, en de lijst van projecten op de de migratiepagina van de Component zoeken.

### De lijst met projecten filteren

U kunt filteren op de volgende criteria:

| Filter | Beschrijving |
|---------|----------|
| [!UICONTROL **Status**] | De status van de migratie: <ul><li>[!UICONTROL **Niet gestart**]</li><li>[!UICONTROL **Gestart**]</li><li>[!UICONTROL **Voltooid**]</li><li>[!UICONTROL **Mislukt**]</li></ul>. |
| [!UICONTROL **Tags**] | Selecteer tags in de lijst met tags. Alleen projecten waarop de geselecteerde labels zijn toegepast, worden weergegeven. |
| [!UICONTROL **Rapportsuite**] | Selecteer om het even welke rapportreeks in de lijst van rapportreeksen. Slechts worden de projecten die de geselecteerde rapportreeksen gebruiken getoond. |
| [!UICONTROL **Eigenaars**] | Selecteer een eigenaar in de lijst met eigenaars. Alleen projecten die eigendom zijn van de gebruikers die u selecteert, worden weergegeven. |
| [!UICONTROL **Overige filters**] | De volgende aanvullende filters zijn beschikbaar: <ul><li>[!UICONTROL **Mijn**]: Hiermee worden alleen projecten weergegeven waarvoor u als eigenaar bent ingesteld.</li><li>[!UICONTROL **Gedeeld met mij**]: Hiermee geeft u alleen projecten weer die met u zijn gedeeld.</li><li>[!UICONTROL **Favorieten**]: Hiermee geeft u alleen projecten weer die als favoriet zijn gemarkeerd. (U kunt een project als favoriet van merken [bestemmingspagina van project](/help/analyze/landing.md).)</li><li>[!UICONTROL **Maandelijks**]</li><li>[!UICONTROL **Jaarlijks**]</li></ul> |

{style="table-layout:auto"}

### De lijst met projecten sorteren

U kunt de lijst met projecten op om het even welke kolom sorteren.

De lijst met projecten sorteren:

1. Selecteer de kolomkop van de kolom waarop u wilt sorteren.

1. (Optioneel) Selecteer nogmaals dezelfde kolomkop om de sorteervolgorde om te keren.

### Een project zoeken

U kunt de lijst van projecten op de de migratiepagina van de Component zoeken om het project te vinden dat u wilt migreren.

1. In het onderzoeksgebied bij de bovenkant van de de migratiepagina van de Component, begin de naam van het project te typen dat u wilt migreren.

1. Selecteer het project wanneer het in het drop-down menu verschijnt.

<!-- is there going to be a way to customize the columns that are displayed? -->
