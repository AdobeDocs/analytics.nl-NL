---
description: Stappen die beschrijven hoe te om een verzoek van de Data Warehouse tot stand te brengen.
title: Vorm een rapportbestemming voor een verzoek van de Data Warehouse
feature: Data Warehouse
source-git-commit: 5ed0c4b8cb4b1a50cf25df1459faecadcc19ea29
workflow-type: tm+mt
source-wordcount: '2081'
ht-degree: 0%

---

# Vorm een rapportbestemming voor een verzoek van de Data Warehouse

>[!AVAILABILITY]
>
>Sommige functies voor Data Warehouse die in dit artikel worden beschreven (en andere artikelen voor Data Warehouse in deze sectie) zijn alleen beschikbaar in de beperkte testfase van de release en zijn mogelijk nog niet beschikbaar in uw omgeving.
>
>Voor informatie over welke functies nog niet voor alle klanten beschikbaar zijn, en voor informatie over de releasetijdlijn van deze functies, raadpleegt u de [releaseopmerkingen](/help/release-notes/latest.md).
>
>Deze notitie wordt verwijderd wanneer de functionaliteit algemeen beschikbaar is. Voor informatie over het evaluatieproces Analytics raadpleegt u [Adobe Analytics-functiereleases](/help/release-notes/releases.md).

Er zijn diverse configuratieopties beschikbaar wanneer het creëren van een verzoek van de Data Warehouse. De volgende informatie beschrijft hoe te om een rapportbestemming voor het verzoek te vormen.

Voor informatie over hoe te beginnen creërend een verzoek, evenals verbindingen aan andere belangrijke configuratieopties, zie [Een Data Warehouse-aanvraag maken](/help/export/data-warehouse/create-request/t-dw-create-request.md).

>[!NOTE]
>
>Overweeg het volgende wanneer het vormen van een rapportbestemming:
>
>* We raden u aan een cloudaccount of e-mailbericht te gebruiken voor uw rapportbestemming. Oudere FTP- en SFTP-accounts zijn beschikbaar, maar worden niet aanbevolen.
>
>* Cloud-accounts zijn gekoppeld aan uw Adobe Analytics-gebruikersaccount. Andere gebruikers kunnen geen cloudaccounts gebruiken of weergeven die u configureert.
>
>* Alle cloudaccounts die u eerder hebt gemaakt [geconfigureerd voor gegevensfeeds](/help/export/analytics-data-feed/create-feed.md) zijn beschikbaar voor gebruik voor Data Warehouse.
>
>* Cloud-accounts die zijn geconfigureerd voor [Adobe Analytics-classificatiegegevens importeren](/help/components/locations/locations-manager.md) van een wolkenbestemming kan worden gebruikt wanneer het vormen van een rapportbestemming. Nochtans, kunnen om het even welke plaatsen die voor het invoeren van classificatiegegevens worden gevormd niet worden gebruikt.

Om de bestemming te vormen waar de rapporten van de Data Warehouse worden verzonden:

1. Begin met het maken van een aanvraag in Adobe Analytics door **[!UICONTROL Tools]** > **[!UICONTROL Data Warehouse]** > [!UICONTROL **Toevoegen**].

   Zie voor meer informatie [Een Data Warehouse-aanvraag maken](/help/export/data-warehouse/create-request/t-dw-create-request.md).

1. Selecteer op de aanvraagpagina Nieuwe Data Warehouse de optie [!UICONTROL **Doel van rapport**] tab.

   ![Tabblad Doel rapporteren](assets/dw-report-destination.png)

1. (Voorwaardelijk) als u eerder een rekening (en een bestemming op die rekening) vormde die u als uw rapportbestemming wilt gebruiken:

   1. Selecteer de account in het menu [!UICONTROL **Account selecteren**] vervolgkeuzelijst.

      Willekeurige wolkenaccounts waarvoor u hebt geconfigureerd [Adobe Analytics-classificatiegegevens importeren](/help/components/locations/locations-manager.md) vanuit een wolkenbestemming wordt hier weergegeven en kan worden gebruikt. Nochtans, kunnen om het even welke plaatsen die voor het invoeren van classificatiegegevens worden gevormd niet worden gebruikt. Voeg in plaats daarvan een nieuwe bestemming toe, zoals hieronder wordt beschreven.

   1. Selecteer in het menu van het menu [!UICONTROL **Doel selecteren**] vervolgkeuzelijst. <!-- Is this correct? -->

