---
description: Leer meer over de richtlijnen en aanbevelingen voor de toestemming van gebruikers om niet-essentiële cookies op apparaten of browsers op te slaan of te lezen.
title: Wat zijn de CNIL-richtlijnen voor toestemming van de gebruiker en cookies
feature: Data Governance
exl-id: 04179e58-dbba-45e2-ba57-7fe5fdedc483
source-git-commit: f6199620033af9c8e304bd0f537d4e0b052ed64d
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 0%

---

# Vrijstelling van CNIL-toestemming

Op 1 oktober 2020 publiceerde de Franse autoriteit voor gegevensbescherming (de &quot;CNIL&quot;) een herziene versie van haar cookie Guidelines (de &quot;Guidelines&quot;) en haar slotaanbevelingen om gebruikers toestemming te geven niet-essentiële cookies en soortgelijke technologieën op gebruikersapparatuur of browsers op te slaan of te lezen (de &quot;Recommendations&quot;).

De richtsnoeren voorzien in een beperkte vrijstelling van de toestemmingsvereiste (&quot;Vrijstelling van toestemming&quot;). De vrijstelling van toestemming is van toepassing op analytische cookies waarvan het doel beperkt is tot het meten van het publiek van de site of de app alleen namens de webuitgever. In de richtsnoeren is bepaald dat de vrijstelling van toestemming alleen van toepassing is als aan de volgende voorwaarden is voldaan:

* 25 maanden maximale gegevensretentie.  U kunt de huidige instellingen voor gegevensbehoud bekijken via Analytics > Admin > Data Governance.  [Gegevens bewaren](https://experienceleague.adobe.com/docs/analytics/technotes/data-retention.html)
* Cookies van derden uitschakelen in ECID. [disableThirdPartyCalls](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/configurations/disablethirdpartycalls.html?lang=en#id-service-api), [disableThirdPartyCookies](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/configurations/disable-cookies.html?lang=en#id-service-api), en [disableIdSyncs](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/configurations/disableidsync.html?lang=en#id-service-api)
* Cookiegrens van 13 maanden.  U kunt de vervaldatum van het cookie voor de analysemogelijkheden overschrijven met de opdracht `cookieLifetime` variabele. Experience Cloud cookies, inclusief Analytics en ECID, verlengen de vervaldatum van de cookie met elk bezoek.  Als u een statische, niet-schuivende verlopen van cookies wilt instellen, kunt u: (1) schrijven aangepaste code om een datum in te stellen waarop de cookie moet worden verwijderd, of (2) gebruik uw CMP om de datum van de cookie opnieuw in te stellen.   [cookieLifetime](https://experienceleague.adobe.com/docs/analytics/implementation/vars/config-vars/cookielifetime.html) en [Experience Cloud Cookies](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-privacy.html?lang=en#ec-cookies)
* Beperkte reikwijdte. Het bereik van de cookie moet beperkt zijn tot één site of toepassing. [Browsercookies](https://experienceleague.adobe.com/docs/analytics/technotes/cookies.html?lang=en&quot;\l&quot;third-party-cookie-implementations)
* Anonymiisatie. Anonymize het laatste octet van het IP Adres. [Algemene accountinstellingen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/general-acct-settings-admin.html)
* ID bezoeker verbergen in rapportage.  De bezoeker-id&#39;s zijn standaard niet zichtbaar in Adobe Workspace en Adobe Reports and Analytics.  Bezoeker-id&#39;s zijn beschikbaar in Gegevensfeeds en Data Warehouse.  De toegang tot gegevensfeeds en Data Warehouse kan worden beperkt door [Toegangsmachtigingen in Admin Console](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html?lang=en&quot;\l&quot;task_040673FE3E3E429B9531FBCB8B6A4391) en [Referentie gegevensfeed-kolom](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-reference.html?lang=en#columns%2C-descriptions%2C-and-data-types)
* Geolocatie-parameters. Geolocatie kan niet preciezer zijn dan het niveau van de postcode. [Zip-optie](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/zip.html?lang=en&quot;\l&quot;zip-in-adobe-experience-platform-launch) en [Algemene accountinstellingen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/general-acct-settings-admin.html?lang=en&quot;\l&quot;admin-tools)
* Stel opties voor aanmelden in.  Met de Inschakelen-service kunt u bezoekersprotocollen instellen om te bepalen of u een cookie op het apparaat of de browser van de gebruiker kunt instellen wanneer u uw site bezoekt. [Inschakelen van service](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/optin-overview.html)
* Gegevensdeling voorkomen.  Als u gegevensdeling naar Adobe Audience Manager wilt voorkomen, gebruikt u de opdracht `opt.dmp` contextvariabele voor [Privacyrapportage](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/consent-variables.html?lang=en&quot;\l&quot;variables) om te voorkomen dat hits worden gedeeld.
* Toegang tot en verwijderbaarheid. Gebruik de Privacy Service voor toegang en schrap verzoeken. [Analyse en Privacy Service](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/an-gdpr-overview.html)

## Aanvullende overwegingen voor gegevensverzameling

De volgende aanvullende overwegingen zijn van toepassing:

* Overweeg de opt-in status in een variabele Analytics te verzamelen om opted-in gegevens van opted-out gegevens voor segmentatie, virtuele rapportreeksen te scheiden, of aan route aan afzonderlijke eindpunten.
* Geen meting buiten de site of de toepassing zonder voorafgaande toestemming, bijvoorbeeld geen offsite campagnes, e-mailcampagnes of iFrames.
* Het verzamelen van persoonsgegevens in variabelen is niet toegestaan zonder toestemming. [Experience Cloud-activiteiten beheren op basis van toestemming van gebruiker](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/use-opt-in-to-control-experience-cloud-activities-based-on-user-consent.html?lang=en%22%20\l%20%22implementation#implementation)
* Gegevens mogen alleen worden gebruikt om anonieme statistieken te produceren, zonder combinatie met andere gegevens.
* Gegevens worden niet gebruikt voor kruisverwijzingsacties.
* GPS-geolocatiegegevens worden niet verzameld.
* Wanneer de eindgebruiker toestemming heeft gegeven, kunnen de bovengenoemde montages worden gewijzigd en de beperkingen worden versoepeld.

Zie voor meer informatie de [CNIL Cookie-vrijstelling](https://www.cnil.fr/en/sheet-ndeg16-use-analytics-your-websites-and-applications) website.
