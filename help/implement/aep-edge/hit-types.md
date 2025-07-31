---
title: Edge Network-gebeurtenistypen in Adobe Analytics
description: Hoe Adobe Analytics gebeurtenissen interpreteert die van de Edge Network zijn ontvangen.
feature: Implementation Basics
role: Admin, Developer
source-git-commit: 8d369bd3be3ae9c075e490e108666728a2cff5dc
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# Edge Network-gebeurtenistypen in Adobe Analytics

Adobe Analytics behandelt treffers verschillend afhankelijk van welke functies u in AppMeasurement roept. [`s.t`](/help/implement/vars/functions/t-method.md) en [`s.tl`](/help/implement/vars/functions/tl-method.md) bevatten bijvoorbeeld of laten bepaalde afmetingen en de paginaweergave verhogen anders. Adobe Experience Platform bevat alleen de opdracht `sendEvent` . Specifieke eigenschappen in de `xdm` -laadbewerking bepalen hoe die gegevens in Adobe Analytics worden geïnterpreteerd.

De Edge Network gebruikt de volgende logica om Adobe Analytics-paginaweergaven en -koppelingsgebeurtenissen te bepalen:

| XDM-lading bevat... | Adobe Analytics... |
|---|---|
| `xdm.web.webPageDetails.name` of `xdm.web.webPageDetails.URL` en no `xdm.web.webInteraction.type` | overweegt lading a **paginamening** |
| `xdm.eventType = web.webPageDetails.pageViews` | overweegt lading a **paginamening** |
| `xdm.web.webInteraction.type` en (`xdm.web.webInteraction.name` of `xdm.web.webInteraction.url`) | overweegt lading a **verbindingsgebeurtenis** |
| `xdm.web.webInteraction.type` en (`xdm.web.webPageDetails.name` of `xdm.web.webPageDetails.url`) | overweegt lading a **verbindingsgebeurtenis** <br/> ook reeksen `xdm.web.webPageDetails.name` en `xdm.web.webPageDetails.URL` aan `null` |
| no `xdm.web.webInteraction.type` en (no `xdm.webPageDetails.name` en no `xdm.web.webPageDetails.URL` ) | Hiermee wordt de lading verwijderd en worden de gegevens genegeerd |

Naast het onderscheiden van paginaweergaven en het klikken van koppelingen, is de volgende logica op zijn plaats die bepaalt als bepaalde gebeurtenissen als A4T worden gecategoriseerd of worden verworpen.

| XDM-lading bevat... | Adobe Analytics... |
| --- | --- |
| `xdm.eventType = display` of <br/>`xdm.eventType = decisioning.propositionDisplay` of <br/>`xdm.eventType = personalization.request` of <br/>`xdm.eventType = decisioning.propositionFetch` en `xdm._experience.decisioning` | overweegt nuttige lading en **A4T** vraag. |
| `xdm.eventType = display` of <br/>`xdm.eventType = decisioning.propositionDisplay` of <br/>`xdm.eventType = personalization.request` of <br/>`xdm.eventType = decisioning.propositionFetch` en geen `xdm._experience.decisioning` | Hiermee wordt de lading verwijderd en worden de gegevens genegeerd |
| `xdm.eventType = click` of `xdm.eventType = decisioning.propositionInteract` and `xdm._experience.decisioning` en no `web.webInteraction.type` | overweegt nuttige lading en **A4T** vraag. |
| `xdm.eventType = click` of `xdm.eventType = decisioning.propositionInteract` en no `xdm._experience.decisioning` en no `web.webInteraction.type` | Hiermee wordt de lading verwijderd en worden de gegevens genegeerd. |

Zie de [ Adobe Analytics ExperienceEvent Volledige groep van het het schemagebied van de Uitbreiding ](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/field-groups/event/analytics-full-extension) voor meer informatie.
