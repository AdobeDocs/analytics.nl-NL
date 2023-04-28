---
title: Opmerkingen bij de release Latest Analytics
description: Bekijk de huidige Adobe Analytics-releaseopmerkingen.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: cd727113683be47793829871c64f057dc764f3ef
workflow-type: tm+mt
source-wordcount: '1674'
ht-degree: 2%

---

# Huidige Adobe Analytics-releaseopmerkingen (april 2023)

**Laatste update**: 21 april 2023

Adobe Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of bijgewerkte functies in Adobe Analytics {#features}

| Functie | Beschrijving | [Uitvoeren start](releases.md) | [Algemene beschikbaarheid](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Backfill voor niet-productiesandboxen** | Wanneer u een gegevensstroom van de Analytics Source Connector maakt in een niet-productiesandbox, wordt de back-up van niet-productiesandboxen beperkt tot 3 maanden. Het zal 13 maanden blijven voor productie zandbakken. | N.v.t. | 26 april 2023 |
| **Rij-/kolomfiltering voor streaming van Analyse Source Connector** | Met de Bronverbinding Analytics in Adobe Experience Platform kunt u nu analysegegevens filteren die worden gebruikt om profielen te vullen in [Klantprofiel in realtime](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=en). Filteren op rijniveau helpt het aantal gebeurtenissen dat aan profielen is gekoppeld, te verminderen. Filteren op kolomniveau helpt de rijkheid van de gebeurtenissen zelf te verminderen, zodat u het gebruik van profielrechten kunt optimaliseren. Deze filtering is alleen van toepassing op gegevens die naar het realtime-klantprofiel worden verzonden en [Identiteitsservice](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=en). **Filteren heeft geen invloed op de gegevens die naar het Data Lake worden verzonden voor gebruik in toepassingen zoals Customer Journey Analytics**. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=en#filtering-for-profile) | N.v.t. | 29 maart 2023 |
| **Gedeeltelijke ondersteuning voor Activity Map met Web SDK** | Beginnend met versie 2.15.0 van SDK van het Web, begonnen wij het bevolken van Activity Map gegevens wanneer het verbinden wordt toegelaten. Dit staat de gebruikers van SDK van het Web toe om Activity Map rapporterend te krijgen als zij verbinding het volgen toegelaten met het Web SDK en Activity Map hebben die in Analytics wordt gevormd.<p>Het toelaten van verbinding het volgen met Web SDK verzendt momenteel verbindingsgebeurtenissen wanneer een klant van één pagina aan volgende navigeert. Dit verschilt van de manier waarop AppMeasurement werkt en kan resulteren in extra factureerbare hits die naar Adobe worden verzonden. Meer informatie [hier](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/track-links.html) en [hier](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable.md) | N.v.t. | 31 maart 2023 |
| **IP-verduistering voor Experience Edge** | Experience Edge biedt ondersteuning voor IP-verwarring voor gegevens die rechtstreeks naar Adobe Experience Platform worden verzonden. Dit komt klanten ten goede die gegevens rechtstreeks naar Platform voor gebruik in CJA of andere oplossingen van het Platform verzenden. IP de verwarring wordt gevormd op het niveau van de gegevensstroom. Het steunt het verwijderen van het laatste octet of het volledige IP adres.<p>**Opmerking**: Obfusatie is NIET van toepassing op gegevens die naar Adobe Analytics worden verzonden. Analytics blijft volledige IP krijgen. IP verwerking blijft afzonderlijk in Analytics worden gedaan. In de toekomst zijn we van plan om de gegevens van Analytics aan de rand te laten verduisteren. | N.v.t. | AEP-release op 26 april 2023 |
| **Gegevenswoordenboek in Analysis Workspace** | Met het gegevenswoordenboek kunnen gebruikers en beheerders de componenten (afmetingen, metriek) in hun analyseomgeving bijhouden, beheren en beter begrijpen. [Meer informatie](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) | 15 maart 2023 | 29 maart 2023 |
| **Het delen van verbindingen voor projecten (geen vereiste login)** | <p>U kunt nu alleen-lezen koppelingen naar Analysis Workspace-projecten delen met mensen die geen toegang hebben tot Adobe Analytics. Dit omvat het delen met mensen buiten uw organisatie of met mensen binnen uw organisatie die niet zijn ingericht voor Adobe Analytics. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/share-projects.html?lang=en#share-public-link)</p> <p>Deze functionaliteit is standaard ingeschakeld en kan door de systeembeheerder worden uitgeschakeld. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/user-preferences.html?lang=en#company-preferences)</p> | 26 april 2023 (alleen voor toegang tot bèta uit de particuliere sector) | Juni 2023 |
| **2 nieuwe eindpuntgidsen voor Adobe Analytics 2.0 API** | <ul><li>[Dimension-API voor analyse](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/dimensions/)</li><li>[API voor analysemetriek](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/metrics/)</li></ul> | N.v.t. | 10 april 2023 |

{style="table-layout:auto"}

## Oplossingen in Adobe Analytics

* Probleem verholpen met opzoekbestanden van het besturingssysteem System.tsv in de gegevensfeed.
* Probleem verholpen met metrische waarden die verschillen tussen rapporten en analyse en werkruimte (AN-315965).
* Probleem verholpen waarbij gedeeltelijke classificaties niet konden worden geïmporteerd. (AN-315854)
* Probleem verholpen met Analytics API 1.4. (AN-316475)
* Probleem verholpen waardoor sommige klanten geen classificaties voor de pagina-dimensie konden krijgen via Report Builder en Rapport &amp; Analytics. (AN-314445)
* Oplossing voor een probleem met de mogelijkheid om waarschuwingen over te dragen. (AN-306457)

### Andere oplossingen

AN-288373; AN-305144; AN-309023; AN-310466; AN-311686; AN-311705; AN-312018; AN-312105; AN-312116; AN-312191; AN-312502; AN-312737; AN-312854; AN-312991; AN-313253; AN-313275; AN-313278; AN-313282; AN-313365; AN-313390; AN-313547; AN-313549; AN-313818; AN-313986; AN-314080; AN-314248; AN-314251; AN-314262; AN-314300; AN-314309; AN-314448; AN-314643; AN-314564; AN-314645; AN-314705; AN-314761; AN-314831; AN-314919; AN-314948; AN-315032; AN-315115; AN-315154; AN-315158; AN-315321; AN-315375; AN-315379; AN-315392; AN-315407; AN-315427; AN-315582; AN-315591; AN-315699; AN-315700; AN-315704; AN-315705; AN-315777; AN-315923; AN-316237; AN-316243; AN-316324; AN-316415; AN-316474; AN-316493; AN-316596; AN-316864;

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders {#admin}

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **Opmerking: Nieuwe IP&#39;s die worden gebruikt door Adobe Analytics Data Feeds en Data Warehouse egress in het London Data Center** | 27 april 2023 | Voor klanten in het Centrum van Gegevens van Londen die de verzoeken en/of rapporten hebben van het Gegevensvoer die van Gegevens aan de dienst worden geleverd FTP/SFTP, zouden de volgende IP adreswaaiers aan uw firewallconfiguratie moeten worden toegevoegd om toegang toe te staan: <ul><li>130.248.244.32/29</li><li>130.248.244.40/29</li></ul> |
| **Opzoekprocessen van apparaten gebruiken nu een derde voor alle apparaatopzoekacties** | 3 maart 2023 | Op 2 maart 2023, als deel van steunuitrol voor cliëntwenken, hebben wij onze processen van de apparatenraadpleging bijgewerkt om een derde voor alle apparatenraadplegingen te gebruiken. Eerder hadden we de derde alleen gebruikt voor zoekopdrachten voor mobiele apparaten. In het kader van deze uitrol werden sommige desktopbesturingssystemen onjuist aangeduid met de tekst &quot;mobile&quot; (bijvoorbeeld &quot;Mobile OS X 10.15.7&quot; in plaats van &quot;OS X 10.15.7&quot;).<p>Tijdens de release van Adobe zullen we deze namen corrigeren. De analytische gegevens en de CJA-rapportage worden met terugwerkende kracht bijgewerkt, aangezien bij de rapportage de naam van het besturingssysteem wordt opgezocht op basis van een id die als onderdeel van de gebeurtenisgegevens is opgenomen. Wanneer de opzoekwaarde die overeenkomt met een id is bijgewerkt, wordt alle rapportage gecorrigeerd, inclusief historische gegevens. Voor [!UICONTROL Data Feeds] klanten, is de verandering retroactief als u een gelijkaardig raadplegingsproces op het tijdstip van het melden gebruikt. Als u de waarde van het besturingssysteem echter opslaat in uw gebeurtenisgegevens, wordt de rapportage alleen in de toekomst bijgewerkt. Zie [Besturingssysteem](/help/components/dimensions/operating-systems.md) voor meer informatie . |
| **Bijwerken naar apparaatraadplegingen als gevolg van Google Client Hints** | 27 februari 2023 | Het voor 16 februari 2023 geplande gebruik van de tips voor de klant is uitgesteld om de kwaliteit van de raadplegingen van het apparaat met behulp van de tips beter te waarborgen. We zijn op 27 februari 2023 verder gegaan met de eerste fase van de release ter ondersteuning van Client Hints. De tweede en laatste fase van de release werd op donderdag 2 maart 2023 afgerond. [Meer informatie](/help/technotes/client-hints.md) |
| **Automatische migratie naar architectuur met classificatieset** | 8 februari 2023 | In de komende maanden is Adobe van plan om alle classificaties in alle organisaties te migreren naar de nieuwste classificatiearchitectuur. Naar schatting zullen de laatste klanten die naar migratie gaan, in mei 2023 plaatsvinden. Geen actie van de klant wordt vereist, en geen onderbreking wordt verwacht. Deze nieuwe architectuur heeft veel voordelen, zoals:<ul><li>Aanzienlijk kortere verwerkingstijd (72 uur → 24 uur)</li><li>De mogelijkheid om de [Classificatiesets](/help/components/classifications/sets/overview.md) UI</li><li>De optie om classificatiegegevens in Adobe Experience Platform in de toekomst via de [Adobe Analytics-bronconnector voor classificatiegegevens](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/classifications.html)</li></ul>Houd rekening met de volgende wijzigingen die mogelijk van invloed zijn op de workflow van uw organisatie:<ul><li>Wanneer u de browser of FTP-import gebruikt, &#39;[!UICONTROL Overwrite on conflict]&#39; is altijd ingeschakeld.</li><li>Wanneer u de browser of FTP-importmodule gebruikt, wordt de optie om direct na het importeren te exporteren niet meer ondersteund.</li><li>De API Analytics 2.0 `GetDimensions` het eindpunt keert nu koordherkenningstekens voor classificaties in plaats van numerieke herkenningstekens terug. Numerieke id&#39;s kunnen nog steeds worden gebruikt, maar Adobe raadt u aan waar mogelijk de nieuwe tekenreeks-id&#39;s te gebruiken. Numerieke id&#39;s kunnen worden opgehaald met de `?expansion=hidden` querytekenreeksparameter.</li></ul>Neem contact op met de klantenservice van Adobe als u een specifieker migratieplan voor uw organisatie wilt of vragen of zorgen hebt over deze migratie. [Meer informatie](/help/components/classifications/sets/overview.md) |

{style="table-layout:auto"}

## Aankondigingen einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **EOL, service Telefoontracering Japanse functies** | 21 maart 2023 | Alleen voor onze klanten in Japan: Bij de **eind mei 2023**, wordt de service Telefoontracering Japanse functies (mod_ktrack) beëindigd. Onze excuses voor het ongemak, maar wij vragen u om de modules die op uw Apache-server zijn geïnstalleerd, te verwijderen of uit te schakelen. Zie de pagina&#39;s 27 en 28 in [dit document](/help/release-notes/mod_ktrackforSiteCatalyst_ver1.40.pdf) ter referentie. |
| **EOL voor[!DNL Reports & Analytics]** | 7 maart 2023 | Effectief **31 december 2023**, is Adobe voornemens te stoppen [!DNL Reports & Analytics] en de bijbehorende verslagen en kenmerken. De rapporten, visualisaties en onderliggende technologie die macht [!DNL Reports & Analytics] voldoet niet meer aan de normen voor Adobe. Meeste [!DNL Reports & Analytics] functies zijn beschikbaar in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). Sinds de release van Analysis Workspace in 2015, [!DNL Reports & Analytics] functionaliteit en mogelijkheden zijn verplaatst naar Analysis Workspace en er is een drempel voor pariteit van de workflow bereikt. [Dit bericht](https://spark.adobe.com/page/6WnF8JK6IRDhf/) legt het einde van het levensproces uit.<p>Op 31 december 2023 zullen we een groot aantal van de bijbehorende functies voor rapporten en analyse beëindigen, waaronder, maar niet beperkt tot: Geplande Rapporten, de Uittreksels van Gegevens, en Rapporten DL. Na 31 december 2023 worden alle geplande rapporten niet meer verzonden. In **April 2023**, worden alle rapporten die volgens de planning na 31 december 2023 zouden verlopen, automatisch bijgewerkt en op 31 december 2023 weer afgehandeld. Bovendien kun je toekomstige rapporten niet langer plannen na 31 december 2023. |
| **EOL van [!UICONTROL People] metrisch** | 9 maart 2023 | Met de afgekeurde [[!DNL Device Co-op]](https://experienceleague.adobe.com/docs/discontinued/using/device-co-op.html), is de Device Co-op-related People-meting niet langer relevant. Op 8 mei 2023 zullen we de [!UICONTROL People] metrisch. Op dat moment zullen we de gegevens doorsturen naar de [!UICONTROL Unique Visitor] metrisch om projecten, segmenten en berekende metriek van het breken te verhinderen.<p>**Opmerking**: De [[!UICONTROL People] Metrisch gekoppeld aan apparaatanalyse](/help/components/metrics/people.md) Deze aankondiging heeft geen gevolgen. |
| **EOL van [!UICONTROL Publishing Lists] functie** | 29 september 2022 | In het kader van de regeling exportgerichte bedrijven voor rapporten en analyses [!UICONTROL Publishing Lists] zijn bedoeld om het einde van de levensduur van **december 2023**. U kunt geen nieuwe of bestaande [!UICONTROL Publishing Lists] om te verzenden of te plannen [!UICONTROL Analysis Workspace] projecten. |
| **EOL voor Data Workbench** | 14 september 2022 | Adobe is voornemens de Data Workbench aan het einde van de levensduur doeltreffend te maken **31 december 2023**. Zie [Aankondiging einde levensduur Data Workbench](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html) voor meer informatie. Neem contact op met de Adobe-accountmanager van uw organisatie voor vragen. |

{style="table-layout:auto"}

## AppMeasurement

Voor de meest recente updates over AppMeasurement-releases (versie 2.23.0) raadpleegt u [AppMeasurement voor JavaScript-releaseopmerkingen](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html).


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release voor 2022](/help/release-notes/2022.md)
* [Opmerkingen bij de release Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* De nieuwste release-updates voor [Adobe Experience Cloud-producten](https://business.adobe.com/products/adobe-experience-cloud-products.html)
