---
description: Een Adobe Analytics-dashboards scorecard maken
title: Een scorecard maken
feature: Analytics Dashboards
role: User, Admin
source-git-commit: 012bbfa54d97ffcaf4cd0de380c196df06a03bfe
workflow-type: tm+mt
source-wordcount: '915'
ht-degree: 0%

---


# Een scorecard maken

Een Adobe Analytics-scorecard toont belangrijke gegevensvisualisaties voor uitvoerende gebruikers in een getimede lay-out, zoals hieronder getoond:

![Voorbeeldscorecard](assets/intro_scorecard.png)

Als curator van dit scorecard, kunt u de Scorecard Bouwer gebruiken om te vormen welke tegels op scorecard voor uw uitvoerende consument verschijnen. U configureert ook hoe de gedetailleerde weergaven, of de onderverdelingen, kunnen worden aangepast wanneer op de tegels wordt getikt. De interface van de Bouwer Scorecard wordt hieronder getoond:

![Scorecard Builder](assets/scorecard_builder.png)

Als u het scorebord wilt maken, moet u het volgende doen:

1. Open de sjabloon [!UICONTROL Blank Mobile Scorecard].
2. Configureer het scorebord met gegevens en sla het op.

## Toegang krijgen tot de sjabloon [!UICONTROL Blank Mobile Scorecard]

U kunt tot het [!UICONTROL Blank Mobile Scorecard] malplaatje op één van de volgende manieren toegang hebben:

**Een nieuw project maken**

1. Open Adobe Analytics en klik op het tabblad **[!UICONTROL Workspace]**.
1. Klik **[!UICONTROL Create project]** en selecteer **[!UICONTROL Blank mobile scorecard]** projectmalplaatje.
1. Klik op **[!UICONTROL Create]**.

![Scorecard-sjabloon](assets/new_template.png)

of

1. Selecteer **[!UICONTROL Analytics dashboards (Mobile App)]** in het menu **[!UICONTROL Tools]**.
1. Klik op de knop **[!UICONTROL Create new scorecard]** in het volgende scherm.

## Vorm scorecard met gegevens en bewaar het

Het scorebordsjabloon implementeren:

1. Geef onder **[!UICONTROL Properties]** (in de rechterrail) een **[!UICONTROL Project report suite]** op waaruit u gegevens wilt gebruiken.

   ![Selectie van rapportsuite](assets/properties_save.png)

1. Als u een nieuwe tegel aan uw scorebord wilt toevoegen, sleept u een metrische waarde uit het linkerdeelvenster en zet u deze neer in de zone **[!UICONTROL Drag and Drop Metrics Here]**. U kunt ook een metrische waarde tussen twee tegels invoegen met behulp van een vergelijkbare workflow.

   ![Tegels toevoegen](assets/build_list.png)


   *Van elke tegel, kunt u tot een gedetailleerde mening toegang hebben die extra informatie over metrisch, zoals hoogste punten voor een lijst van verwante afmetingen toont.*


1. Als u een gerelateerde afmeting aan een metrische waarde wilt toevoegen, sleept u een afmeting uit het linkerdeelvenster en zet u deze op een tegel neer. U kunt bijvoorbeeld de juiste afmetingen (zoals **[!DNL DMA Region]** in dit voorbeeld) toevoegen aan de **[!UICONTROL Unique Visitors]**-meting door deze naar de tegel te slepen en neer te zetten; De afmetingen die u toevoegt, worden weergegeven onder de sectie voor de verdeling van de tegelspecifieke **[!UICONTROL Properties]**. U kunt meerdere afmetingen aan elke tegel toevoegen.

   ![Afmetingen toevoegen](assets/layer_dimensions.png)

   Wanneer u op een tegel in de Scorecard Builder klikt, toont het rechtse spoor de eigenschappen en de kenmerken verbonden aan die tegel. In deze rail, kunt u nieuwe **[!UICONTROL Title]** voor de tegel verstrekken en anders de tegel vormen door componenten te specificeren in plaats van hen te slepen en te laten vallen van de linkerspoorstaaf.

   ![Eigenschappen, tegel](assets/properties_tile.png)

   Als u op tegels klikt, wordt in een dynamische pop-up ook weergegeven hoe de uitsplitsingsweergave wordt weergegeven voor de uitvoerende gebruiker in de app. Als er geen afmeting op de tegel is toegepast, is de afbraakdimensie **hour** of **days**, afhankelijk van het standaarddatumbereik.

   ![Onderverdeling_weergave](assets/break_view.png)

   Elke dimensie die aan de tegel wordt toegevoegd, wordt weergegeven in een vervolgkeuzelijst in de gedetailleerde weergave van de app. De uitvoerende gebruiker kan dan uit de opties kiezen die in de drop-down lijst worden vermeld.

