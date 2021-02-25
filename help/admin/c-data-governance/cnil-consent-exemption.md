---
description: Leer meer over de richtlijnen en aanbevelingen voor de toestemming van gebruikers om niet-essentiële cookies op apparaten of browsers op te slaan of te lezen.
title: Wat zijn de CNIL-richtlijnen voor toestemming van de gebruiker en cookies
translation-type: tm+mt
source-git-commit: c5ebc92622e012699d64c27701b24a88429e9f4f
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 0%

---


# Vrijstelling van CNIL-toestemming

Op 1 oktober 2020 publiceerde de Franse autoriteit voor gegevensbescherming (de &quot;CNIL&quot;) een herziene versie van haar cookie Guidelines (de &quot;Guidelines&quot;) en haar slotaanbevelingen om gebruikers toestemming te geven niet-essentiële cookies en soortgelijke technologieën op gebruikersapparatuur of browsers op te slaan of te lezen (de &quot;Recommendations&quot;).

De richtsnoeren voorzien in een beperkte vrijstelling van de toestemmingsvereiste (&quot;Vrijstelling van toestemming&quot;). De vrijstelling van toestemming is van toepassing op analytische cookies waarvan het doel beperkt is tot het meten van het publiek van de site of de app alleen namens de webuitgever. In de richtsnoeren is bepaald dat de vrijstelling van toestemming alleen van toepassing is als aan de volgende voorwaarden is voldaan:

* 25 maanden maximale gegevensretentie.  U kunt de huidige instellingen voor gegevensbehoud bekijken via Analytics > Admin > Data Governance.  [Gegevens bewaren](https://experienceleague.adobe.com/docs/analytics/technotes/data-retention.html)
* Cookiegrens van 13 maanden.  U kunt de vervaldatum van het analytische cookie overschrijven met de variabele `cookieLifetime`.  [cookieLifetime](https://experienceleague.adobe.com/docs/analytics/implementation/vars/config-vars/cookielifetime.html)
* Beperkte reikwijdte. Het bereik van de cookie moet beperkt zijn tot één site of toepassing. [Browsercookies](https://experienceleague.adobe.com/docs/analytics/technotes/cookies.html?lang=en&quot;\l&quot;third-party-cookie-implementations)
* Anonymiisatie. Anonymize het laatste octet van het IP Adres. [Algemene accountinstellingen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/general-acct-settings-admin.html)
* ID bezoeker verbergen in rapportage.  De bezoeker-id&#39;s zijn standaard niet zichtbaar in Adobe Workspace en Adobe Reports and Analytics.  Bezoeker-id&#39;s zijn beschikbaar in Gegevensfeeds en Data Warehouse.  Toegang tot gegevensfeeds en Data Warehouse kan worden beperkt door [Toegangsmachtigingen in Admin Console](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html?lang=en&quot;\l&quot;task_040673FE3E3E429B9531FBCB8B6A4391)
* Geolocatie-parameters. Geolocatie kan niet preciezer zijn dan het niveau van de postcode. [Zip-](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/zip.html?lang=en&quot;\l&quot;zip-in-adobe-experience-platform-launch) opties en  [algemene accountinstellingen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/general-acct-settings-admin.html?lang=en&quot;\l&quot;admin-tools)
* Stel opties voor aanmelden in.  Met de Inschakelen-service kunt u bezoekersprotocollen instellen om te bepalen of u een cookie op het apparaat of de browser van de gebruiker kunt instellen wanneer u uw site bezoekt. [Inschakelen van service](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/optin-overview.html)
* Gegevensdeling voorkomen.  Als u gegevensdeling naar Adobe Audience Manager wilt uitsluiten, gebruikt u de contextvariabele `opt.dmp` voor [Privacy Reporting](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/consent-variables.html?lang=en&quot;\l&quot;variables) om te voorkomen dat hits worden gedeeld.
* Toegang tot en verwijderbaarheid. Gebruik de Privacy Service voor toegang en schrap verzoeken. [Analyse en Privacy Service](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/an-gdpr-overview.html)

## Aanvullende overwegingen voor gegevensverzameling

De volgende aanvullende overwegingen zijn van toepassing:

* Geen meting buiten de site of de toepassing zonder voorafgaande toestemming, bijvoorbeeld geen offsite campagnes, e-mailcampagnes of iFrames.
* Het verzamelen van persoonsgegevens in variabelen is niet toegestaan zonder toestemming.
* Gegevens mogen alleen worden gebruikt om anonieme statistieken te produceren, zonder combinatie met andere gegevens.
* Gegevens worden niet gebruikt voor kruisverwijzingsacties.
* GPS-geolocatiegegevens worden niet verzameld.

Zie de website [CNIL Cookie Exemption](https://www.cnil.fr/en/sheet-ndeg16-use-analytics-your-websites-and-applications) voor meer informatie.
