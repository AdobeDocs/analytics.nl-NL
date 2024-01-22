---
description: Beschrijvingen van de types van rapportsuite en vergelijking van globale rapportsuites en rollup rapportsuites.
title: Methoden van rapportsuite
feature: Report Suite Settings
exl-id: 97bdc9bd-2212-436b-b3b4-ec518624f9e6
source-git-commit: 4545c3839586231918ba5ebbf17fcac5a366abab
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 0%

---

# Methoden van rapportsuite

<!-- change filename since page name changed? -->

U kunt uw rapportreeksen als één van beide vormen *algemene rapportensuites* of *rollup-rapportsuites*.

## Globale rapportsuites

Een algemene rapportsuite verzamelt gegevens van alle domeinen en apps die eigendom zijn van uw organisatie. De implementatie vereist om alle verzoeken om images naar één rapportsuite te verzenden.

Adobe beveelt in de meeste gevallen aan een algemene rapportenreeks te implementeren. Zie &quot;[Overwegingen voor algemene rapporten](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/global-rs.html)&quot; voor de voordelen van de implementatie van een algemene rapportenreeks.

Met de *taggen met meerdere suite* en *virtuele rapportsuite* benaderingen:

* **Tags toevoegen met meerdere suite**: Met tags met meerdere suite kunt u verzoeken om afbeeldingen niet alleen naar een algemene rapportsuite verzenden, maar ook naar afzonderlijke groepen met onderliggende rapporten. De globale rapportgegevens worden gededupliceerd over alle rapportsuites.

  Bijvoorbeeld, zou u alle gegevens in één globaal rapportreeks kunnen verzamelen en ook secundaire rapportsuites opzetten die op merk, regio, of een andere differentiator worden gebaseerd. De verschillende teams in uw bedrijf konden zich dan op gegevens in de rapportreeksen concentreren die voor hen relevant zijn.

  Om multi-suite het etiketteren te gebruiken, voer de reeksen van het kindrapport en een globale rapportreeks uit die alle gegevens van de kinderen omvat. De volgende code voor uw webpagina&#39;s en apps zal identiteitskaart van de Reeks van het Rapport (RSID) voor de globale rapportreeks en ook RSIDs voor de toepasselijke reeksen van het kindrapport omvatten.<!-- Wording/be more specific? And include any links? -->

  Er wordt een aparte serveraanroep naar elke rapportsuite in de afbeeldingsaanvraag uitgevoerd. De vraag aan de reeksen van het kindrapport is secundaire vraag.

* **Virtuele rapportsuite**: A [virtuele rapportsuite](/help/components/vrs/vrs-about.md) is een vraag op gespecificeerde segmenten die in een globale rapportreeks worden verzameld, en beschikbaar aan gespecificeerde groepen gebruikers. De virtuele rapportsuites staan u toe om rapportelementen voor verschillende eindgebruikers te leiden zonder multi-suite het etiketteren te gebruiken, waarbij secundaire servervraag wordt vermeden.

  Om virtuele rapportreeksen te gebruiken, voer een globale rapportreeks uit en ontleed dan de gegevens om virtuele rapportreeksen met specifieke toegepaste segmenten en met specifieke groepstoestemmingen tot stand te brengen. U kunt virtuele rapportsuites in Virtuele rapportreeksmanager tot stand brengen ([!UICONTROL Components] > [!UICONTROL Virtual report suites]). Zie &quot;[Workflow voor virtuele rapportsuite](/help/components/vrs/c-workflow-vrs/vrs-workflow.md)&quot; voor meer informatie .

Het gebruik van virtuele-rapportsuites in plaats van taggen met meerdere suite is vaak de beste manier, maar virtuele-rapportsuites hebben een aantal beperkingen. Zie &quot;[Virtuele rapportreeksen en tagging met meerdere suite](/help/components/vrs/vrs-considerations.md)&quot; om te bepalen welke rapportsuite-benadering de beste keuze is voor uw bedrijfsbehoeften. Voor een diepgaande vergelijking van virtuele rapportsuites en multi-suite het etiketteren functionaliteit, zie &quot;[Virtuele rapportsuite versus tagging met meerdere suite](/help/components/vrs/vrs-about.md#section_317E4D21CCD74BC38166D2F57D214F78).&quot;

## Rolluprapporten

>[!NOTE]
>
>[!DNL Reports & Analytics] is het enige hulpmiddel dat rollup rapporten steunde. Rapporten en analyses zijn op 17 januari 2024 beëindigd.

<!---### Limitations of Rollup Reports {#limitations-rollups}

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
