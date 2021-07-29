---
title: timestamp
description: Stel handmatig de tijdstempel van de hit in.
exl-id: 9d5ce5ef-2d84-4f65-b2e3-7aa3e219bc34
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# tijdstempel

De `timestamp` variabele plaatst manueel de timestamp van de klap voor timestamp-toegelaten rapportreeksen.

>[!WARNING]
>
>Gebruik deze variabele niet als uw rapportsuite niet expliciet is geconfigureerd voor het accepteren van treffers met een tijdstempel. AppMeasurement stelt automatisch de tijd van een hit voor rapportsuites in die timestamped klappen niet steunen. Als u een hit met deze variabele naar een rapportsuite verzendt die geen tijdstempels ondersteunt, gaan die gegevens permanent verloren.

## Tijdstempel met tags in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.timestamp in AppMeasurement en de redacteur van de douanecode

De variabele `s.timestamp` is een tekenreeks met de datum en tijd van de hit. Geldige tijdstempelindelingen zijn [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) en [Unix time](https://en.wikipedia.org/wiki/Unix_time).

```js
// Timestamp using ISO 8601
s.timestamp = "2020-01-01T00:00:00Z";

// Timestamp using Unix timestamp
s.timestamp = "1577836800";

// Automatically get the current Unix timestamp
s.timestamp = Math.round(new Date().getTime()/1000);

// Automatically get the current ISO 8601 timestamp
s.timestamp = new Date().toISOString();
```

## ISO 8601-waarden

Datums en tijden, uitgedrukt in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601), kunnen verschillende vormen aannemen. Adobe ondersteunt niet alle functies in ISO 8601.

* Zowel de datum als de tijd moeten worden opgegeven, gescheiden door `T`.
* uren en minuten zijn vereist; seconden zijn optioneel, maar aanbevolen.
* Weekdatums en rangteldatums worden niet ondersteund.
* De datum kan in het standaard of uitgebreide formaat zijn. `2020-01-01T00:00:00Z` en `20200101T000000Z` zijn bijvoorbeeld beide geldig.
* Fractionele minuten en seconden zijn technisch geldig, maar de breuken worden genegeerd door Adobe.
* Tijdzones worden ondersteund in de standaardnotatie en in de uitgebreide notatie.

Hier volgt een geldig voorbeeld van ISO 8601-waarden in de variabele `timestamp`:

```text
2020-01-01T00:00:00+00:00
2020-01-01T00:00:00Z
2020-01-01T00:00:00
2020-01-01T00:00
20200101T000000+0000
20200101T000000Z
20200101T000000
20200101T0000
```
