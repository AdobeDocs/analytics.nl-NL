---
title: getQueryParam
description: Haal de waarde van de parameter van het vraagkoord van een URL uit.
translation-type: tm+mt
source-git-commit: 03c3a954c40d17f11f4f80ee3a378fd43948cc5c
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 1%

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
/* Adobe Consulting Plugin: getQueryParam v4.0 */
function getQueryParam(b,c,d){function h(b,a){a=a.split("?").join("&");a=a.split("#").join("&");var c=a.indexOf("&");if(b&&(-1<c||a.indexOf("=")>c)){c=a.substring(c+1);c=c.split("&");for(var d=0,k=c.length;d<k;d++){var f=c[d].split("="),e=f[1];if(f[0].toLowerCase()===b.toLowerCase())return decodeURIComponent(e||!0)}}}if("-v"===b)return{plugin:"getQueryParam",version:"4.0"};var a=function(){if("undefined"!==typeof window.s_c_il)for(var a=0,b;a<window.s_c_il.length;a++)if(b=window.s_c_il[a],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof a&&(a.contextData.getQueryParam="4.0");if(b){c=c||"";d=(d||"undefined"!==typeof a&&a.pageURL||location.href)+"";(4<c.length||-1<c.indexOf("="))&&d&&4>d.length&&(a=c,c=d,d=a);a="";for(var g=b.split(","),l=g.length,e=0;e<l;e++)b=h(g[e],d),"string"===typeof b?(b=-1<b.indexOf("#")?b.substring(0,b.indexOf("#")):b,a+=a?c+b:b):a=""===a?b:a+(c+b);return a}};
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

### Voorbeeld 2

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

### 4.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.
* Afhankelijkheden van `pt`-plug-in zijn verwijderd.

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
