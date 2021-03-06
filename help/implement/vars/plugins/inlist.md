---
title: inList
description: Controleer of een waarde is opgenomen in een andere door tekens gescheiden waarde.
feature: Variables
exl-id: 7eedfd01-2b9a-4fae-a35b-433ca6900f27
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 0%

---

# Adobe-plug-in: inList

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

De `inList` kunt u controleren of er al een waarde bestaat binnen een afgebakende tekenreeks of een JavaScript-arrayobject. Verschillende andere plug-ins zijn afhankelijk van de `inList` insteekmodule werkt. Deze insteekmodule biedt een duidelijk voordeel ten opzichte van de JavaScript-methode `indexOf()` waarbij de waarde niet overeenkomt met een gedeeltelijke tekenreeks. Als u deze insteekmodule bijvoorbeeld hebt gebruikt om te controleren op `"event2"`, komt deze niet overeen met een tekenreeks die `"event25"`. Deze insteekmodule is niet nodig als u niet hoeft te controleren op waarden in afgebakende tekenreeksen of arrays, of als u uw eigen insteekmodule wilt gebruiken `indexOf()` logica.

## De plug-in installeren met de Web SDK of de Adobe Analytics-extensie

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop [!UICONTROL Catalog] knop
1. Installeer en publiceer de [!UICONTROL Common Analytics Plugins] extension
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: Geen
   * Gebeurtenis: Kern - Bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: Gebruikelijke plug-ins voor Analytics
   * Type handeling: Initialiseren inList
1. Sla de wijzigingen in de regel op en publiceer deze.

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
/* Adobe Consulting Plugin: inList v3.0 */
function inList(lv,vtc,d,cc){var b=lv,e=vtc,c=d,f=cc;if("-v"===b)return{plugin:"inList",version:"3.0"};a:{if("undefined"!==typeof window.s_c_il){var a=0;for(var d;a<window.s_c_il.length;a++)if(d=window.s_c_il[a],d._c&&"s_c"===d._c){a=d;break a}}a=void 0}"undefined"!==typeof a&&(a.contextData.inList="3.0");if("string"!==typeof e)return!1;if("string"===typeof b)b=b.split(c||",");else if("object"!==typeof b)return!1;c=0;for(a=b.length;c<a;c++)if(1==f&&e===b[c]||e.toLowerCase()===b[c].toLowerCase())return!0;return!1};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `inList` functie retourneert een Booleaanse waarde, afhankelijk van de invoer. De volgende argumenten worden gebruikt:

* **`lv`** (vereist, tekenreeks of array): Een gescheiden lijst met waarden of een JavaScript-arrayobject dat moet worden doorzocht
* **`vtc`** (vereist, tekenreeks): De waarde waarnaar moet worden gezocht
* **`d`** (optioneel, tekenreeks): Het scheidingsteken dat wordt gebruikt voor het scheiden van afzonderlijke waarden in het dialoogvenster `lv` argument. Heeft als standaardwaarde een komma (`,`) wanneer niet ingesteld.
* **`cc`** (optioneel, Booleaans): Indien ingesteld op `true` of `1`, wordt een onderscheid gemaakt tussen hoofdletters en kleine letters. Indien ingesteld op `false` of weggelaten, dan wordt een case-insensitive controle gemaakt. Standaardwaarden: `false`.

Deze functie aanroepen retourneert `true` als het een gelijke vindt, en `false` als er geen overeenkomst wordt gevonden.

## Voorbeelden

```js
// Returns true
s.events = "event22,event24";
if(inList(s.events,"event22")) {
    // Code will execute
}

// Returns false because event2 is not an exact match in the string
s.events = "event22,event24";
if(inList(s.events,"event2")) {
    // Code will not execute
}

// Returns true because of the NOT operator
s.events = "event22,event24";
if(!inList(s.events,"event23")) {
    // Code will execute
}

// Returns false because of the case-sensitive check
s.events = "event22,event23";
if(inList(s.events,"EVenT23","",true)) {
    // Code will not execute
}

// Returns false because of a mismatched delimiter, treating "events,eVar1" as a single value
s.linkTrackVars = "events,eVar1";
if(inList(s.linkTrackVars,"eVar1","|")) {
    // Code will not execute
}
```

## Versiehistorie

### 3.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### v2.1 (26 september 2019)

* De optie voor de `cc` argument om geen booleaanse waarde te zijn. Bijvoorbeeld: `1` is een geldige controlewaarde voor hoofdletters en kleine letters.

### v2.0 (17 april 2018)

* Puntrelease (opnieuw gecompileerd, kleiner codeformaat).

### v1.01 (27 september 2017)

* Geoptimaliseerde code om grootte te reduceren

### v1.0 (2009)

* Eerste release.
