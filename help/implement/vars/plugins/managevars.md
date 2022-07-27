---
title: manageVars
description: Wijzig de waarden van meerdere analytische variabelen tegelijk.
feature: Variables
exl-id: b80d1c43-7e79-443e-84fb-1f1edffca461
source-git-commit: 7c7a7d8add9edb1538df12b440bc0a15f09efe5e
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---

# Adobe-plug-in: manageVars

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

De `manageVars` kunt u de waarden van meerdere analytische variabelen tegelijk bewerken. U kunt ook waarden instellen op kleine letters of overbodige tekens uit meerdere variabelewaarden tegelijk verwijderen. Adobe raadt u aan deze plug-in te gebruiken als u de waarde van meerdere variabelen tegelijk wilt opruimen.

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
    * Action Type: Initialize manageVars
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
/* Adobe Consulting Plugin: manageVars v3.0 (Requires AppMeasurement) */
function manageVars(cb,l,il){var g=cb,c=l,d=il;if("-v"===g)return{plugin:"manageVars",version:"3.0"};var f=function(){if("undefined"!==typeof window.s_c_il)for(var a=0,b;a<window.s_c_il.length;a++)if(b=window.s_c_il[a],b._c&&"s_c"===b._c)return b}();if("undefined"!==typeof f){f.contextData.manageVars="3.0";f.blankVars=function(a){this[a]&&(0>a.indexOf("contextData")?this[a]="":(a=a.substring(a.indexOf(".")+1),this.contextData[a]&&(this.contextData[a]="")))};f.lowerCaseVars=function(a){this[a]&&("events"!==a&&-1===a.indexOf("contextData")?(this[a]=this[a].toString(),0!==this[a].indexOf("D=")&&(this[a]=this[a].toLowerCase())):-1<a.indexOf("contextData")&&(a=a.substring(a.indexOf(".")+1),this.contextData[a]&&(this.contextData[a]=this.contextData[a].toString().toLowerCase())))};f.cleanStr=function(a){function b(a){if("string"===typeof a){for(a=a.replace(/<\/?[^>]+(>|$)/g,"").trim().replace(/[\u2018\u2019\u201A]/g,"'").replace(/\t+/g,"").replace(/[\n\r]/g," ");-1<a.indexOf("  ");)a=a.replace(/\s\s/g," ");return a}return""}this[a]&&"function"===typeof b&&(0>a.indexOf("contextData")?this[a]=b(this[a]):(a=a.substring(a.indexOf(".")+1),this.contextData[a]&&(this.contextData[a]=b(this.contextData[a].toString()))))};f.pt=function(a,b,c,d){if(a&&this[c]){a=a.split(b||",");b=a.length;for(var e,f=0;f<b;f++)if(e=this[c](a[f],d))return e}};if(!f[g])return!1;c=c||"";d=d||!0;var b,e="pageName,purchaseID,channel,server,pageType,campaign,state,zip,events,products,transactionID";for(b=1;76>b;b++)e+=",prop"+b;for(b=1;251>b;b++)e+=",eVar"+b;for(b=1;6>b;b++)e+=",hier"+b;for(b=1;4>b;b++)e+=",list"+b;for(b in f.contextData)e+=",contextData."+b;if(c){if(1==d)e=c.replace("['",".").replace("']","");else if(0==d){c=c.split(",");d=e.split(",");e="";for(x in c)for(y in-1<c[x].indexOf("contextData")&&(c[x]="contextData."+c[x].split("'")[1]),d)c[x]===d[y]&&(d[y]="");for(y in d)e+=d[y]?","+d[y]:""}f.pt(e,",",g,0);return!0}return""===c&&d?(f.pt(e,",",g,0),!0):!1}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `manageVars` function gebruikt de volgende argumenten:

* **`cb`** (vereist, tekenreeks): De naam van een callback-functie die de plug-in gebruikt om de variabelen Analytics te manipuleren. U kunt de functie Adobe gebruiken zoals `cleanStr` of uw eigen aangepaste functie.
* **`l`** (optioneel, tekenreeks): Een door komma&#39;s gescheiden lijst met variabelen van Analytics die u wilt manipuleren. De standaardwaarde is ALLE Adobe Analytics-variabelen indien deze niet zijn ingesteld, waaronder:
   * `pageName`
   * `purchaseID`
   * `channel`
   * `server`
   * `pageType`
   * `campaign`
   * `state`
   * `zip`
   * `events`
   * `products`
   * `transactionID`
   * Alle profielen
   * Alle eVars
   * Alle hiërarchievariabelen
   * Alle lijstvariabelen
   * Alle contextgegevensvariabelen
* **`Il`** (optioneel, Booleaans): Instellen op `false` als u wilt *uitsluiten* de lijst van de in het `l` in plaats van ze op te nemen. Standaardwaarden: `true`.

Het aanroepen van deze functie retourneert niets. In plaats daarvan worden de waarden van de variabelen van de Analyse veranderd die op de gewenste callback functie worden gebaseerd.

## Voorbeelden van aanroepen

### Voorbeeld 1

De volgende code...

```js
manageVars("lowerCaseVars");
```

...Hiermee wijzigt u de waarden van alle hierboven beschreven variabelen in lagere versies.  De enige uitzondering hierop zijn de gebeurtenisvariabele, zoals sommige gebeurtenissen (bijvoorbeeld scAdd, scCheckout, enz.) zijn hoofdlettergevoelig en mogen niet worden verlaagd

### Voorbeeld 2

De volgende code...

```js
manageVars("lowerCaseVars", "events", false);
```

...produceert in wezen het zelfde resultaat zoals het eerste voorbeeld aangezien de gebeurtenisvariabele niet door gebrek wordt verminderd.

### Voorbeeld 3

De volgende code...

```js
manageVars("lowerCaseVars", "eVar1,eVar2,eVar3,list2");
```

...alleen de waarden van eVar1, eVar2, eVar3 en list2 wijzigen (bijvoorbeeld kleine letters)

### Voorbeeld 4

De volgende code...

```js
manageVars("lowerCaseVars", "eVar1,eVar2,eVar3,list2", false);
```

...wijzigt (bijvoorbeeld in kleine letters) de waarden van alle hierboven beschreven variabelen, behalve voor eVar1, eVar2, eVar3 en list2

### Voorbeeld 5

De volgende code...

```js
manageVars("cleanStr");
```

...wijzigt de waarden van alle hierboven beschreven variabelen, inclusief de gebeurtenisvariabelen.  Specifiek, doet de schoonStr callback functie het volgende aan de waarde van elke variabelen:

* Verwijdert HTML-codering
* Verwijdert witruimten die aan het begin en einde van de waarde worden gevonden
* Hiermee vervangt u enkele aanhalingstekens naar links/rechts (bijvoorbeeld &quot;) met een recht enkel aanhalingsteken (&#39;)
* Hiermee vervangt u tabtekens, nieuwe-regeltekens en Enter-tekens door spaties
* Hiermee vervangt u alle dubbele tekens (of drievoudig, enz.) spaties met één spatie

## Versiehistorie

### 3.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 2.1 (14 januari 2019)

* Opgeloste problemen voor Internet Explorer 11-browsers.
* Wijzigingen voor `s.cleanStr`, die nu gebruikmaakt van de `cleanStr` functie.

### 2.0 (7 mei 2018)

* Puntrelease (inclusief volledige heranalyse/herschrijven van plug-in)
* Toegevoegd `cleanStr` callback, functie
