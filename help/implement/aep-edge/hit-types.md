---
title: Edge Network-gebeurtenistypen in Adobe Analytics
description: Hoe Adobe Analytics gebeurtenissen interpreteert die van de Edge Network zijn ontvangen.
feature: Implementation Basics
role: Admin, Developer
exl-id: 31085025-9c38-4375-8dfb-4fded6542ca7
source-git-commit: 0096a53505b3b1bc925c813c2c6c11ee3c7ee0c0
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---

# Edge Network-gebeurtenistypen in Adobe Analytics

Adobe Analytics behandelt treffers verschillend afhankelijk van welke functies u in AppMeasurement roept. Bijvoorbeeld, [`s.t`](/help/implement/vars/functions/t-method.md) en [`s.tl`](/help/implement/vars/functions/tl-method.md) omvatten of weglaten bepaalde dimensies en verhogende [ paginameningen ](/help/components/metrics/page-views.md) verschillend. Adobe Experience Platform bevat alleen de opdracht [`sendEvent` ](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/sendevent/overview) . Specifieke eigenschappen binnen de [`xdm` ](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/sendevent/xdm) of [`data` ](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/sendevent/data) lading bepalen hoe die gegevens in Adobe Analytics worden geïnterpreteerd.

Edge Network gebruikt de volgende logica om Adobe Analytics [ paginameningen ](/help/components/metrics/page-views.md) en [ verbindingsgebeurtenissen ](/help/components/metrics/page-events.md) te bepalen:

## Paginaweergaven en koppelingsgebeurtenissen met het `xdm` -object

| XDM-lading bevat... | Adobe Analytics... |
|---|---|
| `xdm.web.webPageDetails.name` of `xdm.web.webPageDetails.URL` en no `xdm.web.webInteraction.type` | overweegt lading a **paginamening** |
| `xdm.eventType = web.webpagedetails.pageViews` | overweegt lading a **paginamening** |
| `xdm.web.webInteraction.type` en (`xdm.web.webPageDetails.name` of `xdm.web.webPageDetails.URL`) | overweegt lading a **verbindingsgebeurtenis** <br/> ook reeksen `xdm.web.webPageDetails.name` en `xdm.web.webPageDetails.URL` aan `null` |
| `xdm.web.webInteraction.type` en (`xdm.web.webInteraction.name` of `xdm.web.webInteraction.URL`) | overweegt nuttige lading a **verbindingsgebeurtenis** <br/> ook reeksen `xdm.web.webPageDetails.name` en `xdm.web.webPageDetails.URL` aan `null` indien aanwezig |
| no `xdm.web.webInteraction.type` en no `xdm.web.webPageDetails.name` and no `xdm.web.webPageDetails.URL` | Hiermee wordt de lading verwijderd en worden de gegevens genegeerd |

