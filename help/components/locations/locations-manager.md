---
description: De cloud-importaccount configureren en de locatie waar classificatiegegevens kunnen worden geüpload
keywords: Analysis Workspace
title: Locatiebeheer
feature: Classifications
exl-id: ace70568-220a-44e8-8e5f-f73002b9e2a2
source-git-commit: 5c02b46a7757e07a23505dc8e3dc21b6353aa9e2
workflow-type: tm+mt
source-wordcount: '1460'
ht-degree: 0%

---

# Locatiebeheer

Met Locations Manager kunt u accounts en locaties weergeven, maken, bewerken of verwijderen. Deze kunnen voor elk van de volgende doeleinden worden gebruikt:

* Het uitvoeren van dossiers gebruikend [ Diefstal van Gegevens ](/help/export/analytics-data-feed/create-feed.md)
* Het uitvoeren van rapporten gebruikend [ Data Warehouse ](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)
* Het uitvoeren van dossiers wanneer het gebruiken van [ Report Builder ](/help/analyze/report-builder/report-builder-export.md)
* Het invoeren van schema&#39;s gebruikend [ de reeksen van de Classificatie ](/help/components/classifications/sets/overview.md)

## Locaties weergeven, filteren en zoeken

De manager van de Plaats staat u toe om het even welke plaatsen te bekijken die u creeerde of om het even welke die met de organisatie worden gedeeld. Systeembeheerders kunnen locaties weergeven die door alle gebruikers zijn gemaakt, ongeacht of ze worden gedeeld.

1. Selecteer **[!UICONTROL Components]** > **[!UICONTROL Locations]** om Locations Manager te openen in Adobe Analytics.

1. (Voorwaardelijk) als u een systeembeheerder bent, kunt u de [!UICONTROL **plaatsen van de Mening voor alle gebruikers**] optie toelaten om plaatsen te bekijken die door alle gebruikers in uw organisatie worden gecreeerd. <!-- Maybe add a screenshot? This is new functionality -->

1. Filter of zoek in de lijst met locaties:

   * **Filter:** selecteer het pictogram van de Filter om de lijst van plaatsen te filtreren.

     U kunt locaties filteren op **[!UICONTROL Location Type]** , **[!UICONTROL Account]** of **[!UICONTROL Created By]** .

     ![ de filters van Plaatsen ](assets/locations-filters.png)

   * **Onderzoek:** op het onderzoeksgebied, begin typend de naam van de plaats u wilt bekijken. De resultaten worden gefilterd terwijl u typt. De volgende kolommen worden gezocht: **Naam van de Plaats**, **Type van Plaats**, **Rekening**, en **die door** wordt gecreeerd.

1. (Optioneel) Als u meer dan 1000 locaties hebt, is alleen het eerste beeldscherm van 1000 pixels beschikbaar. Selecteer [!UICONTROL **Lading meer**] om 1.000 meer plaatsen te laden.

## Kolommen configureren in Locatiebeheer

De volgende kolommen zijn beschikbaar in Locations Manager. Om de kolommen aan te passen die in de lijst worden getoond, selecteer **aanpassen lijst** pictogram ![ aanpassen lijstpictogram ](assets/customize-table-icon.png).

* **[!UICONTROL Location name]**: De naam van de locatie. Selecteer het 3 punt menu naast een plaatsnaam om of [ de plaats ](/help/components/locations/configure-import-locations.md) uit te geven of het te schrappen.
* **[!UICONTROL Location type]**: Het type account dat aan de locatie is gekoppeld.
* **[!UICONTROL Account]**: De specifieke account die aan de locatie is gekoppeld.
* **Toepassing**: Het type van toepassing dat de plaats kan worden gebruikt met (zoals de Diefenen van Gegevens, Data Warehouse, of de reeksen van de Classificatie).
* **[!UICONTROL Last used]**: De datum waarop de locatie voor het laatst is gebruikt.
* **[!UICONTROL Created by]**: De gebruiker die de locatie heeft gemaakt.
* **[!UICONTROL Date created]**: De datum waarop de locatie is gemaakt.

