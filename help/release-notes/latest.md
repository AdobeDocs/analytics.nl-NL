---
title: Opmerkingen bij de release van Adobe Analytics
description: De huidige Adobe Analytics-releaseopmerkingen weergeven
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 9821150194e6bc89a5a2dec15a7957aaa177948e
workflow-type: tm+mt
source-wordcount: '1151'
ht-degree: 2%

---

# Huidige Adobe Analytics-releaseopmerkingen (mei 2024)

**Laatste update**: 21 mei 2024

Deze releaseopmerkingen hebben betrekking op de releaseperiode van 15 mei 2024 tot en met juni. Adobe Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie | Beschrijving | [Uitvoeren start](releases.md) | [Algemene beschikbaarheid](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Nieuwe documentatie voor upgrade van Adobe Analytics naar Customer Journey Analytics** | Voor organisaties die van Adobe Analytics aan Customer Journey Analytics bevorderen, zijn er veelvoudige verbeteringsopties en vele overwegingen om in mening te houden gebaseerd op de huidige implementatie van Adobe Analytics van een organisatie en langetermijndoelstellingen. De nieuwe documentatiebronnen zijn nu beschikbaar om u te helpen beter begrijpen:<ul><li>De verschillende upgradepaden die bestaan</li><li>Welke verbeteringspaden beschikbaar zijn op basis van de huidige Adobe Analytics-implementatie van een organisatie</li><li>De voor- en nadelen van elk upgradepad</li><li>Stapsgewijze begeleiding voor elk verbeteringspad</li><li>Overwegingen bij de verwerking van historische gegevens</li></ul>[Aan de slag met de upgrade naar Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/compare-aa-cja/upgrade-to-cja/cja-upgrade-getstarted) | | Nu beschikbaar |
| **Set `contextData` velden via XDM** | Klanten die gegevens naar Adobe Analytics verzenden via de Experience Edge Network kunnen [waarden voor contextgegevens instellen](https://experienceleague.adobe.com/en/docs/analytics/implementation/vars/page-vars/contextdata) rechtstreeks in XDM of in het &#39;data&#39; gedeelte van de lading. |  | Nu beschikbaar |
| **Analytics Real-time Reporting 2.0 API** | De nieuwe Real-time Rapporterende API 2.0 in Adobe Analytics verbetert klantenintegratie en verstrekt snelle rapporteringsresultaten. Deze resultaten kunnen programmatically worden gebruikt om met basis, trended, en breekrapporten te werken. [Meer informatie](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/reports/real-time/) | | vrijdag 30 mei 2024 |
| **Streaming media: Webgegevens naar Adobe Experience Platform Edge Network verzenden met de Web SDK** | U kunt nu de Adobe Experience Platform Web SDK gebruiken om webgegevens voor streamingmedia naar Adobe Experience Platform Edge Network te verzenden. Dankzij deze verbetering kunt u meer gepersonaliseerde campagnes maken en meer gepersonaliseerde inhoud bieden, zodat er meer gegevens over het bijhouden van meldingen beschikbaar zijn.<p>Deze verandering verstrekt een verenigde inzamelingsmethode voor Webimplementaties over alle oplossingen van het Platform, zoals Customer Journey Analytics, Adobe in real time CDP, Adobe Journey Optimizer, en Gebeurtenis het Door:sturen. Eerder was de enige manier om webgegevens van Streaming media naar Edge Network te verzenden met de Media Edge API. <p>(Bijgewerkte documentatiekoppeling die moet worden gevolgd)</p> | | zaterdag 31 mei 2024 |
| **Toename in standaard laag-verkeersdrempels** | In **medio april 2024**, zal de Adobe beginnen verhogend de standaardrapportreeks laag-verkeersdrempels als volgt: ![laagverkeersdrempels](assets/thresholds.png) Dit zal alleen gevolgen hebben voor variabelen die momenteel onder de nieuwe drempelwaarden liggen. Deze veranderingen zullen geleidelijk worden doorgevoerd en wij verwachten dat het werk door de **eind mei**. Aangezien deze verhogingen worden uitgerold, kunt u veranderingen voor high-cardinality variabelen opmerken:<ul><li>Er kunnen meer waarden van dimensies beschikbaar zijn voor rapportage.</li><li>Segmenten en berekende metriek kunnen meer gegevens bevatten.</li><li>Virtuele rapportsuites die op segmenten worden gebaseerd kunnen meer gegevens omvatten.</li><li>De indeling van de uitvoer kan meer gegevens bevatten.</li></ul> | medio april 2024 | zaterdag 31 mei 2024 |
| **Beheerdersinstellingen om de accounts en locaties te beheren die worden gebruikt voor exporteren en importeren** | Een nieuw tabblad &quot;Admin settings&quot; in Locations Manager geeft beheerders controle over de vraag of gebruikers accounts en locaties kunnen maken en bewerken. Deze instellingen zijn van toepassing wanneer gebruikers cloudimport- en -exportaccounts configureren en cloudimport- en exportlocaties configureren. <p>Beheerders kunnen ook de typen accounts beperken (Google Cloud Platform, Azure RBAC, Amazon S3 enzovoort) die gebruikers kunnen maken en gebruiken.</p><p>Eerder kon elke gebruiker accounts en locaties maken, bewerken en gebruiken voor elk type account.</p><p>(Bijgewerkte documentatiekoppeling die moet worden gevolgd)</p> | Juni 2024 | Juni 2024 |
| **Accounts en locaties delen die worden gebruikt voor exporteren en importeren** | Gebruikers kunnen de accounts en locaties die ze maken nu beschikbaar maken voor alle gebruikers in hun organisatie. Alleen account- en locatie-eigenaars en systeembeheerders kunnen accounts en locaties bewerken en verwijderen.<p>Eerder konden accounts en locaties alleen worden gebruikt door de gebruiker die ze heeft gemaakt.</p><p>Deze instellingen zijn beschikbaar wanneer gebruikers cloudimport- en -exportaccounts configureren en cloudimport- en exportlocaties configureren. </p> <p>(Bijgewerkte documentatiekoppeling die moet worden gevolgd)</p> | Juni 2024 | Juni 2024 |
| **Activity Map om minder servervraag voor Web SDK te gebruiken** | Op dit moment worden koppelingsgebeurtenissen voor Activity Mappen als hun eigen gebeurtenissen geteld en extra kosten met zich meegebracht. Deze verbetering neemt sommige verbindingsgebeurtenissen en verpakt hen in de volgende slag, gelijkend op hoe de gebeurtenissen door AppMeasurement worden behandeld. <p>(Bijgewerkte documentatiekoppeling die moet worden gevolgd)</p> | Beta start op 31 mei 2024 | TBD |

{style="table-layout:auto"}

## Oplossingen in Adobe Analytics

* Correctie van de volgende classificatieproblemen: AN-343186; AN-344711; AN-344856; AN-345094; AN-345179; AN-346265; AN-3452 AN-346339; AN-346560; AN-347572; AN-347681; AN-347768; AN-348024
* De volgende problemen met betrekking tot Data Warehouse zijn opgelost: AN-346789; AN-347031; AN-347568;
* Correctie van de volgende gegevensfeeds: AN-343616; AN-345831; AN-345988; AN-346124; AN-346232; AN-346972; AN-347 680; AN-347755; AN-347954
* Probleem met gegevensbronnen opgelost: AN-347890;
* De volgende Analysis Workspace-kwesties zijn opgelost: AN-321503; AN-343103; AN-343471; AN-345171; AN-345223; AN-345912; AN-3460 26; AN-346330; AN-346839; AN-347679
* Het volgende A4T-probleem verholpen: AN-345118.

### Andere correcties voor analysemogelijkheden

AN-327749; AN-332949; AN-342881; AN-343171; AN-343708; AN-344034; AN-34559; AN 346023; AN-346230; AN-346330; AN-346469; AN-346606; AN-346750; AN-346973; 47026; AN-347110; AN-347439;

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders {#admin}

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **Updates van ISO-regio** | zaterdag 10 mei 2024 | Adobe voert op 7 juni 2024 updates voor de ISO-regio uit voor 2024. Verwacht dat er na deze release kleine geo-informatie (regio) updates worden weergegeven. |
| **13 maanden verlopen van opgeslagen`cust_visids`** | donderdag 20 maart 2024 | Een aanstaande versie van de Analytics Hit-verwerkingsengine, bedoeld voor april of mei, zal een 13 maanden durende vervaldatum van opgeslagen `cust_visids`. Als de rapportsuite &#39;Enable Visitor Stitching&#39; heeft ingeschakeld, wordt deze instelling gebruikt voor het zoeken van de `cust_visid` voor een `visid_high/visid_low value` zonder `cust_visid` op de hit. Er is momenteel geen vervaldatum voor de toewijzing van een `cust_visid` voor een `visid_high/visid_low`. Met deze release, als er sinds 13 maanden of meer verstreken zijn `visid_high/visid_low` heeft een `cust_visid` bij een hit verloopt de toewijzing. |

{style="table-layout:auto"}

## Aankondigingen van einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Migratie naar Adobe I/O OAuth Server-aan-Server geloofsbrieven** | vrijdag 11 mei 2023 | Adobe Analytics API- en Livestream-klanten die Adobe I/O JWT-gebruikersgegevens gebruiken, moeten naar Adobe I/O OAuth Server-to-Server-gebruikersgegevens migreren door **1 januari 2025**. Adobe I/O staat niet toe dat vanaf 1 mei 2024 nieuwe JWT-referenties worden gemaakt. Klanten die JWT gebruiken moeten een nieuwe Server-aan-Server referentie OAuth tot stand brengen of hun bestaande JWT-referentie migreren naar een OAuth Server-aan-Server referentie. Klanten moeten ook hun clienttoepassingen bijwerken om de nieuwe OAuth Server-to-Server referenties te kunnen gebruiken. <ul><li>[Migreren van JWT-gebruikersgegevens (Service Account)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Implementatiehandleiding voor nieuwe en oude toepassingen met OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[De nieuwe OAuth Server-to-Server-referenties gebruiken](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Veelgestelde vragen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |

{style="table-layout:auto"}

## AppMeasurement

Voor de meest recente updates over releases van AppMeasurementen (versie 2.26.0) raadpleegt u [AppMeasurement voor JavaScript-releaseopmerkingen](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html).


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2023](/help/release-notes/2023.md)
* [Opmerkingen bij de release Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De nieuwste release-updates voor [Adobe Experience Cloud-producten](https://business.adobe.com/products/adobe-experience-cloud-products.html)
