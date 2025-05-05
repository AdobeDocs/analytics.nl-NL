---
title: doPlugins
description: Vorm logica vlak voordat een slag wordt gecompileerd en verzonden naar Adobe.
feature: Variables
exl-id: c5113be3-04b3-4dd2-8481-ba13149750ca
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# doPlugins

De `doPlugins` De variabele fungeert als een &#39;laatste aanroep&#39; om waarden in te stellen in uw implementatie. Het is de ideale plaats om vraag te maken aan [Methoden van plug-in](../plugins/impl-plugins.md) en stelt de gewenste variabelen in voordat een afbeeldingsaanvraag wordt verzonden. Indien [`usePlugins`](../config-vars/useplugins.md) wordt toegelaten, loopt het automatisch net alvorens om het even welk type beeldverzoek wordt gecompileerd en verzonden naar Adobe, die omvat:

* Alle paginaweergaven ([`t()`](t-method.md)) aanroepen
* Alle koppelingen bijhouden ([`tl()`](tl-method.md)) oproepen, met inbegrip van automatische downloadverbindingen en uitgangsverbindingen

Gebruik de `doPlugins` variabele om insteekcode aan te roepen en definitieve veranderlijke waarden in te stellen vlak alvorens een beeldverzoek wordt gecompileerd en naar Adobe verzonden.

## Gebruik voor Gebeurtenis verzendt callback code gebruikend de uitbreiding van SDK van het Web

In plaats van `doPlugins`, het gebruik van de Web SDK `onBeforeEventSend` met vergelijkbare functionaliteit.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** knop onder [!UICONTROL Adobe Experience Platform Web SDK].
1. Onder [!UICONTROL Data Collection]klikt u op de knop **[!UICONTROL Edit on before event send callback code]** knop.
1. Plaats de gewenste code in de editor.

## Gebruiken `onBeforeEventSend` manueel het uitvoeren van SDK van het Web

In plaats van `doPlugins`, het gebruik van de Web SDK `onBeforeEventSend` met vergelijkbare functionaliteit. Zie [Gebeurtenissen globaal wijzigen](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html?lang=nl-NL#modifying-events-globally) in de documentatie van SDK van het Web voor meer informatie.

```js
// Set the trackingCode XDM field to "New value"
alloy("configure", {
  "onBeforeEventSend": function(content) {
    content.xdm.marketing.trackingCode = "New value";
  }
})
```

## Plug-ins die de Adobe Analytics-extensie gebruiken

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de syntaxis van het AppMeasurement.

## s.doPlugins in AppMeasurement en aangepaste code

Stel de `s.doPlugins` aan een functie die gewenste code bevat. De functie wordt automatisch uitgevoerd wanneer u een volgende aanroep maakt.

```js
s.doPlugins = function() {/* Desired code */};
```

>[!IMPORTANT]
>
>Een functie instellen op de knop `doPlugins` variabele slechts eenmaal in uw implementatie. Als u de `doPlugins` meerdere keren variabele, alleen de meest recente code wordt gebruikt.

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
>Eerdere versies van AppMeasurement hadden iets andere versies `doPlugins()` code. Adobe raadt u aan bovenstaande notatie als beste praktijk te gebruiken.
