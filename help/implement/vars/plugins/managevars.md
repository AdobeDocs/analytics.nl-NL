---
title: manageVars
description: Wijzig de waarden van meerdere analytische variabelen tegelijk.
exl-id: b80d1c43-7e79-443e-84fb-1f1edffca461
source-git-commit: ab078c5da7e0e38ab9f0f941b407cad0b42dd4d1
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 0%

---

# Adobe-plug-in: manageVars

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de insteekmodule `manageVars` kunt u de waarden van meerdere analytische variabelen tegelijk bewerken. U kunt ook waarden instellen op kleine letters of overbodige tekens uit meerdere variabelewaarden tegelijk verwijderen. Adobe raadt u aan deze plug-in te gebruiken als u de waarde van meerdere variabelen tegelijk wilt opruimen.

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
   * Type handeling: ManageVars initialiseren
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
/* Adobe Consulting Plugin: manageVars v3.0 (Requires AppMeasurement) */
function manageVars(cb,l,il){var g=cb,c=l,d=il;if("-v"===g)return{plugin:"manageVars",version:"3.0"};var f=function(){if("undefined"!==typeof window.s_c_il)for(var a=0,b;a<window.s_c_il.length;a++)if(b=window.s_c_il[a],b._c&&"s_c"===b._c)return b}();if("undefined"!==typeof f){f.contextData.manageVars="3.0";f.blankVars=function(a){this[a]&&(0>a.indexOf("contextData")?this[a]="":(a=a.substring(a.indexOf(".")+1),this.contextData[a]&&(this.contextData[a]="")))};f.lowerCaseVars=function(a){this[a]&&("events"!==a&&-1===a.indexOf("contextData")?(this[a]=this[a].toString(),0!==this[a].indexOf("D=")&&(this[a]=this[a].toLowerCase())):-1<a.indexOf("contextData")&&(a=a.substring(a.indexOf(".")+1),this.contextData[a]&&(this.contextData[a]=this.contextData[a].toString().toLowerCase())))};f.cleanStr=function(a){function b(a){if("string"===typeof a){for(a=a.replace(/<\/?[^>]+(>|$)/g,"").trim().replace(/[\u2018\u2019\u201A]/g,"'").replace(/\t+/g,"").replace(/[\n\r]/g," ");-1<a.indexOf("  ");)a=a.replace(/\s\s/g," ");return a}return""}this[a]&&"function"===typeof b&&(0>a.indexOf("contextData")?this[a]=b(this[a]):(a=a.substring(a.indexOf(".")+1),this.contextData[a]&&(this.contextData[a]=b(this.contextData[a].toString()))))};f.pt=function(a,b,c,d){if(a&&this[c]){a=a.split(b||",");b=a.length;for(var e,f=0;f<b;f++)if(e=this[c](a[f],d))return e}};if(!f[g])return!1;c=c||"";d=d||!0;var b,e="pageName,purchaseID,channel,server,pageType,campaign,state,zip,events,products,transactionID";for(b=1;76>b;b++)e+=",prop"+b;for(b=1;251>b;b++)e+=",eVar"+b;for(b=1;6>b;b++)e+=",hier"+b;for(b=1;4>b;b++)e+=",list"+b;for(b in f.contextData)e+=",contextData."+b;if(c){if(1==d)e=c.replace("['",".").replace("']","");else if(0==d){c=c.split(",");d=e.split(",");e="";for(x in c)for(y in-1<c[x].indexOf("contextData")&&(c[x]="contextData."+c[x].split("'")[1]),d)c[x]===d[y]&&(d[y]="");for(y in d)e+=d[y]?","+d[y]:""}f.pt(e,",",g,0);return!0}return""===c&&d?(f.pt(e,",",g,0),!0):!1}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De functie `manageVars` gebruikt de volgende argumenten:

* **`cb`** (vereist, tekenreeks): De naam van een callback-functie die de plug-in gebruikt om de variabelen Analytics te manipuleren. U kunt een functie van de Adobe zoals `cleanStr` of uw eigen douanefunctie gebruiken.
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
* **`Il`** (optioneel, Booleaans): Stel deze optie in op  `false` als u de lijst met variabelen die in het  ** argument zijn gedeclareerd, wilt  `l` uitsluiten in plaats van ze op te nemen. Wordt standaard ingesteld op `true`.

Het aanroepen van deze functie retourneert niets. In plaats daarvan worden de waarden van de variabelen van de Analyse veranderd die op de gewenste callback functie worden gebaseerd.

## Voorbeelden van aanroepen

### Voorbeeld 1

De volgende code...

```js
manageVars("lowerCaseVars");
```

...Hiermee wijzigt u de waarden van alle hierboven beschreven variabelen in lagere versies.  De enige uitzondering hierop zijn de gebeurtenisvariabele, zoals sommige gebeurtenissen (bijvoorbeeld scAdd, scCheckout, enz.) zijn hoofdlettergevoelig en mogen niet worden verlaagd

### Voorbeeld 3

De volgende code...

```js
manageVars("lowerCaseVars", "events", false);
```

...produceert in wezen het zelfde resultaat zoals het eerste voorbeeld aangezien de gebeurtenisvariabele niet door gebrek wordt verminderd.

### Voorbeeld 2

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
* Veranderingen voor `s.cleanStr`, die nu de regelmatige `cleanStr` functie gebruikt.

### 2.0 (7 mei 2018)

* Puntrelease (inclusief volledige heranalyse/herschrijven van plug-in)
* Toegevoegde `cleanStr` callback functie
