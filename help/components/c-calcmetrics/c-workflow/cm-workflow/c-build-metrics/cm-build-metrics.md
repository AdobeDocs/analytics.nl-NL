---
description: De Berekende Bouwer van Metriek verstrekt een canvas om Afmetingen, Metriek, Segmenten, en Functies te slepen en te laten vallen om douanemetriek tot stand te brengen die op de logica van de containerhiërarchie, regels, en exploitanten wordt gebaseerd. Met dit geïntegreerde ontwikkelingshulpmiddel kunt u eenvoudige berekende metriek of complexe, berekende metriek bouwen en opslaan.
title: Metrische gegevens samenstellen
feature: Calculated Metrics
exl-id: 12bb3734-e25d-4c67-8c62-e1226d9aef94
source-git-commit: a1567366c9fad42b3836f43c681d5380e97b09f3
workflow-type: tm+mt
source-wordcount: '1143'
ht-degree: 1%

---

# Metrische gegevens samenstellen {#build-metrics}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_productcompatibility"
>title="Productcompatibiliteit"
>abstract="Geeft aan waar in Customer Journey Analytics deze berekende metrische waarde kan worden gebruikt, zoals in Analysis Workspace, Report Builder enzovoort. Sommige berekende metriek kunnen niet met experimenteren worden gebruikt."
>additional-url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-workspace/panels/experimentation#use-in-experimentation" text="Berekende meetwaarden gebruiken in experimenten"

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_externalid"
>title="Externe id"
>abstract="Het veranderen van Externe identiteitskaart zou kunnen beïnvloeden hoe berekende metrisch in externe bronnen zoals bedrijfsintelligentiegereedschappen verschijnt"

<!-- markdownlint-enable MD034 -->

Adobe Analytics biedt een canvas voor het slepen en neerzetten van dimensies, metriek, segmenten en functies om aangepaste metrische gegevens te maken op basis van logica in de containerhiërarchie, regels en operatoren. Met dit geïntegreerde ontwikkelprogramma kunt u eenvoudige of complexe berekende meetgegevens maken en opslaan.

## Beginnen met het bouwen van een berekende metrische waarde

