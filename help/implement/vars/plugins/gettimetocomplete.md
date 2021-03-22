---
title: getTimeToComplete
description: Meet de tijd die u nodig hebt om een taak te voltooien.
translation-type: tm+mt
source-git-commit: 37a3a44053260d9cdb2a3797e07f6d34592abc1f
workflow-type: tm+mt
source-wordcount: '748'
ht-degree: 0%

---


# Adobe-plug-in: getTimeToComplete

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `getTimeToComplete`-plug-in wordt bijgehouden hoeveel tijd een gebruiker nodig heeft om een proces op een site te voltooien. De &quot;klok&quot;begint wanneer `start` actie wordt geroepen en beëindigt wanneer `stop` actie wordt geroepen. Adobe raadt u aan deze plug-in te gebruiken als er een workflow op de site is die enige tijd in beslag neemt en u wilt weten hoeveel tijd bezoekers nodig hebben om deze te voltooien. Het is niet nodig deze plug-in te gebruiken als de workflow op uw site een korte periode (minder dan 3 seconden) in beslag neemt omdat de granulariteit slechts tot de volledige seconde is.

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
   * Type handeling: getTimeToComplete initialiseren
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met de aangepaste code-editor van Launch

Als u de extensie van de plug-in niet wilt gebruiken, kunt u de aangepaste code-editor gebruiken.

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
/* Adobe Consulting Plugin: getTimeToComplete v4.0 */
function getTimeToComplete(sos,cn,exp,tp){var f=sos,m=cn,l=exp,e=tp;if("-v"===f)return{plugin:"getTimeToComplete",version:"4.0"};var k=function(){if("undefined"!==typeof window.s_c_il)for(var c=0,b;c<window.s_c_il.length;c++)if(b=window.s_c_il[c],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof k&&(k.contextData.getTimeToComplete="4.0");window.formatTime=window.formatTime||function(c,b,d){function e(b,d,c,e){if("string"!==typeof d)return!1;if("string"===typeof b)b=b.split(c||",");else if("object"!==typeof b)return!1;c=0;for(a=b.length;c<a;c++)if(1==e&&d===b[c]||d.toLowerCase()===b[c].toLowerCase())return!0;return!1}if(!("undefined"===typeof c||isNaN(c)||0>Number(c))){var h="";"string"===typeof b&&"d"===b||("string"!==typeof b||!e("h,m,s",b))&&86400<=c?(b=86400,h="days",d=isNaN(d)?1:b/(d*b)):"string"===typeof b&&"h"===b||("string"!==typeof b||!e("m,s",b))&&3600<=c?(b=3600,h="hours",d=isNaN(d)?4:b/(d*b)):"string"===typeof b&&"m"===b||("string"!==typeof b||!e("s",b))&&60<=c?(b=60,h="minutes",d=isNaN(d)?2:b/(d*b)):(b=1,h="seconds",d=isNaN(d)?.2:b/d);h=Math.round(c*d/b)/d+" "+h;0===h.indexOf("1 ")&&(h=h.substring(0,h.length-1));return h}};window.cookieWrite=window.cookieWrite||function(c,b,d){if("string"===typeof c){var e=window.location.hostname,h=window.location.hostname.split(".").length-1;if(e&&!/^[0-9.]+$/.test(e)){h=2<h?h:2;var f=e.lastIndexOf(".");if(0<=f){for(;0<=f&&1<h;)f=e.lastIndexOf(".",f-1),h--;f=0<f?e.substring(f):e}}g=f;b="undefined"!==typeof b?""+b:"";if(d||""===b)if(""===b&&(d=-60),"number"===typeof d){var k=new Date;k.setTime(k.getTime()+6E4*d)}else k=d;return c&&(document.cookie=encodeURIComponent(c)+"="+encodeURIComponent(b)+"; path=/;"+(d?" expires="+k.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof cookieRead)?cookieRead(c)===b:!1}};window.cookieRead=window.cookieRead||function(c){if("string"===typeof c)c=encodeURIComponent(c);else return"";var b=" "+document.cookie,d=b.indexOf(" "+c+"="),e=0>d?d:b.indexOf(";",d);return(c=0>d?"":decodeURIComponent(b.substring(d+2+c.length,0>e?b.length:e)))?c:""};f=f?f.toLowerCase():"start";if("stop"===f||"start"===f){m=m?m:"s_gttc";e?e="d"===e?864E5:"h"===e?36E5:"s"===e?1E3:6E4:(l=30,e=6E4);l=isNaN(l)?30:l;l*=e;k=cookieRead(m);e=new Date;if("stop"===f&&k)return l=Math.round((e.getTime()-k)/1E3),cookieWrite(m,"",0),formatTime(l);"start"!==f||k?k&&Number(k)<e.getTime()+18E5&&cookieWrite(m,k,30):(f=String(e.getTime()),e.setTime(e.getTime()+l),cookieWrite(m,f,e))}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De methode `getTimeToComplete` gebruikt de volgende argumenten:

* **`sos`** (optioneel, tekenreeks): Instellen op  `"start"` wanneer u de timer wilt starten. Stel in op `"stop"` wanneer u de timer wilt stoppen. Wordt standaard ingesteld op `"start"`.
* **`cn`** (optioneel, tekenreeks): De naam van het cookie waarin de begintijd wordt opgeslagen. Wordt standaard ingesteld op `"s_gttc"`.
* **`exp`** (optioneel, geheel getal): Het aantal dagen dat de cookie (en timer) verloopt. Wordt standaard ingesteld op `0`, hetgeen het einde van de browsersessie vertegenwoordigt.

Het roepen van deze methode keert een koord terug dat het aantal dagen, uren, notulen en/of seconden bevat het tussen `"start"` en `"stop"` actie nam.

## Voorbeelden van aanroepen

### Voorbeeld 1

Gebruik deze aanroepen om de tijd te bepalen tussen het moment waarop een bezoeker het uitcheckproces start en het moment waarop hij of zij een aankoop doet.

Start de timer wanneer de bezoeker het uitchecken start:

```js
if(s.events.indexOf("scCheckout") > -1) s.getTimeToComplete("start");
```

Stop de tijdopnemer wanneer de bezoeker de aankoop maakt en reeks prop1 aan het tijdverschil tussen stop en begin:

```js
if(s.events.indexOf("purchase") > -1) s.prop1 = s.getTimeToComplete("stop");
```

s.prop1 legt vast hoeveel tijd nodig is om het aankoopproces te voltooien

### Voorbeeld 2

Als u verscheidene tijdopnemers wilt hebben die tezelfdertijd lopen (om verschillende processen te meten), zult u het cn koekjesargument manueel moeten plaatsen.  Als u bijvoorbeeld wilt meten hoeveel tijd een aankoop nodig heeft om te voltooien, stelt u de volgende code in...

```javascript
if(s.inList(s.events, "scCheckout")) s.getTimeToComplete("start", "gttcpurchase");
if(s.inList(s.events, "purchase")) s.prop1 = s.getTimeToComplete("start", "gttcpurchase");
```

...maar als u (tezelfdertijd) ook wilt meten hoeveel tijd nodig is om een registratieformulier in te vullen, zou u ook de volgende code uitvoeren:

```js
if(s.inList(s.events, "event1")) s.getTimeToComplete("start", "gttcregister", 7);
if(s.inList(s.events, "event2")) s.prop2 = s.getTimeToComplete("stop", "gttcregister", 7);
```

In het tweede voorbeeld is event1 bedoeld om het begin vast te leggen van een registratieproces dat tot 7 dagen kan duren om te voltooien, om welke reden dan ook, en event2 is bedoeld om de voltooiing van de registratie vast te leggen.  s.prop2 legt vast hoeveel tijd nodig is om het registratieproces te voltooien

## Versiehistorie

### 4.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 3.1 (30 september 2019)

* Toegevoegde logica die de waarde &quot;start&quot; of &quot;stop&quot; in het eerste argument vereist.  Met alle andere waarden die worden doorgegeven, wordt de insteekmodule niet uitgevoerd.
* `inList 2.0`-plug-in is bijgewerkt naar `inList 2.1`.

### 3.0 (23 augustus 2018)

* De `formatTime v1.0`-plug-in is bijgewerkt naar `formatTime v1.1`.

### 3.0 (17 april 2018)

* Puntrelease (opnieuw gecompileerd, kleiner codeformaat).
* Kleine correcties.

### (2 juni 2016)

* De afhankelijkheid van de `p_fo`-plug-in is verwijderd.
* Toegevoegde compatibiliteit met H-code en AppMeasurement.
* Logboekregistratie van toegevoegde console.
