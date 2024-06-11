---
description: De cloud-importaccount configureren en de locatie waar classificatiegegevens kunnen worden geüpload
keywords: Analysis Workspace
title: Locatiebeheer
feature: Classifications
exl-id: ace70568-220a-44e8-8e5f-f73002b9e2a2
source-git-commit: 82c6d1e6d748a9b52b5988af5abb78d2c27ca077
workflow-type: tm+mt
source-wordcount: '1443'
ht-degree: 0%

---

# Locatiebeheer

Met Locations Manager kunt u accounts en locaties weergeven, maken, bewerken of verwijderen. Deze kunnen voor elk van de volgende doeleinden worden gebruikt:

* Bestanden exporteren met [Gegevensfeeds](/help/export/analytics-data-feed/create-feed.md)
* Rapporten exporteren met [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)
* Schema&#39;s importeren met [Classificatiesets](/help/components/classifications/sets/overview.md)

## Locaties weergeven, filteren en zoeken

De manager van de Plaats staat u toe om het even welke plaatsen te bekijken die u creeerde of om het even welke die met de organisatie worden gedeeld. Systeembeheerders kunnen locaties weergeven die door alle gebruikers zijn gemaakt, ongeacht of ze worden gedeeld.

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

Een locatie kan alleen worden bewerkt door de gebruiker die de locatie heeft gemaakt of door een systeembeheerder.

Zie voor informatie over het bewerken van een locatie [Locaties voor het importeren en exporteren van cloud configureren](/help/components/locations/configure-import-locations.md).

### Een locatie verwijderen

