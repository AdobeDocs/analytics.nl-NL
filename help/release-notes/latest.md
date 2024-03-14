---
title: Opmerkingen bij de release van Adobe Analytics
description: De huidige Adobe Analytics-releaseopmerkingen weergeven
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 7cb7953e3321f2e8fa814ef6f1607cbe8d0f44de
workflow-type: tm+mt
source-wordcount: '1081'
ht-degree: 1%

---

# Opmerkingen bij de huidige Adobe Analytics-release (maart 2024)

**Laatste update**: 13 maart 2024

Deze opmerkingen hebben betrekking op de releaseperiode van 12 maart 2024 tot en met april 2024. Adobe Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie | Beschrijving | [Uitvoeren start](releases.md) | [Algemene beschikbaarheid](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **AppMeasurement bijwerken** | [release van AppMeasurement v2.26.0](/help/implement/appmeasurement-updates.md) is beschikbaar. | | dinsdag 4 maart 2024 |
| **Nieuwe kolom beschikbaar op de het landende pagina van Projecten** | De **[!UICONTROL Last used]** de kolom is nu beschikbaar wanneer het bekijken van het lusje van Projecten op [Adobe Analytics-landingspagina](https://experienceleague.adobe.com/docs/analytics/analyze/landing.html). <p>Deze informatie kan u helpen bepalen of een project voor gebruikers in uw organisatie waardevol is door de datum en de tijd te tonen toen het project het laatst werd geopend.</p> <p>Eerder **[!UICONTROL Last used]** de kolom was beschikbaar slechts in het Berekende manager van metriek, de manager van Segmenten, en de manager van Alarm.</p> |  | donderdag 13 maart 2024 |
| **Ondersteuning voor analyses van toestemmingsvlaggen die door Google voor DMA worden vereist** | Door de nieuwe Europese privacyregels eist Google dat gegevens die in Europa worden verzameld en aan hen zijn toegezonden, aangeven of twee specifieke soorten toestemming zijn verleend. **Vanaf 6 maart**, zal Google geen gegevens van gebeurtenissen meer accepteren die niet aangeven dat de desbetreffende toestemming is verleend. Adobe Analytics heeft ondersteuning beschikbaar gesteld voor het vastleggen van deze gegevens via een nieuwe adConsent-variabele. U kunt de nieuwe variabele zien die in [Gebruikersinterface voor privacyrapportage](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/privacy-reporting.md). Als u dit wilt activeren en de privacy al ingeschakeld hebt voor de vorige toestemmingsvariabelen, moet u de privacy opnieuw inschakelen. |  | donderdag 13 maart 2024 |
| **Dezelfde cloud-accounts gebruiken voor gegevensfeeds, -Data Warehouse en -classificatiesets** | Cloud-accounts en -locaties die u maakt, kunnen nu worden gebruikt voor het exporteren van gegevens (met gegevensfeeds en -Data Warehouse) en het importeren van gegevens (met classificatiesets).<p> **Wijzigingen bij het configureren van accounts:** Gebruikers kunnen cloudimport- en -exportaccounts configureren en cloudimport- en -exportlocaties configureren die voor de volgende doeleinden kunnen worden gebruikt:<ul><li>Gegevens importeren met classificatiesets</li><li>Gegevens exporteren met gegevensfeeds</li><li>Gegevens exporteren met Data Warehouse.</li></ul><p>**Wijzigingen bij het beheren van accounts**: Gebruikers kunnen de pagina Locaties (onder Componenten > Locaties) gebruiken om alle accounts en locaties die ze maken weer te geven en te beheren, ongeacht waar ze zijn gemaakt. <p>Eerder werd de pagina Locaties alleen toegepast op accounts die zijn gemaakt voor het importeren van gegevens met classificatiesets.</p> | | April 2024 |
| **Beheerders kunnen alle locaties in hun organisatie beheren** | Met een nieuwe optie op de pagina Locaties kunnen beheerders alle locaties in de organisatie weergeven en beheren. <p>Eerder konden beheerders alleen de door hen gemaakte locaties weergeven en beheren.</p> |  | April 2024 |
| **Activity Map gebruikt minder servervraag voor Web SDK** | Op dit moment worden koppelingsgebeurtenissen voor Activity Mappen als hun eigen gebeurtenissen geteld en extra kosten met zich meegebracht. <p>Deze verbetering neemt sommige verbindingsgebeurtenissen en verpakt hen in de volgende slag, gelijkend op hoe de gebeurtenissen door AppMeasurement worden behandeld.</p> |  | donderdag 3 april 2024 |
| **Toename in standaard laag-verkeersdrempels** | In **medio april 2024**, zal de Adobe beginnen verhogend de standaardrapportreeks laag-verkeersdrempels als volgt: ![laagverkeersdrempels](assets/thresholds.png) Dit zal alleen gevolgen hebben voor variabelen die momenteel onder de nieuwe drempelwaarden liggen. Deze veranderingen zullen geleidelijk worden doorgevoerd en wij verwachten dat het werk door de **eind mei**. Aangezien deze verhogingen worden uitgerold, kunt u veranderingen voor high-cardinality variabelen opmerken:<ul><li>Er kunnen meer waarden van dimensies beschikbaar zijn voor rapportage.</li><li>Segmenten en berekende metriek kunnen meer gegevens bevatten.</li><li>Virtuele rapportsuites die op segmenten worden gebaseerd kunnen meer gegevens omvatten.</li><li>De indeling van de uitvoer kan meer gegevens bevatten.</li></ul> | | medio april 2024 |

{style="table-layout:auto"}

## Oplossingen in Adobe Analytics

* Oplossing voor de volgende problemen in verband met classificaties: AN-335632; AN-337559; AN-340164; AN-340370; AN-341089; AN-3412 AN-341469; AN-341481; AN-341760; AN-341778; AN-342144; AN-342258; AN-34233 342400
* Oplossing voor de volgende problemen in verband met classificatieregel Builder: AN-340921; AN-341269; AN-341292; AN-341467; AN-34166; AN-342145; AN-34 329
* Het volgende probleem met intelligente waarschuwingen is opgelost: AN-340736
* Probleem met segmentering opgelost: AN-336242
* De volgende problemen met betrekking tot Data Warehouse zijn opgelost: AN-335354; AN-339446; AN-339774; AN-340221; AN-340599; AN-341277; AN-3420 AN-342088; AN-342592
* Probleem verholpen met gegevensfeeds: AN-335508; AN-340887; AN-341050; AN-341208; AN-341403; AN-341479; AN-341 524; AN-341661; AN-342000; AN-342125; AN-342256; AN-342301; AN-342410; AN-3425 02; AN-342525
* Probleem met Report Builder verholpen: AN-340540
* Oplossing voor de volgende Analysis Workspace-problemen: AN-295889; AN-330981; AN-338818; AN-339730; AN-341114; AN-341520;

### Andere correcties voor analysemogelijkheden

AN-312198; AN-338009; AN-339549; AN-333970; AN-334790; AN-336461; AN-336572; AN 339549; AN-341119; AN-341246; AN-341268; AN-341272; AN-341475; AN-341547; AN-3 41558; AN-341680; AN-342017;

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders {#admin}

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **Adobe API-objectlidtoevoegingen** | donderdag 17 januari 2024 | Adobe kan optionele aanvraag- en antwoordleden (naam/waardeparen) op elk gewenst moment en zonder kennisgeving of wijzigingen in versiebeheer toevoegen aan bestaande API-objecten. De Adobe raadt u aan de API-documentatie te raadplegen van alle hulpprogramma&#39;s van derden die u met onze API&#39;s integreert, zodat dergelijke toevoegingen tijdens de verwerking worden genegeerd, als ze niet worden begrepen. Als deze toevoegingen correct zijn geïmplementeerd, zijn ze vaste wijzigingen voor uw implementatie. De Adobe zal geen parameters verwijderen of vereiste parameters toevoegen zonder standaardbericht door versienota&#39;s eerst te verstrekken. |
| **`getPageLoadTime`insteekmodule vervangen** | donderdag 10 januari 2024 | Deze plug-in wordt niet meer ondersteund. Zijn code gebruikt de performance.timing methode, die (volgens MDN) is geweest [verouderd](https://developer.mozilla.org/en-US/docs/Web/API/PerformanceTiming). Het werk aan een bijgewerkte plug-in is begonnen. |

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
