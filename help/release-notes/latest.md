---
title: Opmerkingen bij de release van Adobe Analytics
description: De huidige Adobe Analytics-releaseopmerkingen weergeven
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: c8d38d67590c0422ed898d20ffa788b5fd34041c
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 2%

---

# Opmerkingen bij de huidige Adobe Analytics-release (23 oktober 2024)

**Laatste update**: 23 oktober 2024

Deze releaseopmerkingen hebben betrekking op de releaseperiode van 16 oktober 2024 tot eind 2024. De versies van Adobe Analytics werken op a [ ononderbroken leveringsmodel ](releases.md), dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie | Beschrijving | [ Het begin van de Uitvoer ](releases.md) | [ Algemene Beschikbaarheid ](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Nieuwe Report Builder voor Adobe Analytics** | De nieuwe Report Builder-toepassing brengt Adobe Analytics een belangrijke update met zich mee, waaronder verbeterde prestaties, gestroomlijnde gebruikersinterface, 2.0 API-ondersteuning en ondersteuning voor Microsoft Excel in Mac, Windows en webbrowsers. Deze toepassing kan samen met de oudere toepassing worden gebruikt, maar niet op hetzelfde bestand. Een verbeteringseigenschap wordt verstrekt om erfeniswerkboeken aan de nieuwe toepassing te bevorderen. [Meer informatie](https://experienceleague.adobe.com/en/docs/analytics/analyze/report-builder/report-buider-overview) |  | donderdag 16 oktober 2024 |
| **de Uitvoer JSON voor het migreren van markeringsimplementatie aan de markeringen van SDK van het Web** | Deze update van de extensie Analytics heeft betrekking op de migratie naar de SDK van Web. U kunt deze update naar de Adobe Analytics-extensie gebruiken als onderdeel van uw workflow om extensieconfiguraties opnieuw te maken met de Web SDK-extensie. In de uitbreiding met Adobe Analytics-tags kunt u Vars, props en gebeurtenissen weergeven als JSON, die kan worden geëxporteerd voor bewerking en kan worden opgenomen in de Web SDK-extensie. |  | donderdag 23 oktober 2024 |

## Oplossingen in Adobe Analytics

Analysis Workspace: AN-356287; AN-358435; AN-359456; AN-359826; AN-360215
Hulpmiddelen Admin: AN-342485; AN-347931; AN-348704; AN-357723; AN-358453; AN-358717; AN-35954 8; AN-360136
Indelingen: AN-359025; AN-359283; AN-359368; AN-359710; AN-359752; AN-359759; AN-35979 AN-359887; AN-360543; AN-360566; AN-360612; AN-360741; AN-360942; AN-360952
Apparaatanalyse: AN-359210
Kenmerken van de klant: AN-357897
Gegevensverzameling: AN-351131; AN-351309; AN-355678; AN-359856
Gegevensinvoer: AN-359699
API voor gegevensherstel: AN-360256
Gegevensbronnen: AN-359290
Data Warehouse: AN-359820
Overlopende waarschuwingen: AN-358132

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders {#admin}

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **niet-Campagneklanten zullen toegang tot Triggers verliezen** | dinsdag 16 oktober 2023 | Op 30 januari 2025 verliezen Adobe Analytics-klanten die geen Adobe Campaign-licentie hebben, de toegang tot het configureren en gebruiken van Triggers. Klanten moeten campagne aanschaffen of het gebruik van Triggers stopzetten of andere Adoben die Triggers-mogelijkheden bieden, bekijken. |
| **de Extra gebieden XDM van het implementatiedetail automatisch in kaart gebracht** | donderdag 11 september 2024 | Als u de Adobe Experience Platform-Edge Network gebruikt om gegevens naar Adobe Analytics te verzenden, worden de XDM-velden `xdm.implementationdetails.name` en `xdm.implementationdetails.environment` nu altijd toegewezen aan contextgegevensvariabelen `c.a.x.implementationdetails.name` en `c.a.x.implementationdetails.environment` . Voorheen konden deze waarden in sommige scenario&#39;s niet worden gevuld. Pas de relevante verwerkingsregels aan om rekening te houden met de beschikbaarheid van deze waarden. |

## Aankondigingen van einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **EOL voor Adobe Analytics API (versie 1.4)** | donderdag 17 juli 2024 | Op **12 augustus, 2026**, zullen de volgende Analytics Verouderde API diensten hun eind van het leven bereiken en zullen worden gesloten, en de huidige integratie die gebruikend deze diensten wordt gebouwd zal ophouden werkend:<ul><li>Adobe Analytics API (versie 1.4)</li><li>Adobe Analytics WSSE-verificatie</li></ul><p>De integratie die Adobe Analytics API (versie 1.4) gebruiken moet aan [ Adobe Analytics 2.0 API ](https://developer.adobe.com/analytics-apis/docs/2.0/) migreren, terwijl de integratie WSSE aan een op OAuth-Gebaseerd authentificatieprotocol in [ Adobe Developer Console ](https://developer.adobe.com/console) moet migreren.</p><p>Zie [ Adobe Analytics 1.4 API EOL FAQ ](/help/admin/c-admin-api/c-admin-14-api-eol.md) voor antwoorden op gemeenschappelijke vragen en verdere begeleiding.</p> |
| **Migratie aan Adobe I/O OAuth Server-aan-Server geloofsbrieven** | vrijdag 11 mei 2023 | Adobe Analytics API en Livestream klanten die de geloofsbrieven van Adobe I/O JWT gebruiken moeten aan de geloofsbrieven van Adobe I/O OAuth Server-aan-Server door **Januari 1, 2025** migreren. Adobe I/O staat niet toe dat vanaf 1 mei 2024 nieuwe JWT-referenties worden gemaakt. Klanten die JWT gebruiken moeten een nieuwe Server-aan-Server referentie OAuth tot stand brengen of hun bestaande JWT-referentie migreren naar een OAuth Server-aan-Server referentie. Klanten moeten ook hun clienttoepassingen bijwerken om de nieuwe OAuth Server-to-Server referenties te kunnen gebruiken. <ul><li>[ migrerend van de Rekening van de Dienst (JWT) geloofsbrieven ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[ gids van de Implementatie voor nieuwe en oude toepassingen met OAuth ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[ Gebruikend de nieuwe Server-aan-Server geloofsbrieven OAuth ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[ FAQs ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |


## AppMeasurement

Voor de recentste updates op de versies van het AppMeasurement (Versie 2.26.0), gelieve te verwijzen naar [ AppMeasurement voor de versienota&#39;s van JavaScript ](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html).


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2024](/help/release-notes/2024.md)
* [ de versienota&#39;s van de Customer Journey Analytics ](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [ het stromen toe:voegen-op versienota&#39;s van de Inzameling van Media ](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De recentste versie werkt voor [ producten van Adobe Experience Cloud ](https://business.adobe.com/products/adobe-experience-cloud-products.html) bij
