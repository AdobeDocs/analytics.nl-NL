---
description: Verklaart de stappen de Admin van Analytics moet voltooien om de inzameling van de verbindingsverbinding van de Activity Map en gebruikersdownload toe te laten.
title: Activity Map inschakelen
uuid: 30433319-d0e6-4977-951a-4492b356e1f2
feature: Activity Map
role: User, Admin
exl-id: 0b2b9f3d-0c75-4eb8-9235-c9c98eb035d3
source-git-commit: d4caf0ddc5cf5402bfef94a64db1c00e1c725658
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 3%

---

# Activity Map inschakelen{#enable-activity-map}

Verklaart de stappen de Admin van Analytics moet voltooien om de inzameling van de verbindingsverbinding van de Activity Map en gebruikersdownload toe te laten.

## Stap 1. Implementatiecode bijwerken {#section_5D1586289DF2489289B1B6C1C80C300D}

De module van de Activity Map maakt deel uit van AppMeasurement.js en het Web SDK (versie 2.15.0 of hoger).
De bibliotheek van het AppMeasurement of SDK van het Web zal de module van de Activity Map wanneer geconcretiseerd laden.

>[!NOTE]
>
>Gegevens over Activity Mappen kunnen alleen worden verzameld als u de update naar **AppMeasurement** **versie 1.6** of hoger of **Web SDK** **versie 2.15.0** of hoger.


1. Download de nieuwste JavaScript-bibliotheek, afhankelijk van het feit of u AppMeasurement of Web SDK gebruikt.

   - **AppMeasurement** code (AppMeasurement_Javascript-1.6.zip) door naar  **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL All admin]** > **[!UICONTROL Code manager]** en [uitvoeren](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html).

     We hebben een aantal [voorbeeldimplementatiecode](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-sample-implementation-code.md) om u te helpen de veranderingen visualiseren die aan de code door de module van de Activity Map te omvatten zijn aangebracht.

   - **Web SDK** code (alloy.js). Zie [SDK installeren - optie 2: de vooraf gebouwde zelfstandige versie installeren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en#option-2%3A-installing-the-prebuilt-standalone-version) voor meer informatie . Gebruik versie 2.15 of hoger.

     Zie [Koppelingen bijhouden](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/track-links.html) voor informatie over hoe te om verbinding het volgen uit te voeren en hoe te om Activiteitstoewijzing toe te laten door het vangen van `region` van het aangeklikte HTML-element.

     >[!NOTE]
     >
     >Het toelaten van verbinding het volgen met Web SDK verzendt momenteel verbindingsgebeurtenissen wanneer een klant van één pagina aan volgende navigeert. Dit is anders dan hoe AppMeasurement werkt en kan mogelijk leiden tot extra factureerbare hits die naar de Adobe worden verzonden.


1. De implementatie valideren:

   1. Wanneer op een klikbaar element wordt geklikt, worden de gegevens opgeslagen in een cookie met de naam s_sq.
   1. De gegevens van de Activity Map kunnen in het vraag-koord op de volgende vraag worden gezien. Bijvoorbeeld:

      ```
      …&c.&a.&Activity Map.&link=My%20Link&region=My%20Region&page=My%20Page&.Activity Map&.a&.c&...
      ```

1. Dit rapport onderbreken met **[!UICONTROL Activity Map Link by Region]** om de koppeling/regio voor die pagina weer te geven:  ![](assets/am_breakdown.png){width="400px"}

## Stap 2. Rapporten Activity Map inschakelen {#section_D14F15D2FC0346FCAD8B3B87E6DD33D4}

Eerst, moet u Activity Map rapporten op een rapport-reeks niveau toelaten.

1. Meld u aan bij Adobe Analytics en ga naar  **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Selecteer een rapportsuite > **[!UICONTROL Edit Settings]** > **[!UICONTROL Activity Map]** > **[!UICONTROL Activity Map Reporting]** .
1. De Activity Map verzamelt de verbindingsgegevens in de rapporten van de Activity Map. Voor activering moet u eerst de variabelen activeren door op **[!UICONTROL Enable Activity Map Reports]**.

   Met deze stap voegt u alle analytische afmetingen toe die u nodig hebt om gegevens te verzamelen.

1. Controleer na ongeveer een uur de instelling [Rapport Activity Map pagina](/help/analyze/activity-map/activitymap-reporting-analytics.md), waarin alle pagina&#39;s worden weergegeven waarop gebruikers op een koppeling hebben geklikt.

## Stap 3. Gebruikers toevoegen aan de toegangsgroep Activity Map {#section_4C7A47BB7DEF4AFFBC276392467F9675}

1. Klik op **[!UICONTROL Add Users to Group]**.

   Hiermee gaat u naar de pagina voor groepsbeheer in de Admin Console.

1. [Gebruikers aan deze groep toevoegen](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/user-groups/groups.html) en **[!UICONTROL Save Group]**.

1. Hierdoor kunnen uw Admin-gebruikers Activity Map downloaden van  **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Tools]** > **[!UICONTROL ActivityMap]** .

>[!NOTE]
>
>Als u wilt dat gebruikers die geen beheerder zijn, Activity Map downloaden, maakt u een nieuwe gebruikersgroep met de machtiging &#39;Gereedschappen&#39; en &#39;Oudere installatie van ClickMap&#39;. Dit machtigingsniveau in combinatie met de Activity Map Access biedt machtigingen om het gereedschap te downloaden en gebruiken.
