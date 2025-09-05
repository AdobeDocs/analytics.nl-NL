---
description: Overzicht van de data die Adobe Analytics verzamelt en andere privacyoverwegingen.
keywords: privacy
title: Privacyoverzicht
feature: Data Governance
exl-id: 71c83106-a047-47d7-9a70-4a24595e3d0a
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '977'
ht-degree: 1%

---

# Privacyoverzicht

Adobe wil uw organisatie inschakelen zodat u zich aan de toepasselijke wetten en regels kunt houden. Zie [ privacy van Adobe Experience Cloud ](https://www.adobe.com/privacy/experience-cloud.html){target=_blank} voor meer informatie. Tussen Adobe Analytics en uw organisatie werkt Adobe als een &#39;gegevensverwerker&#39; en u bent de &#39;gegevenscontroller&#39; (of een equivalent in de toepasselijke wetten op het gebied van privacy en gegevensbescherming). Het is aan uw organisatie om openbaar te maken hoe u de producten en de diensten van Adobe gebruikt omdat uw organisatie exclusief controleert hoe te om de oplossingen van Adobe uit te voeren. Tijdens het gebruik van Adobe Analytics is uw organisatie verantwoordelijk voor het naleven van uw eigen privacybeleid, uw serviceovereenkomst met Adobe en alle toepasselijke wetten.

Adobe beveelt ten zeerste aan de volgende overkoepelende concepten te volgen:

* **als u persoonlijke gegevens verzamelt, zorg ervoor dat u privacywetten en verordeningen naleeft.** Met aangepaste variabelen kunt u vrijwel alles verzamelen waartoe u toegang hebt. U moet echter ook rekening houden met het privacybeleid van uw organisatie en de toepasselijke wetten.
* **verstrekken gemakkelijk-aan-vinden en gemakkelijk-aan-begrijpelijke privacyinformatie voor uw organisatie aan uw klanten.** Tot de nuttige informatie behoren de koppelingen om te weigeren, de manier waarop de bijbehorende gegevens worden gebruikt en de manier waarop u Adobe-services gebruikt of wilt gebruiken.
* **ben zich bewust van zowel lokale wetten als internationale wetten die op u van toepassing zijn.** Als uw organisatie op wereldwijde schaal werkt, kunnen enkele internationale wetten van toepassing zijn.

## Uitsplitsing gegevensverzameling

Adobe biedt meerdere bibliotheken voor gegevensverzameling om gegevens naar Adobe te verzenden. De opmerkelijke voorbeelden omvatten:

* **AppMeasurement**: Een bibliotheek die wordt ontworpen om gegevens rechtstreeks naar Adobe Analytics te verzenden.
* **SDK van het Web**: Een bibliotheek die wordt ontworpen om gegevens naar het netwerk van Adobe Experience Platform te verzenden Edge, dat dan die gegevens aan Adobe Analytics door:sturen.
* **Markeringen**: Een web-based UI die u toestaat om uw implementatie te vormen zonder toegang tot een website of de broncode van de app voorbij de aanvankelijke markeringsimplementatie te vereisen. Extensies zijn beschikbaar voor zowel AppMeasurement als Web SDK.

Adobe Analytics kan de volgende gegevenstypen verzamelen:

| Type gegevens | Details | Voorbeeldvariabelen met deze gegevens |
| --- | --- | --- |
| Paginanamen of URL&#39;s van webpagina&#39;s op uw site | Adobe Analytics kan deze gegevens alleen gebruiken. Voor elke treffer is een URL- of paginanaam vereist. | [ Pagina ](/help/components/dimensions/page.md), [ Pagina URL ](/help/components/dimensions/page-url.md) |
| Op tijd gebaseerde gegevens | Adobe Analytics kan deze gegevens alleen gebruiken. Een tijdstempel is vereist voor gegevensverzameling en op tijd gebaseerde gegevens worden afgeleid van de tijdstempel. | [ Tijd besteed aan pagina ](/help/components/dimensions/time-spent-on-page.md), [ Uur van dag ](/help/components/dimensions/hour-of-day.md), [ AM/PM ](/help/components/dimensions/am-pm.md), [ Weekdag/Weekend ](/help/components/dimensions/weekday-weekend.md), [ Dag van week ](/help/components/dimensions/day-of-week.md), [ Maand van jaar ](/help/components/dimensions/month-of-year.md) |
| Referergegevens | Bibliotheken met gegevensverzamelingen verzamelen standaard de referentie-URL wanneer een bezoeker naar uw website komt. U kunt uw implementatie aanpassen om gegevens binnen het vraagkoord van een verwijzer te verzamelen. Deze praktijk komt vaak voor bij campagnes en het bijhouden en uitvoeren van prestaties. | [ Referrer ](/help/components/dimensions/referrer.md), [ Verwijzend domein ](/help/components/dimensions/referring-domain.md) |
| Geanimeerde id van bezoeker | Bibliotheken met gegevensverzamelingen genereren een bezoekersidentiteitskaart en verwijzen ernaar voor elke browser die uw site bezoekt. Deze id wordt opgeslagen in een cookie. Als een bibliotheek met gegevensverzamelingen geen cookie-id kan instellen, gebruikt de bibliotheek een fallback-methode voor anonieme bezoekersidentificatie. Deze methode impliceert het binden van verwante hits aan het zelfde bezoek gebruikend het IP van de bezoeker adres en het koord van de gebruikersagent. Als uw organisatie IP toegelaten verduistering heeft, wordt dit het plaatsen geëerd. Zie [ Adobe Analytics en browser koekjes ](../cookies/cookies.md) voor meer informatie. | [ Unieke bezoekers ](/help/components/metrics/unique-visitors.md) |
| Identificeerbare bezoeker-id&#39;s | Adobe verzamelt niet automatisch aangepaste bezoeker-id&#39;s. U kunt uw implementatie echter aanpassen om deze gegevens te verzamelen. | [`visitorID`](/help/implement/vars/config-vars/visitorid.md) |
| Externe zoektermen | De externe onderzoeksgegevens omvatten sleutelwoorden die uit onderzoeksmotoren voortkomen. Bibliotheken van gegevensverzamelingen zoeken naar deze gegevens op basis van de verwijzende URL. Veel moderne zoekmachines bevatten deze informatie echter niet meer. | [ sleutelwoord van het Onderzoek ](/help/components/dimensions/search-keyword.md) |
| Interne zoektermen | Interne zoekgegevens bevatten trefwoorden die afkomstig zijn van uw website of de zoekmogelijkheden van de app. Adobe verzamelt niet automatisch interne zoekgegevens. U kunt uw implementatie echter aanpassen om deze gegevens te verzamelen. Dit geldt ook voor organisaties die Adobe Analytics gebruiken. | [eVar](/help/components/dimensions/evar.md) |
| Computer- en browserspecificaties | De bibliotheken van de gegevensinzameling verzamelen automatisch lage entropiebrowser wenken, zoals het browser type, werkend systeemtype, en als het apparaat Desktop of mobiel is. Aangepaste configuratie is vereist voor het verzamelen van hoge entropiehints, zoals de specifieke versie/build van de browser, het apparaatmodel of de versie van het besturingssysteem. Zie [ overzicht van de wenken van de Cliënt ](../client-hints.md) voor meer informatie. | [ Browser ](/help/components/dimensions/browser.md), [ Werkend systeem ](/help/components/dimensions/operating-systems.md), [ Mobiele afmetingen ](/help/components/dimensions/mobile-dimensions.md), [ resolutie van de Monitor ](/help/components/dimensions/monitor-resolution.md) |
| Geolocatie-informatie | Adobe biedt de capaciteit aan om gedetailleerde geoplaats te verhinderen door het laatste octet van een IP adres aan 0 te plaatsen. Dit maakt geo informatie minder nauwkeurig en kan in [ montages van de rapportreeks ](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md) worden geplaatst. | [ Steden ](/help/components/dimensions/cities.md), [ Gebieden ](/help/components/dimensions/regions.md), [ Landen ](/help/components/dimensions/countries.md) |
| IP-adres | Adobe biedt de mogelijkheid om het IP-adres van de bezoeker tijdens het opslaan van deze gegevens te verduisteren (hash) of volledig te verwijderen. EMEA-klanten hebben doorgaans de IP-adresinstelling die standaard verduisterd is. Ongeacht obfuscatie het plaatsen, IP is het adres niet beschikbaar als afmeting in Analysis Workspace; het is slechts inbegrepen in [ voer van Gegevens ](/help/export/analytics-data-feed/data-feed-overview.md). Zie [ Algemene rekeningsmontages ](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md) in de gids Admin voor details rond beschikbare verduisteringsmontages. | Geen |
| Formuliergegevens op uw site | Alle implementatietypen vereisen configuratie om deze gegevens te verzamelen. U kunt deze gegevens opnemen in aangepaste variabelen. | [eVar](/help/components/dimensions/evar.md) |
| Op advertenties of koppelingen op uw site klikken | Wordt verzameld als [`trackExternalLinks`](/help/implement/vars/config-vars/trackexternallinks.md) of [`trackDownloadLinks`](/help/implement/vars/config-vars/trackdownloadlinks.md) is ingeschakeld. Aanvullende informatie, zoals de locatie van klikken, is beschikbaar wanneer u Activity Map inschakelt. | [ Activity Map ](/help/analyze/activity-map/overview.md), [ Verbinding van de Uitgang ](/help/components/dimensions/exit-link.md), [ Verbinding van de Download ](/help/components/dimensions/download-link.md) |
| Producten aangeschaft op uw site | Alle implementatietypen vereisen configuratie om deze gegevens te verzamelen. Adobe biedt verschillende standaardvariabelen om deze informatie te verzamelen. | [ Product ](/help/components/dimensions/product.md), [ Orders ](/help/components/metrics/orders.md), [ Ontvangsten ](/help/components/metrics/revenue.md) |

{style="table-layout:auto"}

Zie het navigatiemenu onder [ Overzicht van Dimensies ](/help/components/dimensions/overview.md) en [ Overzicht van Metriek ](/help/components/metrics/overview.md) voor meer variabelen die Adobe gegevens onder kan potentieel verzamelen.

## Gegevensverwerkingslocaties

Adobe onderhoudt drie gegevensverwerkingslocaties voor Adobe Analytics. Deze sites ontvangen onbewerkte gegevens en verwerken deze in een rapportsuite die is geoptimaliseerd voor gegevensopslag en het ophalen van rapporten. Deze gegevensverwerkingslocaties bevinden zich momenteel in de Verenigde Staten (Oregon), het Verenigd Koninkrijk (Londen) en Singapore. Zie [ de veiligheidsoverzicht van Adobe Analytics ](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adb-analytics-security-wp.pdf){target=_blank} voor meer informatie.
