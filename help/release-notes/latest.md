---
title: Opmerkingen bij de release Latest Analytics
description: Bekijk de huidige Adobe Analytics-releaseopmerkingen.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 15f1cd260709c2ab82d56a545494c31ad86d0ab0
workflow-type: tm+mt
source-wordcount: '1433'
ht-degree: 3%

---

# Opmerkingen bij de huidige Adobe Analytics-release (juni 2023)

**Laatste update**: 1 juni 2023

Adobe Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Geen hooglichten {#highlights}

| Functie | Beschrijving | [Uitvoeren start](releases.md) | [Algemene beschikbaarheid](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Het delen van verbindingen voor projecten (geen vereiste login)** | U kunt nu alleen-lezen koppelingen naar Analysis Workspace-projecten delen met mensen die geen toegang hebben tot Adobe Analytics. Dit omvat het delen met mensen buiten uw organisatie of met mensen binnen uw organisatie die niet zijn ingericht voor Adobe Analytics. [Meer informatie](../analyze/analysis-workspace/curate-share/share-projects.md#share-a-project-with-anyone-no-login-required)<p>Deze functionaliteit is standaard ingeschakeld en kan door de systeembeheerder worden uitgeschakeld. [Meer informatie](../analyze/analysis-workspace/user-preferences.md#company-preferences)</p> | 3 mei 2023 | 7 juni 2023 |
| **Nieuwe functies voor classificatiesets** | [Classificatiesets](/help/components/classifications/sets/overview.md) zijn bijgewerkt met verschillende nieuwe functies:<ul><li>**Consolidaties**: Combineer classificatiesets tot één enkel geconsolideerd classificatieset. De geconsolideerde classificatieset kan worden gebruikt als andere classificatiesets of als een set opzoekgegevens in Customer Jourey Analytics. [Meer informatie](../components/classifications/sets/consolidations/manage.md)</li><li>**Regels**: Waarden automatisch classificeren op basis van regels in de classificatieset. [Meer informatie](../components/classifications/sets/manage/rules.md)</li><li>**Automatisch importeren**: Importeer classificatiegegevens automatisch van cloudopslagbestemmingen. [Meer informatie](../components/classifications/sets/manage/schema.md)</li></ul> | | 7 juni 2023 |
| **Variabele van nieuw AppMeasurement** | De variabele `doubleEncodeLinkParameters` past randgevallen aan waarin implementaties multi-byte karakters in verbinding het volgen variabelen coderen. De meeste implementaties hoeven deze variabele niet te definiëren. [Meer informatie](../implement/vars/config-vars/doubleencodelinkparameters.md) |  | 7 juni 2023 |
| **Beveiligde doelen voor het exporteren van gegevenstoevoer** | Gegevensfeeds kunnen nu naar de volgende opslagdoelen in de cloud worden verzonden:<ul><li>Amazon S3</li><li>Azure RBAC</li><li>Azure SAS</li><li>Google Cloud Platform</li></ul>Doelen die voorheen beschikbaar waren (FTP, SFTP, S3 en Azure Blob) worden niet meer aanbevolen. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/create-feed.html) | 12 juni 2023 | 15 juli 2023 |
| **Bot-rapportage in Workspace** | Bot reporting is nu beschikbaar in Analysis Workspace. Deze functie wordt geleverd met verschillende toevoegingen:<ul><li>Een nieuwe dimensie: [Bot-naam](/help/components/dimensions/bot-name.md)</li><li>Twee nieuwe metriek: [Bodt paginaweergaven](/help/components/metrics/bot-page-views.md) en [Beide voorvallen](/help/components/metrics/bot-occurrences.md).</li><li>Een nieuwe berekende metrische sjabloon: [Hoogte-breedteverhouding van beide pagina&#39;s](/help/components/c-calcmetrics/cm-reference/default-calcmetrics.md)</li><li>Een nieuw rapport over de werkruimte: Bot-rapportage</li></ul>De nieuwe dimensie en metriek bevatten gegevens die vanaf maart 2023 zijn teruggevuld. |  | Juni 7,2023 |

{style="table-layout:auto"}

## Andere nieuwe of bijgewerkte functies {#other}

| Functie | Beschrijving | [Uitvoeren start](releases.md) | [Algemene beschikbaarheid](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Rijen met dynamische afmetingen uit een tabel voor vrije vorm verwijderen** | In een Freeform-tabel in Analysis Workspace kunt u nu snel specifieke rijen met dynamische afmetingen verwijderen met het x-pictogram. Hierbij wordt automatisch de filterregel &#39;Items altijd uitsluiten&#39; toegepast.<p>Eerder, de enige manier om rijen te schrappen die dynamische afmetingen bevatten was manueel een regel in de dialoog van de Filter te creëren. [Meer informatie](/help/analyze/analysis-workspace/visualizations/freeform-table/filter-and-sort.md)</p> | N.v.t. | 17 mei 2023 |
| **Nieuwe knop om een visualisatie in een deelvenster toe te voegen** | Er is nu een nieuwe knop beschikbaar onder aan elk deelvenster in Analysis Workspace, zodat u snel een visualisatie kunt toevoegen. <p>Eerder, de enige methodes om een visualisatie aan een paneel toe te voegen waren een visualisatie van de linkerspoorstaaf te slepen, een bestaande visualisatie te dupliceren of te kopiëren, of een leeg paneel tot stand te brengen. [Meer informatie](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md)</p> | N.v.t. | 17 mei 2023 |
| **Diepe koppeling (mobiele toepassing)** | Hiermee kunnen gebruikers koppelingen naar scorecards verzenden die rechtstreeks naar het scorecard-project in de app leiden. Hierdoor wordt het nog eenvoudiger om projecten te delen en de betrokkenheid van minder technische gebruikers te verhogen. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/analyze/mobapp/create-scorecard.html#share-scorecards-using-a-shareable-link) | N.v.t. | 17 mei 2023 |
| **Dynamische vervolgkeuzefilters** | Wij introduceren een nieuw type drop-down filter dat beschikbare waarden bepaalt die op gegevens binnen het rapporteringswaaier van het paneel en waarden in andere drop-down filters worden gebaseerd. U kunt dynamische vervolgkeuzefilters gebruiken door een dimensie naar de dropzone van het deelvenster te slepen terwijl u de muisknop ingedrukt houdt [!UICONTROL Shift]. Statische vervolgkeuzefilters blijven ongewijzigd door een groep dimensie-items naar de dropzone van het deelvenster te slepen terwijl u de muisknop ingedrukt houdt [!UICONTROL Shift]. [Meer informatie](/help/analyze/analysis-workspace/c-panels/panels.md) |  | 14 juni 2023 |
| **De bijgewerkte pagina Analytics Learning** | Het tabblad Leren op de Adobe Analytics-landingspagina bevat nu de volgende verbeteringen:<ul><li>Verbeterd ontwerp dat meer leerinhoud weergeeft op één pagina met verbeterde navigatie</li><li>Mogelijkheid om de leerinhoud op ervaringsniveau aan te passen (Beginnend, Midden, en Geavanceerd)</li></ul>[Meer informatie](/help/analyze/landing.md) |  | Juni 30,2023 |
| **Componenten sorteren in Analysis Workspace** | Er is nu een nieuwe sorteeroptie beschikbaar wanneer u componenten in de linkertrack of in het gegevenswoordenboek in Analysis Workspace bekijkt. U kunt componenten sorteren op Aanbevolen (de meest gebruikte), Alfabetisch of Categorisch (type).<p>Eerder kon u alleen componenten zoeken of filteren. [Meer informatie](/help/analyze/analysis-workspace/components/analysis-workspace-components.md)</p> | N.v.t. | TBD |

{style="table-layout:auto"}

## Oplossingen in Adobe Analytics

AN-311878; AN-313968; AN-314130; AN-315701; AN-315761; AN-316613; AN-317563; AN-318829; AN-319009; AN-319043; AN-319066; AN-319166; AN-319245; AN-319271; AN-319381; AN-319391; AN-319482; AN-319621; AN-319637; AN-319676; AN-320176; AN-320221; AN-320225; AN-320286; AN-320312; AN-320316; AN-320449; AN-320477; AN-320492; AN-320538; AN-320556; AN-320569; AN-320679; AN-320684; AN-320786; AN-320802; AN-320811; AN-320812; AN-320815; AN-321032; AN-321033; AN-321070; AN-321096; AN-321105; AN-321122; AN-321337;

## Belangrijke kennisgevingen voor Adobe Analytics-beheerders {#admin}

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| **Vervaldatum van 37 maanden voor aankoop-id&#39;s en gebeurtenis-id&#39;s (gebeurtenisserialisatie)** | Mei 25,2023 | Een aanstaande release van de Analytics Hit-verwerkingsengine, bedoeld voor vrijgave in **eind juni 2023 of begin juli 2023**, wordt begonnen met het afdwingen van een vervaldatum van 37 maanden voor aankoop-id&#39;s en gebeurtenis-id&#39;s (gebeurtenisserialisatie). Aankoop-id&#39;s en gebeurtenis-id&#39;s verlopen momenteel nooit in Adobe Analytics. Zodra een aankoop-id of een gebeurtenis-id wordt gezien/gebruikt, wordt bij elke toekomstige hit, ongeacht wanneer, die aankoop of gebeurtenis gemarkeerd als een duplicaat. Met de nieuwe verwerkingsmotor:<ul><li>Aankoop-id&#39;s en gebeurtenis-id&#39;s verlopen altijd na 37 maanden.</li><li>Als de aankoop-id of de gebeurtenis-id 37 maanden is geleden, wordt deze niet langer beschouwd als een dubbele aankoop of gebeurtenis.</li><li> Als u aankoop-id&#39;s of gebeurtenis-id&#39;s van meer dan 37 maanden geleden &quot;opnieuw gebruikt&quot;, worden ze niet langer beschouwd als duplicaten.</li></ul> |
| **Migratie naar Adobe I/O OAuth Server-aan-Server geloofsbrieven** | 11 mei 2023 | Adobe Analytics API- en Livestream-klanten die Adobe I/O JWT-gebruikersgegevens gebruiken, moeten naar Adobe I/O OAuth Server-to-Server-gebruikersgegevens migreren door **1 januari 2025**. Zie de kennisgeving aan het einde van de levensduur in de onderstaande tabel voor meer informatie en tijdlijnen. |
| **Nieuwe IP&#39;s die worden gebruikt door Adobe Analytics Data Feeds en Data Warehouse egress in het London Data Center** | 27 april 2023 | Dit betreft klanten in het Datacentrum van Londen die de verzoeken en/of rapporten hebben van de Diervoeders van Gegevens die aan de dienst FTP/SFTP worden geleverd. De volgende IP adreswaaiers zouden aan uw firewallconfiguratie moeten worden toegevoegd om toegang toe te staan: <ul><li>130.248.244.32/29</li><li>130.248.244.40/29</li></ul> |

{style="table-layout:auto"}

## Aankondigingen einde levensduur (EOL) {#eol}

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Migratie naar Adobe I/O OAuth Server-aan-Server geloofsbrieven** | 11 mei 2023 | Adobe Analytics API- en Livestream-klanten die Adobe I/O JWT-gebruikersgegevens gebruiken, moeten naar Adobe I/O OAuth Server-to-Server-gebruikersgegevens migreren door **1 januari 2025**. Adobe I/O staat niet toe dat vanaf 1 mei 2024 nieuwe JWT-referenties worden gemaakt. Klanten die JWT gebruiken moeten een nieuwe Server-aan-Server referentie OAuth tot stand brengen of hun bestaande JWT-referentie migreren naar een OAuth Server-aan-Server referentie. Klanten moeten ook hun clienttoepassingen bijwerken om de nieuwe OAuth Server-to-Server referenties te kunnen gebruiken. <ul><li>[Migreren van JWT-gebruikersgegevens (Service Account)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[Het gebruiken van de nieuwe geloofsbrieven van Server-aan-Server OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Veelgestelde vragen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |
| **EOL voor[!DNL Reports & Analytics]** | 7 maart 2023 | Effectief **31 december 2023**, is Adobe voornemens te stoppen [!DNL Reports & Analytics] en de bijbehorende verslagen en kenmerken. De rapporten, visualisaties en onderliggende technologie die macht [!DNL Reports & Analytics] voldoet niet meer aan de normen voor Adobe. Meeste [!DNL Reports & Analytics] functies zijn beschikbaar in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). Sinds de release van Analysis Workspace in 2015, [!DNL Reports & Analytics] functionaliteit en mogelijkheden zijn verplaatst naar Analysis Workspace en er is een drempel voor pariteit van de workflow bereikt. [Dit bericht](https://spark.adobe.com/page/6WnF8JK6IRDhf/) legt het einde van het levensproces uit.<p>Op 31 december 2023 zullen we een groot aantal van de bijbehorende functies voor rapporten en analyse beëindigen, waaronder, maar niet beperkt tot: Geplande Rapporten, de Uittreksels van Gegevens, en Rapporten DL. Na 31 december 2023 worden alle geplande rapporten niet meer verzonden. In **April 2023**, worden alle rapporten die volgens de planning na 31 december 2023 zouden verlopen, automatisch bijgewerkt en op 31 december 2023 weer afgehandeld. Bovendien kun je toekomstige rapporten niet langer plannen na 31 december 2023. |
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
