---
title: Implementeren met AMP
description: Adobe Analytics implementeren op AMP-pagina's.
feature: Implementation Basics
exl-id: 51a2662e-2a24-48f1-b17a-d1e1a57a394b
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 0%

---

# Implementeren met AMP

[AMP](https://amp.dev) is een open-source HTML-framework dat een eenvoudige manier biedt om snel en probleemloos webpagina&#39;s te maken.

Aangezien Adobe Analytics een JavaScript-bibliotheek gebruikt om een aanvraag voor een afbeelding te compileren en te verzenden, moet u de implementatie aanpassen om gegevens op pagina&#39;s met AMP naar Adobe te verzenden.

## Bepalen welke methode Adobe Analytics op pagina&#39;s moet worden geïmplementeerd met AMP

Adobe heeft twee methoden gemaakt om Adobe Analytics op pagina&#39;s te implementeren met AMP. Beide gebruiken `<amp-analytics>` HTML-tag. Zie [Label voor amp-analytics](https://amp.dev/documentation/components/amp-analytics) op de documentatie van AMP voor meer informatie.

* **Gebruik de `"adobeanalytics"` volgsjabloon**: Construeer het verzoek Analytics rechtstreeks op de pagina
* **Gebruik de `"analytics_nativeConfig"` volgsjabloon**: Gebruik een iframe met dezelfde toepassingsmetingscode die u op uw normale site implementeert

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

Weeg de voor- en nadelen binnen uw organisatie om te bepalen welke methode u wilt gebruiken. Zie [AMP-voorbeelden](https://github.com/Adobe-Marketing-Cloud/mobile-services/tree/master/samples/mobile-web) op Adobe-verzamelplaats

>[!WARNING]
>
>Gebruik niet beide `"adobeanalytics"` en `"adobeanalytics_nativeConfig"` sjablonen op dezelfde pagina met AMP. Als u dit probeert, kunt u fouten in de browser console en dubbele tellingen bezoekers produceren.

## Methode 1: Gebruik de tag amp-analytics met de sjabloon &quot;adobeanalytics&quot;

De `"adobeanalytics"` het volgen malplaatje gebruikt `<amp-analytics>` HTML-tag om een aanvraag voor bijhouden rechtstreeks samen te stellen. U kunt raakverzoeken opgeven die moeten worden geactiveerd bij specifieke paginagebeurtenissen, zoals wanneer de pagina zichtbaar wordt of wanneer u op een klik klikt. Klik gebeurtenissen kunnen worden aangepast om op bepaalde element-id&#39;s of -klassen toe te passen door een kiezer op te geven. U kunt de sjabloon laden door `type="adobeanalytics"` op de tag amp-analytics.

In het volgende codevoorbeeld worden twee triggers gedefinieerd: `pageLoad` en `click`. De `pageLoad` activeert als het document zichtbaar wordt en de `pageName` variabele zoals gedefinieerd in de `vars` sectie. De tweede trigger `click` wordt geactiveerd wanneer op een knop wordt geklikt. `eVar1` is ingesteld voor deze gebeurtenis met de waarde `button clicked`.

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

In de `click` trigger, kunt u een kiezer opgeven om ervoor te zorgen dat wanneer op het specifieke DOM-element wordt geklikt (in dit geval elke knop), de `buttonClick` Het verzoek wordt in brand gestoken en wordt automatisch geplaatst om deze hit als verbinding het volgen vraag aan te duiden.

Daarnaast `amp-analytics` ondersteunt een aantal variabelevervangingen, zodat AMP gegevenswaarden kan leveren waarvan het op de hoogte is. Zie [variabelen die worden ondersteund in amp-analytics](https://github.com/ampproject/amphtml/blob/master/extensions/amp-analytics/analytics-vars.md) op GitHub voor meer informatie.

>[!NOTE]
>
>Afbeeldingsverzoeken die met deze methode naar Adobe worden verzonden, bevatten geen gegevens voor veel standaardrapporten (bijvoorbeeld browser, schermgrootte of referentie). Als u deze informatie in klappen wilt omvatten, zorg ervoor zij als deel van het koord van de de vraagvraag van het beeldverzoek worden omvat. Zie [Query-parameters voor gegevensverzameling](../validate/query-parameters.md) voor meer informatie .

Adobe identificeert bezoekers die een ingebouwde functie van AMP gebruiken, en plaatst het koekje `adobe_amp_id`. Deze bezoekersidentiteitskaart is uniek aan een andere identiteitskaart die door Adobe Analytics wordt geplaatst (bijvoorbeeld `s_vi` cookie). De Adobe Experience Cloud ID-service wordt niet ondersteund met deze implementatiemethode.

>[!NOTE]
>
>AMP gebruikt CDN&#39;s om inhoud te leveren. Het is gestructureerd om een verschillende unieke bezoeker voor elke CDN te tellen een bezoeker ontvangt inhoud van, die unieke bezoekersaantallen kan opblazen.

Het gebruik van een aparte rapportsuite voor AMP-pagina&#39;s wordt aanbevolen, omdat AMP unieke bezoekers identificeert.

Deze oplossing vereist dat de volgende server u opgeeft in het dialoogvenster `host` de eigenschap komt overeen met de trackingserver op uw hoofdsite, zodat uw bestaande privacybeleidsbesturingselementen worden gerespecteerd. Anders maakt u een apart privacybeleid voor pagina&#39;s met AMP.

## Methode 2: Gebruik de tag amp-analytics met de sjabloon &quot;adobeanalytics_nativeConfig&quot;

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

De `"adobeanalytics_nativeConfig"` sjabloon voegt ook parameters van queryreeksen toe op basis van de variabelen in de `extraUrlParams` van de tag amp-analytics. In het bovenstaande voorbeeld wordt `pageName` en `v1` de parameters worden opgenomen.

>[!IMPORTANT]
>
>Uw `stats.html` pagina moet worden gehost op een apart subdomein van het domein waarop de AMP zelf wordt gehost. Het AMP-framework staat geen iFrames toe van hetzelfde subdomein waarop de AMP-pagina zelf bestaat. Als uw AMP bijvoorbeeld wordt gehost op `amp.example.com`, host uw `stats.html` pagina&#39;s in een afzonderlijk subdomein, zoals `ampmetrics.example.com`.

Als een gebruiker deze methode gebruikt en op uw primaire site niet meer wil bijhouden, wordt het bijhouden van de gegevens ook niet meer uitgevoerd op al uw AMP&#39;s. Het gebruik van deze hulpprogrammapagina betekent ook dat AMP de Adobe Experience Cloud ID Service kan ondersteunen. Een afzonderlijke rapportsuite is niet vereist.

Koppelingen bijhouden en video bijhouden kunnen niet worden gebruikt met deze methode. De `iframeMessage` -tag in AMP kan slechts één keer per pagina worden geladen, zodat u geen andere afbeeldingsaanvragen kunt verzenden nadat het frame is geladen. Voor deze methode zijn ook meer verwerkingsbronnen nodig die de schuifprestaties kunnen beïnvloeden. Deze methode heeft geen invloed op de laadtijd van de pagina, aangezien alle bronnen asynchroon worden geladen.

## Veelgestelde vragen

**Is video het volgen beschikbaar voor één van beide methode?**

Nee. De AMP-standaard ondersteunt alleen triggers voor &quot;visible&quot;, &quot;click&quot; en &quot;timer&quot;. De klasse biedt nog geen ondersteuning voor expliciete triggers voor het bijhouden van video&#39;s die `amp-analytics` tag kan luisteren naar . Ook de `"adobeanalytics_nativeConfig"` De sjabloon kan slechts eenmaal worden geladen, dus volgende afbeeldingsaanvragen nadat een pagina is geladen, zijn niet mogelijk.

**Hoe kan ik AMP-bezoekers onderscheiden van anderen in mijn gegevens?**

Voor alle AMP-pagina&#39;s [!UICONTROL JavaScript Version] dimensie verzamelt een waarde die vergelijkbaar is met `AMP vX.X`. U kunt ook een aangepaste dimensie instellen op &#39;AMP&#39;, zodat u deze bezoekers kunt segmenteren.

**Hoe verhoudt deze implementatiemethode zich tot Facebook Instant-artikelen?**

Facebook Instant Articles biedt een vergelijkbare oplossing voor de `"adobeanalytics_nativeConfig"` methode. De `stats.html` -pagina voor deze methode kunt u gebruiken voor uw analytische behoeften voor AMP en FIA tegelijk. Voor meer informatie over het uitvoeren van het volgen op FIA, zie [Facebook Instant Artikelen](fb-instant-articles.md).
