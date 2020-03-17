---
title: linkURL
description: Overschrijf het automatisch gegenereerde gebruik van de koppeling-URL AppMeasurement in koppelingsvolgaanroepen.
translation-type: tm+mt
source-git-commit: 4a6cfa479559a644588613bd127c5b45ee8787e6

---


# linkURL

Wanneer een koppelingenvolgvraag naar Adobe wordt verzonden, detecteren servers voor gegevensverzameling automatisch de URL. Gebruik de `linkURL` variabele om de gedetecteerde URL te overschrijven.

## URL koppelen in Adobe Experience Platform Launch

Er is geen specifiek veld in Launch om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.linkURL in de redacteur van de douanecode van AppMeasurement en van de Lancering

De `s.linkURL` variabele is een tekenreeks die de URL bevat van de browser toen op de koppeling werd geklikt. Deze variabele vult geen dimensies in die beschikbaar zijn in de rapportage.

```js
s.linkURL = "https://example.com";
```

Als de `linkName` variabele niet voor een verbinding het volgen vraag wordt geplaatst, wordt de `linkURL` variabele in plaats daarvan gebruikt.
