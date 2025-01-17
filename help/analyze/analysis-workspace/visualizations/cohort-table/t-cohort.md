---
description: Maak een cohort en voer een rapport voor cohortanalyse uit in Analysis Workspace.
keywords: Analysis Workspace
title: Een cohortanalyserapport uitvoeren
feature: Cohort Analysis
role: User, Admin
exl-id: 523e6f62-b428-454b-9460-6b06e96742c3
source-git-commit: d4ad8b988ebcc177c76777b20a54cc20e8241d4d
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 1%

---

# Een [!UICONTROL Cohort Analysis] -rapport configureren

Maak een cohort en voer een [!UICONTROL Cohort Analysis] -rapport uit in Analysis Workspace.

1. Klik in Analysis Workspace op het pictogram **[!UICONTROL Visualizations]** in de linkerrails en sleep een **[!UICONTROL Cohort Table]** naar het canvas.

   ![](assets/cohort-table.png)

1. Definieer de waarden **[!UICONTROL Inclusion Criteria]** , **[!UICONTROL Return Criteria]** , **[!UICONTROL Cohort Type]** en **[!UICONTROL Settings]** zoals gedefinieerd in de onderstaande tabel.

   | Element | Beschrijving |
   |--- |--- |
   | **[!UICONTROL Inclusion Criteria]** | U kunt maximaal 10 inclusiesegmenten en maximaal 3 inclusiemetriek toepassen. Met de metrische waarde wordt opgegeven wat een gebruiker in een cohort plaatst. Bijvoorbeeld, als inclusiemetrisch Orden is, slechts zullen de gebruikers die een orde tijdens de tijdwaaier van de cohortanalyse plaatsten in de aanvankelijke cohort worden omvat.<br> de standaardexploitant tussen metriek is EN, maar u kunt het in OF veranderen. Bovendien kunt u numerieke filters toevoegen aan deze cijfers. Bijvoorbeeld: &quot;Bebezoeken >= 1&quot;.</br> |
   | **[!UICONTROL Return Criteria]** | U kunt tot 10 terugkeersegmenten en tot 3 terugkeermetriek toepassen. Metrisch wijst erop of de gebruiker (behoud) of niet (klusje) is behouden. Als de retourwaarde bijvoorbeeld Video-weergaven is, worden alleen gebruikers die video&#39;s tijdens volgende tijdsperioden (na de periode waarin ze aan een cohort zijn toegevoegd) weergegeven als behouden. Een andere maatstaf die retentie kwantificeert, zijn Bezoekingen. |
   | **[!UICONTROL Granularity]** | De tijdsgranulariteit van Dag, Week, Maand, Kwart, of Jaar. |
   | **[!UICONTROL Type]** | **[!UICONTROL Retention]** (standaardwaarde): met een retentiecohort wordt gemeten hoe goed de bezoekerscohorten in de loop der tijd naar de eigenschap terugkeren. Dit is het standaardcohort dat we altijd hebben gehad en dat het gedrag van gebruikers weergeeft en herhaalt. Een [!UICONTROL Retention] -kleur wordt aangegeven door de kleur groen in de tabel.<br>**[!UICONTROL Churn]**: met een churn (ook wel &#39;kenmerk&#39; of &#39;fallout&#39; genoemd) cohort wordt gemeten hoe de bezoekerscohorten in de loop der tijd uit uw eigenschap vallen. Churn = 1 - Behoud. [!UICONTROL Churn] is een goede maatstaf voor kleverigheid en kansen door u te laten zien hoe vaak klanten niet terugkomen. Met churn kunt u de scherpstellingsgebieden analyseren en identificeren. Welke codesegmenten kunnen hierbij enige aandacht krijgen. Een [!UICONTROL Churn] Cohort wordt aangegeven door de kleur rood in de tabel (vergelijkbaar met fallout in onze **[!UICONTROL Flow]**visualisatie). </br> |
   | **[!UICONTROL Settings]** | **[!UICONTROL Rolling Calculation]**: berekent het behoud of de kolom op basis van de vorige kolom in plaats van de kolom Opgenomen (standaard). [!UICONTROL Rolling Calculation] wijzigt de berekeningsmethode voor de &#39;return&#39;-periodes. Bij de normale berekening zijn onafhankelijke gebruikers betrokken die aan de &quot;return&quot;-criteria voldoen en deel uitmaakten van de opnemingsperiode, ongeacht of zij al dan niet in het cohort voor de voorgaande periode waren opgenomen. In plaats daarvan zoekt [!UICONTROL Rolling Calculation] gebruikers die voldoen aan de &quot;return&quot;-criteria en die deel uitmaakten van de vorige periode. Daarom filtert [!UICONTROL Rolling Calculation] de gebruikers die voortdurend aan de periode van de &quot;terugkeer&quot;criteria voldoen. [!UICONTROL Return] -criteria worden toegepast op elk van de perioden die tot de geselecteerde periode leiden. </br><br>**[!UICONTROL Latency Table]**: Een [!UICONTROL Latency] -tabel meet de tijd die is verstreken voor en na de gebeurtenis inclusion. [!UICONTROL Latency] is ideaal voor pre-/postanalyse. Als u bijvoorbeeld een product of campagne wilt starten en u wilt het gedrag vóór bijhouden en zien hoe het na de introductie functioneert, wordt het gedrag vóór en na de introductie naast elkaar weergegeven in de tabel [!UICONTROL Latency] om de directe invloed te zien. De cellen die al in de tabel [!UICONTROL Latency] zijn opgenomen, worden berekend door gebruikers die voldoen aan de [!UICONTROL Inclusion] -criteria voor de opnemingsperiode en vervolgens voldoen aan de [!UICONTROL Return] -criteria in de perioden vóór de opnemingsperiode. [!UICONTROL Latency] -tabellen en [!UICONTROL Custom Dimension] -cohort kunnen niet samen worden gebruikt.</br><br>**[!UICONTROL Custom Dimension Cohort]**: Maak cohorten op basis van de geselecteerde dimensie in plaats van op tijd gebaseerde cohorts (standaard). Vele klanten willen hun cohorten met iets anders dan tijd analyseren en de nieuwe eigenschap van de Cohort van het Dimension van de Douane biedt u de flexibiliteit om cohorten te bouwen die op afmetingen van hun kiezen worden gebaseerd. Met afmetingen zoals marketingkanaal, campagne, product, pagina, regio of een andere dimensie in Adobe Analytics kunt u zien hoe de retentie verandert op basis van de verschillende waarden van deze dimensies. In de definitie van het Cohort-segment van [!UICONTROL Custom Dimension] wordt het item Dimensie alleen toegepast als onderdeel van de opnemingsperiode, niet als onderdeel van de retourdefinitie.</br><br> na het kiezen van de [!UICONTROL Custom Dimension] optie van de Cohort, kunt u slepen en laten vallen welke afmeting u in de dalingsstreek wilt. Dit staat u toe om gelijkaardige afmetingspunten over de zelfde tijdspanne te vergelijken. U kunt bijvoorbeeld de prestaties van steden naast elkaar vergelijken, producten, campagnes, enzovoort. Het zal uw hoogste 14 afmetingspunten terugkeren. U kunt echter een filter gebruiken (dit filter openen door de muis boven de dimensie te houden die is aangesleept) om alleen gewenste dimensie-items weer te geven. Een [!UICONTROL Custom Dimension] Cohort kan niet worden gebruikt met de functie [!UICONTROL Latency] Tabel. </br> |

1. (Optioneel) Pas de **[!UICONTROL Cohort Table Settings]** aan door op het tandwielpictogram te klikken.

   | Instelling | Beschrijving |
   |--- |--- |
   | Alleen percentages weergeven | Hiermee verwijdert u de getalwaarde en geeft u alleen het percentage weer. |
   | Percentages afronden naar dichtstbijzijnde gehele getal | Rondt de percentagewaarde aan het meest dichtbijgelegen geheel in plaats van het tonen van de decimale waarde. |
   | Gemiddelde procentuele rij tonen | Hiermee voegt u een nieuwe rij boven aan de tabel in en voegt u vervolgens het gemiddelde voor de waarden binnen elke kolom toe. |

## Het rapport [!UICONTROL Cohort Analysis] samenstellen

1. Klik op **[!UICONTROL Build]**.

   ![Stap Resultaat](assets/cohort-report.png)

   In het rapport worden bezoekers weergegeven die een bestelling hebben geplaatst ( *`Included`* kolom) en die tijdens volgende bezoeken zijn teruggekeerd naar uw site. De vermindering van bezoeken in tijd laat u toe om problemen te ontdekken en actie te ondernemen.
1. (Optioneel) Maak een segment van een selectie.

   Selecteer cellen (aangrenzend of niet aangrenzend) en klik vervolgens met de rechtermuisknop > **[!UICONTROL Create Segment From Selection]** .

1. In de [ Bouwer van het Segment ](/help/components/segmentation/segmentation-workflow/seg-build.md), geef verder het segment uit, dan klik **[!UICONTROL Save]**.

   Het opgeslagen segment is beschikbaar voor gebruik in het deelvenster [!UICONTROL Segment] in [!UICONTROL Analysis Workspace] .
1. Geef uw cohortproject een naam en sla het op.
1. (Facultatief) [ Kromme en deel ](/help/analyze/analysis-workspace/curate-share/curate.md) de projectcomponenten.

   >[!NOTE]
   >
   >U moet uw project bewaren alvorens de kromming beschikbaar is.

## Een cohortvisualisatie downloaden

Net als andere visualisaties in Analysis Workspace kunt u een cohortvisualisatie downloaden als een CSV- of PDF-bestand. Voor meer informatie, zie [ PDF of Csv- dossiers van de Download ](/help/analyze/analysis-workspace/curate-share/download-send.md).
