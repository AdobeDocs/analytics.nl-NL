---
title: Een gegevensfeed maken of bewerken
description: Leer hoe u een gegevensfeed maakt of bewerkt.
feature: Data Feeds
exl-id: 36c8a40e-6137-4836-9d4b-bebf17b932bc
source-git-commit: 60335be9a60b467969f5e1796ce465a7d453951f
workflow-type: tm+mt
source-wordcount: '1514'
ht-degree: 0%

---

# Een gegevensfeed maken of bewerken

Door een gegevensfeed te maken, kan Adobe weten waar Raw-gegevensbestanden moeten worden verzonden en wat u in elk bestand wilt opnemen. Deze pagina bevat een overzicht van de afzonderlijke instellingen die u kunt aanpassen bij het maken van een gegevensfeed.

Voordat u deze pagina leest, wordt u geadviseerd over basiskennis van gegevensfeeds. Zie [Overzicht van gegevensfeeds](data-feed-overview.md) om ervoor te zorgen dat u voldoet aan de vereisten voor het maken van een gegevensfeed.

## Diervoederinformatievelden

* **Naam**: De naam van de gegevensinvoer. Moet uniek zijn binnen de geselecteerde rapportreeks, en kan tot 255 karakters in lengte zijn.
* **Rapportsuite:** De rapportsuite waarop de gegevensinvoer is gebaseerd. Als de veelvoudige gegevensvoer voor de zelfde rapportreeks wordt gecreeerd, moeten zij verschillende kolomdefinities hebben. Alleen bronrapporten ondersteunen gegevensfeeds; virtuele rapportsuites worden niet ondersteund.
* **E-mail indien voltooid**: Het e-mailadres dat moet worden gemeld wanneer een feed de verwerking heeft voltooid. Het e-mailadres moet correct zijn opgemaakt.
* **Feed-interval**: Uurfeeds bevatten gegevens van één uur. Dagelijkse diervoeders bevatten gegevens over een hele dag; zij omvatten gegevens van middernacht tot middernacht in de tijdzone van de rapportreeks.
* **Vertraging bij verwerking**: Wacht een bepaalde hoeveelheid tijd alvorens een dossier van de gegevensvoer te verwerken. Een vertraging kan handig zijn om mobiele implementaties de mogelijkheid te geven om offlineapparaten online te komen en gegevens te verzenden. Het kan ook worden gebruikt om de server-zijprocessen van uw organisatie in het beheren van eerder verwerkte dossiers aan te passen. In de meeste gevallen is geen uitstel nodig. Een diervoeder kan maximaal 120 minuten worden uitgesteld.
* **Begin- en einddatum**: De begindatum geeft de eerste datum aan waarop u gegevens wilt invoeren. Stel deze datum in het verleden in om onmiddellijk te beginnen met het verwerken van gegevensfeeds voor historische gegevens. De feeds worden verder verwerkt tot de einddatum. De begin en einddata zijn gebaseerd op de tijdzone van de rapportreeks.
* **Doorlopende diervoeders**: Dit selectievakje verwijdert de einddatum, zodat een feed voor onbepaalde tijd kan worden uitgevoerd. Als een feed de verwerking van historische gegevens heeft voltooid, wacht een feed tot de gegevens een bepaald uur of een bepaalde dag zijn verzameld. Zodra het huidige uur of de dag eindigt, begint de verwerking na de gespecificeerde vertraging.

## Doelveld

De velden die beschikbaar zijn onder doelvelden, zijn afhankelijk van het doeltype.

### Google Cloud Platform

Toegang tot GCP-opslagemmers als veilige bestemming

**Velden**
* *Type:* Doeltype van Google Cloud-Platform
* *Project-id:* GCP-project-id waar het opslagsegment bestaat
* *Naam opslagemmertje:* Emmernamen zonder punten zijn beperkt tot 3-63 tekens. Namen die stippen bevatten, kunnen maximaal 222 tekens bevatten, maar elk onderdeel met een punt als scheidingsteken mag niet langer zijn dan 63 tekens.
* *Pad (optioneel):* &amp; *ID rapportsuite toevoegen aan pad:* Locatie van bronnen die moeten worden opgehaald of opgeslagen

![GCP-info](assets/dest-gcp.png)

**Proces voor het maken van serviceaccounts**

De gebruiker moet een serviceaccount maken voor de bestemming Google Cloud-Platform.

Per analytische organisatie wordt slechts één GCP-serviceaccount toegestaan. Zodra de de dienstrekening voor datafeed is gecreeerd, zullen alle extra datafeeds binnen de organisatie met de de dienstrekening vooraf bevolkt worden.

![GCP-serviceaccountgegevens](assets/service-account.png)


### Amazon S3

Amazon S3 bucket-opslag toegankelijk via IAM-rol binnen een vertrouwde entiteit.

**Velden**

