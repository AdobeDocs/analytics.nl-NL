---
title: inList
description: Controleer of een waarde is opgenomen in een andere door tekens gescheiden waarde.
feature: Appmeasurement Implementation
exl-id: 7eedfd01-2b9a-4fae-a35b-433ca6900f27
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 0%

---

# Adobe-insteekmodule: inList

{{plug-in}}

Met de insteekmodule `inList` kunt u controleren of er al een waarde bestaat binnen een afgebakende tekenreeks of een JavaScript-arrayobject. Verschillende andere plug-ins zijn afhankelijk van de plug-in `inList` om te werken. Deze plug-in biedt een duidelijk voordeel ten opzichte van de JavaScript-methode `indexOf()` , waarbij gedeeltelijke tekenreeksen niet overeenkomen. Als u deze plug-in bijvoorbeeld hebt gebruikt om te controleren op `"event2"` , komt deze niet overeen met een tekenreeks die `"event25"` bevat. Deze plug-in is niet nodig als u niet hoeft te controleren op waarden in afgebakende tekenreeksen of arrays, of als u uw eigen `indexOf()` -logica wilt gebruiken.

## De insteekmodule installeren met de extensie Web SDK of Web SDK

Deze insteekmodule wordt nog niet ondersteund voor gebruik in de Web SDK.

## De insteekmodule installeren met de Adobe Analytics-extensie

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken in Adobe Analytics.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop [!UICONTROL Catalog]
1. De extensie [!UICONTROL Common Analytics Plugins] installeren en publiceren
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: geen
   * Event: Core - bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: veelgebruikte plug-ins voor Analytics
   * Type handeling: initialiseren in lijst
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met aangepaste code-editor

Als u niet de Gemeenschappelijke Insteekmodule van Analytics wilt gebruiken, kunt u de redacteur van de douanecode gebruiken.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste eigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder de extensie Adobe Analytics.
1. Vouw de accordeon [!UICONTROL Configure tracking using custom code] uit, zodat de knop [!UICONTROL Open Editor] zichtbaar wordt.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

## Plug-in installeren met AppMeasurement

Kopieer en plak de volgende code ergens in het AppMeasurement-bestand nadat het object Analytics tracking is geïnstantieerd (met [`s_gi`](../functions/s-gi.md) ). Door opmerkingen en versienummers van de code in uw implementatie te behouden, helpt Adobe bij het oplossen van mogelijke problemen.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: inList v3.0 */
function inList(lv,vtc,d,cc){var b=lv,e=vtc,c=d,f=cc;if("-v"===b)return{plugin:"inList",version:"3.0"};a:{if("undefined"!==typeof window.s_c_il){var a=0;for(var d;a<window.s_c_il.length;a++)if(d=window.s_c_il[a],d._c&&"s_c"===d._c){a=d;break a}}a=void 0}"undefined"!==typeof a&&(a.contextData.inList="3.0");if("string"!==typeof e)return!1;if("string"===typeof b)b=b.split(c||",");else if("object"!==typeof b)return!1;c=0;for(a=b.length;c<a;c++)if(1==f&&e===b[c]||e.toLowerCase()===b[c].toLowerCase())return!0;return!1};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De functie `inList` retourneert een Booleaanse waarde, afhankelijk van de invoer. De volgende argumenten worden gebruikt:

* **`lv`** (vereist, tekenreeks of array): Een gescheiden lijst met waarden of een JavaScript-arrayobject dat moet worden doorzocht
* **`vtc`** (required, string): De waarde waarnaar moet worden gezocht
* **`d`** (optioneel, tekenreeks): het scheidingsteken dat wordt gebruikt voor het scheiden van afzonderlijke waarden in het argument `lv` . Heeft als standaardwaarde een komma (`,`).
* **`cc`** (optioneel, Boolean): Bij `true` of `1` wordt een hoofdlettergevoelige controle uitgevoerd. Indien ingesteld op `false` of weggelaten, wordt een niet-hoofdlettergevoelige controle uitgevoerd. Wordt standaard ingesteld op `false` .

Als deze functie wordt aangeroepen, wordt `true` geretourneerd als er een overeenkomst wordt gevonden en `false` als er geen overeenkomst wordt gevonden.

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

* De optie voor het argument `cc` is toegevoegd om geen booleaanse waarde te hebben. `1` is bijvoorbeeld een geldige controlewaarde voor hoofdletters en kleine letters.

### v2.0 (17 april 2018)

* Puntrelease (opnieuw gecompileerd, kleiner codeformaat).

### v1.01 (27 september 2017)

* Geoptimaliseerde code om grootte te reduceren

### v1.0 (2009)

* Eerste release.