1. Als u segmenten op afzonderlijke tegels wilt toepassen, sleept u een segment uit het linkerdeelvenster en zet u het segment direct boven op de tegel neer. Als u het segment op alle tegels in Scorecard wilt toepassen, laat vallen de tegel bovenop scorecard. U kunt ook segmenten toepassen door segmenten te selecteren in het filtermenu onder de datumbereiken. U [configureert en past filters voor uw Scorecards](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/using-panels/using-drop-down-filters.html) op dezelfde manier toe als in Adobe Analytics Workspace.

   ![Segmenten maken voor filter](assets/segment_ui.png)

1. Op dezelfde manier om een component te verwijderen die op het volledige Scorecard wordt toegepast, klik overal op Scorecard buiten de tegels en verwijder het door **x** te klikken die verschijnt wanneer u over de component, zoals hieronder voor **Eerste Bezoekingen** segment toont:

   ![Remove_components](assets/new_remove.png)

1. U kunt combinaties van datumbereiken toevoegen en verwijderen die u in uw scorecard kunt selecteren door de vervolgkeuzelijst met datumbereiken te selecteren.

   ![Nieuwe scorekaart](assets/new_score_card.png)

   Elke nieuwe scorecard begint met 6 datumwaaiercombinaties die zich op de gegevens van vandaag en gisteren concentreren. U kunt overbodige datumbereiken verwijderen door op de x te klikken of u kunt elke datumbereikcombinatie bewerken door op het potlood te klikken.

   ![Nieuwe scorekaart2](assets/new_score_card2.png)

   Als u een primaire datum wilt maken of wijzigen, gebruikt u de vervolgkeuzelijst om een van de beschikbare datumbereiken te selecteren of sleept u een datumcomponent van de rechterrail naar de neerzetzone.

   ![Nieuwe scorekaart3](assets/new_score_card3.png)

   Als u een vergelijkingsdatum wilt maken, kunt u een keuze maken uit handige voorinstellingen voor algemene tijdvergelijkingen in het keuzemenu. U kunt ook een datumcomponent slepen en neerzetten vanaf de rechterrail.

   ![Nieuwe scorekaart4](assets/new_score_card4.png)

   Als het gewenste datumbereik nog niet is gemaakt, kunt u een nieuw datumbereik maken door op het kalenderpictogram te klikken.

   ![Nieuwe scorekaart4](assets/new_score_card5.png)

1. Hiermee gaat u naar de builder van het datumbereik waar u een nieuwe component voor het datumbereik kunt maken en opslaan. Als u het scorebord een naam wilt geven, klikt u op de naamruimte linksboven in het scherm en typt u de nieuwe naam.

   ![Naming_Scorecards](assets/new_name.png)

## De scorecard delen

U kunt als volgt het scorebord delen met een Executive-gebruiker:

1. Klik op het menu **[!UICONTROL Share]** en selecteer **[!UICONTROL Share scorecard]**.

1. Vul in het **[!UICONTROL Share mobile scorecard]**-formulier de velden met:

   * De naam van het scorebord opgeven
   * Beschrijving van het scorebord
   * Relatieve tags toevoegen
   * De ontvangers voor het scorebord opgeven

1. Klik op **[!UICONTROL Share]**.

![Share_Scorecards](assets/new_share.png)

Nadat u een scorecard hebt gedeeld, kunnen uw ontvangers tot het op hun dashboards van Analytics toegang hebben. Als u verdere veranderingen in scorecard in de Scorecard Bouwer aanbrengt, zullen zij automatisch in gedeelde scorecard worden bijgewerkt. De uitvoerende gebruikers zullen dan de veranderingen zien nadat het Scorecard op hun app verfrist.

Als u het Scorecard door nieuwe componenten bij te voegen bijwerkt, kunt u de scorecard opnieuw willen delen (en **[!UICONTROL Share embedded components]** optie) controleren om ervoor te zorgen dat uw uitvoerende gebruikers toegang tot deze veranderingen hebben.