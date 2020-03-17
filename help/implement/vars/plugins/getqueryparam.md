---
title: getQueryParam
description: Haal de waarde van de parameter van het vraagkoord van een URL uit.
translation-type: tm+mt
source-git-commit: 180ad544541f25d02b3a257559bc045abed7387b

---


# Adobe-insteekmodule: getQueryParam

> [!IMPORTANT] Deze plug-in wordt geleverd door Adobe Consulting als een hoffelijkheid om u te helpen meer waarde te krijgen van Adobe Analytics. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `getQueryParam` insteekmodule kunt u de waarde extraheren van elke querytekenreeksparameter in een URL. Het is nuttig om campagnecodes, zowel intern als extern, uit het landen van pagina URLs te halen. Het is ook nuttig wanneer het halen van onderzoekstermijnen of andere parameters van het vraagkoord.

Deze plug-in biedt robuuste functies voor het parseren van complexe URL&#39;s, waaronder hashes en URL&#39;s die meerdere parameters voor queryreeksen bevatten. Als u alleen eenvoudige parametervereisten voor de queryreeks hebt, raadt Adobe u aan de URL-parameterfuncties in Launch of de `Util.getQueryParam` methode in AppMeasurement te gebruiken.

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
   * Type handeling: getQueryParam initialiseren
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met de aangepaste code-editor van Launch

Als u de extensie van de plug-in niet wilt gebruiken, kunt u de aangepaste code-editor gebruiken.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar het [!UICONTROL Extensions] tabblad en klik vervolgens op de [!UICONTROL Configure] knop onder de extensie Adobe Analytics.
1. Vouw de [!UICONTROL Configure tracking using custom code] accordeon uit, zodat de [!UICONTROL Open Editor] knop zichtbaar wordt.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getQueryParam v3.3 (Requires pt plug-in) */
s.getQueryParam=function(qsp,de,url){var g=this,e="",k=function(b,de){de=de.split("?").join("&");de=de.split("#").join("&");var d=de.indexOf("&"),url="";b&&(-1<d||de.indexOf("=")>d)&&(d=de.substring(d+1),url=g.pt(d,"&","gpval",b));return url};qsp=qsp.split(",");var l=qsp.length;g.gpval=function(de,b){if(de){var d=de.split("="),url=d[0];d=d[1]?d[1]:!0;if(b.toLowerCase() ==url.toLowerCase())return"boolean"===typeof d?d:this.unescape(d)}return""};de=de?de:"";url=(url?url:g.pageURL?g.pageURL: location.href)+"";if((4<de.length||-1<de.indexOf("="))&&url&&4>url.length){var b=de;de=url;url=b}for(var h=0;h<l;h++)b=k(qsp[h],url) ,"string"===typeof b?(b=-1<b.indexOf("#")?b.substring(0,b.indexOf("#")):b,e+=e?de+b:b):e=""===e?b:e+(de+b);return e};