1. (Voorwaardelijk) Als u nog geen account hebt geconfigureerd:

   1. Selecteren [!UICONTROL **Account toevoegen**] en geeft u de volgende informatie op:

      | Veld | -functie |
      |---------|----------|
      | [!UICONTROL **Accounttype**] | Selecteer het type cloudaccount. We raden u aan voor elk accounttype één account te hebben, met meerdere locaties binnen dat account. <p>Nadat u een accounttype hebt gekozen, worden de velden weergegeven die specifiek zijn voor dat accounttype. </p> |
      | [!UICONTROL **Accountnaam**] | Geef een naam op voor de account. Deze naam wordt weergegeven wanneer u een locatie maakt. <!-- true? --> |
      | [!UICONTROL **Accountbeschrijving**] | Geef een korte beschrijving van de account om deze te onderscheiden van andere accounts van hetzelfde type account. |

      Vouw voor configuratieinstructies de sectie hieronder uit die overeenkomt met de [!UICONTROL **Accounttype**] die u hebt geselecteerd.

      Gebruik om het even welke volgende rekeningtypes wanneer het vormen van een rapportbestemming. Vouw voor configuratieinstructies het accounttype uit. (Extra [verouderde doelen](#legacy-destinations) zijn ook beschikbaar, maar worden niet aanbevolen.)

      +++Amazon S3

      Geef de volgende informatie op om een Amazon S3 Role ARN-account te configureren:

      | Veld | -functie |
      |---------|----------|
      | [!UICONTROL **Rol ARN**] | U moet een Rol ARN (de Naam van het Middel van Amazon) verstrekken die de Adobe kan gebruiken om toegang tot de rekening van Amazon S3 te krijgen. Om dit te doen, creeert u een IAM toestemmingsbeleid voor de bronrekening, maakt het beleid aan een gebruiker vast, en creeert dan een rol voor de bestemmingsrekening. Zie voor specifieke informatie [deze AWS-documentatie](https://aws.amazon.com/premiumsupport/knowledge-center/cross-account-access-iam/). |
      | [!UICONTROL **ARN gebruiker**] | De Gebruiker ARN (de Naam van het Middel van Amazon) wordt verstrekt door Adobe. U moet deze gebruiker aan het beleid vastmaken u creeerde. |

      {style="table-layout:auto"}

      +++

      +++Google Cloud Platform

      Geef de volgende informatie op om een Google Cloud Platform-account te configureren:

      | Veld | -functie |
      |---------|----------|
      | [!UICONTROL **Project-id**] | Uw Google Cloud-project-id. Zie de [Google Cloud-documentatie over het ophalen van een project-id](https://cloud.google.com/resource-manager/docs/creating-managing-projects#identifying_projects). |

      {style="table-layout:auto"}

      +++

      +++Azure SAS

      Geef de volgende informatie op om een Azure SAS-account te configureren:

      | Veld | -functie |
      |---------|----------|
      | [!UICONTROL **Toepassings-id**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Overzicht** in uw toepassing. Zie de klasse [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft Identity-platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
      | [!UICONTROL **Tenant-id**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Overzicht** in uw toepassing. Zie de klasse [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft Identity-platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
      | [!UICONTROL **URI sleutelvault**] | <p>Het pad naar het SAS-token in Azure Key Vault.  Om Azure SAS te configureren, moet u een SAS-token opslaan als een geheim met Azure Key Vault. Zie voor meer informatie de [Microsoft Azure-documentatie over het instellen en ophalen van een geheim bij Azure Key Vault](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations).</p><p>Nadat de sleutelvault-URI is gemaakt, voegt u een toegangsbeleid toe aan de Key Vault om toestemming te verlenen aan de Azure-toepassing die u hebt gemaakt. Zie voor meer informatie de [Microsoft Azure-documentatie over het toewijzen van een beleid voor toegang tot Key Vault](https://learn.microsoft.com/en-us/azure/key-vault/general/assign-access-policy?tabs=azure-portal).</p> |
      | [!UICONTROL **geheime naam sleutelvault**] | De geheime naam die u hebt gemaakt toen u het geheim toevoegde aan Azure Key Vault. In Microsoft Azure vindt u deze informatie in de Key Vault die u hebt gemaakt, op de **Key Vault** instellingenpagina&#39;s. Zie voor meer informatie de [Microsoft Azure-documentatie over het instellen en ophalen van een geheim bij Azure Key Vault](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations). |
      | [!UICONTROL **Geheim**] | Kopieer het geheim van de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Certificaten en geheimen** in uw toepassing. Zie de klasse [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft Identity-platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |

      {style="table-layout:auto"}

      +++

      +++Azure RBAC

      Geef de volgende informatie op om een Azure RBAC-account te configureren:

      | Veld | -functie |
      |---------|----------|
      | [!UICONTROL **Toepassings-id**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Overzicht** in uw toepassing. Zie de klasse [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft Identity-platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
      | [!UICONTROL **Tenant-id**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Overzicht** in uw toepassing. Zie de klasse [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft Identity-platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
      | [!UICONTROL **Geheim**] | Kopieer het geheim van de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Certificaten en geheimen** in uw toepassing. Zie de klasse [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft Identity-platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |

      {style="table-layout:auto"}

      +++

      +++E-mail

      Geef de volgende informatie op om een e-mailaccount te configureren:

      | Veld | -functie |
      |---------|----------|
      | [!UICONTROL **Ontvangers**] | E-mailmeldingen kunnen naar specifieke gebruikers worden verzonden wanneer het rapport wordt verzonden. Geef één e-mailadres of een lijst met e-mailadressen door komma&#39;s gescheiden op. <!-- How does this differ from the Notification email tab? --> |

   1. Selecteren [!UICONTROL **Locatie toevoegen**] en geeft u de volgende informatie op: |Veld | Functie | |—|—| | [!UICONTROL **Naam**] | De naam van de locatie.  | | [!UICONTROL **Beschrijving**] | Geef een korte beschrijving van de rekening om deze te kunnen onderscheiden van andere rekeningen van hetzelfde type. | | [!UICONTROL **Locatieaccount**] | Selecteer de locatie-account waarin u hebt gemaakt [Een account toevoegen](#add-an-account). |

   1. In de [!UICONTROL **Locatie-eigenschappen**] in, geeft u specifieke informatie op over het accounttype van uw locatieaccount.

      Vouw voor configuratieinstructies de sectie hieronder uit die overeenkomt met de [!UICONTROL **Accounttype**] die u eerder hebt geselecteerd.

      +++Amazon S3

      Geef de volgende informatie op om een Amazon S3-locatie te configureren:

      | Veld | -functie |
      |---------|----------|
      | [!UICONTROL **Naam van emmertje**] | Het emmertje in uw Amazon S3-account waarin u Adobe Analytics-gegevens wilt verzenden. Zorg ervoor dat de gebruiker-ARN die door de Adobe is geleverd, toegang heeft om bestanden naar dit emmertje te uploaden. |
      | [!UICONTROL **Voorvoegsel toets**] | De map in het emmertje waar u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Map_name/ |

      {style="table-layout:auto"}

      +++

      +++Google Cloud Platform

      Geef de volgende informatie op om een locatie voor een Google Cloud Platform te configureren:

      | Veld | -functie |
      |---------|----------|
      | [!UICONTROL **Naam van emmertje**] | Het emmertje binnen uw GCP rekening waar u de gegevens van Adobe Analytics wilt worden verzonden. Zorg ervoor dat u aan Opdrachtgever toestemming hebt verleend die door Adobe wordt verstrekt om dossiers aan dit emmertje te uploaden. Zie voor informatie over het verlenen van machtigingen [Voeg een hoofd aan een beleid op het niveau van de emmertje toe](https://cloud.google.com/storage/docs/access-control/using-iam-permissions#bucket-add) in de Google Cloud-documentatie. |
      | [!UICONTROL **Voorvoegsel toets**] | De map in het emmertje waar u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Map_name/ |

      {style="table-layout:auto"}

      +++

      +++Azure SAS

      Geef de volgende informatie op om een Azure SAS-locatie te configureren:

      | Veld | -functie |
      |---------|----------|
      | [!UICONTROL **Containernaam**] | De container in de account die u hebt opgegeven, waarnaar u Adobe Analytics-gegevens wilt verzenden. |
      | [!UICONTROL **Voorvoegsel toets**] | De map in de container waarin u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Bijvoorbeeld, `folder_name/` |

      {style="table-layout:auto"}

      +++

      +++Azure RBAC

      Geef de volgende informatie op om een Azure RBAC-locatie te configureren:

      | Veld | -functie |
      |---------|----------|
      | [!UICONTROL **Containernaam**] | De container in de account die u hebt opgegeven, waarnaar u Adobe Analytics-gegevens wilt verzenden. Zorg ervoor dat u machtigingen verleent om bestanden te uploaden naar de Azure-toepassing die u eerder hebt gemaakt. |
      | [!UICONTROL **Voorvoegsel toets**] | De map in de container waarin u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Bijvoorbeeld, `folder_name/` |
      | [!UICONTROL **Accountnaam**] | De Azure-opslagaccount. |

      {style="table-layout:auto"}

      +++

   1. Selecteren [!UICONTROL **Opslaan**].

      U kunt nu gegevens importeren naar de account en locatie die u hebt geconfigureerd.

1. Ga door met het configureren van uw verzoek voor Data Warehouse op de [!UICONTROL **Rapportopties**] tab. Zie voor meer informatie [Configureer rapportopties voor een Data Warehouse-verzoek](/help/export/data-warehouse/create-request/dw-request-report-options.md).

## Oudere bestemmingen

>[!IMPORTANT]
>
>De doelen die in deze sectie worden beschreven, zijn verouderd en worden niet aanbevolen. Gebruik in plaats daarvan een van de volgende doelen bij het maken van een gegevensopslagbestemming: Amazon S3, Google Cloud Platform, Azure RBAC, Azure SAS of Email. Zie de bovenstaande informatie voor meer informatie over elk van deze aanbevolen doelen.

De volgende informatie verstrekt configuratieinformatie voor elk van de erfenisbestemmingen:

### FTP

Gegevens van het gegevenspakhuis kunnen aan een Adobe of klant-ontvangen plaats van FTP worden geleverd. Vereist een FTP-host, gebruikersnaam en wachtwoord. Gebruik het padveld om feed-bestanden in een map te plaatsen. Mappen moeten al bestaan; feeds genereren een fout als het opgegeven pad niet bestaat.

Gebruik de volgende informatie wanneer u de beschikbare velden invult:

* [!UICONTROL **Host**]: Voer de gewenste FTP-doel-URL in. Bijvoorbeeld, `ftp://ftp.omniture.com`.
* [!UICONTROL **Pad**]: kan leeg worden gelaten
* [!UICONTROL **Gebruikersnaam**]: Voer de gebruikersnaam in die u wilt aanmelden bij de FTP-site.
* [!UICONTROL **Wachtwoord en wachtwoord bevestigen**]: Voer het wachtwoord in om u aan te melden bij de FTP-site.

### SFTP

SFTP-ondersteuning voor gegevenspakhuis is beschikbaar. Vereist een gastheer SFTP, gebruikersbenaming, en de bestemmingsplaats om een geldige RSA of DSA openbare sleutel te bevatten. U kunt de aangewezen openbare sleutel downloaden wanneer het creëren van de bestemming van het gegevenspakhuis.

### S3

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

### Azure Blob

De steun van het pakhuis van gegevens Azure Blob bestemmingen. Hiervoor is een container, account en sleutel vereist. Amazon versleutelt de gegevens automatisch in rust. Wanneer u de gegevens downloadt, worden deze automatisch gedecodeerd. Zie [Een opslagaccount maken](https://docs.microsoft.com/en-us/azure/storage/common/storage-quickstart-create-account?tabs=azure-portal#view-and-copy-storage-access-keys) in de Microsoft Azure-documenten voor meer informatie.

>[!NOTE]
>
>U moet uw eigen proces uitvoeren om schijfruimte op de bestemming van het gegevenspakhuis te beheren. Adobe verwijdert geen gegevens van de server.