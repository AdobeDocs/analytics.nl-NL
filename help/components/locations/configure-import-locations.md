---
description: De cloud-importaccount configureren en de locatie waar classificatiegegevens kunnen worden geüpload
keywords: Analysis Workspace
title: Locaties voor het importeren en exporteren van cloud configureren
feature: Classifications
exl-id: 55179868-6228-44ff-835c-f4a7b38e929b
source-git-commit: 9b263b0b2d41533630f225d4d4dcc9b1e0c4f1df
workflow-type: tm+mt
source-wordcount: '1686'
ht-degree: 0%

---

# Locaties voor het importeren en exporteren van cloud configureren

<!-- This page is almost duplicated with the "Configure cloud export locations" article in CJA. Differences are that Snowflake isn't supported here and there is a Suffix field for each account type. -->

>[!NOTE]
>
>Houd rekening met het volgende wanneer u locaties maakt en bewerkt:<ul><li>De beheerders van het systeem kunnen gebruikers van het creëren van plaatsen beperken, zoals die in [ wordt beschreven vormen of de gebruikers plaatsen ](/help/components/locations/locations-manager.md#configure-whether-users-can-create-locations) kunnen tot stand brengen. Als u geen plaatsen kunt tot stand brengen zoals die in deze sectie wordt beschreven, contacteer uw systeembeheerder.</li><li>Een locatie kan alleen worden bewerkt door de gebruiker die de locatie heeft gemaakt of door een systeembeheerder.</li></ul>

Nadat u [ een wolkenrekening ](/help/components/locations/configure-import-accounts.md) vormt, kunt u een plaats op die rekening vormen. Eén locatie kan worden gebruikt voor elk van de volgende doeleinden (één locatie kan niet aan meerdere doelen worden gekoppeld):

* Het uitvoeren van dossiers gebruikend [ Diefstal van Gegevens ](/help/export/analytics-data-feed/create-feed.md)
* Het uitvoeren van rapporten gebruikend [ Data Warehouse ](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)
* Het invoeren van schema&#39;s gebruikend [ de reeksen van de Classificatie ](/help/components/classifications/sets/overview.md)

U moet Adobe Analytics configureren met de benodigde informatie voor toegang tot uw cloud-account. Dit proces bestaat uit het toevoegen van en het vormen van de rekening (zoals Amazon S3 Rol ARN, het Platform van de Wolk van Google, enzovoort) zoals die in [ wordt beschreven vormt wolkeninvoer en de uitvoerrekeningen ](/help/components/locations/configure-import-accounts.md), en dan het toevoegen van en het vormen van de plaats binnen die rekening (zoals die in dit artikel wordt beschreven).

Voor informatie over hoe te om bestaande plaatsen te bekijken en te schrappen, zie [ manager van Plaatsen ](/help/components/locations/locations-manager.md).

## Beginnen met het maken of bewerken van een locatie

1. In Adobe Analytics, uitgezochte [!UICONTROL **Componenten**] > [!UICONTROL **Plaatsen**].

1. Voor de [!UICONTROL Locations] pagina, selecteer de [!UICONTROL **Plaatsen**] tabel.

1. (Voorwaardelijk) als u een systeembeheerder bent, kunt u de [!UICONTROL **plaatsen van de Mening voor alle gebruikers**] optie toelaten om plaatsen te bekijken die door alle gebruikers in uw organisatie worden gecreeerd.
   ![ meningsplaatsen voor alle gebruikers ](assets/locations-all-users.png)

1. Om een nieuwe plaats toe te voegen, [!UICONTROL **voeg plaats**] toe. (Als u nog geen rekening hebt toegevoegd, voeg zoals die in [ wordt beschreven wolk toe invoert en de uitvoerrekeningen ](/help/components/locations/configure-import-accounts.md) uitvoert.)

   [!UICONTROL **voegt plaats**] dialoogvertoningen toe

   of

   Om een bestaande plaats uit te geven, selecteer het 3 punt menu naast de plaatsnaam, dan uitgezocht [!UICONTROL **geeft**] uit.

   De [!UICONTROL **details van de Plaats**] dialoogvertoningen.

1. Geef de volgende informatie op:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Naam**] | De naam van de locatie. |
   | [!UICONTROL **Beschrijving**] | Geef een korte beschrijving van de account om deze te onderscheiden van andere accounts van hetzelfde type account. |
   | [!UICONTROL **Gebruik met**] | Selecteer of u deze plaats met **,[!UICONTROL ** Data Warehouse **], of[!UICONTROL ** de reeksen van de Classificatie **]wilt gebruiken.** <p>Houd rekening met het volgende wanneer u een selectie maakt:</p><ul><li>Eén locatie kan niet voor meerdere doeleinden worden gebruikt. Een locatie die bijvoorbeeld wordt gebruikt voor gegevensfeeds, kan niet ook worden gebruikt voor Data Warehouse- of classificatiesets.</li><li>Om dossierconflicten binnen een plaats te vermijden, verander niet de waarde van het [!UICONTROL **Gebruik met**] gebied nadat de plaats is gebruikt.</li><li>Als u een plaats voor een E-mailrekening creeert, uitgezochte [!UICONTROL **Data Warehouse**] op dit gebied. E-maillocaties worden niet ondersteund met gegevensfeeds en classificatiesets.</li></ul> |
   | [!UICONTROL **plaats van het Merk beschikbaar aan alle gebruikers in uw organisatie**] | Schakel deze optie in als u wilt dat andere gebruikers in uw organisatie de locatie kunnen gebruiken.<p>Houd rekening met het volgende wanneer u locaties deelt:</p><ul><li>Locaties die u deelt, kunnen niet worden verwijderd.</li><li>Gedeelde locaties kunnen alleen door de eigenaar van de locatie worden bewerkt.</li><li>Locaties kunnen alleen worden gedeeld als de account waaraan de locatie is gekoppeld, ook wordt gedeeld.</li></ul> |
   | [!UICONTROL **de rekening van de Plaats**] | Selecteer de locatie waar u deze locatie wilt maken. Voor informatie over hoe te om een rekening tot stand te brengen, zie [ de invoer van de wolk en de uitvoerrekeningen ](/help/components/locations/configure-import-accounts.md) vormen. |

