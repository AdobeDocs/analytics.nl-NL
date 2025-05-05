---
description: Leer meer over de richtlijnen en aanbevelingen voor de toestemming van gebruikers om niet-essentiële cookies op apparaten of browsers op te slaan of te lezen.
title: Wat zijn de CNIL-richtlijnen voor toestemming van de gebruiker en cookies
feature: Data Governance
role: Admin
exl-id: 04179e58-dbba-45e2-ba57-7fe5fdedc483
source-git-commit: 43c39b99cbae3e714b7f017dec14dd02fa350790
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# Vrijstelling van CNIL-toestemming

Op 1 oktober 2020 publiceerde de Franse autoriteit voor gegevensbescherming (de &quot;CNIL&quot;) een herziene versie van haar cookie Guidelines (de &quot;Guidelines&quot;) en haar slotaanbevelingen om gebruikers toestemming te geven niet-essentiële cookies en soortgelijke technologieën op gebruikersapparatuur of browsers op te slaan of te lezen (de &quot;Recommendations&quot;).

De richtsnoeren voorzien in een beperkte vrijstelling van de toestemmingsvereiste (&quot;Vrijstelling van toestemming&quot;). De vrijstelling van toestemming is van toepassing op analytische cookies waarvan het doel beperkt is tot het meten van het publiek van de site of de app alleen namens de webuitgever. In de richtsnoeren is bepaald dat de vrijstelling van toestemming alleen van toepassing is als aan de volgende voorwaarden is voldaan:

* 25 maanden maximale gegevensretentie.  U kunt de huidige instellingen voor gegevensbehoud onder [!UICONTROL Analytics] > [!UICONTROL Admin] > [!UICONTROL Data Governance].  [Gegevens bewaren](https://experienceleague.adobe.com/docs/analytics/technotes/data-retention.html?lang=nl-NL)
* Cookies van derden uitschakelen in ECID. [disableThirdPartyCalls](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/configurations/disablethirdpartycalls.html?lang=nl-NL#id-service-api), [disableThirdPartyCookies](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/configurations/disable-cookies.html?lang=nl-NL#id-service-api), en [disableIdSyncs](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/configurations/disableidsync.html?lang=nl-NL#id-service-api)
* Cookie limit van 13 maanden.  U kunt de vervaldatum van het cookie voor de analysemogelijkheden overschrijven met de opdracht `cookieLifetime` variabele. Cookies in Experiencen Cloud, waaronder Analytics en ECID, verlengen de vervaldatum van de cookie met elk bezoek.  Als u een statische, niet-schuivende vervaldatum voor een cookie wilt instellen, kunt u: (1) aangepaste code schrijven om een datum in te stellen waarop de cookie moet worden verwijderd, of (2) uw CMP gebruiken om de datum van de reset van het cookie te bepalen.   [cookieLifetime](https://experienceleague.adobe.com/docs/analytics/implementation/vars/config-vars/cookielifetime.html?lang=nl-NL) en [Experience Cloud Cookies](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-privacy.html?lang=nl-NL#ec-cookies)
* Beperkte reikwijdte. Het bereik van de cookie moet beperkt zijn tot één site of toepassing. [Browsercookies](https://experienceleague.adobe.com/docs/analytics/technotes/cookies/cookies.html?lang=nl-NL#third-party-cookie-limitations)
* Anonymiisatie. Anonymize het laatste octet van het IP Adres. [Algemene accountinstellingen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md)
* ID bezoeker verbergen in rapportage.  De bezoeker-id&#39;s zijn standaard niet zichtbaar in de Adobe-werkruimte en de Adobe-Reports and Analytics.  Bezoeker-id&#39;s zijn beschikbaar in Gegevensfeeds en Data Warehouse.  De toegang tot gegevensfeeds en Data Warehouse kan worden beperkt door [Toegangsmachtigingen in Admin Console](https://experienceleague.adobe.com/docs/core-services/interface/administration/admin-getting-started.html?lang=nl-NL) en [Referentie gegevensfeed-kolom](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-reference.html?lang=nl-NL#columns%2C-descriptions%2C-and-data-types)
* Geolocatie-parameters. Geolocatie kan niet preciezer zijn dan het niveau van de postcode. [Zip-optie](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/zip.html?lang=nl-NL) en [Algemene accountinstellingen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/general-acct-settings-admin.html?lang=nl-NL)
* Stel opties voor aanmelden in.  Met de aanmeldingsservice kunt u bezoekersprotocollen instellen om te bepalen of u een cookie op het apparaat of de browser van de gebruiker kunt instellen wanneer u uw site bezoekt. [Inschakelen van service](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/optin-overview.html?lang=nl-NL)
* Gegevensdeling voorkomen.  Als u gegevensdeling naar Adobe Audience Manager wilt voorkomen, gebruikt u de opdracht `opt.dmp` contextvariabele voor [Privacyrapportage](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/privacy-reporting.md) om te voorkomen dat hits worden gedeeld.
* Toegang tot en verwijderbaarheid. Gebruik de Privacy Service voor toegang en schrap verzoeken. [Analyse en Privacy Service](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/an-gdpr-overview.html?lang=nl-NL)

## Aanvullende overwegingen voor gegevensverzameling

De volgende aanvullende overwegingen zijn van toepassing:

* Adobe Analytics exploiteert datacentra in de Verenigde Staten, het Verenigd Koninkrijk en Singapore om alle klanten flexibiliteit te bieden bij het verzamelen, verwerken en opslaan van hun gegevens op regionaal niveau. Bij het configureren van de eerste configuratie van Adobe Analytics kunnen klanten hun gewenste locatie voor het datacenter selecteren. De gegevens van klanten worden uiteindelijk opgeslagen binnen hun geselecteerde gebied voor het core Analytics product.
* Overweeg de opt-in status in een variabele Analytics te verzamelen om opted-in gegevens van opted-out gegevens voor segmentatie, virtuele rapportreeksen te scheiden, of aan route aan afzonderlijke eindpunten.
* Geen meting buiten de site of de toepassing zonder voorafgaande toestemming, bijvoorbeeld geen offsite campagnes, e-mailcampagnes of iFrames.
* Het verzamelen van persoonsgegevens in variabelen is niet toegestaan zonder toestemming. [De Activiteiten van het Experience Cloud van de controle die op de Toestemming van de Gebruiker worden gebaseerd](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/use-opt-in-to-control-experience-cloud-activities-based-on-user-consent.html?lang=nl-NL#implementing-opt-in-on-the-page)
* Gegevens mogen alleen worden gebruikt om anonieme statistieken te produceren, zonder combinatie met andere gegevens.
* Gegevens worden niet gebruikt voor kruisverwijzingsacties.
* GPS-geolocatiegegevens worden niet verzameld.
* Wanneer de eindgebruiker toestemming heeft gegeven, kunnen de bovengenoemde montages worden gewijzigd en de beperkingen worden versoepeld.

>[!IMPORTANT]
>
>Dit document is niet bedoeld als juridisch of regelgevend advies en vormt geen garantie of contractuele verbintenis van de Adobe. Wij moedigen klanten aan om onafhankelijk juridisch advies in te winnen over de wettelijke en regelgevende verplichtingen van klanten met betrekking tot kwesties die met dit onderwerp verband houden.


Zie de klasse [CNIL Cookie-vrijstelling](https://www.cnil.fr/en/sheet-ndeg16-use-analytics-your-websites-and-applications) website.

