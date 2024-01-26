---
title: useLinkTrackSessionStorage
description: Gegevens voor het bijhouden van koppelingen opslaan in sessieopslag in plaats van een cookie.
feature: Variables
exl-id: 3295195d-bfd6-4af9-9487-dc1ea6c3da23
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# useLinkTrackSessionStorage

Als uw organisatie koppelingen bijhouden gebruikt, gebruikt het AppMeasurement de optie `s_sq` cookie om informatie tussen treffers door te geven. Sommige websiteconfiguraties veroorzaken een conflict met dit cookie. Schakel deze variabele in als u de browsersessieopslag wilt gebruiken voor het bijhouden van koppelingen en het Activity Mappen van gegevens in plaats van een cookie.

Het gebruiken van browser zittingsopslag voor verbinding het volgen komt met verscheidene beperkingen voor:

* De opslag van de zitting werkt niet tussen protocollen. U hebt bijvoorbeeld één pagina die via HTTP wordt aangeboden en de volgende pagina die via HTTPS wordt verzonden. AppMeasurement heeft vanwege protocolverschillen geen toegang tot gegevens over het bijhouden van koppelingen in de sessieopslag.
* Sessieopslag werkt niet in verschillende subdomeinen. Een bezoeker navigeert bijvoorbeeld naar `store.example.com`, navigeert vervolgens naar `toys.example.com`. AppMeasurement heeft vanwege verschillende subdomeinen geen toegang tot gegevens voor het bijhouden van koppelingen in de sessieopslag.

>[!TIP]
>
>De meest betrouwbare implementatie die sessieopslag gebruikt voor het bijhouden van koppelingen, biedt alle inhoud via HTTPS op één subdomein.

AppMeasurement verwijdert de gegevens van de verbinding het volgen van de zittingsopslag na het verzenden van een klap aan Adobe. Deze verloopt ook automatisch wanneer het browsertabblad wordt gesloten.

## De opslag van de de zittingszitting van het verbindingsspoor gebruiken gebruikend Web SDK

De SDK van het Web ondersteunt deze functionaliteit niet.

## De opslag van de verbindingsspoorzitting gebruiken gebruikend de uitbreiding van Adobe Analytics

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de syntaxis van het AppMeasurement.

## s.useLinkTrackSessionStorage in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

De `s.useLinkTrackSessionStorage` variabele is een Booleaanse waarde die bepaalt of het AppMeasurement sessieopslag gebruikt voor het bijhouden van koppelingen in plaats van de `s_sq` cookie. De standaardwaarde is `false`. Deze variabele instellen op `true` als u wilt dat AppMeasurement sessieopslag gebruikt in plaats van de `s_sq` cookie voor het bijhouden van koppelingen en Activity Map.

```js
s.useLinkTrackSessionStorage = true;
```
