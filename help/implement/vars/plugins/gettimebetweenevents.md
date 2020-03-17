---
title: getTimeBetweenEvents
description: Meet de hoeveelheid tijd tussen twee gebeurtenissen.
translation-type: tm+mt
source-git-commit: 180ad544541f25d02b3a257559bc045abed7387b

---


# Adobe-insteekmodule: getTimeBetweenEvents

> [!IMPORTANT] Deze plug-in wordt geleverd door Adobe Consulting als een hoffelijkheid om u te helpen meer waarde te krijgen van Adobe Analytics. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `getTimeBetweenEvents` insteekmodule kunt u bijhouden hoeveel tijd er is tussen twee Analytics-gebeurtenissen, zoals winkelwagentjes en aangepaste gebeurtenissen. Het is handig als u wilt bijhouden hoeveel tijd er nodig is om een afrekenproces te voltooien of om het even welk ander proces dat u tijd wilt meten. Deze insteekmodule is niet nodig als u geen conversieprocessen hebt die u wilt meten hoe lang het duurt.

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
   * Type handeling: getTimeBetweenEvents initialiseren
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

Kopieer en plak de volgende code ergens in het AppMeasurement-bestand nadat het analytics tracking-object is geïnstantieerd (met `s_gi`). Door opmerkingen en versienummers van de code in uw implementatie te behouden, kan Adobe eventuele problemen oplossen.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getTimeBetweenEvents v2.1 (Requires formatTime and inList plug-ins) */
s.getTimeBetweenEvents=function(ste,rt,stp,res,cn,etd,fmt,bml,rte){var s=this;if("string"===typeof ste&&"undefined"!==typeof rt&&"string"===typeof stp&&"undefined"!==typeof res){cn=cn?cn:"s_tbe";etd=isNaN(etd)?1:Number(etd);var f=!1,g=!1,n=!1, p=ste.split(","),q=stp.split(",");rte=rte?rte.split(","):[];for(var h=s.c_r(cn),k,v=new Date,r=v.getTime(),c=new Date,a=0; a<rte.length;++a)s.inList(s.events,rte[a])&&(n=!0);c.setTime(c.getTime()+864E5*etd);for(a=0;a<p.length&&!f&&(f=s.inList(s.events,p[a]),!0!==f);++a);for(a=0;a<q.length&&!g&&(g=s.inList(s.events,q[a]),!0!==g);++a);1===p.length&&1===q.length&&ste===stp&&f&&g?(h&&(k=(r-h)/1E3),s.c_w(cn,r,etd?c:0)):(!f||1!=rt&&h||s.c_w(cn,r,etd?c:0),g&&h&&(k=(v.getTime()-h)/1E3,!0===res&&(n=!0)));!0===n&&(c.setDate( c.getDate()-1),s.c_w(cn,"",c));return k?s.formatTime(k,fmt,bml):""}};

/* Adobe Consulting Plugin: formatTime v1.1 (Requires inList plug-in) */
s.formatTime=function(ns,tf,bml){var s=this;if(!("undefined"===typeof ns||isNaN(ns)||0>Number(ns))){if("string"===typeof tf&&"d"===tf||("string"!==typeof tf||!s.inList("h,m,s",tf))&&86400<=ns){tf=86400;var d="days";bml=isNaN(bml)?1:tf/(bml*tf)} else"string"===typeof tf&&"h"===tf||("string"!==typeof tf||!s.inList("m,s",tf))&&3600<=ns?(tf=3600,d="hours", bml=isNaN(bml)?4: tf/(bml*tf)):"string"===typeof tf&&"m"===tf||("string"!==typeof tf||!s.inList("s",tf))&&60<=ns?(tf=60,d="minutes",bml=isNaN(bml)?2: tf/(bml*tf)):(tf=1,d="seconds",bml=isNaN(bml)?.2:tf/bml);ns=Math.round(ns*bml/tf)/bml+" "+d;0===ns.indexOf("1 ")&&(ns=ns.substring(0,ns.length-1));return ns}};

/* Adobe Consulting Plugin: inList v2.1 */
s.inList=function(lv,vtc,d,cc){if("string"!==typeof vtc)return!1;if("string"===typeof lv)lv=lv.split(d||",");else if("object"!== typeof lv)return!1;d=0;for(var e=lv.length;d<e;d++)if(1==cc&&vtc===lv[d]||vtc.toLowerCase()===lv[d].toLowerCase())return!0;return!1};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `getTimeBetweenEvents` methode gebruikt de volgende argumenten:

* **`ste`** (vereist, tekenreeks): Start timergebeurtenissen. Een door komma&#39;s gescheiden tekenreeks van Analytics-gebeurtenissen naar &quot;start de timer&quot;.
* **`rt`** (vereist, Booleaans): Optie timer opnieuw starten. Stel deze optie in op `true` als u de timer opnieuw wilt starten telkens wanneer de `events` variabele een gebeurtenis start timer bevat. Stel deze optie in op `false` als u niet wilt dat de timer opnieuw wordt gestart wanneer er een gebeurtenis start timer wordt weergegeven.
* **`stp`** (vereist, tekenreeks): Stop timergebeurtenissen. Een door komma&#39;s gescheiden tekenreeks van Analytics-gebeurtenissen die de timer &#39;stoppen&#39;.
* **`res`** (vereist, Booleaans): Optie timer opnieuw instellen. Stel deze optie in op `true` als u de tijd wilt opnemen sinds de timer is gestart EN de timer opnieuw wilt instellen nadat deze is gestopt. Stel deze optie in op `false` als u de tijd wilt opnemen, maar de timer niet wilt stoppen. Indien ingesteld op `false`, blijft de timer actief nadat de gebeurtenisvariabele een stopgebeurtenis vastlegt.
   > [!TIP] Als u dit argument instelt op `false`, wordt het sterk aanbevolen het `rte` argument hieronder in te stellen.
