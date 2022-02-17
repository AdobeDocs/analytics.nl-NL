---
title: trackOffline
description: Schakel offline bijhouden in of uit. Hiermee wordt gewijzigd hoe AppMeturement gegevens verzamelt.
feature: Variables
exl-id: 23a17ddc-01e6-42b6-81b0-c60f15a07231
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# trackOffline

Offline bijhouden is een optionele manier om gegevens te verzamelen in Adobe Analytics. Als een bezoeker de verbinding met internet verbreekt maar door uw site blijft bladeren, worden treffers opgeslagen in een offline wachtrij totdat het apparaat opnieuw verbinding maakt met internet. Offlinetracering wordt meestal gebruikt voor mobiele toepassingen.

De `trackOffline` de variabele bepaalt als u off-line het volgen in uw implementatie wilt gebruiken.

>[!IMPORTANT]
>
>U moet uw rapportreeks vormen om timestamped hits goed te keuren alvorens deze variabele toe te laten. Als een rapportsuite geen treffers met tijdstempels accepteert en deze variabele is ingeschakeld, gaan die gegevens verloren en kunnen deze niet worden hersteld.

Indien deze optie is ingeschakeld, gebruikt AppMeasurement het volgende proces om gegevens naar Adobe te verzenden:

* Wanneer u een verzoek voor een afbeelding compileert, wordt een parameter voor de queryreeks voor een tijdstempel opgenomen.
* Als het apparaat geen Adobe gegevensverzamelingsservers kan bereiken, wordt de hit lokaal op het apparaat opgeslagen.
* Tijdens elke volgende hit probeert AppMeasurement een afbeeldingsverzoek naar Adobe te verzenden.
   * Als het geen servers van de Adobe- gegevensinzameling kan bereiken, wordt de klap toegevoegd aan de rij op het apparaat.
   * Als het de servers van de gegevensinzameling van de Adobe kan bereiken, worden de slag en de rij van klappen terwijl het apparaat off-line was verzonden.

## Offline volgen met tags in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.trackOffline in AppMeasurement en aangepaste code-editor

De `s.trackOffline` variabele is een Booleaanse waarde die offline bijhouden in- of uitschakelt. De standaardwaarde is `false`. Deze waarde instellen op `true` als u offline bijhouden wilt inschakelen.

```js
s.trackOffline = true;
```
