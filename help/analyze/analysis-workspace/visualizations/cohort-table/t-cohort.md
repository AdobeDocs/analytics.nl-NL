---
description: Creeer een cohort en stel een rapport van de cohortanalyse in de Werkruimte van de Analyse in werking.
keywords: Analysis Workspace
title: Een cohortanalyserapport uitvoeren
topic: Reports and analytics
uuid: 5574230f-8f35-43ea-88d6-cb4960ff0bf4
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Een rapport Cohortanalyse configureren

Creeer een cohort en stel een rapport van de cohortanalyse in de Werkruimte van de Analyse in werking.

1. Klik in de analysewerkruimte op het **[!UICONTROL Visualizations]** pictogram in de linkerrails en sleep een item **[!UICONTROL Cohort Table]** naar het canvas.

   ![](assets/cohort-table.png)

1. Definieer de waarden **[!UICONTROL Inclusion Criteria]**, **[!UICONTROL Return Criteria]**, **[!UICONTROL Cohort Type]** en **[!UICONTROL Settings]** zoals gedefinieerd in de onderstaande tabel.

| Element | Beschrijving |
|--- |--- |
| **[!UICONTROL Inclusion Criteria]** | U kunt maximaal 10 inclusiesegmenten en maximaal 3 inclusiemetriek toepassen. Met de metrische waarde wordt opgegeven wat een gebruiker in een cohort plaatst. Bijvoorbeeld, als inclusiemetrisch Orden is, slechts zullen de gebruikers die een orde tijdens de tijdwaaier van de cohortanalyse plaatsten in de aanvankelijke cohort worden omvat.<br>De standaardoperator tussen metriek is AND, maar u kunt deze wijzigen in OR. Bovendien kunt u numerieke filters toevoegen aan deze cijfers. Bijvoorbeeld: &quot;Visit >= 1&quot;.</br> |
| **[!UICONTROL Return Criteria]** | U kunt tot 10 terugkeersegmenten en tot 3 terugkeermetriek toepassen. Metrisch wijst erop of de gebruiker (behoud) of niet (klusje) is behouden. Als de retourwaarde bijvoorbeeld Video-weergaven is, worden alleen gebruikers die video&#39;s tijdens volgende tijdsperioden (na de periode waarin ze aan een cohort zijn toegevoegd) weergegeven als behouden. Een andere maatstaf die retentie kwantificeert, zijn Bezoekingen. |
| **[!UICONTROL Granularity]** | De tijdsgranulariteit van Dag, Week, Maand, Kwart, of Jaar. |
| **[!UICONTROL Type]** | **[!UICONTROL Retention]**(standaard): Met een retentiecohort wordt gemeten hoe goed de bezoekerscohorten in de loop der tijd naar uw eigenschap terugkeren. Dit is het standaardcohort dat we altijd hebben gehad en dat het gedrag van gebruikers weergeeft en herhaalt. Een retentiecohort wordt aangegeven door de kleur groen in de tabel.<br>**[!UICONTROL Churn]**: Een churn (ook wel &#39;kenmerk&#39; of &#39;fallout&#39; genoemd) cohort meet hoe uw bezoekerscohorten in de loop der tijd uit uw eigendom vallen. Churn = 1 - Behoud. Churn is een goede maatstaf voor kleverigheid en kansen door u te laten zien hoe vaak klanten niet terugkomen. U kunt churn gebruiken om aandachtsgebieden te analyseren en te identificeren: Welke cohortsegmenten kunnen enige aandacht krijgen. Een kleurcohort wordt aangegeven door de kleur rood in de tabel (vergelijkbaar met fallout in onze **[!UICONTROL Flow]** visualisatie).</br> |
| **[!UICONTROL Settings]** | **[!UICONTROL Rolling Calculation]**: Bereken het behoud of de kromme op de vorige kolom, eerder dan de Included kolom (gebrek) wordt gebaseerd. Bij Rolling Berekening wordt de berekeningsmethode voor de retourperioden gewijzigd. Bij de normale berekening zijn onafhankelijke gebruikers betrokken die aan de &quot;return&quot;-criteria voldoen en deel uitmaakten van de opnemingsperiode, ongeacht of zij al dan niet in het cohort voor de voorgaande periode waren opgenomen. In plaats daarvan vindt Rolling Berekening gebruikers die aan &quot;terugkeercriteria&quot;voldoen en deel van de vorige periode uitmaakten. Daarom worden met behulp van rolberekeningen filters en treinen de gebruikers gefilterd die gedurende een bepaalde periode voortdurend voldoen aan de criteria voor &quot;return&quot;. Retourcriteria worden toegepast op elk van de perioden tot aan de geselecteerde periode. </br><br>**[!UICONTROL Latency Table]**: Een latentietabel meet de tijd die is verstreken voor en na de opnemingsgebeurtenis. Latentie is erg handig voor pre-/postanalyse. Als u bijvoorbeeld een product of campagne wilt starten en u wilt het gedrag vóór bijhouden en zien hoe het na de introductie functioneert, wordt het gedrag vóór en na de introductie naast elkaar weergegeven om de directe impact te zien. De cellen vóór opname in de Latentie-tabel worden berekend door gebruikers die voldoen aan de criteria voor &quot;opname&quot; voor de opnemingsperiode en vervolgens voldoen aan de criteria voor &quot;terugkeer&quot; in de perioden vóór de opnemingsperiode. Latentietabellen en aangepaste Dimension-cohort kunnen niet samen worden gebruikt.</br><br>**[!UICONTROL Custom Dimension Cohort]**: Maak cohorten op basis van de geselecteerde dimensie in plaats van op tijd gebaseerde cohorts (standaard). Veel klanten willen hun cohorten met iets anders dan tijd analyseren en de nieuwe functie Aangepaste Dimension Cohort biedt u de flexibiliteit om cohorten te maken op basis van de afmetingen die ze kiezen. Gebruik dimensies zoals marketingkanaal, campagne, product, pagina, regio of een andere dimensie in Adobe Analytics om te tonen hoe de retentie verandert op basis van de verschillende waarden van deze dimensies. De definitie van het segment Dimensie van aangepaste cohort past de dimensie-item alleen toe als onderdeel van de opnemingsperiode, niet als onderdeel van de terugkeerdefinitie.</br><br>Nadat u de optie Aangepaste afmetingskleur hebt gekozen, kunt u de gewenste afmeting naar de neerzetzone slepen. Dit staat u toe om gelijkaardige afmetingspunten over de zelfde tijdspanne te vergelijken. U kunt bijvoorbeeld de prestaties van steden naast elkaar vergelijken, producten, campagnes, enzovoort. Het zal uw hoogste 14 afmetingspunten terugkeren. U kunt echter een filter gebruiken (dit filter openen door de muis boven de dimensie te houden die is aangesleept) om alleen gewenste dimensie-items weer te geven. Een aangepaste Dimension-cohort kan niet worden gebruikt met de functie Latentietabel.</br> |

1. Pas het gereedschap aan **[!UICONTROL Cohort Table Settings]** door op het tandwielpictogram te klikken.

| Instelling| Beschrijving|| Alleen percentage weergeven| Hiermee verwijdert u de getalwaarde en geeft u alleen het percentage weer. || Percentage afgerond op het dichtstbijzijnde gehele getal| Rondt de percentagewaarde aan het meest dichtbijgelegen geheel in plaats van het tonen van de decimale waarde. || Gemiddelde procentuele rij tonen| Hiermee voegt u een nieuwe rij boven aan de tabel in en voegt u vervolgens het gemiddelde voor de waarden binnen elke kolom toe. |

## Het rapport Cohort Analysis samenstellen

1. Klik op **[!UICONTROL Build]**.

   ![Stap resultaat](assets/cohort-report.png)

   In het rapport worden bezoekers weergegeven die een bestelling hebben geplaatst ( *`Included`* kolom) en die bij volgende bezoeken zijn teruggekeerd naar uw site. De vermindering van bezoeken in tijd laat u toe om problemen te ontdekken en actie te ondernemen.
1. (Optioneel) Maak een segment van een selectie.

   Selecteer cellen (aangrenzend of niet aangrenzend) en klik vervolgens met de rechtermuisknop > **[!UICONTROL Create Segment From Selection]**.

1. In de Bouwer [van het](https://marketing.adobe.com/resources/help/en_US/analytics/segment/seg_build.html)Segment, geef verder het segment uit, dan klik **[!UICONTROL Save]**.

   Het opgeslagen segment is beschikbaar voor gebruik in het [!UICONTROL Segment] deelvenster in de analysewerkruimte.
1. Geef uw cohortproject een naam en sla het op.
1. (Optioneel) [Curate and share](/help/analyze/analysis-workspace/curate-share/curate.md) the project components.

   >[!NOTE]
   >
   >U moet uw project bewaren alvorens de kromming beschikbaar is.

