---
description: De cloud-importaccount configureren en de locatie waar classificatiegegevens kunnen worden geüpload
keywords: Analysis Workspace
title: Locatiebeheer
feature: Classifications
exl-id: ace70568-220a-44e8-8e5f-f73002b9e2a2
source-git-commit: 7b293c962428c7b8fac62a9f70ce62a0fe8f0cea
workflow-type: tm+mt
source-wordcount: '607'
ht-degree: 0%

---

# Locatiebeheer

Met Locations Manager kunt u accounts en locaties weergeven, maken, bewerken of verwijderen. Deze kunnen voor elk van de volgende doeleinden worden gebruikt:

* Bestanden exporteren met [Gegevensfeeds](/help/export/analytics-data-feed/create-feed.md)
* Rapporten exporteren met [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)
* Schema&#39;s importeren met [Classificatiesets](/help/components/classifications/sets/overview.md)

## Locaties weergeven, filteren en zoeken

Met de locatiebeheer kunt u alle locaties weergeven die u hebt gemaakt. Systeembeheerders kunnen door alle gebruikers gemaakte locaties weergeven.

1. Als u Locations Manager wilt openen in Adobe Analytics, selecteert u **[!UICONTROL Components]** > **[!UICONTROL Locations]**.

1. (Voorwaardelijk) Als u een systeembeheerder bent, kunt u de [!UICONTROL **Locaties voor alle gebruikers weergeven**] om locaties weer te geven die door alle gebruikers in uw organisatie zijn gemaakt. <!-- Maybe add a screenshot? This is new functionality -->

1. Filter of zoek in de lijst met locaties:

   * **Filter:** Selecteer het pictogram Filter om de lijst met locaties te filteren.

     U kunt locaties filteren op **[!UICONTROL Location Type]**, **[!UICONTROL Account]**, of **[!UICONTROL Created By]**.

     ![Locatiefilters](assets/locations-filters.png)

   * **Zoeken:** Typ in het zoekveld de naam van de locatie die u wilt weergeven. De resultaten worden gefilterd terwijl u typt. De volgende kolommen worden doorzocht: **Locatienaam**, **Locatietype**, **Account**, en **Gemaakt door**.

1. (Optioneel) Als u meer dan 1000 locaties hebt, is alleen het eerste beeldscherm van 1000 pixels beschikbaar. Selecteren [!UICONTROL **Meer laden**] om 1.000 meer plaatsen te laden.

## Kolommen configureren in Locatiebeheer

De volgende kolommen zijn beschikbaar in Locations Manager. Als u de kolommen wilt aanpassen die in de tabel worden weergegeven, selecteert u de optie **Tabel aanpassen** pictogram ![Tabelpictogram aanpassen](assets/customize-table-icon.png).

* **[!UICONTROL Location name]**: De naam van de locatie. Selecteer het menu met drie punten naast een locatienaam om [de locatie bewerken](/help/components/locations/configure-import-locations.md) of verwijder het.
* **[!UICONTROL Location type]**: Het type account dat aan de locatie is gekoppeld.
* **[!UICONTROL Account]**: De specifieke account die aan de locatie is gekoppeld.
* **Toepassing**: Het type toepassing waarmee de locatie kan worden gebruikt (zoals Gegevensfeeds, Data Warehouse of Classificatiesets).
* **[!UICONTROL Last used]**: De datum waarop de locatie voor het laatst is gebruikt.
* **[!UICONTROL Created by]**: De gebruiker die de locatie heeft gemaakt.
* **[!UICONTROL Date created]**: De datum waarop de locatie is gemaakt.

## Locaties maken en beheren

U kunt locaties maken, bewerken en verwijderen.

### Een locatie maken

Voor informatie over het maken van een locatie raadpleegt u [Locaties voor het importeren en exporteren van cloud configureren](/help/components/locations/configure-import-locations.md).

<!-- Do I need to add some steps here about how to create a location and then assign that location to be used with DF, DW, or Classifications sets? Need to hear back from Ron and team whether we are including this functionality -->

### Een locatie bewerken

Zie voor informatie over het bewerken van een locatie [Locaties voor het importeren en exporteren van cloud configureren](/help/components/locations/configure-import-locations.md).

### Een locatie verwijderen

>[!IMPORTANT]
>
>Als een plaats wordt geschrapt, zullen om het even welke dossiers van de Invoer van Gegevens, rapporten van de Data Warehouse, of de schema&#39;s van de classificatiereeksen die met de geschrapte plaats worden geassocieerd de volgende tijd ontbreken zij worden gebruikt.
>
>Als u een locatie verwijdert, moet u [uw gegevensfeeds bewerken](/help/export/analytics-data-feed/create-feed.md), [Rapporten Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md), en [Schema&#39;s voor classificatiesets](/help/components/classifications/sets/manage/schema.md) om een functionerende locatie te gebruiken.

Een locatie verwijderen:

1. Selecteer het menu met drie punten in het dialoogvenster [!UICONTROL **Locatienaam**] kolom voor de locatie die u wilt verwijderen.

1. Selecteren [!UICONTROL **Verwijderen**].

## Accounts bewerken

1. Als u accounts wilt bewerken in Locations Manager in Adobe Analytics, selecteert u **[!UICONTROL Components]** > **[!UICONTROL Locations]** en selecteert u vervolgens de [!UICONTROL **Locatieaccounts**] tab.

1. (Voorwaardelijk) Als u een systeembeheerder bent, kunt u de [!UICONTROL **Accounts weergeven voor alle gebruikers**] om locaties weer te geven die door alle gebruikers in uw organisatie zijn gemaakt. <!-- Maybe add a screenshot? This is new functionality -->


1. Selecteren [!UICONTROL **Details weergeven**] op de account die u wilt bewerken.

1. Breng de gewenste wijzigingen aan en selecteer vervolgens [!UICONTROL **Opslaan**].

## Accountsleutels weergeven

Nadat u een account hebt gemaakt, kunt u de accountsleutels voor dat account bekijken. Mogelijk moet u deze informatie weergeven als u de account niet hebt geconfigureerd bij uw cloud provider wanneer u [oorspronkelijk geconfigureerd voor de account](/help/components/locations/configure-import-accounts.md).

Aan menings sleutels verbonden aan een de uitvoerrekening:

1. Selecteer in Adobe Analytics **[!UICONTROL Components]** > **[!UICONTROL Locations]** en selecteert u vervolgens de [!UICONTROL **Locatieaccounts**] tab.

1. Selecteer het pictogram met drie punten op de account die u wilt bewerken en selecteer vervolgens [!UICONTROL **Accountsleutels**].

## Accounts verwijderen

1. Selecteer in Adobe Analytics **[!UICONTROL Components]** > **[!UICONTROL Locations]** en selecteert u vervolgens de [!UICONTROL **Locatieaccounts**] tab.

1. Selecteer het pictogram met drie punten op de account die u wilt bewerken en selecteer vervolgens [!UICONTROL **Account verwijderen**]
