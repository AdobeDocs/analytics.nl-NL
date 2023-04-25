---
title: t
description: Verzend een vraag van de paginamening het volgen aan Adobe.
feature: Variables
exl-id: c4f5b9e2-57a3-4d89-8378-39b7a4737afc
source-git-commit: 6de20d2fbbab6ded6c92f0c6f3536671f4b2ae46
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 0%

---

# t()

De `t()` Deze methode is een belangrijk kernonderdeel van Adobe Analytics. Het neemt alle variabelen die van Analytics op de pagina worden bepaald, compileert hen in een beeldverzoek, en verzendt die gegevens naar de servers van de Adobe- gegevensinzameling.

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

De `t()` Alle gedefinieerde variabelen voor Analytics worden gebruikt en op basis van deze variabelen een URL geformuleerd. Sommige variabelen van de Analyse bepalen URL van het beeld, terwijl andere variabelen vraagkoordparameterwaarden bepalen.

```text
https://data.example.com/b/ss/examplersid/1/?v1=Example%20dimension%20value
```

Adobe ontvangt het beeldverzoek, dan ontleedt de verzoekkopbal, URL, en de parameters van het vraagkoord. Servers voor gegevensverzameling retourneren vervolgens een transparante afbeelding van 1 x 1 pixels, die onzichtbaar op uw site wordt weergegeven.

## Gebeurtenis verzenden met de Web SDK-extensie

Gebruik een handeling om het verzenden van XDM-gebeurtenisgegevens naar Adobe te configureren. De DataStream ontvangt deze gegevens, past om het even welke gevormde afbeeldingen toe, en door:sturen die gegevens aan Adobe Analytics als het de toegevoegde dienst aan die DataStream is.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
1. Onder [!UICONTROL Actions], klikt u op de gewenste handeling of klikt u op de knop **&#39;+&#39;** pictogram om een handeling toe te voegen.
1. Stel de [!UICONTROL Extension] vervolgkeuzelijst naar **[!UICONTROL Adobe Experience Platform Web SDK]** en de [!UICONTROL Action Type] tot **[!UICONTROL Send event]**.

## Gebeurtenis handmatig verzenden met implementatie van de Web SDK

Gebruik de `sendEvent` gebruiken om gegevens naar Adobe te verzenden. De DataStream ontvangt deze gegevens, past om het even welke gevormde afbeeldingen toe, en door:sturen die gegevens aan Adobe Analytics als het de toegevoegde dienst aan die DataStream is.

```js
alloy("sendEvent", {
  "xdm": {}
});
```

Zie [Gebeurtenissen bijhouden](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html) in de documentatie van SDK van het Web voor meer informatie.

## Aanroep voor bijhouden van paginaweergave met de Adobe Analytics-extensie

De extensie Adobe Analytics in Adobe Experience Platform Data Collection heeft een specifieke locatie ingesteld die een aanroep voor het bijhouden van de paginaweergave bevat.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
1. Onder [!UICONTROL Actions], klikt u op de gewenste handeling of klikt u op de knop **&#39;+&#39;** pictogram om een handeling toe te voegen.
1. Stel de [!UICONTROL Extension] vervolgkeuzelijst naar **[!UICONTROL Adobe Analytics]** en de [!UICONTROL Action Type] tot **[!UICONTROL Send Beacon]**.
1. Klik op de knop `s.t()` keuzerondje.

## s.t()-methode in AppMeasurement en de aangepaste code-editor van de extensie Analytics

Roep de `s.t()` methode wanneer u een volgende vraag naar Adobe wilt verzenden.

```js
s.t();
```

U kunt een object ook als argument gebruiken om variabelewaarden te overschrijven. Zie [variabele overschrijvingen](../../js/overrides.md) voor meer informatie .

```js
var y = new Object();
y.eVar1 = "Override value";
s.t(y);
```

>[!NOTE]
>
>In eerdere versies van AppMeasurement werden verschillende coderegels gebruikt om deze functie aan te roepen. In de aanvullende code zijn historisch tijdelijke oplossingen voor verschillende browsers opgenomen. Dit codeblok is niet langer vereist voor standaardisering en beste praktijken in moderne browsers. Alleen de methodeaanroep `s.t()` is nu nodig.
