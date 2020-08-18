---
description: Verklaart de stappen de Admin van Analytics moet voltooien om de inzameling van de verbindingsverbinding van de Activity Map en gebruikersdownload toe te laten.
title: Activity Map inschakelen
topic: Activity map
uuid: 30433319-d0e6-4977-951a-4492b356e1f2
translation-type: tm+mt
source-git-commit: aea3b4448b61e8b1b217b4f74b0b80c9fbedd070
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 6%

---


# Activity Map inschakelen{#enable-activity-map}

Verklaart de stappen de Admin van Analytics moet voltooien om de inzameling van de verbindingsverbinding van de Activity Map en gebruikersdownload toe te laten.

## Stap 1. Werk uw Javascript-code (AppMeasurement) bij naar v1.6 (of hoger) {#section_5D1586289DF2489289B1B6C1C80C300D}

De module Activity Map maakt deel uit van het bestand AppMeasurement.js (dat zich boven aan het bestand bevindt). De bibliotheek AppMeasurement zal de module van de Activity Map wanneer geconcretiseerd laden.

U kunt geen gegevens over de Activity Map verzamelen, tenzij u deze versie (of hoger) van AppMeasurement bijwerkt.

1. Download de nieuwste AppMeasurement-code (AppMeasurement_Javascript-1.6.zip) door naar **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Code Manager]** te gaan en deze [te](https://docs.adobe.com/content/help/en/analytics/implementation/js/overview.html)implementeren.

   We hebben code [voor](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-sample-implementation-code.md) voorbeeldimplementatie opgenomen om u te helpen de wijzigingen die in de code zijn aangebracht, zichtbaar te maken door de module Activity Map op te nemen.

1. De implementatie valideren:

   1. Wanneer op een klikbaar element wordt geklikt, worden de gegevens opgeslagen in een cookie met de naam s_sq.
   1. De gegevens van de Activity Map kunnen in het vraag-koord op de volgende vraag worden gezien. Bijvoorbeeld:

      ```
      …&c.&a.&Activity Map.&link=My%20Link&region=My%20Region&page=My%20Page&.Activity Map&.a&.c&...
      ```

1. Onderbreek dit rapport onderaan door de verbinding/de regio voor die pagina **[!UICONTROL Activity Map Link by Region]** te zien:  ![](assets/am_breakdown.png){width=&quot;400px&quot;}

## Stap 2. Rapporten Activity Map inschakelen {#section_D14F15D2FC0346FCAD8B3B87E6DD33D4}

Eerst, moet u Activity Map rapporten op een rapport-reeks niveau toelaten.

1. Meld u aan bij Adobe Analytics en navigeer naar **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Selecteer een rapportsuite > **[!UICONTROL Edit Settings]** > **[!UICONTROL Activity Map]** > **[!UICONTROL Activity Map Reporting]** .
1. De Activity Map verzamelt de verbindingsgegevens in de rapporten van de Activity Map. U kunt de activering alleen uitvoeren als u eerst de variabelen activeert door op **[!UICONTROL Enable Activity Map Reports]** te klikken.

   Met deze stap voegt u alle analytische afmetingen toe die u nodig hebt om gegevens te verzamelen.

1. Na ongeveer een uur, controleer het rapport [van de Pagina van de](/help/analyze/activity-map/activitymap-reporting-analytics.md)Activity Map, dat alle pagina&#39;s toont waar de gebruikers op een verbinding klikte.

## Stap 3. Gebruikers toevoegen aan de toegangsgroep Activity Map {#section_4C7A47BB7DEF4AFFBC276392467F9675}

1. Klik op **[!UICONTROL Add Users to Group]**.

   Hiermee gaat u naar de pagina voor groepsbeheer in de Admin Console.

1. [Voeg gebruikers toe aan deze groep](https://docs.adobe.com/content/help/nl-NL/analytics/admin/user-product-management/user-groups/groups.html) en **[!UICONTROL Save Group]**.

1. Hierdoor kunnen uw Admin-gebruikers Activity Map downloaden van **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Tools]** > **[!UICONTROL ActivityMap]** .

>[!NOTE]
>
>Als u wilt dat gebruikers die geen beheerder zijn, Activity Map downloaden, maakt u een nieuwe gebruikersgroep met de machtiging &#39;Gereedschappen&#39; en &#39;Oudere ClickMap installeren&#39;. Dit machtigingsniveau in combinatie met de Activity Map Access biedt machtigingen om het gereedschap te downloaden en gebruiken.
