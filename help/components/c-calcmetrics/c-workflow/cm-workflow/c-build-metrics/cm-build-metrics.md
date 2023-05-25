---
description: De Berekende Bouwer van Metriek verstrekt een canvas om Dimension, Metriek, Segmenten, en Functies te slepen en te laten vallen om douanemetriek tot stand te brengen die op containerhiërarchische logica, regels, en exploitanten wordt gebaseerd. Met dit geïntegreerde ontwikkelingshulpmiddel kunt u eenvoudige berekende metriek of complexe, berekende metriek bouwen en opslaan.
title: Metrische gegevens samenstellen
feature: Calculated Metrics
exl-id: 12bb3734-e25d-4c67-8c62-e1226d9aef94
source-git-commit: c64b4199d93443b14e2012459a4d33fdd847eca1
workflow-type: tm+mt
source-wordcount: '955'
ht-degree: 0%

---

# Metrische gegevens samenstellen

Adobe Analytics biedt een canvas voor het slepen en neerzetten van dimensies, metriek, segmenten en functies om aangepaste metrische gegevens te maken op basis van logica in de containerhiërarchie, regels en operatoren. Met dit geïntegreerde ontwikkelprogramma kunt u eenvoudige of complexe berekende meetgegevens maken en opslaan.

U kunt op de volgende manieren beginnen met het maken van een berekende metrische waarde:

* Open in Analysis Workspace een project en selecteer vervolgens **[!UICONTROL Components]** > **[!UICONTROL Create metric]**.
* Open in Analysis Workspace een project en selecteer vervolgens de **Plus** pictogram naast [!UICONTROL **Metrisch**] in de linkerspoorstaaf.
* In [!DNL Analytics], ga naar **[!UICONTROL Components]** > **[!UICONTROL Calculated metrics]** selecteert u vervolgens **[!UICONTROL + Add]** boven aan de pagina Berekende metriek.

![](assets/cm_builder_ui.png)

## Beschikbare velden en gebieden {#section_9382AEEBA4244DD6A9F6C1DD3F6D076B}

