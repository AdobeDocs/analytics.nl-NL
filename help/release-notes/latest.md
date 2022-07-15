---
title: Opmerkingen bij de release Latest Analytics
description: Bekijk de huidige Adobe Analytics-releaseopmerkingen.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 94200622454fe2845a3b86025cd1796d29663736
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 2%

---

# Opmerkingen bij de huidige Adobe Analytics-release (juli 2022)

**Laatste update**: 13 juli 2022

## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2022](/help/release-notes/2022.md)
* [Opmerkingen bij de release Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De nieuwste release-updates voor [Adobe Experience Cloud-producten](https://business.adobe.com/products/adobe-experience-cloud-products.html)

## Nieuwe functies in Adobe Analytics

| Functie | Beschrijving | [Doeldatum](releases.md) |
| ----------- | ---------- | ------- |
| Steun voor het Merchandising Variabelen in XDM voor de Inzameling van de Rand | Hiermee kunnen klanten gegevens verzamelen via Experience Edge/Web SDK om XDM te gebruiken om de verschillende waarden voor Merchandising-variabelen (eVars) op te geven. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/evar-merchandising.html?lang=en) | 29 juni 2022 |

{style=&quot;table-layout:auto&quot;}

## Oplossingen in Adobe Analytics

* Correctie van enkele fouten bij segmentconversie. (AN-291262, AN-294092)

**Oplossingen voor individuele klanten**:

AN-280192; AN-281628; AN-287022; AN-287104; AN-287876; AN-288802; AN-288457; AN-288779; AN-288799; AN-289198; AN-289852; AN-289931; AN-290162; AN-290213; AN-291059; AN-291090; AN-291270; AN-294091; AN-294135; AN-294152; AN-294158; AN-294285; AN-294317; AN-294404; AN-294531; AN-294769; AN-294984; AN-295172; AN-295211; AN-295224; AN-295413; AN-295440; AN-295465; AN-295499; AN-295516;

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **Nieuw domein voor door het systeem gegenereerde e-mails** | 13 juli 2022 | Aan **18 mei 2022** heeft Adobe het domein van de afzender voor e-mails gewijzigd via Workspace-projecten, waarschuwingen en waarschuwingen wegens overlijden, van `noreply@omniture.com` tot `noreply@adobe.com`. Voeg deze nieuwe e-mail aan uw lijst van gewenste personen toe als uw organisatie slechts specifieke afzenders toestaat. |
| **Bijwerken naar nieuwe NetAcuity carrier-database** | 11 juli 2022 | **Vanaf oktober 2022**, aan de vervoerder gerelateerde informatie die is opgeslagen in de `carrier` in Adobe Analytics Data Warehouse and Analytics data feeds will change. Historisch, is het gegevensformaat in die kolom geweest `<domain>:<ISP>`. Adobe heeft een interne raadplegingstabel bijgehouden om deze in kaart te brengen `<domain>:<ISP>` waarden in dragernamen voor rapportagedoeleinden in Adobe Analytics-rapportagehulpprogramma&#39;s (Analysis Workspace, Reports &amp; Analytics, Reporting API, data magazijn, LiveStream, enz.) Het raadplegingsdossier (drager.tsv) wordt ook voorzien van gegevensvoer zodat de gegevensvoer klanten de zelfde afbeeldingen kunnen gebruiken.<p>Deze update verbetert onze dragertoewijzingen door een nauwkeuriger dragergegevensbestand van NetAcuity te gebruiken. Het formaat van de gegevens in de dragerkolom in gegevensvoer zal in de toekomst veranderen. In plaats van `<domain>:<ISP>`, bevat het een dragernaam. Adobe zal de raadplegingstabel blijven gebruiken om zoveel mogelijk continuïteit met het verleden te handhaven rapportering. Meldend hulpmiddelen waar de raadplegingen door Adobe (Analysis Workspace, Rapporten &amp; Analytics, het melden API, gegevenspakhuis, LiveStream, enz.) worden toegepast zal profiteren van nauwkeurigere toewijzingen. Sommige toewijzingen - vooral voor internationale domeinen en ISPs - zullen meer dan anderen veranderen wanneer wij het nieuwe gegevensbestand goedkeuren. Het gegevensvoer dragerraadplegingsdossier (drager.tsv) zal de oude afbeeldingen handhaven en de nieuwe afbeeldingen toevoegen.<p>De verbinding van de Bron van Analytics brengt momenteel niet het dragergebied in kaart, zodat is de dragerrapportering momenteel niet beschikbaar in AEP, CJA etc. Daarom zal het gebruik van het nieuwe dragergegevensbestand niets in AEP beïnvloeden dat op gegevens gebaseerd is die door de Analytics Source Connector worden verstrekt. |
| **Verbeterde IP-naar-geolocatietoewijzing** | 11 juli 2022 | Onze leverancier voor IP raadplegingen, Digitaal Element, bevordert aan een nieuwe betere dataset (de Puls van NetAcuity) voor IP-aan-geolocatiekaart. Adobe Analytics zal deze nieuwe dataset goedkeuren in het **oktober 2022** tijdframe. De nieuwe database is nauwkeuriger dan vorige versies. Sommige IP-aan-geo afbeeldingen zullen veranderen/verbeteren wanneer het nieuwe gegevensbestand wordt goedgekeurd.<p>Alle Adobe Analytics-gereedschappen (Analysis Workspace, Reports &amp; Analytics, Reporting API, data-magazijn, LiveStream, gegevensfeeds enz.) automatisch voordeel halen uit de nieuwe verbeterde toewijzingen. De indeling van de gegevens in gegevensfeeds wordt niet gewijzigd. De gegevens CJA die door de Bronschakelaar van de Analyse worden verstrekt zullen automatisch uit de nieuwe afbeeldingen voordeel halen. |
| **Geplande rapporten onderbreken in rapporten en analyses** | 8 juni 2022 | Op 21 april 2022 hebben we aangekondigd dat verschillende functies die specifiek zijn voor geplande rapporten, zullen worden vervangen ter voorbereiding op het eerder aangekondigde einde van de levensduur van Reports &amp; Analytics. Deze functies omvatten de mogelijkheid om nieuwe rapporten en nieuwe gegevensextracten te plannen.<p>In reactie op verzoeken van klanten die een extensie willen aanvragen en om de overgang van Reports and Analytics te vergemakkelijken, hebben we besloten de toegang tot deze functies te verlengen tot **31 jan. 2023**. Houd er rekening mee dat de vervaltijden voor zowel rapporten als gegevensextracten beperkt blijven tot negen maanden. aan het einde van deze periode wordt de levering van rapporten en gegevensuittreksels gepauzeerd , tenzij het schema opnieuw wordt geactiveerd .<p>Om nog maar eens te herhalen: deze functies zijn verouderd op 31 januari 2023. Voor deze datum moet u de geplande rapportage migreren naar een van de andere methoden die beschikbaar zijn in Adobe Analytics. Neem voor aanvullende vragen of ondersteuning contact op met de klantenservice van Adobe. [Meer informatie](/help/analyze/reports-analytics/scheduled-reports-eol.md) |
| **Geplande taken pauzeren in Report Builder** | 8 juni 2022 | Op 21 april 2022 hebben we wijzigingen doorgevoerd in de geplande taken in Report Builder als onderdeel van onze inspanningen om de prestaties en prestaties te optimaliseren. Deze wijzigingen omvatten het verwijderen van de mogelijkheid om geplande leveringen &#39;end na x occurrences&#39; te laten beëindigen. In antwoord op verschillende verzoeken van klanten die meer tijd zoeken om alternatieven te onderzoeken en te implementeren, hebben we besloten deze optie op beperkte wijze te herstellen tot **31 jan. 2023**.<p>U kunt Report Builder-taken per uur blijven plannen en deze na maximaal 99 exemplaren laten beëindigen. De terugdraaiing geldt alleen voor uurwerk. het &quot; einde na x &quot; komt niet voor alle andere leveringsintervallen ( dagelijks , wekelijks , maandelijks en jaarlijks ) . Deze optie wordt afgekeurd op 31 januari 2023. Neem voor meer vragen of ondersteuning contact op met de klantenservice van Adobe. [Meer informatie](/help/analyze/report-builder/r-arb-scheduled-reports.md) |
| **SFTP-upgrade** | 9 mei 2022 | Eerder, hadden wij meegedeeld dat Adobe zijn Secure File Transfer Protocol (SFTP) diensten in mei 2022 zou bevorderen om betere veiligheid voor dossieroverdracht te verstrekken. We hebben deze upgrade uitgesteld naar de **zomer 2022**. Wanneer deze wijziging plaatsvindt, worden bepaalde SFTP-clientconfiguraties niet meer ondersteund. Dit is alleen van invloed op gegevens die via SFTP naar Adobe Analytics worden verzonden of van worden opgehaald. Dit heeft geen invloed op het FTP-protocol. Om onderbreking van de dienst te vermijden, gelieve ervoor te zorgen dat uw cliënten SFTP (code, hulpmiddelen, de diensten) in overeenstemming met de gedetailleerde veranderingen zijn [hier](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/sftp-upgrade.html). |
| **EOL voor[!DNL Reports & Analytics]** | 4 januari 2022 | Effectief **31 december 2023**, is Adobe voornemens te stoppen [!DNL Reports & Analytics] en de bijbehorende verslagen en kenmerken. De rapporten, visualisaties en onderliggende technologie die macht [!DNL Reports & Analytics] voldoet niet meer aan de technologienormen van Adobe. Meeste [!DNL Reports & Analytics] functies zijn beschikbaar in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). Sinds de release van Analysis Workspace in 2015, [!DNL Reports & Analytics] functionaliteit en mogelijkheden zijn verplaatst naar Analysis Workspace en er is een drempel voor pariteit van de workflow bereikt. [Dit bericht](https://spark.adobe.com/page/6WnF8JK6IRDhf/) legt het einde van het levensproces uit. |

{style=&quot;table-layout:auto&quot;}

## AppMeasurement

Voor de meest recente updates over AppMeasurement-releases (versie 2.22.4) raadpleegt u [AppMeasurement voor JavaScript-releaseopmerkingen](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=en).

