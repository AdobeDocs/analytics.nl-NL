---
title: linkURL
description: Overschrijf de automatisch gegenereerde link-URL die AppMeasurement gebruikt in koppelingsvolgaanroepen.
feature: Appmeasurement Implementation
exl-id: 15d6e423-d9fc-4f84-ad39-0bd91399cde4
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# linkURL

Wanneer een verbinding het volgen vraag naar Adobe wordt verzonden, ontdekken de servers van de gegevensinzameling automatisch URL. Gebruik de variabele `linkURL` om de gedetecteerde URL te overschrijven.

Er zijn geen dimensies in Analysis Workspace die rapporteren over deze variabele. Het bevolkt de `page_event_var1` kolom in [ het voer van Gegevens ](/help/export/analytics-data-feed/data-feed-overview.md).

## URL koppelen met de Web SDK

De koppeling-URL wordt toegewezen aan de volgende variabelen:

* [ voorwerp XDM ](/help/implement/aep-edge/xdm-var-mapping.md): `web.webInteraction.URL`
* [ voorwerp van Gegevens ](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.linkURL` of `data.__adobe.analytics.pev1`

## URL koppelen met de Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de AppMeasurement-syntaxis.

## s.linkURL in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De variabele `s.linkURL` is een tekenreeks die de URL van de browser bevat toen op de koppeling werd geklikt. Deze variabele vult geen dimensies in die beschikbaar zijn in de rapportage.

```js
s.linkURL = "https://example.com";
```

Als het derde argument van [ tl () ](../functions/tl-method.md) methode niet wordt geplaatst, wordt de `linkURL` variabele gebruikt in plaats daarvan.