<table id="table_60A82936321047D1A335331BF83B0972"> 
 <thead> 
  <tr> 
   <th colname="col2" class="entry"> Veld </th> 
   <th colname="col3" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Titel </span> </td> 
   <td colname="col3"> <p>De naam van de metrische waarde is verplicht. U kunt metrisch opslaan tenzij het wordt genoemd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Beschrijving </span> </td> 
   <td colname="col3"> <p>Geef het een gebruikersvriendelijke beschrijving om te tonen waarvoor het wordt gebruikt en het van gelijkaardige degenen te onderscheiden. </p> <p>De beschrijving wordt ook weergegeven in een rapport. Het is beter NIET om de formule in de beschrijving te zetten - in plaats daarvan, beschrijf wat deze metrisch zou moeten en niet zouden moeten worden gebruikt. (De formule wordt geproduceerd aangezien u metrisch bouwt, onder de Summiere rubriek. Dientengevolge, is het niet nodig om de formule aan de beschrijving toe te voegen.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Indeling </span> </td> 
   <td colname="col3"> <p>U kunt kiezen uit Decimaal, Tijd, Percentage en Valuta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Decimalen </span> </td> 
   <td colname="col3"> <p>Toont hoeveel decimalen in het rapport zullen worden getoond. Het maximumaantal decimalen dat u kunt opgeven, is 10. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Naar boven trends tonen als... </span> </td> 
   <td colname="col3"> <p>Deze metrische polariteit die toont of de Analyse een stijgende trend in metrisch als goed (groen) of slecht (rood) zou moeten beschouwen. Als gevolg hiervan zal de grafiek van het rapport als groen of rood worden weergegeven wanneer het omhoog gaat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Tags </span> </td> 
   <td colname="col3"> <p>Tags zijn een goede manier om metriek in te delen. Alle gebruikers kunnen tags maken en een of meer tags toepassen op een metrische waarde. U kunt echter alleen labels zien voor de segmenten die u bezit of die met u zijn gedeeld. Welke soorten markeringen moet u creëren? Hier volgen enkele suggesties voor handige tags: 
     <ul id="ul_9A6CE5F179424687A39F2D5C1A953258"> 
      <li id="li_A8815F2D8D284874AD701A7B103D82A3">Tags gebaseerd op <b>teamnamen</b>, zoals Sociale marketing, Mobiele marketing. </li> 
      <li id="li_A51A4515A541488E9D90296A955E9F4F"><b>Project</b> tags (analysetags), zoals analyse van de pagina Invoer. </li> 
      <li id="li_B4605470A7094026AC168420B64BBCC3"><b>Categorie</b> tags: Mannen; geografie. </li> 
      <li id="li_B6EAB0F2A96C41209C4EC97B9E64390B"><b>Workflow</b> tags: goed te keuren; Gecurreerd voor (een specifieke bedrijfseenheid) </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Samenvatting </span> </td> 
   <td colname="col3"> <p>De <span class="uicontrol"> Samenvatting </span> de formule werkt op om het even welk ogenblik bij u een verandering in de metrische definitie aanbrengt. Deze formule wordt ook weergegeven in de metrische rail links als u de muisaanwijzer boven een metrische waarde houdt en op de knop <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Info_18_N.svg" id="image_BDA0EAF89C19440CB02AE248BA3F968E" /> pictogram. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Definitie </span> </td> 
   <td colname="col3"> <p>Dit is waar u in metriek/berekende metriek, segmenten, en/of functies sleept om berekende metrisch te bouwen. </p> <p> 
     <ul id="ul_B13401A266354DC594C6176025DB61CB"> 
      <li id="li_01776C32C7C5440AA1F847096CBED92B">Als u in berekende metrisch sleept, zal het zijn metrische definitie automatisch uitbreiden. </li> 
      <li id="li_A483D352522E4572AB43042473053359">U kunt definities nesten met containers. In tegenstelling tot gesegmenteerde containers, functioneren deze containers als een wiskundige uitdrukking en bepalen de orde van verrichtingen. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Operator </span> </td> 
   <td colname="col3"> <p>Gedeeld door ( <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Divide_18_N.svg" width="15" id="image_320D7363DE024BDEB21E44606C8B367F" width="25px" /> ) is de standaardoperator, plus de operatoren +, - en x. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Voorvertoning </span> </td> 
   <td colname="col3"> <p>Hiermee kunt u snel informatie lezen over mogelijke fouten. De voorvertoning beslaat de laatste 90 dagen. Dit is een manier om aanvankelijk te graven of u de juiste componenten voor uw metrisch hebt geselecteerd. Een onverwacht resultaat zou betekenen u een tweede blik bij de metrische definitie moet nemen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Productcompatibiliteit </span> </td> 
   <td colname="col3"> <p>De verenigbaarheid van het product toont u of metrisch compatibel is met <a href="https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/current-data.html"  > Huidige gegevens </a>, met volledig verwerkte gegevens of alleen met marketingrapporten (first-touch-toewijzing). <p>Opmerking: De huidige Gegevens steunen niet alle metriek. Metriek die segmenten of functies bevatten, is niet compatibel met de huidige gegevens. <a href="/help/components/c-calcmetrics/cm-compatibility.md"  > Meer... </a> </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Toevoegen </span> </td> 
   <td colname="col3"> <p>Voor alle soorten berekende metriek, kunt u containers en statische aantallen aan de definitie toevoegen. Voor geavanceerde berekende metriek, kunt u segmenten en functies ook toevoegen. </p> <p> 
     <ul id="ul_607C1B303F334062BC620317667DE490"> 
      <li id="li_53462789B8AF4F1AA9B45565D37CF22B">Containers werken als een wiskundige expressie en bepalen de volgorde van bewerkingen. Dus alles in een container wordt verwerkt voor de volgende bewerking. </li> 
      <li id="li_401A9E0D8B3B468990289DBF66A06F63">Als u een segment naar een container sleept, wordt alles in die container gesegmenteerd. (Alleen geavanceerde berekende cijfers) </li> 
      <li id="li_F191B200D7A944F9ADC0573A9A82A6DA">U kunt meerdere segmenten in een container stapelen. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> Pictogram vistuig ( <span class="uicontrol"> Metrisch type </span>, <span class="uicontrol"> Attributie </span>) </td> 
   <td colname="col3"> <p>Als u het tandwielpictogram naast een metrische waarde selecteert, kunt u de instelling <a href="/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md"  > Metrische type- en attributiemodellen </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> + Nieuw </span> </td> 
   <td colname="col3"> <p>Hiermee kunt u een nieuwe component maken, zoals een nieuw segment (dat u naar het <a href="/help/components/segmentation/segmentation-workflow/seg-build.md"  > Segment Builder </a>.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Componenten zoeken </p> </td> 
   <td colname="col3"> <p>Met deze zoekbalk kunt u zoeken naar afmetingen, metriek, segmenten (alleen geavanceerde berekende meetgegevens) en functies (alleen geavanceerde berekende meetgegevens). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Lijst van Dimension </p> </td> 
   <td colname="col3"> <p>In plaats van de Berekende Metrische Bouwer te verlaten om een eenvoudig segment (in de Bouwer van het Segment) te bouwen, b.v. "Pagina = Homepage", kunt u in Pagina slepen en Homepage van Berekende Metrische Bouwer direct selecteren. </p> <p>Dit resulteert in een veel gestroomlijnder werkschema voor het creëren van gesegmenteerde berekende metriek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Lijst met meetwaarden </p> </td> 
   <td colname="col3"> <p>De cijfers zijn ingedeeld in drie categorieën: </p> 
    <ul id="ul_7BF50F4964EF45858FBA1634FBFA45CF"> 
     <li id="li_90F2312927A6499CA1CE04F8FFC912CF">Standaardwaarden ( <img placement="inline"  src="assets/met_icon.png" id="image_65A80F54D73443E78542FE0B31CC3F20" />) </li> 
     <li id="li_A3F59083E79B4AC780D6F8CEDFFD20C9">Berekende standaarden ( <img placement="inline"  src="assets/calc_met_icon.png" id="image_C5674AB9B9EB4DA9A56782D15822C319" />) </li> 
     <li id="li_8735E76637ED4C3F983731A66E04C93E">Metrische sjablonen ( <img placement="inline"  src="assets/cm_template_icon.png" width="25px" id="image_D236601511CC4DD3828F223431E27E88" />) - onder aan de lijst. </li> 
    </ul> <p>Wanneer u de muisaanwijzer boven een metrische waarde houdt, ziet u het pictogram Info rechts ervan: <img placement="inline"  src="assets/info.png" width="150px" id="image_5A65E772A68A4B94ACAD6552CCF21F5F" />. Als u op dit pictogram klikt, krijgt u de volgende informatie: </p> 
    <ul id="ul_DF35DDB9FBFA40C8A93FA0F2286A0BBE"> 
     <li id="li_4215AA9BF93F4C8B941002A7A4D2F50B">De formule van hoe het wordt berekend. </li> 
     <li id="li_6A8E39EB6DCE4377B0B594B6D4FC0294">Een voorproeftrend van metrisch. </li> 
     <li id="li_44C1595E4BE64ED69D1DB3BB6655ED55">Een bewerkingspictogram (potlood) rechtsboven dat u naar de Calculated Metrics Builder brengt waar u deze berekende metrische waarde kunt bewerken. </li> 
    </ul> <p><img placement="break" align="center"  src="assets/info2.png" width="200px" id="image_7D5B2F026A034118BE4DA81B9215A883" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Lijst met segmenten </p> </td> 
   <td colname="col3"> <p>(Alleen Geavanceerde berekende metriek) Als beheerder worden in deze lijst alle segmenten weergegeven die in uw aanmeldingsbedrijf zijn gemaakt. Als u een gebruiker niet-Admin bent, toont deze lijst segmenten u bezit en die met u worden gedeeld. <a href="https://experienceleague.adobe.com/docs/analytics/components/segmentation/segment-reference/seg-rights.html"  > Meer... </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Lijst met functies </p> </td> 
   <td colname="col3"> <p>(Alleen geavanceerde berekende metriek) Functies worden in twee lijsten onderverdeeld: <a href="/help/components/c-calcmetrics/cm-reference/cm-functions.md"  > Basis </a> (meest gebruikt) en <a href="/help/components/c-calcmetrics/cm-reference/cm-adv-functions.md"  > Geavanceerd </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Selector rapportsuite </p> </td> 
   <td colname="col3"> <p>Hiermee kunt u overschakelen op een andere rapportsuite. </p> </td> 
  </tr> 
 </tbody> 
</table>
