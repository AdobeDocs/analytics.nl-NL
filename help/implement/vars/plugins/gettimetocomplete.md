---
title: getTimeToComplete
description: Meet de tijd die u nodig hebt om een taak te voltooien.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe-insteekmodule: getTimeToComplete

> [!IMPORTANT] Deze plug-in wordt geleverd door Adobe Consulting als een hoffelijkheid om u te helpen meer waarde te krijgen van Adobe Analytics. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `getTimeToComplete` insteekmodule wordt bijgehouden hoeveel tijd een gebruiker nodig heeft om een proces op een site te voltooien. De klok begint wanneer de `start` handeling wordt aangeroepen en eindigt wanneer de `stop` handeling wordt aangeroepen. Adobe raadt u aan deze plug-in te gebruiken als er een workflow op de site is die enige tijd in beslag neemt en u wilt weten hoeveel tijd bezoekers nodig hebben om deze te voltooien. Het is niet nodig deze plug-in te gebruiken als de workflow op uw site een korte periode (minder dan 3 seconden) in beslag neemt omdat de granulariteit slechts tot de volledige seconde is.

## De plug-in installeren met de Adobe Experience Platform Launch-extensie

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Go to the [!UICONTROL Extensions] tab, then click on the [!UICONTROL Catalog] button
1. De [!UICONTROL Common Analytics Plugins] extensie installeren en publiceren
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: Geen
   * Gebeurtenis: Kern - Bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: Gebruikelijke plug-ins voor Analytics
   * Type handeling: getTimeToComplete initialiseren
1. Sla de wijzigingen in de regel op en publiceer deze.

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
/* Adobe Consulting Plugin: getTimeToComplete v3.1 (Requires formatTime and inList plug-ins) */
s.getTimeToComplete=function(sos,cn,exp){sos=sos?sos.toLowerCase():"start";if("stop"===sos||"start"===sos){cn=cn?cn:"s_gttc";exp=exp?exp:0;var s=this,d=s.c_r(cn),e=new Date;if("start"===sos&&!d)s.c_w(cn,e.getTime(),exp?new Date(e.getTime()+864E5*exp):0);else if("stop"===sos&&d)return sos=Math.round((e.getTime()-d)/1E3),s.c_w(cn,"",0),s.formatTime(sos)}};

/* Adobe Consulting Plugin: formatTime v1.1 (Requires inList plug-in) */
s.formatTime=function(ns,tf,bml){var s=this;if(!("undefined"===typeof ns||isNaN(ns)||0>Number(ns))){if("string"===typeof tf&&"d"===tf||("string"!==typeof tf||!s.inList("h,m,s",tf))&&86400<=ns){tf=86400;var d="days";bml=isNaN(bml)?1:tf/(bml*tf)} else"string"===typeof tf&&"h"===tf||("string"!==typeof tf||!s.inList("m,s",tf))&&3600<=ns?(tf=3600,d="hours", bml=isNaN(bml)?4: tf/(bml*tf)):"string"===typeof tf&&"m"===tf||("string"!==typeof tf||!s.inList("s",tf))&&60<=ns?(tf=60,d="minutes",bml=isNaN(bml)?2: tf/(bml*tf)):(tf=1,d="seconds",bml=isNaN(bml)?.2:tf/bml);ns=Math.round(ns*bml/tf)/bml+" "+d;0===ns.indexOf("1 ")&&(ns=ns.substring(0,ns.length-1));return ns}};

/* Adobe Consulting Plugin: inList v2.1 */
s.inList=function(lv,vtc,d,cc){if("string"!==typeof vtc)return!1;if("string"===typeof lv)lv=lv.split(d||",");else if("object"!== typeof lv)return!1;d=0;for(var e=lv.length;d<e;d++)if(1==cc&&vtc===lv[d]||vtc.toLowerCase()===lv[d].toLowerCase())return!0;return!1};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `getTimeToComplete` methode gebruikt de volgende argumenten:

* **`sos`** (optioneel, tekenreeks): Instellen op `"start"` wanneer u de timer wilt starten. Instellen op `"stop"` wanneer u de timer wilt stoppen. Wordt standaard ingesteld op `"start"`.
* **`cn`** (optioneel, tekenreeks): De naam van het cookie waarin de begintijd wordt opgeslagen. Wordt standaard ingesteld op `"s_gttc"`.
* **`exp`** (optioneel, geheel getal): Het aantal dagen dat de cookie (en timer) verloopt. De standaardwaarde is `0`, die staat voor het einde van de browsersessie.

Het roepen van deze methode keert een koord terug dat het aantal dagen, uren, notulen en/of seconden bevat het tussen de `"start"` en `"stop"` actie nam.

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

### 3.1 (30 september 2019)

* Toegevoegde logica die de waarde &quot;start&quot; of &quot;stop&quot; in het eerste argument vereist.  Met alle andere waarden die worden doorgegeven, wordt de insteekmodule niet uitgevoerd.
* Bijgewerkte `inList 2.0` plug-in naar `inList 2.1`.

### 3.0 (23 augustus 2018)

* De plug-in is bijgewerkt naar `formatTime v1.0` `formatTime v1.1`.

### 3.0 (17 april 2018)

* Puntrelease (opnieuw gecompileerd, kleiner codeformaat).
* Kleine correcties.

### (2 juni 2016)

* De afhankelijkheid van de `p_fo` plug-in is verwijderd.
* Toegevoegde compatibiliteit met H-code en AppMeasurement.
* Logboekregistratie van toegevoegde console.
