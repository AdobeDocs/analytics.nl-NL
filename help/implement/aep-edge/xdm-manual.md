---
title: XDM-gegevens handmatig toewijzen aan Analyse
description: 'XDM-gegevens handmatig toewijzen van Experience Platform aan Adobe Analytics '
translation-type: tm+mt
source-git-commit: 717c3e23eb2c3fb2477bd77ea92a1dce744f02df
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 0%

---


# XDM-gegevens handmatig toewijzen aan Analyse

De SDK van het Web van het Platform van de Ervaring van Adobe (AEP) omvat hulpmiddelen om u te helpen gegevens tussen het Platform en Analytics manueel in kaart brengen.

Voor XDM-gegevens die niet automatisch worden toegewezen aan Analytics, kunt u [contextgegevens](https://docs.adobe.com/content/help/en/analytics/implementation/vars/page-vars/contextdata.html) toevoegen die overeenkomen met uw [schema](https://docs.adobe.com/content/help/en/experience-platform/xdm/schema/composition.html). Vervolgens kan het door de [verwerkingsregels](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/processing-rules/processing-rules-configuration/t-processing-rules.html) van Analytics worden gebruikt om analytische variabelen te vullen.

Ook, kunt u een standaardreeks acties en productlijsten gebruiken om gegevens met het Web SDK van AEP te verzenden of terug te winnen. Zie [Producten](https://docs.adobe.com/content/help/en/experience-platform/edge/implement/commerce.html)om dit te doen.

## Contextgegevens

Voor gebruik door Analytics worden XDM-gegevens afgevlakt met puntnotatie en beschikbaar gemaakt als `contextData`. In de volgende lijst met waardeparen ziet u een voorbeeld van `context data`:

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
          "g": "http://example.com/home",
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

Alle gegevens die door het randnetwerk worden verzameld, zijn toegankelijk via [verwerkingsregels](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/processing-rules/processing-rules-configuration/t-processing-rules.html). In Analytics, kunt u verwerkingsregels gebruiken om contextgegevens in de variabelen van de Analyse op te nemen.

In de volgende regel is Analytics bijvoorbeeld ingesteld op het vullen van **interne zoektermen (eVar2)** met de gegevens die zijn gekoppeld aan **a.x_atag.search.term(Context Data)**.

![](assets/examplerule.png)


## XDM-schema

Het Platform van de ervaring gebruikt schema&#39;s om de structuur van gegevens op een verenigbare en herbruikbare manier te beschrijven. Door gegevens consistent in verschillende systemen te definiëren, wordt het eenvoudiger om betekenis te behouden en zo waarde te verkrijgen van gegevens. De de contextgegevens van Analytics werken met de structuur die door schema wordt bepaald.

Het volgende voorbeeld toont hoe het [`event` bevel](https://docs.adobe.com/content/help/en/experience-platform/edge/fundamentals/tracking-events.html) met de `xdm` optie kan worden gebruikt om gegevens met het Web SDK van AEP te verzenden en terug te winnen. In dit voorbeeld, past het `event` bevel het Schema [van de Details van de Handel van](https://github.com/adobe/xdm/blob/1c22180490558e3c13352fe3e0540cb7e93c69ca/docs/reference/context/experienceevent-commerce.schema.md) ExperienceEvent aan zodat productListItems `name` en de `SKU` waarden worden gevolgd:


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

Voor meer informatie bij het volgen van gebeurtenissen met het Web SDK van AEP, zie het [Volgen gebeurtenissen](https://docs.adobe.com/content/help/en/experience-platform/edge/fundamentals/tracking-events.html).