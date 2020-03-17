---
description: Nadat u een rapport hebt uitgevoerd, kunt u het rapport aanpassen om de gegevens naar wens weer te geven en te analyseren. U kunt rapportgegevens filteren, wijzigen hoe gegevens grafisch worden weergegeven, granulariteit van datums wijzigen, enzovoort.
title: Overzicht van rapporten aanpassen
topic: Reports and analytics
uuid: 37d221b7-50fd-4425-b2ba-f40911b72a2f
translation-type: tm+mt
source-git-commit: ''

---


# Overzicht van rapporten aanpassen

Nadat u een rapport hebt uitgevoerd, kunt u het rapport aanpassen om de gegevens naar wens weer te geven en te analyseren. U kunt rapportgegevens filteren, wijzigen hoe gegevens grafisch worden weergegeven, granulariteit van datums wijzigen, enzovoort.

## Een aangepast rapport maken {#task_BA6EACA3039C40AEA5605E1D8C76E646}

Stappen die beschrijven hoe te om de huidige configuratie van een rapport als nieuw douanerapport voor alle gebruikers te bewaren om te zien.

<!-- 

t_reports_custom.xml

 -->

Alleen beheerders kunnen een aangepast rapport maken. Wanneer u een douanerapport creeert, wordt het toegevoegd aan het belangrijkste rapporteringsmenu naast het rapport waarop het is gebaseerd.

**Een aangepast rapport maken**

1. Stel een rapport in werking en vorm het zonodig.
1. Klik op **[!UICONTROL More]** > **[!UICONTROL Create Custom Report]**.
1. Geef het rapport een naam en klik vervolgens op **[!UICONTROL Save.]**

   Zorg ervoor dat u geen bestaande rapportnaam dupliceert.

