---
title: Adobe Analytics implementeren met Adobe Experience Platform Edge
description: Overzicht van het gebruik van XDM-gegevens van Experience Platform in Adobe Analytics
exl-id: 7d8de761-86e3-499a-932c-eb27edd5f1a3
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: 914b822aae659d1d0f0b8a98480090ead99e102a
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---

# Adobe Analytics implementeren met het Adobe Experience Platform Edge Network

Met het Adobe Experience Platform Edge-netwerk kunt u gegevens die bestemd zijn voor meerdere producten naar een gecentraliseerde locatie verzenden. Het netwerk van de Rand door:sturen de aangewezen informatie aan de gewenste producten. Met dit concept kunt u de implementatie-inspanningen consolideren, met name voor het overspannen van meerdere gegevensoplossingen.

De Adobe biedt drie belangrijke manieren om gegevens naar het Netwerk van de Rand te verzenden:

* **[Adobe Experience Platform Web SDK](web-sdk/overview.md)**: Gebruik de extensie Web SDK in Adobe Experience Platform Data Collection om gegevens naar Edge te verzenden.
* **[Adobe Experience Platform Mobile SDK](mobile-sdk/overview.md)**: Gebruik de extensie Mobile SDK in Adobe Experience Platform Data Collection om gegevens naar Edge te verzenden.
* **[Adobe Experience Platform Edge Network Server-API](server-api/overview.md)**: Gegevens rechtstreeks naar Edge verzenden met een API.



## Hoe Adobe Analytics Edge Network-gegevens verwerkt

Gegevens die naar het Adobe Experience Platform Edge-netwerk worden verzonden, kunnen in twee indelingen worden opgemaakt:

* XDM-object: conform schema&#39;s op basis van [XDM (Experience Data Model)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl). XDM biedt u flexibiliteit in welke velden worden gedefinieerd als onderdeel van gebeurtenissen. Op het moment dat de gebeurtenissen Adobe Analytics bereiken, worden ze vertaald in een indeling die Adobe Analytics kan verwerken.
* Gegevensobject: gegevens naar het Edge-netwerk verzenden met specifieke velden die zijn toegewezen aan Adobe Analytics. Het netwerk van de Rand ontdekt de aanwezigheid van deze gebieden en door:sturen hen aan Adobe Analytics zonder de behoefte om met een schema in overeenstemming te zijn.


Edge Network gebruikt de volgende logica om paginaweergaven en koppelingsgebeurtenissen van Adobe Analytics te bepalen

| XDM-lading bevat... | Adobe Analytics... |
|---|---|
| `web.webPageDetails.name` of `web.webPageDetails.URL` en nee `web.webInteraction.type` | beschouwt lading als **paginaweergave** |
| `web.webInteraction.type` en (`web.webInteraction.name` of `web.webInteraction.url`) | beschouwt lading als **link, gebeurtenis** |
| `web.webInteraction.type` en (`web.webPageDetails.name` of `web.webPageDetails.url`) | beschouwt lading als **link, gebeurtenis** <br/>`web.webPageDetails.name` en `web.webPageDetails.URL` zijn ingesteld op `null` |
| nee `web.webInteraction.type` en (geen `webPageDetails.name` en nee `web.webPageDetails.URL`) | Hiermee wordt de lading verwijderd en worden de gegevens genegeerd |

{style="table-layout:auto"}

Zie de [Adobe Analytics ExperienceEvent Volledige extensieschema, veldgroep](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/event/analytics-full-extension.html) voor meer informatie .
