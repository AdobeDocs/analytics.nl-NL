---
description: Met segmenten kunt u subsets bezoekers identificeren op basis van kenmerken of interacties op de website. Segmenten zijn ontworpen als gecodificeerde publieksinzichten die u kunt opbouwen voor uw specifieke behoeften en vervolgens kunt controleren, bewerken en delen met andere teamleden of kunt gebruiken in andere Adobe-producten en analysemogelijkheden.
title: Segmenten
feature: Segmentation
exl-id: 11d930ca-5d59-4ea5-b6e5-fe3d57be94fd
source-git-commit: 80e4a3ba4a5985563fcf02acf06997b4592261e4
workflow-type: tm+mt
source-wordcount: '1004'
ht-degree: 1%

---

# Segmenten

Met segmenten kunt u subsets bezoekers identificeren op basis van kenmerken of interacties op de website. Segmenten zijn ontworpen als publieksinzichten die u kunt opbouwen voor uw specifieke behoeften en die u vervolgens kunt controleren, bewerken en delen met andere teamleden of kunt gebruiken in andere Adobe-producten en analysemogelijkheden.

Segmenten zijn gebaseerd op een [!UICONTROL Visitor] -, [!UICONTROL Visit] - en [!UICONTROL Hit] -hiërarchie met behulp van een genest containermodel. Met de geneste containers kunt u bezoekerskenmerken en handelingen definiëren op basis van regels tussen en binnen de containers. Analysesegmenten kunnen worden gemaakt, goedgekeurd, gedeeld, opgeslagen en uitgevoerd voor meerdere producten en mogelijkheden in de [!DNL Adobe Experience Cloud] . De segmenten kunnen van een rapport worden geproduceerd, in een dashboardrapport worden ingebouwd, of worden bookmarked voor snelle toegang.

U kunt segmenten bouwen en bewaren in de bouwer van het Segment, of segmenten van een rapport van de Vallout produceren (in [!UICONTROL Analysis Workspace]). U kunt ook vooraf gebouwde segmenten op basis van specifieke regels tussen geneste containers gebruiken en uitbreiden, zodat u resultaten kunt filteren en op rapporten kunt toepassen. Bovendien kunnen de segmenten samen als [ gestapelde segmenten ](/help/components/segmentation/segmentation-workflow/seg-workflow.md) worden gebruikt.

Segmenten identificeren

- wie uw bezoekers zijn (land, geslacht, koffiewinkel),
- welke apparaten en diensten zij gebruiken (browser, zoekmachine, mobiel apparaat);
- waar zij zijn genavigeerd (zoekmachine, vorige exitpagina, natuurlijke zoekopdracht);
- en nog veel meer.

<!--![](assets/seg.png)-->

Segmenten kunnen op de volgende waarden worden gebaseerd:

- Bezoekers op basis van kenmerken: browsertype, apparaat, aantal bezoeken, land, geslacht.
- Bezoekers op basis van interacties: campagnes, trefwoordzoekfunctie, zoekfunctie.
- Bezoekers op basis van uitgangen en ingangen: bezoekers van Facebook, een gedefinieerde landingspagina, verwijzend domein.
- Bezoekers op basis van aangepaste variabelen: formulierveld, gedefinieerde categorieën, klant-id.

Wanneer u publiekssegmenten maakt in de Segment Builder, definieert u voorwaarden met de operatoren [!UICONTROL AND] en [!UICONTROL OR] tussen containers.

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

Dit type segment filtert gegevenssets op basis van kenmerken die zijn gekoppeld met de operatoren [!UICONTROL AND] en [!UICONTROL OR] .

