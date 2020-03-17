---
description: Deze sectie is bedoeld voor Adobe Analytics-beheerders. Het concentreert zich op de nieuwe verbindingen het volgen parameters en hoe zij verbindingsuniciteit en consistentie over browsers en apparaten verzekeren, en de behandeling van verbinding het verplaatsen op een pagina verbeteren.
title: Methode voor het bijhouden van koppelingen
topic: Activity map
uuid: 67864bf9-33cd-46fa-89a8-4d83d3b81152
translation-type: tm+mt
source-git-commit: ''

---


# Methode voor het bijhouden van koppelingen

Deze sectie is bedoeld voor Adobe Analytics-beheerders. Het concentreert zich op de nieuwe verbindingen het volgen parameters en hoe zij verbindingsuniciteit en consistentie over browsers en apparaten verzekeren, en de behandeling van verbinding het verplaatsen op een pagina verbeteren.

>[!IMPORTANT]
>
>Elke koppeling waarbij de tekst (niet de href) PII (Persoonlijk Identificeerbare informatie) kan bevatten, moet expliciet worden geïmplementeerd met [s_objectID](https://marketing.adobe.com/resources/help/en_US/sc/implement/s_objectID.html) of door de ActivityMap-linkverzameling met [s.ActivityMap.linkExclusions of s.ActivityMap.regionExclusions](/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-methodology.md#configuration-vars)uit te sluiten. Voor meer informatie over hoe de Kaart van de Activiteit PII gegevens kan verzamelen, ga [hier](/help/analyze/activity-map/lnk-tracking-overview.md).

De kaart van de activiteit baseert zijn verbinding het volgen op deze twee IDs:

* Primaire id: dit is de herkenbare parameter van de koppeling .
* Koppelingsgebied: dit is een secundaire parameter die gebruikers toestaat om een koord te specificeren dat van het algemene verbindingsgebied in de pagina of het gebied representatief is. Deze parameter kan automatisch worden gegenereerd als deze niet door de gebruiker wordt opgegeven.

## Primaire id {#section_E8705CC1BDBC47FB8A4FE02293BACFE6}

Als de HTML een s_objectid heeft, dan wordt primaire identiteitskaart in gebreke gesteld aan s_objectid. Anders worden de volgende parameters gebruikt als primaire id (in deze volgorde van prioriteit):

* Intertext
* Alttext
* Titel
* Bron
* Handeling

## InnerText gebruiken in plaats van Koppeling (URL) {#section_70C3573E22274522A8CC035BF18EC468}

Koppelingsactie is de actie die door de webpagina wordt uitgevoerd wanneer op de koppeling wordt geklikt. Dit is doorgaans de URL die wordt bezocht nadat op de koppeling is geklikt. Enkele kwesties u zou kunnen lopen wanneer het gebruiken van de Actie van de Verbinding zijn:

* met twee of meer verschillende koppelingen met dezelfde id
* leesbaarheid van de koppeling
* één koppeling met meerdere handelingen (afhankelijk van het apparaat waar u de koppeling weergeeft)

Dientengevolge, gebruiken wij InnerText met deze voordelen over het gebruiken van Actie van de Verbinding (URL):

* Het is een goede vertegenwoordiging van de identiteit van de Verbinding. Het dupliceren van primaire id&#39;s wordt aanzienlijk gereduceerd, omdat het niet gebruikelijk is om meerdere koppelingen met dezelfde tekst te hebben.
* Het zorgt voor consistentie van de primaire id op verschillende apparaten en browsertypen.
* De positie van een koppeling op de pagina wordt niet gewijzigd.
* Het verbetert leesbaarheid, zodat kunnen de gebruikers beginnen de het volgen van de Verbinding rapporten buiten de Kaart van de Activiteit te analyseren.

## Koppelingsgebied {#section_75BF9B9E3CE94B59ACC3D9AF63E04535}

Met dit nieuwe kenmerk kunnen gebruikers een tekenreeks opgeven die representatief is voor het paginagebied waar de koppeling zich bevindt.

Voor bijvoorbeeld een koppeling &quot;Contact opnemen&quot; in de menusectie van de webpagina wil de gebruiker wellicht een parameter voor het gebied &quot;Menu&quot; doorgeven. Op dezelfde manier kan voor een koppeling &quot;Contact opnemen&quot; in de voettekst van de webpagina de parameter region worden ingesteld op &quot;footer&quot;.

De waarde van het Gebied van de Verbinding wordt niet geplaatst op de verbinding zelf, maar op één element van HTML omhoog de boom van DOM HTML die dat gebied omvat.
Het gebruik van het koppelingsgebied heeft de volgende voordelen:

* Het helpt verbindingen met zelfde primaire identiteitskaart onderscheiden.
* De trend in een gebied wordt minder beïnvloed door het dynamische aspect van de webpagina.
* Gebruikers kunnen de bovenste koppelingen in een gebied zien. Met Gebied als anker, kunnen wij bekledingen van verbindingen tonen die momenteel niet op de pagina (Ajax, het richten) zichtbaar zijn.
* Een gebied kan pagina&#39;s vervangen omdat een bepaald gebied op veel webpagina&#39;s kan worden gebruikt. Het helpt vragen zoals te beantwoorden: &quot;Past mijn &quot;Product Offering&quot;gebied het best op de Vrouwen Landing Pagina of de Landing van Mannen?
* Regio is op zich een relevante dimensie voor het analyseren van zeer dynamische webpagina&#39;s. De reden hiervoor is dat de ruis wordt verwijderd als koppelingen voortdurend worden gewijzigd: een regio &quot;Nieuwst&quot; in de CNN-landingspagina kan een heleboel veranderende koppelingen hebben. Maar de regio zal er altijd zijn. Het zou dus interessant kunnen zijn om de trend op het niveau van de regio gedurende vele dagen te volgen.

**Aangepast gebied bijhouden**

U kunt de parameter Regio voor een koppeling aanpassen (standaard is koppeling-id): Een tag die is ingesteld op &#39;ID&#39; gebruikt alle HTML-elementen met de parameter &#39;id&#39; als een regio. Als u de tag Regio instelt op &quot;id&quot;, worden zeer waarschijnlijk veel afzonderlijke gebieden geretourneerd (zo veel als er verschillende &quot;id&#39;s&quot; op de pagina staan). Als u een meer aangepaste implementatie wilt, kunt u de tag region ook instellen op iets specifiekers, zoals &quot;region_id&quot;.

Hieronder kunt u HTML-voorbeelden weergeven met het kenmerk &#39;id&#39; van het standaardgebied.

```
<div id="content"> 
  <div id="breaking_news"> 
      <a href="breaking-news.html">...</a> 
   </div> 
 <div id="todays_top_headlines"> 
      <a href="breaking-news.html">...</a> 
   </div> 
```

Desgewenst kunt u elementen labelen met een willekeurige tekenreeks-id, in dit geval &#39;&#39;lpos&#39;&#39;, en vervolgens kenmerken toevoegen met de naam &#39;&#39;lpos&#39;&#39;.

```
<script language="JavaScript" type="text/javascript">
s.ActivityMap.regionIDAttribute="lpos";
</script> 
   
<div id="nav" lpos="navbar"> 
  <ul> 
     <li> Menu Category A 
    <ul> 
      <li><a href="">Menu Item A 1</a> 
      <li><a href="">Menu Item A 2</a> 
     </ul> 
    </li> 
     <li> Menu Category B 
     <ul> 
      <li><a href="">Menu Item B 1</a>  
      <li><a href="">Menu Item B 2</a> 
  
   </ul> 
</ul> 
</div> 
  
<div id="content" > 
  <div id="breaking_news" lpos="breaking_news> 
      <a href="breaking-news.html">...</a> 
   </div> 
 <div id="todays_top_headlines"> 
      <a href="breaking-news.html">...</a> 
   </div> 
</div>
```

## Configuratievariabelen {#configuration-vars}

Deze variabelen worden alleen ter referentie vermeld. De Kaart van de activiteit zou behoorlijk uit de doos moeten worden gevormd, maar u kunt uw implementatie aanpassen gebruikend deze variabelen.

<table id="table_7BC8DC3F35CF49288D94BA707F06B283"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Naam variabele </th> 
   <th colname="col2" class="entry"> Voorbeeld </th> 
   <th colname="col3" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> s.ActivityMap.regionIDAtribute </td> 
   <td colname="col2"> Wordt standaard ingesteld op de parameter "id". U kunt dit instellen op een andere parameter. </td> 
   <td colname="col3"> Tekenreeks die het tagkenmerk identificeert dat moet worden gebruikt als regio-id van een bovenliggend element (parent, parent.parent, ...) van s.linkObject, dat wil zeggen <b>het element waarop is geklikt</b>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> s.ActivityMap.link </td> 
   <td colname="col2"> 
    <code>
      //&nbsp;only&nbsp;ever&nbsp;use&nbsp;"title"&nbsp;attributes&nbsp;from&nbsp;A&nbsp;tags function(clickedElement){ &nbsp;&nbsp;&nbsp;var&nbsp;linkId; &nbsp;&nbsp;&nbsp;if(clickedElement&nbsp;&amp;&amp;&nbsp;clickedElement.tagName.toUpperCase()&nbsp;===&nbsp;'A'){ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;linkId&nbsp;=&nbsp;clickedElement.getAttribute('title'); &nbsp;&nbsp;&nbsp;} &nbsp;&nbsp;&nbsp;return&nbsp;linkId; } 
    </code> </td> 
   <td colname="col3"> Functie die het aangeklikte HTMLElement ontvangt en een koordwaarde zou moeten terugkeren die <b>de verbinding vertegenwoordigt die werd geklikt</b>. <p>Wanneer de geretourneerde waarde false is (null, undefined, empty string, 0), wordt geen koppeling bijgehouden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> s.ActivityMap.region </td> 
   <td colname="col2"> 
    <code>
      //&nbsp;only&nbsp;ever&nbsp;use&nbsp;lowercase&nbsp;version&nbsp;of&nbsp;tag&nbsp;name&nbsp;concatenated&nbsp;with&nbsp;first&nbsp;className&nbsp;as&nbsp;the&nbsp;region function(clickedElement){ &nbsp;&nbsp;&nbsp;var&nbsp;regionId,className; &nbsp;&nbsp;&nbsp;while(clickedElement&nbsp;&amp;&amp;&nbsp;(clickedElement=&nbsp;clickedElement.parentNode)){ &nbsp;regionId&nbsp;=&nbsp;clickedElement.tagName; &nbsp;if(regionId){ &nbsp;return&nbsp;regionId.toLowerCase(); &nbsp;} &nbsp;} } 
    </code> </td> 
   <td colname="col3"> Functie die het aangeklikte HTMLElement ontvangt en een koordwaarde zou moeten terugkeren die <b>het gebied vertegenwoordigt waar de verbinding werd gevonden toen klikte</b>. <p>Wanneer de geretourneerde waarde false is (null, undefined, empty string, 0), wordt geen koppeling bijgehouden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> s.ActivityMap.linkExclusions </td> 
   <td colname="col2"> 
    <code>
      //&nbsp;Exclude&nbsp;links&nbsp;tagged&nbsp;with&nbsp;a&nbsp;special&nbsp;linkExcluded&nbsp;CSS&nbsp;class &nbsp;&lt;style&gt; .linkExcluded{ &nbsp;&nbsp;display:&nbsp;block; &nbsp;&nbsp;height:&nbsp;1px; &nbsp;&nbsp;left:&nbsp;-9999px; &nbsp;&nbsp;overflow:&nbsp;hidden; &nbsp;&nbsp;position:&nbsp;absolute; &nbsp;&nbsp;width:&nbsp;1px; } &lt;/style&gt; &lt;a&nbsp;href="next-page.html"&gt;Link&nbsp;is&nbsp;tracked&nbsp;because&nbsp;link&nbsp;does&nbsp;not&nbsp;have&nbsp;hidden&nbsp;text&nbsp;matching&nbsp;the&nbsp;filter.&nbsp;&lt;/a&gt; &lt;a&nbsp;href="next-page.html"&gt;Link&nbsp;not&nbsp;tracked&nbsp;because&nbsp;s.ActivityMap.linkExclusions&nbsp;is&nbsp;set&nbsp;and&nbsp;this&nbsp;link&nbsp;has&nbsp;hidden&nbsp;text&nbsp;matching&nbsp;the&nbsp;filter. &nbsp;&lt;span&nbsp;class="linkExcluded"&gt;exclude-link1&lt;/span&gt; &lt;/a&gt; &lt;a&nbsp;href="next-page.html"&gt;Link&nbsp;not&nbsp;tracked&nbsp;because&nbsp;s.ActivityMap.linkExclusions&nbsp;is&nbsp;set&nbsp;and&nbsp;this&nbsp;link&nbsp;has&nbsp;hidden&nbsp;text&nbsp;matching&nbsp;the&nbsp;filter. &nbsp;&lt;span&nbsp;class="linkExcluded"&gt;exclude-link2&lt;/span&gt; &lt;/a&gt; &lt;script&gt; &nbsp;&nbsp;var&nbsp;s&nbsp;=&nbsp;s_gi('samplersid'); &nbsp;&nbsp;s.ActivityMap.linkExclusions&nbsp;=&nbsp;'exclude-link1,exclude-link2'; &lt;/script&gt; 
    </code> </td> 
   <td colname="col3"> <p>Tekenreeks die een door komma's gescheiden lijst met tekenreeksen ontvangt waarnaar moet worden gezocht in koppelingstekst. Indien gevonden, wordt de koppeling uitgesloten van het volgen door Activiteitenkaart. Als deze niet is ingesteld, wordt niet geprobeerd de koppeling niet meer te volgen op Activiteitenkaart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> s.ActivityMap.regionExclusions </td> 
   <td colname="col2"> 
    <code>
      //&nbsp;Exclude&nbsp;regions&nbsp;on&nbsp;the&nbsp;page&nbsp;from&nbsp;its&nbsp;links&nbsp;being&nbsp;trackable&nbsp;by&nbsp;ActivityMap &lt;div&nbsp;id="links-included"&gt;&nbsp; &nbsp;&nbsp;&lt;a&nbsp;href="next-page.html"&gt;Link&nbsp;is&nbsp;tracked&nbsp;because&nbsp;s.ActivityMap.regionExclusions&nbsp;is&nbsp;set&nbsp;but&nbsp;does&nbsp;not&nbsp;match&nbsp;the&nbsp;filter.&lt;/a&gt; &lt;/div&gt; &lt;div&nbsp;id="links-excluded"&gt;&nbsp; &nbsp;&nbsp;&lt;a&nbsp;href="next-page.html"&gt;Link&nbsp;not&nbsp;tracked&nbsp;because&nbsp;s.ActivityMap.regionExclusions&nbsp;is&nbsp;set&nbsp;and&nbsp;this&nbsp;link&nbsp;matches&nbsp;the&nbsp;filter.&lt;/a&gt; &lt;/div&gt; &lt;script&gt; &nbsp;&nbsp;var&nbsp;s&nbsp;=&nbsp;s_gi('samplersid'); &nbsp;&nbsp;s.ActivityMap.regionExclusions&nbsp;=&nbsp;'links-excluded'; &lt;/script&gt;
    </code> </td> 
   <td colname="col3"> <p>Tekenreeks die een door komma's gescheiden lijst met tekenreeksen ontvangt waarnaar in regiotekst moet worden gezocht. Indien gevonden, wordt de koppeling uitgesloten van het volgen door Activiteitenkaart. Als deze niet is ingesteld, wordt niet geprobeerd de koppeling niet meer te volgen op Activiteitenkaart. </p> </td> 
  </tr> 
 </tbody> 
</table>
