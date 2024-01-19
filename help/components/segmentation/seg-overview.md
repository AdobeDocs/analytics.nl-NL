---
description: Met segmenten kunt u subsets bezoekers identificeren op basis van kenmerken of interacties op de website. De segmenten worden ontworpen als gecodificeerde publieksinzichten die u voor uw specifieke behoeften kunt bouwen, en dan verifiëren, uitgeven, en delen met andere teamleden of gebruik in andere producten van de Adobe en de mogelijkheden van Analytics.
title: Segmenten
feature: Segmentation
exl-id: 11d930ca-5d59-4ea5-b6e5-fe3d57be94fd
source-git-commit: 93099d36a65ca2bf16fbd6342f01bfecdc8c798e
workflow-type: tm+mt
source-wordcount: '1128'
ht-degree: 1%

---

# Segmenten

Met segmenten kunt u subsets bezoekers identificeren op basis van kenmerken of interacties op de website. De segmenten worden ontworpen als publieksinzichten die u voor uw specifieke behoeften kunt bouwen, en dan verifiëren, uitgeven, en delen met andere teamleden of gebruik in andere producten van de Adobe en de mogelijkheden van Analytics.

Segmenten zijn gebaseerd op een [!UICONTROL Visitor], [!UICONTROL Visit], en [!UICONTROL Hit] niveauhiërarchie die een genesteld containermodel gebruikt. Met de geneste containers kunt u bezoekerskenmerken en handelingen definiëren op basis van regels tussen en binnen de containers. Analysesegmenten kunnen worden gemaakt, goedgekeurd, gedeeld, opgeslagen en uitgevoerd voor meerdere producten en mogelijkheden in het deelvenster [!DNL Adobe Experience Cloud]. De segmenten kunnen van een rapport worden geproduceerd, in een dashboardrapport worden ingebouwd, of worden bookmarked voor snelle toegang.

U kunt segmenten bouwen en bewaren in de Bouwer van het Segment, of segmenten van een rapport van de Vallout produceren (in  Analysis Workspace). U kunt ook vooraf gebouwde segmenten op basis van specifieke regels tussen geneste containers gebruiken en uitbreiden, zodat u resultaten kunt filteren en op rapporten kunt toepassen. Daarnaast kunnen segmenten samen worden gebruikt als [gestapelde segmenten](/help/components/segmentation/segmentation-workflow/seg-workflow.md).

Segmenten identificeren

- wie uw bezoekers zijn (land, geslacht, koffiewinkel),
- welke apparaten en diensten zij gebruiken (browser, zoekmachine, mobiel apparaat);
- waar zij zijn genavigeerd (zoekmachine, vorige exitpagina, natuurlijke zoekopdracht);
- en nog veel meer.

<!--![](assets/seg.png)-->

Segmenten kunnen op de volgende waarden worden gebaseerd:

- Bezoekers op basis van kenmerken: browsertype, apparaat, aantal bezoeken, land, geslacht.
- Bezoekers op basis van interacties: campagnes, trefwoordzoekfunctie, zoekfunctie.
- Bezoekers op basis van uitgangen en ingangen: bezoekers uit Facebook, een gedefinieerde landingspagina, verwijzend domein.
- Bezoekers op basis van aangepaste variabelen: formulierveld, gedefinieerde categorieën, klant-id.

Wanneer het bouwen van publiekssegmenten in de Bouwer van het Segment, bepaalt u voorwaarden gebruikend [!UICONTROL AND] en [!UICONTROL OR] operatoren tussen containers.

<table style="table-layout:fixed; border: none;">

<tr>

<td style="background-color: #E5E4E2;" colspan="3" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_User_18_N.svg"/> Bezoekers</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200"></td>
<td style="background-color: #D3D3D3;" colspan="2" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Visit_18_N.svg"/> Bezoeken</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Hits</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;"></td><td colspan="2">EN</td></td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200"></td>
<td style="background-color: #D3D3D3;" colspan="2" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Visit_18_N.svg"/> Bezoeken</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Hits</td>
</tr>
</table>

<table style="table-layout:fixed; border: none;">

<tr>

<td style="background-color: #E5E4E2;" colspan="3" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_User_18_N.svg"/> Bezoekers</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200"></td>
<td style="background-color: #D3D3D3;" colspan="2" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Visit_18_N.svg"/> Bezoeken</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Hits</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;"></td><td colspan="2">OF</td></td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200"></td>
<td style="background-color: #D3D3D3;" colspan="2" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Visit_18_N.svg"/> Bezoeken</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Hits</td>
</tr>
</table>

<!--![](assets/standard_segment_containers.png)-->

Dit type van segmentfilters gegevensreeksen die op eigenschappen worden gebaseerd die met het worden verbonden die [!UICONTROL AND] en [!UICONTROL OR] operatoren.

