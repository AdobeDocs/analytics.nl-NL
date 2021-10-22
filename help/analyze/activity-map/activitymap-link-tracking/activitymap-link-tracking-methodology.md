---
description: Deze sectie is bedoeld voor Adobe Analytics-beheerders. Het concentreert zich op de nieuwe verbindingen het volgen parameters en hoe zij verbindingsuniciteit en consistentie over browsers en apparaten verzekeren, en de behandeling van verbinding het verplaatsen op een pagina verbeteren.
title: Methode voor link tracking
uuid: 67864bf9-33cd-46fa-89a8-4d83d3b81152
feature: Activity Map
role: User, Admin
exl-id: 6aef3a0f-d0dd-4c84-ad44-07b286edbe18
source-git-commit: a6b38c6e7a34c876524ebe15514ac205898549d0
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Methode voor link tracking

Deze sectie is bedoeld voor Adobe Analytics-beheerders. Het concentreert zich op de nieuwe verbindingen het volgen parameters en hoe zij verbindingsuniciteit en consistentie over browsers en apparaten verzekeren, en de behandeling van verbinding het verplaatsen op een pagina verbeteren.

>[!IMPORTANT]
>
>Elke koppeling waarin de tekst (niet de href) PII (Persoonlijk Identificeerbare Informatie) kan bevatten, moet expliciet worden geïmplementeerd met behulp van [s_objectID](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/page-variables.html) of door ActivityMap-linkverzameling uit te sluiten met [s.ActivityMap.linkExclusions of s.ActivityMap.regionExclusions](/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-methodology.md#configuration-vars). Ga voor meer informatie over hoe Activity Map PII-gegevens kan verzamelen naar [hier](/help/analyze/activity-map/lnk-tracking-overview.md).

De Activity Map baseert zijn verbinding het volgen op deze twee IDs:

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
* Het verbetert leesbaarheid, zodat kunnen de gebruikers beginnen de het volgen van de Verbinding rapporten buiten Activity Map te analyseren.

## Koppelingsgebied {#section_75BF9B9E3CE94B59ACC3D9AF63E04535}

Met dit nieuwe kenmerk kunnen gebruikers een tekenreeks opgeven die representatief is voor het paginagebied waar de koppeling zich bevindt.

Voor bijvoorbeeld een koppeling &quot;Contact opnemen&quot; in de menusectie van de webpagina wil de gebruiker wellicht een parameter voor het gebied &quot;Menu&quot; doorgeven. Op dezelfde manier kan voor een koppeling &quot;Contact opnemen&quot; in de voettekst van de webpagina de parameter region worden ingesteld op &quot;footer&quot;.

De waarde van het Gebied van de Verbinding wordt niet geplaatst op de verbinding zelf, maar op één element van HTML omhoog de HTML boom DOM die dat gebied omvat.
Het gebruik van het koppelingsgebied heeft de volgende voordelen:

* Het helpt verbindingen met zelfde primaire identiteitskaart onderscheiden.
* De trend in een gebied wordt minder beïnvloed door het dynamische aspect van de webpagina.
* Gebruikers kunnen de bovenste koppelingen in een gebied zien. Met Gebied als anker, kunnen wij bekledingen van verbindingen tonen die momenteel niet op de pagina (Ajax, het richten) zichtbaar zijn.
* Een gebied kan pagina&#39;s vervangen omdat een bepaald gebied op veel webpagina&#39;s kan worden gebruikt. Het helpt vragen zoals te beantwoorden: &quot;Past mijn &quot;Product Offering&quot;gebied het best op de Vrouwen Landing Pagina of de Landing van Mannen?
* Regio is op zich een relevante dimensie voor het analyseren van zeer dynamische webpagina&#39;s. De reden hiervoor is dat de ruis wordt verwijderd als koppelingen voortdurend worden gewijzigd: een regio &quot;Nieuwst&quot; in de CNN-landingspagina kan een heleboel veranderende koppelingen hebben. Maar de regio zal er altijd zijn. Het zou dus interessant kunnen zijn om de trend op het niveau van de regio gedurende vele dagen te volgen.

**Aangepast gebied bijhouden**

U kunt de parameter Regio voor een koppeling aanpassen (standaard is koppeling-id): Een tag die is ingesteld op &#39;ID&#39; gebruikt alle HTML-elementen met de parameter &#39;id&#39; als een regio. Als u de tag Regio instelt op &quot;id&quot;, worden zeer waarschijnlijk veel afzonderlijke gebieden geretourneerd (zo veel als er verschillende &quot;id&#39;s&quot; op de pagina staan). Als u een meer aangepaste implementatie wilt, kunt u de tag region ook instellen op iets specifiekers, zoals &quot;region_id&quot;.

Hieronder kunt u een voorbeeld van HTML weergeven met het kenmerk &#39;id&#39; van het standaardgebied.

```
<div id="content">
  <div id="breaking_news">
    <a href="breaking-news.html">...</a>
  </div>
  <div id="todays_top_headlines">
    <a href="breaking-news.html">...</a>
  </div>
```

Desgewenst kunt u elementen labelen met een willekeurige tekenreeks-id, in dit geval &quot;lpos&quot;, en vervolgens kenmerken toevoegen met de naam &quot;lpos&quot;.

```
<script language="JavaScript" type="text/javascript">
s.ActivityMap.regionIDAttribute = "lpos";
</script>
<div id="nav" lpos="navbar">
  <ul>
    <li>Menu Category A
      <ul>
        <li><a href="">Menu Item A 1</a>
        <li><a href="">Menu Item A 2</a>
      </ul>
    </li>
    <li>Menu Category B
      <ul>
        <li><a href="">Menu Item B 1</a>
        <li><a href="">Menu Item B 2</a>
      </ul>
    </li>
  </ul>
</div> 
  
<div id="content">
  <div id="breaking_news" lpos="breaking_news>
    <a href="breaking-news.html">...</a>
  </div>
  <div id="todays_top_headlines">
    <a href="breaking-news.html">...</a>
  </div>
```

## Configuratievariabelen {#configuration-vars}

Deze variabelen worden alleen ter referentie vermeld. De Activity Map zou behoorlijk uit de doos moeten worden gevormd, maar u kunt uw implementatie aanpassen gebruikend deze variabelen.

### `s.ActivityMap.regionIDAttribute`

Tekenreeks die het tagkenmerk identificeert dat moet worden gebruikt als regio-id van een bovenliggend (bovenliggend, bovenliggend, ...)-element van `s.linkObject`, d.w.z. **het element waarop is geklikt**.

**Voorbeeld**

Wordt standaard ingesteld op de parameter &quot;id&quot;. U kunt dit instellen op een andere parameter.

### `s.ActivityMap.link`

Functie die de geklikte `HTMLElement` en moet een tekenreekswaarde retourneren die staat voor de koppeling waarop is geklikt. Wanneer de geretourneerde waarde false is (null, undefined, empty string, 0), wordt geen koppeling bijgehouden.

**Voorbeeld**

```
// only ever use "title" attributes from A tags
function(clickedElement) {
  var linkId;
  if (clickedElement && clickedElement.tagName.toUpperCase() === 'A') {
    linkId = clickedElement.getAttribute('title');
  }
  return linkId;
}
```

### `s.ActivityMap.region`

Functie die het aangeklikte HTMLElement ontvangt en een koordwaarde moet terugkeren die vertegenwoordigt **het gebied waar de verbinding werd gevonden toen klikte.** Wanneer de geretourneerde waarde false is (null, undefined, empty string, 0), wordt geen koppeling bijgehouden.

**Voorbeeld**

```
// only ever use lowercase version of tag name concatenated with first className as the region
function(clickedElement) {
  var regionId, className;
  while (clickedElement && (clickedElement = clickedElement.parentNode)) {
    regionId = clickedElement.tagName;
    if (regionId) {
      return regionId.toLowerCase();
    }
  }
}
```

### `s.ActivityMap.linkExclusions`

Tekenreeks die een door komma&#39;s gescheiden lijst met tekenreeksen ontvangt waarnaar moet worden gezocht in koppelingstekst. Indien gevonden, wordt de koppeling uitgesloten van Activity Map. Als deze niet is ingesteld, wordt niet geprobeerd de koppeling niet meer te volgen op Activity Map.

**Voorbeeld**

```
// Exclude links tagged with a special linkExcluded CSS class
<style>
.linkExcluded {
  display: block;
  height: 1px;
  left: -9999px;
  overflow: hidden;
  position: absolute;
  width: 1px;
}
</style>
<a href="next-page.html">
  Link is tracked because link does not have hidden text matching the filter. 
</a>
<a href="next-page.html">
  Link not tracked because s.ActivityMap.linkExclusions is set and this link has hidden text matching the filter.
  <span class="linkExcluded">exclude-link1</span>
</a>
<a href="next-page.html">
  Link not tracked because s.ActivityMap.linkExclusions is set and this link has hidden text matching the filter.
  <span class="linkExcluded">exclude-link2</span>
</a>
<script>
  var s = s_gi('samplersid');
  s.ActivityMap.linkExclusions = 'exclude-link1,exclude-link2';
</script>
```

### `s.ActivityMap.regionExclusions`

Tekenreeks die een door komma&#39;s gescheiden lijst met tekenreeksen ontvangt waarnaar in regiotekst moet worden gezocht. Indien gevonden, wordt de koppeling uitgesloten van Activity Map. Als deze niet is ingesteld, wordt niet geprobeerd de koppeling niet meer te volgen op Activity Map.

**Voorbeeld**

```
// Exclude regions on the page from its links being trackable by ActivityMap
<div id="links-included">
  <a href="next-page.html">
    Link is tracked because s.ActivityMap.regionExclusions is set but does not match the filter.
  </a>
</div>
<div id="links-excluded"> 
  <a href="next-page.html">
    Link not tracked because s.ActivityMap.regionExclusions is set and this link matches the filter.
  </a>
</div>
<script>
  var s = s_gi('samplersid');
  s.ActivityMap.regionExclusions = 'links-excluded';
</script>
```
