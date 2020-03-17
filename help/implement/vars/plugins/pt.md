---
title: pt
description: Hiermee wordt een functie uitgevoerd op een lijst met variabelen.
translation-type: tm+mt
source-git-commit: 180ad544541f25d02b3a257559bc045abed7387b

---


# Adobe-insteekmodule: pt

> [!IMPORTANT] Deze plug-in wordt geleverd door Adobe Consulting als een hoffelijkheid om u te helpen meer waarde te krijgen van Adobe Analytics. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

De `pt` insteekmodule voert een functie of methode uit in een lijst met analytische variabelen. U kunt de `clearVars` methode bijvoorbeeld selectief op verschillende variabelen uitvoeren zonder de methode telkens handmatig aan te roepen. Verscheidene andere stop-ins hangen van deze code af correct in werking te stellen. Deze insteekmodule is niet nodig als u een specifieke functie niet hoeft uit te voeren voor meer dan één variabele Analytics tegelijk, of als u geen afhankelijke insteekmodules gebruikt.

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
   * Type handeling: pt initialiseren
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

Kopieer en plak de volgende code ergens in het AppMeasurement-bestand nadat het analytics tracking-object is geïnstantieerd (met `s_gi`). Door opmerkingen en versienummers van de code in uw implementatie te behouden, kan Adobe eventuele problemen oplossen.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: pt v2.01 */
 s.pt=function(l,de,cf,fa){if(l&&this[cf]){l=l.split(de||",");de=l.length;for(var e,c=0;c<de;c++)if(e=this[cf](l[c],fa))return e}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `pt` methode gebruikt de volgende argumenten:

* **`l`** (vereist, tekenreeks): Een lijst met variabelen die de functie in het `cf` argument kan gebruiken.
* **`de`** (optioneel, tekenreeks): Het scheidingsteken dat de lijst met variabelen in het `l` argument scheidt. Heeft als standaardwaarde een komma (`,`).
* **`cf`** (vereist, tekenreeks): De naam van de callback functie in het voorwerp AppMeasurement die tegen elk van de variabelen in het `l` argument moet worden geroepen.
* **`fa`** (optioneel, tekenreeks): Als de functie in het `cf` argument extra argumenten roept wanneer het loopt, omvat hen hier. Wordt standaard ingesteld op `undefined`.

Wanneer deze methode wordt aangeroepen, wordt een waarde geretourneerd als de callback-functie (in het `cf` argument) een waarde retourneert.

## Voorbeelden van aanroepen

### Voorbeeld 1

De volgende code maakt deel uit van de stop getQueryParam.  Het stelt de getParameterValue helperfunctie tegen elk van de zeer belangrijk-waardeparen in werking die in het querystring van URL (fullQueryString) bevat zijn.  Als u elk sleutelwaardepaar anders wilt extraheren, moet fullQueryString worden gescheiden en worden gesplitst met het teken &quot;&amp;&quot; en ampersand. De parameterKey verwijst naar de parameter van het vraagkoord dat de stop - binnen specifiek probeert uit het vraagkoord te halen

```javascript
returnValue = s.pt(fullQueryString, "&", "getParameterValue", parameterKey)
```

De bovenstaande regel is een sneltoets voor het uitvoeren van code die op het volgende lijkt:

```js
var returnValue = "",
  parameters = fullQueryString.split("&"),
  parametersLength = parameters.length;
for(var i = 0; i < parametersLength; i++)
{
  returnValue = s.getParameterValue(parameters[i], parameterKey);
  if(returnValue !== "") break;
}
```

## Versiehistorie

### 2.01 (24 september 2019)

* Kleine wijzigingen in code om de totale grootte te verkleinen

### 2.0 (17 april 2018)

* Puntrelease (opnieuw gecompileerd, kleiner codeformaat).
* Toegevoegde ondersteuning voor zowel H-code als AppMeasurement.

### 1.0 (23 september 2013)

* Eerste release.
