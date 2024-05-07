---
title: offlineHitLimit
description: Bepaal het maximumaantal controles aan rij voor off-line het volgen.
feature: Variables
exl-id: de6478b3-b95f-4edc-8427-7b915a46b3ba
role: Admin, Developer
source-git-commit: 8bc5e649c5b5852232f4baddcddad0766bc1569a
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# offlineHitLimit

Offline bijhouden is een optionele manier om gegevens te verzamelen in Adobe Analytics. Als een bezoeker de verbinding met internet verbreekt maar door uw site blijft bladeren, worden treffers opgeslagen in een offline wachtrij totdat het apparaat opnieuw verbinding maakt met internet. Offlinetracering wordt meestal gebruikt voor mobiele toepassingen.

De `offlineHitLimit` Met variabele wordt een uiteinde geplaatst op het aantal hits dat lokaal op het apparaat wordt opgeslagen. Deze variabele werkt alleen als [`trackOffline`](trackoffline.md) is ingeschakeld.

## Offline aanraaklimiet met de Web SDK

De SDK van het Web ondersteunt offline bijhouden niet.

## Offline aanraaklimiet met Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de syntaxis van het AppMeasurement.

## s.offlineHitLimit in AppMeasurement en de de redacteur van de de uitbreidingsdouanecode van de Analyse

De `s.offlineHitLimit` een variabele is een geheel getal dat staat voor het maximum aantal hits dat een apparaat opslaat terwijl het offline is. Als deze variabele niet is gedefinieerd, wordt standaard ingesteld op `10`. U kunt het aan om het even welke geheelwaarde plaatsen. Houd bij het instellen van hoge waarden rekening met lokale opslagruimten in de browser van een bezoeker. Deze limiet is doorgaans 5-10 MB.

```js
s.offlineHitLimit = 100;
```
