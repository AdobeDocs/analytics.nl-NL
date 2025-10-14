---
title: pt
description: Hiermee wordt een functie uitgevoerd op een lijst met variabelen.
feature: Appmeasurement Implementation
exl-id: 2ab24a8e-ced3-43ea-bdb5-7c39810e4102
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 0%

---

# Adobe-insteekmodule: pt

{{plug-in}}

De plug-in `pt` voert een functie of methode uit in een lijst met variabelen voor Analytics. U kunt bijvoorbeeld de functie [`clearVars`](../functions/clearvars.md) selectief op verschillende variabelen uitvoeren zonder de functie telkens handmatig aan te roepen. Verscheidene andere stop-ins hangen van deze code af correct in werking te stellen. Deze insteekmodule is niet nodig als u een specifieke functie niet hoeft uit te voeren voor meer dan één variabele Analytics tegelijk, of als u geen afhankelijke insteekmodules gebruikt.

## De insteekmodule installeren met de extensie Web SDK of Web SDK

Deze insteekmodule wordt nog niet ondersteund voor gebruik in de Web SDK.

## De insteekmodule installeren met de Adobe Analytics-extensie

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken in Adobe Analytics.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop [!UICONTROL Catalog]
1. De extensie [!UICONTROL Common Analytics Plugins] installeren en publiceren
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: geen
   * Event: Core - bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: veelgebruikte plug-ins voor Analytics
   * Type handeling: pt initialiseren
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met aangepaste code-editor

Als u niet de Gemeenschappelijke Insteekmodule van Analytics wilt gebruiken, kunt u de redacteur van de douanecode gebruiken.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste eigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder de extensie Adobe Analytics.
1. Vouw de accordeon [!UICONTROL Configure tracking using custom code] uit, zodat de knop [!UICONTROL Open Editor] zichtbaar wordt.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

## Plug-in installeren met AppMeasurement

Kopieer en plak de volgende code ergens in het AppMeasurement-bestand nadat het object Analytics tracking is geïnstantieerd (met [`s_gi`](../functions/s-gi.md) ). Door opmerkingen en versienummers van de code in uw implementatie te behouden, helpt Adobe bij het oplossen van mogelijke problemen.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: pt v3.0 */
function pt(l,de,cf,fa){var b=l,d=de,f=cf,g=fa;if("-v"===b)return{plugin:"pt",version:"3.0"};a:{if("undefined"!==typeof window.s_c_il){var a=0;for(var c;a<window.s_c_il.length;a++)if(c=window.s_c_il[a],c._c&&"s_c"===c._c){a=c;break a}}a=void 0}if("undefined"!==typeof a&&(a.contextData.pt="3.0",b&&a[f])){b=b.split(d||",");d=b.length;for(var e=0;e<d;e++)if(c=a[f](b[e],g))return c}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De functie `pt` gebruikt de volgende argumenten:

* **`l`** (required, string): Een lijst met variabelen die de functie in het `cf` argument kan gebruiken.
* **`de`** (optioneel, tekenreeks): het scheidingsteken tussen de lijst met variabelen in het argument `l` . Heeft als standaardwaarde een komma (`,`).
* **`cf`** (required, string): De naam van de callback functie in het AppMeasurement-object die moet worden aangeroepen voor elk van de variabelen in het `l` -argument.
* **`fa`** (optioneel, tekenreeks): Als de functie in het argument `cf` aanvullende argumenten aanroept wanneer deze wordt uitgevoerd, neemt u deze hier op. Wordt standaard ingesteld op `undefined` .

Als deze functie wordt aangeroepen, wordt een waarde geretourneerd als de callback-functie (in het argument `cf` ) een waarde retourneert.

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

### 2.0 april 2018

* Puntrelease (opnieuw gecompileerd, kleiner codeformaat).
* Toegevoegde ondersteuning voor zowel H-code als AppMeasurement.

### 1.0 (23 september 2013)

* Eerste release.
