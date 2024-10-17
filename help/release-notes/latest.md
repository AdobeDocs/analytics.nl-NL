---
title: Opmerkingen bij de release van Adobe Analytics
description: De huidige Adobe Analytics-releaseopmerkingen weergeven
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: ae03f0d9e5f22c8e8ff6550a33a6f9d18432f46f
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 3%

---

# Opmerkingen bij de huidige Adobe Analytics-release (oktober 2024)

**Laatste update**: 17 oktober 2024

Deze opmerkingen hebben betrekking op de releaseperiode van 2 oktober 2024 tot en met 22 oktober 2024. De versies van Adobe Analytics werken op a [ ononderbroken leveringsmodel ](releases.md), dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie | Beschrijving | [ Het begin van de Uitvoer ](releases.md) | [ Algemene Beschikbaarheid ](releases.md) |
| ----------- | ---------- | ------- | ---- |
| Nieuwe Report Builder voor Adobe Analytics | De nieuwe Report Builder-toepassing biedt Adobe Analytics bijgewerkte functies, zoals verbeterde prestaties, gestroomlijnde gebruikersinterface, 2.0 API-ondersteuning en ondersteuning voor Microsoft Excel in Mac-, Windows- en webbrowsers. [Meer informatie](https://experienceleague.adobe.com/en/docs/analytics/analyze/report-builder/report-buider-overview) |  | donderdag 16 oktober 2024 |

## Oplossingen in Adobe Analytics

Analysis Workspace: AN-343611; AN-355870; AN-357100; AN-358364; AN-358756; AN-359269
Analytics Mobile App: AN-354085
Classificaties: AN-353074; AN-357533; AN-358308; AN-358350; AN-358732; AN-358925; AN-359249
Apparaatanalyse: AN-357968
Gegevensdoorvoer: AN-358489; AN-358542
Data Warehouse: AN-352181; AN-356701; AN-356802; AN-356804; AN-359162

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders {#admin}

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **de Extra gebieden XDM van het implementatiedetail automatisch in kaart gebracht** | donderdag 11 september 2024 | Als u de Adobe Experience Platform-Edge Network gebruikt om gegevens naar Adobe Analytics te verzenden, worden de XDM-velden `xdm.implementationdetails.name` en `xdm.implementationdetails.environment` nu altijd toegewezen aan contextgegevensvariabelen `c.a.x.implementationdetails.name` en `c.a.x.implementationdetails.environment` . Voorheen konden deze waarden in sommige scenario&#39;s niet worden gevuld. Pas de relevante verwerkingsregels aan om rekening te houden met de beschikbaarheid van deze waarden. |

{style="table-layout:auto"}

## Aankondigingen van einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **EOL voor Adobe Analytics API (versie 1.4)** | donderdag 17 juli 2024 | Op **12 augustus, 2026**, zullen de volgende Analytics Verouderde API diensten hun eind van het leven bereiken en zullen worden gesloten, en de huidige integratie die gebruikend deze diensten wordt gebouwd zal ophouden werkend:<ul><li>Adobe Analytics API (versie 1.4)</li><li>Adobe Analytics WSSE-verificatie</li></ul><p>De integratie die Adobe Analytics API (versie 1.4) gebruiken moet aan [ Adobe Analytics 2.0 API ](https://developer.adobe.com/analytics-apis/docs/2.0/) migreren, terwijl de integratie WSSE aan een op OAuth-Gebaseerd authentificatieprotocol in [ Adobe Developer Console ](https://developer.adobe.com/console) moet migreren.</p><p>Zie [ Adobe Analytics 1.4 API EOL FAQ ](/help/admin/c-admin-api/c-admin-14-api-eol.md) voor antwoorden op gemeenschappelijke vragen en verdere begeleiding.</p> |
| **Migratie aan Adobe I/O OAuth Server-aan-Server geloofsbrieven** | vrijdag 11 mei 2023 | Adobe Analytics API en Livestream klanten die de geloofsbrieven van Adobe I/O JWT gebruiken moeten aan de geloofsbrieven van Adobe I/O OAuth Server-aan-Server door **Januari 1, 2025** migreren. Adobe I/O staat niet toe dat vanaf 1 mei 2024 nieuwe JWT-referenties worden gemaakt. Klanten die JWT gebruiken moeten een nieuwe Server-aan-Server referentie OAuth tot stand brengen of hun bestaande JWT-referentie migreren naar een OAuth Server-aan-Server referentie. Klanten moeten ook hun clienttoepassingen bijwerken om de nieuwe OAuth Server-to-Server referenties te kunnen gebruiken. <ul><li>[ migrerend van de Rekening van de Dienst (JWT) geloofsbrieven ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[ gids van de Implementatie voor nieuwe en oude toepassingen met OAuth ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[ Gebruikend de nieuwe Server-aan-Server geloofsbrieven OAuth ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[ FAQs ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |

{style="table-layout:auto"}

## AppMeasurement

Voor de recentste updates op de versies van het AppMeasurement (Versie 2.26.0), gelieve te verwijzen naar [ AppMeasurement voor de versienota&#39;s van JavaScript ](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html).


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2024](/help/release-notes/2024.md)
* [ de versienota&#39;s van de Customer Journey Analytics ](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [ het stromen toe:voegen-op versienota&#39;s van de Inzameling van Media ](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De recentste versie werkt voor [ producten van Adobe Experience Cloud ](https://business.adobe.com/products/adobe-experience-cloud-products.html) bij
