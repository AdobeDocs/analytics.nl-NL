---
description: Beschrijft de stappen betrokken bij het toepassen van filters op een het knippen rapport.
title: Een padrapport filteren met de wizard Aanvragen
feature: Report Builder
role: User, Admin
exl-id: 085351b3-4d9c-45cf-b2a8-379f05932b26
source-git-commit: 1ee50c6a2231795b2ad0015a79e09b7c1c74d850
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 5%

---

# Een padrapport filteren met de wizard Aanvragen

Beschrijft de stappen betrokken bij het toepassen van filters op een het knippen rapport.

In dit voorbeeld worden paden naar sitesectie gebruikt.

1. Klik in Adobe Report Builder op **[!UICONTROL Create]** om de wizard Verzoek te openen.
1. Selecteer de juiste rapportsuite.
1. Selecteer in de structuurweergave aan de linkerkant de optie **[!UICONTROL Paths]** > **[!UICONTROL Site Sections]** > **[!UICONTROL Site Section Paths]**.

   ![](assets/site_section_path_1.png)

1. Geef de juiste datum of data op.
1. Klik op **[!UICONTROL Next]**.
1. In Stap 2 van de Tovenaar, onder **[!UICONTROL Row Labels]** klikt u op de knop **[!UICONTROL Top 1-10 (pattern applied)]** koppeling. In een padrapport wordt standaard een patroon toegepast.

   ![](assets/site_section_path_2.png)

1. Selecteer **[!UICONTROL Filter]** optie.

   ![](assets/filter_option.png)

1. In de **[!UICONTROL Define 'Site Section Paths' Path Pattern]** kunt u
   1. de uitgangspositie van het eerste verslag.
   1. het aantal ingangen u in dit rapport wilt tonen.
1. Klikken **[!UICONTROL Edit]** om een padpatroon te definiëren.
1. Als u een aangepast patroon wilt gebruiken, sleept u een patroon **[!UICONTROL Pattern Objects]** van de lijst links in de **[!UICONTROL Pattern Build Canvas]** rechts.

   ![](assets/custom_pattern.png)

1. U kunt ook een vooraf gedefinieerd patroon selecteren in het menu **[!UICONTROL Select a Pattern]** vervolgkeuzelijst en wijzigen. Hier volgen de beschikbare patronen:

   ![](assets/select_a_pattern.png)

   Sommige van deze patronen zijn specifiek voor rapportbuilder: Het volgende-itempatroon van het pad van het item, het vorige-itempatroon van het pad afsluiten, het volgende-itempatroon.
1. Als u een vooraf gedefinieerd patroon wilt bewerken,
   1. Selecteer het. Selecteer bijvoorbeeld de **[!UICONTROL Exited Site Pattern]**: ![](assets/exited_site_pattern.png)

   1. Nu moet u het pad naar de sitesectie definiëren dat de gebruiker volgt voordat u afsluit. Klik op **[!UICONTROL Specific Item(s): 0 selected]**. U kunt dit pad definiëren door een reeks cellen te selecteren (als u een bestaande aanvraag bewerkt) of door een selectie te maken in een lijst met secties.
   1. Als u wilt selecteren uit een reeks cellen uit een vorige aanvraag, selecteert u **[!UICONTROL From range of cells]** en klik op het pictogram van de celkiezer. Kies vervolgens de cellen uit het rapport. ![](assets/choose_site_section_paths.png)

   1. Selecteer in een lijst met sitesecties de optie **[!UICONTROL From list]** en klik op **[!UICONTROL Add]**.
   1. Elementen verplaatsen vanuit het deelvenster **[!UICONTROL Available Elements]** aan de **[!UICONTROL Selected Elements]** door deze te selecteren en op de oranje pijl te klikken. Klik **[!UICONTROL OK]**. ![](assets/move_site_section_elements.png)

   1. Klik op **[!UICONTROL Save]**.
   1. Klikken **[!UICONTROL OK]** drie keer en klik vervolgens op **[!UICONTROL Finish]**. Het gefilterde padverzoek wordt nu gegenereerd.
