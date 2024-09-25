---
title: Adobe Analytics implementeren met Adobe Experience Platform Edge
description: Overzicht van het gebruik van XDM-gegevens van Experience Platform in Adobe Analytics
exl-id: 7d8de761-86e3-499a-932c-eb27edd5f1a3
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: 4453c2aa2ea70ef4d00b2bc657285287f3250c65
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---

# Adobe Analytics implementeren met de Adobe Experience Platform Edge Network

Met de Adobe Experience Platform-Edge Network kunt u gegevens die bestemd zijn voor meerdere producten naar een gecentraliseerde locatie verzenden. De Edge Network geeft de juiste informatie door aan de gewenste producten. Met dit concept kunt u de implementatie-inspanningen consolideren, met name voor het overspannen van meerdere gegevensoplossingen.

Adobe biedt drie manieren om gegevens naar de Edge Network te verzenden:

* **[SDK van het Web van Adobe Experience Platform](web-sdk/overview.md)**: Gebruik de uitbreiding van SDK van het Web in de Inzameling van Gegevens van Adobe Experience Platform om gegevens naar Edge te verzenden.
* **[Adobe Experience Platform Mobile SDK](mobile-sdk/overview.md)**: Gebruik de Mobiele uitbreiding van SDK in de Inzameling van Gegevens van Adobe Experience Platform om gegevens naar Edge te verzenden.
* **[de Server API van de Edge Network van Adobe Experience Platform](server-api/overview.md)**: Verzend gegevens rechtstreeks naar Edge gebruikend API.



## Hoe Adobe Analytics omgaat met Edge Network-gegevens

Gegevens die naar de Adobe Experience Platform-Edge Network worden verzonden, kunnen in twee indelingen worden opgeslagen:

* XDM voorwerp: Vorm aan schema&#39;s die op [ worden gebaseerd XDM (het Model van Gegevens van de Ervaring) ](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl). XDM biedt u flexibiliteit in welke velden worden gedefinieerd als onderdeel van gebeurtenissen. Op het moment dat de gebeurtenissen Adobe Analytics bereiken, worden ze vertaald in een indeling die Adobe Analytics kan verwerken.
* Gegevensobject: gegevens naar de Edge Network verzenden met specifieke velden die zijn toegewezen aan Adobe Analytics. De Edge Network ontdekt de aanwezigheid van deze gebieden en door:sturen hen aan Adobe Analytics zonder de behoefte om aan een schema in overeenstemming te zijn.

De Edge Network gebruikt de volgende logica om Adobe Analytics paginaweergaven en koppelingsgebeurtenissen te bepalen:

| XDM-lading bevat... | Adobe Analytics... |
|---|---|
| `xdm.web.webPageDetails.name` of `xdm.web.webPageDetails.URL` en no `xdm.web.webInteraction.type` | overweegt lading a **paginamening** |
| `xdm.web.webInteraction.type` en (`xdm.web.webInteraction.name` of `xdm.web.webInteraction.url`) | overweegt lading a **verbindingsgebeurtenis** |
| `web.webInteraction.type` en (`web.webPageDetails.name` of `web.webPageDetails.url`) | overweegt lading a **verbindingsgebeurtenis** <br/>`web.webPageDetails.name` en `web.webPageDetails.URL` wordt geplaatst aan `null` |
| no `web.webInteraction.type` en (no `webPageDetails.name` en no `web.webPageDetails.URL` ) | Hiermee wordt de lading verwijderd en worden de gegevens genegeerd |
| `xdm.eventType = display` of <br/>`xdm.eventType = decisioning.propositionDisplay` of <br/>`xdm.eventType = personalization.request` of <br/>`xdm.eventType = decisioning.propositionFetch` en `xdm._experience.decisioning` | overweegt nuttige lading en **A4T** vraag. |
| `xdm.eventType = display` of <br/>`xdm.eventType = decisioning.propositionDisplay` of <br/>`xdm.eventType = personalization.request` of <br/>`xdm.eventType = decisioning.propositionFetch` en geen `xdm._experience.decisioning` | Hiermee wordt de lading verwijderd en worden de gegevens genegeerd |
| `xdm.eventType = click` of `xdm.eventType = decisioning.propositionInteract` and `xdm._experience.decisioning` en no `web.webInteraction.type` | overweegt nuttige lading en **A4T** vraag. |
| `xdm.eventType = click` of `xdm.eventType = decisioning.propositionInteract` en no `xdm._experience.decisioning` en no `web.webInteraction.type` | Hiermee wordt de lading verwijderd en worden de gegevens genegeerd. |

{style="table-layout:auto"}

Zie de [ Adobe Analytics ExperienceEvent Volledige groep van het het schemagebied van de Uitbreiding ](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/event/analytics-full-extension.html) voor meer informatie.
