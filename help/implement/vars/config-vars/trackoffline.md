---
title: trackOffline
description: Schakel offline bijhouden in of uit. Hiermee wordt gewijzigd hoe AppMeturement gegevens verzamelt.
translation-type: tm+mt
source-git-commit: 979a95ca749a3e21c4ddf48ba2d2a95672938a20

---


# trackOffline

Offline bijhouden is een optionele manier om gegevens te verzamelen in Adobe Analytics. Als een bezoeker de verbinding met internet verbreekt maar door uw site blijft bladeren, worden treffers opgeslagen in een offline wachtrij totdat het apparaat opnieuw verbinding maakt met internet. Offlinetracering wordt meestal gebruikt voor mobiele toepassingen.

De `trackOffline` variabele bepaalt of u het offline volgen in uw implementatie wilt gebruiken.

> [!IMPORTANT] U moet uw rapportreeks vormen om timestamped hits goed te keuren alvorens deze variabele toe te laten. Als een rapportsuite geen treffers met tijdstempels accepteert en deze variabele is ingeschakeld, gaan die gegevens verloren en kunnen deze niet worden hersteld.

Indien deze optie is ingeschakeld, gebruikt AppMeasurement het volgende proces om gegevens naar Adobe te verzenden:

* Wanneer u een verzoek voor een afbeelding compileert, wordt een parameter voor de queryreeks voor een tijdstempel opgenomen.
* Als het apparaat de servers van de de gegevensinzameling van Adobe niet kan bereiken, wordt de slag opgeslagen plaatselijk op het apparaat.
* Tijdens elke volgende druk probeert AppMeturement een beeldverzoek naar Adobe te verzenden.
   * Als Adobe-gegevensverzamelingsservers niet worden bereikt, wordt de hit toegevoegd aan de wachtrij op het apparaat.
   * Als het Adobe-gegevensverzamelingsservers kan bereiken, worden de hit en de wachtrij met hits verzonden terwijl het apparaat offline was.

## Offline volgen in Adobe Experience Platform Launch

Er is geen specifiek veld in Launch om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.trackOffline in AppMeasurement en Launch, aangepaste code-editor

De `s.trackOffline` variabele is een Booleaanse waarde die het offline bijhouden in- of uitschakelt. De standaardwaarde is `false`. Stel deze waarde in op `true` als u offline bijhouden wilt inschakelen.

```js
s.trackOffline = true;
```
