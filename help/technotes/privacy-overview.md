---
description: Overzicht van de data die Adobe Analytics verzamelt en andere privacyoverwegingen.
keywords: privacy
title: Privacyoverzicht
feature: Privacy
exl-id: 71c83106-a047-47d7-9a70-4a24595e3d0a
source-git-commit: ee0bf5beeac3c9780eb0c8420845114f7e840aec
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 11%

---

# Privacyoverzicht

Bezoekers kunnen in het [Adobe Privacy Center](https://www.adobe.com/nl/privacy.html) meer informatie vinden over de manier waarop Adobe de verzamelde data doorgaans gebruikt. Het is aan uw organisatie om bekend te maken hoe u de producten en services van Adobe gebruikt, omdat uw organisatie uitsluitend zelf bepaalt hoe de services van Adobe worden geïmplementeerd. Uw organisatie is verantwoordelijk voor het naleven van uw eigen privacybeleid, uw serviceovereenkomst met Adobe en alle toepasselijke wetten.

Adobe beveelt ten zeerste aan de volgende overkoepelende concepten in acht te nemen:

* **Vermijd het verzamelen van persoonlijk identificeerbare gegevens in Adobe Analytics.** Met aangepaste variabelen kunt u vrijwel alles verzamelen waartoe u toegang hebt. U moet echter ook rekening houden met het privacybeleid van uw organisatie en de toepasselijke wetten.
* **Bezoekers gemakkelijk te vinden en gemakkelijk te begrijpen informatie over opt-out-informatie bieden.** Laat ze toe om zich te onthouden van alles wat niet strikt noodzakelijk is. De meeste landen in de Europese Unie achten analytische cookies niet strikt noodzakelijk.

## Uitsplitsing gegevensverzameling

Adobe Analytics verzamelt automatisch de volgende gegevenstypen of kan deze potentieel verzamelen:

| Type gegevens | Details | Voorbeeldvariabelen met deze gegevens |
| --- | --- | --- |
| Paginanamen of URL&#39;s van webpagina&#39;s op uw site | Altijd verzameld. Voor elke treffer is een URL- of paginanaam vereist. | [Pagina](../components/dimensions/page.md), [Pagina-URL](../components/dimensions/page-url.md) |
| Op tijd gebaseerde gegevens | Altijd verzameld. Tijdstempel is vereist voor gegevensverzameling en op tijd gebaseerde gegevens worden afgeleid van de tijdstempel. | [Tijd besteed aan pagina](../components/dimensions/time-spent-on-page.md), [Uur van dag](../components/dimensions/hour-of-day.md), [AM/PM](../components/dimensions/am-pm.md), [Weekdag/Weekend](../components/dimensions/weekday-weekend.md), [Dag van de week](../components/dimensions/day-of-week.md), [Maand van jaar](../components/dimensions/month-of-year.md) |
| Gegevens van webpagina&#39;s op andere sites | Adobe kan geen gegevens verzamelen op niet-aangesloten sites waar u de broncode van de website niet kunt wijzigen. AppMeasurement verzamelt automatisch de verwijzende URL wanneer een bezoeker naar uw website komt. U kunt uw implementatie aanpassen om gegevens binnen vraagkoorden te verzamelen nadat zij op uw plaats aankomen. | [Referenter](../components/dimensions/referrer.md), [Verwijzen naar domein](../components/dimensions/referring-domain.md) |
| Geanimeerde id van bezoeker | AppMeasurement genereert automatisch een bezoeker-id en verwijst ernaar voor elke browser die uw site bezoekt. Deze id wordt opgeslagen in een cookie. Als er voor een bepaalde implementatie geen cookies beschikbaar zijn, gebruikt Adobe Analytics een fallback-methode voor bezoekersidentificatie met IP-adres en een userAgent-tekenreeks. Zie [Adobe Analytics- en browsercookies](cookies/cookies.md) voor meer informatie . | [Unieke bezoekers](../components/metrics/unique-visitors.md) |
| Identificeerbare bezoeker-id&#39;s | Adobe verzamelt niet automatisch aangepaste gebruikers-id&#39;s van bezoekers. U kunt uw implementatie echter aanpassen om deze gegevens te verzamelen. | [`visitorID`](../implement/vars/config-vars/visitorid.md) |
| Externe zoektermen | AppMeasurement probeert deze gegevens automatisch te verzamelen op basis van de verwijzende URL. Veel moderne zoekmachines bevatten deze informatie echter niet meer. | [Trefwoord zoeken](../components/dimensions/search-keyword.md) |
| Interne zoektermen | Adobe verzamelt niet automatisch interne zoekgegevens. U kunt uw implementatie echter aanpassen om deze gegevens te verzamelen. Dit is een gebruikelijke praktijk voor organisaties die Adobe Analytics gebruiken. | [eVar](../components/dimensions/evar.md) |
| Computer- en browserspecificaties | AppMeasurement verzamelt automatisch lage entropiebrowserhints, zoals het browsertype, het type van het besturingssysteem en als het apparaat desktopcomputers of mobiele apparaten is. De configuratie wordt vereist om hoge entropiewenken, zoals de browser specifieke versie/bouwstijl, het apparatenmodel, of de versie van het werkende systeem te verzamelen. Zie [Overzicht van tips voor klanten](client-hints.md) voor meer informatie . | [Browser](../components/dimensions/browser.md), [Besturingssysteem](../components/dimensions/operating-systems.md), [Mobiele afmetingen](../components/dimensions/mobile-dimensions.md), [Monitorresolutie](../components/dimensions/monitor-resolution.md) |
| Geolocatie-informatie | Adobe biedt de mogelijkheid om het verzamelen van geolocatiegegevens voor elke website of app (op rapportniveau) in of uit te schakelen. Deze gegevens worden automatisch verzameld bij veel implementatietypen, waaronder AppMeasurement. | [Plaatsen](../components/dimensions/cities.md), [Regio&#39;s](../components/dimensions/regions.md), [Landen](../components/dimensions/countries.md) |
| IP-adres | Adobe biedt de capaciteit aan om het laatste octet te bedekken of volledig het IP van de bezoeker adres te bedekken wanneer het opslaan van deze gegevens. EMEA-klanten hebben doorgaans een IP-adres dat standaard volledig verborgen is. IP adres is niet beschikbaar als afmeting in Adobe Analytics; het is slechts inbegrepen in ruwe gegevens ([Gegevensfeeds](../export/analytics-data-feed/data-feed-overview.md)). | Geen |
| Formuliergegevens op uw site | Alle implementatietypen vereisen configuratie om deze gegevens te verzamelen. U kunt deze gegevens opnemen in aangepaste variabelen. | [eVar](../components/dimensions/evar.md) |
| Advertenties of koppelingen waarop op uw site is geklikt | Automatisch verzamelen bij gebruik van AppMeasurement. Aanvullende informatie, zoals de locatie van klikken, is beschikbaar als Activity Map is ingeschakeld. | [Activity Map](../analyze/activity-map/activity-map.md), [Koppeling afsluiten](../components/dimensions/exit-link.md), [Koppeling downloaden](../components/dimensions/download-link.md) |
| Producten aangeschaft op uw site | Alle implementatietypen vereisen configuratie om deze gegevens te verzamelen. Adobe biedt diverse standaardvariabelen aan om deze informatie op te slaan. | [Product](../components/dimensions/product.md), [Orders](../components/metrics/orders.md), [Ontvangsten](../components/metrics/revenue.md) |

{style="table-layout:auto"}

Zie het navigatiemenu onder [Overzicht van Dimension](../components/dimensions/overview.md) en [Overzicht van statistieken](../components/metrics/overview.md) voor meer variabelen waarop Adobe mogelijk gegevens kan verzamelen.
