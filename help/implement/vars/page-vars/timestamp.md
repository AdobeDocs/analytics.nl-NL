---
title: tijdstempel
description: Stel handmatig de tijdstempel van de hit in.
feature: Appmeasurement Implementation
exl-id: 9d5ce5ef-2d84-4f65-b2e3-7aa3e219bc34
role: Admin, Developer
source-git-commit: fcc165536d77284e002cb2ba6b7856be1fdb3e14
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---

# tijdstempel

Met de variabele `timestamp` wordt handmatig de tijdstempel van de hit ingesteld voor rapportsuites waarvoor tijdstempels zijn ingeschakeld.

>[!WARNING]
>
>Gebruik deze variabele niet als uw rapportsuite niet expliciet is geconfigureerd voor het accepteren van treffers met een tijdstempel. AppMeasurement stelt automatisch de tijd van een hit in voor rapportsuites die geen ondersteuning bieden voor treffers met tijdstempels. Als u een hit met deze variabele naar een rapportsuite verzendt die geen tijdstempels ondersteunt, gaan die gegevens permanent verloren.

## Tijdstempel met gebruik van de Web SDK

Tijdstempel wordt [&#x200B; in kaart gebracht voor Adobe Analytics &#x200B;](/help/implement/aep-edge/xdm-var-mapping.md) onder het XDM gebied `xdm.timestamp`. Dit veld ondersteunt alleen Unix-tijd.

## Tijdstempel met Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de AppMeasurement-syntaxis.

## s.timestamp in AppMeasurement en de de coderedacteur van de uitbreiding van de Analytics

De variabele `s.timestamp` is een tekenreeks met de datum en tijd van de hit. Geldige timestamp formaten omvatten [&#x200B; ISO 8601 &#x200B;](https://en.wikipedia.org/wiki/ISO_8601) en [&#x200B; Unix tijd &#x200B;](https://en.wikipedia.org/wiki/Unix_time) in seconden.

```js
// Timestamp using ISO 8601
s.timestamp = "2024-01-01T00:00:00Z";

// Timestamp using Unix timestamp
s.timestamp = "1577836800";

// Automatically get the current Unix timestamp
s.timestamp = Math.round(new Date().getTime()/1000);

// Automatically get the current ISO 8601 timestamp
s.timestamp = new Date().toISOString();
```

## ISO 8601-waarden

De data en de tijden die in [&#x200B; worden uitgedrukt ISO 8601 &#x200B;](https://en.wikipedia.org/wiki/ISO_8601) kunnen verscheidene verschillende vormen nemen. Adobe ondersteunt niet alle functies in ISO 8601.

* Zowel de datum als de tijd moeten worden opgegeven, gescheiden door `T` .
* Uren en minuten zijn vereist; seconden zijn optioneel, maar aanbevolen.
* Weekdatums en rangteldatums worden niet ondersteund.
* De datum kan in het standaard of uitgebreide formaat zijn. `2024-01-01T00:00:00Z` en `20240101T000000Z` zijn bijvoorbeeld allebei geldig.
* Fractionele minuten en seconden zijn technisch geldig, maar de breuken worden genegeerd door Adobe.
* Tijdzones worden ondersteund in de standaardnotatie en in de uitgebreide notatie.

Hieronder vindt u een geldig voorbeeld van ISO 8601-waarden in de variabele `timestamp` :

```text
2024-01-01T00:00:00+00:00
2024-01-01T00:00:00Z
2024-01-01T00:00:00
2024-01-01T00:00
20240101T000000+0000
20240101T000000Z
20240101T000000
20240101T0000
```
