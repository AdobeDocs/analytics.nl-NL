---
title: getPercentPageViewed
description: Haal het percentage op van de pagina die de bezoeker heeft weergegeven.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Adobe-insteekmodule: getPercentPageViewed

>[!IMPORTANT] Deze plug-in wordt geleverd door Adobe Consulting als een hoffelijkheid om u te helpen meer waarde te krijgen van Adobe Analytics. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

De `getPercentPageViewed` insteekmodule meet de schuifactiviteit van een bezoeker om te zien hoeveel van een pagina deze weergeeft voordat deze naar een andere pagina gaat. Deze insteekmodule is niet nodig als de pagina&#39;s klein van hoogte zijn of als u de scrollactiviteit niet wilt meten.

## Plug-in installeren met de aangepaste code-editor van Launch

Als u de extensie van de plug-in niet wilt gebruiken, kunt u de aangepaste code-editor gebruiken.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar het [!UICONTROL Extensions] tabblad en klik vervolgens op de [!UICONTROL Configure] knop onder de extensie Adobe Analytics.
1. Vouw de [!UICONTROL Configure tracking using custom code] accordeon uit, zodat de [!UICONTROL Open Editor] knop zichtbaar wordt.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

## De plug-in installeren met AppMeturement

Kopieer en plak de volgende code ergens in het AppMeasurement-bestand nadat het analytics tracking-object is geïnstantieerd (met [`s_gi`](../functions/s-gi.md)). Door opmerkingen en versienummers van de code in uw implementatie te behouden, kan Adobe eventuele problemen oplossen.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getPercentPageViewed v4.0 w/handlePPVevents helper function (Requires p_fo plug-in) */
s.getPercentPageViewed=function(pid,ch){var s=this,a=s.c_r("s_ppv");a=-1<a.indexOf(",")?a.split(","):[];a[0]=s.unescape(a[0]); pid=pid?pid:s.pageName?s.pageName:document.location.href;s.ppvChange="undefined"===typeof ch||!0==ch?!0:!1;if("undefined"=== typeof s.linkType||"o"!==s.linkType)s.ppvID&&s.ppvID===pid||(s.ppvID=pid,s.c_w("s_ppv",""),s.handlePPVevents()), s.p_fo("s_gppvLoad") &&window.addEventListener&&(window.addEventListener("load",s.handlePPVevents,!1),window.addEventListener("click",s.handlePPVevents, !1),window.addEventListener("scroll",s.handlePPVevents,!1)),s._ppvPreviousPage=a[0]?a[0]:"",s._ppvHighestPercentViewed=a[1]?a[1]:"",s._ppvInitialPercentViewed=a[2]?a[2]:"",s._ppvHighestPixelsSeen=a[3]?a[3]:"",s._ppvFoldsSeen=a[4]?a[4]:"",s._ppvFoldsAvailable=a[5]?a[5]:""};

/* Adobe Consulting Plugin: handlePPVevents helper function (for getPercentPageViewed v4.0 Plugin) */
s.handlePPVevents=function(){if("undefined"!==typeof s_c_il){for(var c=0,g=s_c_il.length;c<g;c++)if(s_c_il[c]&& (s_c_il[c].getPercentPageViewed||s_c_il[c].getPreviousPageActivity)){var s=s_c_il[c];break}if(s&&s.ppvID){var f=Math.max (Math.max(document.body.scrollHeight,document.documentElement.scrollHeight),Math.max(document.body.offsetHeight, document.documentElement.offsetHeight),Math.max(document.body.clientHeight,document.documentElement.clientHeight)),h= window.innerHeight||document.documentElement.clientHeight||document.body.clientHeight;c=(window.pageYOffset|| window.document.documentElement.scrollTop||window.document.body.scrollTop)+h;g=Math.min(Math.round(c/f*100),100);var k=Math.floor(c/h);h=Math.floor(f/h);var d="";if(!s.c_r("s_tp")||s.unescape(s.c_r("s_ppv").split(",")[0])!==s.ppvID||s.p_fo(s.ppvID) ||1==s.ppvChange&&s.c_r("s_tp")&&f!=s.c_r("s_tp")){(s.unescape(s.c_r("s_ppv").split(",")[0])!==s.ppvID||s.p_fo(s.ppvID+"1"))&&s.c_w("s_ips",c);if(s.c_r("s_tp")&&s.unescape(s.c_r("s_ppv").split(",")[0])===s.ppvID){s.c_r("s_tp");d=s.c_r("s_ppv");var e=-1< d.indexOf(",")?d.split(","):[];d=e[0]?e[0]:"";e=e[3]?e[3]:"";var l=s.c_r("s_ips");d=d+","+Math.round(e/f*100)+","+Math.round(l/ f*100)+","+e+","+k}s.c_w("s_tp",f)}else d=s.c_r("s_ppv");var b=d&&-1<d.indexOf(",")?d.split(",",6):[];f=0<b.length?b[0]: escape(s.ppvID);e=1<b.length?parseInt(b[1]):g;l=2<b.length?parseInt(b[2]):g;var m=3<b.length?parseInt(b[3]):c,n=4<b.length? parseInt(b[4]):k;b=5<b.length?parseInt(b[5]):h;0<g&&(d=f+","+(g>e?g:e)+","+l+","+(c>m?c:m)+","+(k>n?k:n)+","+(h>b?h:b)); s.c_w("s_ppv",d)}}};

/* Adobe Consulting Plugin: p_fo (pageFirstOnly) v2.0 */
s.p_fo=function(on){var s=this;s.__fo||(s.__fo={});if(s.__fo[on])return!1;s.__fo[on]={};return!0};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `getPercentPageViewed` methode gebruikt de volgende argumenten:

* **`pid`** (optioneel, tekenreeks):  Een op pagina gebaseerde id die u kunt correleren met de percentages die worden verschaft door de metingen van de plug-in.  Wordt standaard ingesteld op de `pageName` variabele.
* **`ch`** (optioneel, Booleaans):  Stel deze in op `false` (of `0`) als u niet wilt dat de insteekmodule rekening houdt met wijzigingen die na de eerste keer laden in de grootte van een pagina zijn aangebracht. Als deze waarde wordt weggelaten, wordt dit argument standaard ingesteld op `true`. Adobe raadt u aan dit argument in de meeste gevallen weg te laten.

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

**Opmerking**:  Als een volledige pagina zichtbaar is wanneer deze wordt geladen, zijn zowel de afmetingen Hoogste weergegeven percentage als Oorspronkelijk weergegeven percentage gelijk aan 100. Zowel de getoonde als de beschikbare mappen zijn gelijk aan 1.   Wanneer een volledige pagina NIET zichtbaar is wanneer deze wordt geladen maar de bezoeker de pagina nooit omlaag schuift voordat deze naar de volgende pagina gaat, zijn zowel de afmetingen Hoogste percentage weergegeven als Oorspronkelijk percentage weergegeven gelijk aan dezelfde waarde.

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

### v4.0 (7 oktober 2019)

* Toegevoegde `s._ppvFoldsSeen` en `s._ppvFoldsAvailable` oplossingen

### v3.01 (13 augustus 2018)

* Probleem verholpen voor pagina&#39;s met meerdere AppMeturement-objecten op een pagina.

### v3.0 (13 april 2018)

* Puntrelease (opnieuw gecompileerd, kleinere codegrootte)
* Plug-in maakt nu variabelen die aan Adobe Analytics-variabelen moeten worden toegewezen in plaats van geretourneerde waarden
