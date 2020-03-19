---
title: formatTime
description: Zet een aantal seconden in zijn equivalent in notulen, uren, enz. om.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe-insteekmodule: formatTime

> [!IMPORTANT] Deze plug-in wordt geleverd door Adobe Consulting als een hoffelijkheid om u te helpen meer waarde te krijgen van Adobe Analytics. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `formatTime` insteekmodule kunt u een willekeurig aantal seconden duren en deze presenteren in een gespikte indeling, afgerond naar een gewenste benchmarkwaarde. Adobe raadt u aan deze plug-in te gebruiken als u een tijdwaarde in seconden wilt vastleggen en deze wilt omzetten in een bucket-indeling (zoals minuten, dagen of weken). Deze plug-in is niet nodig als u op de tweede computer gebaseerde waarden niet in een indeling met afgeronde tijd wilt plaatsen.

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
   * Type handeling: Initialize formatTime
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
/* Adobe Consulting Plugin: formatTime v1.1 (Requires inList plug-in) */
s.formatTime=function(ns,tf,bml){var s=this;if(!("undefined"===typeof ns||isNaN(ns)||0>Number(ns))){if("string"===typeof tf&&"d"===tf||("string"!==typeof tf||!s.inList("h,m,s",tf))&&86400<=ns){tf=86400;var d="days";bml=isNaN(bml)?1:tf/(bml*tf)} else"string"===typeof tf&&"h"===tf||("string"!==typeof tf||!s.inList("m,s",tf))&&3600<=ns?(tf=3600,d="hours", bml=isNaN(bml)?4: tf/(bml*tf)):"string"===typeof tf&&"m"===tf||("string"!==typeof tf||!s.inList("s",tf))&&60<=ns?(tf=60,d="minutes",bml=isNaN(bml)?2: tf/(bml*tf)):(tf=1,d="seconds",bml=isNaN(bml)?.2:tf/bml);ns=Math.round(ns*bml/tf)/bml+" "+d;0===ns.indexOf("1 ")&&(ns=ns.substring(0, ns.length-1));return ns}};

/* Adobe Consulting Plugin: inList v2.1 */
s.inList=function(lv,vtc,d,cc){if("string"!==typeof vtc)return!1;if("string"===typeof lv)lv=lv.split(d||",");else if("object"!== typeof lv)return!1;d=0;for(var e=lv.length;d<e;d++)if(1==cc&&vtc===lv[d]||vtc.toLowerCase()===lv[d].toLowerCase())return!0;return!1};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `formatTime` methode gebruikt de volgende argumenten:

* **`ns`** (vereist, geheel getal): Het aantal seconden dat moet worden omgezet of geformatteerd
* **`tf`** (optioneel, tekenreeks): Het type indeling waarin de seconden moeten worden geretourneerd. is standaard ingesteld op seconden
   * Instellen op `"d"` als u de tijd in dagen wilt (standaard afgerond op de dichtstbijzijnde benchmark van 1/4 dagen)
   * Ingesteld op `"h"` als u de tijd in uren wilt (standaard afgerond op de dichtstbijzijnde benchmark van 1/4 uur)
   * Instellen op `"m"` als u de tijd in minuten wilt gebruiken (standaard afgerond op de dichtstbijzijnde benchmark van 1/2 minuten)
   * Ingesteld op `"s"` als u de tijd in seconden wilt (standaard afgerond op de dichtstbijzijnde benchmark van 5 seconden)
* **`bml`** (optioneel, nummer): De lengte van de afrondingsbenchmarks. Standaardwaarden voor de benchmarks die in het `tf` argument worden vermeld

De methode retourneert het aantal seconden dat is opgemaakt met de eenheid die u opgeeft in het `tf` argument. Als het `tf` argument niet is ingesteld:

* Iets minder dan een minuut wordt afgerond naar de dichtstbijzijnde benchmark van 5 seconden
* Alles tussen een minuut en een uur wordt afgerond naar de dichtstbijzijnde benchmark van 1/2 minuten
* Om het even wat tussen een uur en een dag wordt afgerond aan het dichtstbijzijnde kwartier benchmark
* Alles wat groter is dan een dag, wordt afgerond naar de dichtstbijzijnde benchmark voor de dag

## Voorbeelden

### Voorbeeld 1

De volgende code...

```js
s.eVar1 = s.formatTime(38242);
```

...zal s.eVar1 gelijk aan &quot;10.5 uren&quot;plaatsen

Het argument dat wordt doorgegeven - 38242 seconden - is gelijk aan 10 uur, 37 minuten en 22 seconden.  Aangezien het tf-argument niet in deze aanroep is ingesteld en het aantal seconden dat wordt doorgegeven tussen een uur en een dag ligt, retourneert de insteekmodule het aantal seconden dat naar de meest overeenkomende benchmark van een kwartier is geconverteerd.

### Voorbeeld 2

De volgende code...

```js
s.eVar1 = s.formatTime(38250);
```

...zal s.eVar1 gelijk aan &quot;10.75 uren&quot;Het argument overgegaan binnen - 38250 seconden - is gelijk aan 10 uren, 37 minuten, en 30 seconden.  Wanneer het aantal seconden wordt afgerond dat in dit geval aan de dichtstbijzijnde benchmark van het kwartuur wordt doorgegeven, wordt de eindwaarde ingesteld op 10,75 uur

### Voorbeeld 3

De volgende code...

```js
s.eVar1 = s.formatTime(38242, "m");
```

...zal s.eVar1 gelijk aan &quot;637.5 minuten&quot;plaatsen

In dit geval dwingt het argument &quot;m&quot; de plug-in de seconden om te zetten naar de dichtstbijzijnde benchmark van halve minuut

### Voorbeeld 4

De volgende code...

```js
s.eVar1 = s.formatTime(38242, "m", 20);
```

...zal s.eVar1 gelijk aan &quot;640 minuten&quot;plaatsen

Met de argumentwaarde tf (&quot;m&quot;) wordt de insteekmodule gedwongen de seconden in minuten om te zetten, maar met de argumentwaarde bml (20) wordt de insteekmodule ook gedwongen om de minuscule conversie naar de dichtstbijzijnde benchmark van 20 minuten af te ronden.

### Voorbeeld 5

De volgende code...

```js
s.eVar1 = s.formatTime(125, "s", 2);
```

...zal s.eVar1 gelijk aan &quot;126 seconden&quot;plaatsen, die het dichtst 2 tweede benchmark aan 125 seconden is

### Voorbeeld 6

De volgende code...

```js
s.eVar1 = s.formatTime(125, "m", 3);
```

...zal s.eVar1 gelijk aan &quot;3 minuten&quot;plaatsen, die het dichtst 3 minieme benchmark aan 125 seconden is

### Voorbeeld 7

De volgende code...

```js
s.eVar1 = s.formatTime(145, "m", .4);
```

...zal s.eVar1 gelijk stellen aan &quot;2.4 minuten&quot;, wat de dichtstbijzijnde 2/5-minute benchmark is (bijvoorbeeld .4 = 2/5) tot 145 seconden

## Versiehistorie

### 1.1 (21 mei 2018)

* Het `bml` argument toegevoegd om meer flexibiliteit bij afronding mogelijk te maken

### 1.0 (15 april 2018)

* Eerste release.
