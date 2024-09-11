---
title: Opmerkingen bij de release van Adobe Analytics
description: De huidige Adobe Analytics-releaseopmerkingen weergeven
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 7dd42948073b56a33c1d00f9b4292d1cc3416470
workflow-type: tm+mt
source-wordcount: '747'
ht-degree: 2%

---

# Opmerkingen bij de huidige Adobe Analytics-release (september 2024)


**Laatste update**: 11 september 2024

Deze releaseopmerkingen betreffen de releaseperiode van 11 september 2024 tot begin oktober. De versies van Adobe Analytics werken op a [ ononderbroken leveringsmodel ](releases.md), dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie | Beschrijving | [ Het begin van de Uitvoer ](releases.md) | [ Algemene Beschikbaarheid ](releases.md) |
|--- | --- | --- | --- |
| **Aanvullende informatie in de &quot;Gebruikte in&quot;kolom in de berekende metrische manager en segmentmanager** | De kolom &quot;Gebruikt in&quot;in de berekende metrische manager en segmentmanager bevat de volgende nieuwe rapporteringsgebieden:<ul><li>**Report Builder**: Toont het aantal berekende metriek of segmenten die in de Report Builder worden gebruikt.</li><li>**Ad hoc componenten**: Toont het aantal ad hoc berekende metriek of ad hoc segmenten die in projecten worden gebruikt. Deze ad hoc berekende metriek en segmenten (anders genoemd geworden &quot;snelle berekende metriek&quot;en &quot;snelle segmenten&quot;) kunnen slechts in het project worden gebruikt waar zij werden gecreeerd, zodat zij afzonderlijk van het &quot;Project&quot;rapporteringsgebied in &quot;Gebruikt in&quot;kolom worden gerapporteerd.</li></ul>Voor meer informatie, zie [ Berekende metriekmanager ](https://experienceleague.adobe.com/en/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-manager) en [ de manager van het Segment ](https://experienceleague.adobe.com/en/docs/analytics/components/segmentation/segmentation-workflow/seg-manage). |  | 11 sep. 2024 |
| **Activity Map v3 uitbreiding** | De extensie Activity Map v3 is nu beschikbaar. Als u de v2-extensie hebt geïnstalleerd, verwijdert u deze voordat u de v3-extensie installeert. Navigeer naar **[!UICONTROL Tools]** > **[!UICONTROL Activity Map]** voor de nieuwste versie van de extensie. |  | 3 sep. 2024 |


## Oplossingen in Adobe Analytics

A4T: AN-355736
Activity Map: AN-353779
Analysis Workspace: AN-348485; AN-349693; AN-357247
Analytics Mobile App: AN-352645
Indelingen: AN-355636; AN-355651; AN-355753; AN-356005; AN-356439; AN-356540; AN-35657 AN-356622
Apparaatanalyse: AN-355138
Gegevensdoorvoer: AN-356258; AN-357133
Data Warehouse: AN-339292; AN-353807
Exportlocaties: AN-356912
Privacy API: AN-352420
Report Builder: AN-352555; AN-354316
Geplande projecten: AN-355971
Segmentering: AN-352095;
Doelrapportage: AN-355748

Andere correcties: AN-349698; AN-349880; AN-354860; AN-355355; AN-356289;

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders {#admin}

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **13 maanden verlopen van opgeslagen`cust_visids`** | woensdag 20 augustus 2024 | **Augustus 20, 2024**, versie van de de verwerkingsmotor van het Bewerkingsmechanisme van het Bezit van de Analyse dwingt een 13 maanden vervaldatum van bewaard `cust_visids` af. Als de rapportsuite &#39;Enable Visitor Stitching&#39; heeft ingeschakeld, wordt deze instelling gebruikt om de `cust_visid` for a `visid_high/visid_low value` with no `cust_visid` te vinden op de hit. Eerder was er geen vervaldatum van de toewijzing van een `cust_visid` voor een `visid_high/visid_low` . Als in deze release 13 maanden of meer zijn verstreken sinds `visid_high/visid_low` een `cust_visid` -resultaat heeft gehad, verloopt de toewijzing. |
| **de Extra gebieden XDM van het implementatiedetail automatisch in kaart gebracht** | donderdag 11 september 2024 | Als u de Adobe Experience Platform-Edge Network gebruikt om gegevens naar Adobe Analytics te verzenden, worden de XDM-velden `xdm.implementationdetails.name` en `xdm.implementationdetails.environment` nu altijd toegewezen aan contextgegevensvariabelen `c.a.x.implementationdetails.name` en `c.a.x.implementationdetails.environment` . Voorheen konden deze waarden in sommige scenario&#39;s niet worden gevuld. Pas de relevante verwerkingsregels aan om rekening te houden met de beschikbaarheid van deze waarden. |

{style="table-layout:auto"}

## Aankondigingen van einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **EOL voor Adobe Analytics API (versie 1.4)** | donderdag 17 juli 2024 | Op **12 augustus, 2026**, zullen de volgende Analytics Verouderde API diensten hun eind-van-leven bereiken en zullen worden gesloten, en de huidige integratie die gebruikend deze diensten wordt gebouwd zal ophouden werkend:<ul><li>Adobe Analytics API (versie 1.4)</li><li>Adobe Analytics WSSE-verificatie</li></ul><p>De integratie die Adobe Analytics API (versie 1.4) gebruiken moet aan [ Adobe Analytics 2.0 API ](https://developer.adobe.com/analytics-apis/docs/2.0/) migreren, terwijl de integratie WSSE aan een op OAuth-Gebaseerd authentificatieprotocol in [ Adobe Developer Console ](https://developer.adobe.com/console) moet migreren.</p><p>Zie [ Adobe Analytics 1.4 API EOL FAQ ](/help/admin/c-admin-api/c-admin-14-api-eol.md) voor antwoorden op gemeenschappelijke vragen en verdere begeleiding.</p> |
| **Migratie aan Adobe I/O OAuth Server-aan-Server geloofsbrieven** | vrijdag 11 mei 2023 | Adobe Analytics API en Livestream klanten die de geloofsbrieven van Adobe I/O JWT gebruiken moeten aan de geloofsbrieven van Adobe I/O OAuth Server-aan-Server door **Januari 1, 2025** migreren. Adobe I/O staat niet toe dat vanaf 1 mei 2024 nieuwe JWT-referenties worden gemaakt. Klanten die JWT gebruiken moeten een nieuwe Server-aan-Server referentie OAuth tot stand brengen of hun bestaande JWT-referentie migreren naar een OAuth Server-aan-Server referentie. Klanten moeten ook hun clienttoepassingen bijwerken om de nieuwe OAuth Server-to-Server referenties te kunnen gebruiken. <ul><li>[ migrerend van de Rekening van de Dienst (JWT) geloofsbrieven ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[ gids van de Implementatie voor nieuwe en oude toepassingen met OAuth ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[ Gebruikend de nieuwe Server-aan-Server geloofsbrieven OAuth ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[ FAQs ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |

{style="table-layout:auto"}

## AppMeasurement

Voor de recentste updates op de versies van het AppMeasurement (Versie 2.26.0), gelieve te verwijzen naar [ AppMeasurement voor de versienota&#39;s van JavaScript ](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html).


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2024](/help/release-notes/2024.md)
* [ de versienota&#39;s van de Customer Journey Analytics ](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [ het stromen toe:voegen-op versienota&#39;s van de Inzameling van Media ](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De recentste versie werkt voor [ producten van Adobe Experience Cloud ](https://business.adobe.com/products/adobe-experience-cloud-products.html) bij
