---
title: t
description: Verzend een pagina mening het volgen vraag naar Adobe.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# t()

De `t()` methode is een belangrijk basisonderdeel van Adobe Analytics. Alle analytische variabelen die op de pagina zijn gedefinieerd, worden gecompileerd tot een verzoek om een afbeelding en die gegevens worden naar Adobe-servers voor gegevensverzameling verzonden.

Neem bijvoorbeeld de volgende JavaScript-code:

```js
// Instantiate the tracking object
var s = s_gi("examplersid");

// Define config variables and page variables
s.trackingServerSecure = "data.example.com";
s.eVar1 = "Example dimension value";

// Compile the variables on the page into an image request to Adobe
s.t();
```

Bij het uitvoeren van de `t()` methode worden alle gedefinieerde analytische variabelen gebruikt en wordt op basis van deze variabelen een URL gemaakt. Sommige variabelen van de Analyse bepalen URL van het beeld, terwijl andere variabelen vraagkoordparameterwaarden bepalen.

```text
https://data.example.com/b/ss/examplersid/1/?v1=Example%20dimension%20value
```

Adobe ontvangt de afbeeldingsaanvraag en parseert vervolgens de parameters voor de aanvraagkoptekst, de URL en de queryreeks. Servers voor gegevensverzameling retourneren vervolgens een transparante afbeelding van 1 x 1 pixels, die onzichtbaar op uw site wordt weergegeven.

## Aanroep voor bijhouden van paginaweergave in Adobe Experience Platform Launch

Bij starten wordt een specifieke locatie ingesteld die een aanroep voor het bijhouden van de paginaweergave bevat.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions]op het pictogram ‘+’
5. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op Adobe Analytics en de knop [!UICONTROL Action Type] To Send Beacon.
6. Klik op het `s.t()` keuzerondje.

## s.t()-methode in de aangepaste code-editor van AppMeasurement en Launch

Roep de `s.t()` methode aan wanneer u een volgende vraag naar Adobe wilt verzenden.

```js
s.t();
```

U kunt een object ook als argument gebruiken om variabelewaarden te overschrijven. Zie [variabele overschrijvingen](../../js/overrides.md) voor meer informatie.

```js
var y = new Object();
y.eVar1 = "Override value";
s.t(y);
```

>[!NOTE] In eerdere versies van AppMeasurement werden verschillende coderegels gebruikt om deze functie aan te roepen. In de aanvullende code zijn historisch tijdelijke oplossingen voor verschillende browsers opgenomen. Dit codeblok is niet langer vereist voor standaardisering en beste praktijken in moderne browsers. Alleen de methode die u nu aanroept, `s.t()` is nodig.
