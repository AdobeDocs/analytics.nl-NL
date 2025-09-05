---
title: Adobe Analytics implementeren met AppMeasurement voor JavaScript
description: Leer hoe u Adobe Analytics implementeert met JavaScript zonder een tagbeheersysteem.
feature: Implementation Basics
exl-id: 25b9d768-c641-4f6c-a4ae-0d6c238c4776
role: Developer
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 4%

---

# Adobe Analytics implementeren met AppMeasurement voor JavaScript

AppMeasurement for JavaScript is historisch gezien een gangbare methode geweest om Adobe Analytics te implementeren. Nochtans, met stijgende populariteit van Tag Management Systems, wordt het gebruiken van [ markeringen in Adobe Experience Platform ](../launch/overview.md) geadviseerd.

Een overzicht op hoog niveau van de uitvoeringstaken:

![ hoe te om de Analyses van Adobe met AppMeasurement voor Javascript uit te voeren, zoals die in deze sectie wordt beschreven.](../assets/appmeasurement-annotated.png)

<table>

<tr>
<th style="width:5%"></th><th style="width:75%"><b>Taak</b></th><th style="width:20%"><b>Meer informatie</b></th>
</tr>

<tr>
<td>1</td><td>Verzeker u <b> een rapportreeks </b> hebt bepaald</td><td><a href="../../admin/tools/manage-rs/report-suites-admin.md">Report Suite Manager</a></td>
</tr>

<tr>
<td>2</td><td><b> Download de vereiste code van JavaScript voor AppMeasurement </b> van de Manager van de Code. Pak het bestand uit.</td><td><a href="../../admin/tools/code-manager-admin.md">Codebeheer</a></td>
</tr>

<tr>
<td>3</td><td><b> voeg <code>AppMeasurement.js</code> aan het malplaatjedossier van uw website </b> toe. De code bevat de bibliotheken die nodig zijn om gegevens naar Adobe te verzenden.

```html
<head>
  <script src="AppMeasurement.js"></script>
  …
</head>
```

</td><td></td>
</tr>

<tr>
<td>4</td><td><b> bepaal configuratievariabelen binnen <code>AppMeasurement.js</code></b>. Wanneer het object Analytics wordt geïnstantieerd, zorgen deze variabelen ervoor dat de instellingen voor gegevensverzameling correct zijn.

```JavaScript
// Instantiate the Analytics tracking object with report suite ID
var s_account = "examplersid";
var s=s_gi(s_account);
 
// Make sure data is sent to the correct tracking server
s.trackingServer = "example.data.adobedc.net";
```

</td><td><a href="../vars/config-vars/configuration-variables.md">Configuratievariabelen</a></td>
</tr>

<tr>
<td>5</td><td><b> bepaalt pagina-vlakke variabelen binnen de paginacode van uw plaats </b>. Deze variabelen bepalen de specifieke afmetingen en de meetgegevens die naar Adobe worden verzonden.

```js
s.pageName = "Example page";
s.eVar1 = "Example eVar";
s.events = "event1";
```

</td><td><a href="../vars/page-vars/page-variables.md">Paginariabelen</a></td>
</tr>

<tr>
<td>6</td><td><b> verzendt de gegevens naar Adobe gebruikend de <code>t()</code> methode </b>, wanneer alle paginariabelen worden bepaald.

```js
s.t();
```

</td><td><a href="../vars/functions/t-method.md">t(), methode</a></td>
</tr>

<tr>
<td>7</td><td><b> breidt en bevestigt uw implementatie </b> uit alvorens het uit aan productie te duwen.</b></td><td></td>
</tr>

</table>

## Aanvullende bronnen

- [Overzicht van variabelen, functies, methoden en plug-ins](../vars/overview.md)
