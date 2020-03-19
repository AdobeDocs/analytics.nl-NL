---
title: offlineHitLimit
description: Bepaal het maximumaantal controles aan rij voor off-line het volgen.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# offlineHitLimit

Offline bijhouden is een optionele manier om gegevens te verzamelen in Adobe Analytics. Als een bezoeker de verbinding met internet verbreekt maar door uw site blijft bladeren, worden treffers opgeslagen in een offline wachtrij totdat het apparaat opnieuw verbinding maakt met internet. Offlinetracering wordt meestal gebruikt voor mobiele toepassingen.

Met de `offlineHitLimit` variabele wordt een uiteinde geplaatst op het aantal hits in de lokale opslagruimte. Deze variabele werkt alleen als deze [`trackOffline`](trackoffline.md) is ingeschakeld.

## Limiet offlinehit in Adobe Experience Platform gestart

Er is geen specifiek veld in Launch om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.offlineHitLimit in de aangepaste code-editor van AppMeasurement en Launch

De `s.offlineHitLimit` variabele is een geheel getal dat het maximale aantal hits vertegenwoordigt dat een apparaat opslaat terwijl het offline is. Als deze variabele niet is gedefinieerd, is er geen limiet voor het aantal treffers dat een apparaat opslaat terwijl het offline is.

```js
s.offlineHitLimit = 100;
```
