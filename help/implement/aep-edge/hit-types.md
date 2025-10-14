---
title: Edge Network-gebeurtenistypen in Adobe Analytics
description: Hoe Adobe Analytics gebeurtenissen interpreteert die van de Edge Network zijn ontvangen.
feature: Implementation Basics
role: Admin, Developer
exl-id: 31085025-9c38-4375-8dfb-4fded6542ca7
source-git-commit: 6e500007e10086c0ff8108856a3563d7702f1130
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# Edge Network-gebeurtenistypen in Adobe Analytics

Adobe Analytics behandelt treffers verschillend afhankelijk van welke functies u in AppMeasurement roept. [`s.t`](/help/implement/vars/functions/t-method.md) en [`s.tl`](/help/implement/vars/functions/tl-method.md) bevatten bijvoorbeeld of laten bepaalde afmetingen en de paginaweergave verhogen anders. Adobe Experience Platform bevat alleen de opdracht `sendEvent` . Specifieke eigenschappen in de `xdm` -laadbewerking bepalen hoe die gegevens in Adobe Analytics worden geïnterpreteerd.

De Edge Network gebruikt de volgende logica om Adobe Analytics-paginaweergaven en -koppelingsgebeurtenissen te bepalen:

| XDM-lading bevat... | Adobe Analytics... |
|---|---|
| `xdm.web.webPageDetails.name` of `xdm.web.webPageDetails.URL` en no `xdm.web.webInteraction.type` | overweegt lading a **paginamening** |
| `xdm.eventType = web.webPageDetails.pageViews` | overweegt lading a **paginamening** |
| `xdm.web.webInteraction.type` en (`xdm.web.webPageDetails.name` of `xdm.web.webPageDetails.url`) | overweegt lading a **verbindingsgebeurtenis** <br/> ook reeksen `xdm.web.webPageDetails.name` en `xdm.web.webPageDetails.URL` aan `null` |
| no `xdm.web.webInteraction.type` en no `xdm.webPageDetails.name` and no `xdm.web.webPageDetails.URL` | Hiermee wordt de lading verwijderd en worden de gegevens genegeerd |

| Laden van gegevensobject bevat... | Adobe Analytics... |
|---|---|
| `data.__adobe.analytics.pageName` of `data.__adobe.analytics.pageURL` en no `data.__adobe.analytics.linkType` | overweegt lading a **paginamening** |
| `data.__adobe.analytics.linkType` en (`data.__adobe.analytics.linkName` of `data.__adobe.analytics.linkURL`) | overweegt lading a **verbindingsgebeurtenis** <br/> ook reeksen `data.__adobe.analytics.pageName` en `data.__adobe.analytics.pageURL` aan `null` |
| no `data.__adobe.analytics.linkType` en no `data.__adobe.analytics.pageName` and no `data.__adobe.analytics.pageURL` | Hiermee wordt de lading verwijderd en worden de gegevens genegeerd |

>[!NOTE]
>
>Als u zowel een `xdm` -object als een `data` -object in dezelfde payload opneemt, controleert Adobe Analytics beide objecten op de respectievelijke velden.

Naast het onderscheiden van paginaweergaven en het klikken van koppelingen, is de volgende logica op zijn plaats die bepaalt als bepaalde gebeurtenissen als A4T worden gecategoriseerd of worden verworpen.

| XDM-lading bevat... | Adobe Analytics... |
|---|---|
| `xdm.eventType = display` of <br/>`xdm.eventType = decisioning.propositionDisplay` of <br/>`xdm.eventType = personalization.request` of <br/>`xdm.eventType = decisioning.propositionFetch` en `xdm._experience.decisioning` | overweegt nuttige lading en **A4T** vraag. |
| `xdm.eventType = display` of <br/>`xdm.eventType = decisioning.propositionDisplay` of <br/>`xdm.eventType = personalization.request` of <br/>`xdm.eventType = decisioning.propositionFetch` en geen `xdm._experience.decisioning` | Hiermee wordt de lading verwijderd en worden de gegevens genegeerd |
| `xdm.eventType = click` of `xdm.eventType = decisioning.propositionInteract` and `xdm._experience.decisioning` en no `web.webInteraction.type` | overweegt nuttige lading en **A4T** vraag. |
| `xdm.eventType = click` of `xdm.eventType = decisioning.propositionInteract` en no `xdm._experience.decisioning` en no `web.webInteraction.type` | Hiermee wordt de lading verwijderd en worden de gegevens genegeerd. |

Zie de [&#x200B; Adobe Analytics ExperienceEvent Volledige groep van het het schemagebied van de Uitbreiding &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/field-groups/event/analytics-full-extension) voor meer informatie.
