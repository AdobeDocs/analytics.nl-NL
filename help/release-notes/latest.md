---
title: Opmerkingen bij de release van Adobe Analytics
description: De huidige Adobe Analytics-releaseopmerkingen weergeven
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 0bd4075a15edeeccdd9db8a70a1e871f9fc5af20
workflow-type: tm+mt
source-wordcount: '663'
ht-degree: 2%

---

# Huidige Adobe Analytics-releaseopmerkingen (release april 2025)

**Laatste update**: 16 april 2025

Deze opmerkingen hebben betrekking op de vrijgaveperiode van 26 maart tot en met mei 2025. De versies van Adobe Analytics werken op a [ ononderbroken leveringsmodel ](releases.md), dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie | Beschrijving | [ Het begin van de Uitvoer ](releases.md) | [ Algemene Beschikbaarheid ](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **voorraad Analytics** | De Inventaris van de Analyse verstrekt een uitvoerig overzicht van uw milieu van Adobe Analytics, met inbegrip van het aantal projecten en componenten, rapportseries, gebruikers, en meer. Door het voorraadproces te automatiseren, kunt u snel de inspanning begrijpen nodig om van Adobe Analytics aan Customer Journey Analytics over te schakelen. Hierdoor wordt de overgang eenvoudiger en sneller. [Meer informatie](https://experienceleague.adobe.com/nl/docs/analytics/admin/admin-tools/analytics-inventory) |  | donderdag 26 maart 2025 |
| **Data Warehouse-slechts afmetingen** | Op basis van feedback van klanten hebben we besloten om deze opnieuw te evalueren. De functie Alleen automatische Data Warehouse wordt niet vrijgegeven zoals eerder is aangekondigd. | | TBD |

## Oplossingen in Adobe Analytics

**A4T**: AN-370625; AN-371279; AN-371351
**Admin Hulpmiddelen**: AN-365072; AN-371303
**Analysis Workspace**: AN-363831; AN-369554
**Classificaties**: AN-370519; AN-370727; AN-370827; AN-370941; AN-370995; AN-371377; AN-31 597; AN-371868; AN-371869; AN-372510; AN-372650; AN-373164; AN-373300; AN-373 AN-373592
**de inzameling van Gegevens**: AN-371877
**het voer van Gegevens**: AN-368676; AN-370225; AN-370514; AN-370521; AN-370687; AN-370761; 370911; AN-371047; AN-371542; AN-371627; AN-371746; AN-372708; AN-373068; AN-3 73179
**Data Warehouse**: AN-366649; AN-369817; AN-370705; AN-371127; AN-371995; AN-372596; AN-3 72940
**de Kanalen van de Marketing**: AN-372308
**Mobiele app**: AN-370287; AN-371335; AN-371374
**Platform**: AN-369510; AN-370435; AN-372150
**Report Builder**: AN-369830; AN-371395; AN-372983

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders {#admin}

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| N.v.t. |  |  |

## Aankondigingen van einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Toegang via erfenisdomeinen of via erfenisSSO** | vrijdag 10 april 2025 | Adobe is van plan om bij te werken hoe gebruikers Adobe Analytics openen om de beveiliging te verbeteren en uw aanmeldingservaring te stroomlijnen. Als deel van deze inspanning, zal de toegang via erfenisdomeinen of via erfenisSSO, met inbegrip van `my.omniture.com`, permanent worden beëindigd op **2 Januari, 2026**. Na deze datum werken de oude aanmeldingsgegevens en de oudere SSO niet meer. Alle gebruikers moeten zich via `experience.adobe.com` aanmelden met hun Adobe Experience Cloud-id&#39;s. Als u hulp met uw identiteitskaart van Experience Cloud nodig hebt, gelieve de beheerder van Adobe Analytics van uw organisatie of [ de Zorg van de Klant van Adobe ](https://helpx.adobe.com/nl/contact.html) te contacteren. |
| **Migratie aan de geloofsbrieven van Server-aan-Server van Adobe I/O OAuth** | zaterdag 17 januari 2025 | Adobe Analytics API en Livestream klanten die de geloofsbrieven van Adobe I/O JWT gebruiken moeten aan de geloofsbrieven van Adobe I/O OAuth Server-aan-Server door **30 Juni, 2025** migreren. Adobe I/O staat niet toe dat vanaf 1 mei 2024 nieuwe JWT-referenties worden gemaakt. Klanten die JWT gebruiken moeten een nieuwe Server-aan-Server referentie OAuth tot stand brengen of hun bestaande JWT-referentie migreren naar een OAuth Server-aan-Server referentie. Klanten moeten ook hun clienttoepassingen bijwerken om de nieuwe OAuth Server-to-Server referenties te kunnen gebruiken. <ul><li>[ migrerend van de Rekening van de Dienst (JWT) geloofsbrieven ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration)</li><li>[ gids van de Implementatie voor nieuwe en oude toepassingen met OAuth ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation)<li>[ Gebruikend de nieuwe Server-aan-Server geloofsbrieven OAuth ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation)</li><li>[ FAQs ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs)</li></ul> |
| **EOL voor Adobe Analytics API (versie 1.4)** | donderdag 17 juli 2024 | Op **12 augustus, 2026**, zullen de volgende Analytics Verouderde API diensten hun eind van het leven bereiken en zullen worden gesloten, en de huidige integratie die gebruikend deze diensten wordt gebouwd zal ophouden werkend:<ul><li>Adobe Analytics API (versie 1.4)</li><li>Adobe Analytics WSSE-verificatie</li></ul><p>De integratie die Adobe Analytics API (versie 1.4) gebruiken moet aan [ Adobe Analytics 2.0 API ](https://developer.adobe.com/analytics-apis/docs/2.0/) migreren, terwijl de integratie WSSE aan een op OAuth-Gebaseerd authentificatieprotocol in [ Adobe Developer Console ](https://developer.adobe.com/console) moet migreren.</p><p>Zie [ Adobe Analytics 1.4 API EOL FAQ ](/help/admin/c-admin-api/c-admin-14-api-eol.md) voor antwoorden op gemeenschappelijke vragen en verdere begeleiding.</p> |


## AppMeasurement

Voor de recentste updates op de versies van AppMeasurement, gelieve te verwijzen naar [ de versienota&#39;s van AppMeasurement ](https://github.com/adobe/appmeasurement/releases).


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2025](/help/release-notes/2025.md)
* [ de versienota&#39;s van Customer Journey Analytics ](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=nl-NL)
* [ het stromen de versienota&#39;s van de Inzameling van Media ](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=nl-NL)
* De recentste versie werkt voor [ producten van Adobe Experience Cloud ](https://business.adobe.com/products/adobe-experience-cloud-products.html) bij