- U kunt [pas veelvoudige segmenten op een rapport of een project toe](/help/components/segmentation/segmentation-workflow/seg-workflow.md).
- De segmenten zijn universeel aan alle rapportseries.
- De [Segment Builder](/help/components/segmentation/segmentation-workflow/seg-workflow.md) vereenvoudigt het maken van segmenten.
- De [Segmentbeheer](/help/components/segmentation/segmentation-workflow/seg-workflow.md) laat u opstelling [workflows](/help/components/segmentation/segmentation-workflow/seg-workflow.md) met functies voor segmentdeling, codering, verificatie en goedkeuring.
- U kunt [tagsegmenten](/help/components/segmentation/segmentation-workflow/seg-workflow.md) om later te organiseren en te zoeken in plaats van omslagen te gebruiken.
- U kunt [Opeenvolgende segmenten](/help/components/segmentation/segmentation-workflow/seg-sequential-build.md).
- De [!UICONTROL Page View] container is nu de [!UICONTROL Hit] container om erop te wijzen dat deze container alle types van gegevens en niet alleen paginameningen segmenteert. De aanroepen voor het bijhouden van koppelingen en trackhandelingen van de mobiele SDK&#39;s worden bijvoorbeeld allemaal opgenomen of uitgesloten in de aanraakcontainer.

## Segmentering in Analysis Workspace

Analysis Workspace bevat de volgende aanvullende functies:

- U kunt [vergelijken, segmenten](../../analyze/analysis-workspace/c-panels/c-segment-comparison/segment-comparison.md).
- Gebruiken [segmenten als afmetingen](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html) in een vergelijking.
- Segmenten gebruiken in [valutanotatie](../../analyze/analysis-workspace/visualizations/fallout/compare-segments-fallout.md).

## Door Adobe verschafte segmenten

De componentrails aan de linkerkant van het scherm geven segmenten weer die door u en uw bedrijf en Adobe segmenten zijn gemaakt en die uit het vak worden geleverd. Wanneer u op **[!UICONTROL Show all]** Deze segmenten worden doorgaans onder aan de lijst weergegeven en worden aan de rechterkant aangeduid met het logo van de Adobe.

## Opeenvolgende segmenten {#sequential}

Met opeenvolgende segmenten kunt u bezoekers identificeren op basis van navigatie en paginaweergave op uw site. Zo kunt u een segment van gedefinieerde handelingen en interacties opgeven. Met behulp van opeenvolgende segmenten kunt u bepalen wat een bezoeker leuk vindt en wat een bezoeker vermijdt. Bij het samenstellen van opeenvolgende segmenten [!UICONTROL THEN] wordt gebruikt om bezoekersnavigatie te bepalen en te bestellen.

<!--![](assets/sequential_seg.png)-->

| Eén bezoeken | Twee bezoeken | Drie bezoeken |
|---|---|---|
| Tijdens het eerste bezoek ging de bezoeker naar de hoofdbestemmingspagina A, die pagina B van de campagne uitsloot en vervolgens pagina C van het Product bekeken. | Tijdens het tweede bezoek ging de bezoeker opnieuw naar de hoofdbestemmingspagina A, met uitzondering van de campagnepagina B, en ging hij opnieuw naar productpagina C en vervolgens naar een nieuwe pagina D. | Tijdens het derde bezoek heeft de bezoeker hetzelfde pad ingevoerd en gevolgd als bij het eerste en tweede bezoek, en vervolgens pagina F geschrapt om rechtstreeks naar een bepaalde productpagina G te gaan. |

De opeenvolgende segmenten kunnen op de volgende klapwaarden worden gebaseerd:

- Bezoekers hebben een reeks pagina-hits: paginaweergaven tijdens één bezoek, paginaweergaven tijdens verschillende bezoeken, bezoeken die paginaweergaven uitsluiten.
- Bezoekers op basis van de weergaven tussen en na de pagina: na een tijdslimiet, tussen hits, na een gebeurtenis.

<table style="table-layout:fixed; border: none;">

<tr>

<td style="background-color: #E5E4E2;" colspan="3" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_User_18_N.svg"/> Bezoekers</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200"></td>
<td style="background-color: #D3D3D3;" colspan="2" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Visit_18_N.svg"/> Bezoeken</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Hits</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;"></td><td colspan="2">DAN</td></td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200"></td>
<td style="background-color: #D3D3D3;" colspan="2" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Visit_18_N.svg"/> Bezoeken</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Hits</td>
</tr>
</table>

<table style="table-layout:fixed; border: none;">

<tr>