* *Type:* Doeltype van Amazon S3
* *Emmertje:* S3 Emmernaam
* *Vertrouwde entiteit ARN:* AWS IAM Entiteit ARN `arn:aws:iam::<12 digit account number>:user/<username>`
* *Rol ARN:* AWS IAM Role ARN `arn:aws:iam::<12 digit account number>:role/<role name>`
* *Pad (optioneel):* &amp; *ID rapportsuite toevoegen aan pad:* Locatie van bronnen die moeten worden opgehaald of opgeslagen
* *Gebied opgeven (optioneel):* Vervolgkeuzelijst van alle beschikbare AWS-regio&#39;s, met inbegrip van de GN-regio&#39;s

![Amazon S3 info](assets/dest-s3-secure.png)


**Vertrouwde entiteit maken en selecteren**

De gebruiker kan een vertrouwde entiteit selecteren uit de opties in het vervolgkeuzemenu of een nieuwe entiteit maken en ophalen door op de knop `Create Entity` knop.

Na klikken op de knop `Create Entity` wordt de gebruiker omgeleid naar een verificatieproces. Zodra de gebruiker verifieert, wordt de vertrouwde op entiteit gecreeerd en aan de opties in dropdown toegevoegd.

In het vervolgkeuzemenu worden alle vertrouwde entiteiten weergegeven die door deze gebruiker in de organisatie zijn gemaakt.

![Entiteitsgegevens](assets/entity-creation.png)

U kunt feeds rechtstreeks naar Amazon S3 buckets verzenden via de oude methode. Zie [Amazon S3-vereisten voor emmernaamgeving](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-s3-bucket-naming-requirements.html) in de Amazon S3-documenten voor meer informatie.

**Velden - Vervangen**

* *Type:* Doeltype van vervangen S3 methode
* *Emmertje:* Amazon S3 Emmernaam
* *Pad (optioneel):* &amp; *ID rapportsuite toevoegen aan pad:* Locatie van bronnen die moeten worden opgehaald of opgeslagen
* *Toegangstoets:* Toegangstoets-id van AWS-gebruiker
* *Geheime sleutel:* Geheime sleutel van AWS-gebruiker
* *Geheime sleutel bevestigen:* Geheime sleutel van AWS-gebruiker opnieuw invoeren

![S3-info](assets/dest-s3-dpr.png)

