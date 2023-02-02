---
description: Nadat u een rapport hebt uitgevoerd, kunt u het rapport aanpassen om de gegevens naar wens weer te geven en te analyseren. U kunt rapportgegevens filteren, wijzigen hoe gegevens grafisch worden weergegeven, granulariteit van datums wijzigen, enzovoort.
title: Overzicht van rapporten aanpassen
uuid: 37d221b7-50fd-4425-b2ba-f40911b72a2f
feature: Reports & Analytics Basics
role: User, Admin
exl-id: 5a042fac-926e-4560-83bf-11f66ddb8273
source-git-commit: ce7f953b8f7f1f7d0616074454e4401937fcc0c7
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 3%

---

# Overzicht van rapporten aanpassen

{{ra-eol}}

Nadat u een rapport hebt uitgevoerd, kunt u het rapport aanpassen om de gegevens naar wens weer te geven en te analyseren. U kunt rapportgegevens filteren, wijzigen hoe gegevens grafisch worden weergegeven, granulariteit van datums wijzigen, enzovoort.

## Een aangepast rapport maken {#task_BA6EACA3039C40AEA5605E1D8C76E646}

U kunt de huidige configuratie van een rapport als nieuw douanerapport voor alle gebruikers opslaan om te zien.

<!-- 

t_reports_custom.xml

 -->

Alleen beheerders kunnen een aangepast rapport maken. Wanneer u een douanerapport creeert, wordt het toegevoegd aan het belangrijkste rapporteringsmenu naast het rapport waarop het is gebaseerd.

Een aangepast rapport maken:

1. Stel een rapport in werking en vorm het zonodig.
1. Klik op **[!UICONTROL More]** > **[!UICONTROL Create Custom Report]**.
1. Geef het rapport een naam en klik vervolgens op **[!UICONTROL Save.]**

   Zorg ervoor dat u geen bestaande rapportnaam dupliceert.

>[!MORELIKETHIS]
>
>* [Menu aanpassen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/customize-menus.html)


## Selecteer een datum of een datumbereik {#task_9BEF7D4D839A4748B76E8500D1406C34}

U kunt de tijdsperiodes voor uw rapportgegevens kiezen.

<!-- 

t_reports_select_date.xml

 -->

U kunt specifieke dagen, weken, maanden of jaren selecteren. U kunt ook vergelijkingsrapporten uitvoeren.

Wanneer u een dashboard opent met rapporten met verschillende datumbereiken, kunt u een nieuw datumbereik kiezen in de kalender. De wijzigingen gelden voor alle rapporten in het dashboard.

Een datumbereik selecteren:

1. Voer een rapport uit.
1. Klik op het kalenderpictogram rechtsboven.
1. Selecteer een datum.

   U kunt:

   * De dagen, maanden, of jaarperiodes van de mening (tot drie).
   * Sleep de cursor over datums om een bereik te selecteren.
   * Voer de datums handmatig in.
   * Klik op de naam van een maand om een maand te selecteren.
   * Klikken **[!UICONTROL Select Preset]** om een vooraf ingestelde datum te selecteren.
   * Datums vergelijken.

1. Klik op **[!UICONTROL Run Report]**.

## Datums vergelijken {#task_95155C3700774B709F5FB81AE96B0824}

U kunt de kalender gebruiken om datumvergelijkingen tussen gerangschikte rapporten uit te voeren.

<!-- 

t_reports_comparing_dates.xml

 -->

U kunt geen datums vergelijken tussen trended-rapporten.

>[!NOTE]
>
>Als u een datumvergelijking wilt uitvoeren op belangrijke metriek in een dashboard, kunt u de gegevens trekken [Report Builder](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/home.html) twee afzonderlijke verzoeken gebruiken. Vervolgens gebruikt u aangepaste formules in Excel om het verschil tussen de twee formules te analyseren.

Datums vergelijken tussen gerangschikte rapporten in rapporten en analyses:

1. Voer een rapport uit.
1. Klik op de kalender rechtsboven.
1. Klik op **[!UICONTROL Compare Dates]**.
1. Selecteer de datums die u wilt gebruiken.
1. Klik op **[!UICONTROL Run Report]**.

## Een percentage weergeven als grafiek {#task_BC28CA19A4834AF6BFE68B5B5AEFE75D}

U kunt specificeren of om het percentage in een rapportlijst als grafiek te tonen.

<!-- 

t_reports_graph_percent.xml

 -->

Deze visualisatie is ook beschikbaar in dashboardrapporten.

Het percentage weergeven als een grafiek in een rapporttabel:

1. Voer een rapport uit dat percentages ondersteunt, zoals een [!UICONTROL Pages Report].
1. Klik op **[!UICONTROL Percent Shown As: Graph]**.

## Rapportgegevens normaliseren {#task_8005B55E59BD479DA67BC618FF8BC94A}