<td style="background-color: #E5E4E2;" colspan="3" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_User_18_N.svg"/> Bezoekers</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200"></td>
<td style="background-color: #D3D3D3;" colspan="2" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Visit_18_N.svg"/> Bezoeken</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Hits</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;"></td><td style="background-color: #D3D3D3;"></td><td>EN</td></td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Hits</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;"></td><td colspan="2">DAN</td></td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200"></td>
<td style="background-color: #D3D3D3;" colspan="2" width="200" height="100"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Visit_18_N.svg"/> Bezoeken</td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Hits</td>

<tr>
<td style="background-color: #E5E4E2;"></td><td style="background-color: #D3D3D3;"></td><td>OF</td></td>
</tr>

<tr>
<td style="background-color: #E5E4E2;" width="200" height="100"></td>
<td style="background-color: #D3D3D3;" width="200" height="100"></td>
<td style="background-color: #C0C0C0;" width="200" height="100" colspan="1"><img src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg"/> Hits</td>
</tr>
</tr>
</table>

<!--![](assets/sequential_segmentation_containers_view.png)-->

Een opeenvolgend segment filtert gegevensreeksen die op gebruikersacties worden gebaseerd gebruikend [!UICONTROL THEN] operator.

## Hoe kan ik-segmentatievideo {#segment-video}

Deze video geeft een kort overzicht van welke segmentcontainers zijn en hoe ze moeten worden gebruikt:

>[!VIDEO](https://video.tv.adobe.com/v/25401/?quality=12&learn=on)


## Toegang tot de segmentatiehulpmiddelen {#access}

+++ **Hoe kan ik de Segment Builder bereiken?**

U kunt tot de Bouwer van het Segment toegang hebben door:

- Een bestaand rapport weergeven en op het pictogram Segmenten klikken  ![Segmentpictogram](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Segmentation_18_N.svg) in de linkernavigatie. Klik in de segmenttrack die wordt weergegeven op **[!UICONTROL Add]**, of

- Klik boven aan Segmentbeheer op **[!UICONTROL + Add]**.  ![Knop Toevoegen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_AddCircle_18_N.svg)

  of

- Klik op een bestaande segmenttitel in Segmentbeheer om het segment te bewerken in Segmentbouwer.

+++

+++ **Hoe kan ik Segmentbeheer openen?**

Toegang tot Segmentbeheer via:

- Ga naar  **[!UICONTROL Analytics]** > **[!UICONTROL Components]** in de bovenste navigatie. Klik vervolgens op **[!UICONTROL Segments]**, of

- Een bestaand rapport weergeven en op het pictogram Segmenten klikken  ![Segmentpictogram](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Segmentation_18_N.svg) in de linkernavigatie. Klik vervolgens op **[!UICONTROL Manage]**, of

- Druk op de schuine streep &#39;/&#39; in de interface en zoek naar segmentmanager.

+++

## Machtigingen {#section_648DFA3A882146C485A84ED014EEC707}

+++ **Welke rechten en voorrechten moet ik gebruiken, creëren, en segmenten beheren?**

Standaard kunnen alle gebruikers persoonlijke segmenten maken en bewerken. Beheerders kunnen echter bepalen wie [machtigingen om segmenten te maken](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/home.html) en kan ze toewijzen aan specifieke groepen. Deze segmenten kunnen rechtstreeks met andere gebruikers van Analytics worden gedeeld.

Beheerders kunnen elk segment bewerken en segmenten delen met groepen en met iedereen in de organisatie. [Meer...](/help/components/segmentation/seg-reference/seg-rights.md)

+++

+++ **Kan ik alle segmenten in mijn bedrijf zien?**

Ja, beheerders kunnen alle segmenten binnen de [!DNL Analysis Workspace] gebruikersinterface.

De Report Builder toont segmenten die u bezit en segmenten die met u worden gedeeld.

+++

+++ **Kan ik alle segmenten Analytics in de Manager van het Segment beheren?**

Ja, kunnen alle segmenten worden beheerd in de Manager van het Segment. De Manager van het segment toont segmenten die aan de eigenaar (gebruiker zichtbaar zijn die het segment) creeerde, gedeelde gebruikers, en admin gebruikers. De segmentkiezer geeft segmenten weer die eigendom zijn van en gedeeld worden met de gebruiker.

Beheerders kunnen alle segmenten in de Analysis Workspace-gebruikersinterface zien.

Report Builder geeft alleen segmenten weer die door u zijn gemaakt of segmenten die specifiek met u zijn gedeeld.

+++

+++ **Waarom kan ik dit segment niet verwijderen?**

Als het segment [bekendgemaakt aan het Experience Cloud](/help/components/segmentation/segmentation-workflow/seg-workflow.md), kunt u deze niet verwijderen of bewerken. U kunt de gekopieerde versie echter wel kopiëren en bewerken.

+++
