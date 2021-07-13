---
description: Beschrijft de stappen betrokken bij het toepassen van filters op een het knippen rapport.
title: Een padrapport filteren met de wizard Aanvragen
uuid: 9b22d5b5-7ae8-49a2-90ae-0c1075562bbe
feature: Report Builder
role: User, Admin
exl-id: 085351b3-4d9c-45cf-b2a8-379f05932b26
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 6%

---

# Een padrapport filteren met de wizard Aanvragen

Beschrijft de stappen betrokken bij het toepassen van filters op een het knippen rapport.

In dit voorbeeld worden paden naar sitesectie gebruikt.

1. Klik in Adobe Report Builder op **[!UICONTROL Create]** om de wizard Verzoek te openen.
1. Selecteer de juiste rapportsuite.
1. Selecteer **[!UICONTROL Paths]** > **[!UICONTROL Site Sections]** > **[!UICONTROL Site Section Paths]** in de structuurweergave aan de linkerkant.

   ![](assets/site_section_path_1.png)

1. Geef de juiste datum of data op.
1. Klik op **[!UICONTROL Next]**.
1. In Stap 2 van de Tovenaar, onder **[!UICONTROL Row Labels]**, klik **[!UICONTROL Top 1-10 (pattern applied)]** verbinding. In een padrapport wordt standaard een patroon toegepast.

   ![](assets/site_section_path_2.png)

1. Selecteer de optie **[!UICONTROL Filter]**.

   ![](assets/filter_option.png)

1. In het dialoogvenster **[!UICONTROL Define 'Site Section Paths' Path Pattern]** kunt u
   1. de uitgangspositie van het eerste verslag.
   1. het aantal ingangen u in dit rapport wilt tonen.
1. Klik op **[!UICONTROL Edit]** om een padpatroon te definiëren.
1. Als u een aangepast patroon wilt, sleept u **[!UICONTROL Pattern Objects]** uit de lijst aan de linkerkant naar **[!UICONTROL Pattern Build Canvas]** aan de rechterkant.

   ![](assets/custom_pattern.png)

1. U kunt ook een vooraf gedefinieerd patroon selecteren in de vervolgkeuzelijst **[!UICONTROL Select a Pattern]** en dit wijzigen. Hier volgen de beschikbare patronen:

   ![](assets/select_a_pattern.png)

   Sommige van deze patronen zijn specifiek voor rapportbuilder: Het volgende-itempatroon van het pad van het item, het vorige-itempatroon van het pad afsluiten, het volgende-itempatroon.
1. Als u een vooraf gedefinieerd patroon wilt bewerken,
   1. Selecteer het. Selecteer bijvoorbeeld **[!UICONTROL Exited Site Pattern]**: ![](assets/exited_site_pattern.png)

   1. Nu moet u het pad naar de sitesectie definiëren dat de gebruiker volgt voordat u afsluit. Klik op **[!UICONTROL Specific Item(s): 0 selected]**. U kunt dit pad definiëren door een reeks cellen te selecteren (als u een bestaande aanvraag bewerkt) of door een selectie te maken in een lijst met secties.
   1. Selecteer **[!UICONTROL From range of cells]** en klik op het pictogram van de celkiezer om een reeks cellen uit een vorige aanvraag te selecteren. Kies vervolgens de cellen uit het rapport. ![](assets/choose_site_section_paths.png)

   1. Selecteer **[!UICONTROL From list]** en klik op **[!UICONTROL Add]** om een lijst met sitesecties te selecteren.
   1. Verplaats elementen van de **[!UICONTROL Available Elements]** kolom naar de **[!UICONTROL Selected Elements]** kolom door hen te selecteren en de oranje pijl te klikken. Klik **[!UICONTROL OK]**. ![](assets/move_site_section_elements.png)

   1. Klik op **[!UICONTROL Save]** om het patroon dat u zojuist hebt gemaakt op te slaan.
   1. Klik **[!UICONTROL OK]** drie keer en klik dan **[!UICONTROL Finish]**. Het gefilterde padverzoek wordt nu gegenereerd.
