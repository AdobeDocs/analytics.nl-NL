---
title: getPercentPageViewed
description: Haal het percentage op van de pagina die de bezoeker heeft weergegeven.
feature: Appmeasurement Implementation
exl-id: 7a842cf0-f8cb-45a9-910e-5793849bcfb8
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 0%

---

# Adobe-insteekmodule: getPercentPageViewed

{{plug-in}}

De insteekmodule `getPercentPageViewed` meet de schuifactiviteit van een bezoeker om te zien hoeveel van een pagina deze weergeeft voordat deze naar een andere pagina gaat. Deze insteekmodule is niet nodig als de pagina&#39;s klein van hoogte zijn of als u de scrollactiviteit niet wilt meten.

## De insteekmodule installeren met de extensie Web SDK of Web SDK

Deze insteekmodule wordt nog niet ondersteund voor gebruik in de Web SDK.

## De insteekmodule installeren met de Adobe Analytics-extensie

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken in Adobe Analytics.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop [!UICONTROL Catalog]
1. De extensie [!UICONTROL Common Analytics Plugins] installeren en publiceren
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: geen
   * Event: Core - bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: veelgebruikte plug-ins voor Analytics
   * Type handeling: Initialize getPercentPageViewed
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met aangepaste code-editor

Als u niet de Gemeenschappelijke Insteekmodule van Analytics wilt gebruiken, kunt u de redacteur van de douanecode gebruiken.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste eigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder de extensie Adobe Analytics.
1. Vouw de accordeon [!UICONTROL Configure tracking using custom code] uit, zodat de knop [!UICONTROL Open Editor] zichtbaar wordt.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

## Plug-in installeren met AppMeasurement

