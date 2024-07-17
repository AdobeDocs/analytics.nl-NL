---
title: Opmerkingen bij de release van Adobe Analytics
description: De huidige Adobe Analytics-releaseopmerkingen weergeven
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: cb0eab15dac6d679e9f912010045e6be2e47df4a
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 1%

---

# Opmerkingen bij de huidige Adobe Analytics-release (juli 2024)

**Laatste update**: 17 juli 2024

Deze releaseopmerkingen hebben betrekking op de periode van 17 juli 2024 tot en met augustus 2024. De versies van Adobe Analytics werken op a [ ononderbroken leveringsmodel ](releases.md), dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie | Beschrijving | [ Het begin van de Uitvoer ](releases.md) | [ Algemene Beschikbaarheid ](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **de verbeteringen van SDK van het Web voor verbinding het volgen** | Verschillende opmerkelijke verbeteringen zijn beschikbaar in de nieuwste versie van de SDK van het Web voor het bijhouden van koppelingen, wat de Activity Map rechtstreeks ten goede komt. Deze nieuwe eigenschappen zijn beschikbaar in zowel de bibliotheek van SDK van het Web JavaScript als de de markeringsuitbreiding van SDK van het Web.<ul><li>Gebeurtenisgroepering: wanneer een bezoeker op een interne koppeling klikt, kunt u ervoor kiezen om gebeurtenisgegevens op de volgende pagina te groeperen in plaats van een aparte gebeurtenisaanroep voor het bijhouden van koppelingen te activeren. Deze verbetering vermindert het aantal gebeurtenissen die SDK van het Web tegen uw contractuele grens gebruikt.</li><li>Filter klikt eigenschappen: een nieuwe callback die `OnBeforeLinkClickSend` vervangt. U kunt deze callback aan filter gebruiken of verduisteren verbinding-verwante gegevens alvorens het naar Adobe te verzenden.</li></ul><p>Zie [ clickCollection ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/clickcollection) in de de gebruikersgids van SDK van het Web voor meer informatie.</p> | Beta openen, 10 juli 2024 | TBD |

{style="table-layout:auto"}

## Oplossingen in Adobe Analytics

* Probleem verholpen waarbij gebruikers zich niet konden aanmelden bij de interface voor analyse (AN-352953)
* Probleem opgelost waarbij gebruikers zich niet konden aanmelden bij de mobiele app Analytics (AN-352463)
* Probleem opgelost waarbij het downloaden van het project als een PDF werd voorkomen (AN-352680)
* Probleem opgelost waarbij classificaties niet werden geïmporteerd (AN-352178)

### Andere correcties voor analysemogelijkheden

AN-352905; AN-352902; AN-352693; AN-352659; AN-352619;
AN-352577; AN-352575; AN-352572; AN-352571; AN-352549; AN-352501; AN-35249; AN-3 352478; AN-352466; AN-352437; AN-352378; AN-352355; AN-352341; AN-352318; AN-3 52297; AN-352272; AN-352267; AN-352263; AN-352088; AN-352019; AN-352018; AN-35 1978; AN-351908; AN-351809; AN-351750; AN-351689; AN-351624; AN-351564; AN-351 351414; AN-351405; AN-351299; AN-351283; AN-351405; AN-351299; AN-3512 31; AN-350710; AN-349912; AN-349786; AN-348300; AN-348061; AN-347865; AN-3476 AN-347478; AN-343611; AN-343114; AN-334124

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders {#admin}

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **13 maanden verlopen van opgeslagen`cust_visids`** | donderdag 22 mei 2024 | Een aanstaande versie van de de verwerkingsmotor van de Hit van Analytics, **voor Juli 2024** wordt gericht, zal beginnen afdwingend een 13 maandenvervaldatum van bewaard `cust_visids`. Als de rapportsuite &#39;Enable Visitor Stitching&#39; heeft ingeschakeld, wordt deze instelling gebruikt om de `cust_visid` for a `visid_high/visid_low value` with no `cust_visid` te vinden op de hit. Er is momenteel geen vervaldatum voor de toewijzing van een `cust_visid` for een `visid_high/visid_low` . Als in deze release 13 maanden of meer zijn verstreken sinds `visid_high/visid_low` een `cust_visid` -resultaat heeft gehad, verloopt de toewijzing. |

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
