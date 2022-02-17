---
title: useLinkTrackSessionStorage
description: Gegevens voor het bijhouden van koppelingen opslaan in sessieopslag in plaats van een cookie.
feature: Variables
exl-id: 3295195d-bfd6-4af9-9487-dc1ea6c3da23
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---

# useLinkTrackSessionStorage

Als uw organisatie koppelingen bijhouden gebruikt, gebruikt AppMeasurement de `s_sq` cookie om informatie tussen treffers door te geven. Sommige websiteconfiguraties veroorzaken een conflict met dit cookie. Schakel deze variabele in als u de browsersessieopslag wilt gebruiken voor het bijhouden van koppelingen en het Activity Mappen van gegevens in plaats van een cookie.

Het gebruiken van browser zittingsopslag voor verbinding het volgen komt met verscheidene beperkingen voor:

* De opslag van de zitting werkt niet tussen protocollen. U hebt bijvoorbeeld één pagina die via HTTP wordt aangeboden en de volgende pagina die via HTTPS wordt verzonden. AppMeasurement heeft vanwege protocolverschillen geen toegang tot gegevens voor het bijhouden van koppelingen in de sessieopslag.
* Sessieopslag werkt niet in verschillende subdomeinen. Een bezoeker navigeert bijvoorbeeld naar `store.example.com`, navigeert vervolgens naar `toys.example.com`. AppMeasurement heeft vanwege verschillende subdomeinen geen toegang tot gegevens voor het bijhouden van koppelingen in de sessieopslag.

>[!TIP]
>
>De meest betrouwbare implementatie die sessieopslag gebruikt voor het bijhouden van koppelingen, biedt alle inhoud via HTTPS op één subdomein.

AppMeturement verwijdert de gegevens van de verbinding van de zittingsopslag na het verzenden van een klap naar Adobe. Deze verloopt ook automatisch wanneer het browsertabblad wordt gesloten.

## Opslag van koppelingsspoorsessies gebruiken met tags in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.useLinkTrackSessionStorage in AppMeasurement en aangepaste code-editor

De `s.useLinkTrackSessionStorage` De variabele is een Booleaanse waarde die bepaalt of AppMeetings sessieopslag gebruikt voor gegevens voor het bijhouden van koppelingen in plaats van de `s_sq` cookie. De standaardwaarde is `false`. Deze variabele instellen op `true` als u wilt dat AppMeasurement sessieopslag gebruikt in plaats van de `s_sq` cookie voor het bijhouden van koppelingen en Activity Map.

```js
s.useLinkTrackSessionStorage = true;
```
