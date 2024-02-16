---
title: Opmerkingen bij de release van Adobe Analytics
description: De huidige Adobe Analytics-releaseopmerkingen weergeven
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: d52e4d41ac0fc6ce6db04e491fc33bac2284f040
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 1%

---

# Opmerkingen bij de huidige Adobe Analytics-release (februari 2024)

**Laatste update**: 16 februari 2024

Deze opmerkingen hebben betrekking op de releaseperiode van 14 februari 2024 tot 11 maart 2024. Adobe Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie | Beschrijving | [Uitvoeren start](releases.md) | [Algemene beschikbaarheid](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Activity Map voor Web SDK zonder extra kosten** | Op dit moment worden koppelingsgebeurtenissen voor Activity Mappen als hun eigen gebeurtenissen geteld en extra kosten met zich meegebracht. Deze verbetering neemt sommige verbindingsgebeurtenissen en verpakt hen in de volgende slag, gelijkend op hoe de gebeurtenissen door AppMeasurement worden behandeld. |  | donderdag 6 maart 2024 |
| **Toename in standaard laag-verkeersdrempels** | In **medio april 2024**, zal de Adobe beginnen verhogend de standaardrapportreeks laag-verkeersdrempels als volgt: ![laagverkeersdrempels](assets/thresholds.png) Dit zal alleen gevolgen hebben voor variabelen die momenteel onder de nieuwe drempelwaarden liggen. Deze veranderingen zullen geleidelijk worden doorgevoerd en wij verwachten dat het werk door de **eind mei**. Aangezien deze verhogingen worden uitgerold, kunt u veranderingen voor high-cardinality variabelen opmerken:<ul><li>Er kunnen meer waarden van dimensies beschikbaar zijn voor rapportage.</li><li>Segmenten en berekende metriek kunnen meer gegevens bevatten.</li><li>Virtuele rapportsuites die op segmenten worden gebaseerd kunnen meer gegevens omvatten.</li></ul> | medio april 2024 | Eind mei 2024 |

{style="table-layout:auto"}

## Oplossingen in Adobe Analytics

* Oplossing voor de volgende problemen in verband met classificaties: AN-319515; AN-337559; AN-338149; AN-338702; AN-338769; AN-33891; AN-393 AN-339649; AN-339668; AN-339669; AN-339776; AN-339822; AN-340017; AN-34020 2; AN-340476;
* Oplossing voor de volgende problemen met betrekking tot de classificatieregel Builder: AN-338385; AN-338399; AN-338592; AN-338810; AN-338893; AN-339 340201; AN-340309;
* De volgende A4T-kwesties zijn opgelost: AN-334830; AN-336194; AN-338309; AN-338650;
* Probleem met gegevensverzameling verholpen: AN-339323
* De volgende problemen met betrekking tot de Data Warehouse zijn opgelost: AN-335542; AN-331425; AN-337215; AN-338445; AN-338643; AN-3394 340066; AN-340207; AN-340460
* Probleem verholpen met gegevensfeeds: AN-335952; AN-338653; AN-339508; AN-339681; AN-340418
* Probleem met gegevensbronnen opgelost: AN-338648
* De volgende Analysis Workspace-kwesties zijn opgelost: AN-326509; AN-336186; AN-336190; AN-336309; AN-337922; AN-338094; AN-383 23; AN-338556; AN-339600; AN-340445

### Andere correcties voor analysemogelijkheden

AN-328239; AN-332908; AN-335449; AN-335517; AN-336075; AN-336100; AN-336128; AN 338088; AN-338270; AN-338393; AN-338494; AN-339326; AN-339742; AN-33983; AN-3 40419

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders {#admin}

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| Adobe API-objectlidtoevoegingen | donderdag 17 januari 2024 | Adobe kan optionele aanvraag- en antwoordleden (naam/waardeparen) op elk gewenst moment en zonder kennisgeving of wijzigingen in versiebeheer toevoegen aan bestaande API-objecten. De Adobe raadt u aan de API-documentatie te raadplegen van alle hulpprogramma&#39;s van derden die u met onze API&#39;s integreert, zodat dergelijke toevoegingen tijdens de verwerking worden genegeerd, als ze niet worden begrepen. Als deze toevoegingen correct zijn geïmplementeerd, zijn ze vaste wijzigingen voor uw implementatie. De Adobe zal geen parameters verwijderen of vereiste parameters toevoegen zonder standaardbericht door versienota&#39;s eerst te verstrekken. |
| `getPageLoadTime` insteekmodule vervangen | donderdag 10 januari 2024 | Deze plug-in wordt niet meer ondersteund. Zijn code gebruikt de performance.timing methode, die (volgens MDN) is geweest [verouderd](https://developer.mozilla.org/en-US/docs/Web/API/PerformanceTiming). Het werk aan een bijgewerkte plug-in is begonnen. |

{style="table-layout:auto"}

## Aankondigingen van einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Migratie naar Adobe I/O OAuth Server-aan-Server geloofsbrieven** | vrijdag 11 mei 2023 | Adobe Analytics API- en Livestream-klanten die Adobe I/O JWT-gebruikersgegevens gebruiken, moeten naar Adobe I/O OAuth Server-to-Server-gebruikersgegevens migreren door **1 januari 2025**. Adobe I/O staat niet toe dat vanaf 1 mei 2024 nieuwe JWT-referenties worden gemaakt. Klanten die JWT gebruiken moeten een nieuwe Server-aan-Server referentie OAuth tot stand brengen of hun bestaande JWT-referentie migreren naar een OAuth Server-aan-Server referentie. Klanten moeten ook hun clienttoepassingen bijwerken om de nieuwe OAuth Server-to-Server referenties te kunnen gebruiken. <ul><li>[Migreren van JWT-gebruikersgegevens (Service Account)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Implementatiehandleiding voor nieuwe en oude toepassingen met OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[De nieuwe OAuth Server-to-Server-referenties gebruiken](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Veelgestelde vragen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |

{style="table-layout:auto"}

## AppMeasurement

Voor de meest recente updates over releases van AppMeasurementen (versie 2.25.0) raadpleegt u [AppMeasurement voor JavaScript-releaseopmerkingen](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html).


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2023](/help/release-notes/2023.md)
* [Opmerkingen bij de release Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De nieuwste release-updates voor [Adobe Experience Cloud-producten](https://business.adobe.com/products/adobe-experience-cloud-products.html)
