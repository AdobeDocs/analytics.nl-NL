---
title: useLinkTrackSessionStorage
description: Gegevens voor het bijhouden van koppelingen opslaan in sessieopslag in plaats van een cookie.
exl-id: 3295195d-bfd6-4af9-9487-dc1ea6c3da23
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---

# useLinkTrackSessionStorage

Als uw organisatie het volgen van verbindingen gebruikt, gebruikt AppMeasurement het `s_sq` koekje om informatie tussen treffers over te gaan. Sommige websiteconfiguraties veroorzaken een conflict met dit cookie. Schakel deze variabele in als u de browsersessieopslag wilt gebruiken voor het bijhouden van koppelingen en het Activity Mappen van gegevens in plaats van een cookie.

Het gebruiken van browser zittingsopslag voor verbinding het volgen komt met verscheidene beperkingen voor:

* De opslag van de zitting werkt niet tussen protocollen. U hebt bijvoorbeeld één pagina die via HTTP wordt aangeboden en de volgende pagina die via HTTPS wordt verzonden. AppMeasurement heeft vanwege protocolverschillen geen toegang tot gegevens voor het bijhouden van koppelingen in de sessieopslag.
* Sessieopslag werkt niet in verschillende subdomeinen. Een bezoeker navigeert bijvoorbeeld naar `store.example.com` en navigeert vervolgens naar `toys.example.com`. AppMeasurement heeft vanwege verschillende subdomeinen geen toegang tot gegevens voor het bijhouden van koppelingen in de sessieopslag.

>[!TIP]
>
>De meest betrouwbare implementatie die sessieopslag gebruikt voor het bijhouden van koppelingen, biedt alle inhoud via HTTPS op één subdomein.

AppMeturement verwijdert de gegevens van de verbinding van de zittingsopslag na het verzenden van een klap naar Adobe. Deze verloopt ook automatisch wanneer het browsertabblad wordt gesloten.

## Opslag van koppelingsspoorsessies gebruiken met tags in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.useLinkTrackSessionStorage in AppMeasurement en aangepaste code-editor

De variabele `s.useLinkTrackSessionStorage` is een Booleaanse waarde die bepaalt of AppMeturement sessieopslag gebruikt voor gegevens voor het bijhouden van koppelingen in plaats van het cookie `s_sq`. De standaardwaarde is `false`. Stel deze variabele in op `true` als u wilt dat AppMeasurement sessieopslag gebruikt in plaats van het `s_sq`-cookie voor het bijhouden en Activity Mappen van koppelingen.

```js
s.useLinkTrackSessionStorage = true;
```
