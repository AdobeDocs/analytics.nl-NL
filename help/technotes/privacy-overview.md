---
description: Overzicht van de data die Adobe Analytics verzamelt en andere privacyoverwegingen.
keywords: privacy
title: Privacyoverzicht
feature: Privacy
exl-id: 71c83106-a047-47d7-9a70-4a24595e3d0a
source-git-commit: 266c354cdc17e99d847ce57c1e6261386299a8cf
workflow-type: tm+mt
source-wordcount: '986'
ht-degree: 1%

---

# Privacyoverzicht

De Adobe wil uw organisatie toelaten zodat u aan toepasselijke wetten en verordeningen kunt voldoen. Zie [Adobe Experience Cloud-privacy](https://www.adobe.com/privacy/experience-cloud.html){target=_blank} voor meer informatie . Tussen Adobe Analytics en uw organisatie fungeert Adobe als een &#39;gegevensverwerker&#39; en u bent de &#39;gegevenscontroller&#39; (of een equivalent in de toepasselijke wetten op het gebied van privacy en gegevensbescherming). Het is aan uw organisatie om te onthullen hoe u de producten en de diensten van de Adobe gebruikt omdat uw organisatie exclusief controleert hoe te om de oplossingen van de Adobe uit te voeren. Tijdens het gebruik van Adobe Analytics is uw organisatie verantwoordelijk voor het naleven van uw eigen privacybeleid, uw serviceovereenkomst met Adobe en alle toepasselijke wetten.

Adobe beveelt ten zeerste aan de volgende overkoepelende concepten te volgen:

* **Als u persoonlijke gegevens verzamelt, moet u ervoor zorgen dat u zich houdt aan de wetten en voorschriften op het gebied van privacy.** Met aangepaste variabelen kunt u vrijwel alles verzamelen waartoe u toegang hebt. U moet echter ook rekening houden met het privacybeleid van uw organisatie en de toepasselijke wetten.
* **Uw klanten eenvoudig te vinden en gemakkelijk-aan-begrijpelijke privacyinformatie voor uw organisatie verstrekken.** De nuttige informatie omvat opt-out verbindingen, hoe hun het doorbladeren gegevens worden gebruikt, en hoe u gebruikt of van plan bent om de diensten van de Adobe te gebruiken.
* **Let op de lokale wetten en de internationale wetten die op jou van toepassing zijn.** Als uw organisatie op mondiale schaal werkt, kunnen sommige internationale wetten van toepassing zijn.

## Uitsplitsing gegevensverzameling

De Adobe biedt veelvoudige bibliotheken van de gegevensinzameling aan om in het verzenden van gegevens naar Adobe bij te staan. De opmerkelijke voorbeelden omvatten:

* **AppMeasurement**: Een bibliotheek die is ontworpen om gegevens rechtstreeks naar Adobe Analytics te verzenden.
* **Web SDK**: Een bibliotheek die is ontworpen om gegevens naar het Adobe Experience Platform Edge-netwerk te verzenden, die deze gegevens vervolgens doorstuurt naar Adobe Analytics.
* **Tags**: Een op het web gebaseerde interface waarmee u uw implementatie kunt configureren zonder dat toegang tot de broncode van een website of toepassing na de initiële tagimplementatie nodig is. De uitbreidingen zijn beschikbaar voor zowel AppMeasurement als Web SDK.

Adobe Analytics kan de volgende gegevenstypen verzamelen:

| Type gegevens | Details | Voorbeeldvariabelen met deze gegevens |
| --- | --- | --- |
| Paginanamen of URL&#39;s van webpagina&#39;s op uw site | Adobe Analytics kan deze gegevens alleen gebruiken. Voor elke treffer is een URL- of paginanaam vereist. | [Pagina](../components/dimensions/page.md), [Pagina-URL](../components/dimensions/page-url.md) |
| Op tijd gebaseerde gegevens | Adobe Analytics kan deze gegevens alleen gebruiken. Een tijdstempel is vereist voor gegevensverzameling en op tijd gebaseerde gegevens worden afgeleid van de tijdstempel. | [Tijd besteed aan pagina](../components/dimensions/time-spent-on-page.md), [Uur van dag](../components/dimensions/hour-of-day.md), [AM/PM](../components/dimensions/am-pm.md), [Weekdag/Weekend](../components/dimensions/weekday-weekend.md), [Dag van de week](../components/dimensions/day-of-week.md), [Maand van jaar](../components/dimensions/month-of-year.md) |
| Referergegevens | Bibliotheken met gegevensverzamelingen verzamelen standaard de referentie-URL wanneer een bezoeker naar uw website komt. U kunt uw implementatie aanpassen om gegevens binnen het vraagkoord van een verwijzer te verzamelen. Deze praktijk komt vaak voor bij campagnes en het bijhouden en uitvoeren van prestaties. | [Referenter](../components/dimensions/referrer.md), [Verwijzen naar domein](../components/dimensions/referring-domain.md) |
| Geanimeerde id van bezoeker | Bibliotheken met gegevensverzamelingen genereren een bezoekersidentiteitskaart en verwijzen ernaar voor elke browser die uw site bezoekt. Deze id wordt opgeslagen in een cookie. Als een bibliotheek met gegevensverzamelingen geen cookie-id kan instellen, gebruikt de bibliotheek een fallback-methode voor anonieme bezoekersidentificatie. Deze methode impliceert het binden van verwante hits aan het zelfde bezoek gebruikend het IP van de bezoeker adres en het koord van de gebruikersagent. Als uw organisatie IP toegelaten verduistering heeft, wordt dit het plaatsen geëerd. Zie [Adobe Analytics- en browsercookies](cookies/cookies.md) voor meer informatie . | [Unieke bezoekers](../components/metrics/unique-visitors.md) |
| Identificeerbare bezoeker-id&#39;s | Adobe verzamelt niet automatisch aangepaste bezoeker-id&#39;s. U kunt uw implementatie echter aanpassen om deze gegevens te verzamelen. | [`visitorID`](../implement/vars/config-vars/visitorid.md) |
| Externe zoektermen | De externe onderzoeksgegevens omvatten sleutelwoorden die uit onderzoeksmotoren voortkomen. Bibliotheken van gegevensverzamelingen zoeken naar deze gegevens op basis van de verwijzende URL. Veel moderne zoekmachines bevatten deze informatie echter niet meer. | [Trefwoord zoeken](../components/dimensions/search-keyword.md) |
| Interne zoektermen | Interne zoekgegevens bevatten trefwoorden die afkomstig zijn van uw website of de zoekmogelijkheden van de app. Adobe verzamelt niet automatisch interne zoekgegevens. U kunt uw implementatie echter aanpassen om deze gegevens te verzamelen. Dit geldt ook voor organisaties die Adobe Analytics gebruiken. | [eVar](../components/dimensions/evar.md) |
| Computer- en browserspecificaties | De bibliotheken van de gegevensinzameling verzamelen automatisch lage entropiebrowser wenken, zoals het browser type, werkend systeemtype, en als het apparaat Desktop of mobiel is. Aangepaste configuratie is vereist voor het verzamelen van hoge entropiehints, zoals de specifieke versie/build van de browser, het apparaatmodel of de versie van het besturingssysteem. Zie [Overzicht van tips voor klanten](client-hints.md) voor meer informatie . | [Browser](../components/dimensions/browser.md), [Besturingssysteem](../components/dimensions/operating-systems.md), [Mobiele afmetingen](../components/dimensions/mobile-dimensions.md), [Monitorresolutie](../components/dimensions/monitor-resolution.md) |
| Geolocatie-informatie | Met Adobe kunt u het verzamelen van gegevens over de geolocatie voor elke website of toepassing (op rapportniveau) in- of uitschakelen. Geolocatiegegevensverzameling is standaard ingeschakeld. | [Plaatsen](../components/dimensions/cities.md), [Regio&#39;s](../components/dimensions/regions.md), [Landen](../components/dimensions/countries.md) |
| IP-adres | De Adobe biedt de capaciteit aan om het IP van de bezoeker adres te verduisteren (knoeiboel) of volledig te verwijderen wanneer het opslaan van deze gegevens. EMEA-klanten hebben doorgaans de IP-adresinstelling die standaard verduisterd is. Ongeacht obfuscatie het plaatsen, IP is het adres niet beschikbaar als afmeting in Analysis Workspace; het is slechts inbegrepen in [Gegevensfeeds](../export/analytics-data-feed/data-feed-overview.md). Zie [Algemene accountinstellingen](../admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md) in de handleiding Admin voor meer informatie over de beschikbare instellingen voor verwarring. | Geen |
| Formuliergegevens op uw site | Alle implementatietypen vereisen configuratie om deze gegevens te verzamelen. U kunt deze gegevens opnemen in aangepaste variabelen. | [eVar](../components/dimensions/evar.md) |
| Op advertenties of koppelingen op uw site klikken | Verzameld indien [`trackExternalLinks`](../implement/vars/config-vars/trackexternallinks.md) of [`trackDownloadLinks`](../implement/vars/config-vars/trackdownloadlinks.md) is ingeschakeld. Aanvullende informatie, zoals de locatie van klikken, is beschikbaar wanneer u Activity Map inschakelt. | [Activity Map](../analyze/activity-map/activity-map.md), [Koppeling afsluiten](../components/dimensions/exit-link.md), [Koppeling downloaden](../components/dimensions/download-link.md) |
| Producten aangeschaft op uw site | Alle implementatietypen vereisen configuratie om deze gegevens te verzamelen. Adobe biedt verschillende standaardvariabelen om deze informatie te verzamelen. | [Product](../components/dimensions/product.md), [Orders](../components/metrics/orders.md), [Ontvangsten](../components/metrics/revenue.md) |

{style="table-layout:auto"}

Zie het navigatiemenu onder [Overzicht van Dimensionen](../components/dimensions/overview.md) en [Overzicht van statistieken](../components/metrics/overview.md) voor meer variabelen waarop de Adobe gegevens kan verzamelen.

## Gegevensverwerkingslocaties

Adobe onderhoudt drie gegevensverwerkingslocaties voor Adobe Analytics. Deze sites ontvangen onbewerkte gegevens en verwerken deze in een rapportsuite die is geoptimaliseerd voor gegevensopslag en het ophalen van rapporten. Deze gegevensverwerkingslocaties bevinden zich momenteel in de Verenigde Staten (Oregon), het Verenigd Koninkrijk (Londen) en Singapore. Zie [Adobe Analytics-beveiligingsoverzicht](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adb-analytics-security-wp.pdf){target=_blank} voor meer informatie .
