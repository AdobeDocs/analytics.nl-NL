---
title: Opmerkingen bij de release Latest Analytics
description: Bekijk de huidige Adobe Analytics-releaseopmerkingen.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 1622f69e4d2a19d72e5748d165567d0bf7c5f83c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Huidige Adobe Analytics-releaseopmerkingen (september 2022)

**Laatste update**: 14 september 2022

## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2022](/help/release-notes/2022.md)
* [Opmerkingen bij de release Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De nieuwste release-updates voor [Adobe Experience Cloud-producten](https://business.adobe.com/products/adobe-experience-cloud-products.html)

## Nieuwe of bijgewerkte functies in Adobe Analytics

| Functie | Beschrijving | [Doeldatum](releases.md) |
| ----------- | ---------- | ------- |
| Visualisatie van combinatieteksten in werkruimte | Met combinatiekaarten kunt u metrische gegevens in Workspace gemakkelijker en intuïtiever vergelijken. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/combo-charts.html) | 14 september 2022 |

{style=&quot;table-layout:auto&quot;}

## Oplossingen in Adobe Analytics

* Correctie van problemen met importeren en exporteren van classificaties. (AN-299267)

**Oplossingen voor individuele klanten**:

AN-288519; AN-289300; AN-297387; AN-297465; AN-297520; AN-297641; AN-298134; AN-298351; AN-298429; AN-298483; AN-298520; AN-298582; AN-298816; AN-298832; AN-298855; AN-298864; AN-299407; AN-299545; AN-299644; AN-299715

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **Wijzigingen in de manier waarop Analytics omgaat met A4T-gegevens die via Experience Edge zijn verzameld** | 14 september 2022 | In maart 2022, veranderde Analytics hoe het sommige vraag uit de Rand van de Ervaring behandelt die A4T gegevens omvat. Hits met A4T die inhoud melden worden gewijzigd zodat zij niet als Mening van de Pagina worden behandeld (`t()`) of Koppeling bijhouden (`tl()`). Deze logica wordt nu bijgewerkt en bevat ook gevallen waarin `propositionDisplay` de gebeurtenissen werden niet op de beoogde wijze gewijzigd. |
| **Automatische scheidingstekens voor lijstvariabelen en lijststeunen in het Web SDK** | 14 september 2022 | Lijstvariabelen en lijsteigenschappen gebruiken nu de scheidingstekens die zijn opgegeven in de instellingen van de rapportsuite, tenzij een scheidingstekenoverschrijving is opgegeven in XDM. Zie de [list](/help/implement/vars/page-vars/list.md) voor meer informatie. |
| **SFTP-upgrade** | 14 september 2022 | Voorheen had Adobe meegedeeld dat Adobe haar Secure File Transfer Protocol (SFTP)-services in september 2022 zou upgraden om de beveiliging voor bestandsoverdracht te verbeteren. Adobe heeft deze upgrade uitgesteld naar **Medio september 2022**. Wanneer deze wijziging plaatsvindt, worden bepaalde SFTP-clientconfiguraties niet meer ondersteund. Dit is alleen van invloed op gegevens die via SFTP naar Adobe Analytics worden verzonden of van worden opgehaald. Dit heeft geen invloed op het FTP-protocol. Om onderbreking van de dienst te vermijden, gelieve ervoor te zorgen dat uw cliënten SFTP (code, hulpmiddelen, de diensten) in overeenstemming met de gedetailleerde veranderingen zijn [hier](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/sftp-upgrade.html). |
| **EOL voor Data Workbench** | 14 september 2022 | Adobe is voornemens de Data Workbench aan het einde van de levensduur doeltreffend te maken **31 december 2023**. Neem contact op met uw medewerker van de klantenservice voor alternatieve oplossingen voor de Data Workbench van als u vragen hebt. |
| **Bijwerken naar apparaatraadplegingen als gevolg van Google Client Hints** | 14 september 2022 | Starten bij **29 september 2022**, Adobe begint clienttips te gebruiken naast de gebruikersagent bij het afleiden van bepaalde apparaatinformatie voor hits die afkomstig zijn van Chromium-browsers, zoals Google Chrome en Microsoft Edge. Dit is in antwoord op het plan van Google om de informatie geleidelijk te verminderen die van het koord van de Agent van de Gebruiker in plaats van gegevens wordt voorgesteld die via cliëntwenken worden overgegaan. Meer informatie over clienttips [hier](https://web.dev/user-agent-client-hints/).<p> Tegen Oktober, zowel zullen de de inzamelingsbibliotheken van AppMeasurement als van SDK van het Web inzameling van cliëntwenken steunen en het vormen of aan hoge entropy cliëntwenken worden verzameld. Als deel van deze verandering, zal Adobe de Atlas van het Apparaat voor alle apparatenraadplegingen met betrekking tot de Agent van de Gebruiker gebruiken. Apparaataturen worden momenteel alleen gebruikt voor mobiele hits. Deze updates kunnen resulteren in kleine wijzigingen in apparaatinformatie die historisch zijn afgeleid van de gebruikersagent, met name browser, type browser, besturingssysteem, besturingssysteemtype en mobiel apparaat. |
| **Bijwerken naar nieuwe NetAcuity carrier-database** | 14 september 2022 | **Vanaf 5 oktober 2022**, aan de vervoerder gerelateerde informatie die is opgeslagen in de `carrier` in Adobe Analytics Data Warehouse and Analytics Data Feeds wordt gewijzigd. Historisch, is het gegevensformaat in die kolom geweest `<domain>:<ISP>`. Adobe heeft een interne raadplegingstabel bijgehouden om deze in kaart te brengen `<domain>:<ISP>` waarden in dragernamen voor rapportagedoeleinden in Adobe Analytics-rapportagehulpprogramma&#39;s (Analysis Workspace, Reports &amp; Analytics, Reporting API, Data Warehouse, LiveStream, enz.). Het opzoekbestand (`carrier.tsv`) wordt ook geleverd met Gegevensfeeds, zodat u dezelfde toewijzingen kunt gebruiken.<p>Deze update verbetert onze dragertoewijzingen door een nauwkeuriger dragergegevensbestand van NetAcuity te gebruiken. Het formaat van de gegevens in de dragerkolom in de Doopvonken van Gegevens zal in de toekomst veranderen. In plaats van `<domain>:<ISP>`, bevat het een dragernaam. Adobe zal de raadplegingstabel blijven gebruiken om zoveel mogelijk continuïteit met het verleden te handhaven rapportering. Meldend hulpmiddelen waar de raadplegingen door Adobe (Analysis Workspace, Rapporten &amp; Analytics, het melden API, gegevenspakhuis, LiveStream, enz.) worden toegepast zal profiteren van nauwkeurigere toewijzingen. Sommige toewijzingen - vooral voor internationale domeinen en ISPs - zullen meer dan anderen veranderen wanneer Adobe het nieuwe gegevensbestand goedkeurt. Het gegevensfeeds drager raadplegingsdossier (`carrier.tsv`) de oude toewijzingen behouden en de nieuwe toewijzingen toevoegen.<p>De verbinding van de Bron van Analytics brengt momenteel niet het dragergebied in kaart, zodat is de dragerrapportering momenteel niet beschikbaar in Experience Platform, CJA etc. Daarom zal het gebruik van het nieuwe dragergegevensbestand niets in Experience Platform beïnvloeden dat op gegevens gebaseerd is die door de Analytics Source Connector worden verstrekt. |
| **Verbeterde IP-naar-geolocatietoewijzing** | 14 september 2022 | Onze leverancier voor IP raadplegingen, Digitaal Element, bevordert aan een nieuwe betere dataset (de Puls van NetAcuity) voor IP-aan-geolocatiekaart. Adobe Analytics zal dit nieuwe gegevensbestand goedkeuren op **5 oktober 2022**. De nieuwe database is nauwkeuriger dan vorige versies. Sommige IP-aan-geo afbeeldingen zullen veranderen/verbeteren wanneer het nieuwe gegevensbestand wordt goedgekeurd.<p>Alle Adobe Analytics-gereedschappen (Analysis Workspace, Reports &amp; Analytics, Reporting API, data-magazijn, LiveStream, gegevensfeeds enz.) automatisch voordeel halen uit de nieuwe verbeterde toewijzingen. De indeling van de gegevens in gegevensfeeds wordt niet gewijzigd. De gegevens CJA die door de Bronschakelaar van de Analyse worden verstrekt zullen automatisch uit de nieuwe afbeeldingen voordeel halen. |
| **Geplande rapporten onderbreken in rapporten en analyses** | 8 juni 2022 | Op 21 april 2022 kondigde Adobe aan dat verschillende specifieke functies van geplande rapporten zouden worden vervangen ter voorbereiding op het eerder aangekondigde einde van de levensduur van Reports &amp; Analytics. Deze functies omvatten de mogelijkheid om nieuwe rapporten en nieuwe gegevensextracten te plannen.<p>In antwoord op verzoeken van klanten die een extensie willen aanvragen en om de overgang van Rapporten &amp; Analytics te vergemakkelijken, heeft Adobe besloten de toegang tot deze functies te verlengen tot **31 jan. 2023**. Houd er rekening mee dat de vervaltijden voor zowel rapporten als gegevensextracten beperkt blijven tot negen maanden. aan het einde van deze periode wordt de levering van rapporten en gegevensuittreksels gepauzeerd , tenzij het schema opnieuw wordt geactiveerd .<p>Om nog maar eens te herhalen: deze functies zijn verouderd op 31 januari 2023. Voor deze datum moet u de geplande rapportage migreren naar een van de andere methoden die beschikbaar zijn in Adobe Analytics. Neem voor aanvullende vragen of ondersteuning contact op met de klantenservice van Adobe. [Meer informatie](/help/analyze/reports-analytics/scheduled-reports-eol.md) |
| **Geplande taken pauzeren in Report Builder** | 8 juni 2022 | Op 21 april 2022 heeft Adobe wijzigingen doorgevoerd in de geplande taken in Report Builder als onderdeel van onze optimalisatie van prestaties en levering. Deze wijzigingen omvatten het verwijderen van de mogelijkheid om geplande leveringen &#39;end na x occurrences&#39; te laten beëindigen. In antwoord op verschillende verzoeken van klanten die meer tijd willen om alternatieven te verkennen en te implementeren, heeft Adobe besloten deze optie op beperkte wijze te herstellen tot **31 jan. 2023**.<p>U kunt Report Builder-taken per uur blijven plannen en deze na maximaal 99 exemplaren laten beëindigen. De terugdraaiing geldt alleen voor uurwerk. het &quot; einde na x &quot; komt niet voor alle andere leveringsintervallen ( dagelijks , wekelijks , maandelijks en jaarlijks ) . Deze optie wordt afgekeurd op 31 januari 2023. Neem voor meer vragen of ondersteuning contact op met de klantenservice van Adobe. [Meer informatie](/help/analyze/report-builder/r-arb-scheduled-reports.md) |
| **EOL voor[!DNL Reports & Analytics]** | 4 januari 2022 | Effectief **31 december 2023**, is Adobe voornemens te stoppen [!DNL Reports & Analytics] en de bijbehorende verslagen en kenmerken. De rapporten, visualisaties en onderliggende technologie die macht [!DNL Reports & Analytics] voldoet niet meer aan de normen voor Adobe. Meeste [!DNL Reports & Analytics] functies zijn beschikbaar in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). Sinds de release van Analysis Workspace in 2015, [!DNL Reports & Analytics] functionaliteit en mogelijkheden zijn verplaatst naar Analysis Workspace en er is een drempel voor pariteit van de workflow bereikt. [Dit bericht](https://spark.adobe.com/page/6WnF8JK6IRDhf/) legt het einde van het levensproces uit. |

{style=&quot;table-layout:auto&quot;}

## AppMeasurement

Voor de meest recente updates over AppMeasurement-releases (versie 2.22.4) raadpleegt u [AppMeasurement voor JavaScript-releaseopmerkingen](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=en).