- U kunt [ veelvoudige segmenten op een rapport of een project ](/help/components/segmentation/segmentation-workflow/t-seg-apply.md) toepassen.
- De segmenten zijn universeel aan alle rapportseries.
- De [ bouwer van het Segment ](/help/components/segmentation/segmentation-workflow/seg-build.md) vereenvoudigt segmentverwezenlijking.
- De [ manager van het Segment ](/help/components/segmentation/segmentation-workflow/seg-manage.md) laat u opstelling [ werkschema&#39;s ](/help/components/segmentation/segmentation-workflow/seg-workflow.md) met segment het delen, het etiketteren, de controle, en goedkeuringseigenschappen.
- U kunt [ markeringssegmenten ](/help/components/segmentation/segmentation-workflow/seg-tag.md) aan organisatie en onderzoek later in plaats van het gebruiken van omslagen.
- U kunt [ opeenvolgende segmenten ](/help/components/segmentation/segmentation-workflow/seg-sequential-build.md) tot stand brengen.
- De container [!UICONTROL Page View] is nu de container van [!UICONTROL Hit] om erop te wijzen dat deze container alle types van gegevens en niet alleen paginameningen segmenteert. Bijvoorbeeld, verbindings het volgen vraag, en de vraag van de spooractie van mobiele SDKs zijn allen inbegrepen of uitgesloten door de klapcontainer.

## Segmentering in Analysis Workspace

Analysis Workspace bevat de volgende aanvullende functies:

- U kunt [ segmenten ](../../analyze/analysis-workspace/c-panels/c-segment-comparison/segment-comparison.md) vergelijken.
- Gebruik segmenten als afmetingen in vrije-vormtabelvisualisaties.
- De segmenten van het gebruik in [ reserveanalyse ](../../analyze/analysis-workspace/visualizations/fallout/compare-segments-fallout.md).

## Door Adobe verschafte segmenten

De component links spoor toont segmenten die door u en uw bedrijf en de segmenten van Adobe worden gecreeerd die uit de doos worden verstrekt. Wanneer u **[!UICONTROL Show all]** klikt, verschijnen deze segmenten typisch bij de bodem van de lijst en door ![ AdobeLogoSmall ](/help/assets/icons/AdobeLogoSmall.svg) geïdentificeerd.

## Sequentiële segmenten {#sequential}

Met opeenvolgende segmenten kunt u bezoekers identificeren op basis van navigatie en paginaweergave op uw site. Zo kunt u een segment van gedefinieerde handelingen en interacties opgeven. Met behulp van opeenvolgende segmenten kunt u bepalen wat een bezoeker leuk vindt en wat een bezoeker vermijdt. Wanneer u opeenvolgende segmenten maakt, wordt de operator [!UICONTROL THEN] gebruikt om de navigatie van bezoekers te definiëren en te bestellen.

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

Een opeenvolgend segment filtert gegevensreeksen die op gebruikersacties gebruikend de [!UICONTROL THEN] exploitant worden gebaseerd.

## Hoe kan ik-segmentatievideo {#segment-video}

Deze video geeft een kort overzicht van welke segmentcontainers zijn en hoe te om hen te gebruiken.


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ de containers van het Segment ](https://video.tv.adobe.com/v/3429104?quality=12&learn=on&captions=dut){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


## Machtigingen {#permissions}

+++ **Welke rechten en voorrechten moet ik gebruiken, creëren, en segmenten beheren?**

Standaard kunnen alle gebruikers persoonlijke segmenten maken en bewerken. Nochtans, kunnen Admins beslissen wie [ toestemmingen zou moeten hebben om segmenten ](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/home.html?lang=nl-NL) tot stand te brengen en hen aan specifieke groepen kunnen toewijzen. Deze segmenten kunnen rechtstreeks met andere gebruikers van Analytics worden gedeeld.

Beheerders kunnen elk segment bewerken en segmenten delen met groepen en met iedereen in de organisatie. [ de rechten van het segment door rol ](/help/components/segmentation/seg-reference/seg-rights.md)

+++

+++ **kan ik alle segmenten in mijn bedrijf zien?**

Ja, beheerders kunnen alle segmenten binnen de gebruikersinterface van [!DNL Analysis Workspace] zien.

In Report Builder worden segmenten die u bezit en segmenten die met u worden gedeeld, weergegeven.

+++

+++ **kan ik alle segmenten van Analytics in de manager van het Segment beheren?**

Ja, kunnen alle segmenten in de manager van het Segment worden beheerd. De manager van het segment toont segmenten die aan de eigenaar (gebruiker zichtbaar zijn die het segment) creeerde, gedeelde gebruikers, en admin gebruikers. De segmentkiezer geeft segmenten weer die eigendom zijn van en gedeeld worden met de gebruiker.

Beheerders kunnen alle segmenten in de Analysis Workspace-gebruikersinterface zien.

Report Builder geeft alleen segmenten weer die door u zijn gemaakt of segmenten die specifiek met u zijn gedeeld.

+++

+++ **waarom kan ik geen segment schrappen?**

Als het segment [ aan Experience Cloud ](/help/components/segmentation/segmentation-workflow/seg-workflow.md) werd gepubliceerd, kunt u niet het segment schrappen of het segment uitgeven. U kunt het segment echter kopiëren en de gekopieerde versie bewerken.

+++