>[!IMPORTANT]
>
>Als een plaats wordt geschrapt, zullen om het even welke dossiers van de Invoer van Gegevens, rapporten van de Data Warehouse, of de schema&#39;s van de classificatiereeksen die met de geschrapte plaats worden geassocieerd de volgende tijd ontbreken zij worden gebruikt.
>
>Als u een locatie verwijdert, moet u [uw gegevensfeeds bewerken](/help/export/analytics-data-feed/create-feed.md), [Rapporten Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md), en [Schema&#39;s voor classificatiesets](/help/components/classifications/sets/manage/schema.md) om een functionerende locatie te gebruiken.

Een locatie kan alleen worden verwijderd door de gebruiker die de locatie heeft gemaakt of door een systeembeheerder.

Een locatie verwijderen in Locations Manager in Adobe Analytics:

1. Selecteren **[!UICONTROL Components]** > **[!UICONTROL Locations]** en selecteert u vervolgens de [!UICONTROL **Locaties**] tab.

1. Selecteer het menu met drie punten in het dialoogvenster [!UICONTROL **Locatienaam**] kolom voor de locatie die u wilt verwijderen.

1. Selecteren [!UICONTROL **Verwijderen**].

## Accounts maken en beheren

U kunt accounts maken, bewerken en verwijderen.

### Een account maken

Voor informatie over het maken van een account raadpleegt u [Cloud-import- en exportaccounts configureren](/help/components/locations/configure-import-accounts.md).

### Een account bewerken

Een account kan alleen worden bewerkt door de gebruiker die het heeft gemaakt of door een systeembeheerder.

Voor informatie over het bewerken van een account raadpleegt u [Cloud-import- en exportaccounts configureren](/help/components/locations/configure-import-accounts.md).

### Accountsleutels weergeven

Nadat u een account hebt gemaakt, kunt u de accountsleutels voor dat account bekijken. Mogelijk moet u deze informatie weergeven als u de account niet hebt geconfigureerd bij uw cloud provider wanneer u [oorspronkelijk geconfigureerd voor de account](/help/components/locations/configure-import-accounts.md).

Aan menings sleutels verbonden aan een de uitvoerrekening:

1. Selecteer in Adobe Analytics **[!UICONTROL Components]** > **[!UICONTROL Locations]** en selecteert u vervolgens de [!UICONTROL **Locatieaccounts**] tab.

1. (Voorwaardelijk) Als u een systeembeheerder bent, kunt u de [!UICONTROL **Locaties voor alle gebruikers weergeven**] om locaties weer te geven die door alle gebruikers in uw organisatie zijn gemaakt. <!-- Maybe add a screenshot? This is new functionality -->

1. Selecteer het pictogram met drie punten op de account die u wilt bewerken en selecteer vervolgens [!UICONTROL **Accountsleutels**].

### Een account verwijderen

>[!IMPORTANT]
>
>Accounts kunnen alleen worden verwijderd als er geen locaties zijn die deze gebruiken. Voordat u een account verwijdert, moet u eerst alle locaties op de account verwijderen, zoals beschreven in [Een locatie verwijderen](#delete-a-location).

Een account kan alleen worden verwijderd door de gebruiker die het heeft gemaakt of door een systeembeheerder.

Een account verwijderen:

1. Selecteer in Adobe Analytics **[!UICONTROL Components]** > **[!UICONTROL Locations]** en selecteert u vervolgens de [!UICONTROL **Locatieaccounts**] tab.

1. (Voorwaardelijk) Als u een systeembeheerder bent, kunt u de [!UICONTROL **Accounts weergeven voor alle gebruikers**] om locaties weer te geven die door alle gebruikers in uw organisatie zijn gemaakt.

1. Selecteer het pictogram met drie punten op de account die u wilt bewerken en selecteer vervolgens [!UICONTROL **Account verwijderen**]

## Bedrijfsbrede instellingen configureren (alleen beheerders)

{{release-limited-testing-section}}

Systeembeheerders kunnen gebruikers beperken bij het maken van accounts en locaties, of ze kunnen de typen accounts beperken die gebruikers kunnen maken en gebruiken.

### Configureren of gebruikers accounts kunnen maken en bewerken

Standaard kunnen alle gebruikers in de organisatie accounts maken en bewerken die ze in uw Adobe Analytics-omgeving maken, zoals wordt beschreven in [cloud-import- en -exportaccounts configureren](/help/components/locations/configure-import-accounts.md).

U kunt voorkomen dat gebruikers accounts maken. Wanneer u dat doet, kunnen gebruikers nog steeds accounts gebruiken die ze al hebben gemaakt, maar ze kunnen ze niet meer bewerken. U kunt accounts verwijderen die gebruikers hebben gemaakt, zoals wordt beschreven in [Een account verwijderen](#delete-an-account).

Alle gebruikers beperken in het maken en bewerken van accounts:

1. Selecteer in Adobe Analytics **[!UICONTROL Components]** > **[!UICONTROL Locations]** en selecteert u vervolgens de [!UICONTROL **Beheerinstellingen**] tab.

1. In de [!UICONTROL **Locatierekeningen**] de optie uit, [!UICONTROL **Gebruikers toestaan om locatierekeningen te maken en te beheren**].

1. Selecteren [!UICONTROL **Opslaan**].

1. (Optioneel) Verwijder alle accounts die gebruikers hebben gemaakt en die u niet langer wilt gebruiken, zoals beschreven in [Een account verwijderen](#delete-an-account).

### Configureren of gebruikers locaties kunnen maken en bewerken

Standaard kunnen alle gebruikers in de organisatie locaties maken en hun locaties bewerken in uw Adobe Analytics-omgeving, zoals wordt beschreven in [cloudimport- en exportlocaties configureren](/help/components/locations/configure-import-locations.md).

U kunt voorkomen dat gebruikers locaties maken. Wanneer u dat doet, kunnen gebruikers nog steeds alle locaties gebruiken die ze al hebben gemaakt, maar kunnen ze ze niet meer bewerken. U kunt locaties verwijderen die gebruikers hebben gemaakt, zoals wordt beschreven in [Locaties verwijderen](#delete-a-location).

Alle gebruikers beperken van het maken en bewerken van locaties:

1. Selecteer in Adobe Analytics **[!UICONTROL Components]** > **[!UICONTROL Locations]** en selecteert u vervolgens de [!UICONTROL **Beheerinstellingen**] tab.

1. In de [!UICONTROL **Locaties**] de optie uit, [!UICONTROL **Gebruikers toestaan locaties te maken en te beheren**].

1. Selecteren [!UICONTROL **Opslaan**].

1. (Optioneel) Verwijder alle locaties die gebruikers hebben gemaakt en die u niet langer wilt gebruiken, zoals beschreven in [Een locatie verwijderen](#delete-a-location).

### Beperken welke accounttypen gebruikers kunnen maken en gebruiken

U kunt de accounttypen beperken die gebruikers zien in de volgende omstandigheden:

* Wanneer [nieuwe accounts maken](/help/components/locations/configure-import-accounts.md).

* Wanneer u kiest welke accounts moeten worden gebruikt bij het exporteren van bestanden met [Gegevensfeeds](/help/export/analytics-data-feed/create-feed.md), rapporten exporteren met [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)of schema&#39;s importeren met [Classificatiesets](/help/components/classifications/sets/overview.md).

Wanneer u accounttypen beperkt zoals beschreven in deze sectie, zijn accounts van het type dat u beperkt, niet meer zichtbaar voor gebruikers. Dit betekent dat er geen nieuwe accounts van dat type kunnen worden gemaakt en dat bestaande accounts van dat type niet kunnen worden gebruikt bij het maken van gegevensfeeds, Data Warehouse of classificatiesets.

Nochtans, moeten de bestaande rekeningen die voor geplande uitvoer worden gevormd worden geschrapt als u hen wilt beperken worden gebruikt.

#### Zorg ervoor dat accounts niet worden gebruikt voor geplande exportbewerkingen

Wanneer u accounttypen beperkt, worden bestaande accounts verborgen en niet verwijderd.

Als de programma&#39;s reeds worden gevormd om gegevens naar een rekening te verzenden die van het type is dat u beperkt, zullen de programma&#39;s blijven lopen zelfs nadat u het accounttype beperkt, en de gegevens zullen blijven worden verzonden naar de rekening.  Als bijvoorbeeld een gegevensfeed is gepland voor het verzenden van gegevens naar een accounttype dat u beperkt, wordt het schema voortgezet.

Als u ervoor moet zorgen dat accounts van een bepaald type niet worden gebruikt in geplande exportbewerkingen, kunt u de accounts verwijderen voordat u [accounttypen beperken](#limit-the-account-types-that-are-available-to-users).

Accounts verwijderen:

1. Zoek de accounts van het accounttype dat u wilt beperken. Deze worden gebruikt voor geplande exportbewerkingen.

1. De accounts verwijderen zoals wordt beschreven in [Een account verwijderen](#delete-an-account).

1. Ga verder met de volgende sectie: [De accounttypen beperken die beschikbaar zijn voor gebruikers](#limit-the-account-types-that-are-available-to-users).

#### De accounttypen beperken die beschikbaar zijn voor gebruikers

U kunt als volgt de accounttypen beperken die beschikbaar zijn voor gebruikers bij het maken en gebruiken van accounts:

1. Selecteer in Adobe Analytics **[!UICONTROL Components]** > **[!UICONTROL Locations]** en selecteert u vervolgens de [!UICONTROL **Beheerinstellingen**] tab.

1. Zoek de [!UICONTROL **Toegestane accounttypen**] sectie.

   De volgende accounttypen zijn standaard beschikbaar voor gebruikers. Schakel een van deze accounttypen uit die u gebruikers wilt beperken.

   * [!UICONTROL **Amazon S3 Role ARN**]

   * [!UICONTROL **Google Cloud Platform**]

   * [!UICONTROL **Azure SAS**]

   * [!UICONTROL **Azure RBAC**]

   * [!UICONTROL **E-mail**]

   * Oudere accounttypen, waaronder [!UICONTROL **Amazon S3**], [!UICONTROL **Azure**], [!UICONTROL **FTP**], en [!UICONTROL **SFTP**]

1. Selecteren [!UICONTROL **Opslaan**].


