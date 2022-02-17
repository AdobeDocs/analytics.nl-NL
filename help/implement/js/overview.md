---
title: AppMeasurement voor JavaScript
description: Leer hoe u Adobe Analytics implementeert met JavaScript zonder een tagbeheersysteem.
feature: Implementation Basics
exl-id: 25b9d768-c641-4f6c-a4ae-0d6c238c4776
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# AppMeasurement voor JavaScript

AppMeasurement voor JavaScript is historisch gezien een veelgebruikte methode geweest om Adobe Analytics te implementeren. Met de toenemende populariteit van systemen voor tagbeheer kunt u echter [tags in Adobe Experience Platform](../launch/overview.md) aanbevolen.

## Algemene workflow voor het verzenden van gegevens naar Adobe met JavaScript

1. Laad de `AppMeasurement.js` bestand. Dit bestand bevat de bibliotheken die nodig zijn om gegevens naar Adobe te verzenden.

   ```html
   <script src="AppMeasurement.js"></script>
   ```

2. Configuratievariabelen definiëren binnen `AppMeasurement.js`. Wanneer het object Analytics wordt geïnstantieerd, zorgen deze variabelen ervoor dat de instellingen voor gegevensverzameling correct zijn. Zie [Configuratievariabelen](../vars/config-vars/configuration-variables.md) voor een volledige lijst met variabelen die u kunt definiëren.

   ```js
   // Instantiate the Analytics tracking object with report suite ID
   var s_account = "examplersid";
   var s=s_gi(s_account);
   // Make sure data is sent to the correct location
   s.trackingServer = "example.data.adobedc.net";
   ```

3. Definieer variabelen op paginaniveau in de paginacode van uw site. Deze variabelen bepalen de specifieke afmetingen en de meetwaarden die naar Adobe worden verzonden. Zie [Paginariabelen](../vars/page-vars/page-variables.md) voor een volledige lijst met variabelen die u kunt definiëren.

   ```js
   s.pageName = "Example page";
   s.eVar1 = "Example eVar";
   s.events = "event1";
   ```

4. Wanneer alle variabelen op paginaniveau zijn gedefinieerd, verzendt u de gegevens naar Adobe met de opdracht `t()` methode. Zie [t](../vars/functions/t-method.md) voor meer informatie .

   ```js
   s.t();
   ```
