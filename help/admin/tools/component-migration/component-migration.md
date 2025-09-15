---
description: Verklaart hoe te om componenten en projecten van Adobe Analytics aan Customer Journey Analytics te migreren.
title: Componenten en projecten migreren van Adobe Analytics naar Customer Journey Analytics
feature: Admin Tools
exl-id: 49c7e47a-464b-4465-9b30-d77f886ca6dc
source-git-commit: ec4475cdd8f0c3e89f528bd60155caa1ca3f0645
workflow-type: tm+mt
source-wordcount: '1635'
ht-degree: 0%

---

# Componenten en projecten migreren van Adobe Analytics naar Customer Journey Analytics

Adobe Analytics-beheerders kunnen Adobe Analytics-projecten en de bijbehorende onderdelen migreren naar Customer Journey Analytics.

Het migratieproces omvat:

* Adobe Analytics-projecten opnieuw maken in Customer Journey Analytics.

* Mapping dimensies and metrics from Adobe Analytics report suites to afmetingen and metrics in Customer Journey Analytics data views.

  Sommige dimensies en metriek worden automatisch toegewezen; andere moet u handmatig toewijzen als onderdeel van het migratieproces. Segmenten worden ook gemigreerd, maar hoeven niet in kaart te worden gebracht als onderdeel van het migratieproces.

  Alle gemigreerde componenten worden in het migratiesamenvatting weergegeven wanneer de migratie is voltooid.

>[!NOTE]
>
>De informatie op deze pagina beschrijft hoe te om projecten en hun bijbehorende componenten met het gebruikersinterface te migreren.
>
>U kunt de migratie ook uitvoeren met de API&#39;s. Voor meer informatie, zie [ Adobe Analytics APIs ](https://adobedocs.github.io/analytics-2.0-apis/?urls.primaryName=Analytics%202.0%20APIs). Alle API-definities zijn beschikbaar in de vervolgkeuzelijst **[!UICONTROL Select a definition]** .


## Een migratie voorbereiden

Alvorens u om het even welke projecten aan Customer Journey Analytics migreert, leer meer over het migreren van projecten in [ voorbereidingen treffen om componenten en projecten van Adobe Analytics aan Customer Journey Analytics ](/help/admin/tools/component-migration/prepare-component-migration.md) te migreren.

Bovendien doe een [ inventaris van Adobe Analytics ](/help/admin/tools/analytics-inventory.md) gebruikend het hulpmiddel beschikbaar aan de beheerders van Analytics.

## Adobe Analytics-projecten migreren naar Customer Journey Analytics

>[!NOTE]
>
>Alvorens u om het even welke projecten aan Customer Journey Analytics zoals die in deze sectie worden beschreven migreert, leer meer over het migreren van projecten in [ voorbereidingen om componenten en projecten van Adobe Analytics aan Customer Journey Analytics ](/help/admin/tools/component-migration/prepare-component-migration.md) te migreren.
>
>**om het even welke afmetingen of metriek die u op dit project en op alle toekomstige projecten over uw volledige org toepast IMS, ongeacht welke gebruiker de migratie uitvoert. Deze toewijzingen kunnen worden bijgewerkt wanneer het migreren van toekomstige projecten.**

1. In Adobe Analytics, selecteer het [!UICONTROL **Admin**] lusje, dan selecteren [!UICONTROL **Alle admin**].

1. Onder [!UICONTROL **configuratie en inzameling van Gegevens**], uitgezochte [!UICONTROL **migratie van de Component**].

