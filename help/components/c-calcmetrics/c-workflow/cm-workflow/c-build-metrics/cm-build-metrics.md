---
description: De Berekende Bouwer van Metriek verstrekt een canvas om Dimension, Metriek, Segmenten, en Functies te slepen en te laten vallen om douanemetriek tot stand te brengen die op containerhiërarchische logica, regels, en exploitanten wordt gebaseerd. Met dit geïntegreerde ontwikkelingshulpmiddel kunt u eenvoudige berekende metriek of complexe, berekende metriek bouwen en opslaan.
title: Metrische gegevens samenstellen
feature: Calculated Metrics
exl-id: 12bb3734-e25d-4c67-8c62-e1226d9aef94
source-git-commit: a6b7622562ced9d28229e094f027c8d0ee79532b
workflow-type: tm+mt
source-wordcount: '1003'
ht-degree: 2%

---

# Metrische gegevens samenstellen

Adobe Analytics biedt een canvas voor het slepen en neerzetten van dimensies, metriek, segmenten en functies om aangepaste metrische gegevens te maken op basis van logica in de containerhiërarchie, regels en operatoren. Met dit geïntegreerde ontwikkelprogramma kunt u eenvoudige of complexe berekende meetgegevens maken en opslaan.

## Beginnen met het bouwen van een berekende metrische waarde

U kunt op de volgende manieren beginnen met het maken van een berekende metrische waarde:

* Open in Analysis Workspace een project en selecteer vervolgens **[!UICONTROL Components]** > **[!UICONTROL Create metric]**.
* Open in Analysis Workspace een project en selecteer vervolgens de **Plus** pictogram naast [!UICONTROL **Metrisch**] in de linkerspoorstaaf.
* In [!DNL Analytics], ga naar **[!UICONTROL Components]** > **[!UICONTROL Calculated metrics]** selecteert u vervolgens **[!UICONTROL + Add]** boven aan de pagina Berekende metriek.

## Gebieden van de builder van Berekende metriek

In de volgende afbeelding en de bijbehorende tabel worden enkele hoofdgebieden en kenmerken van het beheer van berekende metriek uitgelegd.

![](assets/cm_builder_ui.png)

