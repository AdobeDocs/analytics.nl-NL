---
description: Beschrijft de stappen betrokken bij het toepassen van filters op een het knippen rapport.
title: Een padrapport filteren met de wizard Aanvragen
feature: Report Builder
role: User, Admin
exl-id: 085351b3-4d9c-45cf-b2a8-379f05932b26
source-git-commit: d218d07ec16e981d7e148092b91fbbd5711e840f
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 4%

---

# Een padrapport filteren met de wizard Aanvragen

Beschrijft de stappen betrokken bij het toepassen van filters op een het knippen rapport.

In dit voorbeeld worden paden naar sitesectie gebruikt.

1. Klik in Adobe Report Builder op **[!UICONTROL Create]** om de wizard Verzoek te openen.
1. Selecteer de juiste rapportsuite.
1. Selecteer in de structuurweergave aan de linkerkant de optie **[!UICONTROL Paths]** > **[!UICONTROL Site Sections]** > **[!UICONTROL Site Section Paths]**.

   ![Schermafbeelding met geselecteerde paden voor sitesectie.](assets/site_section_path_1.png)

1. Geef de juiste datum of data op.

1. Klik op **[!UICONTROL Next]**.

1. In Stap 2 van de Tovenaar, onder **[!UICONTROL Row Labels]** klikt u op de knop **[!UICONTROL Top 1-10 (pattern applied)]** koppeling. In een padrapport wordt standaard een patroon toegepast.

   ![Screenshot met het standaardpadpatroon.](assets/site_section_path_2.png)

1. Selecteer de **[!UICONTROL Filter]** -optie.

   ![Schermopname die de optie Filter markeert.](assets/filter_option.png)

1. In de **[!UICONTROL Define 'Site Section Paths' Path Pattern]** kunt u
   * De startpositie van het eerste verslag.
   * Het aantal ingangen u in dit rapport wilt tonen.
1. Klikken **[!UICONTROL Edit]** om een padpatroon te definiëren.

1. Als u een aangepast patroon wilt gebruiken, sleept u het gereedschap **[!UICONTROL Pattern Objects]** van de lijst links in de **[!UICONTROL Pattern Build Canvas]** rechts.

   ![](assets/custom_pattern.png)

1. U kunt ook een vooraf gedefinieerd patroon selecteren in het menu **[!UICONTROL Select a Pattern]** vervolgkeuzelijst en wijzigen. Hier volgen de beschikbare patronen:

   ![](assets/select_a_pattern.png)

   Sommige van deze patronen gelden specifiek voor Report Builder: Het volgende-itempatroon van het toegangspad, het vorige-itempatroon van het pad afsluiten, het volgende-itempatroon van het pad.

## Een vooraf gedefinieerd patroon bewerken

Nadat u een patroon hebt geselecteerd, kunt u een vooraf gedefinieerd patroon bewerken.

1. Selecteer het patroon in de bovenstaande stappen. Selecteer bijvoorbeeld de **[!UICONTROL Exited Site Pattern]**:

   ![Schermafbeelding die het geselecteerde patroon markeert.](assets/exited_site_pattern.png)

1. Definieer het pad naar de sitesectie dat de gebruiker volgt voordat deze afsluit. Klik op **[!UICONTROL Specific Item(s): 0 selected]**. U kunt dit pad definiëren door een reeks cellen te selecteren als u een bestaande aanvraag bewerkt of door een selectie te maken in een lijst met secties.

1. Als u wilt selecteren uit een reeks cellen uit een vorige aanvraag, selecteert u **[!UICONTROL From range of cells]** en klik op het pictogram van de celkiezer. Kies vervolgens de cellen uit het rapport.

   ![Screenshot met de opties die u kunt kiezen uit een reeks cellen of uit een lijst.](assets/choose_site_section_paths.png)

1. Selecteer in een lijst met sitesecties de optie **[!UICONTROL From list]** en klik op **[!UICONTROL Add]**.

1. Elementen verplaatsen vanuit het deelvenster **[!UICONTROL Available Elements]** aan de **[!UICONTROL Selected Elements]** door deze te selecteren en op de oranje pijl te klikken. Klik **[!UICONTROL OK]**.

   ![Screenshot met de beschikbare elementen en de geselecteerde elementen.](assets/move_site_section_elements.png)

1. Als u het patroon dat u zojuist hebt gemaakt wilt opslaan, klikt u op **[!UICONTROL Save]**.

1. Klikken **[!UICONTROL OK]** drie keer en klik vervolgens op **[!UICONTROL Finish]** om het gefilterde pad te genereren.
