---
title: pt
description: Hiermee wordt een functie uitgevoerd op een lijst met variabelen.
feature: Variables
exl-id: 2ab24a8e-ced3-43ea-bdb5-7c39810e4102
source-git-commit: c53f886d5329e2a3b5023f9396c3aa2360a86901
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 0%

---

# Adobe-plug-in: pt

{{plug-in}}

De `pt` Hiermee wordt een functie of methode uitgevoerd in een lijst met analytische variabelen. U kunt bijvoorbeeld selectief de opdracht [`clearVars`](../functions/clearvars.md) op verschillende variabelen worden uitgevoerd zonder de functie telkens handmatig aan te roepen. Verscheidene andere stop-ins hangen van deze code af correct in werking te stellen. Deze insteekmodule is niet nodig als u een specifieke functie niet hoeft uit te voeren voor meer dan één variabele Analytics tegelijk, of als u geen afhankelijke insteekmodules gebruikt.

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
    * Action Type: Initialize pt
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
/* Adobe Consulting Plugin: pt v3.0 */
function pt(l,de,cf,fa){var b=l,d=de,f=cf,g=fa;if("-v"===b)return{plugin:"pt",version:"3.0"};a:{if("undefined"!==typeof window.s_c_il){var a=0;for(var c;a<window.s_c_il.length;a++)if(c=window.s_c_il[a],c._c&&"s_c"===c._c){a=c;break a}}a=void 0}if("undefined"!==typeof a&&(a.contextData.pt="3.0",b&&a[f])){b=b.split(d||",");d=b.length;for(var e=0;e<d;e++)if(c=a[f](b[e],g))return c}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `pt` function gebruikt de volgende argumenten:

* **`l`** (vereist, tekenreeks): Een lijst met variabelen die de functie bevat in de `cf` argument kan worden uitgevoerd tegen.
* **`de`** (optioneel, tekenreeks): Het scheidingsteken dat de lijst met variabelen in het dialoogvenster `l` argument. Heeft als standaardwaarde een komma (`,`).
* **`cf`** (vereist, tekenreeks): De naam van de callback functie in het voorwerp AppMeasurement die tegen elk van de variabelen in moet worden geroepen `l` argument.
* **`fa`** (optioneel, tekenreeks): Als de functie in de `cf` Deze argumenten vragen om aanvullende argumenten wanneer deze worden uitgevoerd. Standaardwaarden: `undefined`.

Als deze functie wordt aangeroepen, wordt een waarde geretourneerd als de callback-functie (in het gedeelte `cf` argument) retourneert een waarde.

## Voorbeelden van aanroepen

### Voorbeeld 1

De volgende code maakt deel uit van de stop getQueryParam.  Het stelt de getParameterValue helperfunctie tegen elk van de zeer belangrijk-waardeparen in werking die in het querystring van URL (fullQueryString) bevat zijn.  Als u elk sleutelwaardepaar anders wilt extraheren, moet fullQueryString worden gescheiden en worden gesplitst met het teken &quot;&amp;&quot; en ampersand. De parameterKey verwijst naar de parameter van het vraagkoord dat de stop - binnen specifiek probeert uit het vraagkoord te halen

```js
returnValue = pt(fullQueryString, "&", "getParameterValue", parameterKey)
```

De bovenstaande regel is een sneltoets voor het uitvoeren van code die op het volgende lijkt:

```js
var returnValue = "",
  parameters = fullQueryString.split("&"),
  parametersLength = parameters.length;
for(var i = 0; i < parametersLength; i++)
{
  returnValue = getParameterValue(parameters[i], parameterKey);
  if(returnValue !== "") break;
}
```

## Versiehistorie

### 3.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 2.01 (24 september 2019)

* Kleine wijzigingen in code om de totale grootte te verkleinen

### 2.0 (17 april 2018)

* Puntrelease (opnieuw gecompileerd, kleiner codeformaat).
* Toegevoegde ondersteuning voor zowel H-code als AppMeasurement.

### 1.0 (23 september 2013)

* Eerste release.
