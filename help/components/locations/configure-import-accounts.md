---
description: De cloud-importaccount configureren en de locatie waar classificatiegegevens kunnen worden geüpload
keywords: Analysis Workspace
title: Cloud-import- en exportaccounts configureren
feature: Classifications
exl-id: 40d3d3f1-1047-4c37-8caf-6b0aabaa590a
source-git-commit: ca84a5f807545d7196e2e0e90d3209c32d3fd789
workflow-type: tm+mt
source-wordcount: '1488'
ht-degree: 0%

---

# Cloud-import- en exportaccounts configureren

<!-- This page is almost duplicated with the "Configure cloud export locations" article in CJA. Differences are that Snowflake isn't supported here and there is a Suffix field for each account type. -->

>[!NOTE]
>
>Houd rekening met het volgende wanneer u accounts maakt en bewerkt: <ul><li>De beheerders van het systeem kunnen gebruikers van het creëren van rekeningen beperken, zoals die in [ wordt beschreven vormen of de gebruikers rekeningen ](/help/components/locations/locations-manager.md#configure-whether-users-can-create-accounts) kunnen tot stand brengen. Als u geen rekeningen kunt tot stand brengen zoals die in deze sectie worden beschreven, contacteer uw systeembeheerder.</li><li>Een account kan alleen worden bewerkt door de gebruiker die het heeft gemaakt of door een systeembeheerder.</li></ul>

U kunt een cloudaccount configureren die wordt gebruikt voor een of meer van de volgende doeleinden:

* Het uitvoeren van dossiers gebruikend [ Diefstal van Gegevens ](/help/export/analytics-data-feed/create-feed.md)
* Het uitvoeren van rapporten gebruikend [ Data Warehouse ](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)
* Het uitvoeren van dossiers wanneer het gebruiken van [ Report Builder ](/help/analyze/report-builder/report-builder-export.md)
* Het invoeren van schema&#39;s gebruikend [ de reeksen van de Classificatie ](/help/components/classifications/sets/overview.md)

U moet Adobe Analytics configureren met de benodigde informatie voor toegang tot uw cloud-account. Dit proces bestaat uit het toevoegen van en het vormen van de rekening (zoals Amazon S3 Rol ARN, het Platform van de Wolk van Google, etc.) zoals die in dit artikel wordt beschreven, en dan het toevoegen van en het vormen van de plaats binnen die rekening (zoals een omslag binnen de rekening) zoals die in [ wordt beschreven vormt de wolkinvoer en de uitvoerplaatsen ](/help/components/locations/configure-import-locations.md).

Voor informatie over hoe te om bestaande rekeningen te bekijken en te schrappen, zie [ manager van Plaatsen ](/help/components/locations/locations-manager.md).

Een cloudimport- of -exportaccount configureren:

1. In Adobe Analytics, uitgezochte [!UICONTROL **Componenten**] > [!UICONTROL **Plaatsen**].
1. Voor de [!UICONTROL Locations] pagina, selecteer de [!UICONTROL **rekeningen van de Plaats**] tabel.
1. (Voorwaardelijk) als u een systeembeheerder bent, kunt u de [!UICONTROL **rekeningen van de Mening voor alle gebruikers**] optie toelaten om rekeningen te bekijken die door alle gebruikers in uw organisatie worden gecreeerd.
   ![ meningsrekeningen voor alle gebruikers ](assets/accounts-all-users.png)
1. Om een nieuwe rekening tot stand te brengen, [!UICONTROL **voeg rekening**] toe.

   De [!UICONTROL **de rekeningsdetails van de Plaats**] vertoningen van de dialoog.

   of

   Om een bestaande rekening uit te geven, bepaal de plaats van de rekening die u wilt uitgeven, dan selecteren [!UICONTROL **details**] knoop uitgeven.

   [!UICONTROL **voegt de vertoningen van de rekening**] dialoog toe.

1. Geef de volgende informatie op:

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

   **NOTA:** wanneer het gebruiken van Amazon S3 met de Eendelen van Gegevens en Data Warehouse, slechts wordt de encryptie SSE-S3 gesteund.

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
   | [!UICONTROL **Zeer belangrijke vault URI**] | <p>Het pad naar het SAS-token in Azure Key Vault.  Om Azure SAS te configureren, moet u een SAS-token opslaan als een geheim met Azure Key Vault. Voor informatie, zie de [ Microsoft Azure documentatie over hoe te om een geheim van Azure Key Vault ](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations) te plaatsen en terug te winnen.</p><p>Nadat de sleutelvault-URI is gemaakt, voegt u een toegangsbeleid toe op de Key Vault om toestemming te verlenen aan de Azure-toepassing die u hebt gemaakt. Voor informatie, zie [ Microsoft Azure documentatie over hoe te om een Zeer belangrijk de toegangsbeleid van de Vault toe te wijzen ](https://learn.microsoft.com/en-us/azure/key-vault/general/assign-access-policy?tabs=azure-portal).</p> |
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
   >De e-mailrekeningen kunnen slechts met [ Data Warehouse ](/help/export/data-warehouse/create-request/dw-request-report-destinations.md) worden gebruikt. (De e-mailrekeningen worden niet gesteund met [ de Reeksen van de Diervoeders van Gegevens ](/help/export/analytics-data-feed/create-feed.md) of [ Indeling ](/help/components/classifications/sets/overview.md)).

   Geef de volgende informatie op om een Azure RBAC-account te configureren:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Ontvangers**] | E-mailmeldingen kunnen naar specifieke gebruikers worden verzonden wanneer het rapport wordt verzonden. Geef één e-mailadres of een lijst met e-mailadressen door komma&#39;s gescheiden op. |

   {style="table-layout:auto"}

   +++

   **Verouderde rekeningstypes**

   Deze types van erfenisrekening zijn beschikbaar slechts wanneer het uitvoeren van gegevens met [ de Eigen van Gegevens ](/help/export/analytics-data-feed/create-feed.md) en [ Data Warehouse ](/help/export/data-warehouse/create-request/t-dw-create-request.md). Deze opties zijn niet beschikbaar wanneer het invoeren van gegevens met [ de reeksen van de Classificatie ](/help/components/classifications/sets/manage/schema.md).

   +++FTP

   Gegevens over gegevenstoevoer kunnen worden geleverd aan een door de Adobe of de klant gehoste FTP-locatie. Vereist een FTP-host, gebruikersnaam en wachtwoord. Gebruik het padveld om feed-bestanden in een map te plaatsen. Mappen moeten al bestaan; feeds genereren een fout als het opgegeven pad niet bestaat.

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Gastheer**] | Voer de gewenste FTP-doel-URL in. Bijvoorbeeld `ftp.adobe.com` . |
   | [!UICONTROL **Weg**] | Kan leeg blijven. |
   | [!UICONTROL **Gebruikersnaam**] | Voer de gebruikersnaam in die u wilt aanmelden bij de FTP-site. |
   | [!UICONTROL **Wachtwoord en bevestig wachtwoord**] | Voer het wachtwoord in om u aan te melden bij de FTP-site. |

   {style="table-layout:auto"}

   +++

   +++SFTP

   SFTP-ondersteuning voor gegevensfeeds is beschikbaar. Vereist een gastheer SFTP, gebruikersbenaming, en de bestemmingsplaats om een geldige RSA of DSA openbare sleutel te bevatten. U kunt de juiste openbare sleutel downloaden wanneer u de feed maakt.

   +++

   +++S3

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

   +++

   +++Azure Blob

   Het pakhuis van gegevens steunt de bestemmingen van Azure Blob. Hiervoor is een container, account en sleutel vereist. Amazon versleutelt de gegevens automatisch in rust. Wanneer u de gegevens downloadt, worden deze automatisch gedecodeerd. Zie [ een opslagrekening ](https://docs.microsoft.com/en-us/azure/storage/common/storage-quickstart-create-account?tabs=azure-portal#view-and-copy-storage-access-keys) binnen Microsoft Azure documenten voor meer informatie creëren.

   >[!NOTE]
   >
   >U moet uw eigen proces uitvoeren om schijfruimte op de bestemming van het gegevenspakhuis te beheren. Adobe verwijdert geen gegevens van de server.

   +++

1. Selecteer [!UICONTROL **sparen**].

1. Ga met [ verder vormen wolkeninvoer en uitvoerplaatsen ](/help/components/locations/configure-import-locations.md).
