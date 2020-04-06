---
title: inList
description: Controleer of een waarde is opgenomen in een andere door tekens gescheiden waarde.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Adobe-insteekmodule: inList

>[!IMPORTANT] Deze plug-in wordt geleverd door Adobe Consulting als een hoffelijkheid om u te helpen meer waarde te krijgen van Adobe Analytics. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `inList` insteekmodule kunt u controleren of er al een waarde bestaat binnen een tekenreeks met scheidingstekens of een JavaScript-arrayobject. Verschillende andere plug-ins zijn afhankelijk van de `inList` plug-in die u wilt gebruiken. Deze insteekmodule biedt een duidelijk voordeel ten opzichte van de JavaScript-methode `indexOf()` waarbij gedeeltelijke tekenreeksen niet overeenkomen. Als u deze plug-in bijvoorbeeld hebt gebruikt om te controleren `"event2"`of deze niet overeenkomt met een tekenreeks die `"event25"`deze plug-in bevat. Deze insteekmodule is niet nodig als u niet hoeft te controleren op waarden in afgebakende tekenreeksen of arrays, of als u uw eigen `indexOf()` logica wilt gebruiken.

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
   * Type handeling: Initialiseren inList
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
/* Adobe Consulting Plugin: inList v2.1 */
s.inList=function(lv,vtc,d,cc){if("string"!==typeof vtc)return!1;if("string"===typeof lv)lv=lv.split(d||",");else if("object"!== typeof lv)return!1;d=0;for(var e=lv.length;d<e;d++)if(1==cc&&vtc===lv[d]||vtc.toLowerCase()===lv[d].toLowerCase())return!0;return!1};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `inList` methode gebruikt de volgende argumenten:

* **`lv`** (vereist, tekenreeks of array): Een gescheiden lijst met waarden of een JavaScript-arrayobject dat moet worden doorzocht
* **`vtc`** (vereist, tekenreeks): De waarde waarnaar moet worden gezocht
* **`d`** (optioneel, tekenreeks): Het scheidingsteken dat wordt gebruikt voor het scheiden van afzonderlijke waarden in het `lv` argument. Heeft als standaardwaarde een komma (`,`).
* **`cc`** (optioneel, Booleaans): Indien ingesteld op `true`, wordt een hoofdlettergevoelige controle uitgevoerd. Indien ingesteld op `false` of weggelaten, wordt een niet-hoofdlettergevoelige controle uitgevoerd. Wordt standaard ingesteld op `false`.

Het roepen van deze methode keert terug `true` als het een gelijke vindt, en `false` als het geen gelijke vindt.

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

### Voorbeeld 2

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

...de voorwaardelijke if-instructie is false.  De waarde van het d-argument dat in de aanroep wordt doorgegeven (d.w.z. &quot;|&quot;) gaat ervan uit dat de individuele waarden in s.linkTrackVars worden afgebakend door een pipe-teken, terwijl de waarden in werkelijkheid door een komma worden afgebakend.  In dit geval probeert de plug-in een overeenkomst te maken tussen de gehele waarde van s.linkTrackVars (dat wil zeggen &quot;events,eVar1&quot;) en de waarde die moet worden gezocht (d.w.z. &quot;eVar1&quot;).

## Versiehistorie

### v2.1 (26 september 2019)

* De optie voor het `cc` argument is toegevoegd om geen booleaanse waarde te hebben. Dit `1` is bijvoorbeeld een geldige controlewaarde voor hoofdletters en kleine letters.

### v2.0 (17 april 2018)

* Puntrelease (opnieuw gecompileerd, kleiner codeformaat).

### v1.01 (27 september 2017)

* Geoptimaliseerde code om grootte te reduceren

### v1.0 (2009)

* Eerste release.


