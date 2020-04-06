---
title: useLinkTrackSessionStorage
description: Gegevens voor het bijhouden van koppelingen opslaan in sessieopslag in plaats van een cookie.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# useLinkTrackSessionStorage

Als uw organisatie koppelingen bijhouden gebruikt, gebruikt AppMeasurement het `s_sq` cookie om informatie tussen hits door te geven. Sommige websiteconfiguraties veroorzaken een conflict met dit cookie. Als u de opslag van de browser zittingsopslag voor verbinding het volgen en gegevens van de Kaart van de Activiteit in plaats van een koekje wilt gebruiken, laat deze variabele toe.

Het gebruiken van browser zittingsopslag voor verbinding het volgen komt met verscheidene beperkingen voor:

* De opslag van de zitting werkt niet tussen protocollen. U hebt bijvoorbeeld één pagina die via HTTP wordt aangeboden en de volgende pagina die via HTTPS wordt verzonden. AppMeasurement heeft vanwege protocolverschillen geen toegang tot gegevens voor het bijhouden van koppelingen in de sessieopslag.
* Sessieopslag werkt niet in verschillende subdomeinen. Een bezoeker navigeert bijvoorbeeld naar `store.example.com`en navigeert vervolgens naar `toys.example.com`. AppMeasurement heeft vanwege verschillende subdomeinen geen toegang tot gegevens voor het bijhouden van koppelingen in de sessieopslag.

>[!TIP] De meest betrouwbare implementatie die sessieopslag gebruikt voor het bijhouden van koppelingen, biedt alle inhoud via HTTPS op één subdomein.

AppMeturement verwijdert de gegevens van de verbinding van de zittingsopslag na het verzenden van een klap naar Adobe. Deze verloopt ook automatisch wanneer het browsertabblad wordt gesloten.

## Opslag van een koppelingentrack gebruiken in Adobe Experience Platform Starten

Er is geen specifiek veld in Launch om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.useLinkTrackSessionStorage in AppMeasurement en Launch, aangepaste code-editor

De `s.useLinkTrackSessionStorage` variabele is een Booleaanse waarde die bepaalt of AppMeturement sessieopslag gebruikt voor gegevens voor het bijhouden van koppelingen in plaats van het `s_sq` cookie. De standaardwaarde is `false`. Stel deze variabele in op `true` als u wilt dat AppMeasurement sessieopslag gebruikt in plaats van het `s_sq` cookie voor het bijhouden van koppelingen en Activiteitenkaart.

```js
s.useLinkTrackSessionStorage = true;
```
