---
title: Afmetingen van mobiele levenscyclus
description: Dimensionen op basis van gegevens die zijn verzameld met de Mobile SDK.
feature: Dimensions
exl-id: b7ba45d7-7d30-48a3-a747-ea9fbb253abb
source-git-commit: d940428e1cbe1be6d8263e986e8b641ec18aace1
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 1%

---

# Afmetingen van mobiele levenscyclus

*Deze paginareferentiegegevens worden doorgaans bijgehouden via de Adobe Experience Platform Mobile SDK. Zie voor informatie over mobiele apparaten met gebruikersagent [Afmetingen van mobiele opzoekopdrachten](mobile-dimensions.md). Voor metriek die gebruikend Mobile SDK wordt gevolgd, zie [Metingen over mobiele levenscyclus](../metrics/lifecycle-metrics.md).*

| Naam levenscyclusdimensie | Beschrijving | Variabele van contextgegevens |
| --- | --- | --- |
| [!UICONTROL First Launch Date] | | TBD |
| [!UICONTROL Device Name (SDK)] | | `a.DeviceName` |
| [!UICONTROL Operating System Version (SDK)] | | `a.OSVersion` |
| [!UICONTROL Resolution (SDK)] | | `a.Resolution` |
| [!UICONTROL Acquisition Source] | | `a.referrer.campaign.source` |
| [!UICONTROL App Id] | | `a.AppID` |
| [!UICONTROL Acquisition Medium] | | `a.referrer.campaign.medium` |
| [!UICONTROL Acquisition Term] | | `a.referrer.campaign.term` |
| [!UICONTROL Acquisition Content] | | `a.refferer.campaign.content` |
| [!UICONTROL Acquisition Name] | | `a.referrer.campaign.name` |
| [!UICONTROL Location (down to 10 km)] | | `a.loc.lat.a` + `a.loc.lon.a` |
| [!UICONTROL Location (down to 100 m)] | | `a.loc.lat.b` + `a.loc.lon.b` |
| [!UICONTROL Location (down to 1 m)] | | `a.loc.lat.c` + `a.loc.lon.c` |
| [!UICONTROL Point of Interest Name] | | `a.loc.poi` |
| [!UICONTROL Distance to Point of Interest Center] | | `a.loc.dist` |
| [!UICONTROL Launch Number] | | `a.Launches` |
| [!UICONTROL Days Since First Use] | | `a.DaysSinceFirstUse` |
| [!UICONTROL Action Name] | | TBD |
| [!UICONTROL Lifetime Value (evar)] | | `a.ltv.amount` |
| [!UICONTROL Beacon Major] | | TBD |
| [!UICONTROL Beacon Minor] | | TBD |
| [!UICONTROL Beacon UUID] | | TBD |
| [!UICONTROL Beacon Proximity] | | TBD |
| [!UICONTROL Days Since Last Use] | | `a.DaysSinceFirstUse` |
| [!UICONTROL Hour of Day (SDK)] | | `a.HourOfDay` |
| [!UICONTROL Day of Week (SDK)] | | `a.DayOfWeek` |
| [!UICONTROL Point of Interest ID] | | TBD |

{style="table-layout:auto"}

<!-- Missing: Install Date -->