1. Om de vorm voor het vormen van de plaats te voltooien, ga met de sectie hieronder verder die aan het accounttype beantwoordt dat u op het [!UICONTROL **de rekeningen van de Plaats**] gebied selecteerde. (Aanvullende oudere accounttypen zijn ook beschikbaar, maar worden niet aanbevolen.)

### Amazon S3 Role ARN

Geef de volgende informatie op om een ARN-locatie voor Amazon S3 Role te configureren:

1. [ beginnen creërend of het uitgeven van een plaats ](#begin-creating-or-editing-a-location), zoals hierboven beschreven.

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Emmertje**] | Het emmertje in uw Amazon S3-account waarin u Adobe Analytics-gegevens wilt verzenden. <p>Zorg ervoor dat de Gebruiker ARN die door Adobe werd verstrekt de `S3:PutObject` toestemming heeft om dossiers aan dit emmertje te uploaden. </p><p>Emmernamen moeten voldoen aan specifieke naamgevingsregels. Ze moeten bijvoorbeeld tussen 3 en 63 tekens lang zijn, ze mogen alleen bestaan uit kleine letters, cijfers, puntjes (.) en afbreekstreepjes (-) en ze moeten beginnen en eindigen met een letter of getal. [ A volledige lijst van het noemen van regels is beschikbaar in de documentatie van AWS ](https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucketnamingrules.html). </p> |
   | [!UICONTROL **Prefix**] | De map in het emmertje waar u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Map_name/ |

   {style="table-layout:auto"}

