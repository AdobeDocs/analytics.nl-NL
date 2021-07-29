---
title: linkURL
description: Overschrijf het automatisch gegenereerde gebruik van de koppeling-URL AppMeasurement in koppelingsvolgaanroepen.
exl-id: 15d6e423-d9fc-4f84-ad39-0bd91399cde4
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 1%

---

# linkURL

Wanneer een verbinding het volgen vraag naar Adobe wordt verzonden, ontdekken de servers van de gegevensinzameling automatisch URL. Gebruik de variabele `linkURL` om de gedetecteerde URL te overschrijven.

## URL koppelen met tags in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.linkURL in AppMeasurement en aangepaste code-editor

De variabele `s.linkURL` is een tekenreeks die de URL bevat van de browser toen op de koppeling werd geklikt. Deze variabele vult geen dimensies in die beschikbaar zijn in de rapportage.

```js
s.linkURL = "https://example.com";
```

Als het derde argument van de methode [tl()](../functions/tl-method.md) niet is ingesteld, wordt in plaats daarvan de variabele `linkURL` gebruikt.
