---
description: U kunt koppelingen onderscheiden door de koppelings-id aan te passen met behulp van de variabele s_objectID, door het gebied aan te passen en door het modulebestand AppMeasurement ActivityMap aan te passen.
title: Verschillende koppelingen die verwijzen naar dezelfde koppelings-id en -regio
topic: Activity map
uuid: f2da0cda-a33b-4a12-8d99-1f58386d6d30
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Verschillende koppelingen die verwijzen naar dezelfde koppelings-id en -regio

U kunt koppelingen onderscheiden door de koppelings-id aan te passen met behulp van de variabele s_objectID, door het gebied aan te passen en door het modulebestand AppMeasurement ActivityMap aan te passen.

Als voorbeeld, laten wij zeggen u veelvoudige &quot;Kopen&quot;verbindingen hebt die door de Kaart van de Activiteit onder zelfde identiteitskaart van de Verbinding en Gebied worden geïdentificeerd:

<table id="table_3020E2C0175D455C84E794CF51BE5A93"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Codevoorbeeld </th> 
   <th colname="col2" class="entry"> Koppelings-id </th> 
   <th colname="col3" class="entry"> Regio </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <code>
      &lt;div&nbsp;id="recommendation&nbsp;panel"&gt; 
     &nbsp;&nbsp;&lt;div&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;href="product1.html"&gt;Buy&lt;/a&gt; 
     &nbsp;&nbsp;&nbsp;&lt;/div&gt; 
     &nbsp;&nbsp;&lt;div&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;href="product2.html"&gt;Buy&lt;/a&gt; 
     &nbsp;&nbsp;&nbsp;&lt;/div&gt; 
     &nbsp;&lt;div&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;href="product3.html"&gt;Buy&lt;/a&gt; 
     &nbsp;&nbsp;&nbsp;&lt;/div&gt; 
    </code> </td> 
   <td colname="col2"> <p> </p> <p> </p> <p> </p> <p> </p>Kopen <p> </p> <p> </p> <p>Kopen </p> <p> </p> <p> </p> <p>Kopen </p> </td> 
   <td colname="col3"> <p> </p> <p> </p> <p> </p> <p> </p>aanbevelingsvenster <p> </p> <p> </p> <p>aanbevelingsvenster </p> <p> </p> <p> </p> <p>aanbevelingsvenster </p> </td> 
  </tr> 
 </tbody> 
</table>

Hoe kunt u de webpagina en de codering aanpassen om de waarden van deze koppelingen te onderscheiden? U hebt drie opties: U kunt de identiteitskaart van de Verbinding aanpassen, of het gebied aanpassen, of het dossier van de Module AppMeasurement ActivityMap aanpassen.

## Koppelings-id aanpassen met s_objectID {#section_01B0D463397B4837B2D46F087A6E5937}

