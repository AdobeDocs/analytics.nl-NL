---
title: offlineHitLimit
description: Bepaal het maximumaantal controles aan rij voor off-line het volgen.
feature: Variables
exl-id: de6478b3-b95f-4edc-8427-7b915a46b3ba
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 1%

---

# offlineHitLimit

Offline bijhouden is een optionele manier om gegevens te verzamelen in Adobe Analytics. Als een bezoeker de verbinding met internet verbreekt maar door uw site blijft bladeren, worden treffers opgeslagen in een offline wachtrij totdat het apparaat opnieuw verbinding maakt met internet. Offlinetracering wordt meestal gebruikt voor mobiele toepassingen.

De `offlineHitLimit` Met variabele wordt een uiteinde geplaatst op het aantal hits dat lokaal op het apparaat wordt opgeslagen. Deze variabele werkt alleen als [`trackOffline`](trackoffline.md) is ingeschakeld.

## Off line limiet voor Actief met Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.offlineHitLimit in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De `s.offlineHitLimit` variabele is een geheel getal dat het maximale aantal hits vertegenwoordigt dat een apparaat opslaat terwijl het offline is. Als deze variabele niet is gedefinieerd, is er geen limiet voor het aantal treffers dat een apparaat opslaat terwijl het offline is.

```js
s.offlineHitLimit = 100;
```
