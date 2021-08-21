---
title: getTimeBetweenEvents
description: Meet de hoeveelheid tijd tussen twee gebeurtenissen.
exl-id: 15887796-4fe4-4b3a-9a65-a4672c5ecb34
source-git-commit: ab078c5da7e0e38ab9f0f941b407cad0b42dd4d1
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 0%

---

# Adobe-plug-in: getTimeBetweenEvents

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `getTimeBetweenEvents`-plug-in kunt u bijhouden hoeveel tijd er is tussen twee Analytics-gebeurtenissen, zoals winkelwagentjes en aangepaste gebeurtenissen. Het is handig als u wilt bijhouden hoeveel tijd er nodig is om een afrekenproces te voltooien of om het even welk ander proces dat u tijd wilt meten. Deze insteekmodule is niet nodig als u geen conversieprocessen hebt die u wilt meten hoe lang het duurt.

## Plug-in installeren met tags in Adobe Experience Platform

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar het tabblad [!UICONTROL Extensions] en klik op de knop [!UICONTROL Catalog]
1. De extensie [!UICONTROL Common Analytics Plugins] installeren en publiceren
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: Geen
   * Gebeurtenis: Kern - Bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: Gebruikelijke plug-ins voor Analytics
   * Type handeling: getTimeBetweenEvents initialiseren
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met aangepaste code-editor

Als u de extensie van de plug-in niet wilt gebruiken, kunt u de aangepaste code-editor gebruiken.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder de uitbreiding van Adobe Analytics.
1. Breid [!UICONTROL Configure tracking using custom code] accordeon uit, die [!UICONTROL Open Editor] knoop openbaart.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

## Installeer de plug-in met AppMeasurement

Kopieer en plak de volgende code ergens in het AppMeasurement-bestand nadat het analytics tracking-object is geïnstantieerd (met [`s_gi`](../functions/s-gi.md)). Door opmerkingen en versienummers van de code in uw implementatie te behouden, kunt u Adobe doen met het oplossen van mogelijke problemen.

