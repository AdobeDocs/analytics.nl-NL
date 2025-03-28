---
title: Opmerkingen bij de release van Adobe Analytics
description: De huidige Adobe Analytics-releaseopmerkingen weergeven
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: e0f6b7b5b2933add7f67873a945b78e4200116eb
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 3%

---

# Huidige Adobe Analytics-releaseopmerkingen (release van maart 2025)

**Laatste update**: 12 Maart, 2025

Deze opmerkingen hebben betrekking op de vrijgaveperiode van 5 maart tot en met 5 mei 2025. De versies van Adobe Analytics werken op a [ ononderbroken leveringsmodel ](releases.md), dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie | Beschrijving | [ Het begin van de Uitvoer ](releases.md) | [ Algemene Beschikbaarheid ](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Update aan het gebied van de contextgegevens van Analytics`a.locale`** | Deze update wijzigt hoe het gegevensveld Analytics-context `a.locale` wordt ingesteld bij het verzamelen van gegevens via Experience Edge. Wanneer gegevens naar Adobe Analytics worden verzonden met de functie Experience Edge, worden de velden Analytics gevuld op basis van een toewijzing van XDM-velden. De toewijzing voor `c.a.locale` verwijst naar een niet-standaard XDM-veld, `xdm.environment.language` . Dit veld wordt bijgewerkt om naar het juiste veld te verwijzen, `xdm.environment._dc.language` .<p>De toewijzing zal `xdm.environment.language` voor achterwaartse verenigbaarheid blijven van verwijzingen voorzien. Als beide velden zijn ingesteld, heeft `xdm.environment.language` voor de continuïteit voorrang. U kunt de volledige lijst van afbeeldingen van XDM aan standaardgebieden van Analytics [ hier ](https://experienceleague.adobe.com/en/docs/analytics/implementation/aep-edge/xdm-var-mapping) bekijken. | | donderdag 5 maart 2025 |
| **de verbeteringsgids van Customer Journey Analytics** | Hiermee kunt u een stapsgewijze gids genereren voor het upgraden van Adobe Analytics naar Customer Journey Analytics. Deze handleiding is toegesneden op uw organisatie en houdt rekening met uw huidige Adobe Analytics-omgeving, uw beoogde gebruik voor Customer Journey Analytics en eventuele tijdbesparende afwegingen die uw organisatie wil maken.<p>Als u uw aangepaste hulplijn wilt genereren, meldt u zich aan bij [!DNL Customer Journey Analytics] en selecteert u vervolgens **[!UICONTROL Upgrade to Customer Journey Analytics]** op het tabblad **[!UICONTROL Workspace]** .<p>[Meer informatie](https://experienceleague.adobe.com/en/docs/analytics-platform/using/compare-aa-cja/upgrade-to-cja/cja-upgrade-recommendations#recommended-upgrade-steps-for-most-organizations) |  | woensdag 11 maart 2025 |
| **Data Warehouse-slechts afmetingen** | Met ingang van mei 2025 begint Adobe met het instellen van afmetingen (aangepaste variabelen zoals eVars en props) die een zeer grote kardinaliteit hebben als alleen Data Warehouse. Variabelen met een hoge cardinaliteit hebben veel verschillende waarden, zoals tijdstempels of UUID&#39;s. Deze afmetingen zijn niet meer beschikbaar voor rapportage in Analysis Workspace.<p>Kandidaten voor deze verandering zijn dimensies die de laag-verkeersgrenzen zeer vroeg in de maand overschrijden. Met deze typen dimensies zijn rapporten in Analysis Workspace die op die dimensie zijn gebaseerd, niet nuttig omdat de te rapporteren gegevens slechts een smalle segment van de oorspronkelijke waarden vertegenwoordigen die zijn verzameld.<p>Aangezien Data Warehouse geen lage verkeersgrenzen oplegt, kunt u nuttige rapporten of segmenten nog bouwen die op deze types van dimensies worden gebaseerd. | | Mei 2025 |


## Oplossingen in Adobe Analytics

**Activity Map**: AN-361038
**Hulpmiddelen Admin**: AN-362178; AN-369483
**Analytics API 1.4**: AN-369615
**Analysis Workspace**: AN-353491; AN-363403; AN-367230; AN-367313; AN-368582; AN-369821; AN-370 227;
**Classificaties**: AN-369848; AN-370196; AN-370226; AN-370437
**de Eendelen van Gegevens**: AN-366162; AN-368906; AN-369066; AN-369087; AN-369225; AN-36978
**Beheer van Gegevens**: AN-365157
**Gegevensbronnen**: AN-367550
**Platform**: AN-363931
**Report Builder**: AN-367460; AN-368975

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders {#admin}

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| N.v.t. |  |  |

## Aankondigingen van einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Migratie aan de geloofsbrieven van Server-aan-Server van Adobe I/O OAuth** | zaterdag 17 januari 2025 | Adobe Analytics API en Livestream klanten die de geloofsbrieven van Adobe I/O JWT gebruiken moeten aan de geloofsbrieven van Adobe I/O OAuth Server-aan-Server door **30 Juni, 2025** migreren. Adobe I/O staat niet toe dat vanaf 1 mei 2024 nieuwe JWT-referenties worden gemaakt. Klanten die JWT gebruiken moeten een nieuwe Server-aan-Server referentie OAuth tot stand brengen of hun bestaande JWT-referentie migreren naar een OAuth Server-aan-Server referentie. Klanten moeten ook hun clienttoepassingen bijwerken om de nieuwe OAuth Server-to-Server referenties te kunnen gebruiken. <ul><li>[ migrerend van de Rekening van de Dienst (JWT) geloofsbrieven ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[ gids van de Implementatie voor nieuwe en oude toepassingen met OAuth ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[ Gebruikend de nieuwe Server-aan-Server geloofsbrieven OAuth ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[ FAQs ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |
| **EOL voor Adobe Analytics API (versie 1.4)** | donderdag 17 juli 2024 | Op **12 augustus, 2026**, zullen de volgende Analytics Verouderde API diensten hun eind van het leven bereiken en zullen worden gesloten, en de huidige integratie die gebruikend deze diensten wordt gebouwd zal ophouden werkend:<ul><li>Adobe Analytics API (versie 1.4)</li><li>Adobe Analytics WSSE-verificatie</li></ul><p>De integratie die Adobe Analytics API (versie 1.4) gebruiken moet aan [ Adobe Analytics 2.0 API ](https://developer.adobe.com/analytics-apis/docs/2.0/) migreren, terwijl de integratie WSSE aan een op OAuth-Gebaseerd authentificatieprotocol in [ Adobe Developer Console ](https://developer.adobe.com/console) moet migreren.</p><p>Zie [ Adobe Analytics 1.4 API EOL FAQ ](/help/admin/c-admin-api/c-admin-14-api-eol.md) voor antwoorden op gemeenschappelijke vragen en verdere begeleiding.</p> |


## AppMeasurement

Voor de recentste updates op de versies van AppMeasurement, gelieve te verwijzen naar [ de versienota&#39;s van AppMeasurement ](https://github.com/adobe/appmeasurement/releases).


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2025](/help/release-notes/2025.md)
* [ de versienota&#39;s van Customer Journey Analytics ](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [ het stromen de versienota&#39;s van de Inzameling van Media ](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De recentste versie werkt voor [ producten van Adobe Experience Cloud ](https://business.adobe.com/products/adobe-experience-cloud-products.html) bij
