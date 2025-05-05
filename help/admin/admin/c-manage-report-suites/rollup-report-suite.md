---
description: Beschrijvingen van globale rapportsuites
title: Globale rapportsuites
feature: Report Suite Settings
exl-id: 97bdc9bd-2212-436b-b3b4-ec518624f9e6
role: Admin
source-git-commit: 2f61febc3e19b4b8d57833204b987cb64a9b7467
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# Globale rapportsuites

Een algemene rapportsuite verzamelt gegevens van alle domeinen en apps die eigendom zijn van uw organisatie. De implementatie vereist om alle verzoeken om images naar één rapportsuite te verzenden.

Adobe raadt in de meeste gevallen aan een algemene rapportsuite te implementeren. Zie &quot;[ Globale overwegingen van de rapportreeks ](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/global-rs.html?lang=nl-NL)&quot;voor de voordelen om een globale rapportreeks uit te voeren.

U kunt subsets van de globale gegevens van de het rapportreeks van uw bedrijf aan verschillende eind verstrekken gebruikers gebruikend *multi-suite het etiketteren* en *virtuele de benaderingen van de rapportreeks*:

* **multi-suite het etiketteren**: Het multi-suite etiketteren staat u toe om beeldverzoeken niet alleen naar een globale rapportreeks maar ook naar individuele de reeksen van het kindrapport te verzenden. De globale rapportgegevens worden gededupliceerd over alle rapportsuites.

  Bijvoorbeeld, zou u alle gegevens in één globaal rapportreeks kunnen verzamelen en ook secundaire rapportsuites opzetten die op merk, regio, of een andere differentiator worden gebaseerd. De verschillende teams in uw bedrijf konden zich dan op gegevens in de rapportreeksen concentreren die voor hen relevant zijn.

  Om multi-suite het etiketteren te gebruiken, voer de reeksen van het kindrapport en een globale rapportreeks uit die alle gegevens van de kinderen omvat. De volgende code voor uw webpagina&#39;s en apps zal identiteitskaart van de Reeks van het Rapport (RSID) voor de globale rapportreeks en ook RSIDs voor de toepasselijke reeksen van het kindrapport omvatten.<!-- Wording/be more specific? And include any links? -->

  Er wordt een aparte serveraanroep naar elke rapportsuite in de afbeeldingsaanvraag uitgevoerd. De vraag aan de reeksen van het kindrapport is secundaire vraag.

* **Virtuele rapportreeks**: A [ virtuele rapportreeks ](/help/components/vrs/vrs-about.md) is een vraag op gespecificeerde segmenten die in een globale rapportreeks worden verzameld, en beschikbaar aan gespecificeerde groepen gebruikers. De virtuele rapportsuites staan u toe om rapportelementen voor verschillende eindgebruikers te leiden zonder multi-suite het etiketteren te gebruiken, waarbij secundaire servervraag wordt vermeden.

  Om virtuele rapportreeksen te gebruiken, voer een globale rapportreeks uit en ontleed dan de gegevens om virtuele rapportreeksen met specifieke toegepaste segmenten en met specifieke groepstoestemmingen tot stand te brengen. U kunt virtuele rapportsuites in de Virtuele manager van de rapportsuites tot stand brengen ([!UICONTROL Components] > [!UICONTROL Virtual report suites]). Zie &quot;[ het Virtuele werkschema van de rapportreeks ](/help/components/vrs/c-workflow-vrs/vrs-workflow.md)&quot;voor meer informatie.

Het gebruik van virtuele-rapportsuites in plaats van taggen met meerdere suite is vaak de beste manier, maar virtuele-rapportsuites hebben een aantal beperkingen. Zie &quot;[ Virtuele rapportsuites en multi-suite het etiketteren overwegingen ](/help/components/vrs/vrs-considerations.md)&quot;om te bepalen welke benadering van de rapportsuite de beste keus voor uw bedrijfsbehoeften is. Voor een diepgaande vergelijking van virtuele rapportsuites en multi-suite het etiketteren functionaliteit, zie [ Virtuele rapportsuites vs. multi-suite het etiketteren ](/help/components/vrs/vrs-about.md#section_317E4D21CCD74BC38166D2F57D214F78).

<!---## Rollup reports

>[!NOTE]
>
>[!DNL Reports & Analytics] is the only tool that supported rollup reports. Reports & Analytics was end-of-lifed on January 17, 2024.

Limitations of Rollup Reports {#limitations-rollups}

* Rollups provide total data, but they do not report individual values in reports. For example, eVar1 values are not included, but their aggregate total can be.
* Data is not deduplicated when the rollup combines data across report suites.
* Rollups run nightly at midnight.
* When you add a report suite to an existing rollup, historical data is not included in the rollup.
* All child report suites must have data in them for a rollup to function. If new report suites are included in a rollup, make sure to send at least one page view to each of those report suites.
* Rollup report suites can include a maximum of 40 child report suites.
* Rollup report suites can include a maximum of 100 events.
* Data contained in rollup report suites does not support breakdowns or segments.
* The Pages report is replaced with the Most Popular Sites report, which reports on metrics at the child-suite level.

## Comparison of Global Report Suite and Rollup Report  Features

**Secondary server calls**: Rollups do not incur any additional server calls beyond what a single report suite collects. If your organization uses multi-suite tagging, secondary server calls are made for each additional report suite included in an image request.

>[!TIP]
>
>If you use only a global report suite with [virtual report suites](/help/components/vrs/vrs-considerations.md), no secondary server calls are needed.

**Implementation changes**: Rollups do not require any implementation changes, while global report suites require you to include the global report suite ID in your implementation.

**Duplication**: Global report suites deduplicate unique visitors, while rollups do not. For example, if a user visits three of your domains in the same day, rollups would count three daily unique visitors. Global report suites would record one unique visitor.

**Time frame**: Rollups are only processed at midnight each night, while global report suites report data with standard latency.

**Breadth**: Rollups have no way to communicate between report suites. Global report suites can attribute credit to conversion variables between report suites and provide pathing across report suites.

**Historical data**: Rollups can aggregate historical data, while global report suites only report data from the point they were implemented.

**Reports**: Global report suites provide data on all dimensions; rollups provide aggregate data on only high-level reports.

**Supported products**: Rollups could only be used in Reports & Analytics. They are not supported in Analysis Workspace, or Data Warehouse. Global report suites can be used across all products.

**Number of aggregated report suites**: Rollups only support a maximum of 40 child report suites. Global report suites can be implemented on any number of domains or apps that you own.--->