<!-- 

t_reports_normalize.xml

 -->

Nadat u een rapport met vergeleken data in werking stelt, of voor vergelijkingen A/B, kunt u de gegevens normaliseren om het percentage van verandering tussen de rapporten te tonen. De secundaire gegevensset wordt aangepast om verschillen in het aantal geselecteerde dagen of voor verschillende verkeersvolumes te compenseren.

Om rapportgegevens te normaliseren:

1. Voer een rapport uit dat datumvergelijkingen ondersteunt.
1. Klikken **[!UICONTROL Compare Dates]** en geef vervolgens uw vergelijkingsdatum op.
1. Klik op **[!UICONTROL Run Report]**.
1. Klik op **[!UICONTROL Normalize Data: Yes]**.

## Selecteer een pagina voor een rapport {#task_5CAC3B76BD4C4208B8D53DD972D4771F}

Als u een specifieke pagina op de pagina&#39;s van uw website voor een rapport wilt selecteren:

<!-- 

t_reports_select_page.xml

 -->

1. Genereer een rapport, zoals een [!UICONTROL Page Views Report] ( **[!UICONTROL Reports]** > **[!UICONTROL Site Metrics]** > **[!UICONTROL Page Views]**).
1. Klik op de knop **[!UICONTROL Selected Page]** koppeling.
1. Aan [!UICONTROL Choose Page]selecteert u de pagina&#39;s die u wilt weergeven.
1. Zoek de pagina.
1. Klik op **[!UICONTROL OK.]**

## Rapportsuites vergelijken {#task_6BEBEB2D4F36497C9DA5B18ADAD35546}

U kunt rapporten van twee rapportreeksen in het zelfde rapport tonen.

<!-- 

t_reports_compare_suites.xml

 -->

Naast de grafische vertoning, geeft de lijst van het rapport u een percentagevergelijking. De volgende rapporten kunnen met vergelijkingen worden in werking gesteld:

* Sitecontent
* Mobile
* Verkeersbronnen
* Campagnes
* Producten
* Bezoekersbehoud
* Bezoekersprofiel
* Aangepaste omzetting
* Aangepast verkeer
* Target
* Enquête

Rapportsuites vergelijken:

1. Genereer een rapport waarmee u rapporten kunt vergelijken.
1. Klik op de knop **[!UICONTROL Compare to Site]** koppeling.
1. Zoek de rapportsuite.
1. Klik op **[!UICONTROL OK.]**

## Geef de granulariteit van het rapport op {#task_7ED3EEC9E1704A918B25D06ADA3412E0}

U kunt de totalen van rapporten weergeven op uurbasis, dagelijks, wekelijks, maandelijks, driemaandelijks of jaarlijks basis.

<!-- 

t_reports_granularity.xml

 -->

De tijdsperiode van het rapport bepaalt welke granulariteitsopties beschikbaar zijn. U kunt bijvoorbeeld alleen **[!UICONTROL Hourly]** als u een tijdkader van één of twee dagen hebt geselecteerd. U kunt alleen **[!UICONTROL Yearly]** korreligheid als u meer dan een jaar hebt geselecteerd.

Rapportgranulariteit opgeven:

1. Genereer een trendrapport, zoals **[!UICONTROL Site Content]** > **[!UICONTROL Pages.]**
1. Klik op de knop **[!UICONTROL View by]** en klikt u op een granulariteit.

## Een dagrapport uitvoeren {#task_67CC818ACC3749839B69BDB2ED9AE6B8}

U kunt rapporten op een specifieke dag van de week, zoals over elke Maandag in een bepaalde datumwaaier in werking stellen.

<!-- 

t_reports_day_of_week.xml

 -->

Deze functie is alleen van toepassing op gefilterde rapporten met een datumbereik van week of dag.

Een dagrapport uitvoeren:

1. Voer een trended-rapport uit over een opgegeven datumbereik.
1. Klik op de knop **[!UICONTROL Day of Week]** Klik op een dag.

## Knop &#39;Uitproberen in werkruimte&#39; {#concept_DA41E22460B94BD9ADF63B1CEE2714A7}

Klik op de knop **[!UICONTROL Try In Workspace]** knoop bij de bovenkant van een rapport zal het zelfde rapport in Analysis Workspace laden.

<!-- 

try_in_workspace.xml

 -->

De meeste rapporten in Rapporten &amp; Analytics omvatten nu de knoop van het &quot;Proberen in Werkruimte&quot;om u toe te staan om de huidige mening in Analysis Workspace voor verdere aanpassing te reproduceren.

De knop is momenteel alleen beschikbaar als je gebruikersnaam volledige rechten heeft op Analysis Workspace.

Voor meer informatie over alle manieren kunt u uw rapport aanpassen, zie [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html) hulplijn.
