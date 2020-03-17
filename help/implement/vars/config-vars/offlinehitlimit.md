---
title: offlineHitLimit
description: Bepaal het maximumaantal controles aan rij voor off-line het volgen.
translation-type: tm+mt
source-git-commit: 4a6cfa479559a644588613bd127c5b45ee8787e6

---


# offlineHitLimit

Offline bijhouden is een optionele manier om gegevens te verzamelen in Adobe Analytics. Als een bezoeker de verbinding met internet verbreekt maar door uw site blijft bladeren, worden treffers opgeslagen in een offline wachtrij totdat het apparaat opnieuw verbinding maakt met internet. Offlinetracering wordt meestal gebruikt voor mobiele toepassingen.

Met de `offlineHitLimit` variabele wordt een uiteinde geplaatst op het aantal hits in de lokale opslagruimte. Deze variabele werkt alleen als `trackOffline` dit `true`het geval is.

## Limiet offlinehit in Adobe Experience Platform gestart

Er is geen specifiek veld in Launch om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.offlineHitLimit in de aangepaste code-editor van AppMeasurement en Launch

De `s.offlineHitLimit` variabele is een geheel getal dat het maximale aantal hits vertegenwoordigt dat een apparaat opslaat terwijl het offline is. Als deze variabele niet is gedefinieerd, is er geen limiet voor het aantal treffers dat een apparaat opslaat terwijl het offline is.

```js
s.offlineHitLimit = 100;
```
