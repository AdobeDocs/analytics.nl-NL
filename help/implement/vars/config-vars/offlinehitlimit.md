---
title: offlineHitLimit
description: Bepaal het maximumaantal controles aan rij voor off-line het volgen.
feature: Variables
exl-id: de6478b3-b95f-4edc-8427-7b915a46b3ba
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 1%

---

# offlineHitLimit

Offline bijhouden is een optionele manier om gegevens te verzamelen in Adobe Analytics. Als een bezoeker de verbinding met internet verbreekt maar door uw site blijft bladeren, worden treffers opgeslagen in een offline wachtrij totdat het apparaat opnieuw verbinding maakt met internet. Offlinetracering wordt meestal gebruikt voor mobiele toepassingen.

De `offlineHitLimit` Met variabele wordt een uiteinde geplaatst op het aantal hits dat lokaal op het apparaat wordt opgeslagen. Deze variabele werkt alleen als [`trackOffline`](trackoffline.md) is ingeschakeld.

## Off line limiet voor Actief met tags in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.offlineHitLimit in AppMeasurement en aangepaste code-editor

De `s.offlineHitLimit` variabele is een geheel getal dat het maximale aantal hits vertegenwoordigt dat een apparaat opslaat terwijl het offline is. Als deze variabele niet is gedefinieerd, is er geen limiet voor het aantal treffers dat een apparaat opslaat terwijl het offline is.

```js
s.offlineHitLimit = 100;
```
