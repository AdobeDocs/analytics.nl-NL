---
title: getQueryParam
description: Haal de waarde van de parameter van het vraagkoord van een URL uit.
exl-id: d2d542d1-3a18-43d9-a50d-c06d8bd473b8
translation-type: tm+mt
source-git-commit: 5a087087c8f54650173391bd7766bfdfd12ccb7e
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 0%

---

# Adobe-plug-in: getQueryParam

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de insteekmodule `getQueryParam` kunt u de waarde van elke querytekenreeksparameter in een URL extraheren. Het is nuttig om campagnecodes, zowel intern als extern, uit het landen van pagina URLs te halen. Het is ook nuttig wanneer het halen van onderzoekstermijnen of andere parameters van het vraagkoord.

Deze plug-in biedt robuuste functies voor het parseren van complexe URL&#39;s, waaronder hashes en URL&#39;s die meerdere parameters voor queryreeksen bevatten. Als u slechts eenvoudige de parameterbehoeften van het vraagkoord hebt, adviseert Adobe het gebruiken van de URL parametereigenschappen in Lancering of de [`Util.getQueryParam()`](../functions/util-getqueryparam.md) methode inbegrepen in AppMeasurement.

## De insteekmodule installeren met de Adobe Experience Platform Launch-extensie

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken.

