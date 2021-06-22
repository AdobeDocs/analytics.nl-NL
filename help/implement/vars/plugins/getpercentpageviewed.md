---
title: getPercentPageViewed
description: Haal het percentage op van de pagina die de bezoeker heeft weergegeven.
exl-id: 7a842cf0-f8cb-45a9-910e-5793849bcfb8
source-git-commit: c08be9abf73f4ef2007710839966257350b98f12
workflow-type: tm+mt
source-wordcount: '878'
ht-degree: 0%

---

# Adobe-plug-in: getPercentPageViewed

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de insteekmodule `getPercentPageViewed` wordt de schuifactiviteit van een bezoeker gemeten om te zien hoeveel van een pagina deze weergeeft voordat naar een andere pagina wordt gegaan. Deze insteekmodule is niet nodig als de pagina&#39;s klein van hoogte zijn of als u de scrollactiviteit niet wilt meten.

## De insteekmodule installeren met de Adobe Experience Platform Launch-extensie

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken.

1. Meld u met uw Adobe-id aan bij [launch.adobe.com](https://launch.adobe.com).
1. Klik op de gewenste eigenschap.
1. Ga naar het tabblad [!UICONTROL Extensions] en klik op de knop [!UICONTROL Catalog]
1. De extensie [!UICONTROL Common Analytics Plugins] installeren en publiceren
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: Geen
   * Gebeurtenis: Kern - Bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: Gebruikelijke plug-ins voor Analytics
   * Type handeling: getPercentPageViewed initialiseren
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met de aangepaste code-editor van Launch

1. Meld u met uw Adobe-id aan bij [launch.adobe.com](https://launch.adobe.com).
1. Klik op de gewenste eigenschap.
1. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder de uitbreiding van Adobe Analytics.
1. Breid [!UICONTROL Configure tracking using custom code] accordeon uit, die [!UICONTROL Open Editor] knoop openbaart.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

## Installeer de plug-in met AppMeasurement

Kopieer en plak de volgende code ergens in het AppMeasurement-bestand nadat het analytics tracking-object is geïnstantieerd (met [`s_gi`](../functions/s-gi.md)). Door opmerkingen en versienummers van de code in uw implementatie te behouden, kunt u Adobe doen met het oplossen van mogelijke problemen.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getPercentPageViewed v5.0 w/handlePPVevents helper function (Requires AppMeasurement and the p_fo plugin) */
function getPercentPageViewed(pid,ch){var l=pid,p=ch;function m(){if(window.ppvID){var c=Math.max(Math.max(document.body.scrollHeight,document.documentElement.scrollHeight),Math.max(document.body.offsetHeight,document.documentElement.offsetHeight),Math.max(document.body.clientHeight,document.documentElement.clientHeight)),b=window.innerHeight||document.documentElement.clientHeight||document.body.clientHeight,k=(window.pageYOffset||window.document.documentElement.scrollTop||window.document.body.scrollTop)+b,a=Math.min(Math.round(k/c*100),100),n=Math.floor(k/b);b=Math.floor(c/b);var d="";if(!window.cookieRead("s_tp")||decodeURIComponent(window.cookieRead("s_ppv").split(",")[0])!==window.ppvID||window.p_fo(window.ppvID)||1==window.ppvChange&&window.cookieRead("s_tp")&&c!=window.cookieRead("s_tp")){(decodeURIComponent(window.cookieRead("s_ppv").split(",")[0])!==window.ppvID||window.p_fo(window.ppvID+"1"))&&window.cookieWrite("s_ips",k);if(window.cookieRead("s_tp")&&decodeURIComponent(window.cookieRead("s_ppv").split(",")[0])===window.ppvID){window.cookieRead("s_tp");d=window.cookieRead("s_ppv");var f=-1<d.indexOf(",")?d.split(","):[];d=f[0]?f[0]:"";f=f[3]?f[3]:"";var e=window.cookieRead("s_ips");d=d+","+Math.round(f/c*100)+","+Math.round(e/c*100)+","+f+","+n}window.cookieWrite("s_tp",c)}else d=window.cookieRead("s_ppv");var h=d&&-1<d.indexOf(",")?d.split(",",6):[];c=0<h.length?h[0]:escape(window.ppvID);f=1<h.length?parseInt(h[1]):a;e=2<h.length?parseInt(h[2]):a;var l=3<h.length?parseInt(h[3]):k,m=4<h.length?parseInt(h[4]):n;h=5<h.length?parseInt(h[5]):b;0<a&&(d=c+","+(a>f?a:f)+","+e+","+(k>l?k:l)+","+(n>m?n:m)+","+(b>h?b:h));window.cookieWrite("s_ppv",d)}}if("-v"===l)return{plugin:"getPercentPageViewed",version:"5.0"};var e=function(){if("undefined"!==typeof window.s_c_il)for(var c=0,b;c<window.s_c_il.length;c++)if(b=window.s_c_il[c],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof e&&(e.contextData.getPercentPageViewed="5.0");window.pageName="undefined"!==typeof e&&e.pageName||"";window.cookieWrite=window.cookieWrite||function(c,b,a){if("string"===typeof c){var k=window.location.hostname,e=window.location.hostname.split(".").length-1;if(k&&!/^[0-9.]+$/.test(k)){e=2<e?e:2;var d=k.lastIndexOf(".");if(0<=d){for(;0<=d&&1<e;)d=k.lastIndexOf(".",d-1),e--;d=0<d?k.substring(d):k}}g=d;b="undefined"!==typeof b?""+b:"";if(a||""===b)if(""===b&&(a=-60),"number"===typeof a){var f=new Date;f.setTime(f.getTime()+6E4*a)}else f=a;return c&&(document.cookie=encodeURIComponent(c)+"="+encodeURIComponent(b)+"; path=/;"+(a?" expires="+f.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof window.cookieRead)?window.cookieRead(c)===b:!1}};window.cookieRead=window.cookieRead||function(a){if("string"===typeof a)a=encodeURIComponent(a);else return"";var b=" "+document.cookie,c=b.indexOf(" "+a+"="),e=0>c?c:b.indexOf(";",c);return(a=0>c?"":decodeURIComponent(b.substring(c+2+a.length,0>e?b.length:e)))?a:""};window.p_fo=window.p_fo||function(a){window.__fo||(window.__fo={});if(window.__fo[a])return!1;window.__fo[a]={};return!0};var a=window.cookieRead("s_ppv");a=-1<a.indexOf(",")?a.split(","):[];l=l?l:window.pageName?window.pageName:document.location.href;a[0]=decodeURIComponent(a[0]);window.ppvChange="undefined"===typeof p||1==p?!0:!1;"undefined"!==typeof e&&e.linkType&&"o"===e.linkType||(window.ppvID&&window.ppvID===l||(window.ppvID=l,window.cookieWrite("s_ppv",""),m()),window.p_fo("s_gppvLoad")&&window.addEventListener&&(window.addEventListener("load",m,!1),window.addEventListener("click",m,!1),window.addEventListener("scroll",m,!1)),window._ppvPreviousPage=a[0]?a[0]:"",window._ppvHighestPercentViewed=a[1]?a[1]:"",window._ppvInitialPercentViewed=a[2]?a[2]:"",window._ppvHighestPixelsSeen=a[3]?a[3]:"",window._ppvFoldsSeen=a[4]?a[4]:"",window._ppvFoldsAvailable=a[5]?a[5]:"")};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De methode `getPercentPageViewed` gebruikt de volgende argumenten:

* **`pid`** (optioneel, tekenreeks): Een op pagina gebaseerde id die u kunt correleren met de percentages die worden verschaft door de metingen van de plug-in.  Wordt standaard ingesteld op de variabele `pageName`.
* **`ch`** (optioneel, Booleaans): Stel deze in op  `false` (of  `0`) als u niet wilt dat de insteekmodule rekening houdt met wijzigingen die na de eerste keer laden in de grootte van een pagina zijn aangebracht. Indien weggelaten, is dit argument standaard `true`. Adobe beveelt in de meeste gevallen aan dit argument weg te laten.

Als deze methode wordt aangeroepen, wordt niets geretourneerd. in plaats daarvan worden de volgende variabelen ingesteld :

* `s._ppvPreviousPage`: De naam van de vorige weergegeven pagina. De laatste scrollmaten voor de huidige pagina zijn pas beschikbaar nadat een nieuwe pagina is geladen.
* `s._ppvHighestPercentViewed`: Het hoogste percentage van de vorige pagina dat de bezoeker heeft bekeken (in de hoogte). Het verst mogelijke punt waarop de bezoeker naar de vorige pagina is geschoven.
* `s._ppvInitialPercentViewed`: Het percentage van de vorige pagina dat zichtbaar was toen de vorige pagina voor het eerst werd geladen.
* `s._ppvHighestPixelsSeen`: Het hoogste aantal pixels in totaal dat wordt weergegeven (in de hoogte) wanneer de bezoeker de vorige pagina omlaag schuift.
* `s._ppvFoldsSeen`: Het hoogste aantal &#39;paginamappen&#39; dat wordt bereikt wanneer de bezoeker de vorige pagina omlaag schuift. Deze variabele bevat de vouwfactor &quot;top-of-page&quot;.
* `s._ppvFoldsAvailable`: Het aantal pagina&#39;s dat in totaal beschikbaar is om omlaag te schuiven op de vorige pagina.

Wijs één of meerdere van deze variabelen aan eVars toe om afmetingsgegevens in rapporten te zien.

Deze plug-in maakt een cookie van de eerste fabrikant met de naam `s_ppv` die de bovenstaande waarden bevat. Deze verloopt aan het einde van de browsersessie.

## Voorbeelden van aanroepen

### Voorbeeld 1

De volgende code...

```js
if(s.pageName) s.getPercentPageViewed();
if(s._ppvPreviousPage)
{
  s.prop1 = s._ppvPreviousPage;
  s.prop2 = "highestPercentViewed=" + s._ppvHighestPercentViewed + " | initialPercentViewed=" + s._ppvInitialPercentViewed + " + | foldsSeen=" + s._ppvFoldsSeen + " | foldsAvailable=" + s._ppvFoldsAvailable;
}
```

* Hiermee wordt bepaald of s.pageName is ingesteld en, als dit het geval is, wordt de functie getPercentPageViewed uitgevoerd
* Wanneer de functie getPercentPageViewed wordt uitgevoerd, worden de variabelen gemaakt die in de sectie &quot;Retourneert&quot; hierboven worden beschreven
* Als de variabelen &quot;Returns&quot; met succes zijn ingesteld:
   * De code stelt s.prop1 in op de waarde van s._ppvPreviousPage (dat wil zeggen de vorige waarde van s.pageName of de vorige pagina)
   * De code stelt s.prop2 ook in op het hoogste percentage dat op de vorige pagina is weergegeven en het eerste percentage dat op de vorige pagina is weergegeven, samen met het aantal vouwen dat de bezoeker heeft bereikt en het aantal vouwen dat beschikbaar was

**Opmerking**: Als een volledige pagina zichtbaar is wanneer deze wordt geladen, zijn zowel de afmetingen Hoogste weergegeven percentage als Oorspronkelijk weergegeven percentage gelijk aan 100. Zowel de getoonde als de beschikbare mappen zijn gelijk aan 1.   Wanneer een volledige pagina NIET zichtbaar is wanneer deze wordt geladen maar de bezoeker de pagina nooit omlaag schuift voordat deze naar de volgende pagina gaat, zijn zowel de afmetingen Hoogste percentage weergegeven als Oorspronkelijk percentage weergegeven gelijk aan dezelfde waarde.

### Voorbeeld 2

Stel dat s.prop5 opzij is gezet om een opgerold-up &quot;paginatype&quot;eerder dan de volledige paginanaam te vangen.

Met de volgende code wordt bepaald of s.prop5 is ingesteld en wordt, als dat het geval is, de waarde ervan opgeslagen als de &quot;vorige pagina&quot; die overeenkomt met de afmetingen Hoogste weergegeven percentage en Eerste bekeken percentage.  De waarde wordt wel opgeslagen in de variabele s._ppvPreviousPage, maar kan worden behandeld alsof het het vorige paginatype was in plaats van de vorige paginanaam.

```js
if(s.prop5) s.getPercentPageViewed(s.prop5);
if(s._ppvPreviousPage)
{
  s.prop1 = s._ppvPreviousPage;
  s.prop2 = "highestPercentViewed = " + s._ppvHighestPercentViewed + " | initialPercentViewed=" + s._ppvInitialPercentViewed;
}
```

## Versiehistorie

### 5.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### v4.0 (7 oktober 2019)

* Toegevoegde `s._ppvFoldsSeen`- en `s._ppvFoldsAvailable`-oplossingen

### v3.01 (13 augustus 2018)

* Probleem verholpen voor pagina&#39;s met meerdere AppMeturement-objecten op een pagina.

### v3.0 (13 april 2018)

* Puntrelease (opnieuw gecompileerd, kleinere codegrootte)
* Plug-in maakt nu variabelen die aan Adobe Analytics-variabelen moeten worden toegewezen in plaats van geretourneerde waarden
