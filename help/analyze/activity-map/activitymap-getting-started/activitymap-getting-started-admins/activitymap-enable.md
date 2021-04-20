---
description: Verklaart de stappen de Admin van Analytics moet voltooien om de inzameling van de verbindingsverbinding van de Activity Map en gebruikersdownload toe te laten.
title: Activity Map inschakelen
uuid: 30433319-d0e6-4977-951a-4492b356e1f2
feature: Activity Map
role: Business Practitioner, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 7%

---


# Activity Map inschakelen{#enable-activity-map}

Verklaart de stappen de Admin van Analytics moet voltooien om de inzameling van de verbindingsverbinding van de Activity Map en gebruikersdownload toe te laten.

## Stap 1. Werk uw Javascript-code (AppMeasurement) bij naar v1.6 (of hoger) {#section_5D1586289DF2489289B1B6C1C80C300D}

De module Activity Map maakt deel uit van het bestand AppMeasurement.js (dat zich boven aan het bestand bevindt). De bibliotheek AppMeasurement zal de module van de Activity Map wanneer geconcretiseerd laden.

U kunt geen gegevens over de Activity Map verzamelen, tenzij u deze versie (of hoger) van AppMeasurement bijwerkt.

1. Download de nieuwste AppMeasurement-code (AppMeasurement_Javascript-1.6.zip) door naar **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Code Manager]** te gaan en [deze ](https://docs.adobe.com/content/help/en/analytics/implementation/js/overview.html) te implementeren.

   Wij hebben sommige [code van de steekproefimplementatie ](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-sample-implementation-code.md) omvat om u te helpen de veranderingen visualiseren die aan de code door de module van de Activity Map te omvatten zijn aangebracht.

1. De implementatie valideren:

   1. Wanneer op een klikbaar element wordt geklikt, worden de gegevens opgeslagen in een cookie met de naam s_sq.
   1. De gegevens van de Activity Map kunnen in het vraag-koord op de volgende vraag worden gezien. Bijvoorbeeld:

      ```
      …&c.&a.&Activity Map.&link=My%20Link&region=My%20Region&page=My%20Page&.Activity Map&.a&.c&...
      ```

1. Onderbreek dit rapport onderaan door **[!UICONTROL Activity Map Link by Region]** om de verbinding/het gebied voor die pagina te zien:  ![](assets/am_breakdown.png){width=&quot;400px&quot;}

## Stap 2. Rapporten {#section_D14F15D2FC0346FCAD8B3B87E6DD33D4} voor Activity Map inschakelen

Eerst, moet u Activity Map rapporten op een rapport-reeks niveau toelaten.

1. Meld u aan bij Adobe Analytics en navigeer naar **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Selecteer een rapportsuite > **[!UICONTROL Edit Settings]** > **[!UICONTROL Activity Map]** > **[!UICONTROL Activity Map Reporting]**.
1. De Activity Map verzamelt de verbindingsgegevens in de rapporten van de Activity Map. De activering wordt alleen uitgevoerd als u de variabelen eerst activeert door op **[!UICONTROL Enable Activity Map Reports]** te klikken.

   Met deze stap voegt u alle analytische afmetingen toe die u nodig hebt om gegevens te verzamelen.

1. Na ongeveer een uur, controleer [het Rapport van de Pagina van de Activity Map ](/help/analyze/activity-map/activitymap-reporting-analytics.md), dat alle pagina&#39;s toont waar de gebruikers op een verbinding klikten.

## Stap 3. Gebruikers toevoegen aan toegangsgroep {#section_4C7A47BB7DEF4AFFBC276392467F9675} Activity Mappen

1. Klik op **[!UICONTROL Add Users to Group]**.

   Hiermee gaat u naar de pagina voor groepsbeheer in de Admin Console.

1. [Voeg gebruikers toe aan deze ](https://docs.adobe.com/content/help/nl-NL/analytics/admin/user-product-management/user-groups/groups.html) groep en  **[!UICONTROL Save Group]**.

1. Hierdoor kunnen uw Admin-gebruikers Activity Map downloaden van **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Tools]** > **[!UICONTROL ActivityMap]**.

>[!NOTE]
>
>Als u wilt dat gebruikers die geen beheerder zijn, Activity Map downloaden, maakt u een nieuwe gebruikersgroep met de machtiging &#39;Gereedschappen&#39; en &#39;Oudere ClickMap installeren&#39;. Dit machtigingsniveau in combinatie met de Activity Map Access biedt machtigingen om het gereedschap te downloaden en gebruiken.
