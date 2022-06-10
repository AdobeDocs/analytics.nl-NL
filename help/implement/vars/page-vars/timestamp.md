---
title: timestamp
description: Stel handmatig de tijdstempel van de hit in.
feature: Variables
exl-id: 9d5ce5ef-2d84-4f65-b2e3-7aa3e219bc34
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# tijdstempel

De `timestamp` Met variabele wordt handmatig de tijdstempel van de hit ingesteld voor rapportsuites waarvoor tijdstempels zijn ingeschakeld.

>[!WARNING]
>
>Gebruik deze variabele niet als uw rapportsuite niet expliciet is geconfigureerd voor het accepteren van treffers met een tijdstempel. AppMeasurement stelt automatisch de tijd van een hit voor rapportsuites in die timestamped klappen niet steunen. Als u een hit met deze variabele naar een rapportsuite verzendt die geen tijdstempels ondersteunt, gaan die gegevens permanent verloren.

## Tijdstempel met Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.timestamp in AppMeasurement en de de coderedacteur van de de uitbreiding van de Analyse van de douanecode

De `s.timestamp` variabele is een tekenreeks die de datum en tijd van de hit bevat. Geldige tijdstempelindelingen zijn [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) en [Unix time](https://en.wikipedia.org/wiki/Unix_time).

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

Datum en tijd uitgedrukt in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) kan verschillende vormen aannemen. Adobe ondersteunt niet alle functies in ISO 8601.

* Zowel de datum als de tijd moeten worden opgegeven, gescheiden door `T`.
* uren en minuten zijn vereist; seconden zijn optioneel, maar aanbevolen.
* Weekdatums en rangteldatums worden niet ondersteund.
* De datum kan in het standaard of uitgebreide formaat zijn. Bijvoorbeeld: `2020-01-01T00:00:00Z` en `20200101T000000Z` zijn beide geldig.
* Fractionele minuten en seconden zijn technisch geldig, maar de breuken worden genegeerd door Adobe.
* Tijdzones worden ondersteund in de standaardnotatie en in de uitgebreide notatie.

Hieronder vindt u een geldig voorbeeld van ISO 8601-waarden in de `timestamp` variabele:

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
