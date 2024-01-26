---
title: Adobe Analytics implementeren met AppMeasurement voor JavaScript
description: Leer hoe u Adobe Analytics implementeert met JavaScript zonder een tagbeheersysteem.
feature: Implementation Basics
exl-id: 25b9d768-c641-4f6c-a4ae-0d6c238c4776
role: Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 4%

---

# Adobe Analytics implementeren met AppMeasurement voor JavaScript

AppMeasurement voor JavaScript is historisch gezien een veel gebruikte methode geweest om Adobe Analytics te implementeren. Maar met toenemende populariteit van Tag Management Systems, die [tags in Adobe Experience Platform](../launch/overview.md) wordt aanbevolen.

Een overzicht op hoog niveau van de uitvoeringstaken:

![Hoe te om AdobeAnalyses met AppMeasurement voor Javascript uit te voeren, zoals die in deze sectie wordt beschreven.](../assets/appmeasurement-annotated.png)

<table>

<tr>
<th style="width:5%"></th><th style="width:75%"><b>Taak</b></th><th style="width:20%"><b>Meer informatie</b></th>
</tr>

<tr>
<td>1</td><td>Zorg ervoor dat u <b>een rapportsuite gedefinieerd</b></td><td><a href="../../admin/admin/c-manage-report-suites/report-suites-admin.md">Report Suite Manager</a></td>
</tr>

<tr>
<td>2</td><td><b>De vereiste JavaScript-code voor AppMeasurement downloaden</b> van Codebeheer. Pak het bestand uit.</td><td><a href="../../admin/admin/code-manager-admin.md">Codebeheer</a></td>
</tr>

<tr>
<td>3</td><td><b>Toevoegen <code>AppMeasurement.js</code> naar het sjabloonbestand van uw website</b>. De code bevat de bibliotheken die nodig zijn om gegevens naar de Adobe te verzenden.

```html
<head>
  <script src="AppMeasurement.js"></script>
  …
</head>
```

</td><td></td>
</tr>

<tr>
<td>4</td><td><b>Configuratievariabelen definiëren binnen <code>AppMeasurement.js</code></b>. Wanneer het object Analytics wordt geïnstantieerd, zorgen deze variabelen ervoor dat de instellingen voor gegevensverzameling correct zijn.

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
<td>5</td><td><b>Definieer variabelen op paginaniveau in de paginacode van uw site</b>. Deze variabelen bepalen de specifieke afmetingen en de meetwaarden die naar de Adobe worden verzonden.

```js
s.pageName = "Example page";
s.eVar1 = "Example eVar";
s.events = "event1";
```

</td><td><a href="../vars/page-vars/page-variables.md">Paginariabelen</a></td>
</tr>

<tr>
<td>6</td><td><b>De gegevens naar de Adobe verzenden met de <code>t()</code> methode</b>, wanneer alle paginariabelen zijn gedefinieerd.

```js
s.t();
```

</td><td><a href="../vars/functions/t-method.md">t(), methode</a></td>
</tr>

<tr>
<td>7</td><td><b>Uw implementatie uitbreiden en valideren</b> voordat het naar de productie wordt verplaatst.</b></td><td></td>
</tr>

</table>

## Aanvullende bronnen

- [Overzicht van variabelen, functies, methoden en plug-ins](../vars/overview.md)
