---
title: Opmerkingen bij de release van Adobe Analytics
description: De huidige Adobe Analytics-releaseopmerkingen weergeven
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 9c6da2c1ed5bc2c016da16a5bb821f0064e1ae4f
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 2%

---

# Huidige Adobe Analytics-releaseopmerkingen (release mei 2025)

**Laatste update**: 14 mei 2025

Deze releaseopmerkingen betreffen de releaseperiode van april xx tot en met 18 juni 2025. De versies van Adobe Analytics werken op a [ ononderbroken leveringsmodel ](releases.md), dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie | Beschrijving | [ Het begin van de Uitvoer ](releases.md) | [ Algemene Beschikbaarheid ](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **verlaten paneel van Analysis Workspace opent niet meer en sluit op aanwijzen** | Het linkerdeelvenster in Analysis Workspace wordt gebruikt om onderdelen, deelvensters en visualisaties aan uw project toe te voegen. De optie om het linkerdeelvenster tijdelijk te openen door de muisaanwijzer op een van de pictogrammen aan de linkerkant te plaatsen, is niet meer beschikbaar. Klik in plaats daarvan gewoon op een van deze pictogrammen om het deelvenster open te houden en klik vervolgens op hetzelfde pictogram om het te sluiten. |  | vrijdag 29 mei 2025 |


## Oplossingen in Adobe Analytics

**Alarm**: AN-378351
**Analysis Workspace**: AN-363521; AN-367366; AN-373575; AN-374238; AN-374295; AN-374382; AN-376 938; AN-377176; AN-377467; AN-377942
**overdracht van activa**: AN-373381
**Classificaties**: AN-373166; AN-373479; AN-376074; AN-377337; AN-377505
**Componenten**: AN-314468
**het voer van Gegevens**: AN-370241; AN-375267; AN-376940
**Gegevensbronnen**: AN-375259
**Data Warehouse**: AN-370415; AN-372090;
**Platform**: AN-365681; AN-372306; AN-372616;
**Real-time rapporterend**: AN-365681
**Report Builder**: AN-371395
**Segmentatie**: AN-373576; AN-375858
**Virtuele rapportsuites**: AN-377948; AN-377952
**Regels van Vista**: AN-373292

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders {#admin}

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **verlaten paneel van Analysis Workspace opent niet meer en sluit op aanwijzen** | Het linkerdeelvenster in Analysis Workspace wordt gebruikt om onderdelen, deelvensters en visualisaties aan uw project toe te voegen. De optie om het linkerdeelvenster tijdelijk te openen door de muisaanwijzer op een van de pictogrammen aan de linkerkant te plaatsen, is niet meer beschikbaar. Klik in plaats daarvan gewoon op een van deze pictogrammen om het deelvenster open te houden en klik vervolgens op hetzelfde pictogram om het te sluiten. |  | vrijdag 29 mei 2025 |


## Aankondigingen van einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Toegang via erfenisdomeinen of via erfenisSSO** | vrijdag 10 april 2025 | Adobe is van plan om bij te werken hoe gebruikers Adobe Analytics openen om de beveiliging te verbeteren en uw aanmeldingservaring te stroomlijnen. Als deel van deze inspanning, zal de toegang via erfenisdomeinen of via erfenisSSO, met inbegrip van `my.omniture.com`, permanent worden beëindigd op **2 Januari, 2026**. Na deze datum werken de oude aanmeldingsgegevens en de oudere SSO niet meer. Alle gebruikers moeten zich via `experience.adobe.com` aanmelden met hun Adobe Experience Cloud-id&#39;s. Als u hulp met uw identiteitskaart van Experience Cloud nodig hebt, gelieve de beheerder van Adobe Analytics van uw organisatie of [ de Zorg van de Klant van Adobe ](https://helpx.adobe.com/contact.html) te contacteren. |
| **Migratie aan de geloofsbrieven van Server-aan-Server van Adobe I/O OAuth** | zaterdag 17 januari 2025 | Adobe Analytics API en Livestream klanten die de geloofsbrieven van Adobe I/O JWT gebruiken moeten aan de geloofsbrieven van Adobe I/O OAuth Server-aan-Server door **30 Juni, 2025** migreren. Adobe I/O staat niet toe dat vanaf 1 mei 2024 nieuwe JWT-referenties worden gemaakt. Klanten die JWT gebruiken moeten een nieuwe Server-aan-Server referentie OAuth tot stand brengen of hun bestaande JWT-referentie migreren naar een OAuth Server-aan-Server referentie. Klanten moeten ook hun clienttoepassingen bijwerken om de nieuwe OAuth Server-to-Server referenties te kunnen gebruiken. <ul><li>[ migrerend van de Rekening van de Dienst (JWT) geloofsbrieven ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration)</li><li>[ gids van de Implementatie voor nieuwe en oude toepassingen met OAuth ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation)<li>[ Gebruikend de nieuwe Server-aan-Server geloofsbrieven OAuth ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation)</li><li>[ FAQs ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs)</li></ul> |
| **EOL voor Adobe Analytics API (versie 1.4)** | donderdag 17 juli 2024 | Op **12 augustus, 2026**, zullen de volgende Analytics Verouderde API diensten hun eind van het leven bereiken en zullen worden gesloten, en de huidige integratie die gebruikend deze diensten wordt gebouwd zal ophouden werkend:<ul><li>Adobe Analytics API (versie 1.4)</li><li>Adobe Analytics WSSE-verificatie</li></ul><p>De integratie die Adobe Analytics API (versie 1.4) gebruiken moet aan [ Adobe Analytics 2.0 API ](https://developer.adobe.com/analytics-apis/docs/2.0/) migreren, terwijl de integratie WSSE aan een op OAuth-Gebaseerd authentificatieprotocol in [ Adobe Developer Console ](https://developer.adobe.com/console) moet migreren.</p><p>Zie [ Adobe Analytics 1.4 API EOL FAQ ](/help/admin/c-admin-api/c-admin-14-api-eol.md) voor antwoorden op gemeenschappelijke vragen en verdere begeleiding.</p> |


## AppMeasurement

Voor de recentste updates op de versies van AppMeasurement, gelieve te verwijzen naar [ de versienota&#39;s van AppMeasurement ](https://github.com/adobe/appmeasurement/releases).


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2025](/help/release-notes/2025.md)
* [ de versienota&#39;s van Customer Journey Analytics ](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [ het stromen de versienota&#39;s van de Inzameling van Media ](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De recentste versie werkt voor [ producten van Adobe Experience Cloud ](https://business.adobe.com/products/adobe-experience-cloud-products.html) bij
