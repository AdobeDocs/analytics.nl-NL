---
title: Opmerkingen bij de release van Adobe Analytics
description: De huidige Adobe Analytics-releaseopmerkingen weergeven
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: bb7c5489a38ab6e8164f7d8feeb8f0d918d75853
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 2%

---

# Huidige Adobe Analytics-releaseopmerkingen (augustus 2024)

**Laatste update**: 20 augustus 2024

Deze opmerkingen hebben betrekking op de releaseperiode van 14 augustus 2024 tot en met september 2024. De versies van Adobe Analytics werken op a [ ononderbroken leveringsmodel ](releases.md), dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie | Beschrijving | [ Het begin van de Uitvoer ](releases.md) | [ Algemene Beschikbaarheid ](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **de verbeteringen van SDK van het Web voor verbinding het volgen** | Verschillende opmerkelijke verbeteringen zijn beschikbaar in de nieuwste versie van de SDK van het Web voor het bijhouden van koppelingen, wat de Activity Map rechtstreeks ten goede komt. Deze nieuwe eigenschappen zijn beschikbaar in zowel de bibliotheek van SDK van het Web JavaScript als de de markeringsuitbreiding van SDK van het Web.<ul><li>Gebeurtenisgroepering: wanneer een bezoeker op een interne koppeling klikt, kunt u ervoor kiezen om gebeurtenisgegevens op de volgende pagina te groeperen in plaats van een aparte gebeurtenisaanroep voor het bijhouden van koppelingen te activeren. Deze verbetering vermindert het aantal gebeurtenissen die SDK van het Web tegen uw contractuele grens gebruikt.</li><li>Filter klikt eigenschappen: een nieuwe callback die `OnBeforeLinkClickSend` vervangt. U kunt deze callback aan filter gebruiken of verduisteren verbinding-verwante gegevens alvorens het naar Adobe te verzenden.</li></ul><p>Zie [ clickCollection ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/clickcollection) in de de gebruikersgids van SDK van het Web voor meer informatie.</p> | Beta openen, 10 juli 2024 | vrijdag 18 juli 2024 |

{style="table-layout:auto"}

## Oplossingen in Adobe Analytics

* Probleem verholpen waarbij meerdere onbekende waarden werden weergegeven in Workspace (AN-353632)
* Probleem verholpen waarbij het e-mailbericht met meldingen niet werd verzonden na het toevoegen van nieuwe klanten of nieuwe productprofielen voor Analytics in de beheerconsole (AN-350930)

### Andere correcties voor analysemogelijkheden

AN-354361; AN-354248; AN-354211; AN-354324; AN-351532; AN-349808; AN-347831; AN 353777; AN-354092; AN-354064; AN-354202; AN-354006; AN-354097; AN-352548; AN-3 53819; AN-353818; AN-353628; AN-353747; AN-353527; AN-353490; AN-352647; AN-35 2656; AN-351274; AN-352135; AN-351519; AN-344906; AN-353697; AN-35499; AN-354 354142; AN-354142; AN-354194; AN-354182; AN-354142; AN-354194; AN-3537 58; AN-353039; AN-353612; AN-350799; AN-354414; AN-354636; AN-354249; AN-3536 7; AN-350949; AN-349402; AN-355103; AN-354174; AN-353823; AN-354819; AN-354215; AN-354219; AN-354040; AN-354763; AN-354597; AN-354478; AN-354528; AN-35435

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders {#admin}

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **13 maanden verlopen van opgeslagen`cust_visids`** | woensdag 20 augustus 2024 | **Augustus 20, 2024**, versie van de de verwerkingsmotor van het Bewerkingsmechanisme van het Bezit van de Analyse dwingt een 13 maanden vervaldatum van bewaard `cust_visids` af. Als de rapportsuite &#39;Enable Visitor Stitching&#39; heeft ingeschakeld, wordt deze instelling gebruikt om de `cust_visid` for a `visid_high/visid_low value` with no `cust_visid` te vinden op de hit. Eerder was er geen vervaldatum van de toewijzing van een `cust_visid` voor een `visid_high/visid_low` . Als in deze release 13 maanden of meer zijn verstreken sinds `visid_high/visid_low` een `cust_visid` -resultaat heeft gehad, verloopt de toewijzing. |

{style="table-layout:auto"}

## Aankondigingen van einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **EOL voor Adobe Analytics API (versie 1.4)** | donderdag 17 juli 2024 | Op **12 augustus, 2026**, zullen de volgende Analytics Verouderde API diensten hun eind-van-leven bereiken en zullen worden gesloten, en de huidige integratie die gebruikend deze diensten wordt gebouwd zal ophouden werkend:<ul><li>Adobe Analytics API (versie 1.4)</li><li>Adobe Analytics WSSE-verificatie</li></ul><p>De integratie die Adobe Analytics API (versie 1.4) gebruiken moet aan [ Adobe Analytics 2.0 API ](https://developer.adobe.com/analytics-apis/docs/2.0/) migreren, terwijl de integratie WSSE aan een op OAuth-Gebaseerd authentificatieprotocol in [ Adobe Developer Console ](https://developer.adobe.com/console) moet migreren.</p><p>Zie [ Adobe Analytics 1.4 API EOL FAQ ](/help/admin/c-admin-api/c-admin-14-api-eol.md) voor antwoorden op gemeenschappelijke vragen en verdere begeleiding.</p> |
| **Migratie aan Adobe I/O OAuth Server-aan-Server geloofsbrieven** | vrijdag 11 mei 2023 | Adobe Analytics API en Livestream klanten die de geloofsbrieven van Adobe I/O JWT gebruiken moeten aan de geloofsbrieven van Adobe I/O OAuth Server-aan-Server door **Januari 1, 2025** migreren. Adobe I/O staat niet toe dat vanaf 1 mei 2024 nieuwe JWT-referenties worden gemaakt. Klanten die JWT gebruiken moeten een nieuwe Server-aan-Server referentie OAuth tot stand brengen of hun bestaande JWT-referentie migreren naar een OAuth Server-aan-Server referentie. Klanten moeten ook hun clienttoepassingen bijwerken om de nieuwe OAuth Server-to-Server referenties te kunnen gebruiken. <ul><li>[ migrerend van de Rekening van de Dienst (JWT) geloofsbrieven ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[ gids van de Implementatie voor nieuwe en oude toepassingen met OAuth ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[ Gebruikend de nieuwe Server-aan-Server geloofsbrieven OAuth ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[ FAQs ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |

{style="table-layout:auto"}

## AppMeasurement

Voor de recentste updates op de versies van het AppMeasurement (Versie 2.26.0), gelieve te verwijzen naar [ AppMeasurement voor de versienota&#39;s van JavaScript ](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html).


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2024](/help/release-notes/2024.md)
* [ de versienota&#39;s van de Customer Journey Analytics ](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [ het stromen toe:voegen-op versienota&#39;s van de Inzameling van Media ](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De recentste versie werkt voor [ producten van Adobe Experience Cloud ](https://business.adobe.com/products/adobe-experience-cloud-products.html) bij
