---
description: Verklaart de stappen de Admin van Analytics moet voltooien om de inzameling van de verbindingsverbinding van de Activity Map en gebruikersdownload toe te laten.
title: Activity Map inschakelen
uuid: 30433319-d0e6-4977-951a-4492b356e1f2
feature: Activity Map
role: User, Admin
exl-id: 0b2b9f3d-0c75-4eb8-9235-c9c98eb035d3
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 4%

---

# Activity Map inschakelen{#enable-activity-map}

Verklaart de stappen de Admin van Analytics moet voltooien om de inzameling van de verbindingsverbinding van de Activity Map en gebruikersdownload toe te laten.

## Stap 1. Werk uw Javascript-code (AppMeasurement) bij naar v1.6 (of hoger) {#section_5D1586289DF2489289B1B6C1C80C300D}

De module Activity Map maakt deel uit van het bestand AppMeasurement.js (dat zich boven aan het bestand bevindt). De bibliotheek AppMeasurement zal de module van de Activity Map wanneer geconcretiseerd laden.

U kunt geen gegevens over de Activity Map verzamelen, tenzij u deze versie (of hoger) van AppMeasurement bijwerkt.

1. Download de nieuwste AppMeasurement-code (AppMeasurement_Javascript-1.6.zip) door naar  **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL All admin]** > **[!UICONTROL Code manager]** en [uitvoeren](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html).

   We hebben een aantal [voorbeeldimplementatiecode](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-sample-implementation-code.md) om u te helpen de veranderingen visualiseren die aan de code door de module van de Activity Map te omvatten zijn aangebracht.

1. De implementatie valideren:

   1. Wanneer op een klikbaar element wordt geklikt, worden de gegevens opgeslagen in een cookie met de naam s_sq.
   1. De gegevens van de Activity Map kunnen in het vraag-koord op de volgende vraag worden gezien. Bijvoorbeeld:

      ```
      …&c.&a.&Activity Map.&link=My%20Link&region=My%20Region&page=My%20Page&.Activity Map&.a&.c&...
      ```

1. Dit rapport onderbreken met **[!UICONTROL Activity Map Link by Region]** om de koppeling/regio voor die pagina weer te geven:  ![](assets/am_breakdown.png){width="400px"}

## Stap 2. Rapporten Activity Map inschakelen {#section_D14F15D2FC0346FCAD8B3B87E6DD33D4}

Eerst, moet u Activity Map rapporten op een rapport-reeks niveau toelaten.

1. Meld u aan bij Adobe Analytics en navigeer naar  **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Selecteer een rapportsuite > **[!UICONTROL Edit Settings]** > **[!UICONTROL Activity Map]** > **[!UICONTROL Activity Map Reporting]** .
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
>Als u wilt dat gebruikers die geen beheerder zijn, Activity Map downloaden, maakt u een nieuwe gebruikersgroep met de machtiging &#39;Gereedschappen&#39; en &#39;Oudere ClickMap installeren&#39;. Dit machtigingsniveau in combinatie met de Activity Map Access biedt machtigingen om het gereedschap te downloaden en gebruiken.
