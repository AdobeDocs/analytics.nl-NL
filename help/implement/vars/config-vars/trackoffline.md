---
title: trackOffline
description: Schakel offline bijhouden in of uit. Hiermee wordt gewijzigd hoe AppMeasurement gegevens verzamelt.
feature: Appmeasurement Implementation
exl-id: 23a17ddc-01e6-42b6-81b0-c60f15a07231
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# trackOffline

Offline bijhouden is een optionele manier om gegevens te verzamelen in Adobe Analytics. Als een bezoeker de verbinding met internet verbreekt maar door uw site blijft bladeren, worden treffers opgeslagen in een offline wachtrij totdat het apparaat opnieuw verbinding maakt met internet. Offlinetracering wordt meestal gebruikt voor mobiele toepassingen.

De variabele `trackOffline` bepaalt of u offline tracering wilt gebruiken in uw implementatie.

>[!WARNING]
>
>U moet uw rapportreeks vormen om timestamped hits goed te keuren alvorens deze variabele toe te laten. Als een rapportsuite geen treffers met tijdstempels accepteert en deze variabele is ingeschakeld, gaan die gegevens verloren en kunnen deze niet worden hersteld.

Als deze optie is ingeschakeld, gebruikt AppMeasurement het volgende proces om gegevens naar Adobe te verzenden:

* Wanneer u een verzoek voor een afbeelding compileert, wordt een parameter voor de queryreeks voor een tijdstempel opgenomen.
* Als het apparaat geen Adobe-gegevensverzamelingsservers kan bereiken, wordt de hit lokaal op het apparaat opgeslagen.
* Tijdens elke volgende hit probeert AppMeasurement een verzoek om een afbeelding naar Adobe te verzenden.
   * Als Adobe-gegevensverzamelingsservers niet kunnen worden bereikt, wordt de hit toegevoegd aan de wachtrij op het apparaat.
   * Als het Adobe-gegevensverzamelingsservers kan bereiken, worden de hit en de wachtrij met treffers verzonden terwijl het apparaat offline was.

## Offline tracering met gebruik van de Web SDK

De Web SDK ondersteunt offline bijhouden niet.

## Offline bijhouden met de Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de AppMeasurement-syntaxis.

## s.trackOffline in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De `s.trackOffline` -variabele is een Booleaanse waarde die het offline bijhouden in- of uitschakelt. De standaardwaarde is `false` . Stel deze waarde in op `true` als u offline bijhouden wilt inschakelen.

```js
s.trackOffline = true;
```
