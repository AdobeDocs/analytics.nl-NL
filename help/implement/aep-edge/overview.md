---
title: Adobe Analytics implementeren met Adobe Experience Platform Edge
description: Overzicht van het gebruik van XDM-gegevens van Experience Platform in Adobe Analytics
exl-id: 7d8de761-86e3-499a-932c-eb27edd5f1a3
feature: Implementation Basics
source-git-commit: e0f08e6e53b6d7001bd1163a65facda8e21c91fd
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 3%

---

# Adobe Analytics implementeren met Adobe Experience Platform Edge

Met Adobe Experience Platform Edge kunt u gegevens die bestemd zijn voor meerdere producten naar een gecentraliseerde locatie verzenden. De ervaring Edge stuurt de juiste informatie door naar de gewenste producten. Met dit concept kunt u de implementatie-inspanningen consolideren, met name voor het overspannen van meerdere gegevensoplossingen.

Adobe biedt drie manieren om gegevens naar Experience Edge te verzenden:

* **[Adobe Experience Platform Web SDK](web-sdk/overview.md)**: Gebruik de extensie Web SDK in Adobe Experience Platform Data Collection om gegevens naar Edge te verzenden.
* **[Adobe Experience Platform Mobile SDK](mobile-sdk/overview.md)**: Gebruik de extensie Mobile SDK in Adobe Experience Platform Data Collection om gegevens naar Edge te verzenden.
* **[Adobe Experience Platform Edge Network Server-API](server-api/overview.md)**: Gegevens rechtstreeks naar Edge verzenden met een API.



## Hoe Adobe Analytics omgaat met Edge-gegevens

Gegevens die naar Experience Edge worden verzonden, moeten in overeenstemming zijn met schema&#39;s op basis van [XDM (Experience Data Model)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl). XDM biedt u flexibiliteit in welke velden worden gedefinieerd als onderdeel van gebeurtenissen. Wanneer de gebeurtenissen Adobe Analytics bereiken, worden deze gebeurtenissen vertaald in meer gestructureerde gegevens die Adobe Analytics kan verwerken: paginaweergaven of koppelingsgebeurtenissen.

XDM schrijft zelf niet voor hoe paginaweergaven of koppelingsgebeurtenissen moeten worden gedefinieerd en geeft Adobe Analytics ook niet de opdracht hoe de lading moet worden verwerkt. Bepaalde XDM-velden in het vak die bijvoorbeeld gerelateerd lijken te zijn aan paginaweergaven of koppelingsgebeurtenissen, zoals `eventType`, `web.webPageDetails.pageViews`, of `web.webInteraction.linkEvents` zijn volledig onduidelijk ten uitvoer gelegd en zijn niet relevant voor Adobe Analytics.

Om paginameningen en verbindingsgebeurtenissen behoorlijk te behandelen, wordt de volgende logica toegepast op gegevens die naar het netwerk van de Rand van de Ervaring van de Adobe worden verzonden en door:sturen aan Adobe Analytics.

| XDM-lading bevat... | Adobe Analytics... |
|---|---|
| `web.webPageDetails.name` of `web.webPageDetails.URL` en nee `web.webInteraction.type` | beschouwt lading als **paginaweergave** |
| `web.webInteraction.type` en (`web.webInteraction.name` of `web.webInteraction.url`) | beschouwt lading als **link, gebeurtenis** |
| `web.webInteraction.type` en (`web.webPageDetails.name` of `web.webPageDetails.url`) | beschouwt lading als **link, gebeurtenis** <br/>`web.webPageDetails.name` en `web.webPageDetails.URL` zijn ingesteld op `null` |
| nee `web.webInteraction.type` en (geen `webPageDetails.name` en nee `web.webPageDetails.URL`) | Hiermee wordt de lading verwijderd en worden de gegevens genegeerd |

{style="table-layout:auto"}

