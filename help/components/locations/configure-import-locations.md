---
description: De cloud-importaccount configureren en de locatie waar classificatiegegevens kunnen worden geüpload
keywords: Analysis Workspace
title: Locaties voor het importeren en exporteren van cloud configureren
feature: Classifications
exl-id: 55179868-6228-44ff-835c-f4a7b38e929b
source-git-commit: 5bf6ed9b71a87d79fec960b6618667238019ac7f
workflow-type: tm+mt
source-wordcount: '1465'
ht-degree: 0%

---

# Locaties voor het importeren en exporteren van cloud configureren

<!-- This page is almost duplicated with the "Configure cloud export locations" article in CJA. Differences are that Snowflake isn't supported here and there is a Suffix field for each account type. -->

U kunt een cloudaccount (en een locatie op dat account) configureren. Eén locatie kan worden gebruikt voor elk van de volgende doeleinden (een enkele locatie kan niet worden gekoppeld aan meerdere doelen, zoals Gegevensfeeds en Data Warhouse, of Data Warehouse- en classificatiesets):

* Bestanden exporteren met [Gegevensfeeds](/help/export/analytics-data-feed/create-feed.md)
* Rapporten exporteren met [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)
* Schema&#39;s importeren met [Classificatiesets](/help/components/classifications/sets/overview.md)

U moet Adobe Analytics configureren met de benodigde informatie voor toegang tot uw cloud-account. Dit proces bestaat uit het toevoegen en configureren van de account (zoals Amazon S3 Role ARN, Google Cloud Platform enzovoort) zoals beschreven in [Cloud-import- en exportaccounts configureren](/help/components/locations/configure-import-accounts.md)en vervolgens de locatie binnen die account toevoegen en configureren (zoals beschreven in dit artikel).

## Beginnen met het maken of bewerken van een exportlocatie voor een cloud

1. Selecteer in Adobe Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Locaties**].
1. Op de [!UICONTROL Locations] pagina, selecteert u de [!UICONTROL **Locaties**] tab.
1. Als u een nieuwe locatie wilt maken, selecteert u [!UICONTROL **Locatie toevoegen**]. (Als u nog geen account hebt toegevoegd, voegt u een account toe zoals beschreven in [Cloud-import- en exportaccounts configureren](/help/components/locations/configure-import-accounts.md).)

   of

   Als u een bestaande locatie wilt bewerken, selecteert u het menu met drie punten in het dialoogvenster [!UICONTROL **Locatienaam**] kolom voor de locatie die u wilt bewerken, selecteert u [!UICONTROL **Bewerken**].
Het dialoogvenster Locatie wordt weergegeven.

