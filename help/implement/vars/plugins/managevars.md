---
title: manageVars
description: Wijzig de waarden van meerdere analytische variabelen tegelijk.
feature: Variables
exl-id: b80d1c43-7e79-443e-84fb-1f1edffca461
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '668'
ht-degree: 0%

---

# Adobe-insteekmodule: manageVars

{{plug-in}}

De `manageVars` kunt u de waarden van meerdere analytische variabelen tegelijk bewerken. U kunt ook waarden instellen op kleine letters of overbodige tekens uit meerdere variabelewaarden tegelijk verwijderen. Adobe raadt u aan deze plug-in te gebruiken als u de waarde van meerdere variabelen tegelijk wilt opruimen.

## De insteekmodule installeren met de extensie Web SDK of Web SDK

Deze plug-in wordt nog niet ondersteund voor gebruik in de Web SDK.

## De insteekmodule installeren met de Adobe Analytics-extensie

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken met Adobe Analytics.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop [!UICONTROL Catalog] knop
1. Installeer de [!UICONTROL Common Analytics Plugins] extension
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: geen
   * Event: Core - bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: veelgebruikte plug-ins voor Analytics
   * Type handeling: manageVars initialiseren
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met aangepaste code-editor

Als u niet de Gemeenschappelijke Insteekmodule van Analytics wilt gebruiken, kunt u de redacteur van de douanecode gebruiken.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder de extensie Adobe Analytics.
1. Breid uit [!UICONTROL Configure tracking using custom code] accordion, die de [!UICONTROL Open Editor] knop.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

## Plug-in installeren met AppMeasurement

Kopieer en plak de volgende code ergens in het bestand AppMeasurement nadat het object Analytics tracking is geïnstantieerd (met [`s_gi`](../functions/s-gi.md)). Door opmerkingen en versienummers van de code in uw implementatie te behouden, kunt u Adoben met het oplossen van mogelijke problemen.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: manageVars v3.0 (Requires AppMeasurement) */
function manageVars(cb,l,il){var g=cb,c=l,d=il;if("-v"===g)return{plugin:"manageVars",version:"3.0"};var f=function(){if("undefined"!==typeof window.s_c_il)for(var a=0,b;a<window.s_c_il.length;a++)if(b=window.s_c_il[a],b._c&&"s_c"===b._c)return b}();if("undefined"!==typeof f){f.contextData.manageVars="3.0";f.blankVars=function(a){this[a]&&(0>a.indexOf("contextData")?this[a]="":(a=a.substring(a.indexOf(".")+1),this.contextData[a]&&(this.contextData[a]="")))};f.lowerCaseVars=function(a){this[a]&&("events"!==a&&-1===a.indexOf("contextData")?(this[a]=this[a].toString(),0!==this[a].indexOf("D=")&&(this[a]=this[a].toLowerCase())):-1<a.indexOf("contextData")&&(a=a.substring(a.indexOf(".")+1),this.contextData[a]&&(this.contextData[a]=this.contextData[a].toString().toLowerCase())))};f.cleanStr=function(a){function b(a){if("string"===typeof a){for(a=a.replace(/<\/?[^>]+(>|$)/g,"").trim().replace(/[\u2018\u2019\u201A]/g,"'").replace(/\t+/g,"").replace(/[\n\r]/g," ");-1<a.indexOf("  ");)a=a.replace(/\s\s/g," ");return a}return""}this[a]&&"function"===typeof b&&(0>a.indexOf("contextData")?this[a]=b(this[a]):(a=a.substring(a.indexOf(".")+1),this.contextData[a]&&(this.contextData[a]=b(this.contextData[a].toString()))))};f.pt=function(a,b,c,d){if(a&&this[c]){a=a.split(b||",");b=a.length;for(var e,f=0;f<b;f++)if(e=this[c](a[f],d))return e}};if(!f[g])return!1;c=c||"";d=d||!0;var b,e="pageName,purchaseID,channel,server,pageType,campaign,state,zip,events,products,transactionID";for(b=1;76>b;b++)e+=",prop"+b;for(b=1;251>b;b++)e+=",eVar"+b;for(b=1;6>b;b++)e+=",hier"+b;for(b=1;4>b;b++)e+=",list"+b;for(b in f.contextData)e+=",contextData."+b;if(c){if(1==d)e=c.replace("['",".").replace("']","");else if(0==d){c=c.split(",");d=e.split(",");e="";for(x in c)for(y in-1<c[x].indexOf("contextData")&&(c[x]="contextData."+c[x].split("'")[1]),d)c[x]===d[y]&&(d[y]="");for(y in d)e+=d[y]?","+d[y]:""}f.pt(e,",",g,0);return!0}return""===c&&d?(f.pt(e,",",g,0),!0):!1}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `manageVars` function gebruikt de volgende argumenten:

* **`cb`** (vereist, tekenreeks): de naam van een callback-functie die de insteekmodule gebruikt om de variabelen Analytics te manipuleren. U kunt een Adobe-functie gebruiken zoals `cleanStr` of uw eigen aangepaste functie.
* **`l`** (optioneel, tekenreeks): een door komma&#39;s gescheiden lijst met analytische variabelen die u wilt bewerken. De standaardwaarde is ALLE Adobe Analytics-variabelen indien deze niet zijn ingesteld, waaronder:
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
* **`Il`** (optioneel, Boolean): Instellen op `false` als u *uitsluiten* de lijst van de in het `l` in plaats van ze op te nemen. Standaardwaarden: `true`.

Het aanroepen van deze functie retourneert niets. In plaats daarvan worden de waarden van de variabelen van de Analyse veranderd die op de gewenste callback functie worden gebaseerd.

## Voorbeelden van aanroepen

### Voorbeeld 1

De volgende code...

```js
manageVars("lowerCaseVars");
```

...wijzigt de waarden van alle hierboven beschreven variabelen in lagere versies.  De enige uitzondering hierop zijn de gebeurtenisvariabele, zoals sommige gebeurtenissen (bijvoorbeeld scAdd, scCheckout, enz.) zijn hoofdlettergevoelig en mogen niet worden verlaagd

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

...de waarden van alle hierboven beschreven variabelen (bijv. kleine letters) wijzigen, behalve voor eVar1, eVar2, eVar3 en lijst2

### Voorbeeld 5

De volgende code...

```js
manageVars("cleanStr");
```

...wijzigt de waarden van alle hierboven beschreven variabelen, inclusief de gebeurtenisvariabelen.  Specifiek, doet de schoonStr callback functie het volgende aan de waarde van elke variabelen:

* Verwijdert HTML-codering
* Verwijdert witruimten die aan het begin en einde van de waarde worden gevonden
* Hiermee vervangt u enkele aanhalingstekens naar links/rechts door een recht enkel aanhalingsteken (`'`)
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
