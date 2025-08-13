---
title: Opmerkingen bij de release van Adobe Analytics
description: De huidige Adobe Analytics-releaseopmerkingen weergeven
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 07d6b4e096d239d4940f438c5eca46f496a18131
workflow-type: tm+mt
source-wordcount: '1146'
ht-degree: 1%

---

# Huidige Adobe Analytics-releaseopmerkingen (release augustus 2025)

**Laatste update**: 13 augustus 2025

Deze releaseopmerkingen hebben betrekking op de periode van 13 augustus tot en met 16 september 2025. De versies van Adobe Analytics werken op a [ ononderbroken leveringsmodel ](releases.md), dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of verbeterde functies {#features}

| Functie | Beschrijving | [ Het begin van de Uitvoer ](releases.md) | [ Algemene Beschikbaarheid ](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Analyseer AI verkeer met een nieuw de afmetingspunt van het Type van Referteur** | In oktober, zal een nieuw het type van Referteur afmetingspunt beschikbaar zijn helpen verkeer analyseren dat uit hulpmiddelen AI komt. <p>Dit nieuwe het type van Referteur afmetingspunt, genoemd de Gelijke hulpmiddelen van AI, zal groeperen verwijzend domeinen van belangrijke hulpmiddelen AI, toestaand u om tendensen voor de groep als geheel te bekijken. De initiële lijst met verwijzende domeinen in deze nieuwe categorie omvat (maar is niet beperkt tot):</p><ul><li>chatgpt.com</li><li>claude.ai</li><li>m365.cloud.microsoft</li><li>grok.com</li><li>gemini.google.com</li><li>perplexity.ai</li></ul><p>Het nieuwe dimensie-item is beschikbaar in alle aan Adobe Analytics gerelateerde tools, zoals Analysis Workspace, Report Builder, Data Warehouse, Data Feeds, enzovoort.</p><p>Overweeg het volgende wanneer het gebruiken van dit nieuwe afmetingspunt:</p><ul><li>Het is niet altijd mogelijk om verwijzingsverkeer te onderscheiden dat van resultaten kwam die op &quot;AI wijze&quot;in een onderzoeksmotor worden verstrekt tegenover die die uit klikproductie van traditionele onderzoeksresultaten kwamen.</li><li>Het nieuwe Conversational AI hulpmiddeldimensie punt concentreert zich op belangrijke leveranciers met het meeste verkeer. Een nieuwe trend onthult een stijgend aantal imitatorplaatsen met domeinen gelijkend op belangrijke AI hulpmiddelleveranciers. Dit is waarschijnlijk het gevolg van het gemak waarmee personen of groepen hun eigen AI-tools kunnen maken en deze op internet kunnen hosten. Omdat dit een snel evoluerende ruimte is, gelieve het ondersteuningsteam van Adobe te contacteren als u vindt dat een populaire plaats niet inbegrepen is.</li><li>De dimensie van het verwijzingstype, met inbegrip van het nieuwe Conversational AI hulpmiddelen afmetingspunt, is beschikbaar slechts voor gegevens die door Adobe Analytics worden verwerkt. </li></ul><p>(Koppeling met documentatie die moet worden gevolgd.)</p> |   | Oktober 2025 |
| **Projecten die als PDFs worden gedownload aan uw werkstation** | Wanneer u een project downloadt als een PDF, wordt de PDF gedownload naar de downloadmap op uw werkstation. <p>Als u eerder een project downloadde als een PDF, werd de PDF gestart op een nieuw browsertabblad met een unieke URL.</p><p>Voor meer informatie, zie [ de projecten en gegevens van de Download ](/help/analyze/analysis-workspace/curate-share/download-send.md)</p> |  | dinsdag 25 augustus 2025 |
| **verwijderde projecten zijn onmiddellijk niet beschikbaar door URL en van geplande leveringen geschrapt** | Projecten die worden verwijderd, worden direct verwijderd uit geplande leveringen en zijn niet meer toegankelijk via de URL.<p>Eerder waren projecten opgenomen in geplande leveringen en konden deze gedurende 60 dagen na het verwijderen worden geopend met hun URL.</p><p>Voor meer informatie over het schrappen van projecten, zie [ Overzicht van Projecten ](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md).</p> | | Eind augustus 2025 |
| **Streaming Media: Bijgewerkte gebieden XDM voor het verzamelen van het stromen gegevens van Media in Adobe Experience Platform** | Wanneer het verzamelen van de Gegevens van Media van de Streaming in Adobe Experience Platform, zouden de XDM gebiedspaden onder de rubriek van &quot;Pad van het Gebied XDM&quot;van de Streaming de parameterdocumentatie van Media niet meer moeten worden gebruikt. In plaats daarvan, moeten de klanten die de analytische bronschakelaar uitvoerden om het stromen gegevens van Media in Platform vóór 9 Mei te verzamelen, 2025 hun bestaande configuraties aan mediaReporting gebiedspaden, zoals aangetoond onder de rubriek &quot;het Weg van het Gebied van XDM&quot;van de documentatie van de parameters van Media het Streamen.<p> Deze gebiedspaden worden gevonden op de volgende pagina&#39;s en als &quot;Vervangen&quot;duidelijk: [ Audio en videoparameters ](https://experienceleague.adobe.com/nl/docs/media-analytics/using/implementation/variables/audio-video-parameters), [ Advertentieparameters ](https://experienceleague.adobe.com/nl/docs/media-analytics/using/implementation/variables/ad-parameters), [ de parameters van het Hoofdstuk ](https://experienceleague.adobe.com/nl/docs/media-analytics/using/implementation/variables/chapter-parameters), [ de staatsparameters van de Speler ](https://experienceleague.adobe.com/nl/docs/media-analytics/using/implementation/variables/player-state-parameters), en [ de parameters van de Kwaliteit ](https://experienceleague.adobe.com/nl/docs/media-analytics/using/implementation/variables/quality-parameters). (Geen actie wordt vereist voor klanten die de bron van Analytics schakelaar na 9 Mei, 2025 uitvoeren, en reeds mediaReporting XDM wegen gebruiken.)</p><p>Gegevensinvoer op de afgekeurde XDM-veldpaden gaat door tot eind oktober 2025. Na die tijd, zullen de afgekeurde gebiedspaden volledig worden verwijderd en niet meer zichtbaar in het Schema UI van Adobe Experience Platform, en de gegevens zullen worden verzonden slechts gebruikend mediaReporting gebiedspaden.</p><p>Voor meer informatie, zie [ migreren een implementatie van de Verbinding van Analytics Source aan bijgewerkte XDM Streaming Media ](https://experienceleague.adobe.com/nl/docs/media-analytics/using/media-use-cases/xdm-updates/updated-xdm-fields).</p><p>Neem contact op met uw Adobe Consulting Services of accountteam voor ondersteuning van migratie. </p> |  | Oktober 2025 |

## Oplossingen in Adobe Analytics

**Activity Map**: AN-389205; AN-384186
**Analysis Workspace**: AN-390102; AN-389066; AN-388841; AN-388687; AN-388478; AN-387089; AN-387 044; AN-384560; AN-379213; AN-351639
**Classificaties**: AN-390442; AN-390385; AN-389953; AN-389703; AN-389321; AN-389116; AN-38 833; AN-388717; AN-387987; AN-383329
**de inzameling van Gegevens**: AN-389320
**de Eendelen van Gegevens en Data Warehouse**: AN-389702; AN-388136; AN-38779; AN-384369; AN-383075; AN-380307
**Privacy**:
**Report Builder**: AN-389336; AN-382775
**het Melden**: AN-390398
**Geplande rapporten**:
**de vergelijking van het Segment**:
**Andere**: AN-388180; AN-383164; AN-366532


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
