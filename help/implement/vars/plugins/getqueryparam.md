---
title: getQueryParam
description: Haal de waarde van de parameter van het vraagkoord van een URL uit.
feature: Variables
exl-id: d2d542d1-3a18-43d9-a50d-c06d8bd473b8
source-git-commit: 7c7a7d8add9edb1538df12b440bc0a15f09efe5e
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 1%

---

# Adobe-plug-in: getQueryParam

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

De `getQueryParam` Met de insteekmodule kunt u de waarde extraheren van elke parameter voor queryreeksen in een URL. Het is nuttig om campagnecodes, zowel intern als extern, uit het landen van pagina URLs te halen. Het is ook nuttig wanneer het halen van onderzoekstermijnen of andere parameters van het vraagkoord.

Deze plug-in biedt robuuste functies voor het parseren van complexe URL&#39;s, waaronder hashes en URL&#39;s die meerdere parameters voor queryreeksen bevatten. Als u slechts eenvoudige de parameterbehoeften van het vraagkoord hebt, adviseert Adobe het gebruiken van de URL parametereigenschappen gebruikend het Web SDK of de uitbreiding van Adobe Analytics of [`Util.getQueryParam()`](../functions/util-getqueryparam.md) methode die is opgenomen in AppMeasurement.

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
    * Action Type: Initialize getQueryParam
1. Save and publish the changes to the rule.-->

## Plug-in installeren met aangepaste code-editor

Als u de extensie van de plug-in niet wilt gebruiken, kunt u de aangepaste code-editor gebruiken.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder de extensie Adobe Analytics.
1. Breid uit [!UICONTROL Configure tracking using custom code] accordion, die de [!UICONTROL Open Editor] knop.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getQueryParam v4.0.1  */
function getQueryParam(a,d,f){function n(g,c){c=c.split("?").join("&");c=c.split("#").join("&");var e=c.indexOf("&");if(g&&(-1<e||c.indexOf("=")>e)){e=c.substring(e+1);e=e.split("&");for(var h=0,p=e.length;h<p;h++){var l=e[h].split("="),q=l[1];if(l[0].toLowerCase()===g.toLowerCase())return decodeURIComponent(q||!0)}}return""}if("-v"===a)return{plugin:"getQueryParam",version:"4.0.1"};var b=function(){if("undefined"!==typeof window.s_c_il)for(var g=0,c;g<window.s_c_il.length;g++)if(c=window.s_c_il[g],c._c&&"s_c"===c._c)return c}();"undefined"!==typeof b&&(b.contextData.getQueryParam="4.0");if(a){d=d||"";f=(f||"undefined"!==typeof b&&b.pageURL||location.href)+"";(4<d.length||-1<d.indexOf("="))&&f&&4>f.length&&(b=d,d=f,f=b);b="";for(var m=a.split(","),r=m.length,k=0;k<r;k++)a=n(m[k],f),"string"===typeof a?(a=-1<a.indexOf("#")?a.substring(0,a.indexOf("#")):a,b+=b?d+a:a):b=""===b?a:b+(d+a);return b}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `getQueryParam` function gebruikt de volgende argumenten:

* **`qsp`** (vereist): Een door komma&#39;s gescheiden lijst met parameters voor queryreeksen die moet worden gezocht binnen de URL. Het is niet hoofdlettergevoelig.
* **`de`** (optioneel): Het scheidingsteken dat moet worden gebruikt als meerdere parameters van queryreeksen overeenkomen. Heeft als standaardwaarde een lege tekenreeks.
* **`url`** (optioneel): Een aangepaste URL, tekenreeks of variabele waaruit de parameterwaarden voor de queryreeks moeten worden geëxtraheerd. Standaardwaarden: `window.location`.

Als deze functie wordt aangeroepen, wordt een waarde geretourneerd die afhankelijk is van de bovenstaande argumenten en de URL:

* Als er geen overeenkomende parameter voor een querytekenreeks wordt gevonden, retourneert de functie een lege tekenreeks.
* Als een overeenkomende parameter voor een querytekenreeks wordt gevonden, retourneert de functie de parameterwaarde voor de queryreeks.
* Als een overeenkomende parameter voor een querytekenreeks wordt gevonden maar de waarde leeg is, wordt de functie geretourneerd `true`.
* Als er meerdere overeenkomende parameters voor queryreeksen worden gevonden, retourneert de functie een tekenreeks met elke parameterwaarde die door de tekenreeks in het dialoogvenster `de` argument.

## Voorbeelden

```js
// Given the URL https://example.com/?cid=trackingcode
// Sets the campaign variable to "trackingcode"
s.campaign = getQueryParam('cid');

// Given the URL https://example.com/?cid=trackingcode&ecid=123
// Sets the campaign variable to "trackingcode:123"
s.campaign = getQueryParam('cid,ecid',':');

// Given the URL https://example.com/?cid=trackingcode&ecid=123
// Sets the campaign variable to "trackingcode123"
s.campaign = getQueryParam('cid,ecid');

// Given the URL https://example.com/?cid=trackingcode&ecid=123#location
// Sets the campaign variable to "123"
s.campaign = getQueryParam('ecid');

// Given the URL https://example.com/#location&cid=trackingcode&ecid=123
// Sets the campaign variable to "123"
// The plug-in replaces the URL's hash character with a question mark if a question mark doesn't exist.
s.campaign = getQueryParam('ecid');

// Given the URL https://example.com
// Does not set the campaign variable to a value.
s.pageURL = "https://example.com/?cid=trackingcode";
s.campaign = getQueryParam('cid');

// Given the URL https://example.com
// Sets the campaign variable to "trackingcode"
s.pageURL = "https://example.com/?cid=trackingcode";
s.campaign = getQueryParam('cid','',s.pageURL);

// Given the URL https://example.com
// Sets eVar2 to "123|trackingcode|true|300"
s.eVar1 = "https://example.com/?cid=trackingcode&ecid=123#location&pos=300";
s.eVar2 = getQueryParam('ecid,cid,location,pos','|',s.eVar1);
```

## Versiehistorie

### 4.0.1 (26 maart 2021)

* Bijgewerkte kwestie waar undefined in plaats van &quot;&quot;werd teruggekeerd als vraagparam niet in het vraagkoord aanwezig was.

### 4.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.
* Afhankelijkheden van pt-insteekmodule verwijderd.

### 3.3 (24 september 2019)

* Overbodige logica om codegrootte te verkleinen

### 3.2 (15 mei 2018)

* Verplaatst `findParameterValue` en `getParameterValue` in de `getQueryParam` function

### 3.1 (10 mei 2018)

* Probleem verholpen met het vastleggen van parameters voor queryreeksen zonder waarde

### 3.0 (16 april 2018)

* Puntrelease (opnieuw gecompileerd, kleiner codeformaat).
* De naam van hulplijnfuncties wijzigen in `findParameterValue` en `getParameterValue` voor leesbaarheidsdoeleinden.
* Verwijderde de behoefte om een argument toe te voegen om parameters in het knoeiboel te vinden URL

### 2.5 (8 januari 2016)

* Compatibel met zowel H-code als AppMeasurement (vereist `s.pt` met AppMeasurement).

### 2,4

* De `h` parameter, waardoor de code kan zoeken naar parameters van queryreeksen die na de hash (`#`) teken

### 2,3

* Probleem verholpen waarbij de insteekmodule alleen werkte toen de hash aanwezig was na de trackingcode. Dit probleem is nu opgelost.

### 2,2

* Verwijdert nu hash-tekens (en alles daarna) uit de geretourneerde waarde

### 2,1

* Compatibel met H.10-code