Kopieer en plak de volgende code ergens in het AppMeasurement-bestand nadat het object Analytics tracking is geïnstantieerd (met [`s_gi`](../functions/s-gi.md) ). Door opmerkingen en versienummers van de code in uw implementatie te behouden, helpt Adobe bij het oplossen van mogelijke problemen.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getPercentPageViewed v5.1 */
function getPercentPageViewed(pid,ch){var e=pid,i=ch;if("-v"===e)return{plugin:"getPercentPageViewed",version:"5.1"};var t=function(){if(void 0!==window.s_c_il){for(var e,i=0;i<window.s_c_il.length;i++)if((e=window.s_c_il[i])._c&&"s_c"===e._c)return e}}();function o(){if(window.ppvID){var e=Math.max(Math.max(document.body.scrollHeight,document.documentElement.scrollHeight),Math.max(document.body.offsetHeight,document.documentElement.offsetHeight),Math.max(document.body.clientHeight,document.documentElement.clientHeight)),i=window.innerHeight||document.documentElement.clientHeight||document.body.clientHeight,t=(window.pageYOffset||window.document.documentElement.scrollTop||window.document.body.scrollTop)+i,o=Math.min(Math.round(t/e*100),100),n=Math.floor(e/i),p=Math.floor(t/i),s="";if(!window.cookieRead("s_tp")||decodeURIComponent(window.cookieRead("s_ppv").split(",")[0])!==window.ppvID||window.p_fo(window.ppvID)||!0==window.ppvChange&&window.cookieRead("s_tp")&&e!=window.cookieRead("s_tp")){if((decodeURIComponent(window.cookieRead("s_ppv").split(",")[0])!==window.ppvID||window.p_fo(window.ppvID+"1"))&&window.cookieWrite("s_ips",t),window.cookieRead("s_tp")&&decodeURIComponent(window.cookieRead("s_ppv").split(",")[0])===window.ppvID){window.cookieRead("s_tp");var a=window.cookieRead("s_ppv"),c=a.indexOf(",")>-1?a.split(","):[],d=c[0]?c[0]:"",r=window.cookieRead("s_ips"),l=c[3]?c[3]:"";s=d+","+Math.round(r/e*100)+","+Math.round(l/e*100)+","+o+","+l+","+n+","+p}window.cookieWrite("s_tp",e)}else s=window.cookieRead("s_ppv");var v=s&&s.indexOf(",")>-1?s.split(",",7):[],f=v.length>0?v[0]:encodeURIComponent(window.ppvID),$=v.length>1?parseInt(v[1]):o,h=v.length>2?parseInt(v[2]):o,u=v.length>4?parseInt(v[4]):t,k=v.length>5?parseInt(v[5]):n,m=v.length>6?parseInt(v[6]):p;o>0&&(s=f+","+$+","+(o>h?o:h)+","+o+","+(t>u?t:u)+","+(n>k?n:k)+","+(p>m?p:m)),window.cookieWrite("s_ppv",s)}}void 0!==t&&(t.contextData.getPercentPageViewed="5.1"),window.pageName=void 0!==t&&t.pageName||"",window.cookieWrite=window.cookieWrite||function(e,i,t){if("string"==typeof e){if(g=function(){var e=window.location.hostname,i=window.location.hostname.split(".").length-1;if(e&&!/^[0-9.]+$/.test(e)){i=2<i?i:2;var t=e.lastIndexOf(".");if(0<=t){for(;0<=t&&1<i;)t=e.lastIndexOf(".",t-1),i--;t=0<t?e.substring(t):e}}return t}(),i=void 0!==i?""+i:"",t||""===i){if(""===i&&(t=-60),"number"==typeof t){var o=new Date;o.setTime(o.getTime()+6e4*t)}else o=t}return!!e&&(document.cookie=encodeURIComponent(e)+"="+encodeURIComponent(i)+"; path=/;"+(t?" expires="+o.toUTCString()+";":"")+(g?" domain="+g+";":""),void 0!==window.cookieRead)&&window.cookieRead(e)===i}},window.cookieRead=window.cookieRead||function(e){if("string"!=typeof e)return"";e=encodeURIComponent(e);var i=" "+document.cookie,t=i.indexOf(" "+e+"="),o=0>t?t:i.indexOf(";",t);return(e=0>t?"":decodeURIComponent(i.substring(t+2+e.length,0>o?i.length:o)))?e:""},window.p_fo=window.p_fo||function(e){return window.__fo||(window.__fo={}),!window.__fo[e]&&(window.__fo[e]={},!0)};var n=window.cookieRead("s_ppv"),p=n.indexOf(",")>-1?n.split(","):[];p[0]=p.length>0?decodeURIComponent(p[0]):"",e=e||(window.pageName?window.pageName:document.location.href),void 0===i||!0==i?window.ppvChange=!0:window.ppvChange=!1,void 0!==t&&t.linkType&&"o"===t.linkType||(window.ppvID&&window.ppvID===e||(window.ppvID=e,window.cookieWrite("s_ppv",""),o()),window.p_fo("s_gppvLoad2")&&window.addEventListener&&(window.addEventListener("load",o,!1),window.addEventListener("click",o,!1),window.addEventListener("scroll",o,!1)),this._ppvPreviousPage=p[0]?p[0]:"",this._ppvInitialPercentViewed=p[1]?p[1]:"",this._ppvHighestPercentViewed=p[2]?p[2]:"",this._ppvFinalPercentViewed=p[3]?p[3]:"",this._ppvHighestPixelsSeen=p[4]?p[4]:"",this._ppvFoldsAvailable=p[5]?p[5]:"",this._ppvFoldsSeen=p[6]?p[6]:"")}
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De functie `getPercentPageViewed` gebruikt de volgende argumenten:

* **`pid`** (optioneel, tekenreeks): een variabele of waarde die gelijk is aan de huidige pagina. Wordt standaard ingesteld op de variabele Analytics AppMeasurement `pageName` OR de huidige URL als de variabele AppMeasurement pageName niet is ingesteld.
* **`ch`** (optioneel, Boolean): stel deze waarde in op `false` (of `0` ) als u niet wilt dat de insteekmodule rekening houdt met wijzigingen die na de eerste keer laden in de grootte van een pagina worden aangebracht. Als deze waarde wordt weggelaten, wordt dit argument standaard ingesteld op `true` . Adobe beveelt in de meeste gevallen aan dit argument weg te laten.

Wanneer deze functie wordt aangeroepen, wordt niets geretourneerd; in plaats daarvan worden de volgende variabelen ingesteld:

