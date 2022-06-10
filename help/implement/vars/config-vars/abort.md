---
title: abort
description: De abortvariabele is een booleaanse waarde die voorkomt dat een hit wordt verzonden naar Adobe-gegevensverzamelingsservers.
feature: Variables
exl-id: e4e25a89-272b-4444-b52b-c7fe2478ff30
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# afbreken

De `abort` De variabele is een booleaanse waarde die kan verhinderen dat de volgende volgende volgvraag naar Adobe wordt verzonden. Er bestaat een vergelijkbare functionaliteit in de SDK van het web waarmee u kunt terugkeren `false` voordat een XDM-gebeurtenis wordt verzonden.

## Het verzenden van een gebeurtenis annuleren met de Web SDK-extensie

Gebruik de [!UICONTROL On before event send callback] code-editor en return `false`.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** knop onder [!UICONTROL Adobe Experience Platform Web SDK].
1. Onder [!UICONTROL Data Collection]klikt u op de knop **[!UICONTROL Edit on before event send callback code]** knop.
1. Plaats de volgende code in de code-editor onder alle omstandigheden waarin u het verzenden van gegevens naar Edge wilt afbreken:

```js
return false;
```

## Annuleer het verzenden van een gebeurtenis manueel het uitvoeren van SDK van het Web

Gebruik de `onBeforeEventSend` callback en return `false`. Zie [Gebeurtenissen globaal wijzigen](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#modifying-events-globally) in de documentatie van SDK van het Web voor meer informatie.

```js
alloy("configure"), {
    "onBeforeEventSend": function(content) {
        return false;
    }
}
```

## De abortvariabele gebruiken in de Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.abort in AppMeasurement en de de coderedacteur van de uitbreiding van de Analyse

De `s.abort` variable is a boolean. De standaardwaarde is `false`.

* Indien ingesteld op `true`, de volgende volgende volgende volgende volgvraag ([`t()`](../functions/t-method.md) of [`tl()`](../functions/tl-method.md)) verzendt geen gegevens naar Adobe.
* Indien ingesteld op `false` of niet gedefinieerd, heeft deze variabele geen effect.

```js
s.abort = true;
```

>[!NOTE]
>
>De `abort` variabele herstelt naar `false` na elke volgende vraag. Als u volgende het volgen vraag op de zelfde pagina moet afbreken, plaats `abort` tot `true` opnieuw.

De `abort` kan worden ingesteld in het dialoogvenster [`doPlugins()`](../functions/doplugins.md) -functie. Dit is de laatste functie die wordt uitgevoerd voordat een afbeeldingsaanvraag naar Adobe wordt verzonden. Dit voorbeeld werkt op dezelfde manier als het `onBeforeEventSend` callback die SDK van het Web gebruikt.

```js
s.doPlugins = function(s) {
    s.campaign = s.Util.getQueryParam("cid");
    if ((!s.campaign) && (!s.events)) {
        s.abort = true;
    }
};
```

U kunt de logica centraliseren die u gebruikt om activiteit te identificeren die u niet wilt volgen, zoals sommige douaneverbindingen of externe verbindingen in vertoningsadvertenties.
