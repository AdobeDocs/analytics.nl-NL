---
title: Opmerkingen bij de release van Adobe Analytics
description: De huidige Adobe Analytics-releaseopmerkingen weergeven
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 54be0400a76b1f8dbbf2aab99ed8d771d67e5bc3
workflow-type: tm+mt
source-wordcount: '1051'
ht-degree: 1%

---

# Opmerkingen bij de huidige Adobe Analytics-release (juni 2024)

**Laatste update**: 20 juni 2024

Deze releaseopmerkingen hebben betrekking op de releaseperiode van 12 juni 2024 tot en met juli. Adobe Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie | Beschrijving | [Uitvoeren start](releases.md) | [Algemene beschikbaarheid](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Meerdere velden in een vervolgkeuzemenu selecteren** | Wanneer meerdere velden zijn toegevoegd aan een vervolgkeuzefilter, kunnen gebruikers nu meerdere velden tegelijk selecteren. Het deelvenster wordt gefilterd en bevat een van de geselecteerde velden. <p>Eerder konden gebruikers slechts één veld tegelijk selecteren in een vervolgkeuzemenu.</p><p>Zie voor meer informatie [Statische drop-down segmenten](/help/analyze/analysis-workspace/c-panels/panels.md#static-drop-down-segments) in [Overzicht van deelvensters](/help/analyze/analysis-workspace/c-panels/panels.md).</p> |  | donderdag 19 juni 2024 |
| **Inhoudsopgave voor werkruimteprojecten** | Er is nu een nieuwe inhoudsopgave beschikbaar voor projecten. De inhoudsopgave bevat koppelingen waarmee gebruikers snel naar deelvensters en visualisaties in het project kunnen gaan. De inhoudsopgave kan worden ingeschakeld voor afzonderlijke projecten of voor alle projecten voor een bepaalde gebruiker.<p>Zie voor meer informatie [Inhoudsopgave van project](/help/analyze/analysis-workspace/build-workspace-project/project-table-of-contents.md).</p> |  | donderdag 19 juni 2024 |
| **Hyperlinks maken voor dimensie-items in een vrije-vormtabel** | U kunt hyperlinks maken voor een of meer dimensie-items, zodat hierop kan worden geklikt in een vrije-vormtabel in Analysis Workspace. <p>U kunt hyperlinks maken voor dimensie-items die URL-waarden hebben, of u kunt aangepaste URL&#39;s maken voor dimensie-items die geen URL-waarden hebben.</p><p>U kunt dynamische aangepaste URL&#39;s maken voor meerdere dimensie-items met behulp van variabelen. Variabelen kunnen verwijzen naar de waarde van een dimensie-item of naar de uitsplitsingsdimensie.</p><p>Zie voor meer informatie [Hyperlinks maken voor afmetingen in een vrije-vormtabel](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table-hyperlinks.md).</p> |  | donderdag 19 juni 2024 |
| **Beheerdersinstellingen om de accounts en locaties te beheren die worden gebruikt voor exporteren en importeren** | Een nieuwe [Het tabblad &quot;Admin settings&quot; in Locatiebeheer](/help/components/locations/locations-manager.md#configure-company-wide-settings-administrators-only) geeft beheerders controle over of de gebruikers rekeningen en plaatsen kunnen tot stand brengen en uitgeven. Deze instellingen zijn van toepassing wanneer gebruikers [cloud-import- en -exportaccounts configureren](/help/components/locations/configure-import-accounts.md) en [cloudimport- en exportlocaties configureren](/help/components/locations/configure-import-locations.md). <p>Beheerders kunnen ook de typen accounts beperken (Google Cloud Platform, Azure RBAC, Amazon S3 enzovoort) die gebruikers kunnen maken en gebruiken.</p><p>Eerder kon elke gebruiker accounts en locaties maken, bewerken en gebruiken voor elk type account.</p> | donderdag 12 juni 2024 | vrijdag 20 juni 2024 |
| **Accounts en locaties delen die worden gebruikt voor exporteren en importeren** | Gebruikers kunnen de accounts en locaties die ze maken nu beschikbaar maken voor alle gebruikers in hun organisatie. Alleen account- en locatie-eigenaars en systeembeheerders kunnen accounts en locaties bewerken en verwijderen.<p>Eerder konden accounts en locaties alleen worden gebruikt door de gebruiker die ze heeft gemaakt.</p><p>Deze instellingen zijn beschikbaar wanneer gebruikers [cloud-import- en -exportaccounts configureren](https://experienceleague.adobe.com/en/docs/analytics/components/locations/configure-import-accounts) en [cloudimport- en exportlocaties configureren](https://experienceleague.adobe.com/en/docs/analytics/components/locations/configure-import-locations). </p> | donderdag 12 juni 2024 | vrijdag 20 juni 2024 |
| **Activity Map om minder servervraag voor Web SDK te gebruiken** | Op dit moment worden koppelingsgebeurtenissen voor Activity Mappen als hun eigen gebeurtenissen geteld en extra kosten met zich meegebracht. Deze verbetering neemt sommige verbindingsgebeurtenissen en verpakt hen in de volgende slag, gelijkend op hoe de gebeurtenissen door AppMeasurement worden behandeld. <p>(Bijgewerkte documentatiekoppeling die moet worden gevolgd)</p> | Openingsbètaversie begint op 19 juni 2024 | TBD |
| **Nieuwe API-handleiding voor gegevensbronnen** | De [Adobe Analytics 2.0 Data Sources API](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/data-sources/) eindpunten verstrekken methodes om, te creëren te bekijken, te schrappen en, aan de rekeningen van Gegevensbronnen te uploaden. |  | Nu beschikbaar |
| **Nieuwe methoden in de API Guide voor classificaties** | Er zijn twee nieuwe methoden voor het ophalen van bestandspartities toegevoegd aan de API Guide voor classificaties.<ul><li>[Bestandsindeling voor classificatietaak ophalen](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/classifications/#get-classification-job-file-partition-list)</li><li>[Indelen van indelingstaakbestand voor exporteren ophalen](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/classifications/#get-classification-export-job-file-part)</li></ul> |  | Nu beschikbaar |

{style="table-layout:auto"}

## Oplossingen in Adobe Analytics

* Correctie van de volgende classificatieproblemen: AN-347682; AN-348396; AN-348625; AN-348668; AN-348926; AN-348936; AN-3490 349697; AN-349758; AN-349862; AN-35005 AN-350054; AN-350208; AN-350497; AN-350525; AN-351067
* De volgende problemen met betrekking tot Data Warehouse zijn opgelost: AN-346862; AN-349409; AN-349926; AN-350629; AN-350996
* Correctie van de volgende gegevensfeeds: AN-346727; AN-348282; AN-348334; AN-348725; AN-348726; AN-348823; AN-349 349710; AN-349729; AN-349307; AN-349539; AN-349710; AN-349729; AN-3498 78; AN-349943; AN-350527;
* Probleem met gegevensbronnen opgelost: AN-350038
* De volgende Analysis Workspace-kwesties zijn opgelost: AN-342953; AN-346346; AN-349590; AN-349717; AN-350057; AN-350697; AN-3509 04
* De volgende problemen in verband met de Report Builder zijn opgelost: AN-348903; AN-350691
* De volgende A4T-problemen verholpen: AN-347690; AN-350853

### Andere correcties voor analysemogelijkheden

AN-346470; AN-346850; AN-347227; AN-348145; AN-348564; AN-349001; AN-349008; AN 349211; AN-349719; AN-350523;

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders {#admin}

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **13 maanden verlopen van opgeslagen`cust_visids`** | donderdag 22 mei 2024 | Een volgende release van de Analytics Hit-verwerkingsengine. **gericht voor juli 2024**, wordt een 13 maanden durende vervaldatum van opgeslagen `cust_visids`. Als de rapportsuite &#39;Enable Visitor Stitching&#39; heeft ingeschakeld, wordt deze instelling gebruikt voor het zoeken van de `cust_visid` voor een `visid_high/visid_low value` zonder `cust_visid` op de hit. Er is momenteel geen vervaldatum voor de toewijzing van een `cust_visid` voor een `visid_high/visid_low`. Met deze release, als er sinds 13 maanden of meer verstreken zijn `visid_high/visid_low` heeft een `cust_visid` bij een hit verloopt de toewijzing. |
| **Updates van ISO-regio** | zaterdag 10 mei 2024 | Adobe voert op 7 juni 2024 updates voor de ISO-regio uit voor 2024. Verwacht dat er na deze release kleine geo-informatie (regio) updates worden weergegeven. |

{style="table-layout:auto"}

## Aankondigingen van einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Migratie naar Adobe I/O OAuth Server-aan-Server geloofsbrieven** | vrijdag 11 mei 2023 | Adobe Analytics API- en Livestream-klanten die Adobe I/O JWT-gebruikersgegevens gebruiken, moeten naar Adobe I/O OAuth Server-to-Server-gebruikersgegevens migreren door **1 januari 2025**. Adobe I/O staat niet toe dat vanaf 1 mei 2024 nieuwe JWT-referenties worden gemaakt. Klanten die JWT gebruiken moeten een nieuwe Server-aan-Server referentie OAuth tot stand brengen of hun bestaande JWT-referentie migreren naar een OAuth Server-aan-Server referentie. Klanten moeten ook hun clienttoepassingen bijwerken om de nieuwe OAuth Server-to-Server referenties te kunnen gebruiken. <ul><li>[Migreren van JWT-gebruikersgegevens (Service Account)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Implementatiehandleiding voor nieuwe en oude toepassingen met OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[De nieuwe OAuth Server-to-Server-referenties gebruiken](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Veelgestelde vragen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |

{style="table-layout:auto"}

## AppMeasurement

Voor de meest recente updates over releases van AppMeasurementen (versie 2.26.0) raadpleegt u [AppMeasurement voor JavaScript-releaseopmerkingen](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html).


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2024](/help/release-notes/2024.md)
* [Opmerkingen bij de release Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De nieuwste release-updates voor [Adobe Experience Cloud-producten](https://business.adobe.com/products/adobe-experience-cloud-products.html)
