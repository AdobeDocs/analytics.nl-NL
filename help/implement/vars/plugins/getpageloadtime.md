---
title: getPageLoadTime
description: Houd bij hoeveel tijd een pagina nodig heeft om te laden.
feature: Variables
exl-id: 9bf0e26b-f1af-48a6-900a-712f7e588d37
source-git-commit: 15f1cd260709c2ab82d56a545494c31ad86d0ab0
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 0%

---

# Adobe-plug-in: getPageLoadTime

{{plug-in}}

De `getPageLoadTime` de insteekmodule gebruikt het JavaScript-prestatieobject zodat u kunt meten hoeveel tijd het duurt voordat een pagina volledig is geladen. Adobe raadt u aan deze plug-in te gebruiken als u wilt meten hoelang het duurt om pagina&#39;s te laden.

>OPMERKING/WAARSCHUWING: Als u deze insteekmodule vanaf een vorige versie upgradet, moet u waarschijnlijk ook de code wijzigen die deze functie ook aanroept.  Controleer uw implementatie en test het grondig voordat u gaat implementeren naar productie

## De insteekmodule installeren met de extensie Web SDK of Web SDK

Deze plug-in wordt nog niet ondersteund voor gebruik in de Web SDK.

## De insteekmodule installeren met de Adobe Analytics-extensie

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken in Adobe Analytics.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop [!UICONTROL Catalog] knop
1. Installeer en publiceer de [!UICONTROL Common Analytics Plugins] extension
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: Geen
   * Gebeurtenis: Kern - Bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: Gebruikelijke plug-ins voor Analytics
   * Type handeling: Initialize getPageLoadTime
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met aangepaste code-editor

Als u niet de Gemeenschappelijke Insteekmodule van Analytics wilt gebruiken, kunt u de redacteur van de douanecode gebruiken.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder de extensie Adobe Analytics.
1. Breid uit [!UICONTROL Configure tracking using custom code] accordion, die de [!UICONTROL Open Editor] knop.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

## Plug-in installeren met AppMeasurement

