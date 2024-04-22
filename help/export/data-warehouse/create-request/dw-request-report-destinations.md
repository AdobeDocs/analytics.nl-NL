---
description: Stappen die beschrijven hoe te om een verzoek van de Data Warehouse tot stand te brengen.
title: Vorm een rapportbestemming voor een verzoek van de Data Warehouse
feature: Data Warehouse
exl-id: 3c7faea3-4d90-4274-88f3-e9337c94155f
source-git-commit: 40c64e104dbc3ba97807ef9fee653252d2fdd55e
workflow-type: tm+mt
source-wordcount: '2581'
ht-degree: 0%

---

# Vorm een rapportbestemming voor een verzoek van de Data Warehouse

Er zijn diverse configuratieopties beschikbaar wanneer het creëren van een verzoek van de Data Warehouse. De volgende informatie beschrijft hoe te om een rapportbestemming voor het verzoek te vormen.

Voor informatie over hoe te beginnen creërend een verzoek, evenals verbindingen aan andere belangrijke configuratieopties, zie [Een Data Warehouse-aanvraag maken](/help/export/data-warehouse/create-request/t-dw-create-request.md).

>[!NOTE]
>
>Overweeg het volgende wanneer het vormen van een rapportbestemming:
>
>* We raden u aan een cloudaccount of e-mailbericht te gebruiken voor uw rapportbestemming. [Oudere FTP- en SFTP-accounts](#legacy-destinations) zijn beschikbaar, maar worden niet aanbevolen.
>
>* Alle cloudaccounts die u eerder hebt geconfigureerd, kunnen voor Data Warehouse worden gebruikt. U kunt cloudaccounts op de volgende manieren configureren:
>
>   * Bij configureren [Gegevensfeeds](/help/export/analytics-data-feed/create-feed.md)
>   
>   * Wanneer [Adobe Analytics-classificatiegegevens importeren](/help/components/locations/locations-manager.md) (Accounts kunnen worden gebruikt, maar elke locatie die op die accounts is geconfigureerd, kan niet worden gebruikt.)
>   
>   * Vanuit het Locatiebeheer, in [Componenten > Locaties](/help/components/locations/configure-import-accounts.md).
>
>* Cloud-accounts zijn gekoppeld aan uw Adobe Analytics-gebruikersaccount. Andere gebruikers kunnen geen cloudaccounts gebruiken of weergeven die u configureert.
>
>* U kunt alle locaties bewerken die u maakt met Locatiebeheer in [Componenten > Locaties](/help/components/locations/configure-import-accounts.md)

Om de bestemming te vormen waar de rapporten van de Data Warehouse worden verzonden:

1. Als je nog geen aanvraag hebt ingediend, kun je een aanvraag maken in Adobe Analytics door **[!UICONTROL Tools]** > **[!UICONTROL Data Warehouse]** > [!UICONTROL **Toevoegen**].

   Zie voor meer informatie [Een Data Warehouse-aanvraag maken](/help/export/data-warehouse/create-request/t-dw-create-request.md).

1. Selecteer op de aanvraagpagina Nieuwe Data Warehouse de optie [!UICONTROL **Doel van rapport**] tab.

   ![Tabblad Doel rapporteren](assets/dw-report-destination.png)

1. (Voorwaardelijk) als een cloudaccount (en een bestemming voor die account) al in Adobe Analytics is geconfigureerd, kunt u dit als uw rapportbestemming gebruiken:

   >[!NOTE]
   >
   >De rekeningen zijn beschikbaar aan u slechts als u hen vormde of als zij met een organisatie werden gedeeld u een deel van bent.
   >
   >Als u systeembeheerder bent, [!UICONTROL **Alle doelen tonen**] is beschikbaar. Schakel deze optie in als u toegang wilt hebben tot alle accounts en locaties die door een gebruiker in de organisatie zijn gemaakt.

   1. Selecteer de account in het menu [!UICONTROL **Account selecteren**] vervolgkeuzelijst.

      Alle cloudaccounts die u hebt geconfigureerd in een van de volgende Adobe Analytics-domeinen kunnen worden gebruikt:

      * Bij het importeren van Adobe Analytics-classificatiegegevens, zoals beschreven in [Schema](/help/components/classifications/sets/manage/schema.md).

        Nochtans, kunnen om het even welke plaatsen die voor het invoeren van classificatiegegevens worden gevormd niet worden gebruikt. Voeg in plaats daarvan een nieuwe bestemming toe, zoals hieronder wordt beschreven.

      * Bij het configureren van accounts en locaties in het gebied Locaties, zoals wordt beschreven in [Cloud-import- en exportaccounts configureren](/help/components/locations/configure-import-accounts.md) en [Locaties voor het importeren en exporteren van cloud configureren](/help/components/locations/configure-import-locations.md).

   1. Selecteer in het menu van het menu [!UICONTROL **Doel selecteren**] vervolgkeuzelijst. <!-- Is this correct? -->

1. (Voorwaardelijk) Als u geen toegang hebt tot een cloudaccount die al in Adobe Analytics is geconfigureerd, kunt u een account configureren:

   1. Selecteren [!UICONTROL **Account toevoegen**] en geeft u de volgende informatie op:

      | Veld | Functie |
      |---------|----------|
      | [!UICONTROL **Accounttype**] | Selecteer het type cloudaccount. We raden u aan voor elk accounttype één account te hebben, met meerdere locaties binnen dat account. <p>Nadat u een accounttype hebt gekozen, worden de velden weergegeven die specifiek zijn voor dat accounttype. </p> |
      | [!UICONTROL **Accountnaam**] | Geef een naam op voor de account. Deze naam wordt weergegeven wanneer u een locatie maakt. <!-- true? --> |
      | [!UICONTROL **Accountbeschrijving**] | Geef een korte beschrijving van de account om deze te onderscheiden van andere accounts van hetzelfde type account. |

      Vouw voor configuratieinstructies de sectie hieronder uit die overeenkomt met de [!UICONTROL **Accounttype**] die u hebt geselecteerd.

      Gebruik om het even welke volgende rekeningtypes wanneer het vormen van een rapportbestemming. Vouw voor configuratieinstructies het accounttype uit. (Extra [verouderde doelen](#legacy-destinations) zijn ook beschikbaar, maar worden niet aanbevolen.)

      +++Amazon S3

      Geef de volgende informatie op om een Amazon S3 Role ARN-account te configureren:

      | Veld | Functie |
      |---------|----------|
      | [!UICONTROL **Rol ARN**] | U moet een Rol ARN (de Naam van het Middel van Amazon) verstrekken die de Adobe kan gebruiken om toegang tot de rekening van Amazon S3 te krijgen. Om dit te doen, creeert u een IAM toestemmingsbeleid voor de bronrekening, maakt het beleid aan een gebruiker vast, en creeert dan een rol voor de bestemmingsrekening. Zie voor specifieke informatie [deze AWS-documentatie](https://aws.amazon.com/premiumsupport/knowledge-center/cross-account-access-iam/).<p>Raadpleeg het artikel voor informatie over het instellen van de machtigingen voor het emmertje [Hoe kan ik dwars-rekeningstoegang tot voorwerpen verlenen die in Amazon S3 emmers zijn?](https://repost.aws/knowledge-center/cross-account-access-s3) in het Amazon-kenniscentrum. |
      | [!UICONTROL **ARN gebruiker**] | De Gebruiker ARN (de Naam van het Middel van Amazon) wordt verstrekt door Adobe. U moet deze gebruiker aan het beleid vastmaken u creeerde. |

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
      | [!UICONTROL **URI sleutelvault**] | <p>Het pad naar de SAS URI in Azure Key Vault.  Om Azure SAS te configureren, moet u een SAS-URI opslaan als een geheim met Azure Key Vault. Zie voor meer informatie de [Microsoft Azure-documentatie over het instellen en ophalen van een geheim bij Azure Key Vault](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations).</p><p>Nadat de sleutelvault-URI is gemaakt:<ul><li>Voeg een toegangsbeleid op de Zeer belangrijke vault toe om toestemming aan de Azure toepassing te verlenen die u creeerde.</li><li>Controleer of de toepassings-id is toegekend aan de `Key Vault Certificate User` ingebouwde rol om tot de belangrijkste vault URI toegang te hebben.</br><p>Zie voor meer informatie [Azure ingebouwde rollen](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles).</p></li></ul><p>Zie voor meer informatie de [Microsoft Azure-documentatie over het toewijzen van een beleid voor toegang tot Key Vault](https://learn.microsoft.com/en-us/azure/key-vault/general/assign-access-policy?tabs=azure-portal).</p> |
      | [!UICONTROL **geheime naam sleutelvault**] | De geheime naam die u hebt gemaakt toen u het geheim toevoegde aan Azure Key Vault. In Microsoft Azure vindt u deze informatie in de Key Vault die u hebt gemaakt, op de **Key Vault** instellingenpagina&#39;s. Zie voor meer informatie de [Microsoft Azure-documentatie over het instellen en ophalen van een geheim bij Azure Key Vault](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations). |
      | [!UICONTROL **Geheim**] | Kopieer het geheim van de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Certificaten en geheimen** in uw toepassing. Zie de klasse [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft Identity-platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |

      {style="table-layout:auto"}

+++

      +++Azure RBAC

      Geef de volgende informatie op om een Azure RBAC-account te configureren:

      | Veld | Functie |
      |---------|----------|
      | [!UICONTROL **Toepassings-id**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Overzicht** in uw toepassing. Zie de klasse [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft Identity-platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
      | [!UICONTROL **Tenant-id**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Overzicht** in uw toepassing. Zie de klasse [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft Identity-platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
      | [!UICONTROL **Geheim**] | Kopieer het geheim van de Azure-toepassing die u hebt gemaakt. In Microsoft Azure bevindt deze informatie zich op de **Certificaten en geheimen** in uw toepassing. Zie de klasse [Microsoft Azure-documentatie over het registreren van een toepassing bij het Microsoft Identity-platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |

      {style="table-layout:auto"}

+++

      +++E-mail

      Geef de volgende informatie op om een e-mailaccount te configureren:

      | Veld | Functie |
      |---------|----------|
      | [!UICONTROL **Ontvangers**] | E-mailmeldingen kunnen naar specifieke gebruikers worden verzonden wanneer het rapport wordt verzonden. Geef één e-mailadres of een lijst met e-mailadressen door komma&#39;s gescheiden op. <!-- How does this differ from the Notification email tab? --> |

   1. Selecteren [!UICONTROL **Locatie toevoegen**] en geeft u de volgende informatie op: |Veld | Functie | |—|—| | [!UICONTROL **Naam**] | De naam van de locatie.  | | [!UICONTROL **Beschrijving**] | Geef een korte beschrijving van de account om deze te onderscheiden van andere accounts van hetzelfde type account. | | [!UICONTROL **Locatieaccount**] | Selecteer de locatieaccount die u hebt gemaakt in [Een account toevoegen](#add-an-account). |

   1. In de [!UICONTROL **Locatie-eigenschappen**] in, geeft u specifieke informatie op over het accounttype van uw locatieaccount.

      Vouw voor configuratieinstructies de sectie hieronder uit die overeenkomt met de [!UICONTROL **Accounttype**] die u eerder hebt geselecteerd.

      +++Amazon S3

      Geef de volgende informatie op om een Amazon S3-locatie te configureren:

      | Veld | Functie |
      |---------|----------|
      | [!UICONTROL **Naam van emmertje**] | Het emmertje in uw Amazon S3-account waarin u Adobe Analytics-gegevens wilt verzenden. <p>Zorg ervoor dat de gebruiker-ARN die door de Adobe is geleverd, de `S3:PutObject` toestemming om bestanden naar dit emmertje te uploaden. Met deze machtiging kan de ARN-gebruiker initiële bestanden uploaden en bestanden overschrijven voor volgende uploads.</p><p>Emmernamen moeten voldoen aan specifieke naamgevingsregels. Ze moeten bijvoorbeeld tussen 3 en 63 tekens lang zijn, ze mogen alleen bestaan uit kleine letters, cijfers, puntjes (.) en afbreekstreepjes (-) en ze moeten beginnen en eindigen met een letter of getal. [Een volledige lijst met naamgevingsregels is beschikbaar in de documentatie van AWS](https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucketnamingrules.html). </p> |
      | [!UICONTROL **Voorvoegsel toets**] | De map in het emmertje waar u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Map_name/ |

      {style="table-layout:auto"}

+++

      +++Google Cloud Platform

      Geef de volgende informatie op om een locatie voor een Google Cloud-platform te configureren:

      | Veld | Functie |
      |---------|----------|
      | [!UICONTROL **Naam van emmertje**] | Het emmertje binnen uw GCP rekening waar u de gegevens van Adobe Analytics wilt worden verzonden. <p>Zorg ervoor dat u één van beide volgende toestemmingen aan Opdrachtgever hebt verleend die door Adobe wordt verstrekt:<ul><li>`roles/storage.objectCreator`: Gebruik deze machtiging als u Opdrachtgever wilt beperken tot het maken van alleen bestanden in uw GCP-account. </br>**Belangrijk:** Als u deze toestemming met geplande rapportering gebruikt, moet u een uniek dossier - naam voor elke nieuwe geplande uitvoer gebruiken. Anders, zal de rapportgeneratie ontbreken omdat Principal geen toegang heeft om bestaande dossiers te overschrijven.</li><li>`roles/storage.objectUser`: Gebruik deze machtiging als u wilt dat de Opdrachtgever toegang heeft tot bestanden in uw GCP-account, deze bestanden kan weergeven, bijwerken en verwijderen.</br>Met deze machtiging kan de Opdrachtgever bestaande bestanden overschrijven voor volgende uploads, zonder dat automatisch unieke bestandsnamen moeten worden gegenereerd voor elke nieuwe geplande export.</li></ul><p>Zie voor informatie over het verlenen van machtigingen [Voeg een hoofd aan een beleid op het niveau van de emmertje toe](https://cloud.google.com/storage/docs/access-control/using-iam-permissions#bucket-add) in de Google Cloud-documentatie.</p> |
      | [!UICONTROL **Voorvoegsel toets**] | De map in het emmertje waar u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Map_name/ |

      {style="table-layout:auto"}

+++

      +++Azure SAS

      Geef de volgende informatie op om een Azure SAS-locatie te configureren:

      | Veld | Functie |
      |---------|----------|
      | [!UICONTROL **Containernaam**] | De container in de account die u hebt opgegeven, waarnaar u Adobe Analytics-gegevens wilt verzenden. |
      | [!UICONTROL **Voorvoegsel toets**] | De map in de container waarin u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Bijvoorbeeld: `folder_name/`<p>Zorg ervoor dat de opslag in SAS URI die u hebt opgegeven in het geheime naamveld Key Vault bij de configuratie van de Azure SAS-account, de `Write` toestemming. Hierdoor kan de SAS URI bestanden in uw Azure-container maken. <p>Als u wilt dat de SAS-URI ook bestanden overschrijft, zorgt u ervoor dat de SAS-URI-winkel de `Delete` toestemming.</p><p>Zie voor meer informatie [Bronnen voor blokopslag](https://learn.microsoft.com/en-us/azure/storage/blobs/storage-blobs-introduction#blob-storage-resources) in de Azure Blob Storage-documentatie.</p> |

      {style="table-layout:auto"}

+++

      +++Azure RBAC

      Geef de volgende informatie op om een Azure RBAC-locatie te configureren:

      | Veld | Functie |
      |---------|----------|
      | [!UICONTROL **Containernaam**] | De container in de account die u hebt opgegeven, waarnaar u Adobe Analytics-gegevens wilt verzenden. Zorg ervoor dat u machtigingen verleent om bestanden te uploaden naar de Azure-toepassing die u eerder hebt gemaakt. |
      | [!UICONTROL **Voorvoegsel toets**] | De map in de container waarin u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Bijvoorbeeld: `folder_name/`<p>Zorg ervoor dat de toepassings-id die u hebt opgegeven bij het configureren van de Azure RBAC-account, is toegewezen aan de `Storage Blob Data Contributor` rol om tot de container (omslag) toegang te hebben.</p> <p>Zie voor meer informatie [Azure ingebouwde rollen](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles).</p> |
      | [!UICONTROL **Accountnaam**] | De Azure-opslagaccount. |

      {style="table-layout:auto"}

+++

1. Ga door met het configureren van uw verzoek voor Data Warehouse op de [!UICONTROL **Rapportopties**] tab. Zie voor meer informatie [Configureer rapportopties voor een Data Warehouse-verzoek](/help/export/data-warehouse/create-request/dw-request-report-options.md).

## Oudere bestemmingen

>[!IMPORTANT]
>
>De doelen die in deze sectie worden beschreven, zijn verouderd en worden niet aanbevolen. Gebruik in plaats daarvan een van de volgende doelen bij het maken van een gegevensopslagbestemming: Amazon S3, Google Cloud Platform, Azure RBAC, Azure SAS of Email. Zie de bovenstaande informatie voor meer informatie over elk van deze aanbevolen doelen.

De volgende informatie verstrekt configuratieinformatie voor elk van de erfenisbestemmingen:

### FTP

Gegevens van het gegevenspakhuis kunnen aan een Adobe of klant-ontvangen plaats van FTP worden geleverd. Vereist een FTP-host, gebruikersnaam en wachtwoord. Gebruik het padveld om feed-bestanden in een map te plaatsen. Mappen moeten al bestaan; feeds genereren een fout als het opgegeven pad niet bestaat.

Gebruik de volgende informatie wanneer u de beschikbare velden invult:

#### Accountvelden

* [!UICONTROL **Accountnaam**]: De naam van de FTP-account.

* [!UICONTROL **Accountbeschrijving**]: Een beschrijving van de FTP-account.

* [!UICONTROL **Hostnaam**]: Voer de gewenste FTP-doel-URL in. Bijvoorbeeld: `ftp.company.com`.

  >[!NOTE]
  >
  >  Niet opnemen `ftp://` aan het begin van de URL.

* [!UICONTROL **Gebruikersnaam**]: Voer de gebruikersnaam in die u wilt aanmelden bij de FTP-site.

* [!UICONTROL **Wachtwoord en wachtwoord bevestigen**]: Voer het wachtwoord in om u aan te melden bij de FTP-site.

#### Locatievelden

* [!UICONTROL **Locatienaam**]: De naam van de locatie op de FTP-account waarnaar u bestanden wilt verzenden.

* [!UICONTROL **Locatiebeschrijving**]: Een beschrijving van de locatie op de FTP-account.

* [!UICONTROL **Directorypad**]: Het pad naar de locatie op de FTP-account.

### SFTP

SFTP-ondersteuning voor gegevenspakhuis is beschikbaar. Vereist een gastheer SFTP, gebruikersbenaming, en de bestemmingsplaats om een geldige RSA of DSA openbare sleutel te bevatten. U kunt de aangewezen openbare sleutel downloaden wanneer het creëren van de bestemming van het gegevenspakhuis.

Gebruik de volgende informatie wanneer u de beschikbare velden invult:

#### Accountvelden

* [!UICONTROL **Accountnaam**]: De naam van de FTP-account.

* [!UICONTROL **Accountbeschrijving**]: Een beschrijving van de FTP-account.

* [!UICONTROL **Hostnaam**]: Voer de gewenste doel-URL voor SFTP in. Bijvoorbeeld: `sftp.company.com`.

  >[!NOTE]
  >
  >  Niet opnemen `sftp://` aan het begin van de URL.

* [!UICONTROL **Gebruikersnaam**]: Voer de gebruikersnaam in die u wilt aanmelden bij de SFTP-site.

* [!UICONTROL **Tijdelijke bestandsextensies gebruiken tijdens het uploaden**]: Als deze optie is ingeschakeld, wordt de `.part` bestandsextensie wordt gebruikt tijdens het uploadproces. Laat deze optie ingeschakeld tenzij de bestandsnamen op uw SFTP-server na het uploaden niet kunnen worden gewijzigd.

* [!UICONTROL **Openbare sleutels**]: Download de juiste openbare sleutel wanneer u de bestemming van het gegevenspakhuis maakt.

#### Locatievelden

* [!UICONTROL **Locatienaam**]: De naam van de locatie op de SFTP-account waarnaar u bestanden wilt verzenden.

* [!UICONTROL **Locatiebeschrijving**]: Een beschrijving van de locatie op de SFTP-account.

* [!UICONTROL **Directorypad**]: Het pad naar de locatie op de SFTP-account.

Voor extra informatie over configuratie SFTP, zie [Data Warehouse-aanvragen naar SFTP-servers verzenden](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-dw.md).

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
