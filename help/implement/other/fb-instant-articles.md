---
title: Implementeren met Facebook Instant Artikelen
description: Adobe Analytics implementeren op Facebook Instant Article-pagina's.
feature: Implementation Basics
exl-id: 2189f70d-32f0-4137-9d53-7acab0f15e6c
role: Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# Implementeren met Facebook Instant Artikelen

Met facebook Instant Articles kunnen uitgevers snelle, interactieve artikelen maken op Facebook. Instant artikelen kunnen inhoud tot tien keer sneller laden dan mobiel internet.

U kunt Adobe Analytics insluiten in Facebook Instant-artikelen om het gedrag van bezoekers bij te houden. Aangezien de inhoud van uitgevers zich binnen de Facebook-app en niet op de websites van de uitgever bevindt, verschilt de methode van codering enigszins van een standaard analytische implementatie.

## Workflow

De overkoepelende workflow voor het implementeren van Adobe Analytics is als volgt:

1. Een `stats.html` pagina. Code deze pagina om de parameters van het vraagkoord van URL te trekken en elke parameter aan een variabele van de Analyse toe te wijzen
1. De gastheer van `stats.html` pagina op uw webserver
1. Implementeer analyses in het Facebook Instant-artikel door te verwijzen naar de `stats.html` bestand in een iframe
1. Parameters voor query-plaatsing opnemen in iframe `src` attribute

### Stap 1: Een `stats.html` page

U kunt de onderstaande voorbeeldweergave HTML gebruiken om stats van de instant-artikelen vast te leggen. Dit bestand wordt doorgaans gehost op een van de webservers van uw bedrijf. Elke keer dat een InstantArticle wordt geladen, wordt het bestand in een iframe geladen, waardoor gegevens naar de Adobe worden verzonden.

```html
<html>
  <head>
    <title>Facebook Stats</title>
      <script language="javaScript" type="text/javascript" src="VisitorAPI.js"></script>
      <script language="javaScript" type="text/javascript" src="AppMeasurement.js"></script>
  </head>
  <body>
    <script>
      var v_orgId = "INSERT-ORG-ID-HERE";
      var s_account = "examplersid1,examplersid2";
      var s_trackingServer = "example.data.adobedc.net";
      var visitor = Visitor.getInstance(v_orgId);
      visitor.trackingServer = s_trackingServer;

      var s = s_gi(s_account);
      s.account = s_account;
      s.trackingServer = s_trackingServer;
      s.visitor = visitor;

      s.pageName = s.Util.getQueryParam("pageName");
      s.pageURL = document.referrer; // The referrer to the utility page is the parent frame
      s.campaign = s.Util.getQueryParam("cmpId");
      s.eVar1 = "Facebook Instant Article";
      s.eVar2 = s.Util.getQueryParam("eVar2");

      s.t();
    </script>
  </body>
</html>
```

### Stap 2: Gastheer de `stats.html` pagina op uw webserver

Adobe raadt u aan uw `stats.html` pagina naast de laatste versie van `AppMeasurement.js` en `VisitorAPI.js`. Werk met de juiste technische teams in uw organisatie om dit bestand op de juiste locatie te hosten.

### Stap 3: Verwijzing `stats.html` op elke Facebook Instant Article-pagina

Wanneer u Facebook Instant Article-inhoud maakt, sluit u de inhoud van de analytics HTML in een iframe in. Bijvoorbeeld:

```html
<iframe class="no-margin" src="https://example.com/stats.html" height="0"></iframe>
```

### Stap 4: Aangepaste variabele en gebeurtenis-tracking instellen

Aangepaste variabelen en gebeurtenissen kunnen binnen de analytische HTML worden bijgehouden via twee verschillende methoden:

* Waarden en gebeurtenissen van variabelen rechtstreeks opnemen in het dialoogvenster `stats.html` pagina. Variabelen die hier worden gedefinieerd, zijn het meest geschikt voor waarden die doorgaans hetzelfde zijn voor alle Facebook Instant-artikelen.
* Mogelijke waarden opnemen als onderdeel van een queryreeks die verwijst naar het iframe. Met deze methode kunt u variabelewaarden vanuit het Facebook Instant Article verzenden naar het iframe dat als host fungeert voor de Analytics-code.

In het volgende voorbeeld worden verschillende aangepaste variabelen in een queryreeks getoond. Het JavaScript in `stats.html` zou dan de queryreeks controleren met `s.Util.getQueryParam()`.

```html
<iframe class="no-margin" src="https://example.com/stats.html?eVar2=Dynamic%20article%20title&pageName=Example%20article%20name&cmpId=exampleID123" height="0"></iframe>
```

>[!NOTE]
>
>De dimensie Referrer wordt niet automatisch bijgehouden vanwege de aard van iframes. Zorg ervoor dat u deze dimensie als deel van uw vraagkoord opneemt als u het wilt volgen.

## Facebook Instant Artikelen en privacy

Zolang de pagina Analytics HTML wordt gehost op uw webserver, biedt Adobe ondersteuning voor uw bestaande privacybeleid voor alle Facebook Instant-artikelen. Als een gebruiker op uw primaire site niet meer wil volgen, kan hij of zij ook niet meer op al uw Facebook Instant-artikelen volgen. De nutspagina steunt ook de Dienst van de Identiteit van Adobe Experience Cloud zodat u de gegevens van het Artikel van Facebook Instant met de rest van het Experience Cloud kunt integreren.
