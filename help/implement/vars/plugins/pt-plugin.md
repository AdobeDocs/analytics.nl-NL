---
title: pt
description: Hiermee wordt een functie uitgevoerd op een lijst met variabelen.
exl-id: 2ab24a8e-ced3-43ea-bdb5-7c39810e4102
source-git-commit: ab078c5da7e0e38ab9f0f941b407cad0b42dd4d1
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 0%

---

# Adobe-plug-in: pt

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de insteekmodule `pt` wordt een functie of methode op een lijst met variabelen voor Analytics uitgevoerd. U kunt bijvoorbeeld de functie [`clearVars`](../functions/clearvars.md) selectief op verschillende variabelen uitvoeren zonder de functie telkens handmatig aan te roepen. Verscheidene andere stop-ins hangen van deze code af correct in werking te stellen. Deze insteekmodule is niet nodig als u een specifieke functie niet hoeft uit te voeren voor meer dan één variabele Analytics tegelijk, of als u geen afhankelijke insteekmodules gebruikt.

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
   * Type handeling: pt initialiseren
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
/* Adobe Consulting Plugin: pt v3.0 */
function pt(l,de,cf,fa){var b=l,d=de,f=cf,g=fa;if("-v"===b)return{plugin:"pt",version:"3.0"};a:{if("undefined"!==typeof window.s_c_il){var a=0;for(var c;a<window.s_c_il.length;a++)if(c=window.s_c_il[a],c._c&&"s_c"===c._c){a=c;break a}}a=void 0}if("undefined"!==typeof a&&(a.contextData.pt="3.0",b&&a[f])){b=b.split(d||",");d=b.length;for(var e=0;e<d;e++)if(c=a[f](b[e],g))return c}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De functie `pt` gebruikt de volgende argumenten:

* **`l`** (vereist, tekenreeks): Een lijst met variabelen die de functie in het  `cf` argument kan gebruiken.
* **`de`** (optioneel, tekenreeks): Het scheidingsteken dat de lijst met variabelen in het  `l` argument scheidt. Heeft als standaardwaarde een komma (`,`).
* **`cf`** (vereist, tekenreeks): De naam van de callback functie in het voorwerp AppMeasurement die tegen elk van de variabelen in het  `l` argument moet worden geroepen.
* **`fa`** (optioneel, tekenreeks): Als de functie in het  `cf` argument om extra argumenten roept wanneer het loopt, omvat hen hier. Wordt standaard ingesteld op `undefined`.

Het roepen van deze functie keert een waarde terug als de callback functie (in het `cf` argument) een waarde terugkeert.

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
