---
description: Maak een cohort en voer een rapport voor cohortanalyse uit in Analysis Workspace.
keywords: Analysis Workspace
title: Een cohortanalyserapport uitvoeren
feature: Cohort Analysis
role: User, Admin
exl-id: 523e6f62-b428-454b-9460-6b06e96742c3
source-git-commit: 10ae8213b8745439ab5968853f655a1176b8c38a
workflow-type: tm+mt
source-wordcount: '881'
ht-degree: 0%

---

# Een [!UICONTROL Cohort Analysis] verslag

Een cohort maken en een [!UICONTROL Cohort Analysis] melden in Analysis Workspace.

1. Klik in Analysis Workspace op de knop **[!UICONTROL Visualizations]** pictogram in linkerspoor en sleep een **[!UICONTROL Cohort Table]** naar het canvas.

   ![](assets/cohort-table.png)

1. Definieer de **[!UICONTROL Inclusion Criteria]**, **[!UICONTROL Return Criteria]**, **[!UICONTROL Cohort Type]**, en **[!UICONTROL Settings]** zoals gedefinieerd in de onderstaande tabel.

| Element | Beschrijving |
|--- |--- |
| **[!UICONTROL Inclusion Criteria]** | U kunt maximaal 10 inclusiesegmenten en maximaal 3 inclusiemetriek toepassen. Met de metrische waarde wordt opgegeven wat een gebruiker in een cohort plaatst. Bijvoorbeeld, als inclusiemetrisch Orden is, slechts zullen de gebruikers die een orde tijdens de tijdwaaier van de cohortanalyse plaatsten in de aanvankelijke cohort worden omvat.<br>De standaardoperator tussen metriek is AND, maar u kunt deze wijzigen in OR. Bovendien kunt u numerieke filters toevoegen aan deze cijfers. Bijvoorbeeld: &quot;Visit >= 1&quot;.</br> |
| **[!UICONTROL Return Criteria]** | U kunt tot 10 terugkeersegmenten en tot 3 terugkeermetriek toepassen. Metrisch wijst erop of de gebruiker (behoud) of niet (klusje) is behouden. Als de retourwaarde bijvoorbeeld Video-weergaven is, worden alleen gebruikers die video&#39;s tijdens volgende tijdsperioden (na de periode waarin ze aan een cohort zijn toegevoegd) weergegeven als behouden. Een andere maatstaf die retentie kwantificeert, zijn Bezoekingen. |
| **[!UICONTROL Granularity]** | De tijdsgranulariteit van Dag, Week, Maand, Kwart, of Jaar. |
| **[!UICONTROL Type]** | **[!UICONTROL Retention]**(standaard): Met een retentiecohort wordt gemeten hoe goed de bezoekerscohorten in de loop der tijd naar uw eigenschap terugkeren. Dit is het standaardcohort dat we altijd hebben gehad en dat het gedrag van gebruikers weergeeft en herhaalt. A [!UICONTROL Retention] De kleur wordt aangegeven door de kleur groen in de tabel.<br>**[!UICONTROL Churn]**: Een churn (ook wel &#39;kenmerk&#39; of &#39;fallout&#39; genoemd) cohort meet hoe uw bezoekerscohorten in de loop der tijd uit uw eigendom vallen. Churn = 1 - Behoud. [!UICONTROL Churn] Dit is een goede maatstaf voor zelfgenoegzaamheid en mogelijkheden door u te laten zien hoe vaak klanten niet terugkomen. U kunt churn gebruiken om aandachtsgebieden te analyseren en te identificeren: Welke cohortsegmenten kunnen enige aandacht krijgen. A [!UICONTROL Churn] Cohort wordt aangegeven door de kleur rood in de tabel (vergelijkbaar met fallout in onze **[!UICONTROL Flow]**visualisatie).</br> |
| **[!UICONTROL Settings]** | **[!UICONTROL Rolling Calculation]**: Bereken het behoud of de kromme op de vorige kolom, eerder dan de Included kolom (gebrek) wordt gebaseerd. [!UICONTROL Rolling Calculation] Hiermee wijzigt u de berekeningsmethode voor uw &quot;return&quot;-periodes. Bij de normale berekening zijn onafhankelijke gebruikers betrokken die aan de &quot;return&quot;-criteria voldoen en deel uitmaakten van de opnemingsperiode, ongeacht of zij al dan niet in het cohort voor de voorgaande periode waren opgenomen. In plaats daarvan, [!UICONTROL Rolling Calculation] zoekt gebruikers die voldoen aan de &quot; terugkeercriteria &quot; en deel uitmaakten van de vorige periode . Daarom [!UICONTROL Rolling Calculation] filters en treinen de gebruikers die voortdurend voldoen aan de periode van de &quot;terugkeercriteria&quot;. [!UICONTROL Return] criteria worden toegepast op elk van de perioden die tot de geselecteerde periode leiden. </br><br>**[!UICONTROL Latency Table]**: A [!UICONTROL Latency] de tabel geeft de tijd aan die is verstreken vóór en na de opnemingsgebeurtenis . [!UICONTROL Latency] is erg handig voor pre-/postanalyse. Als u bijvoorbeeld een product of campagne wilt starten en u wilt het gedrag vóór bijhouden en bekijken hoe het na de introductie functioneert, kunt u het volgende doen: [!UICONTROL Latency] in de tabel wordt het gedrag vóór en na de transactie naast elkaar weergegeven om de directe impact te zien . De pre-inclusiecellen in de [!UICONTROL Latency] De tabel wordt berekend door gebruikers die voldoen aan de [!UICONTROL Inclusion] criteria voor de opnemingsperiode en voldoen vervolgens aan de criteria voor [!UICONTROL Return] criteria in de perioden vóór de opnemingsperiode. Let op: [!UICONTROL Latency] tabellen en [!UICONTROL Custom Dimension] Cohort kan niet samen worden gebruikt.</br><br>**[!UICONTROL Custom Dimension Cohort]**: Maak cohorten op basis van de geselecteerde dimensie in plaats van op tijd gebaseerde cohorts (standaard). Veel klanten willen hun cohorten met iets anders dan tijd analyseren en de nieuwe functie van de Cohort van de Dimension van de Douane biedt u de flexibiliteit om cohorten te bouwen die op afmetingen van hun kiezen worden gebaseerd. Met afmetingen zoals marketingkanaal, campagne, product, pagina, regio of een andere dimensie in Adobe Analytics kunt u zien hoe de retentie verandert op basis van de verschillende waarden van deze dimensies. De [!UICONTROL Custom Dimension] Bij de definitie van het cohortensegment wordt de dimensie-item alleen toegepast als onderdeel van de opnemingsperiode, niet als onderdeel van de terugkeerdefinitie.</br><br>Na het kiezen van [!UICONTROL Custom Dimension] Met de optie Cohort kunt u elke gewenste afmeting naar de neerzetzone slepen. Dit staat u toe om gelijkaardige afmetingspunten over de zelfde tijdspanne te vergelijken. U kunt bijvoorbeeld de prestaties van steden naast elkaar vergelijken, producten, campagnes, enzovoort. Het zal uw hoogste 14 afmetingspunten terugkeren. U kunt echter een filter gebruiken (dit filter openen door de muis boven de dimensie te houden die is aangesleept) om alleen gewenste dimensie-items weer te geven. A [!UICONTROL Custom Dimension] Cohort kan niet worden gebruikt met de [!UICONTROL Latency] Tabelfunctie.</br> |

1. Pas de **[!UICONTROL Cohort Table Settings]** door op het tandwielpictogram te klikken.

| Instelling | Beschrijving | | Alleen percentage weergeven | Hiermee verwijdert u de getalwaarde en geeft u alleen het percentage weer. | | Percentage afgerond op het dichtstbijzijnde gehele getal | Rondt de percentagewaarde aan het meest dichtbijgelegen geheel in plaats van het tonen van de decimale waarde. | | Gemiddelde procentuele rij tonen | Hiermee voegt u een nieuwe rij boven aan de tabel in en voegt u vervolgens het gemiddelde voor de waarden binnen elke kolom toe. |

## De [!UICONTROL Cohort Analysis] verslag

1. Klik op **[!UICONTROL Build]**.

   ![Stap Resultaat](assets/cohort-report.png)

   In het rapport worden bezoekers getoond die een bestelling hebben geplaatst ( *`Included`* en die bij volgende bezoeken naar uw site zijn teruggekeerd. De vermindering van bezoeken in tijd laat u toe om problemen te ontdekken en actie te ondernemen.
1. (Optioneel) Maak een segment van een selectie.

   Selecteer cellen (aaneengesloten of niet-aaneengesloten) en klik met de rechtermuisknop > **[!UICONTROL Create Segment From Selection]**.

1. In de [Segment Builder](/help/components/segmentation/segmentation-workflow/seg-build.md), bewerkt u het segment verder en klikt u op **[!UICONTROL Save]**.

   Het opgeslagen segment is beschikbaar voor gebruik in het dialoogvenster [!UICONTROL Segment] in [!UICONTROL Analysis Workspace].
1. Geef uw cohortproject een naam en sla het op.
1. (Optioneel) [Curven en delen](/help/analyze/analysis-workspace/curate-share/curate.md) de projectcomponenten.

   >[!NOTE]
   >
   >U moet uw project bewaren alvorens de kromming beschikbaar is.
