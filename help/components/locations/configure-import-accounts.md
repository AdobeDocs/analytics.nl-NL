---
description: De cloud-importaccount configureren en de locatie waar classificatiegegevens kunnen worden geüpload
keywords: Analysis Workspace
title: Cloud-import- en exportaccounts configureren
feature: Classifications
exl-id: 40d3d3f1-1047-4c37-8caf-6b0aabaa590a
source-git-commit: 66c846dd64ee3ed8f421c834ab82b53b1f0f00a5
workflow-type: tm+mt
source-wordcount: '1204'
ht-degree: 0%

---

# Cloud-import- en exportaccounts configureren

<!-- This page is almost duplicated with the "Configure cloud export locations" article in CJA. Differences are that Snowflake isn't supported here and there is a Suffix field for each account type. -->

U kunt een cloudaccount configureren die wordt gebruikt voor een of meer van de volgende doeleinden:

* Bestanden exporteren met [Gegevensfeeds](/help/export/analytics-data-feed/create-feed.md)
* Rapporten exporteren met [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)
* Schema&#39;s importeren met [Classificatiesets](/help/components/classifications/sets/overview.md)

U moet Adobe Analytics configureren met de benodigde informatie voor toegang tot uw cloud-account. Dit proces bestaat uit het toevoegen en configureren van de account (zoals Amazon S3 Role ARN, Google Cloud Platform enzovoort) zoals beschreven in dit artikel, en het toevoegen en configureren van de locatie binnen die account (zoals een map binnen de account) zoals beschreven in [Locaties voor het importeren en exporteren van cloud configureren](/help/components/locations/configure-import-locations.md).

Ga voor informatie over het beheren van bestaande accounts, zoals het weergeven, bewerken en verwijderen van accounts naar [Locatiebeheer](/help/components/locations/locations-manager.md).

Een cloudimport- of -exportaccount configureren:

1. Selecteer in Adobe Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Locaties**].
1. Op de [!UICONTROL Locations] pagina, selecteert u de [!UICONTROL **Locatieaccounts**] tab.
1. Selecteren [!UICONTROL **Account toevoegen**].

   Het dialoogvenster Account toevoegen wordt weergegeven.

