---
title: doPlugins
description: Vorm logica vlak voordat een slag wordt gecompileerd en verzonden naar Adobe.
feature: Appmeasurement Implementation
exl-id: c5113be3-04b3-4dd2-8481-ba13149750ca
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# doPlugins

De variabele `doPlugins` fungeert als een &#39;laatste aanroep&#39; om waarden in te stellen in uw implementatie. Het is de ideale plaats om vraag aan [ stop-in methodes ](../plugins/impl-plugins.md) te maken en om het even welke gewenste variabelen te plaatsen alvorens een beeldverzoek wordt verzonden. Als [`usePlugins`](../config-vars/useplugins.md) is ingeschakeld, wordt deze automatisch uitgevoerd vlak voordat een type afbeeldingsaanvraag wordt gecompileerd en naar Adobe wordt verzonden, zoals:

* Alle aanroepen van de paginaweergave ([`t()`](t-method.md))
* Alle verbindingen het volgen ([`tl()`](tl-method.md)) vraag, met inbegrip van automatische downloadverbindingen en uitgangsverbindingen

Gebruik de variabele `doPlugins` om insteekcode aan te roepen en de uiteindelijke waarden van de variabelen in te stellen vlak voordat een afbeeldingsaanvraag wordt gecompileerd en naar Adobe wordt verzonden.

## Use On Before Event Send callback code using the Web SDK extension

In plaats van `doPlugins` gebruikt de Web SDK `onBeforeEventSend` met vergelijkbare functionaliteit.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder [!UICONTROL Adobe Experience Platform Web SDK] .
1. Klik onder [!UICONTROL Data Collection] op de knop **[!UICONTROL Edit on before event send callback code]** .
1. Plaats de gewenste code in de editor.

## Gebruik `onBeforeEventSend` handmatig om de Web SDK te implementeren

In plaats van `doPlugins` gebruikt de Web SDK `onBeforeEventSend` met vergelijkbare functionaliteit. Zie [ Veranderend gebeurtenissen globaal ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#modifying-events-globally) in de documentatie van SDK van het Web voor meer informatie.

```js
// Set the trackingCode XDM field to "New value"
alloy("configure", {
  "onBeforeEventSend": function(content) {
    content.xdm.marketing.trackingCode = "New value";
  }
})
```

## Plug-ins die de Adobe Analytics-extensie gebruiken

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de AppMeasurement-syntaxis.

## s.doPlugins in AppMeasurement en aangepaste code

Stel de variabele `s.doPlugins` in op een functie die de gewenste code bevat. De functie wordt automatisch uitgevoerd wanneer u een volgende aanroep maakt.

```js
s.doPlugins = function() {/* Desired code */};
```

>[!IMPORTANT]
>
>Stel een functie slechts eenmaal in de implementatie in op de variabele `doPlugins` . Wanneer u de variabele `doPlugins` meerdere keren instelt, wordt alleen de meest recente code gebruikt.

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
>Eerdere versies van AppMeasurement hadden iets andere `doPlugins()` code. Adobe raadt u aan bovenstaande notatie te gebruiken als aanbevolen werkwijze.