1. Meld u met uw Adobe-id aan bij [launch.adobe.com](https://launch.adobe.com).
1. Klik op de gewenste eigenschap.
1. Ga naar het tabblad [!UICONTROL Extensions] en klik op de knop [!UICONTROL Catalog]
1. De extensie [!UICONTROL Common Analytics Plugins] installeren en publiceren
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: Geen
   * Gebeurtenis: Kern - Bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: Gebruikelijke plug-ins voor Analytics
   * Type handeling: getQueryParam initialiseren
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met de aangepaste code-editor van Launch

Als u de extensie van de plug-in niet wilt gebruiken, kunt u de aangepaste code-editor gebruiken.

1. Meld u met uw Adobe-id aan bij [launch.adobe.com](https://launch.adobe.com).
1. Klik op de gewenste eigenschap.
1. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder de uitbreiding van Adobe Analytics.
1. Breid [!UICONTROL Configure tracking using custom code] accordeon uit, die [!UICONTROL Open Editor] knoop openbaart.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getQueryParam v4.0.1  */
function getQueryParam(a,d,f){function n(g,c){c=c.split("?").join("&");c=c.split("#").join("&");var e=c.indexOf("&");if(g&&(-1<e||c.indexOf("=")>e)){e=c.substring(e+1);e=e.split("&");for(var h=0,p=e.length;h<p;h++){var l=e[h].split("="),q=l[1];if(l[0].toLowerCase()===g.toLowerCase())return decodeURIComponent(q||!0)}}return""}if("-v"===a)return{plugin:"getQueryParam",version:"4.0.1"};var b=function(){if("undefined"!==typeof window.s_c_il)for(var g=0,c;g<window.s_c_il.length;g++)if(c=window.s_c_il[g],c._c&&"s_c"===c._c)return c}();"undefined"!==typeof b&&(b.contextData.getQueryParam="4.0");if(a){d=d||"";f=(f||"undefined"!==typeof b&&b.pageURL||location.href)+"";(4<d.length||-1<d.indexOf("="))&&f&&4>f.length&&(b=d,d=f,f=b);b="";for(var m=a.split(","),r=m.length,k=0;k<r;k++)a=n(m[k],f),"string"===typeof a?(a=-1<a.indexOf("#")?a.substring(0,a.indexOf("#")):a,b+=b?d+a:a):b=""===b?a:b+(d+a);return b}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De methode `getQueryParam` gebruikt de volgende argumenten:

* **`qsp`** (vereist): Een door komma&#39;s gescheiden lijst met parameters voor queryreeksen die moet worden gezocht binnen de URL. Het is niet hoofdlettergevoelig.
* **`de`** (optioneel): Het scheidingsteken dat moet worden gebruikt als meerdere parameters van queryreeksen overeenkomen. Heeft als standaardwaarde een lege tekenreeks.
* **`url`** (optioneel): Een aangepaste URL, tekenreeks of variabele waaruit de parameterwaarden voor de queryreeks moeten worden geëxtraheerd. Wordt standaard ingesteld op `window.location`.

Als deze methode wordt aangeroepen, wordt een waarde geretourneerd die afhankelijk is van de bovenstaande argumenten en de URL:

* Wanneer geen overeenkomende parameter voor een querytekenreeks wordt gevonden, retourneert de methode een lege tekenreeks.
* Wanneer een overeenkomende parameter voor een querytekenreeks wordt gevonden, retourneert de methode de parameterwaarde voor de queryreeks.
* Als een overeenkomende parameter voor een querytekenreeks wordt gevonden maar de waarde leeg is, retourneert de methode `true`.
* Wanneer meerdere overeenkomende parameters voor queryreeksen worden gevonden, retourneert de methode een tekenreeks met elke parameterwaarde die door de tekenreeks in het argument `de` wordt gescheiden.

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

**Opmerking:** de insteekmodule vervangt de URL naar het hashteken van de controle door een vraagteken als er geen vraagteken bestaat.  Als de URL een vraagteken bevat dat voor het hashteken komt, vervangt de insteekmodule de URL naar het hashteken van de controle door een en-teken;

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

**Opmerking:** de derde parameter kan elke tekenreeks/variabele zijn die de code gebruikt om de parameters van de queryreeks te zoeken in

De volgende code stelt s.eVar2 in op &quot;123456|trackingcode1|true|300&quot;:

```js
s.eVar2=s.getQueryParam('ecid,cid,location,pos','|',s.testURL);
```

* De waarde 123456 is afkomstig van de parameter ecid in de variabele s.testURL
* De waarde van trackingCode1 is afkomstig van de parameter cid in de variabele s.testURL
* De waarde true is afkomstig van het bestaan (maar niet de waarde) van de parameter location na het hash-teken in de variabele s.testURL

De waarde 300 is afkomstig van de waarde van de parameter pos in de variabele s.testURL

## Versiehistorie

### 4.0.1 (26 maart 2021)

* Bijgewerkte kwestie waar undefined in plaats van &quot;&quot;werd teruggekeerd als vraagparam niet in het vraagkoord aanwezig was.

### 4.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.
* Afhankelijkheden van pt-insteekmodule verwijderd.

### 3.3 (24 september 2019)

* Overbodige logica om codegrootte te verkleinen

### 3.2 (15 mei 2018)

* `findParameterValue`- en `getParameterValue`-functies verplaatst naar de functie `getQueryParam`

### 3.1 (10 mei 2018)

* Probleem verholpen met het vastleggen van parameters voor queryreeksen zonder waarde

### 3.0 (16 april 2018)

* Puntrelease (opnieuw gecompileerd, kleiner codeformaat).
* De naam van hulplijnfuncties is gewijzigd in `findParameterValue` en `getParameterValue` voor leesbaarheidsdoeleinden.
* Verwijderde de behoefte om een argument toe te voegen om parameters in het knoeiboel te vinden URL

### 2.5 (8 januari 2016)

* Compatibel met zowel H-code als AppMeasurement (vereist `s.pt` met AppMeasurement).

### 2,4

* De parameter `h` is toegevoegd, zodat de code parameters van queryreeksen kan zoeken die na het hash-teken (`#`) zijn gevonden

### 2,3

* Probleem verholpen waarbij de insteekmodule alleen werkte toen de hash aanwezig was na de trackingcode. Dit probleem is nu opgelost.

### 2,2

* Verwijdert nu hash-tekens (en alles daarna) uit de geretourneerde waarde

### 2,1

* Compatibel met H.10-code
