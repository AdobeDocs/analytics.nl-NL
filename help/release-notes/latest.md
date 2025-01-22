---
title: Opmerkingen bij de release van Adobe Analytics
description: De huidige Adobe Analytics-releaseopmerkingen weergeven
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: e281d43204e1c5b10508661f04b880125fe8671c
workflow-type: tm+mt
source-wordcount: '866'
ht-degree: 2%

---

# Huidige Adobe Analytics-releaseopmerkingen (release van januari 2025)

**Laatste update**: 22 Januari, 2024

Deze releaseopmerkingen betreffen de releaseperiode van 15 januari tot medio februari 2025. De versies van Adobe Analytics werken op a [ ononderbroken leveringsmodel ](releases.md), dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie | Beschrijving | [ Het begin van de Uitvoer ](releases.md) | [ Algemene Beschikbaarheid ](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **plannend in de nieuwe Report Builder** | Het plannen staat u niet alleen toe om uw nieuwe werkboeken van de Report Builder te plannen. Bovendien kunt u de metagegevens van oude geplande taken ophalen wanneer u oudere werkboeken omzet. Op deze manier, wanneer u uw oudere werkboeken omzet in nieuwe werkboeken en deze plant, stuurt u ze naar dezelfde e-mail en op dezelfde snelheid als de oudere werkboeken. [Meer informatie](/help/analyze/report-builder/schedule-reportbuilder.md) |  | donderdag 22 januari 2025 |
| **Verbeteringen aan Rapporten (die ook als Malplaatjes worden bekend) in Analysis Workspace** | Er zijn nu verschillende verbeteringen beschikbaar voor Rapporten (ook wel sjablonen genoemd):<ul><li>Wordt nu [!UICONTROL Templates] aangeroepen (wordt niet langer [!UICONTROL Reports] genoemd).</li><li>Verbeterde gebruikerservaring voor het weergeven en zoeken van sjablonen, waaronder de optie om sjablonen weer te geven in een kolomweergave of kaartweergave.</li><li>Nieuwe, intuïtievere locatie voor bedrijfssjablonen (bevindt zich onder **[!UICONTROL Workspace]** > **[!UICONTROL Templates]** ).</li><li>Eerder, werden de bedrijfmalplaatjes betreden van de dialoogdoos toen het creëren van een project.</li><li>Er zijn extra vooraf gebouwde sjablonen beschikbaar.</li></ul>[ leer meer ](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/templates/use-templates).<p>Beheerders kunnen sjablonen maken en deze opslaan voor gebruik door anderen in hun aanmeldingsbedrijf. [Meer informatie](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/templates/create-templates) | donderdag 15 januari 2025 | vrijdag 30 januari 2025 |
| **het bewaartermijn van identiteitskaart van de Transactie** | De bewaarperiode voor de transactie-id van 90 dagen wordt verlengd tot 25 maanden in februari 2025. De `transactionID` variabele identificeert uniek een transactie zodat kan de slag aan gegevens verbinden die door Gegevensbronnen worden geupload. (Documentatiekoppelingen die moeten worden gevolgd) |  | woensdag 11 februari 2025 |

## Oplossingen in Adobe Analytics

A4T: AN-355602; AN-365988
Activity Map: AN-365320
Admin Console: AN-363884
Hulpmiddelen Admin: AN-356747; AN-358776
Advertising Analytics: AN-355488
Analysis Workspace: AN-345318; AN-354801; AN-357052; AN-358975; AN-362886; AN-363831; AN-364124; AN-365257; AN-365319; AN-365462
Analytics 1.4 API: AN-358059
Classificaties: AN-360049; AN-360424; AN-362208; AN-362345; AN-362560; AN-362576; AN-36263 AN-362653; AN-362762; AN-362815; AN-362881; AN-362885; AN-362973; AN-36343; AN; 363558; AN-363860; AN-364239; AN-364480; AN-364451; AN-364528; AN-364548; AN-3 364552; AN-364585; AN-364598; AN-364715; AN-364912; AN-364997; AN-365189; AN-36 5197; AN-365203; AN-365431; AN-365647; AN-365794;
Componentmigratie: AN-362236; AN-365429
Bijdrage-analyse: AN-360146
Gegevensinvoer: AN-356997; AN-362470; AN-362498; AN-362775; AN-363323; AN-363413; AN-36356 9; AN-364063; AN-364142; AN-364294; AN-364298; AN-364325; AN-364367; AN-364594; AN-364995; AN-365272; AN-365519; AN-365760; AN-366152;
API voor gegevensherstel: AN-362773; AN-362874
Gegevensbronnen: AN-360745; AN-362202; AN-364566
Data Warehouse: AN-361447; AN-362616; AN-364524; AN-365108
Mobile App: AN-362856; AN-365270
Oplopende waarschuwingen: AN-355594; AN-364547
Platform: AN-358914; AN-360205; AN-362990; AN-364550; AN-365454; AN-365485
Report Builder: AN-363478; AN-364433; AN-365610
Rapportage Activity Manager: AN-362440
Segmentatie: AN-359921
VISTA-regels: AN-362927

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders {#admin}

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **niet-Campagneklanten zullen toegang tot Triggers verliezen** | dinsdag 16 oktober 2023 | Op 30 Januari, 2025, zullen de klanten van Adobe Analytics die geen vergunning van Adobe Campaign hebben toegang tot de capaciteit verliezen om [ Triggers ](https://experienceleague.adobe.com/en/docs/core-services/interface/services/triggers) te vormen en te verbruiken. Klanten moeten campagne aanschaffen of het gebruik van Triggers stopzetten of andere Adoben die Triggers-mogelijkheden bieden, bekijken. |

## Aankondigingen van einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Migratie aan Adobe I/O OAuth Server-aan-Server geloofsbrieven** | zaterdag 17 januari 2025 | Adobe Analytics API en Livestream klanten die de geloofsbrieven van Adobe I/O JWT gebruiken moeten aan de geloofsbrieven van Adobe I/O OAuth Server-aan-Server door **30 Juni, 2025** migreren. Adobe I/O staat niet toe dat vanaf 1 mei 2024 nieuwe JWT-referenties worden gemaakt. Klanten die JWT gebruiken moeten een nieuwe Server-aan-Server referentie OAuth tot stand brengen of hun bestaande JWT-referentie migreren naar een OAuth Server-aan-Server referentie. Klanten moeten ook hun clienttoepassingen bijwerken om de nieuwe OAuth Server-to-Server referenties te kunnen gebruiken. <ul><li>[ migrerend van de Rekening van de Dienst (JWT) geloofsbrieven ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[ gids van de Implementatie voor nieuwe en oude toepassingen met OAuth ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[ Gebruikend de nieuwe Server-aan-Server geloofsbrieven OAuth ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[ FAQs ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |
| **EOL voor Adobe Analytics API (versie 1.4)** | donderdag 17 juli 2024 | Op **12 augustus, 2026**, zullen de volgende Analytics Verouderde API diensten hun eind van het leven bereiken en zullen worden gesloten, en de huidige integratie die gebruikend deze diensten wordt gebouwd zal ophouden werkend:<ul><li>Adobe Analytics API (versie 1.4)</li><li>Adobe Analytics WSSE-verificatie</li></ul><p>De integratie die Adobe Analytics API (versie 1.4) gebruiken moet aan [ Adobe Analytics 2.0 API ](https://developer.adobe.com/analytics-apis/docs/2.0/) migreren, terwijl de integratie WSSE aan een op OAuth-Gebaseerd authentificatieprotocol in [ Adobe Developer Console ](https://developer.adobe.com/console) moet migreren.</p><p>Zie [ Adobe Analytics 1.4 API EOL FAQ ](/help/admin/c-admin-api/c-admin-14-api-eol.md) voor antwoorden op gemeenschappelijke vragen en verdere begeleiding.</p> |


## AppMeasurement

Voor de recentste updates op de versies van het AppMeasurement (Versie 2.26.0), gelieve te verwijzen naar [ AppMeasurement voor de versienota&#39;s van JavaScript ](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html).


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2024](/help/release-notes/2024.md)
* [ de versienota&#39;s van de Customer Journey Analytics ](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [ het stromen de versienota&#39;s van de Inzameling van Media ](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De recentste versie werkt voor [ producten van Adobe Experience Cloud ](https://business.adobe.com/products/adobe-experience-cloud-products.html) bij
