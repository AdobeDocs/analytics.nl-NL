---
title: Opmerkingen bij de release Latest Analytics
description: Bekijk de huidige Adobe Analytics-releaseopmerkingen.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 383266dddf4ccedcb354975bca3da5f4c6003285
workflow-type: tm+mt
source-wordcount: '1502'
ht-degree: 2%

---

# Huidige Adobe Analytics-releaseopmerkingen (mei 2023)

**Laatste update**: 30 mei 2023

Adobe Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of bijgewerkte functies in Adobe Analytics {#features}

| Functie | Beschrijving | [Uitvoeren start](releases.md) | [Algemene beschikbaarheid](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Backfill voor niet-productiesandboxen** | Wanneer u een gegevensstroom van de Analytics Source Connector maakt in een niet-productiesandbox, wordt de back-up van niet-productiesandboxen beperkt tot 3 maanden. Het zal 13 maanden blijven voor productie zandbakken. | N.v.t. | 26 april 2023 |
| **Het delen van verbindingen voor projecten (geen vereiste login)** | U kunt nu alleen-lezen koppelingen naar Analysis Workspace-projecten delen met mensen die geen toegang hebben tot Adobe Analytics. Dit omvat het delen met mensen buiten uw organisatie of met mensen binnen uw organisatie die niet zijn ingericht voor Adobe Analytics. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/share-projects.html?lang=en#share-public-link)<p>Deze functionaliteit is standaard ingeschakeld en kan door de systeembeheerder worden uitgeschakeld. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/user-preferences.html?lang=en#company-preferences)</p> | 3 mei 2023 | 5 juni 2023 |
| **Bijgewerkt startscherm voor de app Analytics-dashboards (Mobile App)** | Het nieuwe bijgewerkte scherm van het Huis staat u toe om elk van uw scorecards in één geconsolideerde scorecard lijst te bekijken.  Als u toegang tot meer dan één organisatie onder één login hebt, zullen alle scorecards van uw organisaties in één enkele lijst beschikbaar zijn. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/analyze/mobapp/executive.html#use-dashboards) | N.v.t. | 10 mei 2023 |
| **Componenten sorteren in Analysis Workspace** | Er is nu een nieuwe sorteeroptie beschikbaar wanneer u componenten in de linkertrack of in het gegevenswoordenboek in Analysis Workspace bekijkt. U kunt componenten sorteren op Aanbevolen (de meest gebruikte), Alfabetisch of Categorisch (type).<p>Eerder kon u alleen componenten zoeken of filteren. [Meer informatie](/help/analyze/analysis-workspace/components/analysis-workspace-components.md)</p> | N.v.t. | TBD |
| **Rijen met dynamische afmetingen uit een tabel voor vrije vorm verwijderen** | In een Freeform-tabel in Analysis Workspace kunt u nu snel specifieke rijen met dynamische afmetingen verwijderen met het x-pictogram. Hierbij wordt automatisch de filterregel &#39;Items altijd uitsluiten&#39; toegepast.<p>Eerder, de enige manier om rijen te schrappen die dynamische afmetingen bevatten was manueel een regel in de dialoog van de Filter te creëren. [Meer informatie](/help/analyze/analysis-workspace/visualizations/freeform-table/filter-and-sort.md)</p> | N.v.t. | 17 mei 2023 |
| **Nieuwe knop om een visualisatie in een deelvenster toe te voegen** | Er is nu een nieuwe knop beschikbaar onder aan elk deelvenster in Analysis Workspace, zodat u snel een visualisatie kunt toevoegen. <p>Eerder, de enige methodes om een visualisatie aan een paneel toe te voegen waren een visualisatie van de linkerspoorstaaf te slepen, een bestaande visualisatie te dupliceren of te kopiëren, of een leeg paneel tot stand te brengen. [Meer informatie](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md)</p> | N.v.t. | 17 mei 2023 |
| **Diepe koppeling (mobiele toepassing)** | Hiermee kunnen gebruikers koppelingen naar scorecards verzenden die rechtstreeks naar het scorecard-project in de app leiden. Hierdoor wordt het nog eenvoudiger om projecten te delen en de betrokkenheid van minder technische gebruikers te verhogen. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/analyze/mobapp/create-scorecard.html#share-scorecards-using-a-shareable-link) | N.v.t. | 17 mei 2023 |

{style="table-layout:auto"}

## Oplossingen in Adobe Analytics

AN-312098; AN-318309; AN-316675; AN-318173; AN-310359; AN-317613; AN-318836; AN-315744; AN-311772; AN-318719; AN-314074; AN-316651<!--"Verified" status-->; AN-318602; AN-315961; AN-317534; AN-318607; AN-316498; AN-316648; AN-318244; AN-317747; AN-318432; AN-318231; AN-317590; AN-318415; AN-318154; AN-316647; N-314417; AN-317614; AN-317725; AN-318114; AN-317876; AN-318052; AN-317966; AN-316477; AN-318036; AN-317931; AN-318045; AN-316246; AN-317281; AN-317879; AN-308077; AN-317708; AN-316115; AN-315963

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders {#admin}

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **Vervaldatum van 37 maanden voor aankoop-id&#39;s en gebeurtenis-id&#39;s (gebeurtenisserialisatie)** | Mei 25,2023 | Een aanstaande release van de Analytics Hit-verwerkingsengine, bedoeld voor vrijgave in **eind juni 2023 of begin juli 2023**, wordt begonnen met het afdwingen van een vervaldatum van 37 maanden voor aankoop-id&#39;s en gebeurtenis-id&#39;s (gebeurtenisserialisatie). Aankoop-id&#39;s en gebeurtenis-id&#39;s verlopen momenteel nooit in Adobe Analytics. Zodra een aankoop-id of een gebeurtenis-id wordt gezien/gebruikt, wordt bij elke toekomstige hit, ongeacht wanneer, die aankoop of gebeurtenis gemarkeerd als een duplicaat. Met de nieuwe verwerkingsmotor:<ul><li>Aankoop-id&#39;s en gebeurtenis-id&#39;s verlopen altijd na 37 maanden.</li><li>Als de aankoop-id of de gebeurtenis-id 37 maanden is geleden, wordt deze niet langer beschouwd als een dubbele aankoop of gebeurtenis.</li><li> Als u aankoop-id&#39;s of gebeurtenis-id&#39;s van meer dan 37 maanden geleden &quot;opnieuw gebruikt&quot;, worden ze niet langer beschouwd als duplicaten.</li></ul> |
| **Migratie naar AdobeIO OAuth Server-to-Server-referenties** | 11 mei 2023 | Adobe Analytics API- en Livestream-klanten die AdobeIO JWT-gebruikersgegevens gebruiken, moeten door **1 januari 2025**. Zie de kennisgeving aan het einde van de levensduur in de onderstaande tabel voor meer informatie en tijdlijnen. |
| **Nieuwe IP&#39;s die worden gebruikt door Adobe Analytics Data Feeds en Data Warehouse egress in het London Data Center** | 27 april 2023 | Dit betreft klanten in het Datacentrum van Londen die de verzoeken en/of rapporten hebben van de Diervoeders van Gegevens die aan de dienst FTP/SFTP worden geleverd. De volgende IP adreswaaiers zouden aan uw firewallconfiguratie moeten worden toegevoegd om toegang toe te staan: <ul><li>130.248.244.32/29</li><li>130.248.244.40/29</li></ul> |
| **Opzoekprocessen van apparaten gebruiken nu een derde voor alle apparaatopzoekacties** | 3 maart 2023 | Op 2 maart 2023, als deel van steunuitrol voor cliëntwenken, hebben wij onze processen van de apparatenraadpleging bijgewerkt om een derde voor alle apparatenraadplegingen te gebruiken. Eerder hadden we de derde alleen gebruikt voor zoekopdrachten voor mobiele apparaten. In het kader van deze uitrol werden sommige desktopbesturingssystemen onjuist aangeduid met de tekst &quot;mobile&quot; (bijvoorbeeld &quot;Mobile OS X 10.15.7&quot; in plaats van &quot;OS X 10.15.7&quot;).<p>Tijdens de release van Adobe zullen we deze namen corrigeren. De analytische gegevens en de CJA-rapportage worden met terugwerkende kracht bijgewerkt, aangezien bij de rapportage de naam van het besturingssysteem wordt opgezocht op basis van een id die als onderdeel van de gebeurtenisgegevens is opgenomen. Wanneer de opzoekwaarde die overeenkomt met een id is bijgewerkt, wordt alle rapportage gecorrigeerd, inclusief historische gegevens. Voor [!UICONTROL Data Feeds] klanten, zijn de veranderingen retroactief als u een gelijkaardig raadplegingsproces op het tijdstip van het melden gebruikt. Als u de waarde van het besturingssysteem echter opslaat in uw gebeurtenisgegevens, wordt de rapportage alleen in de toekomst bijgewerkt. Zie [Besturingssysteem](/help/components/dimensions/operating-systems.md) voor meer informatie . |

{style="table-layout:auto"}

## Aankondigingen einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Migratie naar AdobeIO OAuth Server-to-Server-referenties** | 11 mei 2023 | Adobe Analytics API- en Livestream-klanten die AdobeIO JWT-gebruikersgegevens gebruiken, moeten door **1 januari 2025**. AdobeIO staat niet toe dat vanaf 1 mei 2024 nieuwe JWT-referenties worden gemaakt. Klanten die JWT gebruiken moeten een nieuwe Server-aan-Server referentie OAuth tot stand brengen of hun bestaande JWT-referentie migreren naar een OAuth Server-aan-Server referentie. Klanten moeten ook hun clienttoepassingen bijwerken om de nieuwe OAuth Server-to-Server referenties te kunnen gebruiken. <ul><li>[Migreren van JWT-gebruikersgegevens (Service Account)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Het gebruiken van de nieuwe geloofsbrieven van Server-aan-Server OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Veelgestelde vragen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul>![](assets/jwt.png) |
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
