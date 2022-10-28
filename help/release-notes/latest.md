---
title: Opmerkingen bij de release Latest Analytics
description: Bekijk de huidige Adobe Analytics-releaseopmerkingen.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 7c66414129e262954e5521a28b878424099ac6ad
workflow-type: tm+mt
source-wordcount: '1412'
ht-degree: 2%

---

# Opmerkingen bij de huidige Adobe Analytics-release (oktober/november 2022)

**Laatste update**: 28 oktober 2022

Adobe Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of bijgewerkte functies in Adobe Analytics

| Functie | Beschrijving | [Uitvoeren start](releases.md) | [Algemene beschikbaarheid](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **[!UICONTROL Key metric summary]** visualisatie | De [!UICONTROL Key metric summary] Met visualisatie kunt u zien hoe een belangrijke metriek binnen één tijdsperiode trending. Ook kunt u de metrische prestaties in twee tijdframes vergelijken. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/key-metric.html?lang=en) | 5 oktober 2022 | 19 oktober 2023 |
| **Niet-hoofdlettergevoelige meerwaardevariabelen** | Voor niet-hoofdlettergevoelige meerwaardevariabelen worden de waarden opgeslagen in `mvvar1 - mvvar3` en `post_mvvar1 - post_mvvar3` in Gegevensfeeds wordt niet langer automatisch verlaagd. In plaats daarvan zullen de gegevensfeeds (en de gegevens die door de Verbinding van de Bron van Analytics aan Adobe Experience Platform en CJA worden overgegaan) het originele geval weerspiegelen dat van de pagina werd overgegaan. | N.v.t. | 24 oktober 2022 |

{style=&quot;table-layout:auto&quot;}

## Oplossingen in Adobe Analytics

* Probleem verholpen waarbij de naam van recente MacOS-versies onjuist &quot;Macintosh&quot; werd genoemd. Met deze correctie begint de dimensie van het besturingssysteem met het gebruik van &quot;MacOS&quot;-versienummering, te beginnen met MacOS 11. (AN-301834)
* Probleem opgelost met het datumbereik &quot;vaste datums&quot; in Report Builder. (AN-303684)
* Problemen verholpen waarbij de interface voor gegevensinvoer niet werd geladen. (AN-303803, AN-303784)

### Andere oplossingen

