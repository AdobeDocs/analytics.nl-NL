---
title: AppMeasurement voor JavaScript
description: Leer hoe u Adobe Analytics implementeert met JavaScript zonder een tagbeheersysteem.
translation-type: tm+mt
source-git-commit: 59956169308291e7607a2712cd63a802d7b8bd11

---


# AppMeasurement voor JavaScript

AppMeasurement voor JavaScript is historisch gezien een veelgebruikte methode geweest voor het implementeren van Adobe Analytics. Als tagbeheersystemen steeds populairder worden, wordt het gebruik van [Adobe Experience Platform Launch](../launch/overview.md) echter aanbevolen.

## Algemene workflow voor het verzenden van gegevens naar Adobe met JavaScript

1. Laad het `AppMeasurement.js` bestand. Dit bestand bevat de bibliotheken die nodig zijn om gegevens naar Adobe te verzenden.

   ```html
   <script src="AppMeasurement.js"></script>
   ```

2. Definieer configuratievariabelen binnen `AppMeasurement.js`. Wanneer het object Analytics wordt geïnstantieerd, zorgen deze variabelen ervoor dat de instellingen voor gegevensverzameling correct zijn. Zie de variabelen [van de](../vars/config-vars/configuration-variables.md) Configuratie voor een volledige lijst van variabelen u kunt bepalen.

   ```js
   // Instantiate the Analytics tracking object with report suite ID
   var s_account = "examplersid";
   var s=s_gi(s_account);
   // Make sure data is sent to the correct location
   s.trackingServer = "example.omtrdc.net";
   ```

3. Definieer variabelen op paginaniveau in de paginacode van uw site. Deze variabelen bepalen de specifieke afmetingen en de meetgegevens die naar Adobe worden verzonden. Zie [Paginariabelen](../vars/page-vars/page-variables.md) voor een volledige lijst met variabelen die u kunt definiëren.

   ```js
   s.pageName = "Example page";
   s.eVar1 = "Example eVar";
   s.events = "event1";
   ```

4. Wanneer alle variabelen op paginaniveau zijn gedefinieerd, verzendt u de gegevens naar Adobe met behulp van de `t` functie. Zie [het](../vars/functions/t-method.md) voor meer informatie.

   ```js
   s.t();
   ```
