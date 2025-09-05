---
description: Schakel afmetingen in zodat Activity Map gegevens kan verzamelen.
title: Activity Map Reporting
feature: Admin Tools
exl-id: 9300c12e-3ade-4850-8a22-cba61b35ca67
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Activity Map Reporting

Staat u toe om dimensies voor gebruik met [ Activity Map ](/help/analyze/activity-map/overview.md) toe te laten.

**[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Selecteer een rapportsuite > **[!UICONTROL Edit Settings]** > **[!UICONTROL Activity Map]** > **[!UICONTROL Activity Map Reporting]**

Deze sectie van de documentatie richt zich op het toelaten van dimensies die Activity Map gebruikt. Zie [ overzicht van Activity Map ](/help/analyze/activity-map/overview.md) voor meer informatie over de bekleding, implementatievariabelen, en dimensies.

Wanneer u de knop **[!UICONTROL Enable Activity Map Reports]** selecteert, worden de volgende afmetingen gemaakt:

* [[!UICONTROL Activity Map Link]](/help/components/dimensions/activity-map-link.md): De naam van de koppeling waarop is geklikt.
* [[!UICONTROL Activity Map Region]](/help/components/dimensions/activity-map-region.md): De naam van het gebied waarop is geklikt.
* [[!UICONTROL Activity Map Page]](/help/components/dimensions/activity-map-page.md): De paginanaam op het moment dat op de koppeling werd geklikt.
* [[!UICONTROL Activity Map Link By Region]](/help/components/dimensions/activity-map-link-by-region.md): Een samengevoegde waarde van Activity Map Link en Activity Map Region.

Zodra toegelaten, kan uw implementatie beginnen gegevens naar deze dimensies voor gebruik in [ Analysis Workspace ](/help/analyze/analysis-workspace/home.md) en [ Browser uitbreidingsbekleding ](/help/analyze/activity-map/overlay/overview.md) te verzenden.

>[!NOTE]
>
>Als u Activity Map inschakelt voor een rapportsuite, wordt deze permanent ingeschakeld zonder dat dit in de toekomst wordt uitgeschakeld.
