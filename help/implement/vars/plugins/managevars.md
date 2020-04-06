---
title: manageVars
description: Wijzig de waarden van meerdere analytische variabelen tegelijk.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Adobe-insteekmodule: manageVars

>[!IMPORTANT] Deze plug-in wordt geleverd door Adobe Consulting als een hoffelijkheid om u te helpen meer waarde te krijgen van Adobe Analytics. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `manageVars` insteekmodule kunt u de waarden van meerdere analytische variabelen tegelijk bewerken. U kunt ook waarden instellen op kleine letters of overbodige tekens uit meerdere variabelewaarden tegelijk verwijderen. Adobe raadt u aan deze plug-in te gebruiken als u de waarde van meerdere variabelen tegelijk wilt opruimen.

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
   * Type handeling: ManageVars initialiseren
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
/* Adobe Consulting Plugin: manageVars v2.1 (Requires pt plug-in and other necessary callback plug-ins) */
s.manageVars=function(cb,l,il){var s=this;if(!s[cb])return!1;l=l||"";il=il||!0;var a,d="pageName,purchaseID,channel,server, pageType,campaign,state,zip,events,products,transactionID";for(a=1;76>a;a++)d+=",prop"+a;for(a=1;251>a;a++)d+=",eVar"+a;for(a=1;6>a;a++)d+=",hier"+a;for(a=1;4>a;a++)d+=",list"+a;for(a in s.contextData)d+=",contextData."+a;if(l){if(1==il)d=l.replace("['", ".").replace("']","");else if(0==il){l=l.split(",");il=d.split(",");d="";for(x in l)for(y in-1<l[x].indexOf("contextData")&& (l[x]="contextData."+l[x].split("'")[1]),il)l[x]===il[y]&&(il[y]="");for(y in il)d+=il[y]?","+il[y]:""}s.pt(d,",",cb,0);return!0} return""===l&&il?(s.pt(d,",",cb,0),!0):!1};

/* Adobe Consulting Plugin: lowerCaseVars for manageVars (Requires manageVars plug-in) */
s.lowerCaseVars=function(v){var s=this;s[v]&&("events"!==v&&-1===v.indexOf("contextData")?(s[v]=s[v].toString(),0!== s[v].indexOf("D=")&&(s[v]=s[v].toLowerCase())):-1<v.indexOf("contextData")&&(v=v.substring(v.indexOf(".")+1),s.contextData[v]&& (s.contextData[v]=s.contextData[v].toString().toLowerCase())))};

/* Adobe Consulting Plugin: cleanStr for manageVars (Requires manageVars and cleanStr plug-ins) */
s.cleanStr=function(v){var s=this;s[v]&&"function"!==typeof cleanStr&&(0>v.indexOf("contextData")?s[v]=cleanStr(s[v]): (v=v.substring(v.indexOf(".")+1),s.contextData[v]&&(s.contextData[v]=cleanStr(s.contextData[v].toString()))))};

/* Adobe Consulting Plugin: cleanStr v1.0 */
function cleanStr(str){if("string"===typeof str){str=str.replace(/<\/?[^>]+(>|$)/g,"").trim().replace(/[\u2018\u2019\u201A]/g, "'").replace(/\t+/g,"").replace(/[\n\r]/g," ");for(;-1<str.indexOf("  ");)str=str.replace(/\s\s/g," ");return str}return""};

/* Adobe Consulting Plugin: pt v2.01 */
s.pt=function(l,de,cf,fa){if(l&&this[cf]){l=l.split(de||",");de=l.length;for(var e,c=0;c<de;c++)if(e=this[cf](l[c],fa))return e}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `manageVars` methode gebruikt de volgende argumenten:

* **`cb`** (vereist, tekenreeks): De naam van een callback-functie die de plug-in gebruikt om de variabelen Analytics te manipuleren. U kunt een Adobe-functie net als `cleanStr` uw eigen aangepaste functie gebruiken.
* **`l`** (optioneel, tekenreeks): Een door komma&#39;s gescheiden lijst met variabelen van Analytics die u wilt manipuleren. Wordt standaard ingesteld op ALL Adobe Analytics-variabelen, waaronder:
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
* **`Il`** (optioneel, Booleaans): Stel deze optie in op `false` als u de lijst met variabelen die in het *argument zijn gedeclareerd, wilt* uitsluiten `l` in plaats van ze op te nemen. Wordt standaard ingesteld op `true`.

Het aanroepen van deze methode retourneert niets. In plaats daarvan worden de waarden van de variabelen van de Analyse veranderd die op de gewenste callback functie worden gebaseerd.

## Voorbeelden van aanroepen

### Voorbeeld 1

De volgende code...

```js
s.manageVars("lowerCaseVars");
```

...Hiermee wijzigt u de waarden van alle hierboven beschreven variabelen in lagere versies.  De enige uitzondering hierop zijn de gebeurtenisvariabele, zoals sommige gebeurtenissen (bijvoorbeeld scAdd, scCheckout, enz.) zijn hoofdlettergevoelig en mogen niet worden verlaagd

### Voorbeeld 2

De volgende code...

```js
s.manageVars("lowerCaseVars", "events", false);
```

...produceert in wezen het zelfde resultaat zoals het eerste voorbeeld aangezien de gebeurtenisvariabele niet door gebrek wordt verminderd.

### Voorbeeld 3

De volgende code...

```js
s.manageVars("lowerCaseVars", "eVar1,eVar2,eVar3,list2");
```

...alleen de waarden van eVar1, eVar2, eVar3 en list2 wijzigen (bijvoorbeeld kleine letters)

### Voorbeeld 4

De volgende code...

```js
s.manageVars("lowerCaseVars", "eVar1,eVar2,eVar3,list2", false);
```

...wijzigt (bijvoorbeeld in kleine letters) de waarden van alle hierboven beschreven variabelen, behalve voor Var1, eVar2, eVar3 en list2

### Voorbeeld 5

De volgende code...

```js
s.manageVars("cleanStr");
```

...wijzigt de waarden van alle hierboven beschreven variabelen, inclusief de gebeurtenisvariabelen.  Specifiek, doet de schoonStr callback functie het volgende aan de waarde van elke variabelen:

* Verwijdert HTML-codering
* Verwijdert witruimten die aan het begin en einde van de waarde worden gevonden
* Hiermee vervangt u enkele aanhalingstekens naar links/rechts (bijvoorbeeld &quot;) met een recht enkel aanhalingsteken (&#39;)
* Hiermee vervangt u tabtekens, nieuwe-regeltekens en Enter-tekens door spaties
* Hiermee vervangt u alle dubbele tekens (of drievoudig, enz.) spaties met één spatie

## Versiehistorie

### 2.1 (14 januari 2019)

* Opgeloste problemen voor Internet Explorer 11-browsers.
* Wijzigingen voor `s.cleanStr`, die nu de reguliere `cleanStr` functie gebruiken.

### 2.0 (7 mei 2018)

* Puntrelease (inclusief volledige heranalyse/herschrijven van plug-in)
* Toegevoegde `cleanStr` callback-functie