1. Zoek elk project dat u wilt migreren. U kunt de projectlijst filteren, sorteren of doorzoeken.

   Door gebrek, slechts worden de projecten die met u worden gedeeld getoond. Om alle projecten in uw organisatie te bekijken, selecteer het **pictogram van de Filter**, dan breid [!UICONTROL **Andere filters**] uit en selecteer [!UICONTROL **tonen allen**]. (Voor meer informatie over het filtreren, het sorteren, en het zoeken van de projectlijst, zie [ Filter, soort, en onderzoek de lijst van projecten ](#filter-sort-and-search-the-list-of-projects).)

1. (Voorwaardelijk) om veelvoudige projecten in één keer te migreren, selecteer checkbox links van elk project dat u wilt migreren, dan selecteren [!UICONTROL **migreren aan Customer Journey Analytics**].

   Overweeg het volgende wanneer het migreren van veelvoudige projecten:

   * U kunt maximaal 20 projecten selecteren om tegelijk te migreren.

   * De migratiestatus moet gelijk zijn voor alle projecten die u migreert.

     Als u bijvoorbeeld een project selecteert om te migreren met de migratiestatus **[!UICONTROL Not started]** , kunt u geen ander project met de migratiestatus **[!UICONTROL Failed]** selecteren.

   * U moet de zelfde projecteigenaar voor alle projecten aanwijzen u migreert.

   * De afmetingen en de metriek moeten aan de zelfde gegevensmening voor alle projecten worden in kaart gebracht u migreert.

   [!UICONTROL **Migreer project_name aan Customer Journey Analytics**] dialoogdoos wordt getoond.

   <!-- add screenshot -->

1. (Voorwaardelijk) om één enkel project, muis over het project te migreren dat u wilt migreren, dan selecteren **pictogram van de Migrate** ![ project ](assets/migrate.svg) migreren.

   [!UICONTROL **Migreer project_name aan Customer Journey Analytics**] dialoogdoos wordt getoond.

   <!-- add screenshot -->

1. Op het [!UICONTROL **bezit van het Project**] gebied, begin typend de naam van de gebruiker die u als eigenaar van de projecten wilt plaatsen die in Customer Journey Analytics worden gemigreerd, dan hun naam in het drop-down menu.

   De eigenaar die u opgeeft, heeft volledige beheerrechten voor de gemigreerde projecten. De eigenaar moet een beheerder zijn in Customer Journey Analytics. U kunt de eigendom van de projecten in een latere stap wijzigen.

1. In het [!UICONTROL **schema van de Kaart voor rapportreeksen**] sectie, selecteer een rapportreeks.

1. In het [!UICONTROL **drop-down menu van de mening van Gegevens**], selecteer de de gegevensmening van Customer Journey Analytics waar u de projecten en de componenten wilt worden gemigreerd.

   Wanneer u veelvoudige projecten migreert, worden alle projecten u migreert gecombineerd in de enige afbeelding van de gegevensmening.

1. Selecteer [!UICONTROL **schema van de Kaart**].

1. In het [!UICONTROL **schema van de Kaart**] sectie, breid de [!UICONTROL **Afmetingen**] en [!UICONTROL **Metriek**] secties uit.

   Sommige dimensies en metriek in Adobe Analytics worden automatisch toegewezen aan een dimensie of metrisch in Customer Journey Analytics. Andere moeten handmatig worden toegewezen.

   **kaart automatisch dimensies en metriek**

   >[!NOTE]
   >
   >   Als u WebSDK gebruikte om gegevens in Adobe Experience Platform in te voeren, kunnen de afmetingen en de metriek niet automatisch in kaart worden gebracht. Voor meer informatie, zie [ Eerste vereisten ](/help/admin/tools/component-migration/prepare-component-migration.md#prerequisites) in [ voorbereidingen treffen om componenten en projecten van Adobe Analytics aan Customer Journey Analytics ](/help/admin/tools/component-migration/prepare-component-migration.md) te migreren.

   Sommige dimensies en metriek in Adobe Analytics worden automatisch toegewezen aan een dimensie of metrisch in Customer Journey Analytics. U kunt geen toewijzingsbeslissingen maken voor deze dimensies en metriek.

   Bijvoorbeeld, **viseert** metrisch in Adobe Analytics wordt automatisch in kaart gebracht met **Sessies** metrisch in Customer Journey Analytics.

   U kunt om het even welke afmeting of metrisch selecteren om hun bijbehorende IDs te bekijken.

   <!-- update screenshot after I can see the Status column -->

   ![ schema van de migratie van het Project ](assets/project-migration-schema.png)

   **kaart manueel dimensies en metriek**

   Bepaalde afmetingen en maateenheden in Adobe Analytics kunnen niet automatisch worden toegewezen aan een dimensie of metrisch in Customer Journey Analytics.

   Wanneer een afmeting of metrisch niet automatisch in kaart kan worden gebracht, toont een oranje teller naast de [!UICONTROL **Afmetingen**] of [!UICONTROL **Metriek**] sectiekop, die op het aantal dimensies of metriek wijzen die manueel in kaart moeten worden gebracht. In de lijst, toont een waarschuwingspictogram ![ waarschuwingspictogram ](assets/schema-warning.png) naast elke afmeting of metrisch die manueel in kaart moet worden gebracht.

   Bovendien zegt de [!UICONTROL **kolom van de Status**] [!UICONTROL **niet in kaart gebracht**].

   <!-- update screenshot after I can see the Status column -->

   ![ het schemahandkaart van de Migratie ](assets/schema-manual-map.png)

1. Om dimensies en metriek manueel in kaart te brengen, selecteer een afmeting of metrisch die een waarschuwingspictogram ![ waarschuwingspictogram ](assets/schema-warning.png) bevat, dan in het [!UICONTROL **In kaart gebrachte metrische**] gebied van Customer Journey Analytics (of het [!UICONTROL **In kaart gebrachte de afmeting van Customer Journey Analytics**] gebied als u een afmeting in kaart brengt), selecteer de afmeting of metrisch in Customer Journey Analytics die u aan de afmeting wilt in kaart brengen.

   ![ kaartdimensies en metriek ](assets/schema-manual-map-drop-down.png)

   Nadat een afmeting of metrisch in kaart wordt gebracht, verdwijnt het waarschuwingspictogram en de [!UICONTROL **kolomveranderingen van de Status**] &lbrace;in kaart gebracht [!UICONTROL **&#x200B;**] met een groene punt. (Een status van [!UICONTROL **In kaart gebrachte**] met een grijze punt wijst erop dat de afmeting of metrisch tijdens een vorige migratie in kaart werd gebracht; om het even welke vorige afbeeldingen kunnen niet worden bijgewerkt.)

   Herhaal dit proces voor elke afmeting of metrisch die het waarschuwingspictogram bevat.

   Nadat alle dimensies en metriek in de het rapportreeks van Adobe Analytics aan een afmeting of metrisch in de het rapportreeks van Customer Journey Analytics in kaart worden gebracht, verschijnt een groen vinkje ![ naast de naam van de rapportreeks in het ](assets/report-suite-check.png) schema van de Kaart voor de sectie van de rapportsuites [!UICONTROL **.**]

1. (Voorwaardelijk) als de projecten u migreert meer dan één rapportreeks bevatten, selecteer een andere rapportreeks in het [!UICONTROL **schema van de Kaart voor rapportreeksen**] sectie, dan herhaal stap 6 door Stap 10. <!-- double-check that the step numbers are still correct -->

1. Selecteer [!UICONTROL **migreren**].

   >[!WARNING]
   >
   >Een het waarschuwingsbericht toont op scherm nadat u [!UICONTROL **selecteert Migreer**]. Alvorens u verkiest om verder te gaan, begrijp dat om het even welke afmetingen of metriek u op dit project en op alle toekomstige projecten over uw volledige IMS org van toepassing is, ongeacht welke gebruiker de migratie uitvoert. Deze toewijzingen kunnen worden bijgewerkt tijdens het migreren van toekomstige projecten.

   Nadat een migratie voltooit, verstrekt de [!UICONTROL **status van de Migratie**] pagina een samenvatting van wat werd gemigreerd.

   Als de migratie ontbreekt, zie [ opnieuw een ontbroken migratie ](#retry-a-failed-migration) sectie hieronder voor meer informatie.

1. (Optioneel) Nadat projecten zijn gemigreerd, kunt u de eigendom van de projecten overdragen aan elke gebruiker in Customer Journey Analytics. Voor meer informatie, zie [ activa van de Overdracht ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/tools/asset-transfer/transfer-assets) in de Gids van Customer Journey Analytics.

## Een mislukte migratie opnieuw proberen

Als een migratie mislukt, kunt u de migratie opnieuw proberen.

Alvorens een ontbroken migratie opnieuw te proberen, zorg ervoor u om het even welke [ niet gestaafde elementen ](/help/admin/tools/component-migration/prepare-component-migration.md#understand-unsupported-elements-that-cause-errors) uit het project verwijdert.

>[!NOTE]
>
>Als de migratie na het opnieuw proberen blijft mislukken, neemt u contact op met de klantenservice met de project-id. U kunt projectidentiteitskaart op de de statuspagina van de Migratie vinden. <!-- when does this page display? How can they get there -->

Een mislukte migratie opnieuw proberen:

1. In Adobe Analytics, selecteer het [!UICONTROL **Admin**] lusje, dan selecteren [!UICONTROL **Alle admin**].

1. Onder [!UICONTROL **configuratie en inzameling van Gegevens**], uitgezochte [!UICONTROL **migratie van de Component**].

1. Selecteer [!UICONTROL **Ontbroken**] in de [!UICONTROL **statuskolom van de Migratie**] naast het project dat u wilt opnieuw proberen.

   ![ ontbroken kolom van de migratiestatus ](assets/migration-failed.png)

   De [!UICONTROL **statusvertoningen van de Migratie**] pagina.

   Deze pagina toont ook onmiddellijk na de voltooiing van de migratiestappen die in de sectie [ worden beschreven de projecten van Adobe Analytics aan Customer Journey Analytics ](#migrate-adobe-analytics-projects-to-customer-journey-analytics) hierboven migreren.

1. Selecteer [!UICONTROL **opnieuw migratie**].

## De lijst met projecten filteren, sorteren en doorzoeken

U kunt filteren, sorteren, en de lijst van projecten op de de migratiepagina van de Component zoeken.

### De lijst met projecten filteren

U kunt filteren op de volgende criteria:

| Filter | Beschrijving |
|---------|----------|
| [!UICONTROL **Status**] | De status van de migratie: <ul><li>[!UICONTROL **niet begonnen**]</li><li>[!UICONTROL **Begonnen**]</li><li>[!UICONTROL **Voltooid**]</li><li>[!UICONTROL **Ontbroken**]</li></ul>. |
| [!UICONTROL **Markeringen**] | Selecteer tags in de lijst met tags. Alleen projecten waarop de geselecteerde labels zijn toegepast, worden weergegeven. |
| [!UICONTROL **Reeks van het Rapport**] | Selecteer om het even welke rapportreeks in de lijst van rapportreeksen. Slechts worden de projecten die de geselecteerde rapportreeksen gebruiken getoond. |
| [!UICONTROL **Eigenaars**] | Selecteer een eigenaar in de lijst met eigenaars. Alleen projecten die eigendom zijn van de gebruikers die u selecteert, worden weergegeven. |
| [!UICONTROL **Andere filters**] | De volgende aanvullende filters zijn beschikbaar: <ul><li>[!UICONTROL **Mine**]: Toont slechts projecten waar u als eigenaar wordt geplaatst.</li><li>[!UICONTROL **die met me**] wordt gedeeld: Toont slechts projecten die met u zijn gedeeld.</li><li>[!UICONTROL **Favorieten**]: Toont slechts projecten die als favoriet duidelijk zijn. (U kunt een project als favoriet van het [ project merken landend pagina ](/help/analyze/landing.md).)</li><li>[!UICONTROL **Maandelijks**]</li><li>[!UICONTROL **jaarlijks**]</li></ul> |

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