Kopieer en plak de volgende code ergens in het bestand AppMeasurement nadat het object Analytics tracking is geïnstantieerd (met [`s_gi`](../functions/s-gi.md)). Door opmerkingen en versienummers van de code in uw implementatie te behouden, kunt u Adobe doen met het oplossen van mogelijke problemen.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getPageLoadTime v3.0 */
!function(){let e=globalThis.window||this;e.getPageLoadTime=function(t){let i=function(){if(e.s_c_il){for(let t in e.s_c_il)if("s_c"===e.s_c_il[t]._c)return e.s_c_il[t]}}();function n(){var i=performance.timing;i.loadEventEnd>0&&(clearInterval(e.pi),""===e.cookieRead("s_plt")&&e.cookieWrite("s_plt",function e(t,i){if(t>=0&&i>=0)return t-i<6e4&&t-i>=0?parseFloat((t-i)/1e3).toFixed(2):60}(i.loadEventEnd,i.navigationStart)+","+t)),e.ptc=i.loadEventEnd}if(i&&(i.contextData.getPageLoadTime="3.1"),t=t||i&&i.pageName||document.location.href,e.cookieWrite=e.cookieWrite||function(t,i,n){if("string"==typeof t){if(g=function(){var t=e.location.hostname,i=e.location.hostname.split(".").length-1;if(t&&!/^[0-9.]+$/.test(t)){i=2<i?i:2;var n=t.lastIndexOf(".");if(0<=n){for(;0<=n&&1<i;)n=t.lastIndexOf(".",n-1),i--;n=0<n?t.substring(n):t}}return n}(),i=void 0!==i?""+i:"",n||""===i){if(""===i&&(n=-60),"number"==typeof n){var o=new Date;o.setTime(o.getTime()+6e4*n)}else o=n}return!!t&&(document.cookie=encodeURIComponent(t)+"="+encodeURIComponent(i)+"; path=/;"+(n?" expires="+o.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!=typeof cookieRead)&&cookieRead(t)===i}},e.cookieRead=e.cookieRead||function(e){if("string"!=typeof e)return"";e=encodeURIComponent(e);var t=" "+document.cookie,i=t.indexOf(" "+e+"="),n=0>i?i:t.indexOf(";",i);return(e=0>i?"":decodeURIComponent(t.substring(i+2+e.length,0>n?t.length:n)))?e:""},e.p_fo=e.p_fo||function(t){return e.__fo||(e.__fo={}),!e.__fo[t]&&(e.__fo[t]={},!0)},performance&&e.p_fo("performance")){var o=performance;o.clearResourceTimings(),""!==e.cookieRead("s_plt")&&(o.timing.loadEventEnd>0&&clearInterval(e.pi),this._pltLoadTime=e.cookieRead("s_plt").split(",")[0],this._pltPreviousPage=e.cookieRead("s_plt").split(",")[1],e.cookieWrite("s_plt","")),0===o.timing.loadEventEnd?e.pi=setInterval(function(){n()},250):o.timing.loadEventEnd>0&&(e.ptc?e.ptc===o.timing.loadEventEnd&&1===o.getEntries().length&&(e.pwp=setInterval(function(){var i;(i=performance).getEntries().length>0&&(e.ppfe===i.getEntries().length?clearInterval(e.pwp):e.ppfe=i.getEntries().length),""===e.cookieRead("s_plt")&&e.cookieWrite("s_plt",((i.getEntries()[i.getEntries().length-1].responseEnd-i.getEntries()[0].startTime)/1e3).toFixed(2)+","+t)},500)):n())}},e.getPageLoadTime.getVersion=function(){return{plugin:"getPageLoadTime",version:"3.0"}}}();
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `getPercentPageViewed` function gebruikt de volgende argumenten:

* **`pv`** (optioneel, tekenreeks): De dimensie waarmee de laadtijd van de pagina moet worden gecorreleerd.  Deze waarde moet gelijk zijn aan een waarde die de pagina zelf identificeert. Wanneer deze niet is ingesteld, wordt voor dit argument standaard de Adobe AppMeasurement pageName-variabele (d.w.z. s.pageName) gebruikt of de URL wanneer s.pageName niet is ingesteld

Het aanroepen van deze functie retourneert niets; in plaats daarvan worden de volgende variabelen ingesteld :

* `window._pltPreviousPage`: De waarde van de vorige pagina (d.w.z. wat is doorgegeven aan het argument pv)
* `window._pltLoadTime`: De tijd in seconden die de vorige pagina nodig had om te laden

Met de insteekmodule getPageLoadTime wordt één cookie van de eerste fabrikant gemaakt:

* `s_plt`: De tijd, in seconden, die de vorige pagina nam om te laden.  Bevat ook de waarde van wat in het pv-argument werd overgegaan.  Verloopt aan het einde van de browsersessie.

## Voorbeeld

```js
// 1. Run the getPageLoadTime function if the pageName variable is set
// 2. Set prop10 to the load time of the previous page
// 3. Set eVar10 to the name of the previous page
// 4. Set event100 to the load time (in seconds) of the previous page. A numeric event is required to capture this value.
// You can then use event100 in calculated metrics to obtain the average page load time per page.
if(s.pageName) getPageLoadTime();
if(window._pltPreviousPage)
{
  s.prop10 = window._pltLoadTime;
  s.eVar10 = window._pltPreviousPage
  s.events = "event100=" + window._pltLoadTime;
}
```

## Versiehistorie

### 3.0 (6 december 2022)

* Volledige herschrijving van de plug-in om deze oplossing-agnostisch te maken.  Dit is nu bijvoorbeeld compatibel met de SDK van Adobe Experience Platform Web
* Hiermee maakt u de `_pltPreviousPage` en `_pltLoadTime` variabelen in het vensterobject (in plaats van in het object AppMeasurement)
* Hiermee wordt de noodzaak van het s_pltp-cookie verwijderd. Alles wordt nu alleen in het s_plt-cookie opgeslagen
* Omvat de functie getVersion om met het oplossen van problemen te helpen

### 2.0.1 (26 maart 2021)

* Correctie van het probleem waarbij de insteekmodule de waarden voor het s-object niet correct instelde.

### 2.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 1.0 (22 mei 2018)

* Eerste release.