## Locaties maken en beheren

U kunt locaties maken, bewerken en verwijderen.

### Een locatie maken

Voor informatie over hoe te om een plaats tot stand te brengen, zie [ de invoer van de wolk en de uitvoerplaatsen ](/help/components/locations/configure-import-locations.md) vormen.

<!-- Do I need to add some steps here about how to create a location and then assign that location to be used with DF, DW, or Classifications sets? Need to hear back from Ron and team whether we are including this functionality -->

### Een locatie bewerken

Een locatie kan alleen worden bewerkt door de gebruiker die de locatie heeft gemaakt of door een systeembeheerder.

Voor informatie over hoe te om een plaats uit te geven, zie [ de invoer van de wolk en de uitvoerplaatsen ](/help/components/locations/configure-import-locations.md) vormen.

### Een locatie verwijderen

>[!IMPORTANT]
>
>Als een locatie wordt verwijderd, mislukken gegevensfeed-bestanden, Data Warehouse-rapporten of indelingssetschema&#39;s die aan de verwijderde locatie zijn gekoppeld de volgende keer dat ze worden gebruikt.
>
>Als u een plaats schrapt, zou u uw Diefen van Gegevens ](/help/export/analytics-data-feed/create-feed.md) moeten uitgeven, [ Data Warehouse rapporten ](/help/export/data-warehouse/create-request/dw-request-report-destinations.md), en [ de reeksen van de Classificatie schema&#39;s ](/help/components/classifications/sets/manage/schema.md) om een werkende plaats te gebruiken.[

Een locatie kan alleen worden verwijderd door de gebruiker die de locatie heeft gemaakt of door een systeembeheerder.

Een locatie verwijderen in Locations Manager in Adobe Analytics:

1. Selecteer **[!UICONTROL Components]** > **[!UICONTROL Locations]**, dan selecteren de [!UICONTROL **Plaatsen**] tabel.

1. Selecteer het 3 puntmenu in de [!UICONTROL **naam van de Plaats**] kolom voor de plaats die u wilt schrappen.

1. Selecteer [!UICONTROL **Schrapping**].

## Accounts maken en beheren

U kunt accounts maken, bewerken en verwijderen.

### Een account maken

Voor informatie over hoe te om een rekening tot stand te brengen, zie [ de invoer van de wolk en de uitvoerrekeningen ](/help/components/locations/configure-import-accounts.md) vormen.

### Een account bewerken

Een account kan alleen worden bewerkt door de gebruiker die het heeft gemaakt of door een systeembeheerder.

Voor informatie over hoe te om een rekening uit te geven, zie [ de invoer van de wolk en de uitvoerrekeningen ](/help/components/locations/configure-import-accounts.md) vormen.

### Accountsleutels weergeven

Nadat u een account hebt gemaakt, kunt u de accountsleutels voor dat account bekijken. U zou deze informatie kunnen moeten bekijken als u niet klaar was met het vormen van de rekening met uw wolkenleverancier toen u [ oorspronkelijk de rekening ](/help/components/locations/configure-import-accounts.md) vormde.

Aan menings sleutels verbonden aan een de uitvoerrekening:

1. In Adobe Analytics, selecteer **[!UICONTROL Components]** > **[!UICONTROL Locations]**, dan selecteren de [!UICONTROL **rekeningen van de Plaats**] tabel.

1. (Voorwaardelijk) als u een systeembeheerder bent, kunt u de [!UICONTROL **plaatsen van de Mening voor alle gebruikers**] optie toelaten om plaatsen te bekijken die door alle gebruikers in uw organisatie worden gecreeerd. <!-- Maybe add a screenshot? This is new functionality -->

1. Selecteer het pictogram met drie punten op de rekening die u wilt uitgeven, dan selecteren [!UICONTROL **sleutels van de Rekening**].

### Een account verwijderen

>[!IMPORTANT]
>
>Accounts kunnen alleen worden verwijderd als er geen locaties zijn die deze gebruiken. Alvorens u een rekening schrapt, moet u om het even welke plaatsen op de rekening eerst schrappen, zoals die in [ wordt beschreven een plaats ](#delete-a-location) schrappen.

Een account kan alleen worden verwijderd door de gebruiker die het heeft gemaakt of door een systeembeheerder.

Een account verwijderen:

1. In Adobe Analytics, selecteer **[!UICONTROL Components]** > **[!UICONTROL Locations]**, dan selecteren de [!UICONTROL **rekeningen van de Plaats**] tabel.

1. (Voorwaardelijk) als u een systeembeheerder bent, kunt u de [!UICONTROL **rekeningen van de Mening voor alle gebruikers**] optie toelaten om plaatsen te bekijken die door alle gebruikers in uw organisatie worden gecreeerd.

1. Selecteer het pictogram met drie punten op de rekening die u wilt uitgeven, dan selecteren [!UICONTROL **rekening van de Schrapping**]

## Bedrijfsbrede instellingen configureren (alleen beheerders)

Systeembeheerders kunnen gebruikers beperken bij het maken van accounts en locaties, of ze kunnen de typen accounts beperken die gebruikers kunnen maken en gebruiken.

![ Admin montages tabel ](assets/locations-admin-settings.png)

### Configureren of gebruikers accounts kunnen maken en bewerken

Door gebrek, kunnen alle gebruikers in de organisatie rekeningen tot stand brengen en rekeningen uitgeven die zij in uw milieu van Adobe Analytics creëren, zoals die in [ wordt beschreven vormt wolkinvoer en de uitvoerrekeningen ](/help/components/locations/configure-import-accounts.md).

U kunt voorkomen dat gebruikers accounts maken. Wanneer u dat doet, kunnen gebruikers nog steeds accounts gebruiken die ze al hebben gemaakt, maar ze kunnen ze niet meer bewerken. U kunt rekeningen schrappen die de gebruikers hebben gecreeerd, zoals die in [ wordt beschreven een rekening ](#delete-an-account) schrappen.

Alle gebruikers beperken in het maken en bewerken van accounts:

1. In Adobe Analytics, selecteer **[!UICONTROL Components]** > **[!UICONTROL Locations]**, dan selecteren de [!UICONTROL **montages Admin**] tabel.

1. In de [!UICONTROL **rekeningen van Plaatsen**] sectie, schrap de optie, [!UICONTROL **staat gebruikers toe om plaatsrekeningen**] tot stand te brengen en te beheren.

1. Selecteer [!UICONTROL **sparen**].

1. (Facultatief) Schrap om het even welke rekeningen die de gebruikers hebben gecreeerd die u hen niet meer wilt gebruiken, zoals die in [ wordt beschreven een rekening ](#delete-an-account) schrappen.

### Configureren of gebruikers locaties kunnen maken en bewerken

Door gebrek, kunnen alle gebruikers in de organisatie plaatsen tot stand brengen en plaatsen uitgeven zij in uw milieu van Adobe Analytics creëren, zoals die in [ wordt beschreven vormt wolkinvoer en uitvoerplaatsen ](/help/components/locations/configure-import-locations.md).

U kunt voorkomen dat gebruikers locaties maken. Wanneer u dat doet, kunnen gebruikers nog steeds alle locaties gebruiken die ze al hebben gemaakt, maar kunnen ze ze niet meer bewerken. U kunt plaatsen schrappen die de gebruikers hebben gecreeerd, zoals die in [ worden beschreven plaats van de Schrapping ](#delete-a-location).

Alle gebruikers beperken van het maken en bewerken van locaties:

1. In Adobe Analytics, selecteer **[!UICONTROL Components]** > **[!UICONTROL Locations]**, dan selecteren de [!UICONTROL **montages Admin**] tabel.

1. In de [!UICONTROL **sectie van Plaats**], schrap de optie, [!UICONTROL **staat gebruikers toe om plaatsen**] tot stand te brengen en te leiden.

1. Selecteer [!UICONTROL **sparen**].

1. (Facultatief) Schrap om het even welke plaatsen die de gebruikers hebben gecreeerd die u hen niet meer wilt gebruiken, zoals die in [ wordt beschreven Schrap een plaats ](#delete-a-location).

### Beperken welke accounttypen gebruikers kunnen maken en gebruiken

U kunt de accounttypen beperken die gebruikers zien in de volgende omstandigheden:

* Wanneer [ het creëren van nieuwe rekeningen ](/help/components/locations/configure-import-accounts.md).

* Wanneer het kiezen van welke rekeningen om te gebruiken wanneer het uitvoeren van dossiers die [ de Eigen van Gegevens ](/help/export/analytics-data-feed/create-feed.md) gebruiken, het uitvoeren van rapporten gebruikend [ Data Warehouse ](/help/export/data-warehouse/create-request/dw-request-report-destinations.md), of het invoeren van schema&#39;s gebruikend [ de reeksen van de Classificatie ](/help/components/classifications/sets/overview.md).

Wanneer u accounttypen beperkt zoals beschreven in deze sectie, zijn accounts van het type dat u beperkt, niet meer zichtbaar voor gebruikers. Dit betekent dat er geen nieuwe accounts van dat type kunnen worden gemaakt en dat bestaande accounts van dat type niet kunnen worden gebruikt bij het maken van gegevensfeeds, Data Warehouse of classificatiesets.

Nochtans, moeten de bestaande rekeningen die voor geplande uitvoer worden gevormd worden geschrapt als u hen wilt beperken worden gebruikt.

#### Zorg ervoor dat accounts niet worden gebruikt voor geplande exportbewerkingen

Wanneer u accounttypen beperkt, worden bestaande accounts verborgen en niet verwijderd.

Als de programma&#39;s reeds worden gevormd om gegevens naar een rekening te verzenden die van het type is dat u beperkt, zullen de programma&#39;s blijven lopen zelfs nadat u het accounttype beperkt, en de gegevens zullen blijven worden verzonden naar de rekening.  Als bijvoorbeeld een gegevensfeed is gepland voor het verzenden van gegevens naar een accounttype dat u beperkt, wordt het schema voortgezet.

Als u moet ervoor zorgen dat de rekeningen van een bepaald type niet in geplande uitvoer worden gebruikt, kunt u de rekeningen schrappen alvorens u [ de accounttypes ](#limit-the-account-types-that-are-available-to-users) beperkt.

Accounts verwijderen:

1. Zoek de accounts van het accounttype dat u wilt beperken. Deze worden gebruikt voor geplande exportbewerkingen.

1. Schrap de rekeningen, zoals die in [ worden beschreven Schrap een rekening ](#delete-an-account).

1. Ga met de volgende sectie verder, [ Beperk de rekeningstypes die aan gebruikers ](#limit-the-account-types-that-are-available-to-users) beschikbaar zijn.

#### De accounttypen beperken die beschikbaar zijn voor gebruikers

U kunt als volgt de accounttypen beperken die beschikbaar zijn voor gebruikers bij het maken en gebruiken van accounts:

1. In Adobe Analytics, selecteer **[!UICONTROL Components]** > **[!UICONTROL Locations]**, dan selecteren de [!UICONTROL **montages Admin**] tabel.

1. Bepaal de plaats van [!UICONTROL **Toegelaten accounttypes**] sectie.

   De volgende accounttypen zijn standaard beschikbaar voor gebruikers. Schakel een van deze accounttypen uit die u gebruikers wilt beperken.

   Er moet ten minste één accounttype zijn geselecteerd.

   * [!UICONTROL **Amazon S3 Rol ARN**]

   * [!UICONTROL **Google Cloud Platform**]

   * [!UICONTROL **Azure SAS**]

   * [!UICONTROL **Azure RBAC**]

   * [!UICONTROL **E-mail**]

   * Verouderde rekeningstypes, met inbegrip van [!UICONTROL **Amazon S3**], [!UICONTROL **Azure**], [!UICONTROL **FTP**], en [!UICONTROL **SFTP**]

1. Selecteer [!UICONTROL **sparen**].