De gebruiker die u opgeeft voor het uploaden van gegevensfeeds, moet het volgende hebben [machtigingen](https://docs.aws.amazon.com/AmazonS3/latest/API/API_Operations_Amazon_Simple_Storage_Service.html):

* s3:GetObject
* s3:PutObject
* s3:PutObjectAcl

Voor elke upload naar een Amazon S3 emmertje, [!DNL Analytics] voegt de emmereigenaar aan BucketOwnerFullControl ACL toe, al dan niet het emmertje een beleid heeft dat het vereist. Zie voor meer informatie &quot;[Wat is de instelling BucketOwnerFullControl voor Amazon S3-gegevensfeeds?](df-faq.md#BucketOwnerFullControl)&quot;

**Ondersteunde AWS-regio&#39;s**:
* us-East-2
* us-East-1
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
* cn-North-1
* cn-northwest-1


### Azure Blob

Azure Blob Secure destination using Role-Based Access Control (RBAC) or Shared Access Signature (SAS). Wanneer u het toegangsbeheer kiest, wordt de inhoud van het deelvenster bijgewerkt met de bijbehorende velden.

**Velden - RBAC**
* *Type:* Doeltype van Azure Blob
* *Toegangsbeheer:* Optie om RBAC of SAS te gebruiken
* *Active Directory Tenant ID:* Organisatie-id van Azure-account
* *Toepassings-id:* Toepassings-id van Active Directory-adapter
* *Clientgeheim:* Azure Client Secret
* *Naam opslagaccount:* Naam van account dat gegevensobjecten bevat
* *Containernaam:* Container die tot een bepaalde opslagrekening behoort.
* *Pad (optioneel):* &amp; *ID rapportsuite toevoegen aan pad:* Locatie van bronnen die moeten worden opgehaald of opgeslagen

![Azure RBAC-info](assets/dest-azure-rbac.png)

**Velden - SAS**
* *Type:* Doeltype van Azure Blob
* *Toegangsbeheer:* Optie om RBAC of SAS te gebruiken
* *Active Directory Tenant ID:* ID van Azure Active Directory-instantie
* *Toepassings-id:* Toepassings-id van Active Directory-adapter
* *Clientgeheim:* Azure Client Secret
* *Sleutelvault-URI:* Locatie van Azure Key Vault
* *Sleutelvaultgeheime naam:* Geheime naam voor toegang tot beveiligde sleutelvault
* *Pad (optioneel):* &amp; *ID rapportsuite toevoegen aan pad:* Locatie van bronnen die moeten worden opgehaald of opgeslagen

![Azure SAS-info](assets/dest-azure-sas.png)

**Velden - Vervangen**
* *Type:* Doeltype van Azure Blob
* *Container:* Naam van de Azure-container
* *Pad (optioneel):* &amp; *ID rapportsuite toevoegen aan pad:* Locatie van bronnen die moeten worden opgehaald of opgeslagen
* *Account:* Azure-accountgeheim
* *Sleutelvault-URI:* Locatie van Azure Key Vault
* *Sleutelvaultgeheime naam:* Geheime naam voor toegang tot beveiligde sleutelvault

U moet uw eigen proces uitvoeren om schijfruimte op de voederbestemming te beheren. Adobe verwijdert geen gegevens van de server.
Zie [Een opslagaccount maken](https://docs.microsoft.com/en-us/azure/storage/common/storage-quickstart-create-account?tabs=azure-portal#view-and-copy-storage-access-keys) in de Microsoft Azure-documenten voor meer informatie.

![Azure Vervangen info](assets/dest-azure-dpr.png)

>[!NOTE]
>
>U moet uw eigen proces uitvoeren om schijfruimte op de voederbestemming te beheren. Adobe verwijdert geen gegevens van de server.

### FTP - Vervangen

**Velden**
* *Type:* Doeltype van FTP
* *Host:* Eindpunt voor toegang tot host
* *Pad (optioneel):* &amp; *ID rapportsuite toevoegen aan pad:* Locatie van bronnen die moeten worden opgehaald of opgeslagen
* *Gebruikersnaam:* Gebruikersnaam voor host
* *Wachtwoord:* Wachtwoord voor host
* *Wachtwoord bevestigen:* Wachtwoord voor host opnieuw invoeren en verifiëren

![FTP-info](assets/dest-ftp-dpr.png)

### SFTP - Vervangen

SFTP-ondersteuning voor gegevensfeeds is beschikbaar. Vereist een gastheer SFTP, gebruikersbenaming, en de bestemmingsplaats om een geldige RSA of DSA openbare sleutel te bevatten. U kunt de juiste openbare sleutel downloaden wanneer u de feed maakt.

**Velden**
* *Type:* Doeltype van SFTP
* *Host:* Eindpunt voor toegang tot host
* *Pad (optioneel):* &amp; *ID rapportsuite toevoegen aan pad:* Locatie van bronnen die moeten worden opgehaald of opgeslagen
* *Openbare RSA-sleutel:* of *Openbare DSA-sleutel:* Openbare sleutel voor toegang tot host

![SFTP-informatie](assets/dest-sftp-dpr.png)

## Definities gegevenskolom

Alle kolommen zijn beschikbaar, ongeacht of ze gegevens bevatten. Een gegevensfeed moet ten minste één kolom bevatten.

* **Te verwijderen tekens verwijderen**: Bij het verzamelen van gegevens kunnen sommige tekens (zoals nieuwe regels) problemen veroorzaken. Schakel dit selectievakje in als u deze tekens uit feed-bestanden wilt verwijderen.
* **Compressie-indeling**: Het type compressie dat wordt gebruikt. Gzip-uitvoerbestanden in `.tar.gz` gebruiken. Bestanden overslaan in `.zip` gebruiken.
* **Verpakkingstype**: Eén bestand levert de uitvoer van `hit_data.tsv` bestand in één, mogelijk enorm bestand. Met meerdere bestanden worden uw gegevens gepagineerd in 2 GB blokken (ongecomprimeerd). Als er meerdere bestanden zijn geselecteerd en de niet-gecomprimeerde gegevens voor het rapportagevenster kleiner zijn dan 2 GB, wordt er één bestand verzonden. Adobe raadt u aan voor de meeste gegevensfeeds meerdere bestanden te gebruiken.
* **Manifest**: Of Adobe een [manifestbestand](c-df-contents/datafeeds-contents.md#feed-manifest) naar de bestemming wanneer geen gegevens voor een voederinterval worden verzameld. Als u Manifest File selecteert, ontvangt u een manifestbestand dat lijkt op het volgende wanneer geen gegevens worden verzameld:

```text
   Datafeed-Manifest-Version: 1.0
    Lookup-Files: 0
    Data-Files: 0
    Total-Records: 0
```

* **Kolomsjablonen**: Adobe raadt u aan een kolomsjabloon te maken wanneer u veel gegevensfeeds maakt. Als u een kolomsjabloon selecteert, worden automatisch de opgegeven kolommen in de sjabloon opgenomen. Adobe biedt standaard ook diverse sjablonen.
* **Beschikbare kolommen**: Alle beschikbare gegevenskolommen in Adobe Analytics. Klikken [!UICONTROL Add all] om alle kolommen in een gegevenstoevoer op te nemen.
* **Opgenomen kolommen**: De kolommen die in een gegevensfeed moeten worden opgenomen. Klikken [!UICONTROL Remove all] om alle kolommen uit een gegevensvoer te verwijderen.
* **CSV downloaden**: Hiermee wordt een CSV-bestand gedownload dat alle kolommen bevat.
