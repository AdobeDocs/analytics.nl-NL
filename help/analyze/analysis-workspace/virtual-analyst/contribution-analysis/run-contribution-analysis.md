---
description: Stel een rapport van de Analyse van de Bijdrage in een project van de Werkruimte in werking.
title: Bijdrageanalyse uitvoeren
uuid: 5282a5f9-0771-4974-93cb-335204bde114
feature: AI-gereedschappen
role: User, Admin
exl-id: 20d1ba8d-3e4e-4702-ae28-5eb6bf00847b
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 3%

---

# Bijdrageanalyse uitvoeren

De bijdrageanalyse is een intensief machinaal leerproces dat bedoeld is om contribuanten aan een waargenomen anomalie in Adobe Analytics aan het licht te brengen. De bedoeling is de gebruiker te helpen om gebieden van nadruk of mogelijkheden voor extra analyse veel sneller te vinden dan anders mogelijk zou zijn.

## Bijdrageanalyse uitvoeren {#section_7D2C5E48A5664727941DF4C90976D9DC}

Er zijn twee manieren om een beroep te doen op de analyse van de bijdrage in een project:

* In een vrije lijst met dagelijkse granulariteit, klik om het even welke rij met de rechtermuisknop aan en selecteer **[!UICONTROL Run Contribution Analysis]**. U kunt het zelfs op rijen in werking stellen die geen anomalie tonen.

   >[!NOTE]
   >
   >Wij steunen momenteel de analyse van de bijdragen alleen met de dagelijkse granulariteit.

   ![](assets/run_ca.png)

* Houd de muisaanwijzer boven een afwijkend gegevenspunt in een lijndiagram in een lijndiagram. Klik op de koppeling **[!UICONTROL Analyze]** die wordt weergegeven.

   ![](assets/contribution-analysis.png)

1. (Optioneel) Nadat u in het lijndiagram of een tabel op **[!UICONTROL Run Contribution Analysis]** hebt geklikt, kunt u het bereik van de analyse beperken (en zo de analyse versnellen) met [de afmetingen](#section_F6932F4BF74544B5872164E7B1E0C6FC) uitsluiten.

1. Wacht terwijl de analyse van uw bijdrage wordt geladen. Dit kan veel tijd in beslag nemen, afhankelijk van de grootte van uw rapportenpakket en het aantal dimensies. De analyse van de bijdrage voert analyse op de hoogste 50.000 punten per dimensie uit.
1. Analysis Workspace laadt vervolgens een nieuw deelvenster voor de analyse van bijdragen rechtstreeks in dit project. U zult veel vertrouwde panelen opmerken als u Analyse van de Bijdrage in Rapporten &amp; Analytics eerder hebt gebruikt:

   * Een visualisatie die het aantal **Visits** op die dag toont.
   * Een maandelijkse **Bezoekt trendlijn** voor context.
   * **De belangrijkste** Punten die tot deze anomalie hebben bijgedragen, die door de  [bijdragescore](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html), plus metrisch in kwestie wordt gesorteerd, en een Unieke Metrisch van Bezoekers om metrisch in context vanuit een rangschikkend perspectief te zetten.

   * In de tabel [Gegenereerde segmenten](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) (Top Item Clusters) worden koppelingen van de bovenste items aangegeven op basis van de bijdragenscore, anomalieën en het totale percentage dat bijdraagt aan de afwijkende meting. Dit wordt vervolgens vastgelegd als een publiekssegment (bijdragesegment 1, bijdragesegment 2, enz.). Als u op de knop &quot;i&quot; (info) klikt, krijgt u een weergave van de definitie van elk automatisch segment, inclusief de items die er bovenaan staan:

      ![](assets/auto_segment.png)

1. Aangezien de analyse van de bijdrage nu deel van Analysis Workspace uitmaakt, kunt u uit een aantal van zijn eigenschappen van het de klikmenu van een lijst van een lijst voordeel halen om uw analyse nog betekenisvoller te maken, zoals:

   * [Elk afmetingsitem omlaag splitsen op een andere afmeting.](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md)
   * [Een of meer rijen Trending.](/help/analyze/analysis-workspace/home.md#section_34930C967C104C2B9092BA8DCF2BF81A)
   * [Nieuwe visualisaties toevoegen.](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md)
   * [Waarschuwingen maken.](/help/components/c-alerts/intellligent-alerts.md)
   * [Segmenten maken of vergelijken.](/help/analyze/analysis-workspace/c-panels/c-segment-comparison/segment-comparison.md)

>[!NOTE]
>
>We benadrukken de anomalie die wordt geanalyseerd met een blauwe stip in de bijdrageanalyse en de projecten voor intelligente waarschuwingen die eraan gekoppeld zijn. Dit geeft een duidelijkere indicatie van hoe de anomalie wordt geanalyseerd.

## Afmetingen uitsluiten van bijdrageanalyse {#section_F6932F4BF74544B5872164E7B1E0C6FC}

Het kan voorkomen dat u bepaalde dimensies wilt uitsluiten van de Contribute-analyse. Het kan bijvoorbeeld zijn dat u helemaal niets aan uw browser of hardware kunt schelen en dat u de analyse wilt versnellen door deze te verwijderen.

1. Nadat u **[!UICONTROL Run Contribution Analysis]** (of **[!UICONTROL Analyze]** in een lijngrafiek) hebt geklikt, toont het **[!UICONTROL Excluded Dimensions]** paneel.

1. Sleep gewoon ongewenste afmetingen naar het **[!UICONTROL Excluded Dimensions]**-deelvenster en sla de lijst op door op **[!UICONTROL Set as Default]** te klikken. U kunt ook op **[!UICONTROL Clear All]** klikken om opnieuw te beginnen met het selecteren van de afmetingen die u wilt uitsluiten.

   ![](assets/exclude_dimensions.png)

1. Klik nogmaals op **[!UICONTROL Run Contribution Analysis]** nadat u afmetingen hebt toegevoegd om uit te sluiten (of wanneer u dit niet wilt doen).
1. Als u ooit de lijst van uitgesloten afmetingen moet herzien, enkel dubbelklik Dimension, en de lijst van uitgesloten dimensies toont:

   ![](assets/excluded-dimensions.png)

1. Verwijder gewoon ongewenste afmetingen door op de x naast de elementen te klikken en de lijst vervolgens op te slaan door op **[!UICONTROL Set as Default]** te klikken.