* **`cn`** (optioneel, tekenreeks): De cookienaam waar de tijd van de eerste gebeurtenis wordt opgeslagen. Wordt standaard ingesteld op `"s_tbe"`.
* **`etd`** (optioneel, geheel getal): De vervaltijd voor de cookie in dagen. Stel in op verlopen aan het einde van de browsersessie. `0` Wordt standaard ingesteld op 1 dag.
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
* **`bml`** (optioneel, nummer): De lengte van de afrondingsbenchmark volgens de vorm van het `fmt` argument. Als het `fmt` argument bijvoorbeeld is `"s"` en dit argument is `2`, wordt de geretourneerde waarde afgerond naar de dichtstbijzijnde 2-secondenbenchmark. Als `fmt` argument `"m"` en dit argument is `0.5`, wordt de geretourneerde waarde afgerond naar de dichtstbijzijnde halftijdse benchmark.
* **`rte`** (optioneel, tekenreeks): Door komma&#39;s gescheiden tekenreeks van gebeurtenissen Analytics die de timer verwijderen of verwijderen. Heeft als standaardwaarde niets.

Wanneer deze methode wordt aangeroepen, wordt een geheel getal geretourneerd dat de hoeveelheid tijd vertegenwoordigt tussen de gebeurtenis start timer en de gebeurtenis stop timer in de gewenste indeling.

## Voorbeelden van aanroepen

### Voorbeeld 1

De volgende code...

```js
s.eVar1 = s.getTimeBetweenEvents("event1", true, "event2", true, "", 0, "s", 2, "event3");
```

...functioneert als volgt:

* De timer start wanneer s.events event1 bevat.
* De timer wordt telkens opnieuw gestart wanneer s.events event1 bevat
* De timer stopt wanneer s.events event2 bevat
* De timer wordt opnieuw ingesteld (d.w.z. gaat naar 0 seconden) telkens wanneer s.events event2 bevat
* De timer wordt ook opnieuw ingesteld wanneer s.events gebeurtenis3 OF bevat wanneer de bezoeker zijn/haar browser sluit
* Wanneer een werkelijke tijd tussen event1 en event2 wordt geregistreerd, stelt de plug-in eVar1 in op het aantal seconden tussen de twee gebeurtenissen die worden ingesteld, afgerond op de dichtstbijzijnde 2-secondenstandaard (bijvoorbeeld 0 seconden, 2 seconden, 4 seconden, 10 seconden, 184 seconden enz.)
* Als s.events event2 bevat voordat een timer is gestart, wordt eVar1 helemaal niet ingesteld.

### Voorbeeld 2

De volgende code...

```js
s.eVar1 = s.getTimeBetweenEvents("event1", false, "event2", false, "s_20", 20, "h", 1.5, "event3");
```

...functioneert als volgt:

* De timer start wanneer s.events event1 bevat.
* De timer wordt NIET telkens opnieuw gestart als s.events event1 bevat, maar de oorspronkelijke timer blijft actief
* De timer stopt NIET wanneer s.events event2 bevat, maar de insteekmodule neemt de tijd op sinds de oorspronkelijke gebeurtenis1-instelling is opgenomen
* De timer wordt opgeslagen in een cookie met de naam &quot;s_20&quot;
* De timer wordt alleen opnieuw ingesteld wanneer s.events event3 OF bevat wanneer 20 dagen zijn verstreken sinds de timer is gestart
* Wanneer een tijd tussen (de originele) gebeurtenis1 en event2 wordt geregistreerd, stelt de plug-in eVar1 in op het aantal uren tussen de twee gebeurtenissen die worden ingesteld, afgerond naar de dichtstbijzijnde benchmark van 1/2 uur (bijvoorbeeld 0 uur, 1,5 uur, 3 uur, 7,5 uur, 478,5 uur enz.)

### Voorbeeld 3

De volgende code...

```js
s.eVar1 = s.getTimeBetweenEvents("event1", true, "event2", true);
```

...vergelijkbare resultaten zal opleveren als in het eerste bovenstaande voorbeeld; de waarde van eVar1 wordt echter geretourneerd in seconden, minuten, uren of dagen, afhankelijk van de uiteindelijke lengte van de timer.  De timer verloopt ook 1 dag nadat deze voor het eerst is ingesteld in plaats van op het moment dat de bezoeker de browser sluit.

## Versiehistorie

### 2.1 (26 mei 2018)

* Hiermee past u de wijzigingen toe die in de nieuwe versie van de `formatTime` plug-in zijn aangebracht.

### 2.0 (6 april 2018)

* Volledige herschrijven/opnieuw analyseren van plug-in.
