---
title: inList
description: Controleer of een waarde is opgenomen in een andere door tekens gescheiden waarde.
exl-id: 7eedfd01-2b9a-4fae-a35b-433ca6900f27
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# Adobe-plug-in: inList

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de insteekmodule `inList` kunt u controleren of er al een waarde bestaat binnen een tekenreeks met scheidingstekens of een JavaScript-arrayobject. Verschillende andere plug-ins zijn afhankelijk van de `inList` plug-in om te werken. Deze insteekmodule biedt een duidelijk voordeel ten opzichte van de JavaScript-methode `indexOf()`, waarbij gedeeltelijke tekenreeksen niet overeenkomen. Als u deze insteekmodule bijvoorbeeld hebt gebruikt om te controleren op `"event2"`, komt deze niet overeen met een tekenreeks die `"event25"` bevat. Deze insteekmodule is niet nodig als u niet hoeft te controleren op waarden in afgebakende tekenreeksen of arrays, of als u uw eigen `indexOf()` logica wilt gebruiken.

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
   * Type handeling: Initialiseren inList
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
/* Adobe Consulting Plugin: inList v3.0 */
function inList(lv,vtc,d,cc){var b=lv,e=vtc,c=d,f=cc;if("-v"===b)return{plugin:"inList",version:"3.0"};a:{if("undefined"!==typeof window.s_c_il){var a=0;for(var d;a<window.s_c_il.length;a++)if(d=window.s_c_il[a],d._c&&"s_c"===d._c){a=d;break a}}a=void 0}"undefined"!==typeof a&&(a.contextData.inList="3.0");if("string"!==typeof e)return!1;if("string"===typeof b)b=b.split(c||",");else if("object"!==typeof b)return!1;c=0;for(a=b.length;c<a;c++)if(1==f&&e===b[c]||e.toLowerCase()===b[c].toLowerCase())return!0;return!1};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De methode `inList` gebruikt de volgende argumenten:

* **`lv`** (vereist, tekenreeks of array): Een gescheiden lijst met waarden of een JavaScript-arrayobject dat moet worden doorzocht
* **`vtc`** (vereist, tekenreeks): De waarde waarnaar moet worden gezocht
* **`d`** (optioneel, tekenreeks): Het scheidingsteken dat wordt gebruikt voor het scheiden van afzonderlijke waarden in het  `lv` argument. Heeft als standaardwaarde een komma (`,`).
* **`cc`** (optioneel, Booleaans): Indien ingesteld op  `true`, wordt een hoofdlettergevoelige controle uitgevoerd. Indien ingesteld op `false` of weggelaten, wordt een niet-hoofdlettergevoelige controle uitgevoerd. Wordt standaard ingesteld op `false`.

Als deze methode wordt aangeroepen, wordt `true` geretourneerd als er een overeenkomst wordt gevonden en `false` als er geen overeenkomst wordt gevonden.

## Voorbeelden van aanroepen

### Voorbeeld 1

Indien...

```js
s.events="event22,event24";
```

...en de volgende code wordt uitgevoerd...

```js
if(s.inList(s.events,"event22"))
```

...de voorwaardelijke if-instructie is waar

### Voorbeeld 3

Indien...

```js
s.events="event22,event24";
```

...en de volgende code wordt uitgevoerd...

```js
if(s.inList(s.events,"event2"))
```

...de voorwaardelijke if-instructie is false omdat de inList-aanroep geen exacte overeenkomst heeft gemaakt tussen event2 en een van de gescheiden waarden in s.events

### Voorbeeld 3

Indien...

```js
s.events="event22,event24";
```

...en de volgende code wordt uitgevoerd...

```js
if(!s.inList(s.events,"event23"))
```

...de voorwaardelijke if-instructie is waar omdat de aanroep inList geen exacte overeenkomst heeft gemaakt tussen event23 en een van de gescheiden-waarden in s.events (let op de operator &quot;NOT&quot; aan het begin van de aanroep van de variabele inList).

### Voorbeeld 4

Indien...

```js
s.events = "event22,event23";
```

...en de volgende code wordt uitgevoerd...

```js
if(s.inList(s.events,"EVenT23","",1))
```

...de voorwaardelijke if-instructie is false.  Hoewel dit voorbeeld niet praktisch is, toont het de behoefte aan gebruiksvoorzichtigheid wanneer het gebruiken van de case gevoelige vlag aan.

### Voorbeeld 5

Indien...

```js
s.linkTrackVars = "events,eVar1";
```

...en de volgende code wordt uitgevoerd...

```js
if(s.inList(s.linkTrackVars,"eVar1","|"))
```

...de voorwaardelijke if-instructie is false.  De waarde van het d-argument dat in de aanroep wordt doorgegeven (d.w.z. &quot;|&quot;) gaat ervan uit dat de individuele waarden in s.linkTrackVars worden afgebakend door een pipe-teken, terwijl de waarden in werkelijkheid door een komma worden afgebakend.  In dit geval probeert de plug-in een overeenkomst te maken tussen de gehele waarde van s.linkTrackVars (dat wil zeggen &quot;events,eVar1&quot;) en de waarde waarnaar moet worden gezocht (d.w.z. &quot;eVar1&quot;).

## Versiehistorie

### 3.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### v2.1 (26 september 2019)

* Optie voor argument `cc` toegevoegd om geen booleaanse waarde te zijn. `1` is bijvoorbeeld een geldige controlewaarde voor hoofdletters en kleine letters.

### v2.0 (17 april 2018)

* Puntrelease (opnieuw gecompileerd, kleiner codeformaat).

### v1.01 (27 september 2017)

* Geoptimaliseerde code om grootte te reduceren

### v1.0 (2009)

* Eerste release.