>[!MORELIKETHIS]
>
>* [Menu aanpassen](https://marketing.adobe.com/resources/help/en_US/reference/customize_menus.html)


## Selecteer een datum of een datumbereik {#task_9BEF7D4D839A4748B76E8500D1406C34}

De stappen die heet beschrijven om te gebruiken kiezen de tijdsperioden voor uw rapportgegevens.

<!-- 

t_reports_select_date.xml

 -->

U kunt specifieke dagen, weken, maanden of jaren selecteren. U kunt ook vergelijkingsrapporten uitvoeren.

Wanneer u een dashboard opent met rapporten met verschillende datumbereiken, kunt u een nieuw datumbereik kiezen in de kalender. De wijzigingen gelden voor alle rapporten in het dashboard.

**Een datumbereik selecteren**

1. Voer een rapport uit.
1. Klik op het kalenderpictogram rechtsboven.
1. Selecteer een datum.

   U kunt:

   * De dagen, maanden, of jaarperiodes van de mening (tot drie).
   * Sleep de cursor over datums om een bereik te selecteren.
   * Voer de datums handmatig in.
   * Klik op de naam van een maand om een maand te selecteren.
   * Klik **[!UICONTROL Select Preset]** om een vooraf ingestelde datum te selecteren.
   * Datums vergelijken.

1. Klik op **[!UICONTROL Run Report]**.

## Datums vergelijken {#task_95155C3700774B709F5FB81AE96B0824}

Stappen die beschrijven hoe u de kalender kunt gebruiken om datumvergelijkingen tussen gerangschikte rapporten in werking te stellen.

<!-- 

t_reports_comparing_dates.xml

 -->

U kunt geen datums vergelijken tussen trended-rapporten.

> [!NOTE] Als u een datumvergelijking op zeer belangrijke metriek in een dashboard wilt uitvoeren, kunt u de gegevens in de Bouwer [van het](https://marketing.adobe.com/resources/help/en_US/arb/) Rapport trekken gebruikend twee afzonderlijke verzoeken. Vervolgens gebruikt u aangepaste formules in Excel om het verschil tussen de twee formules te analyseren.

Datums vergelijken tussen gerangschikte rapporten in rapporten en analyses:

1. Voer een rapport uit.
1. Klik op de kalender rechtsboven.
1. Klik op **[!UICONTROL Compare Dates]**.
1. Selecteer de datums die u wilt gebruiken.
1. Klik op **[!UICONTROL Run Report]**.

## Een percentage weergeven als grafiek {#task_BC28CA19A4834AF6BFE68B5B5AEFE75D}

Stappen die beschrijven hoe te om of te specificeren om het percentage in een rapportlijst als grafiek te tonen.

<!-- 

t_reports_graph_percent.xml

 -->

Deze visualisatie is ook beschikbaar in dashboardrapporten.

1. Voer een rapport uit dat percentages ondersteunt, zoals een [!UICONTROL Pages Report].
1. Klik op **[!UICONTROL Percent Shown As: Graph]**.

## Rapportgegevens normaliseren {#task_8005B55E59BD479DA67BC618FF8BC94A}

Stappen die beschrijven hoe te om rapportgegevens te normaliseren.

<!-- 

t_reports_normalize.xml

 -->

Nadat u een rapport met vergeleken data in werking stelt, of voor vergelijkingen A/B, kunt u de gegevens normaliseren om het percentage van verandering tussen de rapporten te tonen. De secundaire gegevensset wordt aangepast om verschillen in het aantal geselecteerde dagen of voor verschillende verkeersvolumes te compenseren.

**Om rapportgegevens te normaliseren**

1. Voer een rapport uit dat datumvergelijkingen ondersteunt.
1. Klik **[!UICONTROL Compare Dates]** en geef de datum van de vergelijking op.
1. Klik op **[!UICONTROL Run Report]**.
1. Klik op **[!UICONTROL Normalize Data: Yes]**.

## Selecteer een pagina voor een rapport {#task_5CAC3B76BD4C4208B8D53DD972D4771F}

Stappen die beschrijven hoe te om een specifieke pagina van de pagina&#39;s van uw website voor een rapport te selecteren.

<!-- 

t_reports_select_page.xml

 -->

1. Genereer een rapport, bijvoorbeeld een rapport [!UICONTROL Page Views Report] ( **[!UICONTROL Reports]** > **[!UICONTROL Site Metrics]** > **[!UICONTROL Page Views]**).
1. Klik op de **[!UICONTROL Selected Page]** koppeling.
1. Selecteer [!UICONTROL Choose Page]op de pagina&#39;s die u wilt weergeven.
1. Zoek de pagina.
1. Klik op **[!UICONTROL OK.]**

## Rapportsuites vergelijken {#task_6BEBEB2D4F36497C9DA5B18ADAD35546}

Stappen die beschrijven hoe te om rapporten van twee rapportreeksen in het zelfde rapport te tonen.

<!-- 

t_reports_compare_suites.xml

 -->

Naast de grafische vertoning, geeft de lijst van het rapport u een percentagevergelijking. De volgende rapporten kunnen met vergelijkingen worden in werking gesteld:

* Site-inhoud
* Mobiel
* Verkeersbronnen
* Campagnes
* Producten
* Bezoeker retentie
* Bezoekerprofiel
* Aangepaste omzetting
* Aangepast verkeer
* Doel
* Enquête

**Rapportsuites vergelijken**

1. Genereer een rapport waarmee u rapporten kunt vergelijken.
1. Klik op de **[!UICONTROL Compare to Site]** koppeling.
1. Zoek de rapportsuite.
1. Klik op **[!UICONTROL OK.]**

## Geef de granulariteit van het rapport op {#task_7ED3EEC9E1704A918B25D06ADA3412E0}

Stappen die beschrijven hoe de totalen van rapporten per uur, dag, week, maand, driemaandelijks, of jaarlijks worden weergegeven.

<!-- 

t_reports_granularity.xml

 -->

De tijdsperiode van het rapport bepaalt welke granulariteitsopties beschikbaar zijn. U kunt bijvoorbeeld alleen selecteren **[!UICONTROL Hourly]** als u een tijdframe van één of twee dagen hebt geselecteerd. U kunt alleen **[!UICONTROL Yearly]** granulariteit selecteren als u meer dan een jaar hebt geselecteerd.

**Rapportgranulariteit opgeven**

1. Genereer een trendrapport, zoals **[!UICONTROL Site Content]** > **[!UICONTROL Pages.]**
1. Klik op de **[!UICONTROL View by]** koppeling en klik vervolgens op een granulariteit.

## Een dagrapport uitvoeren {#task_67CC818ACC3749839B69BDB2ED9AE6B8}

Stappen die beschrijven hoe rapporten op een specifieke dag van de week, zoals over elke Maandag in een bepaalde datumwaaier in werking te stellen.

<!-- 

t_reports_day_of_week.xml

 -->

Deze functie is alleen van toepassing op gefilterde rapporten met een datumbereik van week of dag.

1. Voer een trended-rapport uit over een opgegeven datumbereik.
1. Klik op de **[!UICONTROL Day of Week]** koppeling en klik vervolgens op een dag.

## Knop &#39;Uitproberen in werkruimte&#39; {#concept_DA41E22460B94BD9ADF63B1CEE2714A7}

Als u op de **[!UICONTROL Try In Workspace]** knop boven aan een rapport klikt, wordt hetzelfde rapport geladen in de analysewerkruimte.

<!-- 

try_in_workspace.xml

 -->

De meeste rapporten in Rapporten &amp; Analytics omvatten nu een knoop &quot;van het Probeer in Werkruimte&quot;om u toe te staan om de huidige mening in de Werkruimte van de Analyse voor verdere aanpassing te reproduceren.

De knop is momenteel alleen beschikbaar als uw gebruikersnaam volledige rechten heeft voor de analysewerkruimte.

Voor meer informatie over alle manieren kunt u uw rapport aanpassen, zie de gids van de Werkruimte [van de](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/) Analyse.
