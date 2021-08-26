---
title: XDM-gegevens handmatig toewijzen aan Analyse
description: XDM-gegevens handmatig toewijzen van Experience Platform aan Adobe Analytics
exl-id: 6d973b35-1558-435c-9ae5-80c012d4e7ba
source-git-commit: 7cb2489c2deaf8e75c71589895314067a010caf8
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 0%

---

# XDM-gegevens handmatig toewijzen aan Analyse

De SDK van het Web van Adobe Experience Platform (AEP) bevat hulpmiddelen om u te helpen gegevens tussen het Platform en Analytics manueel in kaart te brengen.

Voor XDM-gegevens die niet automatisch aan Analytics worden toegewezen, kunt u [contextgegevens](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/contextdata.html) toevoegen om uw [schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html) aan te passen. Dan kan het door Analytics [verwerkingsregels](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/processing-rules/processing-rules-configuration/t-processing-rules.html) worden gebruikt om de variabelen van de Analyse te bevolken.

Ook, kunt u een standaardreeks acties en productlijsten gebruiken om gegevens met [AEP Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=en) te verzenden of terug te winnen.

## Contextgegevens

Te gebruiken door Analytics, worden de gegevens XDM afgevlakt gebruikend puntnotatie en ter beschikking gesteld als `contextData`. In de volgende lijst met waardeparen ziet u een voorbeeld van `context data`:

```javascript
{
          "bh": "900",
          "bw": "1680",
          "c": "24",
          "c.a.d.key.[0]": "value1",
          "c.a.d.key.[1]": "value2",
          "c.a.d.object.key1": "value1",
          "c.a.d.object.key2.[0]": "value2",
          "c.a.x.environment.browserdetails.javascriptenabled": "true",
          "c.a.x.environment.type": "browser",
          "cust_hit_time_gmt": "1579781427",
          "g": "https://example.com/home",
          "gn": "home",
          "j": "1.8.5",
          "k": "Y",
          "s": "1680x1050",
          "tnta": "218287:1:0|0,218287:1:0|2,218287:1:0|1,218287:1:0|32767,218287:1:0|1,218287:1:0|0,218287:1:0|1,218287:1:0|0,218287:1:0|1",
          "user_agent": "Mozilla/5.0 AppleWebKit/537.36 Safari/537.36",
          "v": "Y"
        }
```

## Verwerkingsregels

Alle gegevens die door het randnetwerk worden verzameld, zijn toegankelijk via [verwerkingsregels](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/processing-rules/processing-rules-configuration/t-processing-rules.html). In Analytics, kunt u verwerkingsregels gebruiken om contextgegevens in de variabelen van de Analyse op te nemen.

In de volgende regel is Analytics bijvoorbeeld ingesteld op het vullen van **Interne zoektermen (eVar2)** met de gegevens die zijn gekoppeld aan **a.x_atag.search.term(Context Data)**.

![](assets/examplerule.png)


## XDM-schema

Het Experience Platform gebruikt schema&#39;s om de structuur van gegevens op een verenigbare en herbruikbare manier te beschrijven. Door gegevens consistent in verschillende systemen te definiëren, wordt het eenvoudiger om betekenis te behouden en zo waarde te verkrijgen van gegevens. De de contextgegevens van Analytics werken met de structuur die door schema wordt bepaald.

In het volgende voorbeeld wordt getoond hoe de opdracht [`event`](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html) kan worden gebruikt met de optie `xdm` om gegevens te verzenden en op te halen met de AEP Web SDK. In dit voorbeeld komt de opdracht `event` overeen met het [ExperienceEvent Commerce Details Schema](https://github.com/adobe/xdm/blob/1c22180490558e3c13352fe3e0540cb7e93c69ca/docs/reference/context/experienceevent-commerce.schema.md), zodat de waarden productListItems `name` en `SKU` worden bijgehouden:


```
alloy("event",{
  "xdm":{
    "commerce":{
      "productViews":{
        "value":1
      }
    },
    "productListItems":[
      {
        "SKU":"HT105",
        "name":"Large Field Hat",
      },
      {
        "SKU":"HT104",
        "name":"Small Field Hat",
      }
    ]
  }
});
```

Zie [Gebeurtenissen bijhouden](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html) voor meer informatie over het bijhouden van gebeurtenissen met de AEP Web SDK.