AN-295574; AN-296354; AN-297143; AN-299501; AN-301755; AN-302054; AN-302304; AN-302631; AN-302811; AN-303090; AN-303372; AN-303428; AN-303429; AN-303432; AN-303434; AN-303437; AN-303438; AN-303519; AN-303610; AN-303656; AN-303659; AN-303663; AN-303664; AN-303818; AN-303823; AN-303837; AN-304036; AN-304195; AN-304321; AN-304325; AN-304339; AN-304356; AN-304435; AN-304457; AN-304509; AN-304519; AN-304534

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **Bijwerken naar apparaatraadplegingen als gevolg van Google Client Hints** | 14 oktober 2022 | Het gebruik van client-tips in de opzoekprocedure van apparaten, oorspronkelijk gepland voor 26 oktober 2022, is uitgesteld tot **Januari 2023**. <p> <p>Vanaf oktober 2022 is het mogelijk om cliëntwenken met of de bibliotheken van SDK van het Web of van JavaScript van de Meting te verzamelen AppMeasurement. Maar de cliëntwenken zullen niet in apparatenraadpleging tot Januari 2023 worden opgenomen. Op die datum, zal Adobe beginnen gebruikend cliëntwenken naast gebruiker-Agent wanneer het afleiden van bepaalde apparateninformatie voor klappen die uit Chromium browsers, zoals Google Chrome en Microsoft Edge komen. Dit is in antwoord op het plan van Google om de informatie geleidelijk te verminderen die van het user-Agent koord in plaats van gegevens wordt voorgesteld die via cliëntwenken worden overgegaan. <p> <p>Als deel van deze verandering, zal Adobe de Atlas van het Apparaat voor alle apparatenraadplegingen met betrekking tot gebruiker-Agent gebruiken. [Meer informatie](/help/technotes/client-hints.md) |
| **Standaardlandingspagina** | 29 september 2022 | De [nieuwe bestemmingspagina](/help/analyze/landing.md) die eerder dit jaar is geïntroduceerd, wordt de standaardeigenschap voor alle gebruikers in de **Januari 2023**. De huidige pagina wordt afgekeurd en iedereen moet de nieuwe ervaring gebruiken. |
| **[!UICONTROL Anomaly detection]automatisch afloopcondities** | 29 september 2022 | Vandaag, [!UICONTROL Anomaly detection] auto-looppas op alle kolommen van tijd-reeksen vrije lijsten. Om ervoor te zorgen dat gegevens beschikbaar zijn voor analyse en projecten sneller worden geladen, wijzigt Adobe de manier waarop Anomaly-detectie automatisch wordt uitgevoerd. Starten **26 oktober 2022**, [!UICONTROL Anomaly detection] zal auto-looppas slechts op de eerste metrische kolom in een lijst. U kunt kolommontages vormen om anomalieopsporing op andere kolommen in werking te stellen, indien nodig. |
| **Bijwerken naar nieuwe NetAcuity carrier-database** | 26 september 2022 | Deze actualisering, die oorspronkelijk gepland was op 5 oktober 2022, is uitgesteld tot **januari 2023**. Informatie over de vervoerder die is opgeslagen in het `carrier` in Adobe Analytics Data Warehouse and Analytics Data Feeds wordt gewijzigd. Historisch, is het gegevensformaat in die kolom geweest `<domain>:<ISP>`. Adobe heeft een interne raadplegingstabel bijgehouden om deze in kaart te brengen `<domain>:<ISP>` waarden in dragernamen voor rapportagedoeleinden in Adobe Analytics-rapportagehulpprogramma&#39;s (Analysis Workspace, Reports &amp; Analytics, Reporting API, Data Warehouse, LiveStream, enz.). Het opzoekbestand (`carrier.tsv`) wordt ook geleverd met Gegevensfeeds, zodat u dezelfde toewijzingen kunt gebruiken.<p>Deze update verbetert onze dragertoewijzingen door een nauwkeuriger dragergegevensbestand van NetAcuity te gebruiken. Het formaat van de gegevens in de dragerkolom in de Doopvonken van Gegevens zal in de toekomst veranderen. In plaats van `<domain>:<ISP>`, bevat het een dragernaam. Adobe zal de raadplegingstabel blijven gebruiken om zoveel mogelijk continuïteit met het verleden te handhaven rapportering. Meldend hulpmiddelen waar de raadplegingen door Adobe (Analysis Workspace, Rapporten &amp; Analytics, het melden API, gegevenspakhuis, LiveStream, enz.) worden toegepast zal profiteren van nauwkeurigere toewijzingen. Sommige toewijzingen - vooral voor internationale domeinen en ISPs - zullen meer dan anderen veranderen wanneer Adobe het nieuwe gegevensbestand goedkeurt. Het gegevensfeeds drager raadplegingsdossier (`carrier.tsv`) de oude toewijzingen behouden en de nieuwe toewijzingen toevoegen.<p>De verbinding van de Bron van Analytics brengt momenteel niet het dragergebied in kaart, zodat is de dragerrapportering momenteel niet beschikbaar in Experience Platform, CJA etc. Daarom zal het gebruik van het nieuwe dragergegevensbestand niets in Experience Platform beïnvloeden dat op gegevens gebaseerd is die door de Analytics Source Connector worden verstrekt. |
| **Verbeterde IP-naar-geolocatietoewijzing** | 26 september 2022 | Onze leverancier voor IP raadplegingen, Digitaal Element, bevordert aan een nieuwe betere dataset (de Puls van NetAcuity) voor IP-aan-geolocatiekaart. Oorspronkelijk voor oktober 2022 gepland, zal Adobe Analytics deze nieuwe dataset goedkeuren in **januari 2023**. De nieuwe database is nauwkeuriger dan vorige versies. Sommige IP-aan-geo afbeeldingen zullen veranderen/verbeteren wanneer het nieuwe gegevensbestand wordt goedgekeurd.<p>Alle Adobe Analytics-gereedschappen (Analysis Workspace, Reports &amp; Analytics, Reporting API, data-magazijn, LiveStream, gegevensfeeds enz.) automatisch voordeel halen uit de nieuwe verbeterde toewijzingen. De indeling van de gegevens in gegevensfeeds wordt niet gewijzigd. De gegevens CJA die door de Bronschakelaar van de Analyse worden verstrekt zullen automatisch uit de nieuwe afbeeldingen voordeel halen. |
| **Geplande rapporten onderbreken in rapporten en analyses** | 8 juni 2022 | Op 21 april 2022 kondigde Adobe aan dat verschillende specifieke functies van geplande rapporten zouden worden vervangen ter voorbereiding op het eerder aangekondigde einde van de levensduur van Reports &amp; Analytics. Deze functies omvatten de mogelijkheid om nieuwe rapporten en nieuwe gegevensextracten te plannen.<p>In antwoord op verzoeken van klanten die een extensie willen aanvragen en om de overgang van Rapporten &amp; Analytics te vergemakkelijken, heeft Adobe besloten de toegang tot deze functies te verlengen tot **31 jan. 2023**. Houd er rekening mee dat de vervaltijden voor zowel rapporten als gegevensextracten beperkt blijven tot negen maanden. aan het einde van deze periode wordt de levering van rapporten en gegevensuittreksels gepauzeerd , tenzij het schema opnieuw wordt geactiveerd .<p>Om nog maar eens te herhalen: deze functies zijn verouderd op 31 januari 2023. Voor deze datum moet u de geplande rapportage migreren naar een van de andere methoden die beschikbaar zijn in Adobe Analytics. Neem voor aanvullende vragen of ondersteuning contact op met de klantenservice van Adobe. [Meer informatie](/help/analyze/reports-analytics/scheduled-reports-eol.md) |
| **Geplande taken pauzeren in Report Builder** | 8 juni 2022 | Op 21 april 2022 heeft Adobe wijzigingen doorgevoerd in de geplande taken in Report Builder als onderdeel van onze optimalisatie van prestaties en levering. Deze wijzigingen omvatten het verwijderen van de mogelijkheid om geplande leveringen &#39;end na x occurrences&#39; te laten beëindigen. In antwoord op verschillende verzoeken van klanten die meer tijd willen om alternatieven te verkennen en te implementeren, heeft Adobe besloten deze optie op beperkte wijze te herstellen tot **31 jan. 2023**.<p>U kunt Report Builder-taken per uur blijven plannen en deze na maximaal 99 exemplaren laten beëindigen. De terugdraaiing geldt alleen voor uurwerk. het &quot; einde na x &quot; komt niet voor alle andere leveringsintervallen ( dagelijks , wekelijks , maandelijks en jaarlijks ) . Deze optie wordt afgekeurd op 31 januari 2023. Neem voor meer vragen of ondersteuning contact op met de klantenservice van Adobe. [Meer informatie](/help/analyze/report-builder/r-arb-scheduled-reports.md) |

