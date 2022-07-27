---
title: formatTime
description: Zet een aantal seconden in zijn equivalent in notulen, uren, enz. om.
feature: Variables
exl-id: 4b98e7fe-f05b-4346-b284-697268adc1a2
source-git-commit: 7c7a7d8add9edb1538df12b440bc0a15f09efe5e
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# Adobe-plug-in: formatTime

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

De `formatTime` Met de insteekmodule kunt u een willekeurig aantal seconden duren en deze presenteren in een gespikte indeling, afgerond naar een gewenste benchmarkwaarde. Adobe raadt u aan deze plug-in te gebruiken als u een tijdswaarde in seconden wilt vastleggen en deze wilt omzetten in een bucket-indeling (zoals minuten, dagen of weken). Deze plug-in is niet nodig als u op de tweede computer gebaseerde waarden niet in een indeling met afgeronde tijd wilt plaatsen.

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
    * Action Type: Initialize formatTime
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
/* Adobe Consulting Plugin: formatTime v2.0 */
function formatTime(ns,tf,bml){var f=ns,d=tf,e=bml;function h(b,d,c,e){if("string"!==typeof d)return!1;if("string"===typeof b)b=b.split(c||",");else if("object"!==typeof b)return!1;c=0;for(a=b.length;c<a;c++)if(1==e&&d===b[c]||d.toLowerCase()===b[c].toLowerCase())return!0;return!1}if(arguments&&"-v"===arguments[0])return{plugin:"formatTime",version:"2.0"};var b=function(){if("undefined"!==typeof window.s_c_il)for(var b=0,c;b<window.s_c_il.length;b++)if(c=window.s_c_il[b],c._c&&"s_c"===c._c)return c}();"undefined"!==typeof b&&(b.contextData.formatTime="2.0");if(!("undefined"===typeof f||isNaN(f)||0>Number(f))){b="";if("string"===typeof d&&"d"===d||("string"!==typeof d||!h("h,m,s",d))&&86400<=f){var c=86400;var g="days";b=isNaN(e)?1:c/(e*c)}else"string"===typeof d&&"h"===d||("string"!==typeof d||!h("m,s",d))&&3600<=f?(c=3600,g="hours",b=isNaN(e)?4:c/(e*c)):"string"===typeof d&&"m"===d||("string"!==typeof d||!h("s",d))&&60<=f?(c=60,g="minutes",b=isNaN(e)?2:c/(e*c)):(c=1,g="seconds",b=isNaN(e)?.2:c/e);b=Math.round(f*b/c)/b+" "+g;0===b.indexOf("1 ")&&(b=b.substring(0,b.length-1));return b}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `formatTime` function gebruikt de volgende argumenten:

* **`ns`** (vereist, geheel getal): Het aantal seconden dat moet worden omgezet of geformatteerd
* **`tf`** (optioneel, tekenreeks): Het type indeling waarin de seconden moeten worden geretourneerd. is standaard ingesteld op seconden
   * Instellen op `"d"` als u de tijd in dagen wilt (standaard afgerond op de dichtstbijzijnde benchmark van 1/4 dagen)
   * Instellen op `"h"` als u de tijd in uren wilt (standaard afgerond op de dichtstbijzijnde benchmark van 1/4 uur)
   * Instellen op `"m"` als u de tijd in minuten wilt (standaard afgerond op de dichtstbijzijnde benchmark van 1/2 minuten)
   * Instellen op `"s"` als u de tijd in seconden wilt (standaard afgerond op de dichtstbijzijnde benchmark van 5 seconden)
* **`bml`** (optioneel, nummer): De lengte van de afrondingsbenchmarks. Standaardwaarden van de benchmarks die zijn opgenomen in de `tf` argument

De functie retourneert het aantal seconden dat wordt opgemaakt met de eenheid die u opgeeft in het dialoogvenster `tf` argument. Als de `tf` argument is niet ingesteld:

* Iets minder dan een minuut wordt afgerond naar de dichtstbijzijnde benchmark van 5 seconden
* Alles tussen een minuut en een uur wordt afgerond naar de dichtstbijzijnde benchmark van 1/2 minuten
* Om het even wat tussen een uur en een dag wordt afgerond aan het dichtstbijzijnde kwartier benchmark
* Alles wat groter is dan een dag, wordt afgerond naar de dichtstbijzijnde benchmark voor de dag

## Voorbeelden

```js
// Sets eVar1 to "10.5 hours".
// 38242 seconds equals 10 hours, 37 minutes, and 22 seconds. Since the tf argument is not set, the value returned is the number of seconds converted to the nearest quarter-hour benchmark.
s.eVar1 = formatTime(38242);

// Sets eVar4 to "10.75 hours".
// 38250 seconds equals 10 hours, 37 minutes, and 30 seconds. This value rounds up to the nearest quarter hour.
s.eVar4 = formatTime(38250);

// Sets eVar9 to "637.5 minutes".
s.eVar9 = formatTime(38242, "m");

// Sets eVar14 to "640 minutes".
// The tf argument forces the returned value to minutes, while the bml argument forces the value to the nearest 20-minute increment.
s.eVar14 = formatTime(38242, "m", 20);

// Sets eVar2 to "126 seconds", the closest 2-second benchmark to 125 seconds.
s.eVar2 = formatTime(125, "s", 2);

// Sets eVar7 to "3 minutes", the closest 3-minute benchmark to 125 seconds.
s.eVar7 = formatTime(125, "m", 3);

// Sets eVar55 to "2.4 minutes, the closest 2/5-minute benchmark to 145 seconds.
s.eVar55 = formatTime(145, "m", .4);
```

## Versiehistorie

### 2.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 1.1 (21 mei 2018)

* De `bml` argument om meer flexibiliteit bij afronding mogelijk te maken

### 1.0 (15 april 2018)

* Eerste release.
