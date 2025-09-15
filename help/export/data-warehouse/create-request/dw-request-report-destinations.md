---
description: Stappen die beschrijven hoe u een Data Warehouse-aanvraag maakt.
title: Een rapportbestemming voor een Data Warehouse-aanvraag configureren
feature: Data Warehouse
exl-id: 3c7faea3-4d90-4274-88f3-e9337c94155f
source-git-commit: f0a5f72667fd6fc7847ede82d5196d9159fc558c
workflow-type: tm+mt
source-wordcount: '1977'
ht-degree: 0%

---

# Een rapportbestemming voor een Data Warehouse-aanvraag configureren

Er zijn verschillende configuratieopties beschikbaar wanneer u een Data Warehouse-aanvraag maakt. De volgende informatie beschrijft hoe te om een rapportbestemming voor het verzoek te vormen.

Voor informatie over hoe te beginnen creërend een verzoek, evenals verbindingen aan andere belangrijke configuratieopties, zie [ een verzoek van Data Warehouse ](/help/export/data-warehouse/create-request/t-dw-create-request.md) creëren.

>[!NOTE]
>
>Overweeg het volgende wanneer het vormen van een rapportbestemming:
>
>* We raden u aan een cloudaccount of e-mailbericht te gebruiken voor uw rapportbestemming. [ Verouderde FTP en de rekeningen van SFTP ](#legacy-destinations) zijn beschikbaar maar niet geadviseerd.
>
>* Alle cloudaccounts die u eerder hebt geconfigureerd, zijn beschikbaar voor Data Warehouse. U kunt cloudaccounts op de volgende manieren configureren:
>
>   * Wanneer het vormen van [ de Diefstal van Gegevens ](/help/export/analytics-data-feed/create-feed.md)
>   
>   * Wanneer [ het invoeren van de classificatiegegevens van Adobe Analytics ](/help/components/locations/locations-manager.md) (De Rekeningen kunnen worden gebruikt, maar om het even welke plaatsen die op die rekeningen worden gevormd kunnen niet zijn.)
>   
>   * Van de manager van Plaatsen, in [ Componenten > Plaatsen ](/help/components/locations/configure-import-accounts.md).
>
>* Cloud-accounts zijn gekoppeld aan uw Adobe Analytics-gebruikersaccount. Andere gebruikers kunnen geen cloudaccounts gebruiken of weergeven die u configureert.
>
>* U kunt om het even welke plaatsen uitgeven die u van de manager van Plaatsen in [ Componenten > Plaatsen ](/help/components/locations/configure-import-accounts.md) creeert

Om de bestemming te vormen waar de rapporten van Data Warehouse worden verzonden:

1. Als u niet reeds hebt, begin creërend een verzoek in Adobe Analytics door te selecteren **[!UICONTROL Tools]** > **[!UICONTROL Data Warehouse]** > [!UICONTROL **voeg**] toe.

   Voor extra details, zie [ een verzoek van Data Warehouse ](/help/export/data-warehouse/create-request/t-dw-create-request.md) creëren.

1. Voor de Nieuwe Data Warehouse verzoekpagina, selecteer de [!UICONTROL **bestemming van het Rapport**] tabel.

   ![ de bestemmingslusje van het Rapport ](assets/dw-report-destination.png)

1. (Voorwaardelijk) als een cloudaccount (en een bestemming voor die account) al in Adobe Analytics is geconfigureerd, kunt u dit als uw rapportbestemming gebruiken:

   >[!NOTE]
   >
   >De rekeningen zijn beschikbaar aan u slechts als u hen vormde of als zij met een organisatie werden gedeeld u een deel van bent.
   >
   >Als u een systeembeheerder bent, [!UICONTROL **toon alle bestemmingen**] optie is beschikbaar. Schakel deze optie in als u toegang wilt hebben tot alle accounts en locaties die door een gebruiker in de organisatie zijn gemaakt.

   1. Selecteer de rekening van het [!UICONTROL **drop-down menu van de Rekening**].

      Alle cloudaccounts die u hebt geconfigureerd in een van de volgende Adobe Analytics-domeinen kunnen worden gebruikt:

      * Wanneer het invoeren van de classificatiegegevens van Adobe Analytics, zoals die in [ Schema ](/help/components/classifications/sets/manage/schema.md) worden beschreven.

        Nochtans, kunnen om het even welke plaatsen die voor het invoeren van classificatiegegevens worden gevormd niet worden gebruikt. Voeg in plaats daarvan een nieuwe bestemming toe, zoals hieronder wordt beschreven.

      * Wanneer het vormen van rekeningen en plaatsen in het gebied van Plaatsen, zoals die in [ worden beschreven vorm wolk invoer en de uitvoerrekeningen ](/help/components/locations/configure-import-accounts.md) en [ vorm wolk invoer en de uitvoerplaatsen ](/help/components/locations/configure-import-locations.md).

   1. Selecteer de bestemming verbonden aan de rekening van [!UICONTROL **Uitgezochte bestemming**] drop-down menu. <!-- Is this correct? -->

1. (Voorwaardelijk) Als u geen toegang hebt tot een cloudaccount die al in Adobe Analytics is geconfigureerd, kunt u een account configureren:

   1. Selecteer het [!UICONTROL **drop-down menu van de Rekening**], dan uitgezocht [!UICONTROL **voeg rekening**] toe.

   1. Geef in het dialoogvenster Account toevoegen de volgende gegevens op:

      | Veld | Functie |
      |---------|----------|
      | [!UICONTROL **de rekeningsnaam van de Plaats**] | De naam van het locatieaccount. Deze naam wordt weergegeven wanneer u een locatie maakt |
      | [!UICONTROL **de rekeningsbeschrijving van de Plaats**] | Geef een korte beschrijving van de account om deze te onderscheiden van andere accounts van hetzelfde type account. |
      | [!UICONTROL **maak rekening beschikbaar aan alle gebruikers in uw organisatie**] | Schakel deze optie in als u wilt dat andere gebruikers in uw organisatie de account kunnen gebruiken.<p>Houd rekening met het volgende wanneer u accounts deelt:</p><ul><li>Accounts die u deelt, kunnen niet worden verwijderd.</li><li>Gedeelde accounts kunnen alleen door de eigenaar van de account worden bewerkt.</li><li>Iedereen kan een locatie voor de gedeelde account maken.</li></ul> |
      | [!UICONTROL **Type van Rekening**] | Selecteer het type cloudaccount. We raden u aan voor elk accounttype één account te hebben, met meerdere locaties binnen dat account.<p>De beheerders van het systeem kunnen de accounttypes beperken die de gebruikers kunnen tot stand brengen, zoals die in [ wordt beschreven vormen of de gebruikers rekeningen ](/help/components/locations/locations-manager.md#configure-whether-users-can-create-accounts) kunnen tot stand brengen. Als u geen rekeningen kunt tot stand brengen zoals die in deze sectie worden beschreven, contacteer uw systeembeheerder.</p> |

   1. In de [!UICONTROL **eigenschappen van de Rekening**] sectie, specificeer informatie specifiek voor het accounttype dat u selecteerde.

      Voor configuratieinstructies, breid de sectie onder uit die aan het [!UICONTROL **type van Rekening**] beantwoordt dat u selecteerde. (Aanvullende oudere accounttypen zijn ook beschikbaar, maar worden niet aanbevolen.)

      **de types van Rekening**

      +++Amazon S3 Role ARN

      **NOTA:** wanneer het gebruiken van Amazon S3 met Data Warehouse, slechts wordt de encryptie SSE-S3 gesteund.

      Geef de volgende informatie op om een Amazon S3 Role ARN-account te configureren:

      | Veld | Functie |
      |---------|----------|
      | [!UICONTROL **ARN van de Rol**] | U moet een Role ARN (de Naam van het Middel van Amazon) verstrekken die Adobe kan gebruiken om tot de rekening van Amazon S3 toegang te krijgen. Om dit te doen, creeert u een IAM toestemmingsbeleid voor de bronrekening, maakt het beleid aan een gebruiker vast, en creeert dan een rol voor de bestemmingsrekening. Voor specifieke informatie, zie [ deze documentatie van AWS ](https://aws.amazon.com/premiumsupport/knowledge-center/cross-account-access-iam/). |

      {style="table-layout:auto"}

      +++

      +++Google Cloud Platform

      Geef de volgende informatie op om een Google Cloud Platform-account te configureren:

      | Veld | Functie |
      |---------|----------|
      | [!UICONTROL **identiteitskaart van het Project**] | Uw Google Cloud-project-id. Zie de [ documentatie van de Wolk van Google over het krijgen van een project identiteitskaart ](https://cloud.google.com/resource-manager/docs/creating-managing-projects#identifying_projects). |

      {style="table-layout:auto"}

      +++

      +++Azure SAS

      Geef de volgende informatie op om een Azure SAS-account te configureren:

      | Veld | Functie |
      |---------|----------|
      | [!UICONTROL **identiteitskaart van de Toepassing**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure, wordt deze informatie gevestigd op het **Overzicht** lusje binnen uw toepassing. Voor meer informatie, zie [ Microsoft Azure documentatie over hoe te om een toepassing met het de identiteitsplatform van Microsoft ](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app) te registreren. |
      | [!UICONTROL **identiteitskaart van de HTENT**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure, wordt deze informatie gevestigd op het **Overzicht** lusje binnen uw toepassing. Voor meer informatie, zie [ Microsoft Azure documentatie over hoe te om een toepassing met het de identiteitsplatform van Microsoft ](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app) te registreren. |
      | [!UICONTROL **Zeer belangrijke vault URI**] | <p>Het pad naar het SAS-token in Azure Key Vault.  Om Azure SAS te configureren, moet u een SAS-token opslaan als een geheim met Azure Key Vault. Voor informatie, zie de [ Microsoft Azure documentatie over hoe te om een geheim van Azure Key Vault ](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations) te plaatsen en terug te winnen.</p><p>Nadat de sleutelvault-URI is gemaakt, voegt u een toegangsbeleid toe op de Key Vault om toestemming te verlenen aan de Azure-toepassing die u hebt gemaakt. Voor informatie, zie [ Microsoft Azure documentatie over hoe te om een Zeer belangrijk de toegangsbeleid van de Vault toe te wijzen ](https://learn.microsoft.com/en-us/azure/key-vault/general/assign-access-policy?tabs=azure-portal).</p><p>of</p><p>Als u een toegangsrol direct wilt verlenen zonder een toegangsbeleid te creëren, zie [ Microsoft Azure documentatie over hoe te om Azure rollen toe te wijzen gebruikend Azure portaal ](https://learn.microsoft.com/en-us/azure/role-based-access-control/role-assignments-portal). Hiermee voegt u de roltoewijzing voor de toepassings-id toe aan toegang tot de sleutelvault-URI. </p> |
      | [!UICONTROL **Zeer belangrijke geheime naam van de kluis**] | De geheime naam die u hebt gemaakt toen u het geheim toevoegde aan Azure Key Vault. In Microsoft Azure, wordt deze informatie gevestigd in de Belangrijkste Vault u, op de **Zeer belangrijke de montagespagina van de Vault** creeerde. Voor informatie, zie de [ Microsoft Azure documentatie over hoe te om een geheim van Azure Key Vault ](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations) te plaatsen en terug te winnen. |
      | [!UICONTROL **het rekeningsgeheim van de Plaats**] | Kopieer het geheim van de Azure-toepassing die u hebt gemaakt. In Microsoft Azure, wordt deze informatie gevestigd op het **Certificaten &amp; geheimen** lusje binnen uw toepassing. Voor meer informatie, zie [ Microsoft Azure documentatie over hoe te om een toepassing met het de identiteitsplatform van Microsoft ](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app) te registreren. |

      {style="table-layout:auto"}

      +++   

      +++Azure RBAC

      Geef de volgende informatie op om een Azure RBAC-account te configureren:

      | Veld | Functie |
      |---------|----------|
      | [!UICONTROL **identiteitskaart van de Toepassing**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure, wordt deze informatie gevestigd op het **Overzicht** lusje binnen uw toepassing. Voor meer informatie, zie [ Microsoft Azure documentatie over hoe te om een toepassing met het de identiteitsplatform van Microsoft ](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app) te registreren. |
      | [!UICONTROL **identiteitskaart van de HTENT**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure, wordt deze informatie gevestigd op het **Overzicht** lusje binnen uw toepassing. Voor meer informatie, zie [ Microsoft Azure documentatie over hoe te om een toepassing met het de identiteitsplatform van Microsoft ](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app) te registreren. |
      | [!UICONTROL **het rekeningsgeheim van de Plaats**] | Kopieer het geheim van de Azure-toepassing die u hebt gemaakt. In Microsoft Azure, wordt deze informatie gevestigd op het **Certificaten &amp; geheimen** lusje binnen uw toepassing. Voor meer informatie, zie [ Microsoft Azure documentatie over hoe te om een toepassing met het de identiteitsplatform van Microsoft ](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app) te registreren. |

      {style="table-layout:auto"}

      +++

      +++E-mail

      >[!NOTE]
      >
      >De e-mailrekeningen kunnen slechts met [ Diefstal van Gegevens ](/help/export/analytics-data-feed/create-feed.md) worden gebruikt. (E-mailrekeningen worden niet gesteund met [ Data Warehouse ](/help/export/data-warehouse/create-request/dw-request-report-destinations.md) of [ de reeksen van de Classificatie ](/help/components/classifications/sets/overview.md)).

      Geef de volgende informatie op om een Azure RBAC-account te configureren:

      | Veld | Functie |
      |---------|----------|
      | [!UICONTROL **Ontvangers**] | E-mailmeldingen kunnen naar specifieke gebruikers worden verzonden wanneer het rapport wordt verzonden. Geef één e-mailadres of een lijst met e-mailadressen door komma&#39;s gescheiden op. |

      {style="table-layout:auto"}

      +++

1. Ga door het vormen van uw verzoek van Data Warehouse op het [!UICONTROL **opties van het Rapport**] tabel. Voor meer informatie, zie [ rapportopties voor een verzoek van Data Warehouse ](/help/export/data-warehouse/create-request/dw-request-report-options.md) vormen.

## Oudere accounttypen

>[!IMPORTANT]
>
>De doelen die in deze sectie worden beschreven, zijn verouderd en worden niet aanbevolen. Gebruik in plaats daarvan een van de volgende doelen bij het maken van een gegevensopslagbestemming: Amazon S3, Google Cloud Platform, Azure RBAC, Azure SAS of Email. Zie de bovenstaande informatie voor meer informatie over elk van deze aanbevolen doelen.

De volgende informatie verstrekt configuratieinformatie voor elk van de erfenisbestemmingen:

### FTP

Gegevens over een gegevenspakhuis kunnen worden geleverd aan een door de klant gehoste FTP-locatie. Vereist een FTP-host, gebruikersnaam en wachtwoord. Gebruik het padveld om feed-bestanden in een map te plaatsen. Mappen moeten al bestaan; feeds genereren een fout als het opgegeven pad niet bestaat.

Gebruik de volgende informatie wanneer u de beschikbare velden invult:

#### Accountvelden

* [!UICONTROL **naam van de Rekening**]: De naam van de rekening van FTP.

* [!UICONTROL **beschrijving van de Rekening**]: Een beschrijving van de rekening van FTP.

* [!UICONTROL **Hostname**]: Ga de gewenste bestemming URL van FTP in. Bijvoorbeeld `ftp.company.com` .

  >[!NOTE]
  >
  >  Neem `ftp://` niet op aan het begin van de URL.

* [!UICONTROL **Gebruikersnaam**]: Ga de gebruikersbenaming in aan login aan de plaats van FTP.

* [!UICONTROL **Wachtwoord en bevestig wachtwoord**]: Ga het wachtwoord in om aan login aan de plaats van FTP.

#### Locatievelden

* [!UICONTROL **naam van de Plaats**]: De naam van de plaats op de rekening van FTP waar u verzonden dossiers wilt.

* [!UICONTROL **beschrijving van de Plaats**]: Een beschrijving van de plaats op de rekening van FTP.

* [!UICONTROL **weg van de Folder**]: De weg aan de plaats op de rekening van FTP.

### SFTP

SFTP-ondersteuning voor gegevenspakhuis is beschikbaar. Vereist een gastheer SFTP, gebruikersbenaming, en de bestemmingsplaats om een geldige RSA of DSA openbare sleutel te bevatten. U kunt de aangewezen openbare sleutel downloaden wanneer het creëren van de bestemming van het gegevenspakhuis.

Gebruik de volgende informatie wanneer u de beschikbare velden invult:

#### Accountvelden

* [!UICONTROL **naam van de Rekening**]: De naam van de rekening van FTP.

* [!UICONTROL **beschrijving van de Rekening**]: Een beschrijving van de rekening van FTP.

* [!UICONTROL **Hostname**]: Ga de gewenste bestemmingURL van SFTP in. Bijvoorbeeld `sftp.company.com` .

  >[!NOTE]
  >
  >  Neem `sftp://` niet op aan het begin van de URL.

* [!UICONTROL **Gebruikersnaam**]: Ga de gebruikersbenaming in aan login aan de plaats van SFTP.

* [!UICONTROL **de tijdelijke dossieruitbreidingen van het Gebruik tijdens upload**]: Wanneer toegelaten, wordt de `.part` dossieruitbreiding gebruikt tijdens het uploadproces. Laat deze optie ingeschakeld tenzij de bestandsnamen op uw SFTP-server na het uploaden niet kunnen worden gewijzigd.

* [!UICONTROL **Openbare sleutels**]: Download de aangewezen openbare sleutel wanneer het creëren van de bestemming van het gegevenspakhuis.

#### Locatievelden

* [!UICONTROL **naam van de Plaats**]: De naam van de plaats op de rekening SFTP waar u verzonden dossiers wilt.

* [!UICONTROL **beschrijving van de Plaats**]: Een beschrijving van de plaats op de rekening SFTP.

* [!UICONTROL **de weg van de Folder**]: De weg aan de plaats op de rekening SFTP.

Voor extra informatie over configuratie SFTP, zie [ verzoeken van Data Warehouse naar servers SFTP verzenden ](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-dw.md).

### S3

U kunt opslaggegevens rechtstreeks naar Amazon S3 emmers verzenden. Dit bestemmingstype vereist een naam van het Emmertje, een Zeer belangrijke identiteitskaart van de Toegang, en een Geheime Sleutel. Zie [ Amazon S3 emmer noemende vereisten ](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-s3-bucket-naming-requirements.html) binnen Amazon S3 docs voor meer informatie.

De gebruiker u voor het uploaden van gegevens van het gegevenspakhuis verstrekt moet de volgende [ toestemmingen ](https://docs.aws.amazon.com/AmazonS3/latest/API/API_Operations_Amazon_Simple_Storage_Service.html) hebben:

* s3 :GetObject
* s3 :PutObject
* s3 :PutObjectAcl

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

De steun van het pakhuis van gegevens Azure Blob bestemmingen. Hiervoor is een container, account en sleutel vereist. Amazon versleutelt de gegevens automatisch in rust. Wanneer u de gegevens downloadt, worden deze automatisch gedecodeerd. Zie [ een opslagrekening ](https://docs.microsoft.com/en-us/azure/storage/common/storage-quickstart-create-account?tabs=azure-portal#view-and-copy-storage-access-keys) binnen Microsoft Azure documenten voor meer informatie creëren.

>[!NOTE]
>
>U moet uw eigen proces uitvoeren om schijfruimte op de bestemming van het gegevenspakhuis te beheren. Adobe verwijdert geen gegevens van de server.
