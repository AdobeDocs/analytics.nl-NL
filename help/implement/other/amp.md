---
title: Implementeren met AMP
description: Adobe Analytics implementeren op AMP-pagina's.
translation-type: tm+mt
source-git-commit: c3c581eab8a4677831968574c9fb8d6f6eadd7e9
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 0%

---


# Implementeren met AMP

[](https://amp.dev) AMP is een open-source HTML-framework dat een eenvoudige manier biedt om snel en probleemloos webpagina&#39;s te maken.

Aangezien Adobe Analytics een JavaScript-bibliotheek gebruikt om een aanvraag voor een afbeelding te compileren en te verzenden, moet u de implementatie aanpassen om gegevens op pagina&#39;s met AMP naar Adobe te verzenden.

## Bepalen welke methode Adobe Analytics op pagina&#39;s moet worden geïmplementeerd met AMP

Adobe heeft twee methoden gemaakt om Adobe Analytics op pagina&#39;s te implementeren met AMP. Beide gebruiken de tag `<amp-analytics>` HTML. Zie [amp-analytics tag](https://amp.dev/documentation/components/amp-analytics) in de documentatie van AMP voor meer informatie.

* **Gebruik de  `"adobeanalytics"` volgende sjabloon**: Construeer het verzoek Analytics rechtstreeks op de pagina
* **Gebruik de  `"analytics_nativeConfig"` volgende sjabloon**: Gebruik een iframe met dezelfde toepassingsmetingscode die u op uw normale site implementeert

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

Weeg de voor- en nadelen binnen uw organisatie om te bepalen welke methode u wilt gebruiken. Zie [AMP-voorbeelden1/> op Adobe&lt;itHub-opslagplaats voor voorbeeldcode.](https://github.com/Adobe-Marketing-Cloud/mobile-services/tree/master/samples/mobile-web)

>[!WARNING]
>
>Gebruik niet zowel de `"adobeanalytics"`- als `"adobeanalytics_nativeConfig"`-sjablonen op dezelfde pagina met AMP. Als u dit probeert, kunt u fouten in de browserconsole genereren en bezoekers dubbel tellen.

## Methode 1: Gebruik de tag amp-analytics met de sjabloon &quot;adobeanalytics&quot;

De sjabloon `"adobeanalytics"` voor het bijhouden van sjablonen gebruikt de HTML-tag `<amp-analytics>` om rechtstreeks een aanvraag voor het bijhouden van wijzigingen samen te stellen. U kunt raakverzoeken opgeven die worden geactiveerd bij specifieke paginagebeurtenissen, zoals wanneer de pagina zichtbaar wordt of bij een klik. Klik op gebeurtenissen om deze op bepaalde element-id&#39;s of -klassen toe te passen door een kiezer op te geven. U kunt de sjabloon laden door `type="adobeanalytics"` toe te voegen aan de tag amp-analytics.

In het volgende codevoorbeeld worden twee triggers gedefinieerd: `pageLoad` en `click`. De trigger `pageLoad` wordt geactiveerd wanneer het document zichtbaar wordt en bevat de variabele `pageName` zoals gedefinieerd in de sectie `vars`. De tweede trigger `click` wordt geactiveerd wanneer op een knop wordt geklikt. `eVar1` wordt ingesteld voor deze gebeurtenis met de waarde  `button clicked`.

```html
<amp-analytics type="adobeanalytics">
  <script type="application/json">
    {
      "requests": {
        "myClick": "${click}&v1=${eVar1}",
      },
      "vars": {
        "host": "example.data.adobedc.net",
        "reportSuites": "reportSuiteID",
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

In de `click` trigger kunt u een kiezer opgeven om ervoor te zorgen dat wanneer op het specifieke DOM-element wordt geklikt (in dit geval elke knop), het `buttonClick`-verzoek wordt geactiveerd en automatisch wordt ingesteld om deze hit aan te duiden als een aanroep om de koppeling te volgen.

Daarnaast ondersteunt `amp-analytics` een aantal variabele vervangingen, zodat AMP gegevenswaarden kan leveren waarvan het gebruik bekend is. Zie [variabelen die in amp-analytics](https://github.com/ampproject/amphtml/blob/master/extensions/amp-analytics/analytics-vars.md) op GitHub worden ondersteund voor meer informatie.

>[!NOTE]
>
>Afbeeldingsverzoeken die met deze methode naar Adobe worden verzonden, bevatten geen gegevens voor veel standaardrapporten (bijvoorbeeld browser, schermgrootte of referentie). Als u deze informatie in hits wilt opnemen, moet u ervoor zorgen dat deze worden opgenomen in de queryreeks voor afbeeldingsverzoeken. Zie [Query-parameters voor gegevensverzameling](../validate/query-parameters.md) voor meer informatie.

Adobe identificeert bezoekers met een ingebouwde AMP-functie en stelt de cookie `adobe_amp_id` in. Deze bezoeker-id is uniek voor elke andere id die door Adobe Analytics is ingesteld (bijvoorbeeld het cookie `s_vi`). De Adobe Experience Cloud ID Service wordt niet ondersteund met deze implementatiemethode.

>[!NOTE]
>
>AMP gebruikt CDN&#39;s om inhoud te leveren. Het is gestructureerd om voor elke CDN een andere unieke bezoeker te tellen waaruit een bezoeker inhoud ophaalt, waardoor het aantal unieke bezoekers kan toenemen.

Het gebruik van een aparte rapportsuite voor AMP-pagina&#39;s wordt aanbevolen, omdat AMP unieke bezoekers identificeert.

Deze oplossing vereist dat de trackingserver die u opgeeft in de eigenschap `host` overeenkomt met de trackingserver op uw hoofdsite, zodat uw bestaande besturingselementen voor het privacybeleid worden gerespecteerd. Anders maakt u een apart privacybeleid voor pagina&#39;s met AMP.

## Methode 2: Gebruik de tag amp-analytics met de sjabloon &quot;adobeanalytics_nativeConfig&quot;

De tag `"adobeanalytics_nativeConfig"` is eenvoudiger te implementeren, omdat deze dezelfde tagmethodologie gebruikt als voor uw normale webpagina&#39;s. Voeg het volgende toe aan uw `amp-analytics`-tag:

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

Deze benadering verzendt gegevens naar een nutswebpagina door middel van query-tekenreeksparameters die aan de `iframeMessage` aanvraagparameter zijn toegevoegd. Deze querytekenreeksparameters kunnen elke gewenste naam hebben, zolang uw `stats.html`-pagina is geconfigureerd om gegevens van deze parameters te verzamelen.

De sjabloon `"adobeanalytics_nativeConfig"` voegt ook parameters van queryreeksen toe op basis van de variabelen die worden vermeld in de sectie `extraUrlParams` van de tag amp-analytics. In het bovenstaande voorbeeld zijn de parameters `pageName` en `v1` opgenomen.

>[!IMPORTANT]
>
>Uw `stats.html`-pagina moet worden gehost op een apart subdomein van het domein waarop de AMP zelf wordt gehost. Het AMP-framework staat geen iframes toe van hetzelfde subdomein waarop de AMP-pagina zelf bestaat. Als uw AMP bijvoorbeeld wordt gehost op `amp.example.com`, host u uw `stats.html`-pagina op een apart subdomein, zoals `ampmetrics.example.com`.

Als u deze methode gebruikt en een gebruiker niet meer op uw primaire site hoeft te volgen, wordt het bijhouden van de gegevens op al uw AMP&#39;s ook uitgeschakeld. Het gebruik van deze hulpprogrammapagina betekent ook dat AMP de Adobe Experience Cloud ID Service kan ondersteunen. Een afzonderlijke rapportsuite is niet vereist.

Met deze methode kunt u geen koppelingsreeksspatiëring en videoreeksspatiëring gebruiken. De tag `iframeMessage` in AMP kan slechts eenmaal per pagina worden geladen. U kunt dus geen andere afbeeldingsverzoeken verzenden nadat het frame is geladen. Voor deze methode zijn ook meer verwerkingsbronnen vereist, wat van invloed kan zijn op de schuifprestaties. Deze methode heeft geen invloed op de laadtijd van de pagina, aangezien alle bronnen asynchroon worden geladen.

## Veelgestelde vragen

**Is videotracering beschikbaar voor beide methoden?**

Nee. De AMP-standaard ondersteunt alleen triggers voor &quot;visible&quot;, &quot;click&quot; en &quot;timer&quot;. De tag biedt nog geen ondersteuning voor expliciete triggers voor het bijhouden van video&#39;s waarnaar de tag `amp-analytics` kan luisteren. Bovendien kan de sjabloon `"adobeanalytics_nativeConfig"` maar één keer worden geladen, zodat volgende afbeeldingsverzoeken nadat een pagina is geladen niet mogelijk zijn.

**Hoe kan ik AMP-bezoekers onderscheiden van andere bezoekers in mijn data?**

Voor alle AMP-pagina&#39;s verzamelt de [!UICONTROL JavaScript Version]-dimensie een waarde die vergelijkbaar is met `AMP vX.X`. U kunt ook een aangepaste dimensie instellen op &#39;AMP&#39;, zodat u deze bezoekers kunt segmenteren.

**Hoe verhoudt deze implementatiemethode zich tot de Instant-artikelen van Facebook?**

Onmiddellijke Facebook-artikelen bieden ondersteuning voor een vergelijkbare oplossing als de `"adobeanalytics_nativeConfig"`-methode. De `stats.html`-pagina voor deze methode kan tegelijk voorzien in uw analysebehoeften voor zowel AMP als FIA. Zie [Onmiddellijke Facebook-artikelen](fb-instant-articles.md) voor meer informatie over het implementeren van tracering op FIA.
