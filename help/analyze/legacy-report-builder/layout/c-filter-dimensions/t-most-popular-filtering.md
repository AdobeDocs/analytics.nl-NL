---
description: Het rangschikken en voorwaardelijke filters die u gebruikend logica Van Boole met EN/OR onderzoeksuitdrukkingen vormt.
title: Populairste filters
uuid: 558fa592-41be-4e66-8705-81262afe1fc7
feature: Report Builder
role: User, Admin
exl-id: 31587740-6caa-40cb-bb24-d7a15181f642
source-git-commit: e09234ca27fbf923e026aa1f2ed0ebfed636bf7c
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 0%

---

# Populairste filters

{{legacy-arb}}

Het rangschikken en voorwaardelijke filters die u gebruikend logica Van Boole met EN/OR onderzoeksuitdrukkingen vormt.

De meeste populaire filters zijn expressiefilters die u configureert met behulp van Booleaanse logica met AND/OR-voorwaarden, zoals [!UICONTROL Page does not contain]*`<product name>`*met voorwaarden of groepen voorwaarden zoals [!UICONTROL Includes All] , [!UICONTROL Includes Any] of [!UICONTROL Excludes All] . U kunt [&#x200B; sparen &#x200B;](/help/analyze/legacy-report-builder/layout/c-filter-dimensions/saved-filters.md) deze uitdrukkingen voor ander verzoek in dit werkboek, of in andere werkboeken.

**om tot een Populairste filter** te leiden

1. Maak of bewerk een aanvraag en ga door naar de [!UICONTROL Request Wizard: Step 2] .

1. Klik in het [!UICONTROL Request Wizard: Step 2] op de koppeling naast de dimensie in het raster en kies vervolgens **[!UICONTROL Filter]** .

   ![&#x200B; Schermafbeelding die de Define dialoog van de Filter met opties tonen om door Toepassing, Gebruiker, en Project te filtreren.](/help/admin/tools/assets/filter.png)

1. Schakel [!UICONTROL Choose Page] in het **[!UICONTROL Most Popular]** -formulier in en configureer vervolgens de volgende opties:

   **Begin Rank:** De beginnende rang van een afmeting. Een standaardrangorde van 1 geeft het bovenste item in de lijst met gerapporteerde gegevens aan. Voor de dimensie [!UICONTROL Page] geeft een beginmarkering van 1 bijvoorbeeld de enkele meest gevraagde pagina van uw site aan. U zou 10 of een andere waarde als beginnende rangtelcel kunnen specificeren, die een rapport veroorzaakt die met 10 als hoogste begint. De metriek worden geschikt in dalende orde, zodat de lijnpunten met de grootste activiteit eerst in de lijst worden gemeld. Als u meer dan 50.000 paginanamen in één verzoek vereist, maar duizenden pagina&#39;s hebt waarop om te melden, kunt u het verzoek kopiëren en de beginnende rang veranderen om de aangewezen gegevens in blokken van 50.000 terug te winnen.

   **Aantal Ingangen:** ( [!UICONTROL Pivot Layout] slechts) bepaalt hoeveel punten voor bepaalde metrisch over een datumwaaier worden gemeld. Sommige metriek kan van honderden ingangen voor metrisch, terwijl anderen slechts een paar kunnen tonen. Bijvoorbeeld, voor de afmeting [!UICONTROL Site Section], wijst een aantal ingangen van 25 erop dat het rapport de 25 meest bezochte pagina&#39;s toont.

   Met pijlen kunt u de [!UICONTROL Starting Rank] en [!UICONTROL Number of Entries] van het eerste gegevenspunt in het blad wijzigen. Standaard is [!UICONTROL Starting Rank] ingesteld op 1 en [!UICONTROL Number of Entries] op 10. Deze waarden kunnen voor bepaalde metingen worden aangepast van minimaal 1 tot maximaal 50.000. Elke metrische waarde heeft zijn eigen plafond op [!UICONTROL Number of Entries]. Geen negatieve waarden of nul zijn toegestaan in deze velden. Als u een [!UICONTROL Starting Rank] as 15 en [!UICONTROL Number of Entries] as 10 kiest, worden de tien meest bezochte pagina&#39;s door gegevensaanvragen voor de norm geretourneerd. De eerste bezochte pagina is nummer 15 in de lijst voor het specifieke datumbereik. Alle meest opgevraagde pagina&#39;s met een ranglijst van 15e tot en met 25e worden in aflopende volgorde weergegeven.

   >[!NOTE]
   >
   >Het toepassen van filters op bestaande verzoeken veroorzaakt veranderingen in de gepresenteerde gegevens. Stel dat u de bovenste tien [!UICONTROL Pages] hebt toegewezen aan de cellen $A$1 tot $A$10, met 1 voor [!UICONTROL Starting Rank] en 10 voor [!UICONTROL Number of Entries] . Als u deze waarden wijzigt in 1 voor [!UICONTROL Starting Rank] en slechts 3 voor [!UICONTROL Number of Entries] , worden de gegevens die eerder de cellen $A$4 tot en met $A$10 invullen, niet meer weergegeven.

1. Klik op **[!UICONTROL Add]** om een zoekopdracht te maken.

1. Configureer in het formulier [!UICONTROL Define Filter] de voorwaarden die geschikt zijn voor uw behoeften.


   ![&#x200B; Schermafbeelding die de Define dialoog van de Filter toont.](assets/expressions_define_filter.png)

   Met het pictogram voor het selecteren van cellen kunt u een voorwaarde zoeken die is gedefinieerd in de waarde van een cel. ![&#x200B; het uitgezochte celpictogram.](assets/select_cell_icon.png)

   De **voegt voorwaarde** verbinding toe laat u een voorwaarde aan de uitdrukking toevoegen. Er is geen limiet aan het aantal voorwaarden dat u kunt toevoegen.

1. Klik op **[!UICONTROL OK]**.

   ![&#x200B; Schermafbeelding van de Define dialoog van de Filter met de O.K. knoop in de bodem rechterkant.](assets/choose_page_02.png)

1. Klik in het [!UICONTROL Choose Page] -formulier op **[!UICONTROL Save]** om de expressie op te slaan.
1. Klik op **[!UICONTROL OK]**.
