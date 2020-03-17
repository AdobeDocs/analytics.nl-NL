---
description: 'U kunt de afmetingen van het publiek AAM door Analytics gebruiken. De geïntegreerde segmenten zijn nieuwe dimensies van Analytics genoemd identiteitskaart van het publiek en de Naam van het publiek, en kunnen enkel als een andere dimensie worden gebruikt die Analytics verzamelt. In Gegevensfeeds worden de publiek-id''s opgeslagen in de kolom "mc_audiences". Deze afmetingen zijn momenteel niet beschikbaar in Data Workbench of LiveStream. Enkele voorbeelden van de manier waarop de dimensies van het publiek kunnen worden benut zijn '
solution: Experience Cloud
title: De publieksgegevens in Analytics gebruiken
uuid: 203925fb-f070-441c-813a-43099cb9b2b9
translation-type: tm+mt
source-git-commit: ''

---


# De publieksgegevens in Analytics gebruiken

U kunt de afmetingen van het publiek AAM door Analytics gebruiken. De geïntegreerde segmenten zijn nieuwe dimensies van Analytics genoemd identiteitskaart van het publiek en de Naam van het publiek, en kunnen enkel als een andere dimensie worden gebruikt die Analytics verzamelt. In Gegevensfeeds worden de publiek-id&#39;s opgeslagen in de kolom &quot;mc_audiences&quot;. Deze afmetingen zijn momenteel niet beschikbaar in Data Workbench of LiveStream. Enkele voorbeelden van de manier waarop de dimensies van het publiek kunnen worden benut zijn:

## Werkruimte Analyse {#section_C70837499BEA4DED885B3486C9E02C68}

In de Werkruimte van de Analyse, verschijnen de segmenten AAM als twee dimensies.

1. Ga naar **[!UICONTROL Workspace]**.
1. Selecteer in de lijst met **[!UICONTROL Dimensions]** de afmetingen **[!UICONTROL Audience ID]** of **[!UICONTROL Audience Name]**. Naam is een vriendelijke indeling van de id.

   ![](assets/aw-mcaudiences.png)

## Segmentvergelijking {#section_E72B80B6470C42D4B9B19BE90E6070A2}

[De Vergelijking](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/segment-comparison.html) van het segment ontdekt de statistisch meest significante verschillen tussen twee segmenten. De gegevens van het publiek kunnen in de Vergelijking van het Segment op twee manieren worden gebruikt: 1) als de twee segmenten die worden vergeleken, en 2) als items in de tabel &quot;Top Dimension Items&quot;.

1. Ga naar **[!UICONTROL Workspace]** en selecteer het **[!UICONTROL Segment Comparison]** paneel van de linkerspoorstaaf.

1. Zoeken naar [!UICONTROL Audiences Name] in het **[!UICONTROL Component]** menu.

1. Open [!UICONTROL Audiences Name]zodat de verwante dimensie-items worden weergegeven.
1. Sleep het publiek u in de bouwer van de Vergelijking van het Segment wilt vergelijken.
1. (Optioneel): U kunt ook andere dimensie-items of -segmenten invoegen. Maximaal 2 kunnen worden vergeleken.
1. Klik op **[!UICONTROL Build]**.

   De dimensies Soorten publiek-id en Naam worden automatisch weergegeven in de tabel &#39;Items voor de bovenste afmeting&#39;, omdat dit aanvullende profielgegevens zijn voor de twee segmenten die worden vergeleken.

   ![](assets/aud-segcompare.png)

## Klantenreis (stroom) in analysewerkruimte {#section_FC30E5795C9D4539838E30FE11FAEA6E}

AAM-segmentgegevens worden via hit-by-hit doorgegeven aan Analytics en vertegenwoordigen het publiekslidmaatschap voor een bezoeker op dat moment. Dit betekent dat een bezoeker in één segment kan vallen (bijvoorbeeld &quot;Bewustmaking&quot;), en later in aanmerking komen voor een meer gekwalificeerd segment (bv. &quot;Overweging&quot;). U kunt [stroom](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/flow.html) in de Werkruimte van de Analyse gebruiken om de reis visualiseren een bezoeker tussen publiek neemt.

1. Ga naar **[!UICONTROL Workspace]** en selecteer de **[!UICONTROL Flow]** visualisatie in de linkerrails.

1. Sleep de [!UICONTROL Audience Name] dimensie naar de Flow Builder.
1. Klik op **[!UICONTROL Build]**.
1. (Optioneel): Sleep een andere dimensie naar de stroomvisualisatie om een [interdimensionale stroom](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/multi-dimensional-flow.html)te maken.

![](assets/flow-aamaudiences.png)

Soorten publiek kan ook worden gebruikt in [uitvalvisualisaties](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/fallout_flow.html).

## Venn Visualisatie in de werkruimte Analyse {#section_E78AB764FB5047148B51DC1526B0DF89}

[In de Venn-visualisaties](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/venn.html) wordt de overlapping tussen maximaal 3 segmenten weergegeven.

1. Ga naar **[!UICONTROL Workspace]** en selecteer de **[!UICONTROL Venn]** visualisatie in de linkerrails.

1. Zoek naar [!UICONTROL Audience Name] in het componentenmenu.
1. Open [!UICONTROL Audience Name] zodat de verwante dimensie-items worden weergegeven.
1. Sleep het publiek dat u wilt vergelijken naar de Venn builder.
1. (Optioneel): U kunt andere afmetingspunten of segmenten eveneens brengen; maximaal 3 kunnen worden vergeleken.
1. Klik op **[!UICONTROL Build]**.

![](assets/venn-viz.png)

## Segment Builder {#section_2AA81852A1404AB894472CA8959461B6}

U kunt de dimensies van het publiek in de Bouwer [](https://marketing.adobe.com/resources/help/en_US/analytics/segment/seg_build.html)van het Segment van de Analyse, samen met de gedragsinformatie opnemen die de Analytics verzamelt.

1. Ga naar **[!UICONTROL Components]** > **[!UICONTROL Segments]** .
1. Klik **[!UICONTROL Add]** om een nieuw segment te maken.
1. Nadat u het segment een naam hebt gegeven, sleept u de [!UICONTROL Audience Name] dimensie naar het deelvenster Definities.
1. (Optioneel): Voeg andere criteria aan het segment toe.
1. Sla het segment op.

   ![](assets/aud-segbuilder.png)

## Rapporten en analyses en Report Builder {#section_04E8FD30F73344D7937AD3C6CD19E34A}

1. Ga naar **[!UICONTROL Reports]** > **[!UICONTROL Visitor Profile]** > **[!UICONTROL Audience ID Reports]** om het analyserapport weer te geven.
1. Vanuit deze map hebt u toegang tot de afmetingen Audience ID en Audience Name.

   ![](assets/mc-audiences.png)

