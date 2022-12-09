---
description: Het rangschikken en voorwaardelijke filters die u gebruikend logica Van Boole met EN/OR onderzoeksuitdrukkingen vormt.
title: Populairste filters
uuid: 558fa592-41be-4e66-8705-81262afe1fc7
feature: Report Builder
role: User, Admin
exl-id: 31587740-6caa-40cb-bb24-d7a15181f642
source-git-commit: e7346b11a7d3eb4c18ec02df6c8a07574e02a2b4
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 1%

---

# Populairste filters

Het rangschikken en voorwaardelijke filters die u gebruikend logica Van Boole met EN/OR onderzoeksuitdrukkingen vormt.

De meeste Populaire filters zijn uitdrukkingsfilters die u gebruikend logica Van Boole met EN/OF voorwaarden vormt, zoals [!UICONTROL Page does not contain]*`<product name>`*met omstandigheden of groepen van omstandigheden zoals [!UICONTROL Includes All], [!UICONTROL Includes Any], of [!UICONTROL Excludes All]. U kunt [opslaan](/help/analyze/report-builder/layout/c-filter-dimensions/saved-filters.md) deze uitdrukkingen voor andere verzoek in dit werkboek, of in andere werkboeken.

**Een meest populaire filter maken**

1. Een aanvraag maken of bewerken en naar de [!UICONTROL Request Wizard: Step 2].

   ![Stapinfo](/help/admin/admin/assets/filter.png)

1. Op de [!UICONTROL Request Wizard: Step 2]klikt u op de koppeling naast de dimensie in het raster en kiest u **[!UICONTROL Filter]**.
1. Op de [!UICONTROL Choose Page] form, enable **[!UICONTROL Most Popular]** Configureer vervolgens de volgende opties:

   **Beginpositie:** De beginpositie van een dimensie. Een standaardrangorde van 1 geeft het bovenste item in de lijst met gerapporteerde gegevens aan. Bijvoorbeeld voor de dimensie [!UICONTROL Page], een beginmarkering van 1 geeft de enige meest gevraagde pagina van uw site aan. U zou 10 of een andere waarde als beginnende rangtelcel kunnen specificeren, die een rapport veroorzaakt die met 10 als hoogste begint. De metriek worden geschikt in dalende orde, zodat de lijnpunten met de grootste activiteit eerst in de lijst worden gemeld. Als u meer dan 50.000 paginanamen in één verzoek vereist, maar duizenden pagina&#39;s hebt waarop om te melden, kunt u het verzoek kopiëren en de beginnende rang veranderen om de aangewezen gegevens in blokken van 50.000 terug te winnen.

   **Aantal vermeldingen:** ( [!UICONTROL Pivot Layout] (slechts) bepaalt hoeveel punten voor bepaalde metrisch over een datumwaaier worden gerapporteerd. Sommige metriek kan van honderden ingangen voor metrisch, terwijl anderen slechts een paar kunnen tonen. Bijvoorbeeld voor de dimensie [!UICONTROL Site Section]Een aantal van 25 geeft aan dat het rapport de 25 meest bezochte pagina&#39;s bevat.

   Met pijlen kunt u de [!UICONTROL Starting Rank] en [!UICONTROL Number of Entries] van het eerste gegevenspunt op het blad. Standaard worden de [!UICONTROL Starting Rank] is ingesteld op 1 en [!UICONTROL Number of Entries] tot en met 10. Deze waarden kunnen voor bepaalde metingen worden aangepast van minimaal 1 tot maximaal 50.000. Elke metrie heeft zijn eigen plafond op [!UICONTROL Number of Entries]. Geen negatieve waarden of nul zijn toegestaan in deze velden. Als u een [!UICONTROL Starting Rank] als 15 en [!UICONTROL Number of Entries] als 10 , komen de gegevensverzoeken voor metrische informatie terug op de tien meest bezochte pagina &#39; s , waar de eerste meest bezochte pagina nummer 15 is in de lijst voor het specifieke datumbereik . Alle meest opgevraagde pagina&#39;s met een ranglijst van 15e tot en met 25e worden in aflopende volgorde weergegeven.

   >[!NOTE]
   >
   >Het toepassen van filters op bestaande verzoeken veroorzaakt veranderingen in de gepresenteerde gegevens. Stel dat u de top tien hebt toegewezen [!UICONTROL Pages] naar cellen $A$1 tot en met $A$10, met 1 voor [!UICONTROL Starting Rank] en 10 voor [!UICONTROL Number of Entries]. Als u deze waarden wijzigt in 1 voor [!UICONTROL Starting Rank] en slechts 3 voor [!UICONTROL Number of Entries], zullen de gegevens die eerder cellen $A$4 tot $A$10 vulden niet meer verschijnen.

1. Als u een zoekopdracht wilt maken, klikt u op **[!UICONTROL Add]**.

   ![Stapinfo](assets/expressions_define_filter.png)

1. Op de [!UICONTROL Define Filter] vorm, vorm de voorwaarden aangewezen voor uw behoeften.

   ![select_cell_icon.png](assets/select_cell_icon.png): Hiermee kunt u een voorwaarde zoeken die is gedefinieerd in de waarde van een cel.

   **Voorwaarde toevoegen:** Voegt een voorwaarde aan de uitdrukking toe. Er is geen limiet aan het aantal voorwaarden dat u kunt toevoegen.

1. Klik op **[!UICONTROL OK]**.

   ![Stapinfo](assets/choose_page_02.png)

1. Op de [!UICONTROL Choose Page] formulier, klikken **[!UICONTROL Save]** om de expressie op te slaan.
1. Klik op **[!UICONTROL OK]**.