```js
/* Adobe Consulting Plugin: getTimeBetweenEvents v3.0 (AppMeasurement highly recommended) */
function getTimeBetweenEvents(ste,rt,stp,res,cn,etd,fmt,bml,rte){var v=ste,B=rt,x=stp,C=res,k=cn,m=etd,E=fmt,F=bml,p=rte;if("-v"===v)return{plugin:"getTimeBetweenEvents",version:"3.0"};var q=function(){if("undefined"!==typeof window.s_c_il)for(var c=0,b;c<window.s_c_il.length;c++)if(b=window.s_c_il[c],b._c&&"s_c"===b._c)return b}();if("undefined"!==typeof q&&(q.contextData.getTimeBetweenEvents="3.0",window.cookieWrite=window.cookieWrite||function(c,b,d){if("string"===typeof c){var n=window.location.hostname,f=window.location.hostname.split(".").length-1;if(n&&!/^[0-9.]+$/.test(n)){f=2<f?f:2;var l=n.lastIndexOf(".");if(0<=l){for(;0<=l&&1<f;)l=n.lastIndexOf(".",l-1),f--;l=0<l?n.substring(l):n}}g=l;b="undefined"!==typeof b?""+b:"";if(d||""===b)if(""===b&&(d=-60),"number"===typeof d){var e=new Date;e.setTime(e.getTime()+6E4*d)}else e=d;return c&&(document.cookie=encodeURIComponent(c)+"="+encodeURIComponent(b)+"; path=/;"+(d?" expires="+e.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof window.cookieRead)?window.cookieRead(c)===b:!1}},window.cookieRead=window.cookieRead||function(c){if("string"===typeof c)c=encodeURIComponent(c);else return"";var b=" "+document.cookie,d=b.indexOf(" "+c+"="),e=0>d?d:b.indexOf(";",d);return(c=0>d?"":decodeURIComponent(b.substring(d+2+c.length,0>e?b.length:e)))?c:""},window.formatTime=window.formatTime||function(c,b,d){function e(b,d,c,e){if("string"!==typeof d)return!1;if("string"===typeof b)b=b.split(c||",");else if("object"!==typeof b)return!1;c=0;for(a=b.length;c<a;c++)if(1==e&&d===b[c]||d.toLowerCase()===b[c].toLowerCase())return!0;return!1}if(!("undefined"===typeof c||isNaN(c)||0>Number(c))){var f="";"string"===typeof b&&"d"===b||("string"!==typeof b||!e("h,m,s",b))&&86400<=c?(b=86400,f="days",d=isNaN(d)?1:b/(d*b)):"string"===typeof b&&"h"===b||("string"!==typeof b||!e("m,s",b))&&3600<=c?(b=3600,f="hours",d=isNaN(d)?4:b/(d*b)):"string"===typeof b&&"m"===b||("string"!==typeof b||!e("s",b))&&60<=c?(b=60,f="minutes",d=isNaN(d)?2:b/(d*b)):(b=1,f="seconds",d=isNaN(d)?.2:b/d);f=Math.round(c*d/b)/d+" "+f;0===f.indexOf("1 ")&&(f=f.substring(0,f.length-1));return f}},window.inList=window.inList||function(c,b,d,e){if("string"!==typeof b)return!1;if("string"===typeof c)c=c.split(d||",");else if("object"!==typeof c)return!1;d=0;for(a=c.length;d<a;d++)if(1==e&&b===c[d]||b.toLowerCase()===c[d].toLowerCase())return!0;return!1},"string"===typeof v&&"undefined"!==typeof B&&"string"===typeof x&&"undefined"!==typeof C)){k=k?k:"s_tbe";m=isNaN(m)?1:Number(m);var r=!1,t=!1,y=v.split(","),z=x.split(",");p=p?p.split(","):[];for(var u=window.cookieRead(k),w,D=new Date,A=D.getTime(),h=new Date,e=0;e<p.length;++e)if(window.inList(q.events,p[e])){h.setDate(h.getDate()-1);window.cookieWrite(k,"",h);return}h.setTime(h.getTime()+864E5*m);for(e=0;e<y.length&&!r&&(r=window.inList(q.events,y[e]),!0!==r);++e);for(e=0;e<z.length&&!t&&(t=window.inList(q.events,z[e]),!0!==t);++e);1===y.length&&1===z.length&&v===x&&r&&t?(u&&(w=(A-u)/1E3),window.cookieWrite(k,A,m?h:0)):(!r||1!=B&&u||window.cookieWrite(k,A,m?h:0),t&&u&&(w=(D.getTime()-u)/1E3,!0===C&&(h.setDate(h.getDate()-1),window.cookieWrite(k,"",h))));return w?window.formatTime(w,E,F):""}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De functie `getTimeBetweenEvents` gebruikt de volgende argumenten:

* **`ste`** (vereist, tekenreeks): Start timergebeurtenissen. Een door komma&#39;s gescheiden tekenreeks van Analytics-gebeurtenissen naar &quot;start de timer&quot;.
* **`rt`** (vereist, Booleaans): Optie timer opnieuw starten. Stel in op `true` als u de timer opnieuw wilt starten telkens wanneer de variabele `events` een gebeurtenis start timer bevat. Stel de waarde in op `false` als u niet wilt dat de timer opnieuw wordt gestart wanneer er een gebeurtenis start timer wordt weergegeven.
* **`stp`** (vereist, tekenreeks): Stop timergebeurtenissen. Een door komma&#39;s gescheiden tekenreeks van Analytics-gebeurtenissen die de timer &#39;stoppen&#39;.
* **`res`** (vereist, Booleaans): Optie timer opnieuw instellen. Stel de waarde in op `true` als u de tijd wilt opnemen sinds de timer is gestart EN de timer opnieuw wilt instellen nadat deze is gestopt. Stel in op `false` als u de tijd wilt opnemen, maar de timer niet wilt stoppen. Indien ingesteld op `false`, blijft de timer actief nadat de gebeurtenisvariabele een stopgebeurtenis vastlegt.

   >[!TIP]
   >
   >Als u dit argument op `false` plaatst, wordt het plaatsen van `rte` hieronder argument hoogst geadviseerd.
* **`cn`** (optioneel, tekenreeks): De cookienaam waar de tijd van de eerste gebeurtenis wordt opgeslagen. Wordt standaard ingesteld op `"s_tbe"`.
* **`etd`** (optioneel, geheel getal): De vervaltijd voor de cookie in dagen. Stel in op `0` om te verlopen aan het einde van de browsersessie. Wordt standaard ingesteld op 1 dag.
* **`fmt`** (optioneel, tekenreeks): De notatie van de tijd waarin het aantal seconden wordt geretourneerd (standaardinstellingen op niets)
   * `"s"` voor seconden
   * `"m"` voor minuten
   * `"h"` voor uren
   * `"d"` dagen
   * Wanneer niet geplaatst, is het formaat van de terugkeerwaarde gebaseerd op de volgende regels:
      * Iets minder dan een minuut wordt afgerond naar de dichtstbijzijnde benchmark van 5 seconden. Bijvoorbeeld, 10 seconden, 15 seconden
      * Alles tussen een minuut en een uur wordt afgerond naar de dichtstbijzijnde benchmark van 1/2 minuten. Bijvoorbeeld 30,5 minuten, 31 minuten
      * Om het even wat tussen een uur en een dag wordt afgerond aan het dichtstbijzijnde kwartier benchmark. Bijvoorbeeld 2,25 uur, 3,5 uur
      * Alles wat groter is dan een dag, wordt afgerond naar de dichtstbijzijnde benchmark voor de dag. Bijvoorbeeld 1 dagen, 3 dagen, 9 dagen
* **`bml`** (optioneel, nummer): De lengte van de afrondingsbenchmark volgens de vorm van het  `fmt` argument. Als het argument `fmt` bijvoorbeeld `"s"` is en dit argument `2` is, wordt de geretourneerde waarde afgerond naar de dichtstbijzijnde benchmark van 2 seconden. Als `fmt` argument `"m"` is en dit argument `0.5` is, wordt de terugkeerwaarde afgerond aan de dichtstbijzijnde half-minieme benchmark.
* **`rte`** (optioneel, tekenreeks): Door komma&#39;s gescheiden tekenreeks van gebeurtenissen Analytics die de timer verwijderen of verwijderen. Heeft als standaardwaarde niets.

Als deze functie wordt aangeroepen, wordt een geheel getal geretourneerd dat de hoeveelheid tijd vertegenwoordigt tussen de gebeurtenis start timer en de gebeurtenis stop timer in de gewenste indeling.

## Voorbeelden van aanroepen

```js
// The timer starts or restarts when the events variable contains event1
// The timer stops and resets when the events variable contains event2
// The timer resets when the events variable contains event3 or the visitor closes their browser
// Sets eVar1 to the number of seconds between event1 and event2, rounded to the nearest 2-second benchmark
s.eVar1 = getTimeBetweenEvents("event1", true, "event2", true, "", 0, "s", 2, "event3");

// The timer starts when the events variable contains event1. It does NOT restart with subsequent hits that also contain event1
// The timer records a "lap" when the events variable contains event2. It does not stop the timer.
// The timer resets when the events variable contains event3 or if more than 20 days pass since the timer started
// The timer is stored in a cookie labeled "s_20"
// Sets eVar4 to the number of hours between event1 and event2, rounded to the nearest 90-minute benchmark
s.eVar4 = getTimeBetweenEvents("event1", false, "event2", false, "s_20", 20, "h", 1.5, "event3");

// Similar to the above timer in eVar4, except the return value is returned in seconds/minutes/hours/days depending on the timer length.
// The timer expires after 1 day.
s.eVar4 = getTimeBetweenEvents("event1", true, "event2", true);
```

## Versiehistorie

### 3.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 2.1 (26 mei 2018)

* Hiermee past u de wijzigingen toe die zijn aangebracht in de nieuwe versie van de `formatTime`-plug-in.

### 2.0 (6 april 2018)

* Volledige herschrijven/opnieuw analyseren van plug-in.
