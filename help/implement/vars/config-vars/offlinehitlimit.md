---
title: offlineHitLimit
description: Bepaal het maximumaantal controles aan rij voor off-line het volgen.
feature: Appmeasurement Implementation
exl-id: de6478b3-b95f-4edc-8427-7b915a46b3ba
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# offlineHitLimit

Offline bijhouden is een optionele manier om gegevens te verzamelen in Adobe Analytics. Als een bezoeker de verbinding met internet verbreekt maar door uw site blijft bladeren, worden treffers opgeslagen in een offline wachtrij totdat het apparaat opnieuw verbinding maakt met internet. Offlinetracering wordt meestal gebruikt voor mobiele toepassingen.

Met de variabele `offlineHitLimit` wordt een uiteinde geplaatst op het aantal treffers dat lokaal in de winkel van het apparaat wordt opgeslagen. Deze variabele werkt alleen als [`trackOffline`](trackoffline.md) is ingeschakeld.

## Offline limiet voor treffers met gebruik van de Web SDK

De Web SDK ondersteunt offline bijhouden niet.

## Offline aanraaklimiet met Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de AppMeasurement-syntaxis.

## s.offlineHitLimit in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De variabele `s.offlineHitLimit` is een geheel getal dat staat voor het maximale aantal hits dat een apparaat opslaat terwijl het offline is. Als deze variabele niet is gedefinieerd, wordt standaard ingesteld op `10` . U kunt het aan om het even welke geheelwaarde plaatsen. Houd bij het instellen van hoge waarden rekening met lokale opslagruimten in de browser van een bezoeker. Deze limiet is doorgaans 5-10 MB.

```js
s.offlineHitLimit = 100;
```
