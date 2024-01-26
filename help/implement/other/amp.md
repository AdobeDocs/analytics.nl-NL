---
title: Implementeren met AMP
description: Adobe Analytics implementeren op AMP-pagina's.
feature: Implementation Basics
exl-id: 51a2662e-2a24-48f1-b17a-d1e1a57a394b
role: Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '917'
ht-degree: 0%

---

# Implementeren met AMP

[AMP](https://amp.dev) is een open-source HTML-framework dat een eenvoudige manier biedt om snel en probleemloos webpagina&#39;s te maken.

Aangezien Adobe Analytics een JavaScript-bibliotheek gebruikt om een aanvraag voor een afbeelding te compileren en te verzenden, moet u de implementatie aanpassen om gegevens naar de Adobe te verzenden op pagina&#39;s die AMP gebruiken.

## Bepalen welke methode Adobe Analytics op pagina&#39;s moet worden geïmplementeerd met AMP

Adobe heeft twee methoden gemaakt om Adobe Analytics op pagina&#39;s te implementeren met AMP. Beide gebruiken `<amp-analytics>` HTML-tag. Zie [amp-analytics](https://amp.dev/documentation/components/amp-analytics) in de documentatie van AMP voor meer informatie.

* **Gebruik de `"adobeanalytics"` template**: Construeer het verzoek Analytics rechtstreeks op de pagina
* **Gebruik de `"analytics_nativeConfig"` template**: Gebruik een iframe met dezelfde AppMeasurement-code die u op uw normale site implementeert

In de volgende tabel worden deze twee methoden vergeleken:

|   | **`"adobeanalytics"`template** | **`"adobeanalytics_nativeConfig"`template** |
|---|---|---|
| Bezoeker/bezoek telt mee in bestaande rapportenreeks | Hoge inflatie | Minimale inflatie |
| Een aparte rapportsuite gebruiken | Aanbevolen | Niet nodig |
| Nieuwe bezoekers vs. retourbezoekers | Niet ondersteund | Ondersteund |
| Bezoekersidentiteitsservice | Niet ondersteund | Ondersteund |
| Video en koppeling bijhouden | Gedeeltelijke ondersteuning | Nog niet ondersteund |
| Probleem bij de uitvoering | Ongemakkelijk | Relatief eenvoudig |
| Adobe Experience Cloud-integratie | Niet ondersteund | Gedeeltelijke ondersteuning |

Weeg de voor- en nadelen af, zodat u de beste implementatiemethode voor uw organisatie kunt kiezen.

>[!WARNING]
>
>Gebruik niet beide `"adobeanalytics"` en `"adobeanalytics_nativeConfig"` sjablonen op dezelfde pagina met AMP. Als u dit probeert, kunt u fouten in de browser console en dubbele tellingen bezoekers produceren.

## Methode 1: De `<amp-analytics>` tag met de `"adobeanalytics"` template

De `"adobeanalytics"` het volgen malplaatje gebruikt `<amp-analytics>` HTML-tag om een aanvraag voor bijhouden rechtstreeks samen te stellen. U kunt raakverzoeken opgeven die moeten worden geactiveerd bij specifieke paginagebeurtenissen, zoals wanneer de pagina zichtbaar wordt of wanneer u op een klik klikt. Klik gebeurtenissen kunnen worden aangepast om op bepaalde element-id&#39;s of -klassen toe te passen door een kiezer op te geven. U kunt de sjabloon laden door `type="adobeanalytics"` op de tag amp-analytics.

In het volgende codevoorbeeld worden twee triggers gedefinieerd: `pageLoad` en `click`. De `pageLoad` activeert als het document zichtbaar wordt en de `pageName` variabele zoals gedefinieerd in de `vars` sectie. De tweede trigger `click` wordt geactiveerd wanneer op een knop wordt geklikt. De `eVar1` variabele wordt ingesteld voor deze gebeurtenis met de waarde `button clicked`.

```html
<amp-analytics type="adobeanalytics">
  <script type="application/json">
    {
      "requests": {
        "myClick": "${click}&v1=${eVar1}",
      },
      "vars": {
        "host": "example.data.adobedc.net",
        "reportSuites": "reportSuiteID1,reportSuiteID2",
        "pageName": "Adobe Analytics Using amp-analytics tag"
      },
      "triggers": {
        "pageLoad": {
          "on": "visible",
          "request": "pageview"
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

De `<amp-analytics>` -tag ondersteunt variabelevervangingen, zodat AMP gegevenswaarden kan opgeven die het kent. Zie [variabelen ondersteund in `amp-analytics`](https://github.com/ampproject/amphtml/blob/main/extensions/amp-analytics/analytics-vars.md) op GitHub voor meer informatie.

>[!NOTE]
>
>Afbeeldingsverzoeken die met deze methode naar de Adobe worden verzonden, bevatten geen gegevens voor veel standaardrapporten (bijvoorbeeld browser, schermgrootte of referentie). Als u deze informatie in klappen wilt omvatten, zorg ervoor dat zij als deel van het koord van de de vraagvraag van het beeldverzoek worden omvat. Zie [Query-parameters voor gegevensverzameling](../validate/query-parameters.md) voor een volledige lijst van beeldverzoeken vraagparameters en hun bijbehorende variabelen.

Adobe identificeert bezoekers die een ingebouwde functie van AMP gebruiken, en plaatst het koekje `adobe_amp_id`. Deze bezoeker-id is uniek voor elke andere id die door Adobe Analytics is ingesteld. Voor elke CDN waarvan een bezoeker inhoud ophaalt, wordt een andere unieke bezoeker geteld. Hierdoor kan het aantal unieke bezoekers stijgen. Het gebruik van een aparte rapportsuite voor AMP-pagina&#39;s wordt ten zeerste aanbevolen, omdat AMP unieke bezoekers identificeert. De Adobe Experience Cloud ID Service wordt niet ondersteund.

Deze oplossing vereist dat de volgende server u opgeeft in het dialoogvenster `host` de eigenschap komt overeen met de trackingserver op uw hoofdsite, zodat uw bestaande privacybeleidsbesturingselementen worden gerespecteerd. Anders maakt u een apart privacybeleid voor pagina&#39;s met AMP.

## Methode 2: De `<amp-analytics>` tag met de `"adobeanalytics_nativeConfig"` template

De `"adobeanalytics_nativeConfig"` -tag is eenvoudiger te implementeren, omdat deze dezelfde coderingsmethode gebruikt die u op uw normale webpagina&#39;s gebruikt. Voeg het volgende toe aan uw `amp-analytics` tag:

```html
<amp-analytics type="adobeanalytics_nativeConfig">
  <script type="application/json">
    {
      "requests": {
        "base": "https://${host}",
        "iframeMessage": "${base}/stats.html?campaign=${queryParam(campaign)}&pageURL=${ampdocUrl}&ref=${documentReferrer}"
      },
      "vars": {
        "host": "example.data.adobedc.net"
      },
      "extraUrlParams": {
      "pageName": "Example AMP page",
      "v1": "eVar1 example value"
      }
    }
 </script>
</amp-analytics>
```

Een HTML-pagina die wordt gehost op uw webservers is ook vereist:

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
      var s_account = "examplersid1,examplersid2";
      var s_trackingServer = "example.data.adobedc.net";
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

Deze benadering verzendt gegevens naar een nutWeb-pagina door vraagkoordparameters die aan worden toegevoegd `iframeMessage` request parameter. Deze parameters van het vraagkoord kunnen worden genoemd wat u houdt, zolang uw `stats.html` pagina is geconfigureerd om gegevens van deze pagina te verzamelen.

De `"adobeanalytics_nativeConfig"` sjabloon voegt ook parameters van queryreeksen toe op basis van de variabelen in de `extraUrlParams` van de `<amp-analytics>` -tag. In het bovenstaande voorbeeld wordt `pageName` en `v1` de parameters worden opgenomen.

>[!IMPORTANT]
>
>Uw `stats.html` pagina moet worden gehost op een apart subdomein van het domein waarop de AMP zelf wordt gehost. Het AMP-framework staat geen iFrames toe van hetzelfde subdomein waarop de AMP-pagina zelf bestaat. Als uw AMP bijvoorbeeld wordt gehost op `amp.example.com`, host uw `stats.html` pagina&#39;s in een afzonderlijk subdomein, zoals `ampmetrics.example.com`.

Als een gebruiker deze methode gebruikt en op uw primaire site niet meer wil bijhouden, wordt het bijhouden van de gegevens bij al uw AMP&#39;s ook uitgeschakeld. Het gebruik van deze hulpprogrammapagina betekent ook dat AMP de Adobe Experience Cloud ID Service kan ondersteunen. Een afzonderlijke rapportsuite is niet vereist.

Koppelingen bijhouden en video bijhouden kunnen niet worden gebruikt met deze methode. De `iframeMessage` -tag in AMP kan slechts één keer per pagina worden geladen, zodat u geen andere afbeeldingsaanvragen kunt verzenden nadat het frame is geladen. Voor deze methode zijn ook meer verwerkingsbronnen nodig die de prestaties van het schuiven kunnen beïnvloeden. Deze methode heeft geen invloed op de laadtijd van de pagina, aangezien alle bronnen asynchroon worden geladen.

## Veelgestelde vragen

**Hoe kan ik AMP-bezoekers onderscheiden van anderen in mijn gegevens?**

Voor alle AMP-pagina&#39;s [!UICONTROL JavaScript Version] dimensie verzamelt een waarde die vergelijkbaar is met `AMP vX.X`. U kunt ook een aangepaste dimensie instellen op &#39;AMP&#39;, zodat u deze bezoekers kunt segmenteren.

**Hoe verhoudt deze implementatiemethode zich tot Facebook Instant-artikelen?**

Facebook Instant Articles biedt een vergelijkbare oplossing voor de `"adobeanalytics_nativeConfig"` methode. De `stats.html` -pagina voor deze methode kunt u gebruiken voor uw analytische behoeften voor AMP en FIA tegelijk. Voor meer informatie over het uitvoeren van het volgen op FIA, zie [Facebook Instant Artikelen](fb-instant-articles.md).
