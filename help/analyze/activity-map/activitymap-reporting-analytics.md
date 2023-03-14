---
description: Beschrijft hoe te om toestemmingen te plaatsen en welke afmetingen in Analytics beschikbaar zijn.
title: Activity Map-rapportage in Analytics
uuid: 057c6ab2-aa06-4779-ac16-f9b367d9ea43
feature: Activity Map
role: User, Admin
exl-id: 8d7be302-bdfc-4370-b8f0-ab1af1e439ca
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 6%

---

# Activity Map-rapportage in Analytics

Beschrijft hoe te om toestemmingen te plaatsen en welke afmetingen in Analytics beschikbaar zijn.

## Machtigingen instellen {#section_BDCD9914B31A4066A50D23DDDF1ABB37}

Voordat gebruikers de afmetingen van de Activity Map kunnen rapporteren, moet u als beheerder

* [Gebruikers toevoegen aan de toegangsgroep Activity Map](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable.md).
* Voeg rapportsuites toe u toegang tot deze groep wilt hebben. Ga naar **[!UICONTROL Admin]** > **[!UICONTROL All admin]** > **[!UICONTROL User management]** > **[!UICONTROL Groups]** > **[!UICONTROL Activity Map Access]** > **[!UICONTROL Edit]**.
* De gebruikerstoegang tot dimensies aanpassen. Zie de onderstaande paragraaf.

## Afmetingen Activity Map analyse {#section_9395A7A5585F4ABE9F7C6CD0124B02A5}

U kunt [gebruikerstoegang aanpassen aan dimensies](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/customize-report-access/groups-dimensions.html) op granulair niveau. Hier volgen de afmetingen voor de Activity Map die beschikbaar zijn in Analytics:

| Dimension | Beschrijving |
|---|---|
| Activity Map-pagina | Hier worden de pagina&#39;s weergegeven waarop op een koppeling is geklikt. |
| Activity Map | Hiermee geeft u alle verzamelde koppelingsgebieden op de hele website weer. Als een gebied op meerdere pagina&#39;s wordt weergegeven, wordt de maateenheid voor alle pagina&#39;s samengevoegd. |
| Koppelingen Activity Mappen | Hiermee geeft u alle verzamelde koppelingen op de hele website weer. |
| Koppelingen en regio Activity Mappen | Hiermee geeft u alle verzamelde koppelingen met hun regio op de hele website weer. |
| Activity Map XY | Ongebruikt |

* Deze afmetingen moeten beschikbaar zijn in Analysis Workspace, Reports &amp; Analytics en Report Builder, op voorwaarde dat uw analytische implementatie [ingeschakeld voor Activity Map](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable.md).
* Navigeer in Rapporten &amp; Analytics naar **[!UICONTROL View All Reports]** > **[!UICONTROL Activity Map]**.

* Als u een koppeling en een gebied voor een specifieke pagina wilt bekijken, hoeft u alleen maar een onderverdeling te maken van de gewenste pagina voor Activity Map naar de Activity Map Koppelingen en regio.