| Locatie in afbeelding | Naam en functie |
|---|---|
| 1 | **Titel:** De naam van de metrische waarde is verplicht. U kunt metrisch opslaan tenzij het wordt genoemd. |
| 2 | **Omschrijving:** Geef het een gebruikersvriendelijke beschrijving om te tonen waarvoor het wordt gebruikt en het van gelijkaardige degenen te onderscheiden. <p>De beschrijving wordt ook weergegeven in een rapport. Het is beter NIET om de formule in de beschrijving te zetten - in plaats daarvan, beschrijf wat deze metrisch zou moeten en niet zouden moeten worden gebruikt. (De formule wordt geproduceerd aangezien u metrisch bouwt, onder de Summiere rubriek. Dientengevolge, is het niet nodig om de formule aan de beschrijving toe te voegen.) </p> |
| 3 | **Indeling:** U kunt kiezen uit Decimaal, Tijd, Percentage en Valuta. |
| 4 | **Decimalen:** Toont hoeveel decimalen in het rapport zullen worden getoond. Het maximumaantal decimalen dat u kunt opgeven, is 10. |
| 5 | **Toon de Opwaartse Trend als:** Deze metrische polariteit die toont of de Analyse een stijgende trend in metrisch als goed (groen) of slecht (rood) zou moeten beschouwen. Als gevolg hiervan zal de grafiek van het rapport als groen of rood worden weergegeven wanneer het omhoog gaat. |
| 6 | **Tags:** Tags zijn een goede manier om metriek in te delen. Alle gebruikers kunnen tags maken en een of meer tags toepassen op een metrische waarde. U kunt echter alleen labels zien voor de segmenten die u bezit of die met u zijn gedeeld. Welke soorten markeringen moet u creëren? Hier volgen enkele suggesties voor handige tags:<ul><li>**Teamnamen**, zoals Sociale marketing, Mobiele marketing.</li><li>**Projecten** (analysetags), zoals analyse van de pagina Entry.</li><li>**Categorieën**, zoals vrouwen; Geografie.</li><li>**Workflows**, zoals goed te keuren; Gecurreerd voor (een specifieke bedrijfseenheid)</li></ul> |
| 7 | **Overzicht:** <p>De Summiere formule werkt op elk ogenblik bij u een verandering in de metrische definitie aanbrengt. Deze formule wordt ook weergegeven in de metrische rail links als u de muisaanwijzer boven een metrische waarde houdt en op de knop <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Info_18_N.svg" id="image_BDA0EAF89C19440CB02AE248BA3F968E" /> pictogram. </p> |
| 8 | **Definitie:** Dit is waar u in metriek/berekende metriek, segmenten, en/of functies sleept om berekende metrisch te bouwen. <ul><li>Als u in berekende metrisch sleept, zal het zijn metrische definitie automatisch uitbreiden. </li> <li>U kunt definities nesten met containers. In tegenstelling tot gesegmenteerde containers, functioneren deze containers als een wiskundige uitdrukking en bepalen de orde van verrichtingen. </li> </ul> |
| 9 | **Operator:** Gedeeld door ( <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Divide_18_N.svg" width="15" id="image_320D7363DE024BDEB21E44606C8B367F" width="25px" /> ) is de standaardoperator, plus de operatoren +, - en x. |
| 10 | **Voorvertoning:** Hiermee kunt u snel informatie lezen over mogelijke fouten. De voorvertoning beslaat de laatste 90 dagen. Dit is een manier om aanvankelijk te graven of u de juiste componenten voor uw metrisch hebt geselecteerd. Een onverwacht resultaat zou betekenen u een tweede blik bij de metrische definitie moet nemen. |
| 11 | **Productcompatibiliteit:** <p>De verenigbaarheid van het product toont u of metrisch compatibel is met <a href="https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/current-data.html"  > Huidige gegevens </a>, met volledig verwerkte gegevens of alleen met marketingrapporten (first-touch-toewijzing). <p>Opmerking: De huidige Gegevens steunen niet alle metriek. Metriek die segmenten of functies bevatten, is niet compatibel met de huidige gegevens. <a href="/help/components/c-calcmetrics/cm-compatibility.md"  > Meer... </a> </p> </p> |
| 12 | **Toevoegen:** Voor alle soorten berekende metriek, kunt u containers en statische aantallen aan de definitie toevoegen. Voor geavanceerde berekende metriek, kunt u segmenten en functies ook toevoegen. <ul><li>Containers werken als een wiskundige expressie en bepalen de volgorde van bewerkingen. Dus alles in een container wordt verwerkt voor de volgende bewerking.</li><li>Als u een segment naar een container sleept, wordt alles in die container gesegmenteerd. (Alleen geavanceerde berekende cijfers)</li><li>U kunt meerdere segmenten in een container stapelen.</li></ul> |
| 13 | **Pictogram tandwiel (metrisch type, kenmerk):** Als u het tandwielpictogram naast een metrische waarde selecteert, kunt u de instelling <a href="/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md"  > Metrische type- en attributiemodellen </a>. |
| 14 | **Nieuw:** Hiermee kunt u een nieuwe component maken, zoals een nieuw segment (dat u naar het <a href="/help/components/segmentation/segmentation-workflow/seg-build.md"  > Segment Builder </a>.) |
| 15 | **Componenten zoeken:** Met deze zoekbalk kunt u zoeken naar afmetingen, metriek, segmenten (alleen geavanceerde berekende meetgegevens) en functies (alleen geavanceerde berekende meetgegevens). |
| 16 | **Lijst met Dimension:** In plaats van de Berekende Metrische Bouwer te verlaten om een eenvoudig segment (in de Bouwer van het Segment) te bouwen, b.v. &quot;Pagina = Homepage&quot;, kunt u in Pagina slepen en Homepage van Berekende Metrische Bouwer direct selecteren.<p>Dit resulteert in een veel gestroomlijnder werkschema voor het creëren van gesegmenteerde berekende metriek.</p> |
| 17 | **Lijst met metriek:** De cijfers zijn ingedeeld in drie categorieën: <ul> <li>Standaardwaarden (<img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Event_18_N.svg" id="image_65A80F54D73443E78542FE0B31CC3F20" />) </li><li>Berekende standaarden ( <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calculator_18_N.svg" id="image_C5674AB9B9EB4DA9A56782D15822C319" />) </li><li id="li_8735E76637ED4C3F983731A66E04C93E">Metrische sjablonen ( <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Folder_18_N.svg" id="image_D236601511CC4DD3828F223431E27E88" />) - onder aan de lijst. </li> </ul> <p>Wanneer u de muisaanwijzer boven een metrische waarde houdt, ziet u het pictogram Info rechts ervan: <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Info_18_N.svg" width="15px" id="image_5A65E772A68A4B94ACAD6552CCF21F5F" />. Als u op dit pictogram klikt, krijgt u de volgende informatie: </p><ul> <li>De formule van hoe het wordt berekend. </li><li>Een voorproeftrend van metrisch. </li><li>Een bewerkingspictogram (potlood) <img placement="break" align="center"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Edit_18_N.svg" width="15px" id="image_7D5B2F026A034118BE4DA81B9215A883" /> bij het hoogste recht dat u aan de Berekende Bouwer van Metriek zal nemen waar u deze berekende metrisch kunt uitgeven. </li></ul> |
| 18 | **Lijst met segmenten:** (Alleen Geavanceerde berekende metriek) Als beheerder worden in deze lijst alle segmenten weergegeven die in uw aanmeldingsbedrijf zijn gemaakt. Als u een gebruiker niet-Admin bent, toont deze lijst segmenten u bezit en die met u worden gedeeld. <a href="https://experienceleague.adobe.com/docs/analytics/components/segmentation/segment-reference/seg-rights.html"  > Meer... </a> |
| 19 | **Lijst met functies:** (Alleen geavanceerde berekende metriek) Functies worden in twee lijsten onderverdeeld: <a href="/help/components/c-calcmetrics/cm-reference/cm-functions.md"  > Basis </a> (meest gebruikt) en <a href="/help/components/c-calcmetrics/cm-reference/cm-adv-functions.md"  > Geavanceerd </a>. |
| 20 | **Selector rapportsuite:** Hiermee kunt u overschakelen op een andere rapportsuite. |

{style="table-layout:auto"}
