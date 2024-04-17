---
title: Opmerkingen bij de release van Adobe Analytics
description: De huidige Adobe Analytics-releaseopmerkingen weergeven
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 627a813d0d5595521d72f0cf832b3a1ceb7655f8
workflow-type: tm+mt
source-wordcount: '1211'
ht-degree: 1%

---

# Huidige Adobe Analytics-releaseopmerkingen (april 2024)

**Laatste update**: 17 april 2024

Deze releaseopmerkingen hebben betrekking op de releaseperiode van 17 april 2024 tot en met mei. Adobe Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie | Beschrijving | [Uitvoeren start](releases.md) | [Algemene beschikbaarheid](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Streaming media: Roku-gegevens verzenden naar Adobe Experience Platform Edge Network** | Wanneer [Media Analytics installeren met Experience Platform Edge](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/edge-recommended/media-edge-sdk/implementation-edge)kunt u de Adobe Experience Platform Roku SDK gebruiken om streaming Media-gegevens naar Adobe Experience Platform te verzenden. |  | zaterdag 12 april 2024 |
| **Verbeterde workflow voor Web SDK-migratie** | Met Adobe Experience Platform-gegevensverzameling worden nu automatisch veel velden van het gegevensobject rechtstreeks toegewezen aan Adobe Analytics. Deze verbeterde workflow biedt de volgende voordelen:<ul><li>Het staat uw organisatie toe om aan SDK van het Web te migreren zonder zich over het creëren van of het houden van aan een [!UICONTROL XDM schema]. Zie [Variabele voor gegevensobject toewijzen](https://experienceleague.adobe.com/en/docs/analytics/implementation/aep-edge/data-var-mapping) voor meer informatie . (Meer documentatiekoppelingen)</li><li>Nadat u naar SDK van het Web migreert, is uw organisatie in een betere positie om van Adobe Analytics aan Customer Journey Analytics te migreren. Dit komt omdat SDK van het Web voor een naadloze migratie aan Customer Journey Analytics toestaat.</li></ul> (Binnenkort vindt u meer informatie over deze en andere migratieopties.) |  | April 2024 |
| **Verbetering van machtigingen voor alleen project [!UICONTROL Workspace] componenten** | Eerder, als een gebruiker (Gebruiker A) een project met een andere gebruiker (Gebruiker B) deelde, en Gebruiker B gaf geeft geeft geeft toegang tot het project uit, zou Gebruiker B het project kunnen uitgeven. Gebruiker B kan echter geen bewerkingen uitvoeren [!UICONTROL Quick Segments] ingesloten in het project. Deze beperking is nu verwijderd. Gebruiker B kan deze bewerken [!UICONTROL Quick Segments] en andere projectgebonden componenten die in het gedeelde project zijn ingesloten. |  | donderdag 17 april 2024 |
| **Dezelfde cloudaccounts gebruiken voor [!UICONTROL Data Feeds], [!UICONTROL Data Warehouse], en[!UICONTROL Classification sets]** | Cloud-accounts en -locaties die u maakt, kunnen nu worden gebruikt voor het exporteren van gegevens (met [!UICONTROL Data Feeds] en [!UICONTROL Data Warehouse]) en gegevens importeren (met [!UICONTROL Classification sets]).<p> **Wijzigingen bij het configureren van accounts:** Gebruikers kunnen [Cloud-import- en exportaccounts configureren](https://experienceleague.adobe.com/en/docs/analytics/components/locations/configure-import-accounts) en [Locaties voor het importeren en exporteren van cloud configureren](https://experienceleague.adobe.com/en/docs/analytics/components/locations/configure-import-locations) die kunnen worden gebruikt voor een van de volgende doeleinden:<ul><li>Gegevens importeren met [!UICONTROL Classification sets]</li><li>Gegevens exporteren met [!UICONTROL Data Feeds]</li><li>Gegevens exporteren met [!UICONTROL Data Warehouse].</li></ul><p>**Wijzigingen bij het beheren van accounts**: Gebruikers kunnen de opdracht [Locaties](https://experienceleague.adobe.com/en/docs/analytics/components/locations/locations-manager) pagina (onder [!UICONTROL Components] > Lochandelingen) om alle accounts en locaties te bekijken en te beheren die ze maken, ongeacht waar ze zijn gemaakt. <p>Eerder [!UICONTROL Locations] pagina alleen toegepast op accounts die zijn gemaakt voor het importeren van gegevens met [!UICONTROL Classification sets].</p> | | donderdag 17 april 2024 |
| **Beheerders kunnen alle locaties en accounts in hun organisatie beheren** | Met een nieuwe optie op het tabblad Locaties (op de pagina Componenten > Locaties) kunnen beheerders alle locaties in de organisatie weergeven en beheren.<p>Een nieuwe optie op de knop [Locatie](https://experienceleague.adobe.com/en/docs/analytics/components/locations/locations-manager) Via het tabblad accounts (op de pagina Componenten > Locaties) kunnen beheerders alle accounts in de organisatie weergeven en beheren.</p> <p>Eerder konden beheerders alleen de locaties en accounts weergeven en beheren die ze hadden gemaakt.</p> |  | donderdag 17 april 2024 |
| **Toename in standaard laag-verkeersdrempels** | In **medio april 2024**, zal de Adobe beginnen verhogend de standaardrapportreeks laag-verkeersdrempels als volgt: ![laagverkeersdrempels](assets/thresholds.png) Dit zal alleen gevolgen hebben voor variabelen die momenteel onder de nieuwe drempelwaarden liggen. Deze veranderingen zullen geleidelijk worden doorgevoerd en wij verwachten dat het werk door de **eind mei**. Aangezien deze verhogingen worden uitgerold, kunt u veranderingen voor high-cardinality variabelen opmerken:<ul><li>Er kunnen meer waarden van dimensies beschikbaar zijn voor rapportage.</li><li>Segmenten en berekende metriek kunnen meer gegevens bevatten.</li><li>Virtuele rapportsuites die op segmenten worden gebaseerd kunnen meer gegevens omvatten.</li><li>De indeling van de uitvoer kan meer gegevens bevatten.</li></ul> | medio april 2024 | zaterdag 31 mei 2024 |
| **Activity Map gebruikt minder servervraag voor Web SDK** | Op dit moment worden koppelingsgebeurtenissen voor Activity Mappen als hun eigen gebeurtenissen geteld en extra kosten met zich meegebracht. <p>Deze verbetering neemt sommige verbindingsgebeurtenissen en verpakt hen in de volgende slag, gelijkend op hoe de gebeurtenissen door AppMeasurement worden behandeld.</p> |  | donderdag 1 mei 2024 |

{style="table-layout:auto"}

## Oplossingen in Adobe Analytics

* Correctie van de volgende classificatieproblemen: AN-343439; AN-343503; AN-343504; AN-343986; AN-344262; AN-344564; AN-3452 AN-345234
* Oplossing voor de volgende problemen met Classifications Rule Builder: AN-341488; AN-342501; AN-345751
* Het volgende probleem met intelligente waarschuwingen is opgelost: AN-343466.
* Probleem met segmentering opgelost: AN-342313
* Probleem met Data Warehouse verholpen: AN-344292
* Correctie van de volgende gegevensfeeds: AN-339545; AN-340092; AN-342124; AN-342862; AN-343737; AN-344035; AN-344 329; AN-344703; AN-344721; AN-344940; AN-345180; AN-345196; AN-34525; AN-3452 36; AN-345326; AN-345631; AN-345659
* Probleem met gegevensbronnen opgelost: AN-343541
* De volgende Analysis Workspace-kwesties zijn opgelost: AN-336303; AN-336472; AN-338422; AN-338556; AN-339718; AN-340147; AN-3403 01; AN-340421; AN-340951; AN-341172; AN-342905; AN-342909; AN-34348; AN-34357 0; AN-344050; AN-344182; AN-344763; AN-344768;
* De volgende problemen met Analytics Admin: AN-342519; AN-342523; AN-343623; AN-343882; AN-344237; AN-344829; AN-345 opgelost 235;
* De volgende A4T-problemen opgelost: AN-341619; AN-344402
* Probleem verholpen met de volgende mobiele app: AN-342010

### Andere correcties voor analysemogelijkheden

AN-336099; AN-337474; AN-337993; AN-339718; AN-339901; AN-340014; AN-341356; AN 343021; AN-343102; AN-343353; AN-343416; AN-340014; AN-344037; AN-344525; AN-3 45737

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders {#admin}

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **13 maanden verlopen van opgeslagen`cust_visids`** | donderdag 20 maart 2024 | Een aanstaande versie van de Analytics Hit-verwerkingsengine, bedoeld voor april of mei, zal een 13 maanden durende vervaldatum van opgeslagen `cust_visids`. Als de rapportsuite &#39;Enable Visitor Stitching&#39; heeft ingeschakeld, wordt deze instelling gebruikt voor het zoeken van de `cust_visid` voor een `visid_high/visid_low value` zonder `cust_visid` op de hit. Er is momenteel geen vervaldatum voor de toewijzing van een `cust_visid` voor een `visid_high/visid_low`. Met deze release, als er sinds 13 maanden of meer verstreken zijn `visid_high/visid_low` heeft een `cust_visid` bij een hit zal de mapping verlopen . |
| **Adobe API-objectlidtoevoegingen** | donderdag 17 januari 2024 | Adobe kan optionele aanvraag- en antwoordleden (naam/waardeparen) op elk gewenst moment en zonder kennisgeving of wijzigingen in versiebeheer toevoegen aan bestaande API-objecten. De Adobe raadt u aan de API-documentatie te raadplegen van alle hulpprogramma&#39;s van derden die u met onze API&#39;s integreert, zodat dergelijke toevoegingen tijdens de verwerking worden genegeerd, als ze niet worden begrepen. Als deze toevoegingen correct zijn geïmplementeerd, zijn ze vaste wijzigingen voor uw implementatie. De Adobe zal geen parameters verwijderen of vereiste parameters toevoegen zonder standaardbericht door versienota&#39;s eerst te verstrekken. |

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
