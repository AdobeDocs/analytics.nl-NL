---
description: Beschrijft hoe te om toestemmingen te plaatsen en welke afmetingen in Analytics beschikbaar zijn.
title: Rapportage van Activity Mappen in Analytics
feature: Activity Map
role: User, Admin
exl-id: 8d7be302-bdfc-4370-b8f0-ab1af1e439ca
source-git-commit: a979fc8787fa96f8fa8317996ac66341a6f54354
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 1%

---

# Rapportage van Activity Mappen in Analytics

Beschrijft hoe te om toestemmingen te plaatsen en welke afmetingen in Analytics beschikbaar zijn.

## Machtigingen instellen {#permissions}

Voordat gebruikers de afmetingen van de Activity Map kunnen rapporteren, moet u als beheerder

* [Gebruikers toevoegen aan het productprofiel voor toegang tot Activity Map](/help/analyze/activity-map/activitymap-getting-started/activitymap-enable.md).
* De gebruikerstoegang tot dimensies aanpassen. Zie de onderstaande paragraaf.

## Afmetingen Activity Map analyse {#dimensions}

U kunt [gebruikerstoegang aanpassen aan dimensies](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/customize-report-access/groups-dimensions.html) op granulair niveau. Hier volgen de Activity Mappen die beschikbaar zijn in Analytics:

| Dimension | Beschrijving |
|---|---|
| Activity Map-pagina | Hier worden de pagina&#39;s weergegeven waarop op een koppeling is geklikt. |
| Activity Map | Hiermee geeft u alle verzamelde koppelingsgebieden op de hele website weer. Als een gebied op meerdere pagina&#39;s wordt weergegeven, wordt de maateenheid voor alle pagina&#39;s samengevoegd. |
| Koppelingen Activity Mappen | Hiermee geeft u alle verzamelde koppelingen op de hele website weer. |
| Koppelingen en regio Activity Mappen | Hiermee geeft u alle verzamelde koppelingen met hun regio op de hele website weer. |
| Activity Map XY | Ongebruikt |

* Deze afmetingen moeten beschikbaar zijn in Analysis Workspace en Report Builder, op voorwaarde dat uw analytische implementatie [ingeschakeld voor Activity Map](/help/analyze/activity-map/activitymap-getting-started/activitymap-enable.md).
* In Analysis Workspace, trek de Activiteitenkaart-verwante dimensies in een rapport.
* Als u een koppeling en een gebied voor een specifieke pagina wilt bekijken, hoeft u alleen maar een onderverdeling te maken van de gewenste pagina voor Activity Map naar de Activity Map Koppelingen en regio.
