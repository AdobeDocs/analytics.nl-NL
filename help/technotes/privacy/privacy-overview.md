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

Adobe wil uw organisatie inschakelen zodat u zich aan de toepasselijke wetten en regels kunt houden. Zie [&#x200B; privacy van Adobe Experience Cloud &#x200B;](https://www.adobe.com/privacy/experience-cloud.html){target=_blank} voor meer informatie. Tussen Adobe Analytics en uw organisatie werkt Adobe als een &#39;gegevensverwerker&#39; en u bent de &#39;gegevenscontroller&#39; (of een equivalent in de toepasselijke wetten op het gebied van privacy en gegevensbescherming). Het is aan uw organisatie om openbaar te maken hoe u de producten en de diensten van Adobe gebruikt omdat uw organisatie exclusief controleert hoe te om de oplossingen van Adobe uit te voeren. Tijdens het gebruik van Adobe Analytics is uw organisatie verantwoordelijk voor het naleven van uw eigen privacybeleid, uw serviceovereenkomst met Adobe en alle toepasselijke wetten.

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
| Paginanamen of URL&#39;s van webpagina&#39;s op uw site | Adobe Analytics kan deze gegevens alleen gebruiken. Voor elke treffer is een URL- of paginanaam vereist. | [&#x200B; Pagina &#x200B;](/help/components/dimensions/page.md), [&#x200B; Pagina URL &#x200B;](/help/components/dimensions/page-url.md) |
| Op tijd gebaseerde gegevens | Adobe Analytics kan deze gegevens alleen gebruiken. Een tijdstempel is vereist voor gegevensverzameling en op tijd gebaseerde gegevens worden afgeleid van de tijdstempel. | [&#x200B; Tijd besteed aan pagina &#x200B;](/help/components/dimensions/time-spent-on-page.md), [&#x200B; Uur van dag &#x200B;](/help/components/dimensions/hour-of-day.md), [&#x200B; AM/PM &#x200B;](/help/components/dimensions/am-pm.md), [&#x200B; Weekdag/Weekend &#x200B;](/help/components/dimensions/weekday-weekend.md), [&#x200B; Dag van week &#x200B;](/help/components/dimensions/day-of-week.md), [&#x200B; Maand van jaar &#x200B;](/help/components/dimensions/month-of-year.md) |
| Referergegevens | Bibliotheken met gegevensverzamelingen verzamelen standaard de referentie-URL wanneer een bezoeker naar uw website komt. U kunt uw implementatie aanpassen om gegevens binnen het vraagkoord van een verwijzer te verzamelen. Deze praktijk komt vaak voor bij campagnes en het bijhouden en uitvoeren van prestaties. | [&#x200B; Referrer &#x200B;](/help/components/dimensions/referrer.md), [&#x200B; Verwijzend domein &#x200B;](/help/components/dimensions/referring-domain.md) |
| Geanimeerde id van bezoeker | Bibliotheken met gegevensverzamelingen genereren een bezoekersidentiteitskaart en verwijzen ernaar voor elke browser die uw site bezoekt. Deze id wordt opgeslagen in een cookie. Als een bibliotheek met gegevensverzamelingen geen cookie-id kan instellen, gebruikt de bibliotheek een fallback-methode voor anonieme bezoekersidentificatie. Deze methode impliceert het binden van verwante hits aan het zelfde bezoek gebruikend het IP van de bezoeker adres en het koord van de gebruikersagent. Als uw organisatie IP toegelaten verduistering heeft, wordt dit het plaatsen geëerd. Zie [&#x200B; Adobe Analytics en browser koekjes &#x200B;](../cookies/cookies.md) voor meer informatie. | [&#x200B; Unieke bezoekers &#x200B;](/help/components/metrics/unique-visitors.md) |
| Identificeerbare bezoeker-id&#39;s | Adobe verzamelt niet automatisch aangepaste bezoeker-id&#39;s. U kunt uw implementatie echter aanpassen om deze gegevens te verzamelen. | [`visitorID`](/help/implement/vars/config-vars/visitorid.md) |
| Externe zoektermen | De externe onderzoeksgegevens omvatten sleutelwoorden die uit onderzoeksmotoren voortkomen. Bibliotheken van gegevensverzamelingen zoeken naar deze gegevens op basis van de verwijzende URL. Veel moderne zoekmachines bevatten deze informatie echter niet meer. | [&#x200B; sleutelwoord van het Onderzoek &#x200B;](/help/components/dimensions/search-keyword.md) |
| Interne zoektermen | Interne zoekgegevens bevatten trefwoorden die afkomstig zijn van uw website of de zoekmogelijkheden van de app. Adobe verzamelt niet automatisch interne zoekgegevens. U kunt uw implementatie echter aanpassen om deze gegevens te verzamelen. Dit geldt ook voor organisaties die Adobe Analytics gebruiken. | [eVar](/help/components/dimensions/evar.md) |
| Computer- en browserspecificaties | De bibliotheken van de gegevensinzameling verzamelen automatisch lage entropiebrowser wenken, zoals het browser type, werkend systeemtype, en als het apparaat Desktop of mobiel is. Aangepaste configuratie is vereist voor het verzamelen van hoge entropiehints, zoals de specifieke versie/build van de browser, het apparaatmodel of de versie van het besturingssysteem. Zie [&#x200B; overzicht van de wenken van de Cliënt &#x200B;](../client-hints.md) voor meer informatie. | [&#x200B; Browser &#x200B;](/help/components/dimensions/browser.md), [&#x200B; Werkend systeem &#x200B;](/help/components/dimensions/operating-systems.md), [&#x200B; Mobiele afmetingen &#x200B;](/help/components/dimensions/mobile-dimensions.md), [&#x200B; resolutie van de Monitor &#x200B;](/help/components/dimensions/monitor-resolution.md) |
| Geolocatie-informatie | Adobe biedt de capaciteit aan om gedetailleerde geoplaats te verhinderen door het laatste octet van een IP adres aan 0 te plaatsen. Dit maakt geo informatie minder nauwkeurig en kan in [&#x200B; montages van de rapportreeks &#x200B;](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md) worden geplaatst. | [&#x200B; Steden &#x200B;](/help/components/dimensions/cities.md), [&#x200B; Gebieden &#x200B;](/help/components/dimensions/regions.md), [&#x200B; Landen &#x200B;](/help/components/dimensions/countries.md) |
| IP-adres | Adobe biedt de mogelijkheid om het IP-adres van de bezoeker tijdens het opslaan van deze gegevens te verduisteren (hash) of volledig te verwijderen. EMEA-klanten hebben doorgaans de IP-adresinstelling die standaard verduisterd is. Ongeacht obfuscatie het plaatsen, IP is het adres niet beschikbaar als afmeting in Analysis Workspace; het is slechts inbegrepen in [&#x200B; voer van Gegevens &#x200B;](/help/export/analytics-data-feed/data-feed-overview.md). Zie [&#x200B; Algemene rekeningsmontages &#x200B;](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md) in de gids Admin voor details rond beschikbare verduisteringsmontages. | Geen |
| Formuliergegevens op uw site | Alle implementatietypen vereisen configuratie om deze gegevens te verzamelen. U kunt deze gegevens opnemen in aangepaste variabelen. | [eVar](/help/components/dimensions/evar.md) |
| Op advertenties of koppelingen op uw site klikken | Wordt verzameld als [`trackExternalLinks`](/help/implement/vars/config-vars/trackexternallinks.md) of [`trackDownloadLinks`](/help/implement/vars/config-vars/trackdownloadlinks.md) is ingeschakeld. Aanvullende informatie, zoals de locatie van klikken, is beschikbaar wanneer u Activity Map inschakelt. | [&#x200B; Activity Map &#x200B;](/help/analyze/activity-map/overview.md), [&#x200B; Verbinding van de Uitgang &#x200B;](/help/components/dimensions/exit-link.md), [&#x200B; Verbinding van de Download &#x200B;](/help/components/dimensions/download-link.md) |
| Producten aangeschaft op uw site | Alle implementatietypen vereisen configuratie om deze gegevens te verzamelen. Adobe biedt verschillende standaardvariabelen om deze informatie te verzamelen. | [&#x200B; Product &#x200B;](/help/components/dimensions/product.md), [&#x200B; Orders &#x200B;](/help/components/metrics/orders.md), [&#x200B; Ontvangsten &#x200B;](/help/components/metrics/revenue.md) |

{style="table-layout:auto"}

Zie het navigatiemenu onder [&#x200B; Overzicht van Dimensies &#x200B;](/help/components/dimensions/overview.md) en [&#x200B; Overzicht van Metriek &#x200B;](/help/components/metrics/overview.md) voor meer variabelen die Adobe gegevens onder kan potentieel verzamelen.

## Gegevensverwerkingslocaties

Adobe onderhoudt drie gegevensverwerkingslocaties voor Adobe Analytics. Deze sites ontvangen onbewerkte gegevens en verwerken deze in een rapportsuite die is geoptimaliseerd voor gegevensopslag en het ophalen van rapporten. Deze gegevensverwerkingslocaties bevinden zich momenteel in de Verenigde Staten (Oregon), het Verenigd Koninkrijk (Londen) en Singapore. Zie [&#x200B; de veiligheidsoverzicht van Adobe Analytics &#x200B;](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adb-analytics-security-wp.pdf){target=_blank} voor meer informatie.
