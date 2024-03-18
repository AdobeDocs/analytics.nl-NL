---
title: linkURL
description: Hef het automatisch gegenereerde gebruik van het URL-AppMeasurement voor koppelingen op in de aanroepen voor het bijhouden van koppelingen.
feature: Variables
exl-id: 15d6e423-d9fc-4f84-ad39-0bd91399cde4
role: Admin, Developer
source-git-commit: 12347957a7a51dc1f8dfb46d489b59a450c2745a
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---

# linkURL

Wanneer een verbinding het volgen vraag naar Adobe wordt verzonden, ontdekken de servers van de gegevensinzameling automatisch URL. Gebruik de `linkURL` variabele om de gedetecteerde URL te overschrijven.

## URL koppelen met de SDK van het Web

De koppeling-URL wordt toegewezen aan de volgende variabelen:

* [XDM-object](/help/implement/aep-edge/xdm-var-mapping.md): `web.webInteraction.URL`
* [Data, object](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.linkURL` of `data.__adobe.analytics.pev1`

## URL koppelen met de Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de syntaxis van het AppMeasurement.

## s.linkURL in AppMeasurement en de de coderedacteur van de uitbreiding van de Analyse

De `s.linkURL` variabele is een tekenreeks die de URL bevat van de browser toen op de koppeling werd geklikt. Deze variabele vult geen dimensies in die beschikbaar zijn in de rapportage.

```js
s.linkURL = "https://example.com";
```

Indien het derde argument van de [tl()](../functions/tl-method.md) methode is niet ingesteld, de `linkURL` in plaats daarvan wordt een variabele gebruikt.
