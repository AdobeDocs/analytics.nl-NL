---
title: Implementeren met AMP
description: Adobe Analytics implementeren op AMP-pagina's.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Implementeren met AMP

[AMP](https://amp.dev) is een open-source HTML-framework dat een eenvoudige manier biedt om snel en probleemloos webpagina&#39;s te maken.

Aangezien Adobe Analytics een JavaScript-bibliotheek gebruikt om een aanvraag voor een afbeelding te compileren en te verzenden, is het nodig dat de implementatie wordt aangepast om gegevens naar Adobe te verzenden op pagina&#39;s die AMP gebruiken.

## Bepaal welke methode u gebruikt om Adobe Analytics te implementeren op pagina&#39;s

Adobe heeft twee methoden gemaakt voor de implementatie van Adobe Analytics op pagina&#39;s met AMP. Beide gebruiken de `<amp-analytics>` HTML-tag. Zie [amp-analytics markering](https://github.com/ampproject/amphtml/tree/master/extensions/amp-analytics) op het ampproject GitHub voor meer informatie.

* **Gebruik de`"adobeanalytics"`volgende sjabloon**: Construeer het verzoek Analytics rechtstreeks op de pagina
* **Gebruik de`"analytics_nativeConfig"`volgende sjabloon**: Gebruik een iframe met dezelfde toepassingsmetingscode die u op uw normale site implementeert

In de volgende tabel worden deze twee methoden vergeleken:

|  | **Sjabloon &quot;adobeanalytics&quot;** | **&quot;adobeanalytics_nativeConfig&quot;-sjabloon** |
|---|---|---|
| Bezoeker/bezoek telt mee in bestaande rapportenreeks | Hoge inflatie | Minimale inflatie |
| Een aparte rapportsuite gebruiken | Aanbevolen | Niet nodig |
| Nieuwe bezoekers vs. retourbezoekers | Niet ondersteund | Ondersteund |
| Bezoekersidentiteitsservice | Niet ondersteund | Ondersteund |
| Video en koppeling bijhouden | Gedeeltelijke ondersteuning | Nog niet ondersteund |
| Uitvoeringsmoeilijkheden | Enigszins moeilijk | Relatief eenvoudig |
| Adobe Experience Cloud-integratie | Niet ondersteund | Gedeeltelijke ondersteuning |

Weeg de voor- en nadelen binnen uw organisatie om te bepalen welke methode u wilt gebruiken. Zie [AMP-voorbeelden](https://github.com/Adobe-Marketing-Cloud/mobile-services/tree/master/samples/mobile-web) in de GitHub-opslagplaats van Adobe voor voorbeeldcode.

>[!WARNING] Gebruik AMP niet zowel de `"adobeanalytics"` als de `"adobeanalytics_nativeConfig"` sjablonen op dezelfde pagina. Als u dit probeert, kunt u fouten in de browser console en dubbele tellingen bezoekers produceren.

## Methode 1: Gebruik de tag amp-analytics met de sjabloon &quot;adobeanalytics&quot;

In de `"adobeanalytics"` sjabloon voor bijhouden wordt de `<amp-analytics>` HTML-tag gebruikt om rechtstreeks een aanvraag voor bijhouden samen te stellen. U kunt raakverzoeken opgeven die moeten worden geactiveerd bij specifieke paginagebeurtenissen, zoals wanneer de pagina zichtbaar wordt of wanneer u op een klik klikt. Klik gebeurtenissen kunnen worden aangepast om op bepaalde element-id&#39;s of -klassen toe te passen door een kiezer op te geven. U kunt de sjabloon laden door deze toe te voegen `type="adobeanalytics"` aan de tag amp-analytics.

In het volgende codevoorbeeld worden twee triggers gedefinieerd: `pageLoad` en `click`. De `pageLoad` trigger wordt geactiveerd wanneer het document zichtbaar wordt en bevat de `pageName` variabele zoals gedefinieerd in de `vars` sectie. De tweede trigger wordt `click` geactiveerd wanneer op een knop wordt geklikt. `eVar1` wordt ingesteld voor deze gebeurtenis met de waarde `button clicked`.

```html
<amp-analytics type="adobeanalytics">
  <script type="application/json">
    {
      "requests": {
        "myClick": "${click}&v1=${eVar1}",
      },
      "vars": {
        "host": "example.sc.omtrdc.net",
        "reportSuites": "reportSuiteID",
        "pageName": "Adobe Analytics Using amp-analytics tag"
      },
      "triggers": {
        "pageLoad": {
          "on": "visible",
          "request": "pageView"
        },
        "click": {
          "on": "click",
          "selector": "button",
          "request": "myClick",
          "vars": {
            "eVar1": "button clicked"
          }
        }
      }
    }
  </script>
</amp-analytics>
```

In de `click` trekker, kunt u een selecteur specificeren om ervoor te zorgen dat wanneer het specifieke element DOM (in dit geval, om het even welke knoop) wordt geklikt, het `buttonClick` verzoek in brand wordt gestoken en automatisch wordt geplaatst om deze klem als verbinding het volgen vraag aan te duiden.

Daarnaast `amp-analytics` wordt een aantal variabelevervangingen ondersteund, zodat AMP gegevenswaarden kan leveren waarvan het op de hoogte is. Zie [variabelen die in amp-analytics](https://github.com/ampproject/amphtml/blob/master/extensions/amp-analytics/analytics-vars.md) op GitHub voor meer informatie worden gesteund.

>[!NOTE] Afbeeldingsverzoeken die met deze methode naar Adobe worden verzonden, bevatten geen gegevens voor veel standaardrapporten (bijvoorbeeld browser, schermgrootte of referentie). Als u deze informatie in klappen wilt omvatten, zorg ervoor zij als deel van het koord van de de vraagvraag van het beeldverzoek worden omvat. Zie de parameters [van de de inzamelingsvraag van](../validate/query-parameters.md) Gegevens voor meer informatie.

Adobe identificeert bezoekers die een ingebouwde functie van AMP gebruiken, en plaatst het koekje `adobe_amp_id`. Deze bezoeker-id is uniek voor elke andere id die door Adobe Analytics is ingesteld (bijvoorbeeld het `s_vi` cookie). De Adobe Experience Cloud ID Service wordt niet ondersteund met deze implementatiemethode.

>[!NOTE] AMP gebruikt CDN&#39;s om inhoud te leveren. Het is gestructureerd om een verschillende unieke bezoeker voor elke CDN te tellen een bezoeker ontvangt inhoud van, die unieke bezoekersaantallen kan opblazen.

Het gebruik van een aparte rapportsuite voor AMP-pagina&#39;s wordt aanbevolen, omdat AMP unieke bezoekers identificeert.

Deze oplossing vereist dat de volgende server u in het `host` bezit specificeert de volgende server op uw belangrijkste plaats aanpast, zodat uw bestaande controles van het privacybeleid worden geëerbiedigd. Anders maakt u een apart privacybeleid voor pagina&#39;s met AMP.

## Methode 2: Gebruik de tag amp-analytics met de sjabloon &quot;adobeanalytics_nativeConfig&quot;

De `"adobeanalytics_nativeConfig"` tag is eenvoudiger te implementeren, omdat deze dezelfde coderingsmethode gebruikt als voor uw normale webpagina&#39;s. Voeg het volgende toe aan uw `amp-analytics` tag:

```html
<amp-analytics type="adobeanalytics_nativeConfig">
  <script type="application/json">
    {
      "requests": {
        "base": "https://${host}",
        "iframeMessage": "${base}/stats.html?campaign=${queryParam(campaign)}&pageURL=${ampdocUrl}&ref=${documentReferrer}"
      },
      "vars": {
        "host": "example.sc.omtrdc.net"
      },
      "extraUrlParams": {
      "pageName": "Example AMP page",
      "v1": "eVar1 example value"
      }
    }
 </script>
</amp-analytics>
```

Er is ook een HTML-pagina vereist die wordt gehost op uw webservers:

```html
<html>
  <head>
    <title>Stats Example</title>
    <script language="JavaScript" type="text/javascript" src="VisitorAPI.js"></script>
    <script language="JavaScript" type="text/javascript" src="AppMeasurement.js"></script>
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
      s.visitorNamespace = s_visitorNamespace;
      s.visitor = visitor;
      s.pageName = s.Util.getQueryParam("pageName");
      s.eVar1 = s.Util.getQueryParam("v1");
      s.campaign = s.Util.getQueryParam("campaign");
      s.pageURL = s.Util.getQueryParam("pageURL");
      s.referrer = s.Util.getQueryParam("ref");
      s.t();
    </script>
  </body>
</html>
```

Deze benadering verzendt gegevens naar een nutWeb-pagina door vraagkoordparameters die aan de `iframeMessage` verzoekparameter worden toegevoegd. Deze parameters van het vraagkoord kunnen worden genoemd wat u houdt, zolang uw `stats.html` pagina wordt gevormd om gegevens van hen te verzamelen.

De `"adobeanalytics_nativeConfig"` sjabloon voegt ook parameters van queryreeksen toe op basis van de variabelen die worden vermeld in de `extraUrlParams` sectie van de tag amp-analytics. In het bovenstaande voorbeeld zijn de `pageName` parameters en de `v1` parameters opgenomen.

>[!IMPORTANT] De pagina moet worden gehost op een ander subdomein dan het domein waarop de geaccepteerde marktpraktijk wordt gehost. `stats.html` Het AMP-framework staat geen iFrames toe van hetzelfde subdomein waarop de AMP-pagina zelf bestaat. Als uw AMP bijvoorbeeld wordt gehost op `amp.example.com`, host u uw `stats.html` pagina op een apart subdomein, zoals `ampmetrics.example.com`.

Als een gebruiker deze methode gebruikt en op uw primaire site niet meer wil bijhouden, wordt het bijhouden van de gegevens ook niet meer uitgevoerd op al uw AMP&#39;s. Als u deze hulpprogrammapagina gebruikt, kan AMP ook ondersteuning bieden voor de Adobe Experience Cloud ID Service. Een afzonderlijke rapportsuite is niet vereist.

Koppelingen bijhouden en video bijhouden kunnen niet worden gebruikt met deze methode. De tag `iframeMessage` in AMP kan slechts één keer per pagina worden geladen. U kunt dus geen andere afbeeldingsaanvragen verzenden nadat het frame is geladen. Voor deze methode zijn ook meer verwerkingsbronnen nodig die de schuifprestaties kunnen beïnvloeden. Deze methode heeft geen invloed op de laadtijd van de pagina, aangezien alle bronnen asynchroon worden geladen.

## Veelgestelde vragen

**Is video het volgen beschikbaar voor één van beide methode?**

Nee. De AMP-standaard ondersteunt alleen triggers voor &quot;visible&quot;, &quot;click&quot; en &quot;timer&quot;. De tag biedt nog geen ondersteuning voor expliciete triggers voor het bijhouden van video&#39;s waarnaar de `amp-analytics` tag kan luisteren. Bovendien kan de `"adobeanalytics_nativeConfig"` sjabloon maar één keer worden geladen, zodat volgende afbeeldingsaanvragen nadat een pagina is geladen niet mogelijk zijn.

**Hoe kan ik AMP-bezoekers onderscheiden van anderen in mijn gegevens?**

Voor alle AMP-pagina&#39;s wordt met de [!UICONTROL JavaScript Version] dimensie een vergelijkbare waarde verzameld `AMP vX.X`. U kunt ook een aangepaste dimensie instellen op &#39;AMP&#39;, zodat u deze bezoekers kunt segmenteren.

**Hoe vergelijk deze implementatiemethode met Facebook Instant-artikelen?**

Facebook Instant Articles ondersteunt een vergelijkbare oplossing als de `"adobeanalytics_nativeConfig"` methode. De `stats.html` pagina voor deze methode kan aan uw analytische behoeften voor zowel AMP als FIA gelijktijdig voldoen. Raadpleeg [Metant-artikelen](fb-instant-articles.md)op Facebook voor meer informatie over het implementeren van tracering op FIA.
