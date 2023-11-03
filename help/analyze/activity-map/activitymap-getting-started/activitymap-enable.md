---
description: Verklaart de stappen de Admin van Analytics moet voltooien om de inzameling van de verbindingsverbinding van de Activity Map en gebruikersdownload toe te laten.
title: Activity Map inschakelen
feature: Activity Map
role: Admin
exl-id: 0b2b9f3d-0c75-4eb8-9235-c9c98eb035d3
mini-toc-levels: 3
source-git-commit: bb9ba0400116aff3aea5307c48c6ac560603995e
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 1%

---


# Activity Map activeren en inschakelen

Verklaart de stappen de Admin van Analytics moet voltooien om de inzameling van de verbindingsverbinding van de Activity Map en gebruikersdownload toe te laten.

## Stap 1. Activity Map activeren {#update_code}

De module van de Activity Map maakt deel uit van AppMeasurement.js, de markeringen van Adobe Experience Platform, en het Web SDK (alloy.js). Gegevens over Activity Mappen kunnen alleen worden verzameld als u de update naar **Web SDK versie 2.15.0** of hoger, **Adobe Analytics-tagextensie v1.90** of hoger, **AppMeasurement versie 1.6** of hoger.

+++Web SDK (extensie Tags)

Navigeer in Adobe Experience Platform-tags naar de eigenschap waarvoor u Analytics implementeert. Onder [!UICONTROL Extensions] -> [!UICONTROL Adobe Experience Platform Web SDK], selecteert u **[!UICONTROL Enable click data collection]** zoals hieronder gemarkeerd. Vervolgens maakt u de bibliotheek met de wijzigingen en publiceert u de bibliotheek naar de productie.

![](assets/web_sdk.png)

+++

+++Handmatige Web SDK-implementatie

Zie [Koppelingen bijhouden](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/track-links.html) voor informatie over hoe te om verbinding het volgen uit te voeren en hoe te om Activiteitstoewijzing toe te laten door het vangen van `region` van het aangeklikte HTML-element.

>[!NOTE]
>
>Het toelaten van verbinding het volgen met Web SDK verzendt momenteel verbindingsgebeurtenissen wanneer een klant van één pagina aan volgende navigeert. Dit is anders dan hoe AppMeasurement werkt en kan mogelijk leiden tot extra factureerbare hits die naar de Adobe worden verzonden.

+++

+++extensie Analytics (Adobe Experience Platform-tags)

Navigeer in Adobe Experience Platform-tags naar de eigenschap waarvoor u Analytics implementeert. In de [!UICONTROL Install Extension] dialoogvenster, selecteren **[!UICONTROL Use Activity Map]**.

![](assets/aa_extension.png)

+++

+++AppMeasurement

Download de nieuwste JavaScript-bibliotheek, afhankelijk van het feit of u AppMeasurement of Web SDK gebruikt.
Ga naar **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL All admin]** > **[!UICONTROL Code manager]** en [uitvoeren](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html).

+++

## Stap 2. Rapporten Activity Map inschakelen {#enable}

Eerst, moet u Activity Map rapporten op het rapport-reeks niveau toelaten.

1. Meld u aan bij Adobe Analytics en ga naar  **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Selecteer een rapportsuite > **[!UICONTROL Edit Settings]** > **[!UICONTROL Activity Map]** > **[!UICONTROL Activity Map Reporting]** .

1. De Activity Map verzamelt de verbindingsgegevens in de rapporten van de Activity Map. Voor activering moet u eerst de variabelen activeren door op **[!UICONTROL Enable Activity Map Reports]**.

   Met deze stap voegt u alle analytische afmetingen toe die u nodig hebt om gegevens te verzamelen.

   ![](assets/enable.png)

1. Controleer na ongeveer een uur de instelling [Rapport Activity Map pagina](/help/analyze/activity-map/activitymap-reporting-analytics.md), waarin alle pagina&#39;s worden weergegeven waarop gebruikers op een koppeling hebben geklikt.

## Stap 3. Gebruikers toevoegen aan [!UICONTROL Activity Map Access] productprofiel {#add_users}

1. Klik op **[!UICONTROL Add Users to Group]**.

   Hiermee gaat u naar de pagina met productprofielen in het dialoogvenster [Adobe Admin Console](https://adminconsole.adobe.com/E2F05B3B52F54D2E0A490D44@AdobeOrg/overview).

1. Als u geen [!UICONTROL Activity Map Access] productprofiel, doe dit nu. De voor dit profiel vereiste machtigingsitems zijn [!UICONTROL Analytics Tools] > [!UICONTROL Activity Map] en [!UICONTROL Analytics Tools] > [!UICONTROL Segment Publishing].

1. Voeg gebruikers toe aan dat productprofiel. Hierdoor kunnen uw gebruikers Activity Map downloaden van  **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Tools]** > **[!UICONTROL ActivityMap]** .