U kunt de berekende metrische bouwer gebruiken om berekende metriek tot stand te brengen of uit te geven. Wanneer gecreeerd op deze manier, zijn de berekende metriek beschikbaar in de componentenlijst en kunnen dan in projecten door uw organisatie worden gebruikt. Alternatief, kunt u snel berekende metrisch tot stand brengen die slechts voor het project beschikbaar is waar het werd gecreeerd, zoals die in [ wordt beschreven creeer berekende metriek voor één enkel project ](/help/analyze/analysis-workspace/components/apply-create-metrics.md#create-calculated-metrics-for-a-single-project) in [ Metriek ](/help/analyze/analysis-workspace/components/apply-create-metrics.md).

Heb toegang tot de berekende metrische bouwer beginnen creërend berekende metrisch die in de componentenlijst beschikbaar is.

1. Heb toegang tot de berekende metrische bouwer op om het even welke volgende manieren:

   * Open in Analysis Workspace een project en selecteer vervolgens **[!UICONTROL Components]** > **[!UICONTROL Create metric]** .
   * In Analysis Workspace, open een project, dan selecteer **plus** pictogram naast de [!UICONTROL **sectie van Metriek**] in de linkerspoorlijn.
   * Ga in [!DNL Adobe Analytics] naar **[!UICONTROL Components]** > **[!UICONTROL Calculated metrics]** en selecteer vervolgens **[!UICONTROL + Add]** boven aan de pagina Berekende meetgegevens.

1. Ga met [ Gebieden van de berekende metrische bouwer ](#areas-of-the-calculated-metrics-builder) verder.

## Gebieden van de builder van Berekende metriek

In de volgende afbeelding en de bijbehorende tabel worden enkele hoofdgebieden en kenmerken van de builder van berekende metriek uitgelegd.

![](assets/cm_builder_ui.png)

| Locatie in afbeelding | Naam en functie |
|---|---|
| 1 | **Titel:** Naming metrisch is verplicht. U kunt metrisch opslaan tenzij het wordt genoemd. |
| 2 | **Beschrijving:** geef het een gebruikersvriendelijke beschrijving om te tonen wat het voor wordt gebruikt en het van gelijkaardige degenen te onderscheiden. <p>De beschrijving wordt ook weergegeven in een rapport. Het is beter NIET om de formule in de beschrijving te zetten - in plaats daarvan, beschrijf wat deze metrisch zou moeten en niet zouden moeten worden gebruikt. (De formule wordt geproduceerd aangezien u metrisch bouwt, onder de Summiere rubriek. Dientengevolge, is het niet nodig om de formule aan de beschrijving toe te voegen.) </p> |
| 3 | **Formaat:** de Keuzen omvatten Decimaal, Tijd, Percentage, en Valuta. |
| 4 | **Decimale Plaatsen:** toont hoeveel decimalen in het rapport zullen worden getoond. Het maximumaantal decimalen dat u kunt opgeven is 10. |
| 5 | **toon de Hogere Tendens als:** Deze metrische polariteit die toont of Analytics een stijgende trend in metrisch als goed (groen) of slecht (rood) zou moeten overwegen. Als gevolg hiervan zal de grafiek van het rapport als groen of rood worden weergegeven wanneer het omhoog gaat. |
| 6 | **Markeringen:** het Etiketteren is een goede manier om metriek te organiseren. Alle gebruikers kunnen tags maken en een of meer tags toepassen op een metrische waarde. U kunt echter alleen labels zien voor de segmenten die u bezit of die met u zijn gedeeld. Welke soorten markeringen moet u creëren? Hier volgen enkele suggesties voor handige tags:<ul><li>{de namen van 0} Team **, zoals Sociale Marketing, Mobiele Marketing.**</li><li>**Projecten** (analysetags), zoals ingang-pagina analyse.</li><li>**Categorieën**, zoals Vrouwen; Geografie.</li><li>**Werkschema&#39;s**, zoals om worden goedgekeurd; Gekruld voor (een specifieke bedrijfseenheid)</li></ul> |
| 7 | **Samenvatting:** <p>De Summiere formule werkt op elk ogenblik bij u een verandering in de metrische definitie aanbrengt. Deze formule wordt ook weergegeven in de metrische rail links als u de muisaanwijzer boven een metrische waarde houdt en op de knop <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Info_18_N.svg" id="image_BDA0EAF89C19440CB02AE248BA3F968E" /> pictogram. </p> |
| 8 | **Definitie:** dit is waar u in metriek/berekende metriek, segmenten, en/of functies sleept om berekende metrisch te bouwen. <ul><li>Als u in berekende metrisch sleept, zal het zijn metrische definitie automatisch uitbreiden. </li> <li>U kunt definities nesten met containers. In tegenstelling tot gesegmenteerde containers, functioneren deze containers als een wiskundige uitdrukking en bepalen de orde van verrichtingen. </li> </ul> |
| 9 | **Exploitant:** gedeeld door ( <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Divide_18_N.svg" width="15" id="image_320D7363DE024BDEB21E44606C8B367F" width="25px" /> ) is de standaardoperator, plus de operatoren +, - en x. |
| 10 | **Voorproef:** verstrekt een snel gelezen over om het even welke mogelijke fouten. De voorvertoning beslaat de laatste 90 dagen. Dit is een manier om aanvankelijk te graven of u de juiste componenten voor uw metrisch hebt geselecteerd. Een onverwacht resultaat zou betekenen u een tweede blik bij de metrische definitie moet nemen. |
| 11 | **de verenigbaarheid van het Product:** de verenigbaarheid van het Product toont u of metrisch met <a href="https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/current-data.html?lang=nl-NL"  > Huidige Gegevens </a>, met volledig Verwerkte Gegevens, of slechts met de rapporten van het Kanaal van de Marketing (first-touch toewijzing) compatibel is. <p>Opmerking: de huidige gegevens ondersteunen niet alle meetgegevens. Metriek die segmenten of functies bevatten, is niet compatibel met de huidige gegevens. <a href="/help/components/c-calcmetrics/cm-compatibility.md"  > Meer... </a> </p> </p> |
| 12 | **voegt toe:** voor alle soorten berekende metriek, kunt u containers en statische aantallen aan de definitie toevoegen. Voor geavanceerde berekende metriek, kunt u segmenten en functies ook toevoegen. <ul><li>Containers werken als een wiskundige expressie en bepalen de volgorde van bewerkingen. Dus alles in een container wordt verwerkt voor de volgende bewerking.</li><li>Als u een segment naar een container sleept, wordt alles in die container gesegmenteerd. (Alleen geavanceerde berekende cijfers)</li><li>U kunt meerdere segmenten in een container stapelen.</li></ul> |
| 13 | **het pictogram van het Gewas (Metrische Type, Attributie):** het selecteren van het tandwielpictogram naast metrisch laat u het <a href="/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md"  > metrische type en attributiemodellen </a> specificeren. |
| 14 | **Nieuw:** laat u een nieuwe component, zoals een nieuw segment tot stand brengen (dat u aan <a href="/help/components/segmentation/segmentation-workflow/seg-build.md"  > de Bouwer van het Segment </a> neemt.) |
| 15 | **Componenten van het Onderzoek:** Deze onderzoeksbar laat u naar dimensies, metriek, segmenten (gevorderde berekende metriek slechts), en functies (geavanceerde berekende metriek slechts) zoeken. |
| 16 | **Lijst van Afmetingen:** eerder dan het verlaten van Berekende Metrische Bouwer om een eenvoudig segment (in de Bouwer van het Segment) te bouwen, b.v. &quot;Pagina = Homepage&quot;, kunt u in Pagina slepen en Homepage direct van de Berekende Metrische Bouwer selecteren.<p>Dit resulteert in een veel gestroomlijnder werkschema voor het creëren van gesegmenteerde berekende metriek.</p> |
| 17 | **Lijst van Metriek:** Metriek komt in 3 categorieën: <ul> <li>Standaardmetriek (<img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Event_18_N.svg" id="image_65A80F54D73443E78542FE0B31CC3F20" />) </li><li>Berekende cijfers ( <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calculator_18_N.svg" id="image_C5674AB9B9EB4DA9A56782D15822C319" />) </li><li id="li_8735E76637ED4C3F983731A66E04C93E">Metrische sjablonen ( <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Folder_18_N.svg" id="image_D236601511CC4DD3828F223431E27E88" /> ) - onder aan de lijst. </li> </ul> <p>Wanneer u de muisaanwijzer boven een metrische waarde houdt, ziet u het pictogram Info rechts ervan: <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Info_18_N.svg" width="15px" id="image_5A65E772A68A4B94ACAD6552CCF21F5F" />. Als u op dit pictogram klikt, krijgt u de volgende informatie: </p><ul> <li>De formule van hoe het wordt berekend. </li><li>Een voorproeftrend van metrisch. </li><li>Een pictogram voor bewerken (potlood) <img placement="break" align="center"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Edit_18_N.svg" width="15px" id="image_7D5B2F026A034118BE4DA81B9215A883" /> bij het hoogste recht dat u aan de Berekende Bouwer van Metriek zal nemen waar u deze berekende metrische waarde kunt uitgeven. </li></ul> |
| 18 | **Lijst van Segmenten:** (Geavanceerde berekende metriek slechts) als Admin, toont deze lijst alle segmenten die in uw login bedrijf worden gecreeerd. Als u een gebruiker niet-Admin bent, toont deze lijst segmenten u bezit en die met u worden gedeeld. <a href="https://experienceleague.adobe.com/docs/analytics/components/segmentation/segment-reference/seg-rights.html?lang=nl-NL"  > Meer... </a> |
| 19 | **Lijst van Functies:** (Geavanceerde berekende metriek slechts) de Functies worden verdeeld in twee lijsten: <a href="/help/components/c-calcmetrics/cm-reference/cm-functions.md"  > Basis </a> (het meest vaak gebruikt) en <a href="/help/components/c-calcmetrics/cm-reference/cm-adv-functions.md"  > Geavanceerd </a>. |
| 20 | **de selecteur van de Reeks van het Rapport:** laat u aan een verschillende rapportreeks schakelen. |

{style="table-layout:auto"}
