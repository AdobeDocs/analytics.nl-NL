---
title: Opmerkingen bij de release van Adobe Analytics
description: De huidige Adobe Analytics-releaseopmerkingen weergeven
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: ebe6716a3dde89d7212385c25044fb533d7737c2
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 1%

---

# Huidige Adobe Analytics-releaseopmerkingen (release van juli 2025)

**Laatste update**: 16 juli 2025

Deze releaseopmerkingen hebben betrekking op de periode van 7 juli tot en met 15 augustus 2025. De versies van Adobe Analytics werken op a [ ononderbroken leveringsmodel ](releases.md), dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie | Beschrijving | [ Het begin van de Uitvoer ](releases.md) | [ Algemene Beschikbaarheid ](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Livestream TNT Gebieden met algoritmen** | Livestream wordt vernieuwd om ervoor te zorgen dat de technologie modern en stabiel blijft. Als deel van dat verfrist zich, als uw gebied van TNT een algoritme in het heeft, zullen wij beginnen opnemend het gebied van TNT in output Livestream. Dit omvat echter alleen de eerder ondersteunde elementen: `campaignId`, `recipeId`, `trafficType`, `actionId` en `actionName` . Het algemene TNT-schema voor LiveStream blijft ongewijzigd. |   | Juli 7,2025 |
| **bijgewerkte navigatie aan de Attributen UI van de Klant** | De gebruikersinterface Klantkenmerken is nu rechtstreeks toegankelijk vanuit de toepassingskiezer in Adobe Experience Cloud. | woensdag 1 juli 2025 | TBD |

## Oplossingen in Adobe Analytics

**Activity Map**: AN-360987
**Analysis Workspace**: AN-378094; AN-380979; AN-382908; AN-387652;
**classificaties**: AN-382412; AN-383157; AN-384616; AN-384803; AN-385933; AN-387320; AN-387 351; AN-387832; AN-387833; AN-387839; AN-387915;
**de inzameling van Gegevens**: AN-387661
**het voer van Gegevens**: AN-375172; AN-384369; AN-387859; AN-387952; AN-388155;
**Platform**: AN-382813; AN-386627; AN-386815
**Privacy**: AN-384390
**Report Builder**: AN-388035
**het Melden**: AN-380441
**Geplande rapporten**: AN-378280; AN-378331
**vergelijking van het segment**: AN-368766


## Aankondigingen van einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Verouderde Report Builder** | donderdag 18 juni 2025 | De oude Report Builder-add-in wordt in juni 2026 opgeheven. Alle gebruikers zouden moeten beginnen hun erfeniswerkboeken aan [ nieuwe Report Builder ](https://experienceleague.adobe.com/nl/docs/analytics/analyze/report-builder/rb-overview) te bevorderen. De nieuwe Report Builder is beschikbaar voor zowel Adobe Analytics- als Customer Journey Analytics-klanten. Het heeft [ dichtbij eigenschappariteit ](https://experienceleague.adobe.com/nl/docs/analytics/analyze/report-builder/convert-workbooks#unsupported) plus vele nieuwe geschikte eigenschappen en verbeteringen UI. Om het verbeteringsproces te vergemakkelijken, omvat de nieuwe Report Builder een gemakkelijke werkboekomzettingseigenschap. De nieuwe Report Builder is alleen beschikbaar als add-in via de Microsoft Store. Vele organisaties vereisen een intern goedkeuringsproces alvorens toe:voegen-binnen ter beschikking kan worden gesteld aan gebruikers. Wacht tijd en werk nu met uw organisatie om ervoor te zorgen dat u voldoende tijd hebt om uw werkboeken te upgraden vóór de EOL-datum. |
| **Toegang via erfenisdomeinen of via erfenisSSO** | vrijdag 10 april 2025 | Adobe is van plan om bij te werken hoe gebruikers Adobe Analytics openen om de beveiliging te verbeteren en uw aanmeldingservaring te stroomlijnen. Als deel van deze inspanning, zal de toegang via erfenisdomeinen of via erfenisSSO, met inbegrip van `my.omniture.com`, permanent worden beëindigd op **2 Januari, 2026**. Na deze datum werken de oude aanmeldingsgegevens en de oudere SSO niet meer. Alle gebruikers moeten zich via `experience.adobe.com` aanmelden met hun Adobe Experience Cloud-id&#39;s. Als u hulp met uw identiteitskaart van Experience Cloud nodig hebt, gelieve de beheerder van Adobe Analytics van uw organisatie of [ de Zorg van de Klant van Adobe ](https://helpx.adobe.com/nl/contact.html) te contacteren. |
| **Adobe Analytics API (versie 1.4)** | donderdag 17 juli 2024 | Op **12 augustus, 2026**, zullen de volgende Analytics Verouderde API diensten hun eind van het leven bereiken en zullen worden gesloten, en de huidige integratie die gebruikend deze diensten wordt gebouwd zal ophouden werkend:<ul><li>Adobe Analytics API (versie 1.4)</li><li>Adobe Analytics WSSE-verificatie</li></ul><p>De integratie die Adobe Analytics API (versie 1.4) gebruiken moet aan [ Adobe Analytics 2.0 API ](https://developer.adobe.com/analytics-apis/docs/2.0/) migreren, terwijl de integratie WSSE aan een op OAuth-Gebaseerd authentificatieprotocol in [ Adobe Developer Console ](https://developer.adobe.com/console) moet migreren.</p><p>Zie [ Adobe Analytics 1.4 API EOL FAQ ](/help/admin/c-admin-api/c-admin-14-api-eol.md) voor antwoorden op gemeenschappelijke vragen en verdere begeleiding.</p> |


## AppMeasurement

Voor de recentste updates op de versies van AppMeasurement, gelieve te verwijzen naar [ de versienota&#39;s van AppMeasurement ](https://github.com/adobe/appmeasurement/releases).


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2025](/help/release-notes/2025.md)
* [ de versienota&#39;s van Customer Journey Analytics ](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=nl-NL)
* [ het stromen de versienota&#39;s van de Inzameling van Media ](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=nl-NL)
* De recentste versie werkt voor [ producten van Adobe Experience Cloud ](https://business.adobe.com/products/adobe-experience-cloud-products.html) bij
