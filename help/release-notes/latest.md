---
title: Opmerkingen bij de release van Adobe Analytics
description: De huidige Adobe Analytics-releaseopmerkingen weergeven
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 924f5f670d2f29269a5ba6623079e839f1fe8122
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 3%

---

# Opmerkingen bij de huidige Adobe Analytics-release (release van februari 2025)

**Laatste update**: 21 februari, 2024

Deze releaseopmerkingen hebben betrekking op de periode van 11 februari tot medio maart 2025. De versies van Adobe Analytics werken op a [ ononderbroken leveringsmodel ](releases.md), dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie | Beschrijving | [ Het begin van de Uitvoer ](releases.md) | [ Algemene Beschikbaarheid ](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **het bewaartermijn van identiteitskaart van de Transactie** | De bewaarperiode voor de transactie-id van 90 dagen werd verlengd tot 25 maanden. De `transactionID` variabele identificeert uniek een transactie zodat kan de slag aan gegevens verbinden die door Gegevensbronnen worden geupload. Leer meer [ hier ](https://experienceleague.adobe.com/en/docs/analytics/implementation/vars/page-vars/transactionid) en [ hier ](https://experienceleague.adobe.com/en/docs/analytics/import/data-sources/transactionid). |  | vrijdag 20 februari 2025 |
| **de Vervoer API van Gegevens verwijzing** | De [ verwijzing ](https://adobedocs.github.io/analytics-2.0-apis/?urls.primaryName=Data%20Feeds%20APIs) voor de feeds API van Gegevens is nu beschikbaar. |  | vrijdag 30 januari 2025 |
| **LiveStream API - de implementatie van de Cliënt** | Gebruik de LiveStream-clientimplementatie om LiveStream-gegevens te gebruiken. [Meer informatie](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/livestream/clientcode/) |  | woensdag 18 februari 2025 |
| **Update aan Classificaties API** | U kunt nu afzonderlijke classificatievelden of -toetsen verwijderen van de server. Dit verstrekt een alternatief aan het schrappen van een volledige classificatiedataset met de methode van DELETE. [Meer informatie](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/classifications/remove-values/) |  | woensdag 18 februari 2025 |


## Oplossingen in Adobe Analytics

**Analysis Workspace**: AN-359974; AN-366212; AN-368460
**Classificaties**: AN-367186; AN-367328; AN-368548
**migratie van de Component**: AN-364529; AN-366398; AN-367509;
**Diefstal van Gegevens**: AN-365685; AN-366745; AN-367256; AN-367349; AN-368363
**Data Warehouse**: AN-368178; AN-368331;
**Mobiele app**: AN-367137
**Platform**: AN-351924; AN-365540; AN-365866; AN-366898; AN-367856; AN-367933
**Report Builder**: AN-366456; AN-36655;
**Virtuele Reeksen van het Rapport**: AN-367411
**VISTA regels**: AN-365331

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders {#admin}

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **Opkomende update van het veld Contextgegevens voor Analytics`a.locale`** | zaterdag 21 februari 2025 | Op 5 maart 2025 wordt een update uitgevoerd naar de instelling van het gegevensveld Analytics context `a.locale` bij het verzamelen van gegevens via Experience Edge. Wanneer gegevens naar Adobe Analytics worden verzonden met de functie Experience Edge, worden de velden Analytics gevuld op basis van een toewijzing van XDM-velden. De toewijzing voor `c.a.locale` verwijst naar een niet-standaard XDM-veld, `xdm.environment.language` . Dit veld wordt bijgewerkt om naar het juiste veld te verwijzen, `xdm.environment._dc.language` .  De toewijzing zal `xdm.environment.language` voor achterwaartse verenigbaarheid blijven van verwijzingen voorzien. Als beide velden zijn ingesteld, heeft `xdm.environment.language` voor de continuïteit voorrang. U kunt de volledige lijst van afbeeldingen van XDM aan standaardgebieden van Analytics [ hier ](https://experienceleague.adobe.com/en/docs/analytics/implementation/aep-edge/xdm-var-mapping) bekijken. |
| **niet-Campagneklanten zullen toegang tot Triggers verliezen** | dinsdag 16 oktober 2023 | Op 30 Januari, 2025, verliezen de klanten van Adobe Analytics die geen Adobe Campaign vergunning hebben toegang tot de capaciteit om [ Trekkers ](https://experienceleague.adobe.com/en/docs/core-services/interface/services/triggers) te vormen en te verbruiken. Klanten moeten campagne aanschaffen of het gebruik van Triggers stopzetten of andere Adobe-tools die Triggers-mogelijkheden bieden, bekijken. |

## Aankondigingen van einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Migratie aan de geloofsbrieven van Server-aan-Server van Adobe I/O OAuth** | zaterdag 17 januari 2025 | Adobe Analytics API en Livestream klanten die de geloofsbrieven van Adobe I/O JWT gebruiken moeten aan de geloofsbrieven van Adobe I/O OAuth Server-aan-Server door **30 Juni, 2025** migreren. Adobe I/O staat niet toe dat vanaf 1 mei 2024 nieuwe JWT-referenties worden gemaakt. Klanten die JWT gebruiken moeten een nieuwe Server-aan-Server referentie OAuth tot stand brengen of hun bestaande JWT-referentie migreren naar een OAuth Server-aan-Server referentie. Klanten moeten ook hun clienttoepassingen bijwerken om de nieuwe OAuth Server-to-Server referenties te kunnen gebruiken. <ul><li>[ migrerend van de Rekening van de Dienst (JWT) geloofsbrieven ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[ gids van de Implementatie voor nieuwe en oude toepassingen met OAuth ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[ Gebruikend de nieuwe Server-aan-Server geloofsbrieven OAuth ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[ FAQs ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |
| **EOL voor Adobe Analytics API (versie 1.4)** | donderdag 17 juli 2024 | Op **12 augustus, 2026**, zullen de volgende Analytics Verouderde API diensten hun eind van het leven bereiken en zullen worden gesloten, en de huidige integratie die gebruikend deze diensten wordt gebouwd zal ophouden werkend:<ul><li>Adobe Analytics API (versie 1.4)</li><li>Adobe Analytics WSSE-verificatie</li></ul><p>De integratie die Adobe Analytics API (versie 1.4) gebruiken moet aan [ Adobe Analytics 2.0 API ](https://developer.adobe.com/analytics-apis/docs/2.0/) migreren, terwijl de integratie WSSE aan een op OAuth-Gebaseerd authentificatieprotocol in [ Adobe Developer Console ](https://developer.adobe.com/console) moet migreren.</p><p>Zie [ Adobe Analytics 1.4 API EOL FAQ ](/help/admin/c-admin-api/c-admin-14-api-eol.md) voor antwoorden op gemeenschappelijke vragen en verdere begeleiding.</p> |


## AppMeasurement

Voor de recentste updates op de versies van AppMeasurement (Versie 2.26.0), gelieve te verwijzen naar [ AppMeasurement voor de versienota&#39;s van JavaScript ](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html).


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2024](/help/release-notes/2024.md)
* [ de versienota&#39;s van Customer Journey Analytics ](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [ het stromen de versienota&#39;s van de Inzameling van Media ](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De recentste versie werkt voor [ producten van Adobe Experience Cloud ](https://business.adobe.com/products/adobe-experience-cloud-products.html) bij
