---
description: Beschrijft de stappen betrokken bij het toepassen van filters op een reserverapport.
title: Een uitvalrapport filteren met de wizard Aanvragen
uuid: 269e900e-23bd-48d8-9bac-69e3167a9c18
feature: Report Builder
role: User, Admin
exl-id: 6134d7d4-7287-4a83-92b6-d250ca15cf69
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 9%

---

# Een uitvalrapport filteren met de wizard Aanvragen

Beschrijft de stappen betrokken bij het toepassen van filters op een reserverapport.

In dit voorbeeld wordt het rapport Pagina-uitval weergegeven.

1. Klik in Adobe Report Builder op **[!UICONTROL Create]** om de wizard Verzoek te openen.
1. Selecteer de juiste rapportsuite.
1. Selecteer **[!UICONTROL Paths]** > **[!UICONTROL Page]** > **[!UICONTROL Page Fallout]** in de structuurweergave aan de linkerkant.

   ![](assets/page_fallout.png)

1. Configureer de juiste [datumbereiken](/help/analyze/report-builder/data-requests/configuring-report-dates/custom-calendar.md).
1. Klik op **[!UICONTROL Next]**.
1. In Stap 2 van de Tovenaar, onder **[!UICONTROL Row Labels]**, klik **[!UICONTROL Define Checkpoints]** verbinding. (In een uitvalrapport moet u altijd padelementen definiëren, in tegenstelling tot in een padrapport, waarin een patroon vooraf wordt toegepast.)

   ![](assets/define_checkpoints.png)

1. Selecteer de optie **[!UICONTROL Filter]**.

1. Definieer in het dialoogvenster **[!UICONTROL Define Site Section Fallout Checkpoints]** controlepunten vanuit een bereik cellen of vanuit een lijst. Klik vervolgens op **[!UICONTROL OK]**.
1. Bepaal of u een keuze wilt maken uit een reeks cellen of uit een lijst.
1. Als u een keuze maakt in een lijst, klikt u op **[!UICONTROL Add]** om controlepunten te selecteren die u wilt toevoegen aan het uitvalpad. U kunt tussen 3 en 8 controlepunten definiëren. (Zoek naar beschikbare elementen door **[!UICONTROL More]** te klikken.)

   Zie [Dimension filteren](/help/analyze/report-builder/layout/c-filter-dimensions/filter-dimensions.md) voor meer informatie over het verfijnen van het filter. 1. Verplaats **[!UICONTROL Available Elements]** van de linkerkolom naar rechts door deze te selecteren en op de oranje pijl te klikken.
1. Klik **[!UICONTROL OK]** drie keer, dan klik **[!UICONTROL Finish]**.

   Het rapport moet nu worden vernieuwd.