* `window._ppvPreviousPage`: De naam van de vorige weergegeven pagina. De laatste scrollmaten voor de huidige pagina zijn pas beschikbaar nadat een nieuwe pagina is geladen.
* `window._ppvInitialPercentViewed`: Het percentage van de vorige pagina dat zichtbaar was toen de vorige pagina voor het eerst werd geladen. Als de hele pagina zichtbaar is wanneer deze voor het eerst wordt geladen, is deze waarde `100` .
* `window._ppvHighestPercentViewed`: het hoogste percentage van de vorige pagina dat de bezoeker heeft weergegeven (in de hoogte). Het grootste punt waarop de bezoeker naar de vorige pagina is geschoven. Als de hele pagina zichtbaar is wanneer deze voor het eerst wordt geladen, is deze waarde `100` .
* `window._ppvFinalPercentViewed`: Het percentage van de vorige pagina dat zichtbaar was op het punt dat de bezoeker naar de huidige pagina heeft verplaatst. Deze waarde is gelijk aan of groter dan het oorspronkelijk weergegeven percentage en is ook gelijk aan of kleiner dan de hoogst weergegeven percentagepagina.
* `window._ppvHighestPixelsSeen`: Het hoogste aantal pixels in totaal dat de bezoeker op de vorige pagina naar beneden heeft geschoven (in de hoogte).
* `window._ppvFoldsAvailable`: Het totale aantal pagina&#39;s dat beschikbaar is om omlaag te schuiven op de vorige pagina. Als de hele pagina zichtbaar is wanneer deze voor het eerst wordt geladen, is deze waarde `1` .
* `window._ppvFoldsSeen`: Het hoogste aantal &#39;paginamappen&#39; dat wordt bereikt wanneer de bezoeker de vorige pagina omlaag schuift. Deze variabele bevat de vouwfactor &quot;top-of-page&quot;. Als de hele pagina zichtbaar is wanneer deze voor het eerst wordt geladen, is deze waarde `1` .

Wijs één of meerdere van deze variabelen aan eVars toe om afmetingsgegevens in rapporten te zien.

Deze plug-in maakt drie cookies van de eerste fabrikant die aan het einde van een browsersessie verlopen:

* `s_ppv`: slaat elk van de waarden op die door de functie aan te roepen worden blootgesteld
* `s_tp`: slaat de totale pixelhoogte van de vorige pagina op
* `s_ips`: slaat het aanvankelijke percentage op dat van de vorige pagina is verschoven

## Voorbeelden

```js
// 1. Runs the getPercentPageViewed function if the page variable is set
// 2. Sets prop1 to the previous value of the page variable
// 3. Sets prop2 to the intial percent, the highest percent, and the final percent viewed; the number of folds available on the page, and the number of folds viewed ( of the previous page)
if(s.pageName) getPercentPageViewed();
if(_ppvPreviousPage)
{
  s.prop1 = _ppvPreviousPage;
  s.prop2 = "initialPercent=" + _ppvInitialPercentViewed + " | highestPercent=" + _ppvHighestPercentViewed + " | finalPercent=" + _ppvFinalPercentViewed + " | foldsAvailable=" + _ppvFoldsAvailable + " | foldsSeen=" + _ppvFoldsSeen;
}

// Given prop5 operates as a page type variable:
// 1. Runs the getPercentPageViewed function if prop5 has a value
// 2. Sets prop1 to the previous value of the page type
// 3. Sets prop2 to the initial percent viewed and the highest percent viewed.
if(s.prop5) getPercentPageViewed(s.prop5);
if(_ppvPreviousPage)
{
  s.prop1 = _ppvPreviousPage;
  s.prop2 = "initialPercent=" + _ppvInitialPercentViewed + " | highestPercent=" + _ppvHighestPercentViewed;
}
```

## Versiehistorie

### 5.1 (8 december 2022)

* De oplossing `_finalPercentViewed` toegevoegd

### 5.0.1 (22 juni 2021)

* Probleem verholpen waarbij bepaalde speciale tekens ertoe leidden dat de insteekmodule werd afgebroken.

### 5.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### v4.0 (7 oktober 2019)

* Toegevoegde `s._ppvFoldsSeen` en `s._ppvFoldsAvailable` oplossingen

### v3.01 (13 augustus 2018)

* Probleem verholpen met pagina&#39;s die meerdere AppMeasurement-objecten op een pagina hebben.

### v3.0 (13 april 2018)

* Puntrelease (opnieuw gecompileerd, kleinere codegrootte)
* Plug-in maakt nu variabelen die aan Adobe Analytics-variabelen moeten worden toegewezen in plaats van geretourneerde waarden
