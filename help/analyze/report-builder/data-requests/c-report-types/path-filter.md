---
description: Beschrijft de stappen betrokken bij het toepassen van filters op een het knippen rapport.
title: Een padrapport filteren met de wizard Verzoek
topic: Report builder
uuid: 9b22d5b5-7ae8-49a2-90ae-0c1075562bbe
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Een padrapport filteren met de wizard Verzoek

Beschrijft de stappen betrokken bij het toepassen van filters op een het knippen rapport.

In dit voorbeeld worden paden naar sitesectie gebruikt.

1. Klik in Adobe Report Builder **[!UICONTROL Create]** om de wizard Verzoek te openen.
1. Selecteer de juiste rapportsuite.
1. Selecteer in de structuurweergave aan de linkerkant **[!UICONTROL Paths]** > **[!UICONTROL Site Sections]** > **[!UICONTROL Site Section Paths]**.

   ![](assets/site_section_path_1.png)

1. Geef de juiste datum of data op.
1. Klik op **[!UICONTROL Next]**.
1. In Stap 2 van de Tovenaar, onder **[!UICONTROL Row Labels]**, klik de **[!UICONTROL Top 1-10 (pattern applied)]** verbinding. In een padrapport wordt standaard een patroon toegepast.

   ![](assets/site_section_path_2.png)

1. Selecteer de **[!UICONTROL Filter]** optie.

   ![](assets/filter_option.png)

1. In het **[!UICONTROL Define 'Site Section Paths' Path Pattern]** dialoogvenster kunt u
   1. de uitgangspositie van het eerste verslag.
   1. het aantal ingangen u in dit rapport wilt tonen.
1. Klik **[!UICONTROL Edit]** om een padpatroon te definiëren.
1. Als u een aangepast patroon wilt, sleept u een willekeurig patroon uit de lijst aan de linkerkant naar het **[!UICONTROL Pattern Objects]** **[!UICONTROL Pattern Build Canvas]** rechtergedeelte.

   ![](assets/custom_pattern.png)

1. U kunt ook een vooraf gedefinieerd patroon selecteren in de **[!UICONTROL Select a Pattern]** vervolgkeuzelijst en dit wijzigen. Hier volgen de beschikbare patronen:

   ![](assets/select_a_pattern.png)

   Sommige van deze patronen zijn specifiek voor rapportbuilder: Het volgende-itempatroon van het pad van het item, het vorige-itempatroon van het pad afsluiten, het volgende-itempatroon.
1. Als u een vooraf gedefinieerd patroon wilt bewerken,
   1. Selecteer het. Selecteer bijvoorbeeld de **[!UICONTROL Exited Site Pattern]**: ![](assets/exited_site_pattern.png)

   1. Nu moet u het pad naar de sitesectie definiëren dat de gebruiker volgt voordat u afsluit. Klik op **[!UICONTROL Specific Item(s): 0 selected]**. U kunt dit pad definiëren door een reeks cellen te selecteren (als u een bestaande aanvraag bewerkt) of door een selectie te maken in een lijst met secties.
   1. Als u wilt selecteren uit een reeks cellen uit een vorige aanvraag, selecteert u **[!UICONTROL From range of cells]** en klikt u op het pictogram van de celkiezer. Kies vervolgens de cellen uit het rapport. ![](assets/choose_site_section_paths.png)

   1. Als u een gedeelte in een lijst met sitesecties wilt selecteren, selecteert **[!UICONTROL From list]** en klikt u **[!UICONTROL Add]**.
   1. Verplaats elementen van de **[!UICONTROL Available Elements]** kolom naar de **[!UICONTROL Selected Elements]** kolom door deze te selecteren en op de oranje pijl te klikken. Klik **[!UICONTROL OK]**. ![](assets/move_site_section_elements.png)

   1. Klik op **[!UICONTROL Save]** om het patroon dat u zojuist hebt ingesteld op te slaan.
   1. Klik **[!UICONTROL OK]** drie keer en klik dan **[!UICONTROL Finish]**. Het gefilterde padverzoek wordt nu gegenereerd.
