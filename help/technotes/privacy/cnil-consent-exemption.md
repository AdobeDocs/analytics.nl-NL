---
description: Leer meer over de richtlijnen en aanbevelingen voor de toestemming van gebruikers om niet-essentiële cookies op apparaten of browsers op te slaan of te lezen.
title: Wat zijn de CNIL-richtlijnen voor toestemming van de gebruiker en cookies
feature: Data Governance
role: Admin
exl-id: 04179e58-dbba-45e2-ba57-7fe5fdedc483
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 0%

---

# Vrijstelling van CNIL-toestemming

Op 1 oktober 2020 publiceerde de Franse autoriteit voor gegevensbescherming (de &quot;CNIL&quot;) een herziene versie van haar cookie Guidelines (de &quot;Guidelines&quot;) en haar slotaanbevelingen om gebruikers toestemming te geven niet-essentiële cookies en soortgelijke technologieën op gebruikersapparatuur of browsers op te slaan of te lezen (de &quot;Aanbevelingen&quot;).

De richtsnoeren voorzien in een beperkte vrijstelling van de toestemmingsvereiste (&quot;Vrijstelling van toestemming&quot;). De vrijstelling van toestemming is van toepassing op analytische cookies waarvan het doel beperkt is tot het meten van het publiek van de site of de app alleen namens de webuitgever. In de richtsnoeren is bepaald dat de vrijstelling van toestemming alleen van toepassing is als aan de volgende voorwaarden is voldaan:

* 25 maanden maximale gegevensretentie.  U kunt de huidige instellingen voor gegevensbehoud bekijken onder [!UICONTROL Analytics] > [!UICONTROL Admin] > [!UICONTROL Data Governance] .  [ Behoud van Gegevens ](/help/technotes/data-retention.md)
* Cookies van derden uitschakelen in ECID. [ disableThirdPartyCalls ](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/configurations/disablethirdpartycalls.html#id-service-api), [ disableThirdPartyCookies ](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/configurations/disable-cookies.html#id-service-api), en [ disableIdSyncs ](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/configurations/disableidsync.html#id-service-api)
* Cookie limit van 13 maanden.  U kunt de vervaldatum van het analytische cookie overschrijven met de variabele `cookieLifetime` . Experience Cloud cookies, inclusief Analytics en ECID, verlengen de vervaldatum van de cookie met elk bezoek.  Als u een statische, niet-schuivende vervaldatum voor een cookie wilt instellen, kunt u: (1) aangepaste code schrijven om een datum in te stellen waarop de cookie moet worden verwijderd, of (2) uw CMP gebruiken om de datum van de reset van het cookie te bepalen.   [ cookieLifetime ](/help/implement/vars/config-vars/cookielifetime.md) en [ de Cookies van Experience Cloud ](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-privacy.html#ec-cookies)
* Beperkte reikwijdte. Het bereik van de cookie moet beperkt zijn tot één site of toepassing. [ Browser Cookies ](/help/technotes/cookies/cookies.md#third-party-cookie-limitations)
* Anonymiisatie. Anonymize het laatste octet van het IP Adres. [ Algemene Montages van de Rekening ](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md)
* ID bezoeker verbergen in rapportage.  De bezoeker-id&#39;s zijn standaard niet zichtbaar in Adobe Workspace en Adobe Reports and Analytics.  Bezoeker-id&#39;s zijn beschikbaar in Gegevensfeeds en Data Warehouse.  De toegang tot de Diervoeders van Gegevens en Data Warehouse kan door [ Toestemmingen van de Toegang in Admin Console ](https://experienceleague.adobe.com/docs/core-services/interface/administration/admin-getting-started.html) worden beperkt en [ de Verwijzing van de Kolom van de Diervoeders van Gegevens ](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md)
* Geolocatie-parameters. Geolocatie kan niet preciezer zijn dan het niveau van de postcode. [ Optie van het Zip ](/help/implement/vars/page-vars/zip.md) en [ Algemene de Montages van de Rekening ](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md)
* Stel opties voor aanmelden in.  Met de aanmeldingsservice kunt u bezoekersprotocollen instellen om te bepalen of u een cookie op het apparaat of de browser van de gebruiker kunt instellen wanneer u uw site bezoekt. [ Opt-In Dienst ](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/optin-overview.html)
* Gegevensdeling voorkomen.  Om gegevens uit te sluiten die aan Adobe Audience Manager delen, gebruik de `opt.dmp` contextvariabele voor [ de Rapportering van de Privacy ](/help/admin/tools/manage-rs/edit-settings/privacy-reporting.md) aan blokklappen worden gedeeld.
* Toegang tot en verwijderbaarheid. Gebruik de Privacy Service voor toegang en verwijder verzoeken. [ Analytics &amp; Privacy Service ](gdpr.md)

## Aanvullende overwegingen voor gegevensverzameling

De volgende aanvullende overwegingen zijn van toepassing:

* Adobe Analytics exploiteert datacentra in de Verenigde Staten, het Verenigd Koninkrijk en Singapore om alle klanten flexibiliteit te bieden bij het verzamelen, verwerken en opslaan van hun gegevens op regionaal niveau. Bij het configureren van de eerste configuratie van Adobe Analytics kunnen klanten hun gewenste locatie voor het datacenter selecteren. De gegevens van klanten worden uiteindelijk opgeslagen binnen hun geselecteerde gebied voor het core Analytics product.
* Overweeg de opt-in status in een variabele Analytics te verzamelen om opted-in gegevens van opted-out gegevens voor segmentatie, virtuele rapportreeksen te scheiden, of aan route aan afzonderlijke eindpunten.
* Geen meting buiten de site of de toepassing zonder voorafgaande toestemming, bijvoorbeeld geen offsite campagnes, e-mailcampagnes of iFrames.
* Het verzamelen van persoonsgegevens in variabelen is niet toegestaan zonder toestemming. [ de Activiteiten die van de Controle Experience Cloud op de Toestemming van de Gebruiker worden gebaseerd ](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/use-opt-in-to-control-experience-cloud-activities-based-on-user-consent.html#implementing-opt-in-on-the-page)
* Gegevens mogen alleen worden gebruikt om anonieme statistieken te produceren, zonder combinatie met andere gegevens.
* Gegevens worden niet gebruikt voor kruisverwijzingsacties.
* GPS-geolocatiegegevens worden niet verzameld.
* Wanneer de eindgebruiker toestemming heeft gegeven, kunnen de bovengenoemde montages worden gewijzigd en de beperkingen worden versoepeld.

>[!IMPORTANT]
>
>Dit document is niet bedoeld als juridisch of regelgevend advies en vormt geen garantie of contractuele verbintenis van Adobe. Wij moedigen klanten aan om onafhankelijk juridisch advies in te winnen over de wettelijke en regelgevende verplichtingen van klanten met betrekking tot kwesties die met dit onderwerp verband houden.

Voor meer informatie, zie de [ website van de Vrijstelling van het Koekje 0&rbrace; CNIL.](https://www.cnil.fr/en/sheet-ndeg16-use-analytics-your-websites-and-applications)