1. Selecteer [!UICONTROL **sparen**].

   U kunt nu gegevens importeren of exporteren naar of van de account en locatie die u hebt geconfigureerd. Om gegevens uit te voeren, gebruik [&#128279;](/help/export/analytics-data-feed/create-feed.md) of [ Data Warehouse ](/help/export/data-warehouse/create-request/dw-request-report-destinations.md) van de Eigendommen van 0&rbrace; Gegevens.  Om gegevens in te voeren, gebruik [ de reeksen van de Classificatie ](/help/components/classifications/sets/overview.md).

   Geïmporteerde gegevens worden niet verwijderd uit de cloudbestemming nadat ze zijn geïmporteerd.

   >[!NOTE]
   >
   >   Als u eerder [ FTP gebruikte om classificaties ](/help/components/classifications/importer/c-uploading-saint-data-files-via-ftp.md) in Adobe Analytics in te voeren, moest u een FIN- dossier uploaden. Dit FIN-bestand is niet nodig bij het importeren van accounts in de cloud.


### Google Cloud Platform

Geef de volgende informatie op om een locatie voor een Google Cloud-platform te configureren:

1. [ beginnen creërend of het uitgeven van een plaats ](#begin-creating-or-editing-a-location), zoals hierboven beschreven.

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Emmertje**] | Het emmertje binnen uw GCP rekening waar u de gegevens van Adobe Analytics wilt worden verzonden. Zorg ervoor dat u aan Opdrachtgever toestemming hebt verleend die door Adobe wordt verstrekt om dossiers aan dit emmertje te uploaden. |
   | [!UICONTROL **Prefix**] | De map in het emmertje waar u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Map_name/ |

   {style="table-layout:auto"}

1. Selecteer [!UICONTROL **sparen**].

   U kunt nu gegevens importeren of exporteren naar of van de account en locatie die u hebt geconfigureerd. Om gegevens uit te voeren, gebruik [&#128279;](/help/export/analytics-data-feed/create-feed.md) of [ Data Warehouse ](/help/export/data-warehouse/create-request/dw-request-report-destinations.md) van de Eigendommen van 0&rbrace; Gegevens.  Om gegevens in te voeren, gebruik [ de reeksen van de Classificatie ](/help/components/classifications/sets/overview.md).

   Geïmporteerde gegevens worden niet verwijderd uit de cloudbestemming nadat ze zijn geïmporteerd.

   >[!NOTE]
   >
   >   Als u eerder [ FTP gebruikte om classificaties ](/help/components/classifications/importer/c-uploading-saint-data-files-via-ftp.md) in Adobe Analytics in te voeren, moest u een FIN- dossier uploaden. Dit FIN-bestand is niet nodig bij het importeren van accounts in de cloud.


### Azure SAS

Geef de volgende informatie op om een Azure SAS-locatie te configureren:

1. [ beginnen creërend of het uitgeven van een plaats ](#begin-creating-or-editing-a-location), zoals hierboven beschreven.

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Container**] | De container in de account die u hebt opgegeven, waarnaar u Adobe Analytics-gegevens wilt verzenden. |
   | [!UICONTROL **Prefix**] | De map in de container waarin u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Bijvoorbeeld: `folder_name/` |

   {style="table-layout:auto"}

1. Selecteer [!UICONTROL **sparen**].

   U kunt nu gegevens importeren of exporteren naar of van de account en locatie die u hebt geconfigureerd. Om gegevens uit te voeren, gebruik [&#128279;](/help/export/analytics-data-feed/create-feed.md) of [ Data Warehouse ](/help/export/data-warehouse/create-request/dw-request-report-destinations.md) van de Eigendommen van 0&rbrace; Gegevens.  Om gegevens in te voeren, gebruik [ de reeksen van de Classificatie ](/help/components/classifications/sets/overview.md).

   Geïmporteerde gegevens worden niet verwijderd uit de cloudbestemming nadat ze zijn geïmporteerd.

   >[!NOTE]
   >
   >   Als u eerder [ FTP gebruikte om classificaties ](/help/components/classifications/importer/c-uploading-saint-data-files-via-ftp.md) in Adobe Analytics in te voeren, moest u een FIN- dossier uploaden. Dit FIN-bestand is niet nodig bij het importeren van accounts in de cloud.


### Azure RBAC

Geef de volgende informatie op om een Azure RBAC-locatie te configureren:

1. [ beginnen creërend of het uitgeven van een plaats ](#begin-creating-or-editing-a-location), zoals hierboven beschreven.

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Rekening**] | De Azure-opslagaccount. |
   | [!UICONTROL **Container**] | De container in de account die u hebt opgegeven, waarnaar u Adobe Analytics-gegevens wilt verzenden. Zorg ervoor dat u machtigingen verleent om bestanden te uploaden naar de Azure-toepassing die u eerder hebt gemaakt. |
   | [!UICONTROL **Prefix**] | De map in de container waarin u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Bijvoorbeeld: `folder_name/` |

   {style="table-layout:auto"}

1. Selecteer [!UICONTROL **sparen**].

   U kunt nu gegevens importeren of exporteren naar of van de account en locatie die u hebt geconfigureerd. Om gegevens uit te voeren, gebruik [&#128279;](/help/export/analytics-data-feed/create-feed.md) of [ Data Warehouse ](/help/export/data-warehouse/create-request/dw-request-report-destinations.md) van de Eigendommen van 0&rbrace; Gegevens.  Om gegevens in te voeren, gebruik [ de reeksen van de Classificatie ](/help/components/classifications/sets/overview.md).

   Geïmporteerde gegevens worden niet verwijderd uit de cloudbestemming nadat ze zijn geïmporteerd.

   >[!NOTE]
   >
   >   Als u eerder [ FTP gebruikte om classificaties ](/help/components/classifications/importer/c-uploading-saint-data-files-via-ftp.md) in Adobe Analytics in te voeren, moest u een FIN- dossier uploaden. Dit FIN-bestand is niet nodig bij het importeren van accounts in de cloud.

### E-mail

Om een e-mailplaats te vormen, specificeer de volgende informatie:

1. [ beginnen creërend of het uitgeven van een plaats ](#begin-creating-or-editing-a-location), zoals hierboven beschreven.

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Onderwerp**] | Het onderwerp van het e-mailbericht. |
   | [!UICONTROL **Nota&#39;s**] | De inhoud van het e-mailbericht |

   {style="table-layout:auto"}

1. Selecteer [!UICONTROL **sparen**].

   U kunt gegevens naar de rekening en de plaats nu uitvoeren die u wanneer het gebruiken van [ de Eigen van Gegevens ](/help/export/analytics-data-feed/create-feed.md) vormde. (E-mailplaatsen worden niet gesteund met [ Data Warehouse ](/help/export/data-warehouse/create-request/dw-request-report-destinations.md) of [ de reeksen van de Classificatie ](/help/components/classifications/sets/overview.md)).

### Oudere accounttypen

Deze types van erfenisrekening zijn beschikbaar slechts wanneer het uitvoeren van gegevens met [ de Eigen van Gegevens ](/help/export/analytics-data-feed/create-feed.md) en [ Data Warehouse ](/help/export/data-warehouse/create-request/t-dw-create-request.md). Deze opties zijn niet beschikbaar wanneer het invoeren van gegevens met [ de reeksen van de Classificatie ](/help/components/classifications/sets/manage/schema.md).

+++FTP

Gegevens over gegevenstoevoer kunnen naar een door de Adobe of klant gehoste FTP-locatie worden verzonden. Geef de map op. Gebruik het veld Pad om feed-bestanden in een map te plaatsen.

| Veld | Functie |
|---------|----------|
| [!UICONTROL **de weg van de Folder**] | Voer het pad naar de map op de FTP-server in. Mappen moeten al bestaan; feeds genereren een fout als het opgegeven pad niet bestaat. </br> bijvoorbeeld, `/folder_name/folder_name`. |

{style="table-layout:auto"}

+++

+++SFTP

Gegevens over gegevenstoevoer kunnen worden geleverd aan een Adobe of door de klant gehoste SFTP-locatie. De bestemmingsplaats moet een geldige RSA of DSA openbare sleutel bevatten. U kunt de juiste openbare sleutel downloaden wanneer u de feed maakt.

| Veld | Functie |
|---------|----------|
| [!UICONTROL **de weg van de Folder**] | Voer het pad naar de map op de FTP-server in. Mappen moeten al bestaan; feeds genereren een fout als het opgegeven pad niet bestaat. </br> bijvoorbeeld, `/folder_name/folder_name`. |

{style="table-layout:auto"}

+++

+++S3

U kunt opslaggegevens rechtstreeks naar Amazon S3 emmers verzenden. Dit bestemmingstype vereist een naam van het Emmertje, een Zeer belangrijke identiteitskaart van de Toegang, en een Geheime Sleutel. Zie [ Amazon S3 emmer noemende vereisten ](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-s3-bucket-naming-requirements.html) binnen Amazon S3 docs voor meer informatie.

De gebruiker u voor het uploaden van gegevens van het gegevenspakhuis verstrekt moet de volgende [ toestemmingen ](https://docs.aws.amazon.com/AmazonS3/latest/API/API_Operations_Amazon_Simple_Storage_Service.html) hebben:

* s3:GetObject
* s3:PutObject
* s3:PutObjectAcl

De volgende 16 standaard AWS-gebieden worden ondersteund (waarbij zo nodig het juiste handtekeningalgoritme wordt gebruikt):

* us-East-2
* us-oost-1
* us-west-1
* us-west-2
* ap-zuid-1
* ap-northeast-2
* ap-zuidoost-1
* ap-zuidoost-2
* ap-northeast-1
* ca-centraal-1
* EU-centraal-1
* EU-west-1
* EU-west-2
* eu-west-3
* eu-noord-1
* sa-Oost-1

>[!NOTE]
>
>De regio cn-North-1 wordt niet ondersteund.

+++

+++Azure Blob

De steun van het pakhuis van gegevens Azure Blob bestemmingen. Hiervoor is een container, account en sleutel vereist. Amazon versleutelt de gegevens automatisch in rust. Wanneer u de gegevens downloadt, worden deze automatisch gedecodeerd. Zie [ een opslagrekening ](https://docs.microsoft.com/en-us/azure/storage/common/storage-quickstart-create-account?tabs=azure-portal#view-and-copy-storage-access-keys) binnen Microsoft Azure documenten voor meer informatie creëren.

>[!NOTE]
>
>U moet uw eigen proces uitvoeren om schijfruimte op de bestemming van het gegevenspakhuis te beheren. Adobe verwijdert geen gegevens van de server.

+++