/* Adobe Consulting Plugin: pt v2.01 */ 
s.pt=function(l,de,cf,fa){if(l&&this[cf]){l=l.split(de||",");de=l.length;for(var e,c=0;c<de;c++)if(e=this[cf](l[c],fa))return e}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `getQueryParam` methode gebruikt de volgende argumenten:

* **`qsp`** (vereist): Een door komma&#39;s gescheiden lijst met parameters voor queryreeksen die moet worden gezocht binnen de URL. Het is niet hoofdlettergevoelig.
* **`de`** (optioneel): Het scheidingsteken dat moet worden gebruikt als meerdere parameters van queryreeksen overeenkomen. Heeft als standaardwaarde een lege tekenreeks.
* **`url`** (optioneel): Een aangepaste URL, tekenreeks of variabele waaruit de parameterwaarden voor de queryreeks moeten worden geëxtraheerd. Wordt standaard ingesteld op `window.location`.

Als deze methode wordt aangeroepen, wordt een waarde geretourneerd die afhankelijk is van de bovenstaande argumenten en de URL:

* Wanneer geen overeenkomende parameter voor een querytekenreeks wordt gevonden, retourneert de methode een lege tekenreeks.
* Wanneer een overeenkomende parameter voor een querytekenreeks wordt gevonden, retourneert de methode de parameterwaarde voor de queryreeks.
* Als een overeenkomende parameter voor een querytekenreeks wordt gevonden maar de waarde leeg is, wordt de methode geretourneerd `true`.
* Als er meerdere overeenkomende parameters voor queryreeksen worden gevonden, retourneert de methode een tekenreeks met elke parameterwaarde die door de tekenreeks in het `de` argument wordt gescheiden.

## Voorbeelden van aanroepen

### Voorbeeld 1

Als de huidige URL als volgt is:

```js
http://www.abc123.com/?cid=trackingcode1
```

Met de volgende code wordt s.campagne ingesteld op &#39;trackingcode1&#39;:

```js
s.campaign=s.getQueryParam('cid');
```

### Voorbeeld 2

Als de huidige URL als volgt is:

```js
http://www.abc123.com/?cid=trackingcode1&ecid=123456
```

Met de volgende code wordt s.campagne ingesteld op &#39;trackingcode1:123456&#39;:

```js
s.campaign=s.getQueryParam('cid,ecid',':');
```

### Voorbeeld 3

Als de huidige URL als volgt is:

```js
http://www.abc123.com/?cid=trackingcode1&ecid=123456
```

Met de volgende code wordt s.campagne ingesteld op &#39;trackingcode1123456&#39;:

```js
s.campaign=s.getQueryParam('cid,ecid');
```

### Voorbeeld 4

Als de huidige URL als volgt is:

```js
http://www.abc123.com/?cid=trackingcode1&ecid=123456#location
```

Met de volgende code wordt s.campagne ingesteld op &quot;123456&quot;:

```js
s.campaign=s.getQueryParam('ecid');
```

### Voorbeeld 5

Als de huidige URL als volgt is:

```js
http://www.abc123.com/#location&cid=trackingcode1&ecid=123456
```

Met de volgende code wordt s.campagne ingesteld op &quot;123456&quot;

```js
s.campaign=s.getQueryParam('ecid');
```

**Opmerking:** De insteekmodule vervangt de URL naar het hash-teken van de controle door een vraagteken als er geen vraagteken bestaat.  Als de URL een vraagteken bevat dat voor het hashteken komt, vervangt de insteekmodule de URL naar het hashteken van de controle door een en-teken;

### Voorbeeld 6

Als de huidige URL de volgende is...

```js
http://www.abc123.com/
```

...en als de variabele s.testURL als volgt is ingesteld:

```js
s.testURL="http://www.abc123.com/?cid=trackingcode1&ecid=123456#location&pos=300";
```

De volgende code stelt s.campagne helemaal niet in:

```js
s.campaign=s.getQueryParam('cid');
```

De volgende code stelt s.campagne echter in op &#39;trackingcode1&#39;:

```js
s.campaign=s.getQueryParam('cid','',s.testURL);
```

**Opmerking:** de derde parameter kan om het even welke koord/variabele zijn die de code zal gebruiken om de parameters van het vraagkoord in te vinden

Met de volgende code wordt s.eVar2 ingesteld op &quot;123456|trackingcode1|true|300&quot;:

```js
s.eVar2=s.getQueryParam('ecid,cid,location,pos','|',s.testURL);
```

* De waarde 123456 is afkomstig van de parameter ecid in de variabele s.testURL
* De waarde van trackingCode1 is afkomstig van de parameter cid in de variabele s.testURL
* De waarde true is afkomstig van het bestaan (maar niet de waarde) van de parameter location na het hash-teken in de variabele s.testURL

De waarde 300 is afkomstig van de waarde van de parameter pos in de variabele s.testURL

## Versiehistorie

### 3.3 (24 september 2019)

* Overbodige logica om codegrootte te verkleinen

### 3.2 (15 mei 2018)

* Verplaatst `findParameterValue` en `getParameterValue` functioneert in de `getQueryParam` functie

### 3.1 (10 mei 2018)

* Probleem verholpen met het vastleggen van parameters voor queryreeksen zonder waarde

### 3.0 (16 april 2018)

* Puntrelease (opnieuw gecompileerd, kleiner codeformaat).
* De naam van hulpfuncties is gewijzigd in `findParameterValue` en `getParameterValue` voor leesbaarheidsdoeleinden.
* Verwijderde de behoefte om een argument toe te voegen om parameters in het knoeiboel te vinden URL

### 2.5 (8 januari 2016)

* Compatibel met zowel H-code als AppMeasurement (vereist `s.pt` met AppMeasurement).

### 2.4

* De `h` parameter toegevoegd, zodat de code kan zoeken naar parameters van queryreeksen die na het hash-teken (`#`) worden gevonden

### 2.3

* Probleem verholpen waarbij de insteekmodule alleen werkte toen de hash aanwezig was na de trackingcode. Dit probleem is nu opgelost.

### 2.2

* Verwijdert nu hash-tekens (en alles daarna) uit de geretourneerde waarde

### 2.1

* Compatibel met H.10-code
