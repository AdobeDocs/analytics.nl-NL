---
description: Het rangschikken en voorwaardelijke filters die u gebruikend logica Van Boole met EN/OR onderzoeksuitdrukkingen vormt.
title: Populairste filters
uuid: 558fa592-41be-4e66-8705-81262afe1fc7
feature: Report Builder
role: User, Admin
exl-id: 31587740-6caa-40cb-bb24-d7a15181f642
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 1%

---

# Populairste filters

Het rangschikken en voorwaardelijke filters die u gebruikend logica Van Boole met EN/OR onderzoeksuitdrukkingen vormt.

De meeste Populaire filters zijn expressiefilters die u gebruikend logica Van Boole met EN/OF voorwaarden, zoals [!UICONTROL Page does not contain]*`<product name>`*met voorwaarden of groepen voorwaarden zoals [!UICONTROL Includes All], [!UICONTROL Includes Any], of [!UICONTROL Excludes All] vormt. U kunt [save](/help/analyze/report-builder/layout/c-filter-dimensions/saved-filters.md) deze uitdrukkingen voor ander verzoek in dit werkboek, of in andere werkboeken.

**Een meest populaire filter maken**

1. Creeer of geef een verzoek uit, en ga naar [!UICONTROL Request Wizard: Step 2].

   ![Stapinfo](assets/dimension_filter.png)

1. Klik op [!UICONTROL Request Wizard: Step 2] op de koppeling naast de dimensie in het raster en kies **[!UICONTROL Filter]**.
1. Schakel in het formulier [!UICONTROL Choose Page] **[!UICONTROL Most Popular]** in en configureer vervolgens de volgende opties:

   **Beginpositie:** de beginpositie van een dimensie. Een standaardrangorde van 1 geeft het bovenste item in de lijst met gerapporteerde gegevens aan. Voor de dimensie [!UICONTROL Page] geeft een beginmarkering van 1 bijvoorbeeld de enkele meest gevraagde pagina van uw site aan. U zou 10 of een andere waarde als beginnende rangtelcel kunnen specificeren, die een rapport veroorzaakt die met 10 als hoogste begint. De metriek worden geschikt in dalende orde, zodat de lijnpunten met de grootste activiteit eerst in de lijst worden gemeld. Als u meer dan 50.000 paginanamen in één verzoek vereist, maar duizenden pagina&#39;s hebt waarop om te melden, kunt u het verzoek kopiëren en de beginnende rang veranderen om de aangewezen gegevens in blokken van 50.000 terug te winnen.

   **Aantal ingangen:**  ( [!UICONTROL Pivot Layout] slechts) bepaalt hoeveel punten voor bepaalde metrisch over een datumwaaier worden gemeld. Sommige metriek kan van honderden ingangen voor metrisch, terwijl anderen slechts een paar kunnen tonen. Bijvoorbeeld, voor de afmeting [!UICONTROL Site Section], wijst een aantal ingangen van 25 erop dat het rapport de 25 meest bezochte pagina&#39;s toont.

   Met pijlen kunt u de [!UICONTROL Starting Rank] en [!UICONTROL Number of Entries] van het eerste gegevenspunt in het blad wijzigen. Standaard is [!UICONTROL Starting Rank] ingesteld op 1 en [!UICONTROL Number of Entries] op 10. Deze waarden kunnen voor bepaalde metingen worden aangepast van minimaal 1 tot maximaal 50.000. Elke metrische waarde heeft zijn eigen plafond op [!UICONTROL Number of Entries]. Geen negatieve waarden of nul zijn toegestaan in deze velden. Als u een [!UICONTROL Starting Rank] als 15 en [!UICONTROL Number of Entries] als 10 kiest, komen de gegevensverzoeken voor metrisch terug de 10 meest bezochte pagina&#39;s, waar de eerste meest bezochte pagina nummer 15 in de lijst voor de specifieke datumwaaier is. Alle meest opgevraagde pagina&#39;s met een ranglijst van 15e tot en met 25e worden in aflopende volgorde weergegeven.

   >[!NOTE]
   >
   >Het toepassen van filters op bestaande verzoeken veroorzaakt veranderingen in de gepresenteerde gegevens. Stel dat u de bovenste tien [!UICONTROL Pages] hebt toegewezen aan de cellen $A$1 tot $A$10, met 1 voor [!UICONTROL Starting Rank] en 10 voor [!UICONTROL Number of Entries]. Als u deze waarden wijzigt in 1 voor [!UICONTROL Starting Rank] en slechts 3 voor [!UICONTROL Number of Entries], zullen de gegevens die eerder cellen $A$4 tot $A$10 invullen, niet meer verschijnen.

1. Als u een zoekopdracht wilt maken, klikt u op **[!UICONTROL Add]**.

   ![Stapinfo](assets/expressions_define_filter.png)

1. Configureer op het formulier [!UICONTROL Define Filter] de voorwaarden die geschikt zijn voor uw behoeften.

   ![select_cell_icon.png](assets/select_cell_icon.png): Hiermee kunt u een voorwaarde zoeken die is gedefinieerd in de waarde van een cel.

   **Voorwaarde toevoegen:een voorwaarde** toevoegen aan de expressie. Er is geen limiet aan het aantal voorwaarden dat u kunt toevoegen.

1. Klik op **[!UICONTROL OK]**.

   ![Stapinfo](assets/choose_page_02.png)

1. Klik in het formulier [!UICONTROL Choose Page] op **[!UICONTROL Save]** om de expressie op te slaan.
1. Klik op **[!UICONTROL OK]**.
