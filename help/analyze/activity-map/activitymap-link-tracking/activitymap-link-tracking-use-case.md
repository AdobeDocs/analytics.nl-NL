---
description: U kunt koppelingen onderscheiden door de koppelings-id aan te passen met de variabele s_objectID, door het gebied aan te passen en door het modulebestand van de module AppMeasurement ActivityMap aan te passen.
title: Koppelingen differentiëren die verwijzen naar dezelfde koppelings-id en -regio
uuid: f2da0cda-a33b-4a12-8d99-1f58386d6d30
feature: Activity Map
role: User, Admin
exl-id: 43fe4eb9-08fe-4e20-bc02-3f712c3dec1d
source-git-commit: 25eccb2b9fe3827e62b0ae98d9bebf7a97b239f5
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 5%

---

# Koppelingen differentiëren die verwijzen naar dezelfde koppelings-id en -regio

U kunt koppelingen onderscheiden door de koppelings-id aan te passen met behulp van de variabele s_objectID, door het gebied aan te passen en door het modulebestand AppMeasurement ActivityMap aan te passen.

Stel bijvoorbeeld dat u meerdere &quot;Kopen&quot;-koppelingen hebt die door Activity Map onder dezelfde koppelings-id en -regio worden geïdentificeerd:

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
    <code>&lt;div&nbsp;id="recommendation&nbsp;panel"&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;div&gt;</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;href="product1.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;div&gt;</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;href="product2.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;div&gt;</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;href="product3.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt;</code><br/>
    <code>&lt;/div&gt;</code>
   </td>
   <td colname="col2">
     <br/>
     <br/>
    Kopen<br/>
     <br/>
     <br/>
    Kopen<br/>
     <br/>
     <br/>
    Kopen<br/>
     <br/>
     <br/>
   </td> 
   <td colname="col3">
     <br/>
     <br/>
    aanbevelingen, deelvenster<br/>
     <br/>
     <br/>
    aanbevelingen, deelvenster<br/>
     <br/>
     <br/>
    aanbevelingen, deelvenster<br/>
     <br/>
     <br/>
   </td>
  </tr>
 </tbody>
</table>

Hoe kunt u uw webpagina en tags aanpassen om de waarden van deze koppelingen te onderscheiden? U hebt drie opties: U kunt de identiteitskaart van de Verbinding aanpassen, of het gebied aanpassen, of het dossier van de Module AppMeasurement ActivityMap aanpassen.

## Koppelings-id aanpassen met s_objectID {#section_01B0D463397B4837B2D46F087A6E5937}

Door een unieke object-id te maken, `s_objectID`Voor een koppeling of koppelingslocatie op een pagina kunt u de Activity Map beter bijhouden of Activity Map gebruiken om te rapporteren over een koppelingstype of -locatie, in plaats van de URL van de koppeling. Klikken [hier](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/page-variables.html) voor meer informatie over de `s_objectID` variabele.

>[!IMPORTANT]
>
>Een volgpuntkomma (`;`) is vereist bij gebruik `s_objectID` in Activity Map.

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
    <code>&lt;div&nbsp;id="recommendation&nbsp;panel"&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;div&gt;</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;onClick="s_objectID='Product1';"&nbsp;href="product1.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;div&gt; </code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;onClick="s_objectID='Product2';"&nbsp;href="product2.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt; </code><br/>
    <code>&nbsp;&lt;div&gt; </code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;onClick="s_objectID='Product3';"&nbsp;href="product3.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt;</code><br/>
    <code>&lt;/div&gt;</code>
   </td> 
   <td colname="col2">
     <br/>
     <br/>
    Product1<br/>
     <br/>
     <br/>
    Product2<br/>
     <br/>
     <br/>
    Product3<br/>
     <br/>
     <br/>
   </td> 
   <td colname="col3">
     <br/>
     <br/>
    aanbevelingen, deelvenster<br/>
     <br/>
     <br/>
    aanbevelingen, deelvenster<br/>
     <br/>
     <br/>
    aanbevelingen, deelvenster<br/>
     <br/>
     <br/>
   </td>
  </tr>
 </tbody>
</table>

## Het gebied aanpassen {#section_6B1EF302573B445DBAF44176D0A12DB9}

U kunt de regio aanpassen door ervoor te zorgen dat voor elke link &quot;Kopen&quot; een eigen regio is gedefinieerd. Hiervoor voegt u een `"id"` aan een van de bovenliggende elementen van elke &quot;Buy&quot;-ankertag.

>[!NOTE]
>
>U bent niet strikt beperkt tot de `"id"` parameter als regio-id. U kunt ook uw eigen id instellen met de JavaScript-variabele `"s.ActivityMap.regionIDAttribute"`.

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
    <code>&lt;div&nbsp;id="recommendation&nbsp;panel"&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;div&nbsp;id="region&nbsp;a"&gt;</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;href="product1.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;div&nbsp;id="region&nbsp;b"&gt;</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;href="product2.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;div&nbsp;id="region&nbsp;c"&gt;</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;href="product3.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt;</code><br/>
    <code>&lt;/div&gt;</code>
   </td> 
   <td colname="col2">
     <br/>
     <br/>
    Kopen<br/>
     <br/>
     <br/>
    Kopen<br/>
     <br/>
     <br/>
    Kopen<br/>
     <br/>
     <br/>
   </td> 
   <td colname="col3">
     <br/>
     <br/>
    regio a<br/>
     <br/>
     <br/>
    regio b<br/>
     <br/>
     <br/>
    regio c<br/>
     <br/>
     <br/>
   </td>
  </tr>
 </tbody>
</table>

## Het bestand ActivityMap voor AppMeasurement-module aanpassen {#section_B933BB9F944E4D5389002908A5A881F8}

>[!CAUTION]
>
>Controleer of de gewijzigde code goed werkt. Adobe is niet verantwoordelijk voor het gedrag van de gewijzigde code.

Hier volgen enkele voorbeelden **algemeen** koppelingen-/regiofuncties die u kunt opnemen (in gewijzigde vorm) in het bestand AppMeasurement.js.

```js
s.ActivityMap.link = function(ele, linkName) {
  if (linkName) {
    return linkName;
  }
  if (ele) {
    if (ele.tagName == 'A' && ele.href) {
      return ele.href;
    }
  }
}
```

De `linkName` wordt overgegaan tijdens vraag aan `s.tl()`.

```js
s.ActivityMap.region = function(ele) {
  var className,
  classNames = {
    'header': 1,
    'navbar': 1,
    'left-content': 1,
    'main-content': 1,
    'footer': 1,
  }; 
  while ((ele && (ele = ele.parentNode))) {
    if ((className=ele.className) && classNames[className]) {
      return className;
    }
  }
  return "BODY";
}
```
