---
title: manageVars
description: Wijzig de waarden van meerdere analytische variabelen tegelijk.
feature: Appmeasurement Implementation
exl-id: b80d1c43-7e79-443e-84fb-1f1edffca461
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '668'
ht-degree: 0%

---

# Adobe-insteekmodule: manageVars

{{plug-in}}

Met de plug-in `manageVars` kunt u de waarden van meerdere analytische variabelen tegelijk bewerken. U kunt ook waarden instellen op kleine letters of overbodige tekens uit meerdere variabelewaarden tegelijk verwijderen. Adobe raadt u aan deze plug-in te gebruiken als u de waarde van meerdere variabelen tegelijk wilt opruimen.

## De insteekmodule installeren met de extensie Web SDK of Web SDK

Deze insteekmodule wordt nog niet ondersteund voor gebruik in de Web SDK.

## De insteekmodule installeren met de Adobe Analytics-extensie

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken in Adobe Analytics.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop [!UICONTROL Catalog]
1. De extensie [!UICONTROL Common Analytics Plugins] installeren en publiceren
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: geen
   * Event: Core - bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: veelgebruikte plug-ins voor Analytics
   * Type handeling: manageVars initialiseren
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met aangepaste code-editor

Als u niet de Gemeenschappelijke Insteekmodule van Analytics wilt gebruiken, kunt u de redacteur van de douanecode gebruiken.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste eigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder de extensie Adobe Analytics.
1. Vouw de accordeon [!UICONTROL Configure tracking using custom code] uit, zodat de knop [!UICONTROL Open Editor] zichtbaar wordt.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

## Plug-in installeren met AppMeasurement

Kopieer en plak de volgende code ergens in het AppMeasurement-bestand nadat het object Analytics tracking is geïnstantieerd (met [`s_gi`](../functions/s-gi.md) ). Door opmerkingen en versienummers van de code in uw implementatie te behouden, helpt Adobe bij het oplossen van mogelijke problemen.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: manageVars v3.0 (Requires AppMeasurement) */
function manageVars(cb,l,il){var g=cb,c=l,d=il;if("-v"===g)return{plugin:"manageVars",version:"3.0"};var f=function(){if("undefined"!==typeof window.s_c_il)for(var a=0,b;a<window.s_c_il.length;a++)if(b=window.s_c_il[a],b._c&&"s_c"===b._c)return b}();if("undefined"!==typeof f){f.contextData.manageVars="3.0";f.blankVars=function(a){this[a]&&(0>a.indexOf("contextData")?this[a]="":(a=a.substring(a.indexOf(".")+1),this.contextData[a]&&(this.contextData[a]="")))};f.lowerCaseVars=function(a){this[a]&&("events"!==a&&-1===a.indexOf("contextData")?(this[a]=this[a].toString(),0!==this[a].indexOf("D=")&&(this[a]=this[a].toLowerCase())):-1<a.indexOf("contextData")&&(a=a.substring(a.indexOf(".")+1),this.contextData[a]&&(this.contextData[a]=this.contextData[a].toString().toLowerCase())))};f.cleanStr=function(a){function b(a){if("string"===typeof a){for(a=a.replace(/<\/?[^>]+(>|$)/g,"").trim().replace(/[\u2018\u2019\u201A]/g,"'").replace(/\t+/g,"").replace(/[\n\r]/g," ");-1<a.indexOf("  ");)a=a.replace(/\s\s/g," ");return a}return""}this[a]&&"function"===typeof b&&(0>a.indexOf("contextData")?this[a]=b(this[a]):(a=a.substring(a.indexOf(".")+1),this.contextData[a]&&(this.contextData[a]=b(this.contextData[a].toString()))))};f.pt=function(a,b,c,d){if(a&&this[c]){a=a.split(b||",");b=a.length;for(var e,f=0;f<b;f++)if(e=this[c](a[f],d))return e}};if(!f[g])return!1;c=c||"";d=d||!0;var b,e="pageName,purchaseID,channel,server,pageType,campaign,state,zip,events,products,transactionID";for(b=1;76>b;b++)e+=",prop"+b;for(b=1;251>b;b++)e+=",eVar"+b;for(b=1;6>b;b++)e+=",hier"+b;for(b=1;4>b;b++)e+=",list"+b;for(b in f.contextData)e+=",contextData."+b;if(c){if(1==d)e=c.replace("['",".").replace("']","");else if(0==d){c=c.split(",");d=e.split(",");e="";for(x in c)for(y in-1<c[x].indexOf("contextData")&&(c[x]="contextData."+c[x].split("'")[1]),d)c[x]===d[y]&&(d[y]="");for(y in d)e+=d[y]?","+d[y]:""}f.pt(e,",",g,0);return!0}return""===c&&d?(f.pt(e,",",g,0),!0):!1}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De functie `manageVars` gebruikt de volgende argumenten:

* **`cb`** (vereist, tekenreeks): de naam van een callback-functie die de plug-in gebruikt om de variabelen Analytics te manipuleren. U kunt een Adobe-functie zoals `cleanStr` of uw eigen aangepaste functie gebruiken.
* **`l`** (optioneel, tekenreeks): een door komma&#39;s gescheiden lijst met analysevariabelen die u wilt bewerken. De standaardwaarde is ALLE Adobe Analytics-variabelen indien deze niet zijn ingesteld, waaronder:
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
* **`Il`** (facultatief, boolean): Reeks aan `false` als u ** de lijst van variabelen wilt uitsluiten die in het `l` argument in plaats van hen worden verklaard. Wordt standaard ingesteld op `true` .

Het aanroepen van deze functie retourneert niets. In plaats daarvan worden de waarden van de variabelen van de Analyse veranderd die op de gewenste callback functie worden gebaseerd.

## Voorbeelden van aanroepen

### Voorbeeld 1

De volgende code...

```js
manageVars("lowerCaseVars");
```

...wijzigt de waarden van alle hierboven beschreven variabelen in lagere versies.  De enige uitzondering hierop is de gebeurtenisvariabele, aangezien sommige gebeurtenissen (zoals scAdd, scCheckout, enz.) hoofdlettergevoelig zijn en niet mogen worden verlaagd

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

...de waarden van alle hierboven beschreven variabelen (bijv. kleine letters) wijzigen, behalve voor eVar1, eVar2, eVar3 en list2

### Voorbeeld 5

De volgende code...

```js
manageVars("cleanStr");
```

...wijzigt de waarden van alle hierboven beschreven variabelen, inclusief de gebeurtenisvariabelen.  Specifiek, doet de schoonStr callback functie het volgende aan de waarde van elke variabelen:

* Verwijdert HTML-codering
* Verwijdert witruimten die aan het begin en einde van de waarde worden gevonden
* Vervangt enkele aanhalingstekens naar links/rechts door een recht enkel aanhalingsteken (`'`)
* Hiermee vervangt u tabtekens, nieuwe-regeltekens en Enter-tekens door spaties
* Hiermee vervangt u alle dubbele (of driedubbele, enz.) spaties door één spatie

## Versiehistorie

### 3.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 2.1 (14 januari 2019)

* Opgeloste problemen voor Internet Explorer 11-browsers.
* Wijzigingen voor `s.cleanStr` , die nu de reguliere `cleanStr` functie gebruikt.

### 2.0 (7 mei 2018)

* Puntrelease (inclusief volledige heranalyse/herschrijven van plug-in)
* Toegevoegde callback-functie `cleanStr`
