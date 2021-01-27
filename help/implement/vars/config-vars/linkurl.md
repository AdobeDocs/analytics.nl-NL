---
title: linkURL
description: Overschrijf het automatisch gegenereerde gebruik van de koppeling-URL AppMeasurement in koppelingsvolgaanroepen.
translation-type: tm+mt
source-git-commit: 423e9b753a3b7b1e0a8e8b9748f9694d718abd18
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 1%

---


# linkURL

Wanneer een verbinding het volgen vraag naar Adobe wordt verzonden, ontdekken de servers van de gegevensinzameling automatisch URL. Gebruik de variabele `linkURL` om de gedetecteerde URL te overschrijven.

## URL koppelen in Adobe Experience Platform Launch

Er is geen specifiek veld in Launch om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.linkURL in de redacteur van de douanecode van AppMeasurement en van de Lancering

De variabele `s.linkURL` is een tekenreeks die de URL bevat van de browser toen op de koppeling werd geklikt. Deze variabele vult geen dimensies in die beschikbaar zijn in de rapportage.

```js
s.linkURL = "https://example.com";
```

Als het derde argument van de methode [tl()](../functions/tl-method.md) niet is ingesteld, wordt in plaats daarvan de variabele `linkURL` gebruikt.
