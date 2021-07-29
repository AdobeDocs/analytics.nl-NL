---
title: t
description: Verzend een vraag van de paginamening het volgen aan Adobe.
exl-id: c4f5b9e2-57a3-4d89-8378-39b7a4737afc
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# t()

De methode `t()` is een belangrijke kerncomponent voor Adobe Analytics. Het neemt alle variabelen die van Analytics op de pagina worden bepaald, compileert hen in een beeldverzoek, en verzendt die gegevens naar de servers van de Adobe- gegevensinzameling.

Neem bijvoorbeeld de volgende JavaScript-code:

```js
// Instantiate the tracking object
var s = s_gi("examplersid");

// Define config variables and page variables
s.trackingServerSecure = "data.example.com";
s.eVar1 = "Example dimension item";

// Compile the variables on the page into an image request to Adobe
s.t();
```

Wanneer u de methode `t()` uitvoert, worden alle gedefinieerde variabelen Analytics uitgevoerd en wordt op basis van deze variabelen een URL gemaakt. Sommige variabelen van de Analyse bepalen URL van het beeld, terwijl andere variabelen vraagkoordparameterwaarden bepalen.

```text
https://data.example.com/b/ss/examplersid/1/?v1=Example%20dimension%20value
```

Adobe ontvangt het beeldverzoek, dan ontleedt de verzoekkopbal, URL, en de parameters van het vraagkoord. Servers voor gegevensverzameling retourneren vervolgens een transparante afbeelding van 1 x 1 pixels, die onzichtbaar op uw site wordt weergegeven.

## Aanroep voor bijhouden van paginaweergave met tags in Adobe Experience Platform

De UI van de Inzameling van Gegevens heeft een specifieke plaats reeks een pagina mening volgende vraag.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions] op het pictogram &#39;+&#39;
5. Stel het [!UICONTROL Extension]-vervolgkeuzemenu in op Adobe Analytics en [!UICONTROL Action Type] op Band verzenden.
6. Klik op het keuzerondje `s.t()`.

## s.t()-methode in AppMeasurement en aangepaste code-editor

Roep de methode `s.t()` wanneer u een volgende vraag naar Adobe wilt verzenden.

```js
s.t();
```

U kunt een object ook als argument gebruiken om variabelewaarden te overschrijven. Zie [variabele overschrijvingen](../../js/overrides.md) voor meer informatie.

```js
var y = new Object();
y.eVar1 = "Override value";
s.t(y);
```

>[!NOTE]
>
>In eerdere versies van AppMeasurement werden verschillende coderegels gebruikt om deze functie aan te roepen. In de aanvullende code zijn historisch tijdelijke oplossingen voor verschillende browsers opgenomen. Dit codeblok is niet langer vereist voor standaardisering en beste praktijken in moderne browsers. Alleen de methodeaanroep `s.t()` is nu nodig.
