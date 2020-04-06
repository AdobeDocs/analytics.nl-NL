---
title: Meteen artikelen implementeren met Facebook
description: Implementeer Adobe Analytics op Facebook Instant Article-pagina's.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Meteen artikelen implementeren met Facebook

Met Facebook Instant Articles kunnen uitgevers snelle, interactieve artikelen maken op Facebook. Instant artikelen kunnen inhoud tot tien keer sneller laden dan mobiel internet.

U kunt Adobe Analytics insluiten op Facebook Instant Articles om het gedrag van de bezoeker te volgen. Aangezien de inhoud van uitgevers zich binnen de Facebook-app bevindt en niet op de websites van de uitgever, verschilt de methode van codering enigszins van een standaard analytische implementatie.

## Workflow

De volgende overkoepelende workflow voor het implementeren van Adobe Analytics:

1. Maak een `stats.html` pagina. Code deze pagina om de parameters van het vraagkoord van URL te trekken en elke parameter aan een variabele van de Analyse toe te wijzen
1. De `stats.html` pagina hosten op uw webserver
1. Analyses implementeren in het Facebook Instant Article door naar het `stats.html` bestand in een iframe te verwijzen
1. Parameters voor querybepaling opnemen in het iframe- `src` kenmerk

### Stap 1: Een `stats.html` pagina maken

U kunt de HTML-voorbeeldcode hieronder gebruiken om stats van de instant artikelen vast te leggen. Dit bestand wordt doorgaans gehost op een van de webservers van uw bedrijf. Elke keer dat een InstantArticle wordt geladen, wordt het bestand in een iframe geladen, waardoor gegevens naar Adobe worden verzonden.

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
      var s_account = "examplersid";
      var s_trackingServer = "example.sc.omtrdc.net";
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

### Stap 2: De `stats.html` pagina hosten op uw webserver

Adobe raadt u aan uw `stats.html` pagina naast de nieuwste versie van `AppMeasurement.js` en `VisitorAPI.js`. Werk met de juiste engineeringteams in uw organisatie om dit bestand op de juiste locatie te hosten.

### Stap 3: Referentie `stats.html` op elke pagina van Facebook Instant Article

Wanneer u Facebook Instant Article-inhoud maakt, sluit u de HTML-inhoud van de analyse in een iframe in. Bijvoorbeeld:

```html
<iframe class="no-margin" src="https://example.com/stats.html" height="0"></iframe>
```

### Stap 4: Aangepaste variabelen en gebeurtenissen bijhouden instellen

Aangepaste variabelen en gebeurtenissen kunnen binnen de HTML van de analyse op twee manieren worden bijgehouden:

* Waarden en gebeurtenissen van variabelen rechtstreeks op de `stats.html` pagina opnemen. Variabelen die u hier definieert, zijn het beste voor waarden die doorgaans hetzelfde zijn voor alle Instant-artikelen op Facebook.
* Mogelijke waarden opnemen als onderdeel van een queryreeks die verwijst naar het iframe. Met deze methode kunt u variabelewaarden vanuit het Instant Article van Facebook verzenden naar het iframe dat als host fungeert voor de Analytics-code.

In het volgende voorbeeld worden verschillende aangepaste variabelen in een queryreeks getoond. JavaScript in `stats.html` zou dan de queryreeks controleren met behulp van `s.Util.getQueryParam()`.

```html
<iframe class="no-margin" src="https://example.com/stats.html?eVar2=Dynamic%20article%20title&pageName=Example%20article%20name&cmpId=exampleID123" height="0"></iframe>
```

>[!NOTE] De dimensie Referrer wordt niet automatisch bijgehouden vanwege de aard van iframes. Zorg ervoor dat u deze dimensie als deel van uw vraagkoord opneemt als u het wilt volgen.

## Meteen artikelen en privacy op Facebook

Zolang de HTML-pagina Analytics op uw webserver wordt gehost, ondersteunt Adobe uw bestaande privacybeleid voor alle onmiddellijke Facebook-artikelen. Als een gebruiker op uw primaire site niet meer wil volgen, weigert hij of zij al uw onmiddellijke Facebook-artikelen te volgen. De nutspagina steunt ook de Dienst van de Identiteit van de Ervaring Cloud zodat u de Gegevens van het Onmiddellijk Artikel van Facebook met de rest van de Cloud van de Ervaring kunt integreren.
