---
title: linkURL
description: Overschrijf het automatisch gegenereerde gebruik van de koppeling-URL AppMeasurement in koppelingsvolgaanroepen.
feature: Variables
exl-id: 15d6e423-d9fc-4f84-ad39-0bd91399cde4
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 1%

---

# linkURL

Wanneer een verbinding het volgen vraag naar Adobe wordt verzonden, ontdekken de servers van de gegevensinzameling automatisch URL. Gebruik de `linkURL` variabele om de gedetecteerde URL te overschrijven.

## URL koppelen met tags in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.linkURL in AppMeasurement en aangepaste code-editor

De `s.linkURL` variabele is een tekenreeks die de URL bevat van de browser toen op de koppeling werd geklikt. Deze variabele vult geen dimensies in die beschikbaar zijn in de rapportage.

```js
s.linkURL = "https://example.com";
```

Indien het derde argument van de [tl()](../functions/tl-method.md) methode is niet ingesteld, de `linkURL` in plaats daarvan wordt een variabele gebruikt.