>[!TIP]
>
>XDM-veldnamen in de payload zijn hoofdlettergevoelig (bijvoorbeeld `webPageDetails.URL` ). Het veld `xdm.eventType` is een tekenreekswaarde met een eigen set geaccepteerde waarden en het omhulsel in deze waarden komt mogelijk niet overeen met XDM-veldnamen. Voor toegelaten waarden, zie het `eventType` gebied in de [ klasse XDM ExperienceEvent ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/experienceevent#eventType).

+++Minimale paginaweergave met `xdm` -velden

```json
{
  "xdm": {
    "web": {
      "webPageDetails": {
        "name": "Example page",
        "URL": "https://example.com/page"
      }
    }
  }
}
```

+++

+++Minimale paginaweergave met `xdm.eventType`

```json
{
  "xdm": {
    "eventType": "web.webpagedetails.pageViews"
  }
}
```

+++

+++Minimale gebeurtenis link met aanbevolen velden

```json
{
  "xdm": {
    "web": {
      "webInteraction": {
        "type": "other",
        "name": "Header nav: Pricing",
        "URL": "https://example.com/pricing"
      }
    }
  }
}
```

+++

## Paginaweergaven en koppelingsgebeurtenissen met het `data` -object

| Laden van gegevensobject bevat... | Adobe Analytics... |
|---|---|
| `data.__adobe.analytics.pageName` of `data.__adobe.analytics.pageURL` en no `data.__adobe.analytics.linkType` | overweegt lading a **paginamening** |
| `data.__adobe.analytics.linkType` en (`data.__adobe.analytics.linkName` of `data.__adobe.analytics.linkURL`) | overweegt lading a **verbindingsgebeurtenis** <br/> ook reeksen `data.__adobe.analytics.pageName` en `data.__adobe.analytics.pageURL` aan `null` |
| no `data.__adobe.analytics.linkType` en no `data.__adobe.analytics.pageName` and no `data.__adobe.analytics.pageURL` | Hiermee wordt de lading verwijderd en worden de gegevens genegeerd |

+++Minimale paginaweergave met `data` -velden

```json
{
  "data": {
    "__adobe": {
      "analytics": {
        "pageName": "Example page",
        "pageURL": "https://example.com/page"
      }
    }
  }
}
```

+++

+++Minimale gebeurtenis link met `data` velden

```json
{
  "data": {
    "__adobe": {
      "analytics": {
        "linkType": "o",
        "linkName": "Header nav: Pricing",
        "linkURL": "https://example.com/pricing"
      }
    }
  }
}
```

+++

>[!NOTE]
>
>Als u zowel een `xdm` -object als een `data` -object in dezelfde payload opneemt, controleert Adobe Analytics beide objecten op de respectievelijke velden.

## A4T- en beslissingsgerelateerde gebeurtenissen

Naast het onderscheiden van paginaweergaven en koppelingsgebeurtenissen, bepaalt de volgende logica of bepaalde beslissingsgebeurtenissen als A4T worden gecategoriseerd of worden verworpen.

| XDM-lading bevat... | Adobe Analytics... |
|---|---|
| `xdm.eventType = decisioning.propositionDisplay` en `xdm._experience.decisioning` | overweegt nuttige lading en **A4T** vraag. |
| `xdm.eventType = decisioning.propositionDisplay` en no `xdm._experience.decisioning` | Hiermee wordt de lading verwijderd en worden de gegevens genegeerd |
| `xdm.eventType = decisioning.propositionInteract` en `xdm._experience.decisioning` en no `xdm.web.webInteraction.type` | overweegt nuttige lading en **A4T** vraag. |
| `xdm.eventType = decisioning.propositionInteract` en no `xdm._experience.decisioning` en no `xdm.web.webInteraction.type` | Hiermee wordt de lading verwijderd en worden de gegevens genegeerd. |
| `xdm.eventType = decisioning.propositionFetch` | Hiermee wordt de lading verwijderd en worden de gegevens genegeerd |

>[!TIP]
>
>De volgende `eventType` -waarden zijn afgekeurd. Deze waarden hebben hetzelfde effect op logica als op de huidige tegenhangers:
>
>* Het gebeurtenistype `display` is vervangen. Gebruik in plaats hiervan `decisioning.propositionDisplay` .
>* Het gebeurtenistype `click` is vervangen. Gebruik in plaats hiervan `decisioning.propositionInteract` .
>* Het gebeurtenistype `personalization.request` is vervangen. Gebruik in plaats hiervan `decisioning.propositionFetch` .

+++Minimale A4T-weergave

```json
{
  "xdm": {
    "eventType": "decisioning.propositionDisplay",
    "_experience": {
      "decisioning": {
        "propositions": [
          {
            "id": "example-proposition-id",
            "scope": "example-scope",
            "scopeDetails": { "decisionProvider": "AJO" }
          }
        ],
        "propositionEventType": { "display": 1 }
      }
    }
  }
}
```

+++

+++Minimale A4T-interactie

```json
{
  "xdm": {
    "eventType": "decisioning.propositionInteract",
    "_experience": {
      "decisioning": {
        "propositions": [
          {
            "id": "example-proposition-id",
            "scope": "example-scope",
            "scopeDetails": { "decisionProvider": "AJO" }
          }
        ],
        "propositionEventType": { "interact": 1 }
      }
    }
  }
}
```

+++

Zie de [ Adobe Analytics ExperienceEvent Volledige groep van het het schemagebied van de Uitbreiding ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/analytics-full-extension) voor meer informatie.
