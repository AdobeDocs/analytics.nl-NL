---
title: getTimeToComplete
description: Meet de tijd die u nodig hebt om een taak te voltooien.
feature: Variables
exl-id: 90a93480-3812-49d4-96f0-8eaf5a70ce3c
source-git-commit: 77142b65fe0f88826b8b0df5bba4a4dc1a0dbecf
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# Adobe-plug-in: getTimeToComplete

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

De `getTimeToComplete` de insteekmodule volgt de tijd die een gebruiker nodig heeft om een proces op een site te voltooien. De &quot;klok&quot; begint wanneer de `start` handeling wordt aangeroepen en eindigt wanneer de `stop` handeling wordt aangeroepen. Adobe raadt u aan deze plug-in te gebruiken als er een workflow op de site is die enige tijd in beslag neemt en u wilt weten hoeveel tijd bezoekers nodig hebben om deze te voltooien. Het is niet nodig deze plug-in te gebruiken als de workflow op uw site een korte periode (minder dan 3 seconden) in beslag neemt omdat de granulariteit slechts tot de volledige seconde is.

<!--## Install the plug-in using the Web SDK or the Adobe Analytics extension

Adobe offers an extension that allows you to use most commonly-used plug-ins.

1. Log in to [Adobe Experience Platform Data Collection](https://experience.adobe.com/data-collection) using your AdobeID credentials.
1. Click the desired tag property.
1. Go to the [!UICONTROL Extensions] tab, then click on the [!UICONTROL Catalog] button
1. Install and publish the [!UICONTROL Common Analytics Plugins] extension
1. If you haven't already, create a rule labeled "Initialize Plug-ins" with the following configuration:
    * Condition: None
    * Event: Core – Library Loaded (Page Top)
1. Add an action to the above rule with the following configuration:
    * Extension: Common Analytics Plugins
    * Action Type: Initialize getTimeToComplete
1. Save and publish the changes to the rule.-->

## Plug-in installeren met aangepaste code-editor

Als u de extensie van de plug-in niet wilt gebruiken, kunt u de aangepaste code-editor gebruiken.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder de extensie Adobe Analytics.
1. Breid uit [!UICONTROL Configure tracking using custom code] accordion, die de [!UICONTROL Open Editor] knop.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

## Installeer de plug-in met AppMeasurement

Kopieer en plak de volgende code ergens in het AppMeasurement-bestand nadat het analytics tracking-object is geïnstantieerd (met [`s_gi`](../functions/s-gi.md)). Door opmerkingen en versienummers van de code in uw implementatie te behouden, kunt u Adobe doen met het oplossen van mogelijke problemen.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getTimeToComplete v4.0 */
function getTimeToComplete(sos,cn,exp,tp){var f=sos,m=cn,l=exp,e=tp;if("-v"===f)return{plugin:"getTimeToComplete",version:"4.0"};var k=function(){if("undefined"!==typeof window.s_c_il)for(var c=0,b;c<window.s_c_il.length;c++)if(b=window.s_c_il[c],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof k&&(k.contextData.getTimeToComplete="4.0");window.formatTime=window.formatTime||function(c,b,d){function e(b,d,c,e){if("string"!==typeof d)return!1;if("string"===typeof b)b=b.split(c||",");else if("object"!==typeof b)return!1;c=0;for(a=b.length;c<a;c++)if(1==e&&d===b[c]||d.toLowerCase()===b[c].toLowerCase())return!0;return!1}if(!("undefined"===typeof c||isNaN(c)||0>Number(c))){var h="";"string"===typeof b&&"d"===b||("string"!==typeof b||!e("h,m,s",b))&&86400<=c?(b=86400,h="days",d=isNaN(d)?1:b/(d*b)):"string"===typeof b&&"h"===b||("string"!==typeof b||!e("m,s",b))&&3600<=c?(b=3600,h="hours",d=isNaN(d)?4:b/(d*b)):"string"===typeof b&&"m"===b||("string"!==typeof b||!e("s",b))&&60<=c?(b=60,h="minutes",d=isNaN(d)?2:b/(d*b)):(b=1,h="seconds",d=isNaN(d)?.2:b/d);h=Math.round(c*d/b)/d+" "+h;0===h.indexOf("1 ")&&(h=h.substring(0,h.length-1));return h}};window.cookieWrite=window.cookieWrite||function(c,b,d){if("string"===typeof c){var e=window.location.hostname,h=window.location.hostname.split(".").length-1;if(e&&!/^[0-9.]+$/.test(e)){h=2<h?h:2;var f=e.lastIndexOf(".");if(0<=f){for(;0<=f&&1<h;)f=e.lastIndexOf(".",f-1),h--;f=0<f?e.substring(f):e}}g=f;b="undefined"!==typeof b?""+b:"";if(d||""===b)if(""===b&&(d=-60),"number"===typeof d){var k=new Date;k.setTime(k.getTime()+6E4*d)}else k=d;return c&&(document.cookie=encodeURIComponent(c)+"="+encodeURIComponent(b)+"; path=/;"+(d?" expires="+k.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof cookieRead)?cookieRead(c)===b:!1}};window.cookieRead=window.cookieRead||function(c){if("string"===typeof c)c=encodeURIComponent(c);else return"";var b=" "+document.cookie,d=b.indexOf(" "+c+"="),e=0>d?d:b.indexOf(";",d);return(c=0>d?"":decodeURIComponent(b.substring(d+2+c.length,0>e?b.length:e)))?c:""};f=f?f.toLowerCase():"start";if("stop"===f||"start"===f){m=m?m:"s_gttc";e?e="d"===e?864E5:"h"===e?36E5:"s"===e?1E3:6E4:(l=30,e=6E4);l=isNaN(l)?30:l;l*=e;k=cookieRead(m);e=new Date;if("stop"===f&&k)return l=Math.round((e.getTime()-k)/1E3),cookieWrite(m,"",0),formatTime(l);"start"!==f||k?k&&Number(k)<e.getTime()+18E5&&cookieWrite(m,k,30):(f=String(e.getTime()),e.setTime(e.getTime()+l),cookieWrite(m,f,e))}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `getTimeToComplete` function gebruikt de volgende argumenten:

* **`sos`** (optioneel, tekenreeks): Instellen op `"start"` wanneer u de timer wilt starten. Instellen op `"stop"` wanneer u de timer wilt stoppen. Standaardwaarden: `"start"`.
* **`cn`** (optioneel, tekenreeks): De naam van het cookie waarin de begintijd wordt opgeslagen. Standaardwaarden: `"s_gttc"`.
* **`exp`** (optioneel, geheel getal): Het aantal seconden, uren of dagen (afhankelijk van de `tp` time-parting argument) dat het koekje (en tijdopnemer) verloopt. Wordt standaard ingesteld op 30 minuten.
* **`tp`** (optioneel, tekenreeks): De time-parting-tekenreeks die de cookie (en timer) vervalt en die wordt gebruikt met de `exp` argument. Stel in op &quot;d&quot; voor dagen, &quot;h&quot; voor uren of &quot;s&quot; voor seconden. Als deze niet is ingesteld, wordt de vervaldatum van het cookie (en de timer) standaard ingesteld op 30 minuten, ongeacht wat de waarde `exp` argument is ingesteld op.

Als deze functie wordt aangeroepen, wordt een tekenreeks geretourneerd die het aantal dagen, uren, minuten en/of seconden bevat dat nodig was tussen de `"start"` en `"stop"` handeling.

## Voorbeelden

```js
// Start the timer when the visitor starts the checkout
if(s.events.indexOf("scCheckout") > -1) getTimeToComplete("start");

// Stop the timer when the visitor makes the purchase and set prop1 to the time difference between stop and start
// Sets prop1 to the amount of time it took to complete the purchase process
if(s.events.indexOf("purchase") > -1) s.prop1 = getTimeToComplete("stop");

// Simultaneously track the time it takes to complete a purchase and to fill out a registration form
// Stores each timer in their own respective cookies so they run independently
if(inList(s.events, "scCheckout")) getTimeToComplete("start", "gttcpurchase");
if(inList(s.events, "purchase")) s.prop1 = getTimeToComplete("start", "gttcpurchase");
if(inList(s.events, "event1")) getTimeToComplete("start", "gttcregister", 7, "d");
if(inList(s.events, "event2")) s.prop2 = getTimeToComplete("stop", "gttcregister", 7, "d");
```

## Versiehistorie

### 4.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 3.1 (30 september 2019)

* Toegevoegde logica die de waarde &quot;start&quot; of &quot;stop&quot; in het eerste argument vereist.  Met alle andere waarden die worden doorgegeven, wordt de insteekmodule niet uitgevoerd.
* Bijgewerkt `inList 2.0` insteekmodule voor `inList 2.1`.

### 3.0 (23 augustus 2018)

* De `formatTime v1.0` insteekmodule voor `formatTime v1.1`.

### 3.0 (17 april 2018)

* Puntrelease (opnieuw gecompileerd, kleiner codeformaat).
* Kleine correcties.

### (2 juni 2016)

* De afhankelijkheid van de `p_fo` insteekmodule.
* Toegevoegde compatibiliteit met H-code en AppMeasurement.
* Logboekregistratie van toegevoegde console.
