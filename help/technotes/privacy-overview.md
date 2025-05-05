---
description: Overzicht van de data die Adobe Analytics verzamelt en andere privacyoverwegingen.
keywords: privacy
title: Privacyoverzicht
feature: Privacy
exl-id: 71c83106-a047-47d7-9a70-4a24595e3d0a
source-git-commit: f0d12c4a9462b6a8c5ba47944854164bb4f0d908
workflow-type: tm+mt
source-wordcount: '978'
ht-degree: 1%

---

# Privacyoverzicht

De Adobe wil uw organisatie toelaten zodat u aan toepasselijke wetten en verordeningen kunt voldoen. Zie [ privacy van Adobe Experience Cloud ](https://www.adobe.com/privacy/experience-cloud.html){target=_blank}  voor meer informatie. Tussen Adobe Analytics en uw organisatie fungeert Adobe als een &#39;gegevensverwerker&#39; en u bent de &#39;gegevenscontroller&#39; (of een equivalent in de toepasselijke wetten op het gebied van privacy en gegevensbescherming). Het is aan uw organisatie om te onthullen hoe u de producten en de diensten van de Adobe gebruikt omdat uw organisatie exclusief controleert hoe te om de oplossingen van de Adobe uit te voeren. Tijdens het gebruik van Adobe Analytics is uw organisatie verantwoordelijk voor het naleven van uw eigen privacybeleid, uw serviceovereenkomst met Adobe en alle toepasselijke wetten.

Adobe beveelt ten zeerste aan de volgende overkoepelende concepten te volgen:

* **als u persoonlijke gegevens verzamelt, zorg ervoor dat u privacywetten en verordeningen naleeft.** Met aangepaste variabelen kunt u vrijwel alles verzamelen waartoe u toegang hebt. U moet echter ook rekening houden met het privacybeleid van uw organisatie en de toepasselijke wetten.
* **verstrekken gemakkelijk-aan-vinden en gemakkelijk-aan-begrijpelijke privacyinformatie voor uw organisatie aan uw klanten.** De nuttige informatie omvat opt-out verbindingen, hoe hun het doorbladeren gegevens worden gebruikt, en hoe u gebruikt of van plan bent om de diensten van de Adobe te gebruiken.
* **ben zich bewust van zowel lokale wetten als internationale wetten die op u van toepassing zijn.** Als uw organisatie op wereldwijde schaal werkt, kunnen enkele internationale wetten van toepassing zijn.

## Uitsplitsing gegevensverzameling

De Adobe biedt veelvoudige bibliotheken van de gegevensinzameling aan om in het verzenden van gegevens naar Adobe bij te staan. De opmerkelijke voorbeelden omvatten:

* **AppMeasurement**: Een bibliotheek die wordt ontworpen om gegevens rechtstreeks naar Adobe Analytics te verzenden.
* **SDK van het Web**: Een bibliotheek die wordt ontworpen om gegevens naar het netwerk van Adobe Experience Platform Edge te verzenden, dat dan die gegevens aan Adobe Analytics door:sturen.
* **Markeringen**: Een web-based UI die u toestaat om uw implementatie te vormen zonder toegang tot een website of de broncode van de app voorbij de aanvankelijke markeringsimplementatie te vereisen. De uitbreidingen zijn beschikbaar voor zowel AppMeasurement als Web SDK.

Adobe Analytics kan de volgende gegevenstypen verzamelen:

| Type gegevens | Details | Voorbeeldvariabelen met deze gegevens |
| --- | --- | --- |
| Paginanamen of URL&#39;s van webpagina&#39;s op uw site | Adobe Analytics kan deze gegevens alleen gebruiken. Voor elke treffer is een URL- of paginanaam vereist. | [ Pagina ](../components/dimensions/page.md), [ Pagina URL ](../components/dimensions/page-url.md) |
| Op tijd gebaseerde gegevens | Adobe Analytics kan deze gegevens alleen gebruiken. Een tijdstempel is vereist voor gegevensverzameling en op tijd gebaseerde gegevens worden afgeleid van de tijdstempel. | [ Tijd besteed aan pagina ](../components/dimensions/time-spent-on-page.md), [ Uur van dag ](../components/dimensions/hour-of-day.md), [ AM/PM ](../components/dimensions/am-pm.md), [ Weekdag/Weekend ](../components/dimensions/weekday-weekend.md), [ Dag van week ](../components/dimensions/day-of-week.md), [ Maand van jaar ](../components/dimensions/month-of-year.md) |
| Referergegevens | Bibliotheken met gegevensverzamelingen verzamelen standaard de referentie-URL wanneer een bezoeker naar uw website komt. U kunt uw implementatie aanpassen om gegevens binnen het vraagkoord van een verwijzer te verzamelen. Deze praktijk komt vaak voor bij campagnes en het bijhouden en uitvoeren van prestaties. | [ Referrer ](../components/dimensions/referrer.md), [ Verwijzend domein ](../components/dimensions/referring-domain.md) |
| Geanimeerde id van bezoeker | Bibliotheken met gegevensverzamelingen genereren een bezoekersidentiteitskaart en verwijzen ernaar voor elke browser die uw site bezoekt. Deze id wordt opgeslagen in een cookie. Als een bibliotheek met gegevensverzamelingen geen cookie-id kan instellen, gebruikt de bibliotheek een fallback-methode voor anonieme bezoekersidentificatie. Deze methode impliceert het binden van verwante hits aan het zelfde bezoek gebruikend het IP van de bezoeker adres en het koord van de gebruikersagent. Als uw organisatie IP toegelaten verduistering heeft, wordt dit het plaatsen geëerd. Zie [ Adobe Analytics en browser koekjes ](cookies/cookies.md) voor meer informatie. | [ Unieke bezoekers ](../components/metrics/unique-visitors.md) |
| Identificeerbare bezoeker-id&#39;s | Adobe verzamelt niet automatisch aangepaste bezoeker-id&#39;s. U kunt uw implementatie echter aanpassen om deze gegevens te verzamelen. | [`visitorID`](../implement/vars/config-vars/visitorid.md) |
| Externe zoektermen | De externe onderzoeksgegevens omvatten sleutelwoorden die uit onderzoeksmotoren voortkomen. Bibliotheken van gegevensverzamelingen zoeken naar deze gegevens op basis van de verwijzende URL. Veel moderne zoekmachines bevatten deze informatie echter niet meer. | [ sleutelwoord van het Onderzoek ](../components/dimensions/search-keyword.md) |
| Interne zoektermen | Interne zoekgegevens bevatten trefwoorden die afkomstig zijn van uw website of de zoekmogelijkheden van de app. Adobe verzamelt niet automatisch interne zoekgegevens. U kunt uw implementatie echter aanpassen om deze gegevens te verzamelen. Dit geldt ook voor organisaties die Adobe Analytics gebruiken. | [eVar](../components/dimensions/evar.md) |
| Computer- en browserspecificaties | De bibliotheken van de gegevensinzameling verzamelen automatisch lage entropiebrowser wenken, zoals het browser type, werkend systeemtype, en als het apparaat Desktop of mobiel is. Aangepaste configuratie is vereist voor het verzamelen van hoge entropiehints, zoals de specifieke versie/build van de browser, het apparaatmodel of de versie van het besturingssysteem. Zie [ overzicht van de wenken van de Cliënt ](client-hints.md) voor meer informatie. | [ Browser ](../components/dimensions/browser.md), [ Werkend systeem ](../components/dimensions/operating-systems.md), [ Mobiele afmetingen ](../components/dimensions/mobile-dimensions.md), [ resolutie van de Monitor ](../components/dimensions/monitor-resolution.md) |
| Geolocatie-informatie | De Adobe biedt de capaciteit aan om gedetailleerde geoplaats te verhinderen door het laatste octet van een IP adres aan 0 te plaatsen. Dit maakt geo informatie minder nauwkeurig en kan in [ montages van de rapportreeks ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/general-acct-settings-admin.html) worden geplaatst. | [ Steden ](../components/dimensions/cities.md), [ Gebieden ](../components/dimensions/regions.md), [ Landen ](../components/dimensions/countries.md) |
| IP-adres | De Adobe biedt de capaciteit aan om het IP van de bezoeker adres te verduisteren (knoeiboel) of volledig te verwijderen wanneer het opslaan van deze gegevens. EMEA-klanten hebben doorgaans de IP-adresinstelling die standaard verduisterd is. Ongeacht obfuscatie het plaatsen, IP is het adres niet beschikbaar als afmeting in Analysis Workspace; het is slechts inbegrepen in [ voer van Gegevens ](../export/analytics-data-feed/data-feed-overview.md). Zie [ Algemene rekeningsmontages ](../admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md) in de gids Admin voor details rond beschikbare verduisteringsmontages. | Geen |
| Formuliergegevens op uw site | Alle implementatietypen vereisen configuratie om deze gegevens te verzamelen. U kunt deze gegevens opnemen in aangepaste variabelen. | [eVar](../components/dimensions/evar.md) |
| Op advertenties of koppelingen op uw site klikken | Wordt verzameld als [`trackExternalLinks`](../implement/vars/config-vars/trackexternallinks.md) of [`trackDownloadLinks`](../implement/vars/config-vars/trackdownloadlinks.md) is ingeschakeld. Aanvullende informatie, zoals de locatie van klikken, is beschikbaar wanneer u Activity Map inschakelt. | [ Activity Map ](../analyze/activity-map/overview.md), [ Verbinding van de Uitgang ](../components/dimensions/exit-link.md), [ Verbinding van de Download ](../components/dimensions/download-link.md) |
| Producten aangeschaft op uw site | Alle implementatietypen vereisen configuratie om deze gegevens te verzamelen. Adobe biedt verschillende standaardvariabelen om deze informatie te verzamelen. | [ Product ](../components/dimensions/product.md), [ Orders ](../components/metrics/orders.md), [ Ontvangsten ](../components/metrics/revenue.md) |

{style="table-layout:auto"}

Zie het navigatiemenu onder [ Dimensionen overzicht ](../components/dimensions/overview.md) en [ Overzicht van Metriek ](../components/metrics/overview.md) voor meer variabelen die de Adobe gegevens onder kan verzamelen.

## Gegevensverwerkingslocaties

Adobe onderhoudt drie gegevensverwerkingslocaties voor Adobe Analytics. Deze sites ontvangen onbewerkte gegevens en verwerken deze in een rapportsuite die is geoptimaliseerd voor gegevensopslag en het ophalen van rapporten. Deze gegevensverwerkingslocaties bevinden zich momenteel in de Verenigde Staten (Oregon), het Verenigd Koninkrijk (Londen) en Singapore. Zie [ de veiligheidsoverzicht van Adobe Analytics ](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adb-analytics-security-wp.pdf){target=_blank}  voor meer informatie.
