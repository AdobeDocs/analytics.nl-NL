---
title: afbreken
description: De abortvariabele is een Booleaanse waarde die voorkomt dat een hit wordt verzonden naar Adobe-servers voor gegevensverzameling.
feature: Appmeasurement Implementation
exl-id: e4e25a89-272b-4444-b52b-c7fe2478ff30
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 0%

---

# afbreken

De variabele `abort` is een Booleaanse waarde die kan voorkomen dat de volgende volgaanroep naar Adobe wordt verzonden. De Web SDK beschikt over vergelijkbare functionaliteit waarmee u `false` kunt retourneren voordat een XDM-gebeurtenis wordt verzonden.

## Het verzenden van een gebeurtenis annuleren met de extensie Web SDK

Gebruik de [!UICONTROL On before event send callback] code-editor en retourneer `false` .

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder [!UICONTROL Adobe Experience Platform Web SDK] .
1. Klik onder [!UICONTROL Data Collection] op de knop **[!UICONTROL Edit on before event send callback code]** .
1. Plaats de volgende code in de code-editor onder alle omstandigheden waarin u het verzenden van gegevens naar Edge wilt afbreken:

```js
return false;
```

## Annuleer het verzenden van een gebeurtenis manueel het uitvoeren van het Web SDK

Gebruik de callback en return `onBeforeEventSend` `false` . Zie [ Veranderend gebeurtenissen globaal ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#modifying-events-globally) in de documentatie van SDK van het Web voor meer informatie.

```js
alloy("configure"), {
    "onBeforeEventSend": function(content) {
        return false;
    }
}
```

## De abortvariabele gebruiken in de Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de AppMeasurement-syntaxis.

## s.abort in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De variabele `s.abort` is een booleaanse waarde. De standaardwaarde is `false` .

* Indien ingesteld op `true` , verzendt de volgende volgaanroep ( [`t()`](../functions/t-method.md) of [`tl()`](../functions/tl-method.md) ) geen gegevens naar Adobe.
* Indien ingesteld op `false` of niet gedefinieerd, heeft deze variabele geen effect.

```js
s.abort = true;
```

>[!NOTE]
>
>De variabele `abort` wordt na elke volgende aanroep opnieuw ingesteld op `false` . Als u volgende volgaanroepen op dezelfde pagina wilt afbreken, stelt u `abort` opnieuw in op `true` .

De variabele `abort` kan worden ingesteld in de functie [`doPlugins()`](../functions/doplugins.md) . Dit is de laatste functie die wordt uitgevoerd voordat een afbeeldingsaanvraag naar Adobe wordt verzonden. Dit voorbeeld werkt op ongeveer dezelfde manier als de callback van `onBeforeEventSend` via de Web SDK.

```js
s.doPlugins = function(s) {
    s.campaign = s.Util.getQueryParam("cid");
    if ((!s.campaign) && (!s.events)) {
        s.abort = true;
    }
};
```

U kunt de logica centraliseren die u gebruikt om activiteit te identificeren die u niet wilt volgen, zoals sommige douaneverbindingen of externe verbindingen in vertoningsadvertenties.
