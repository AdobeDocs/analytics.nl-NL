---
title: formatTime
description: Zet een aantal seconden in zijn equivalent in notulen, uren, enz. om.
exl-id: 4b98e7fe-f05b-4346-b284-697268adc1a2
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 0%

---

# Adobe-plug-in: formatTime

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `formatTime`-plug-in kunt u een willekeurig aantal seconden duren en deze presenteren in een gespikte indeling, afgerond op een gewenste benchmarkwaarde. Adobe raadt u aan deze plug-in te gebruiken als u een tijdswaarde in seconden wilt vastleggen en deze wilt omzetten in een bucket-indeling (zoals minuten, dagen of weken). Deze plug-in is niet nodig als u op de tweede computer gebaseerde waarden niet in een indeling met afgeronde tijd wilt plaatsen.

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
   * Type handeling: Initialize formatTime
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
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: formatTime v2.0 */
function formatTime(ns,tf,bml){var f=ns,d=tf,e=bml;function h(b,d,c,e){if("string"!==typeof d)return!1;if("string"===typeof b)b=b.split(c||",");else if("object"!==typeof b)return!1;c=0;for(a=b.length;c<a;c++)if(1==e&&d===b[c]||d.toLowerCase()===b[c].toLowerCase())return!0;return!1}if(arguments&&"-v"===arguments[0])return{plugin:"formatTime",version:"2.0"};var b=function(){if("undefined"!==typeof window.s_c_il)for(var b=0,c;b<window.s_c_il.length;b++)if(c=window.s_c_il[b],c._c&&"s_c"===c._c)return c}();"undefined"!==typeof b&&(b.contextData.formatTime="2.0");if(!("undefined"===typeof f||isNaN(f)||0>Number(f))){b="";if("string"===typeof d&&"d"===d||("string"!==typeof d||!h("h,m,s",d))&&86400<=f){var c=86400;var g="days";b=isNaN(e)?1:c/(e*c)}else"string"===typeof d&&"h"===d||("string"!==typeof d||!h("m,s",d))&&3600<=f?(c=3600,g="hours",b=isNaN(e)?4:c/(e*c)):"string"===typeof d&&"m"===d||("string"!==typeof d||!h("s",d))&&60<=f?(c=60,g="minutes",b=isNaN(e)?2:c/(e*c)):(c=1,g="seconds",b=isNaN(e)?.2:c/e);b=Math.round(f*b/c)/b+" "+g;0===b.indexOf("1 ")&&(b=b.substring(0,b.length-1));return b}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De methode `formatTime` gebruikt de volgende argumenten:

* **`ns`** (vereist, geheel getal): Het aantal seconden dat moet worden omgezet of geformatteerd
* **`tf`** (optioneel, tekenreeks): Het type indeling waarin de seconden moeten worden geretourneerd. is standaard ingesteld op seconden
   * Stel in op `"d"` als u de tijd in dagen wilt (standaard afgerond op de dichtstbijzijnde benchmark van 1/4 dagen).
   * Stel in op `"h"` als u de tijd in uren wilt (standaard afgerond op de dichtstbijzijnde benchmark van 1/4 uur).
   * Stel in op `"m"` als u de tijd in minuten wilt (standaard afgerond op de dichtstbijzijnde benchmark van 1/2 minuten).
   * Stel in op `"s"` als u de tijd in seconden wilt (standaard afgerond op de dichtstbijzijnde benchmark van 5 seconden).
* **`bml`** (optioneel, nummer): De lengte van de afrondingsbenchmarks. Standaardwaarden voor de benchmarks in het argument `tf`

De methode retourneert het aantal seconden dat is opgemaakt met de eenheid die u opgeeft in het argument `tf`. Als het argument `tf` niet is ingesteld:

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

...zal s.eVar1 gelijk aan &quot;10.75 uren&quot;plaatsen
Het argument dat wordt doorgegeven - 38250 seconden - is gelijk aan 10 uur, 37 minuten en 30 seconden.  Wanneer het aantal seconden wordt afgerond dat in dit geval aan de dichtstbijzijnde benchmark van het kwartuur wordt doorgegeven, wordt de eindwaarde ingesteld op 10,75 uur

### Voorbeeld 3

De volgende code...

```js
s.eVar1 = s.formatTime(38242, "m");
```

...zal s.eVar1 gelijk stellen aan &quot;637.5 minuten&quot;

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

...zal s.eVar1 gelijk stellen aan &quot;3 minuten&quot;, wat de dichtstbijzijnde 3-minieme benchmark aan 125 seconden is

### Voorbeeld 7

De volgende code...

```js
s.eVar1 = s.formatTime(145, "m", .4);
```

...zal s.eVar1 gelijk stellen aan &quot;2,4 minuten&quot;, de dichtstbijzijnde 2/5-minuten-benchmark (bv. .4 = 2/5) tot 145 seconden

## Versiehistorie

### 2.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 1.1 (21 mei 2018)

* Het argument `bml` is toegevoegd om meer flexibiliteit bij afronding mogelijk te maken

### 1.0 (15 april 2018)

* Eerste release.