{style=&quot;table-layout:auto&quot;}

## Aankondigingen aan het einde van de levensduur

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **EOL van [!UICONTROL Publishing Lists] functie** | 29 september 2022 | Als onderdeel van het EOL van Rapporten &amp; Analytics, worden de het publiceren lijsten vermeld om eind van het leven in te bereiken **december 2023**. U kunt geen nieuwe of bestaande Publishing Lists maken om Analysis Workspace-projecten te verzenden of te plannen. [Meer informatie](/help/admin/admin/publishing-list.md) |
| **EOL voor Data Workbench** | 14 september 2022 | Adobe is voornemens de Data Workbench aan het einde van de levensduur doeltreffend te maken **31 december 2023**. Zie [Aankondiging einde levensduur Data Workbench](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html) voor meer informatie. Neem contact op met de Adobe-accountmanager van uw organisatie voor vragen. |
| **EOL voor[!DNL Reports & Analytics]** | 4 januari 2022 | Effectief **31 december 2023**, is Adobe voornemens te stoppen [!DNL Reports & Analytics] en de bijbehorende verslagen en kenmerken. De rapporten, visualisaties en onderliggende technologie die macht [!DNL Reports & Analytics] voldoet niet meer aan de normen voor Adobe. Meeste [!DNL Reports & Analytics] functies zijn beschikbaar in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). Sinds de release van Analysis Workspace in 2015, [!DNL Reports & Analytics] functionaliteit en mogelijkheden zijn verplaatst naar Analysis Workspace en er is een drempel voor pariteit van de workflow bereikt. [Dit bericht](https://spark.adobe.com/page/6WnF8JK6IRDhf/) legt het einde van het levensproces uit. |

{style=&quot;table-layout:auto&quot;}

## AppMeasurement

Voor de meest recente updates over AppMeasurement-releases (versie 2.23.0) raadpleegt u [AppMeasurement voor JavaScript-releaseopmerkingen](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=en).

## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2022](/help/release-notes/2022.md)
* [Opmerkingen bij de release Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De nieuwste release-updates voor [Adobe Experience Cloud-producten](https://business.adobe.com/products/adobe-experience-cloud-products.html)
