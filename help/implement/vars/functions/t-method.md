---
title: t
description: Verzend een vraag van de paginamening het volgen naar Adobe.
feature: Appmeasurement Implementation
exl-id: c4f5b9e2-57a3-4d89-8378-39b7a4737afc
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# t()

De methode `t()` is een belangrijke kerncomponent voor Adobe Analytics. Alle analysevariabelen die op de pagina zijn gedefinieerd, worden gecompileerd tot een verzoek om een afbeelding en die gegevens worden naar Adobe-servers voor gegevensverzameling verzonden.

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

Wanneer u de methode `t()` uitvoert, worden alle variabelen van Analytics gedefinieerd en wordt op basis van deze variabelen een URL gemaakt. Sommige variabelen van de Analyse bepalen URL van het beeld, terwijl andere variabelen vraagkoordparameterwaarden bepalen.

```text
https://data.example.com/b/ss/examplersid/1/?v1=Example%20dimension%20item
```

Adobe ontvangt de afbeeldingsaanvraag en parseert vervolgens de parameters voor de aanvraagheader, URL en queryreeks. Servers voor gegevensverzameling retourneren vervolgens een transparante afbeelding van 1 x 1 pixels, die onzichtbaar op uw site wordt weergegeven.

## Gebeurtenis verzenden met de extensie Web SDK

Gebruik een handeling om het verzenden van XDM-gebeurtenisgegevens naar Adobe te configureren. De DataStream ontvangt deze gegevens, past om het even welke gevormde afbeeldingen toe, en door:sturen die gegevens aan Adobe Analytics als het de toegevoegde dienst aan die DataStream is.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Ga naar het tabblad [!UICONTROL Rules] en klik vervolgens op de gewenste regel (of maak een regel).
1. Klik onder [!UICONTROL Actions] op de gewenste handeling of klik op het pictogram **&#39;+&#39;** om een handeling toe te voegen.
1. Stel de vervolgkeuzelijst [!UICONTROL Extension] in op **[!UICONTROL Adobe Experience Platform Web SDK]** en [!UICONTROL Action Type] op **[!UICONTROL Send event]** .

## Gebeurtenis handmatig verzenden met implementatie van de Web SDK

Gebruik de opdracht `sendEvent` om gegevens naar Adobe te verzenden. De DataStream ontvangt deze gegevens, past om het even welke gevormde afbeeldingen toe, en door:sturen die gegevens aan Adobe Analytics als het de toegevoegde dienst aan die DataStream is.

```js
alloy("sendEvent", {
  "xdm": {}
});
```

Zie [`sendEvent` ](https://experienceleague.adobe.com/nl/docs/experience-platform/web-sdk/commands/sendevent/overview) in de documentatie van SDK van het Web voor meer informatie.

## Aanroep voor bijhouden van paginaweergave met de Adobe Analytics-extensie

De extensie Adobe Analytics in Adobe Experience Platform Data Collection heeft een specifieke locatie ingesteld die een aanroep voor het bijhouden van de paginaweergave bevat.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Ga naar het tabblad [!UICONTROL Rules] en klik vervolgens op de gewenste regel (of maak een regel).
1. Klik onder [!UICONTROL Actions] op de gewenste actie of klik op het pictogram **&#39;+&#39;** om een actie toe te voegen.
1. Stel de vervolgkeuzelijst [!UICONTROL Extension] in op **[!UICONTROL Adobe Analytics]** en de vervolgkeuzelijst op [!UICONTROL Action Type] op **[!UICONTROL Send Beacon]** .
1. Klik op het keuzerondje `s.t()` .

## s.t()-methode in AppMeasurement en de aangepaste code-editor van de extensie Analytics

Roep de methode `s.t()` aan wanneer u een volgende aanroep naar Adobe wilt verzenden.

```js
s.t();
```

U kunt een object ook als argument gebruiken om variabelewaarden te overschrijven. Zie [ veranderlijke met voeten treedt ](../../js/overrides.md) voor meer informatie.

```js
var y = new Object();
y.eVar1 = "Override value";
s.t(y);
```

>[!NOTE]
>
>In eerdere versies van AppMeasurement werden verschillende coderegels gebruikt om deze functie aan te roepen. In de aanvullende code zijn historisch tijdelijke oplossingen voor verschillende browsers opgenomen. Dit codeblok is niet langer vereist voor standaardisering en beste praktijken in moderne browsers. Nu is alleen de methodeaanroep `s.t()` nodig.
