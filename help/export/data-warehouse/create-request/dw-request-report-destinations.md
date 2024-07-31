---
description: Stappen die beschrijven hoe te om een verzoek van de Data Warehouse tot stand te brengen.
title: Vorm een rapportbestemming voor een verzoek van de Data Warehouse
feature: Data Warehouse
exl-id: 3c7faea3-4d90-4274-88f3-e9337c94155f
source-git-commit: f41144d5889d03441f06806256ec79aa25d242cf
workflow-type: tm+mt
source-wordcount: '2612'
ht-degree: 0%

---

# Vorm een rapportbestemming voor een verzoek van de Data Warehouse

Er zijn diverse configuratieopties beschikbaar wanneer het creëren van een verzoek van de Data Warehouse. De volgende informatie beschrijft hoe te om een rapportbestemming voor het verzoek te vormen.

Voor informatie over hoe te beginnen creërend een verzoek, evenals verbindingen aan andere belangrijke configuratieopties, zie [ een verzoek van de Data Warehouse ](/help/export/data-warehouse/create-request/t-dw-create-request.md) creëren.

>[!NOTE]
>
>Overweeg het volgende wanneer het vormen van een rapportbestemming:
>
>* We raden u aan een cloudaccount of e-mailbericht te gebruiken voor uw rapportbestemming. [ Verouderde FTP en de rekeningen van SFTP ](#legacy-destinations) zijn beschikbaar maar niet geadviseerd.
>
>* Alle cloudaccounts die u eerder hebt geconfigureerd, kunnen voor Data Warehouse worden gebruikt. U kunt cloudaccounts op de volgende manieren configureren:
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

Om de bestemming te vormen waar de rapporten van de Data Warehouse worden verzonden:

1. Als u niet reeds hebt, begin creërend een verzoek in Adobe Analytics door te selecteren **[!UICONTROL Tools]** > **[!UICONTROL Data Warehouse]** > [!UICONTROL **voeg**] toe.

   Voor extra details, zie [ een verzoek van de Data Warehouse ](/help/export/data-warehouse/create-request/t-dw-create-request.md) creëren.

1. Voor de Nieuwe pagina van het de verzoekverzoek van de Data Warehouse, selecteer de [!UICONTROL **bestemming van het Rapport**] tabel.

   ![ de bestemmingslusje van het Rapport ](assets/dw-report-destination.png)

1. (Voorwaardelijk) als een cloudaccount (en een bestemming voor die account) al in Adobe Analytics is geconfigureerd, kunt u dit als uw rapportbestemming gebruiken:

   >[!NOTE]
   >
   >De rekeningen zijn beschikbaar aan u slechts als u hen vormde of als zij met een organisatie werden gedeeld u een deel van bent.
   >
   >Als u een systeembeheerder bent, [!UICONTROL **toon alle bestemmingen**] optie is beschikbaar. Schakel deze optie in als u toegang wilt hebben tot alle accounts en locaties die door een gebruiker in de organisatie zijn gemaakt.

   1. Selecteer de rekening van [!UICONTROL **Uitgezochte rekening**] drop-down menu.

      Alle cloudaccounts die u hebt geconfigureerd in een van de volgende Adobe Analytics-domeinen kunnen worden gebruikt:

      * Wanneer het invoeren van de classificatiegegevens van Adobe Analytics, zoals die in [ Schema ](/help/components/classifications/sets/manage/schema.md) worden beschreven.

        Nochtans, kunnen om het even welke plaatsen die voor het invoeren van classificatiegegevens worden gevormd niet worden gebruikt. Voeg in plaats daarvan een nieuwe bestemming toe, zoals hieronder wordt beschreven.

      * Wanneer het vormen van rekeningen en plaatsen in het gebied van Plaatsen, zoals die in [ worden beschreven vorm wolk invoer en de uitvoerrekeningen ](/help/components/locations/configure-import-accounts.md) en [ vorm wolk invoer en de uitvoerplaatsen ](/help/components/locations/configure-import-locations.md).

   1. Selecteer de bestemming verbonden aan de rekening van [!UICONTROL **Uitgezochte bestemming**] drop-down menu. <!-- Is this correct? -->

1. (Voorwaardelijk) Als u geen toegang hebt tot een cloudaccount die al in Adobe Analytics is geconfigureerd, kunt u een account configureren:

   1. Selecteer [!UICONTROL **toevoegen rekening**], dan specificeer de volgende informatie:

      | Veld | Functie |
      |---------|----------|
      | [!UICONTROL **Type van Rekening**] | Selecteer het type cloudaccount. We raden u aan voor elk accounttype één account te hebben, met meerdere locaties binnen dat account. <p>Nadat u een accounttype hebt gekozen, worden de velden weergegeven die specifiek zijn voor dat accounttype. </p> |
      | [!UICONTROL **de naam van de Rekening**] | Geef een naam op voor de account. Deze naam wordt weergegeven wanneer u een locatie maakt. <!-- true? --> |
      | [!UICONTROL **beschrijving van de Rekening**] | Geef een korte beschrijving van de account om deze te onderscheiden van andere accounts van hetzelfde type account. |

      Voor configuratieinstructies, breid de sectie onder uit die aan het [!UICONTROL **type van Rekening**] beantwoordt dat u selecteerde.

      Gebruik om het even welke volgende rekeningtypes wanneer het vormen van een rapportbestemming. Vouw voor configuratieinstructies het accounttype uit. (De extra [ erfenisbestemmingen ](#legacy-destinations) zijn ook beschikbaar, maar niet geadviseerd.)

      +++Amazon S3

      Geef de volgende informatie op om een Amazon S3 Role ARN-account te configureren:

      | Veld | Functie |
      |---------|----------|
      | [!UICONTROL **ARN van de Rol**] | U moet een Rol ARN (de Naam van het Middel van Amazon) verstrekken die de Adobe kan gebruiken om toegang tot de rekening van Amazon S3 te krijgen. Om dit te doen, creeert u een IAM toestemmingsbeleid voor de bronrekening, maakt het beleid aan een gebruiker vast, en creeert dan een rol voor de bestemmingsrekening. Voor specifieke informatie, zie [ deze documentatie van AWS ](https://aws.amazon.com/premiumsupport/knowledge-center/cross-account-access-iam/).<p>Voor informatie over hoe te opstelling ziet de toestemming van het emmertje, het artikel [ hoe ik dwars-rekeningstoegang tot voorwerpen kan verlenen die in Amazon S3 emmers zijn?](https://repost.aws/knowledge-center/cross-account-access-s3) in het Amazon-kenniscentrum. |
      | [!UICONTROL **ARN VAN DE Gebruiker**] | De Gebruiker ARN (de Naam van het Middel van Amazon) wordt verstrekt door Adobe. U moet deze gebruiker aan het beleid vastmaken u creeerde. |

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
      | [!UICONTROL **Zeer belangrijke vault URI**] | <p>Het pad naar de SAS URI in Azure Key Vault.  Om Azure SAS te configureren, moet u een SAS-URI opslaan als een geheim met Azure Key Vault. Voor informatie, zie de [ Microsoft Azure documentatie over hoe te om een geheim van Azure Key Vault ](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations) te plaatsen en terug te winnen.</p><p>Nadat de sleutelvault-URI is gemaakt:<ul><li>Voeg een toegangsbeleid op de Zeer belangrijke vault toe om toestemming aan de Azure toepassing te verlenen die u creeerde.</li><li>Zorg ervoor dat de toepassings-id de `Key Vault Certificate User` ingebouwde rol heeft gekregen om toegang te krijgen tot de sleutelvault URI.</br><p>Voor meer informatie, zie [ Azure ingebouwde rollen ](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles).</p></li></ul><p>Voor informatie, zie [ Microsoft Azure documentatie over hoe te om een Zeer belangrijk de toegangsbeleid van de Vault toe te wijzen ](https://learn.microsoft.com/en-us/azure/key-vault/general/assign-access-policy?tabs=azure-portal).</p> |
      | [!UICONTROL **Zeer belangrijke geheime naam van de kluis**] | De geheime naam die u hebt gemaakt toen u het geheim toevoegde aan Azure Key Vault. In Microsoft Azure, wordt deze informatie gevestigd in de Belangrijkste Vault u, op de **Zeer belangrijke de montagespagina&#39;s van de Uitvault** creeerde. Voor informatie, zie de [ Microsoft Azure documentatie over hoe te om een geheim van Azure Key Vault ](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations) te plaatsen en terug te winnen. |
      | [!UICONTROL **Geheim**] | Kopieer het geheim van de Azure-toepassing die u hebt gemaakt. In Microsoft Azure, wordt deze informatie gevestigd op het **Certificaten &amp; geheimen** lusje binnen uw toepassing. Voor meer informatie, zie [ Microsoft Azure documentatie over hoe te om een toepassing met het de identiteitsplatform van Microsoft ](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app) te registreren. |

      {style="table-layout:auto"}

+++

      +++Azure RBAC

      Geef de volgende informatie op om een Azure RBAC-account te configureren:

      | Veld | Functie |
      |---------|----------|
      | [!UICONTROL **identiteitskaart van de Toepassing**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure, wordt deze informatie gevestigd op het **Overzicht** lusje binnen uw toepassing. Voor meer informatie, zie [ Microsoft Azure documentatie over hoe te om een toepassing met het de identiteitsplatform van Microsoft ](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app) te registreren. |
      | [!UICONTROL **identiteitskaart van de HTENT**] | Kopieer deze id uit de Azure-toepassing die u hebt gemaakt. In Microsoft Azure, wordt deze informatie gevestigd op het **Overzicht** lusje binnen uw toepassing. Voor meer informatie, zie [ Microsoft Azure documentatie over hoe te om een toepassing met het de identiteitsplatform van Microsoft ](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app) te registreren. |
      | [!UICONTROL **Geheim**] | Kopieer het geheim van de Azure-toepassing die u hebt gemaakt. In Microsoft Azure, wordt deze informatie gevestigd op het **Certificaten &amp; geheimen** lusje binnen uw toepassing. Voor meer informatie, zie [ Microsoft Azure documentatie over hoe te om een toepassing met het de identiteitsplatform van Microsoft ](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app) te registreren. |

      {style="table-layout:auto"}

+++

      +++E-mail

      Geef de volgende informatie op om een e-mailaccount te configureren:

      | Veld | Functie |
      |---------|----------|
      | [!UICONTROL **Ontvangers**] | E-mailmeldingen kunnen naar specifieke gebruikers worden verzonden wanneer het rapport wordt verzonden. Geef één e-mailadres of een lijst met e-mailadressen door komma&#39;s gescheiden op. <!-- How does this differ from the Notification email tab? --> |

   1. Selecteer [!UICONTROL **plaats**] toevoegen, dan specificeer de volgende informatie:

      | Veld | Functie |
      |---------|----------|
      | [!UICONTROL **Naam**] | De naam van de locatie. |
      | [!UICONTROL **Beschrijving**] | Geef een korte beschrijving van de account om deze te onderscheiden van andere accounts van hetzelfde type account. |
      | [!UICONTROL **de rekening van de Plaats**] | Selecteer de plaatsrekening die u in [ creeerde voeg een rekening ](#add-an-account) toe. |

   1. In de [!UICONTROL **eigenschappen van de Plaats**] sectie, specificeer informatie specifiek voor het accounttype van uw plaatsrekening.

      Voor configuratieinstructies, breid de sectie onder uit die aan het [!UICONTROL **type van Rekening**] beantwoordt dat u eerder selecteerde.

      +++Amazon S3

      Geef de volgende informatie op om een Amazon S3-locatie te configureren:

      | Veld | Functie |
      |---------|----------|
      | [!UICONTROL **naam van het Emmertje**] | Het emmertje in uw Amazon S3-account waarin u Adobe Analytics-gegevens wilt verzenden. <p>Zorg ervoor dat de Gebruiker ARN die door Adobe werd verstrekt de `S3:PutObject` toestemming heeft om dossiers aan dit emmertje te uploaden. Met deze machtiging kan de ARN-gebruiker initiële bestanden uploaden en bestanden overschrijven voor volgende uploads.</p><p>Emmernamen moeten voldoen aan specifieke naamgevingsregels. Ze moeten bijvoorbeeld tussen 3 en 63 tekens lang zijn, ze mogen alleen bestaan uit kleine letters, cijfers, puntjes (.) en afbreekstreepjes (-) en ze moeten beginnen en eindigen met een letter of getal. [ A volledige lijst van het noemen van regels is beschikbaar in de documentatie van AWS ](https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucketnamingrules.html). </p> |
      | [!UICONTROL **Zeer belangrijke prefix**] | De map in het emmertje waar u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Map_name/ |

      {style="table-layout:auto"}

+++

      +++Google Cloud Platform

      Geef de volgende informatie op om een locatie voor een Google Cloud-platform te configureren:

      | Veld | Functie |
      |---------|----------|
      | [!UICONTROL **naam van het Emmertje**] | Het emmertje binnen uw GCP rekening waar u de gegevens van Adobe Analytics wilt worden verzonden. <p>Zorg ervoor dat u één van beiden van de volgende toestemmingen aan Principal hebt verleend die door Adobe wordt verstrekt: (Voor informatie over het verlenen van toestemmingen, zie [ een hoofd aan een emmertje-vlakke beleid ](https://cloud.google.com/storage/docs/access-control/using-iam-permissions#bucket-add) in de documentatie van de Wolk van Google toevoegen.)<ul><li>`roles/storage.objectCreator`: Gebruik deze machtiging als u Opdrachtgever wilt beperken tot het maken van alleen bestanden in uw GCP-account. </br>**Belangrijk:** als u deze toestemming met geplande rapportering gebruikt, moet u een uniek dossier - naam voor elke nieuwe geplande uitvoer gebruiken. Anders, zal de rapportgeneratie ontbreken omdat Principal geen toegang heeft om bestaande dossiers te overschrijven.</li><li>`roles/storage.objectUser`: Gebruik deze machtiging als u wilt dat de Opdrachtgever toegang heeft tot de bestanden in uw GCP-account, deze bestanden kan weergeven, bijwerken en verwijderen.</br> Deze toestemming staat Principal toe om bestaande dossiers voor verdere uploads, zonder de behoefte te beschrijven om unieke dossiernamen voor elke nieuwe geplande uitvoer automatisch te produceren.</li></ul><p>Als uw organisatie [ het beleidsbeperkingen van de Organisatie ](https://cloud.google.com/storage/docs/org-policy-constraints) gebruikt om slechts de rekening van het Platform van de Wolk van Google in uw lijst van gewenste personen toe te staan, hebt u de volgende Adobe-Bezit de organisatieidentiteitskaart van het Platform van Google Cloud nodig: <ul><li>`DISPLAY_NAME`: `adobe.com`</li><li>`ID`: `178012854243`</li><li>`DIRECTORY_CUSTOMER_ID`: `C02jo8puj`</li></ul> </p> |
      | [!UICONTROL **Zeer belangrijke prefix**] | De map in het emmertje waar u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Map_name/ |

      {style="table-layout:auto"}

+++

      +++Azure SAS

      Geef de volgende informatie op om een Azure SAS-locatie te configureren:

      | Veld | Functie |
      |---------|----------|
      | [!UICONTROL **naam van de Container**] | De container in de account die u hebt opgegeven, waarnaar u Adobe Analytics-gegevens wilt verzenden. |
      | [!UICONTROL **Zeer belangrijke prefix**] | De map in de container waarin u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Bijvoorbeeld: `folder_name/`<p>Zorg ervoor dat de opslag van SAS URI die u in het geheime naamveld Key Vault hebt opgegeven bij de configuratie van de Azure SAS-account, de `Write` -machtiging heeft. Hierdoor kan de SAS URI bestanden in uw Azure-container maken. <p>Als u wilt dat de SAS-URI ook bestanden overschrijft, controleert u of de SAS-URI-opslag de machtiging `Delete` heeft.</p><p>Voor meer informatie, zie [ de opslagmiddelen van de Blob ](https://learn.microsoft.com/en-us/azure/storage/blobs/storage-blobs-introduction#blob-storage-resources) in de Azure documentatie van de Opslag van Blob.</p> |

      {style="table-layout:auto"}

+++

      +++Azure RBAC

      Geef de volgende informatie op om een Azure RBAC-locatie te configureren:

      | Veld | Functie |
      |---------|----------|
      | [!UICONTROL **naam van de Container**] | De container in de account die u hebt opgegeven, waarnaar u Adobe Analytics-gegevens wilt verzenden. Zorg ervoor dat u machtigingen verleent om bestanden te uploaden naar de Azure-toepassing die u eerder hebt gemaakt. |
      | [!UICONTROL **Zeer belangrijke prefix**] | De map in de container waarin u de gegevens wilt plaatsen. Geef een mapnaam op en voeg vervolgens een backslash achter de naam toe om de map te maken. Bijvoorbeeld: `folder_name/`<p>Controleer of de toepassings-id die u hebt opgegeven bij het configureren van de Azure RBAC-account, de rol `Storage Blob Data Contributor` heeft gekregen voor toegang tot de container (map).</p> <p>Voor meer informatie, zie [ Azure ingebouwde rollen ](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles).</p> |
      | [!UICONTROL **de naam van de Rekening**] | De   Azure-opslagaccount. |

      {style="table-layout:auto"}

+++

1. Ga door het vormen van uw verzoek van de Data Warehouse op het [!UICONTROL **opties van het Rapport**] tabel. Voor meer informatie, zie [ rapportopties voor een verzoek van de Data Warehouse ](/help/export/data-warehouse/create-request/dw-request-report-options.md) vormen.

## Oudere bestemmingen

>[!IMPORTANT]
>
>De doelen die in deze sectie worden beschreven, zijn verouderd en worden niet aanbevolen. Gebruik in plaats daarvan een van de volgende doelen bij het maken van een gegevensopslagbestemming: Amazon S3, Google Cloud Platform, Azure RBAC, Azure SAS of Email. Zie de bovenstaande informatie voor meer informatie over elk van deze aanbevolen doelen.

De volgende informatie verstrekt configuratieinformatie voor elk van de erfenisbestemmingen:

### FTP

Gegevens van het gegevenspakhuis kunnen aan een Adobe of klant-ontvangen plaats van FTP worden geleverd. Vereist een FTP-host, gebruikersnaam en wachtwoord. Gebruik het padveld om feed-bestanden in een map te plaatsen. Mappen moeten al bestaan; feeds genereren een fout als het opgegeven pad niet bestaat.

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

Voor extra informatie over configuratie SFTP, zie [ verzoeken van de Data Warehouse naar servers SFTP verzenden ](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-dw.md).

### S3

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

### Azure Blob

De steun van het pakhuis van gegevens Azure Blob bestemmingen. Hiervoor is een container, account en sleutel vereist. Amazon versleutelt de gegevens automatisch in rust. Wanneer u de gegevens downloadt, worden deze automatisch gedecodeerd. Zie [ een opslagrekening ](https://docs.microsoft.com/en-us/azure/storage/common/storage-quickstart-create-account?tabs=azure-portal#view-and-copy-storage-access-keys) binnen Microsoft Azure documenten voor meer informatie creëren.

>[!NOTE]
>
>U moet uw eigen proces uitvoeren om schijfruimte op de bestemming van het gegevenspakhuis te beheren. Adobe verwijdert geen gegevens van de server.
