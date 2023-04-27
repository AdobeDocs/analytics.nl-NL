---
title: doPlugins
description: Vorm logica vlak voordat een slag wordt gecompileerd en verzonden naar Adobe.
feature: Variables
exl-id: c5113be3-04b3-4dd2-8481-ba13149750ca
source-git-commit: 41154580c272514e504c5478215bb67795488de3
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# doPlugins

De `doPlugins` De variabele fungeert als een &#39;laatste aanroep&#39; om waarden in te stellen in uw implementatie. Het is de ideale plaats om vraag te maken aan [Methoden van plug-in](../plugins/impl-plugins.md) en stelt de gewenste variabelen in voordat een afbeeldingsaanvraag wordt verzonden. Indien [`usePlugins`](../config-vars/useplugins.md) wordt toegelaten, loopt het automatisch net alvorens om het even welk type beeldverzoek wordt gecompileerd en verzonden naar Adobe, die omvat:

* Alle paginaweergaven ([`t()`](t-method.md)) oproepen
* Alle koppelingen bijhouden ([`tl()`](tl-method.md)) oproepen, met inbegrip van automatische downloadverbindingen en uitgangsverbindingen

Gebruik de `doPlugins` variabele om insteekcode aan te roepen en definitieve veranderlijke waarden in te stellen vlak alvorens een beeldverzoek wordt gecompileerd en verzonden naar Adobe.

## Gebruik voor Gebeurtenis verzendt callback code gebruikend de uitbreiding van SDK van het Web

In plaats van `doPlugins`, gebruikt de Web SDK `onBeforeEventSend` met vergelijkbare functionaliteit.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** knop onder [!UICONTROL Adobe Experience Platform Web SDK].
1. Onder [!UICONTROL Data Collection]klikt u op de knop **[!UICONTROL Edit on before event send callback code]** knop.
1. Plaats de gewenste code in de editor.

## Gebruiken `onBeforeEventSend` manueel het uitvoeren van SDK van het Web

In plaats van `doPlugins`, gebruikt de Web SDK `onBeforeEventSend` met vergelijkbare functionaliteit. Zie [Gebeurtenissen globaal wijzigen](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#modifying-events-globally) in de documentatie van SDK van het Web voor meer informatie.

```js
// Set the trackingCode XDM field to "New value"
alloy("configure", {
  "onBeforeEventSend": function(content) {
    content.xdm.marketing.trackingCode = "New value";
  }
})
```

## Plug-ins die de Adobe Analytics-extensie gebruiken

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.doPlugins in AppMeasurement en aangepaste code

Stel de `s.doPlugins` aan een functie die gewenste code bevat. De functie wordt automatisch uitgevoerd wanneer u een volgende aanroep maakt.

```js
s.doPlugins = function() {/* Desired code */};
```

>[!IMPORTANT]
>
>Een functie instellen op de `doPlugins` variabele slechts eenmaal in uw implementatie. Als u de `doPlugins` meerdere keren variabele, alleen de meest recente code wordt gebruikt.

## Voorbeelden

```js
// Set eVar1 to the web page's title
s.doPlugins = function() {
  s.eVar1 = window.document.title;
};

// Use the getPreviousValue plug-in (requires plug-in code outside the function)
s.doPlugins = function() {
  s.eVar1 = s.getPreviousValue(s.pageName,'gpv_pn');
}
```

>[!NOTE]
>
>Eerdere versies van AppMeasurement hadden iets verschillende versies `doPlugins()` code. Adobe raadt u aan de bovenstaande notatie te gebruiken als aanbevolen werkwijze.
