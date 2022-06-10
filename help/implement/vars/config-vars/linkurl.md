---
title: linkURL
description: Overschrijf het automatisch gegenereerde gebruik van de koppeling-URL AppMeasurement in koppelingsvolgaanroepen.
feature: Variables
exl-id: 15d6e423-d9fc-4f84-ad39-0bd91399cde4
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 1%

---

# linkURL

Wanneer een verbinding het volgen vraag naar Adobe wordt verzonden, ontdekken de servers van de gegevensinzameling automatisch URL. Gebruik de `linkURL` variabele om de gedetecteerde URL te overschrijven.

## URL koppelen met de SDK van het Web

URL koppeling is [toegewezen voor Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) onder het XDM-veld `web.webInteraction.URL`.

## URL koppelen met de Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.linkURL in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De `s.linkURL` variabele is een tekenreeks die de URL bevat van de browser toen op de koppeling werd geklikt. Deze variabele vult geen dimensies in die beschikbaar zijn in de rapportage.

```js
s.linkURL = "https://example.com";
```

Indien het derde argument van de [tl()](../functions/tl-method.md) methode is niet ingesteld, de `linkURL` in plaats daarvan wordt een variabele gebruikt.