Door een unieke object-id te maken voor een koppeling of koppelingslocatie op een pagina, kunt u de activiteitstoewijzing verbeteren of Activiteitenkaart gebruiken om te rapporteren over een koppelingstype of -locatie, in plaats van de koppelings-URL. Klik [hier](https://marketing.adobe.com/resources/help/en_US/sc/implement/s_objectID.html) voor meer informatie over de variabele s_objectID.

>[!IMPORTANT]
>
>Merk op dat een volgpuntkomma (;) wordt vereist wanneer het gebruiken van s_objectID in de Kaart van de Activiteit.

<table id="table_9439A5F320304E439A19842CF3EBA456"> 
 <thead> 
  <tr> 
   <th colname="col02" class="entry"> Codevoorbeeld </th> 
   <th colname="col2" class="entry"> Koppelings-id </th> 
   <th colname="col3" class="entry"> Regio </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col02"> 
    <code>
      &lt;div&nbsp;id="recommendation&nbsp;panel"&gt; 
     &nbsp;&nbsp;&lt;div&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;onClick="s_objectID='Product1';"&nbsp;href="product1.html"&gt;Buy&lt;/a&gt; 
     &nbsp;&nbsp;&nbsp;&lt;/div&gt; 
     &nbsp;&nbsp;&lt;div&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;onClick="s_objectID='Product2';"&nbsp;href="product2.html"&gt;Buy&lt;/a&gt; 
     &nbsp;&nbsp;&nbsp;&lt;/div&gt; 
     &nbsp;&lt;div&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;onClick="s_objectID='Product3';"&nbsp;href="product3.html"&gt;Buy&lt;/a&gt; 
     &nbsp;&nbsp;&nbsp;&lt;/div&gt;&nbsp;&nbsp;&nbsp; 
    </code> </td> 
   <td colname="col2"> <p> </p> <p> </p> <p> </p>Product1 <p> </p> <p> </p> <p>Product 2 </p> <p> </p> <p> </p> <p>Product 3 </p> <p> </p> </td> 
   <td colname="col3"> <p> </p> <p> </p> <p> </p> <p>aanbevelingen, deelvenster </p> <p> </p> <p> </p> <p>aanbevelingen, deelvenster </p> <p> </p> <p> </p> <p>aanbevelingen, deelvenster </p> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Het gebied aanpassen {#section_6B1EF302573B445DBAF44176D0A12DB9}

U kunt de regio aanpassen door ervoor te zorgen dat voor elke &quot;koop&quot;verbinding een eigen Gebied wordt bepaald. Hiervoor voegt u een parameter &quot;id&quot; toe aan een van de bovenliggende elementen van elke ankertag &quot;Buy&quot;.

>[!NOTE] U bent niet strikt beperkt tot de parameter &quot;id&quot; als regio-id. U kunt ook uw eigen id instellen met de JavaScript-variabele &quot;s.ActivityMap.regionIDAattribute&quot;.

<table id="table_250DB52A869C466B942517BABA1C287B"> 
 <thead> 
  <tr> 
   <th colname="col02" class="entry"> Codevoorbeeld </th> 
   <th colname="col2" class="entry"> Koppelings-id </th> 
   <th colname="col3" class="entry"> Regio </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col02"> 
    <code>
      &lt;div&nbsp;id="recommendation&nbsp;panel"&gt; 
     &nbsp;&nbsp;&lt;div&nbsp;id="region&nbsp;a"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;href="product1.html"&gt;Buy&lt;/a&gt; 
     &nbsp;&nbsp;&nbsp;&lt;/div&gt; 
     &nbsp;&nbsp;&lt;div&nbsp;id="region&nbsp;b"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;href="product2.html"&gt;Buy&lt;/a&gt; 
     &nbsp;&nbsp;&nbsp;&lt;/div&gt; 
     &nbsp;&lt;div&nbsp;id="region&nbsp;c"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;href="product3.html"&gt;Buy&lt;/a&gt; 
     &nbsp;&nbsp;&nbsp;&lt;/div&gt; 
    </code> </td> 
   <td colname="col2"> <p> </p> <p> </p> <p> </p> <p>Kopen </p> <p> </p> <p> </p> <p>Kopen </p> <p> </p> <p> </p> <p>Kopen </p> </td> 
   <td colname="col3"> <p> </p> <p> </p> <p> </p>regio a <p> </p> <p> </p> <p>regio b </p> <p> </p> <p> </p> <p>regio c </p> </td> 
  </tr> 
 </tbody> 
</table>

## Het bestand ActivityMap voor AppMeasurement-module aanpassen {#section_B933BB9F944E4D5389002908A5A881F8}

>[!CAUTION]
>
>Controleer of de gewijzigde code goed werkt. Adobe is niet verantwoordelijk voor het gedrag van de gewijzigde code.

Hier zijn een paar voorbeelden van** generische verbinding** verbinding/gebiedfuncties u (in gewijzigde vorm) in uw AppMeasurement.js- dossier kon omvatten.

```
s.ActivityMap.link = function(ele,linkName){ 
if(linkName){ 
return linkName; 
} 
if(ele){ 
if(ele.tagName == 'A' && ele.href){ 
return ele.href; 
} 
} 
} 
```

LinkName wordt overgegaan tijdens vraag aan s.tl.

```
s.ActivityMap.region = function(ele){ 
var className, 
classNames = { 
'header': 1, 
'navbar': 1, 
'left-content': 1, 
'main-content': 1, 
'footer': 1, 
}; 
  while( (ele && (ele = ele.parentNode))){ 
if( (className=ele.className) && classNames[className]){ 
return className; 
} 
} 
return "BODY"; 
} 
```