1. Geef de volgende informatie op: |Veld | Functie | |—|—| | [!UICONTROL **Naam van locatieaccount**] | De naam van het locatieaccount. Deze naam wordt weergegeven wanneer u een locatie maakt | | [!UICONTROL **Beschrijving van locatieaccount**] | Geef een korte beschrijving van de account om deze te onderscheiden van andere accounts van hetzelfde type account. | | [!UICONTROL **Accounttype**] | Selecteer het type cloudaccount. We raden u aan voor elk accounttype één account te hebben, met meerdere locaties binnen dat account. |
1. In de [!UICONTROL **Accounteigenschappen**] in, geeft u specifieke informatie op over het accounttype dat u hebt geselecteerd.

   Vouw voor configuratieinstructies de sectie hieronder uit die overeenkomt met de [!UICONTROL **Accounttype**] die u hebt geselecteerd. (Aanvullende oudere accounttypen zijn ook beschikbaar, maar worden niet aanbevolen.)

   **Accounttypen**

   +++Amazon S3 Role ARN

   Geef de volgende informatie op om een Amazon S3 Role ARN-account te configureren:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Rol ARN**] | U moet een Rol ARN (de Naam van het Middel van Amazon) verstrekken die de Adobe kan gebruiken om toegang tot de rekening van Amazon S3 te krijgen. Om dit te doen, creeert u een IAM toestemmingsbeleid voor de bronrekening, maakt het beleid aan een gebruiker vast, en creeert dan een rol voor de bestemmingsrekening. Zie voor specifieke informatie [deze AWS-documentatie](https://aws.amazon.com/premiumsupport/knowledge-center/cross-account-access-iam/). |

   {style="table-layout:auto"}

+++

   +++Google Cloud Platform

   Geef de volgende informatie op om een Google Cloud Platform-account te configureren:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Project-id**] | Uw Google Cloud-project-id. Zie de [Google Cloud-documentatie over het ophalen van een project-id](https://cloud.google.com/resource-manager/docs/creating-managing-projects#identifying_projects). |

   {style="table-layout:auto"}

+++

   +++Azure SAS

   Geef de volgende informatie op om een Azure SAS-account te configureren:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Toepassings-id**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Overzicht** in uw toepassing. Zie de klasse [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft Identity-platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
   | [!UICONTROL **Tenant-id**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Overzicht** in uw toepassing. Zie de klasse [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft Identity-platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
   | [!UICONTROL **URI sleutelvault**] | <p>Het pad naar het SAS-token in Azure Key Vault.  Om Azure SAS te configureren, moet u een SAS-token opslaan als een geheim met Azure Key Vault. Zie voor meer informatie de [Microsoft Azure-documentatie over het instellen en ophalen van een geheim bij Azure Key Vault](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations).</p><p>Nadat de sleutelvault-URI is gemaakt, voegt u een toegangsbeleid toe op de Key Vault om toestemming te verlenen aan de Azure-toepassing die u hebt gemaakt. Zie voor meer informatie de [Microsoft Azure-documentatie over het toewijzen van een beleid voor toegang tot Key Vault](https://learn.microsoft.com/en-us/azure/key-vault/general/assign-access-policy?tabs=azure-portal).</p> |
   | [!UICONTROL **geheime naam sleutelvault**] | De geheime naam die u hebt gemaakt toen u het geheim toevoegde aan Azure Key Vault. In Microsoft Azure vindt u deze informatie in de Key Vault die u hebt gemaakt, op de **Key Vault** instellingenpagina. Zie voor meer informatie de [Microsoft Azure-documentatie over het instellen en ophalen van een geheim bij Azure Key Vault](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations). |
   | [!UICONTROL **Locatierekeninggeheim**] | Kopieer het geheim van de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Certificaten en geheimen** in uw toepassing. Zie de klasse [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft Identity-platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |

   {style="table-layout:auto"}

+++

   +++Azure RBAC

   Geef de volgende informatie op om een Azure RBAC-account te configureren:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Toepassings-id**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Overzicht** in uw toepassing. Zie de klasse [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft Identity-platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
   | [!UICONTROL **Tenant-id**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Overzicht** in uw toepassing. Zie de klasse [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft Identity-platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
   | [!UICONTROL **Locatierekeninggeheim**] | Kopieer het geheim van de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Certificaten en geheimen** in uw toepassing. Zie de klasse [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft Identity-platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |

   {style="table-layout:auto"}

+++

   **Oudere accounttypen**

   Deze oudere accounttypen zijn alleen beschikbaar wanneer u gegevens exporteert met [Gegevensfeeds](/help/export/analytics-data-feed/create-feed.md) en [Data Warehouse](/help/export/data-warehouse/create-request/t-dw-create-request.md). Deze opties zijn niet beschikbaar wanneer u gegevens importeert met [Classificatiesets](/help/components/classifications/sets/manage/schema.md).

   +++FTP

   Gegevens over gegevenstoevoer kunnen naar een door de Adobe of klant gehoste FTP-locatie worden verzonden. Vereist een FTP-host, gebruikersnaam en wachtwoord. Gebruik het padveld om feed-bestanden in een map te plaatsen. Mappen moeten al bestaan; feeds genereren een fout als het opgegeven pad niet bestaat.

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Host**] | Voer de gewenste FTP-doel-URL in. Bijvoorbeeld: `ftp://ftp.omniture.com`. |
   | [!UICONTROL **Pad**] | Kan leeg blijven. |
   | [!UICONTROL **Gebruikersnaam**] | Voer de gebruikersnaam in die u wilt aanmelden bij de FTP-site. |
   | [!UICONTROL **Wachtwoord en wachtwoord bevestigen**] | Voer het wachtwoord in om u aan te melden bij de FTP-site. |

   {style="table-layout:auto"}

+++

   +++SFTP

   SFTP-ondersteuning voor gegevensfeeds is beschikbaar. Vereist een gastheer SFTP, gebruikersbenaming, en de bestemmingsplaats om een geldige RSA of DSA openbare sleutel te bevatten. U kunt de juiste openbare sleutel downloaden wanneer u de feed maakt.

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

   Het pakhuis van gegevens steunt de bestemmingen van Azure Blob. Hiervoor is een container, account en sleutel vereist. Amazon versleutelt de gegevens automatisch in rust. Wanneer u de gegevens downloadt, worden deze automatisch gedecodeerd. Zie [Een opslagaccount maken](https://docs.microsoft.com/en-us/azure/storage/common/storage-quickstart-create-account?tabs=azure-portal#view-and-copy-storage-access-keys) in de Microsoft Azure-documenten voor meer informatie.

   >[!NOTE]
   >
   >U moet uw eigen proces uitvoeren om schijfruimte op de bestemming van het gegevenspakhuis te beheren. Adobe verwijdert geen gegevens van de server.

+++

1. Selecteren [!UICONTROL **Opslaan**].

1. Doorgaan met [Locaties voor het importeren en exporteren van cloud configureren](/help/components/locations/configure-import-locations.md).