1. Geef de volgende informatie op: |Veld | Functie | |—|—| | [!UICONTROL **Naam**] | De naam van de locatie.  | | [!UICONTROL **Beschrijving**] | Geef een korte beschrijving van de account om deze te onderscheiden van andere accounts van hetzelfde type account. | | [!UICONTROL **Gebruiken met**] | Selecteer of u deze locatie wilt gebruiken met [!UICONTROL **Gegevensfeeds**], [!UICONTROL **Data Warehouse**], of [!UICONTROL **Classificatiesets**]. <p>Houd rekening met het volgende wanneer u een selectie maakt:</p><ul><li>Eén locatie kan niet voor meerdere doeleinden worden gebruikt. Een locatie die bijvoorbeeld wordt gebruikt voor gegevensfeeds, kan niet ook worden gebruikt voor Data Warehouse- of classificatiesets.</li><li>Wijzig de waarde van de optie [!UICONTROL **Gebruiken met**] veld nadat de locatie is gebruikt.</li></ul> | | [!UICONTROL **Locatieaccount**] | Selecteer de locatie waar u deze locatie wilt maken. Voor informatie over het maken van een account raadpleegt u [Een account toevoegen](#add-an-account). |

1. In de [!UICONTROL **Locatie-eigenschappen**] in, geeft u specifieke informatie op over het accounttype van uw locatieaccount.

   Doorgaan met de sectie hieronder die overeenkomt met het accounttype dat u hebt geselecteerd in het dialoogvenster [!UICONTROL **Locatieaccounts**] veld. (Aanvullende oudere accounttypen zijn ook beschikbaar, maar worden niet aanbevolen.)



### Amazon S3 Role ARN

Geef de volgende informatie op om een ARN-locatie voor Amazon S3 Role te configureren:

1. [Beginnen met het maken of bewerken van een exportlocatie voor een cloud](#begin-creating-or-editing-a-cloud-export-location), zoals hierboven beschreven.

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Naam van emmertje**] | Het emmertje in uw Amazon S3-account waarin u Adobe Analytics-gegevens wilt verzenden. <p>Zorg ervoor dat de gebruiker-ARN die door de Adobe is geleverd, de `S3:PutObject` toestemming om bestanden naar dit emmertje te uploaden. </p><p>Emmernamen moeten voldoen aan specifieke naamgevingsregels. Ze moeten bijvoorbeeld tussen 3 en 63 tekens lang zijn, ze mogen alleen bestaan uit kleine letters, cijfers, puntjes (.) en afbreekstreepjes (-) en ze moeten beginnen en eindigen met een letter of getal. [Een volledige lijst met naamgevingsregels is beschikbaar in de documentatie van AWS](https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucketnamingrules.html). </p> |
   | [!UICONTROL **Voorvoegsel toets**] | De map in het emmertje waar u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Map_name/ |

   {style="table-layout:auto"}

1. Selecteren [!UICONTROL **Opslaan**].

   U kunt nu gegevens importeren of exporteren naar of van de account en locatie die u hebt geconfigureerd. Voor het exporteren van gegevens gebruikt u [Gegevensfeeds](/help/export/analytics-data-feed/create-feed.md) of [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md). Voor het importeren van gegevens gebruikt u [Classificatiesets](/help/components/classifications/sets/overview.md).

   Geïmporteerde gegevens worden niet verwijderd uit de cloudbestemming nadat ze zijn geïmporteerd.

   >[!NOTE]
   >
   >   Als u eerder [FTP voor het importeren van classificaties](/help/components/classifications/importer/c-uploading-saint-data-files-via-ftp.md) naar Adobe Analytics, moet u een FIN-bestand uploaden. Dit FIN-bestand is niet nodig bij het importeren van accounts in de cloud.


### Google Cloud Platform

Geef de volgende informatie op om een locatie voor een Google Cloud-platform te configureren:

1. [Beginnen met het maken of bewerken van een exportlocatie voor een cloud](#begin-creating-or-editing-a-cloud-export-location), zoals hierboven beschreven.

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Naam van emmertje**] | Het emmertje binnen uw GCP rekening waar u de gegevens van Adobe Analytics wilt worden verzonden. Zorg ervoor dat u aan Opdrachtgever toestemming hebt verleend die door Adobe wordt verstrekt om dossiers aan dit emmertje te uploaden. |
   | [!UICONTROL **Voorvoegsel toets**] | De map in het emmertje waar u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Map_name/ |

   {style="table-layout:auto"}

1. Selecteren [!UICONTROL **Opslaan**].

   U kunt nu gegevens importeren of exporteren naar of van de account en locatie die u hebt geconfigureerd. Voor het exporteren van gegevens gebruikt u [Gegevensfeeds](/help/export/analytics-data-feed/create-feed.md) of [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md). Voor het importeren van gegevens gebruikt u [Classificatiesets](/help/components/classifications/sets/overview.md).

   Geïmporteerde gegevens worden niet verwijderd uit de cloudbestemming nadat ze zijn geïmporteerd.

   >[!NOTE]
   >
   >   Als u eerder [FTP voor het importeren van classificaties](/help/components/classifications/importer/c-uploading-saint-data-files-via-ftp.md) naar Adobe Analytics, moet u een FIN-bestand uploaden. Dit FIN-bestand is niet nodig bij het importeren van accounts in de cloud.


### Azure SAS

Geef de volgende informatie op om een Azure SAS-locatie te configureren:

1. [Beginnen met het maken of bewerken van een exportlocatie voor een cloud](#begin-creating-or-editing-a-cloud-export-location), zoals hierboven beschreven.

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Containernaam**] | De container in de account die u hebt opgegeven, waarnaar u Adobe Analytics-gegevens wilt verzenden. |
   | [!UICONTROL **Voorvoegsel toets**] | De map in de container waarin u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Bijvoorbeeld: `folder_name/` |

   {style="table-layout:auto"}

1. Selecteren [!UICONTROL **Opslaan**].

   U kunt nu gegevens importeren of exporteren naar of van de account en locatie die u hebt geconfigureerd. Voor het exporteren van gegevens gebruikt u [Gegevensfeeds](/help/export/analytics-data-feed/create-feed.md) of [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md). Voor het importeren van gegevens gebruikt u [Classificatiesets](/help/components/classifications/sets/overview.md).

   Geïmporteerde gegevens worden niet verwijderd uit de cloudbestemming nadat ze zijn geïmporteerd.

   >[!NOTE]
   >
   >   Als u eerder [FTP voor het importeren van classificaties](/help/components/classifications/importer/c-uploading-saint-data-files-via-ftp.md) naar Adobe Analytics, moet u een FIN-bestand uploaden. Dit FIN-bestand is niet nodig bij het importeren van accounts in de cloud.


### Azure RBAC

Geef de volgende informatie op om een Azure RBAC-locatie te configureren:

1. [Beginnen met het maken of bewerken van een exportlocatie voor een cloud](#begin-creating-or-editing-a-cloud-export-location), zoals hierboven beschreven.

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Containernaam**] | De container in de account die u hebt opgegeven, waarnaar u Adobe Analytics-gegevens wilt verzenden. Zorg ervoor dat u machtigingen verleent om bestanden te uploaden naar de Azure-toepassing die u eerder hebt gemaakt. |
   | [!UICONTROL **Voorvoegsel toets**] | De map in de container waarin u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Bijvoorbeeld: `folder_name/` |
   | [!UICONTROL **Accountnaam**] | De Azure-opslagaccount. |

   {style="table-layout:auto"}

1. Selecteren [!UICONTROL **Opslaan**].

   U kunt nu gegevens importeren of exporteren naar of van de account en locatie die u hebt geconfigureerd. Voor het exporteren van gegevens gebruikt u [Gegevensfeeds](/help/export/analytics-data-feed/create-feed.md) of [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md). Voor het importeren van gegevens gebruikt u [Classificatiesets](/help/components/classifications/sets/overview.md).

   Geïmporteerde gegevens worden niet verwijderd uit de cloudbestemming nadat ze zijn geïmporteerd.

   >[!NOTE]
   >
   >   Als u eerder [FTP voor het importeren van classificaties](/help/components/classifications/importer/c-uploading-saint-data-files-via-ftp.md) naar Adobe Analytics, moet u een FIN-bestand uploaden. Dit FIN-bestand is niet nodig bij het importeren van accounts in de cloud.

### Oudere accounttypen

Deze oudere accounttypen zijn alleen beschikbaar wanneer u gegevens exporteert met [Gegevensfeeds](/help/export/analytics-data-feed/create-feed.md) en [Data Warehouse](/help/export/data-warehouse/create-request/t-dw-create-request.md). Deze opties zijn niet beschikbaar wanneer u gegevens importeert met [Classificatiesets](/help/components/classifications/sets/manage/schema.md).

+++FTP

Gegevens over gegevenstoevoer kunnen naar een door de Adobe of klant gehoste FTP-locatie worden verzonden. Geef de map op. Gebruik het veld Pad om feed-bestanden in een map te plaatsen.

| Veld | Functie |
|---------|----------|
| [!UICONTROL **Directorypad**] | Voer het pad naar de map op de FTP-server in. Mappen moeten al bestaan; feeds genereren een fout als het opgegeven pad niet bestaat. </br>Bijvoorbeeld: `/folder_name/folder_name`. |

{style="table-layout:auto"}

+++

+++SFTP

Gegevens over gegevenstoevoer kunnen worden geleverd aan een Adobe of door de klant gehoste SFTP-locatie. De bestemmingsplaats moet een geldige RSA of DSA openbare sleutel bevatten. U kunt de juiste openbare sleutel downloaden wanneer u de feed maakt.

| Veld | Functie |
|---------|----------|
| [!UICONTROL **Directorypad**] | Voer het pad naar de map op de FTP-server in. Mappen moeten al bestaan; feeds genereren een fout als het opgegeven pad niet bestaat. </br>Bijvoorbeeld: `/folder_name/folder_name`. |

{style="table-layout:auto"}

+++

+++S3

U kunt opslaggegevens rechtstreeks naar Amazon S3 emmers verzenden. Dit bestemmingstype vereist een naam van het Emmertje, een Zeer belangrijke identiteitskaart van de Toegang, en een Geheime Sleutel. Zie [Amazon S3-vereisten voor emmernaamgeving](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-s3-bucket-naming-requirements.html) in de Amazon S3-documenten voor meer informatie.

De gebruiker u voor het uploaden gegevens van het gegevenspakhuis verstrekt moet het volgende hebben: [machtigingen](https://docs.aws.amazon.com/AmazonS3/latest/API/API_Operations_Amazon_Simple_Storage_Service.html):

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

De steun van het pakhuis van gegevens Azure Blob bestemmingen. Hiervoor is een container, account en sleutel vereist. Amazon versleutelt de gegevens automatisch in rust. Wanneer u de gegevens downloadt, worden deze automatisch gedecodeerd. Zie [Een opslagaccount maken](https://docs.microsoft.com/en-us/azure/storage/common/storage-quickstart-create-account?tabs=azure-portal#view-and-copy-storage-access-keys) in de Microsoft Azure-documenten voor meer informatie.

>[!NOTE]
>
>U moet uw eigen proces uitvoeren om schijfruimte op de bestemming van het gegevenspakhuis te beheren. Adobe verwijdert geen gegevens van de server.

+++


