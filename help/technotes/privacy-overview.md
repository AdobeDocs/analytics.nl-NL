---
description: Overzicht van de data die Adobe Analytics verzamelt en andere privacyoverwegingen.
keywords: privacy
title: Privacyoverzicht
feature: Privacy
exl-id: 71c83106-a047-47d7-9a70-4a24595e3d0a
source-git-commit: 04f8602ccfa7fd2d1d2f3c56f477aeee3739c563
workflow-type: tm+mt
source-wordcount: '962'
ht-degree: 1%

---

# Privacyoverzicht

De Adobe wil uw organisatie toelaten zodat u de toepasselijke privacywetten en verordeningen kunt naleven. Zie [Adobe Experience Cloud-privacy](https://www.adobe.com/privacy/experience-cloud.html) voor meer informatie . Wat Adobe Analytics betreft, fungeert Adobe als een &quot;gegevensverwerker&quot; en bent u de &quot;gegevenscontroller&quot; (of een equivalent in de toepasselijke wetgeving inzake privacy en gegevensbescherming). Het is aan uw organisatie om te onthullen hoe u de producten en de diensten van de Adobe gebruikt omdat uw organisatie exclusief controleert hoe te om de oplossingen van de Adobe uit te voeren. Uw organisatie is verantwoordelijk voor het naleven van uw eigen privacybeleid, uw serviceovereenkomst met Adobe en alle toepasselijke wetten.

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
| Paginanamen of URL&#39;s van webpagina&#39;s op uw site | Altijd verzameld voor Adobe Analytics werkt. Voor elke treffer is een URL- of paginanaam vereist. | [Pagina](../components/dimensions/page.md), [Pagina-URL](../components/dimensions/page-url.md) |
| Op tijd gebaseerde gegevens | Altijd verzameld voor Adobe Analytics werkt. Een tijdstempel is vereist voor gegevensverzameling en op tijd gebaseerde gegevens worden afgeleid van de tijdstempel. | [Tijd besteed aan pagina](../components/dimensions/time-spent-on-page.md), [Uur van dag](../components/dimensions/hour-of-day.md), [AM/PM](../components/dimensions/am-pm.md), [Weekdag/Weekend](../components/dimensions/weekday-weekend.md), [Dag van de week](../components/dimensions/day-of-week.md), [Maand van jaar](../components/dimensions/month-of-year.md) |
| Gegevens van webpagina&#39;s op andere sites | Adobe kan geen gegevens verzamelen op niet-gekoppelde sites waar u de broncode van de website of app niet kunt wijzigen. Bibliotheken met gegevensverzamelingen verzamelen standaard de referentie-URL wanneer een bezoeker naar uw website komt. U kunt uw implementatie aanpassen om gegevens binnen vraagkoorden te verzamelen nadat de website of de toepassingsbezoekers aankomen. | [Referenter](../components/dimensions/referrer.md), [Verwijzen naar domein](../components/dimensions/referring-domain.md) |
| Geanimeerde id van bezoeker | Bibliotheken met gegevensverzamelingen genereren een bezoekersidentiteitskaart en verwijzen ernaar voor elke browser die uw site bezoekt. Deze id wordt opgeslagen in een cookie. Als een bibliotheek van de gegevensinzameling geen koekjes om het even welke reden kan plaatsen, gebruikt de bibliotheek een fallback methode van bezoekersidentificatie gebruikend IP adres en userAgent koord. Zie [Adobe Analytics- en browsercookies](cookies/cookies.md) voor meer informatie . | [Unieke bezoekers](../components/metrics/unique-visitors.md) |
| Identificeerbare bezoeker-id&#39;s | Adobe verzamelt niet automatisch aangepaste bezoekers-id&#39;s. U kunt uw implementatie echter aanpassen om deze gegevens te verzamelen. | [`visitorID`](../implement/vars/config-vars/visitorid.md) |
| Externe zoektermen | De externe onderzoeksgegevens omvatten sleutelwoorden die uit onderzoeksmotoren voortkomen. Bibliotheken van gegevensverzamelingen zoeken naar deze gegevens op basis van de verwijzende URL. Veel moderne zoekmachines bevatten deze informatie echter niet meer. | [Trefwoord zoeken](../components/dimensions/search-keyword.md) |
| Interne zoektermen | Interne zoekgegevens bevatten trefwoorden die afkomstig zijn van uw website of de zoekmogelijkheden van de app. Adobe verzamelt niet automatisch interne zoekgegevens. U kunt uw implementatie echter aanpassen om deze gegevens te verzamelen. Dit geldt ook voor organisaties die Adobe Analytics gebruiken. | [eVar](../components/dimensions/evar.md) |
| Computer- en browserspecificaties | AppMeasurement verzamelt automatisch lage entropiebrowserhints, zoals het browsertype, het type van het besturingssysteem en als het apparaat desktopcomputers of mobiele apparaten is. Aangepaste configuratie is vereist voor het verzamelen van hoge entropiehints, zoals de specifieke versie/build van de browser, het apparaatmodel of de versie van het besturingssysteem. Zie [Overzicht van tips voor klanten](client-hints.md) voor meer informatie . | [Browser](../components/dimensions/browser.md), [Besturingssysteem](../components/dimensions/operating-systems.md), [Mobiele afmetingen](../components/dimensions/mobile-dimensions.md), [Monitorresolutie](../components/dimensions/monitor-resolution.md) |
| Geolocatie-informatie | Met Adobe kunt u het verzamelen van gegevens over de geolocatie voor elke website of toepassing (op rapportniveau) in- of uitschakelen. Geolocatiegegevensverzameling is standaard ingeschakeld. De bibliotheken van de gegevensinzameling omvatten geolocation als het wordt toegelaten. | [Plaatsen](../components/dimensions/cities.md), [Regio&#39;s](../components/dimensions/regions.md), [Landen](../components/dimensions/countries.md) |
| IP-adres | De Adobe biedt de capaciteit aan om het laatste octet te verduisteren of volledig het IP van de bezoeker adres te verduisteren wanneer het opslaan van deze gegevens. EMEA-klanten hebben doorgaans het IP-adres dat standaard volledig verduisterd is. Ongeacht obfuscatie het plaatsen, IP is het adres niet beschikbaar als afmeting in Adobe Analytics; het is slechts inbegrepen in [Gegevensfeeds](../export/analytics-data-feed/data-feed-overview.md). | Geen |
| Formuliergegevens op uw site | Alle implementatietypen vereisen configuratie om deze gegevens te verzamelen. U kunt deze gegevens opnemen in aangepaste variabelen. | [eVar](../components/dimensions/evar.md) |
| Op advertenties of koppelingen op uw site klikken | Wordt standaard verzameld met een bibliotheek voor gegevensverzameling. Aanvullende informatie, zoals de locatie van klikken, is beschikbaar wanneer u Activity Map inschakelt. | [Activity Map](../analyze/activity-map/activity-map.md), [Koppeling afsluiten](../components/dimensions/exit-link.md), [Koppeling downloaden](../components/dimensions/download-link.md) |
| Producten aangeschaft op uw site | Alle implementatietypen vereisen configuratie om deze gegevens te verzamelen. Adobe biedt verschillende standaardvariabelen om deze informatie te verzamelen. | [Product](../components/dimensions/product.md), [Orders](../components/metrics/orders.md), [Ontvangsten](../components/metrics/revenue.md) |

{style="table-layout:auto"}

Zie het navigatiemenu onder [Overzicht van Dimensionen](../components/dimensions/overview.md) en [Overzicht van statistieken](../components/metrics/overview.md) voor meer variabelen waarop de Adobe gegevens kan verzamelen.

## Gegevensverwerkingslocaties

Adobe onderhoudt drie gegevensverwerkingslocaties voor Adobe Analytics. Deze sites ontvangen onbewerkte gegevens en verwerken deze in een rapportsuite die is geoptimaliseerd voor gegevensopslag en het ophalen van rapporten. Deze gegevensverwerkingslocaties bevinden zich in **Oregon**, **Londen**, en **Singapore**. Zie [Adobe Analytics-beveiligingsoverzicht](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adb-analytics-security-wp.pdf) voor meer informatie .
