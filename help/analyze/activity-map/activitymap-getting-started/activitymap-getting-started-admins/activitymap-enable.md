---
description: Verklaart de stappen de Admin van Analytics moet voltooien om de de verbindingsinzameling van de Kaart van de Activiteit en gebruikersdownload toe te laten.
title: Activiteitenoverzicht inschakelen
topic: Activity map
uuid: 30433319-d0e6-4977-951a-4492b356e1f2
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Activiteitenoverzicht inschakelen{#enable-activity-map}

Verklaart de stappen de Admin van Analytics moet voltooien om de de verbindingsinzameling van de Kaart van de Activiteit en gebruikersdownload toe te laten.

## Stap 1. Werk uw Javascript-code (AppMeasurement) bij naar v1.6 (of hoger) {#section_5D1586289DF2489289B1B6C1C80C300D}

De module Activiteitenkaart maakt deel uit van het bestand AppMeasurement.js (dat zich boven in het bestand bevindt). De bibliotheek AppMeasurement zal de module van de Kaart van de Activiteit wanneer geconcretiseerd laden.

De gegevens van de Kaart van de activiteit kunnen niet worden verzameld tenzij u aan deze versie (of hoger) van AppMeasurement bijwerkt.

1. Download de nieuwste AppMeasurement-code (AppMeasurement_Javascript-1.6.zip) door naar **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Code Manager]** te gaan en deze [te](https://marketing.adobe.com/resources/help/en_US/sc/implement/js_implementation.html)implementeren.

   We hebben code [voor](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-sample-implementation-code.md) voorbeeldimplementatie opgenomen om u te helpen de wijzigingen die in de code zijn aangebracht, zichtbaar te maken door de module Activiteitenkaart op te nemen.

1. De implementatie valideren:

   1. Wanneer op een klikbaar element wordt geklikt, worden de gegevens opgeslagen in een cookie met de naam s_sq.
   1. De gegevens van de Kaart van de Activiteit kunnen in het vraag-koord op de volgende vraag worden gezien. Bijvoorbeeld:

      ```
      …&c.&a.&Activity Map.&link=My%20Link&region=My%20Region&page=My%20Page&.Activity Map&.a&.c&...
      ```

1. Onderbreek dit rapport onderaan door de verbinding/de regio voor die pagina **[!UICONTROL Activity Map Link by Region]** te zien:  ![](assets/am_breakdown.png){width=&quot;400px&quot;}

## Stap 2. Activiteitentoewijzingsrapporten inschakelen {#section_D14F15D2FC0346FCAD8B3B87E6DD33D4}

Eerst, moet u de rapporten van de Kaart van de Activiteit op een rapport-reeks niveau toelaten.

1. Meld u aan bij Adobe Analytics en navigeer naar **[!UICONTROL Analytics]** > **[!UICONTROL Admin > Report Suites >[select report suite]> Edit Settings > Activity Map]** > **[!UICONTROL Activity Map Reporting]** .
1. De Kaart van de activiteit verzamelt de verbindingsgegevens in de rapporten van de Kaart van de Activiteit. U kunt de activering alleen uitvoeren als u eerst de variabelen activeert door op **[!UICONTROL Enable Activity Map Reports]** te klikken.

   Met deze stap voegt u alle analytische afmetingen toe die u nodig hebt om gegevens te verzamelen.

1. Na ongeveer een uur, controleer het Rapport [van de Pagina van de](/help/analyze/activity-map/activitymap-reporting-analytics.md)Activiteitenkaart, dat alle pagina&#39;s toont waar de gebruikers op een verbinding klikte.

## Stap 3. Gebruikers toevoegen aan de toegangsgroep Activiteitenkaart {#section_4C7A47BB7DEF4AFFBC276392467F9675}

1. Klik op **[!UICONTROL Add Users to Group]**.

   Hiermee gaat u naar de pagina voor groepsbeheer in de beheerconsole.

1. [Voeg gebruikers toe aan deze groep](https://marketing.adobe.com/resources/help/en_US/reference/groups.html) en **[!UICONTROL Save Group]**.

1. Hierdoor kunnen uw Admin-gebruikers de Activity Map downloaden van **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Tools]** > **[!UICONTROL ActivityMap]** .

>[!NOTE] Als u niet-admin gebruikers de Kaart van de Activiteit wilt downloaden, creeer een nieuwe gebruikersgroep die toestemmingen aan &quot;Hulpmiddelen&quot;en &quot;Oudere Installatie ClickMap van de Verouderde verleent. Dit niveau van toestemming die met de Toegang van de Kaart van de Activiteit wordt gecombineerd verleent toestemmingen om het hulpmiddel te downloaden en te gebruiken.
