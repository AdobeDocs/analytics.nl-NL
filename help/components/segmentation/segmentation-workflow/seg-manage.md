---
description: In Segmentbeheer kunt u op verschillende manieren segmenten curven, zoals delen, filteren, labelen, goedkeuren, kopiëren, verwijderen en markeren als favorieten.
title: Segmenten beheren (Segmentbeheer)
feature: Segmentation
exl-id: be182a55-23cb-415f-a7d0-3c1efeead1a1
source-git-commit: 8e8f59f747ddacc5462cbc177d199a5e0e91908a
workflow-type: tm+mt
source-wordcount: '924'
ht-degree: 0%

---

# Segmentbeheer

In Segmentbeheer kunt u op verschillende manieren segmenten curven, zoals delen, filteren, labelen, goedkeuren, kopiëren, verwijderen en markeren als favorieten.

De manager van het Segment van Analytics toont u alle segmenten u bezit en die met u zijn gedeeld. Gebruikers op beheerniveau kunnen alle segmenten in de organisatie zien. Dit overzicht bevat de gebruikersinterface en de mogelijkheden van Segmentbeheer.

![ de manager van Segmenten ](assets/segments-manager.png)

## Toegang tot Segmentbeheer

1. Selecteer in Adobe Analytics de tab **[!UICONTROL Components]** en selecteer vervolgens **[!UICONTROL Segments]** .

   of

   In een bestaand rapport, selecteer het pictogram van Segmenten ![ ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Segmentation_18_N.svg) in de linkernavigatie, dan uitgezochte **[!UICONTROL Manage]**.

## Beschikbare handelingen in Segmentbeheer

In Segmentbeheer kunt u:

* [Filtersegmenten](/help/components/segmentation/segmentation-workflow/t-seg-filter.md)

* [Segmenten markeren als favorieten](/help/components/segmentation/segmentation-workflow/t-seg-favorite.md)

* [Segmenten goedkeuren](/help/components/segmentation/segmentation-workflow/seg-approve.md)

* [Tagsegmenten](/help/components/segmentation/segmentation-workflow/seg-tag.md)

* [Segmenten delen](/help/components/segmentation/segmentation-workflow/t-seg-share.md)

* Een segment exporteren naar een CSV-bestand.

* [Segmenten kopiëren](/help/components/segmentation/segmentation-workflow/seg-copy.md)

* [Segmenten verwijderen](/help/components/segmentation/segmentation-workflow/seg-delete.md)

## Kolommen configureren

U kunt de informatie vormen die voor elk segment in de Manager van het Segment wordt getoond door de kolommen te vormen die worden getoond.

De zichtbare kolommen configureren in Segmentbeheer:

1. Selecteer in Adobe Analytics de tab **[!UICONTROL Components]** en selecteer vervolgens **[!UICONTROL Segments]** .

1. In de Manager van het Segment, selecteer **aanpassen kolommen** pictogram ![ aanpassen kolompictogram ](assets/customize-columns-icon.png), dan selecteer de kolommen die u in de Manager van het Segment wilt worden getoond.

   De volgende kolommen zijn beschikbaar:

   | Kolomtitel | Beschrijving |
   |---|---|
   | Titel en beschrijving | Deze waarden worden verstrekt in de bouwer van het Segment. Als u de titel en beschrijving wilt bewerken, selecteert u de titelkoppeling om de Segment Builder te openen. |
   | Favorieten | Hiermee geeft u sterpictogrammen weer naast elk segment, zodat u segmenten kunt markeren als favorieten. Voor meer informatie, zie [ segmenten van het Teken als favorieten ](/help/components/segmentation/segmentation-workflow/t-seg-favorite.md). |
   | Reeksen rapporteren | Deze kolom geeft aan in welke rapportsuite het segment het laatst is opgeslagen. |
   | Eigenaar | Geeft aan wie eigenaar is van het segment. Als niet-beheerder, kunt u slechts segmenten zien u bezit of die met u werden gedeeld. |
   | Labels (niet gecontroleerd in kolomkiezer, vandaar dat de kolom niet wordt weergegeven) | Tags die op het segment zijn toegepast, door u of door personen die het segment met u hebben gedeeld. |
   | Gedeeld met | Hier worden personen of groepen weergegeven (alleen Admin) of Alle personen (alleen Admin) waarmee u het segment hebt gedeeld. <p>Wanneer een segment door u of met u wordt gedeeld, toont een aandeelpictogram naast de segmentnaam.</p> |
   | Datum gewijzigd | Hiermee geeft u de datum weer waarop het segment voor het laatst is gewijzigd. |
   | Gebruikt in | Hiermee kunt u zien waar segmenten momenteel worden gebruikt en hoe vaak deze in elk gebied worden gebruikt. <p>Bijvoorbeeld, als het segment in 40 projecten en 2 alarm wordt gebruikt, dan toont de waarde van deze kolom als [!UICONTROL **42 componenten**].</p> <p>Selecteer de waarde in deze kolom om de uitsplitsing te zien van waar de segmenten (bijvoorbeeld, [!UICONTROL **Projecten (40)**] worden gebruikt, [!UICONTROL **Alarm (2)**]). Bovendien kunt u de lijst met items weergeven waarin de segmenten worden gebruikt. Bijvoorbeeld, zie zo de lijst van projecten waar zij worden gebruikt, selecteer de [!UICONTROL **Projecten (40)**] verbinding.</p><p>Elk van de volgende gebieden toont het aantal instanties van segmenten die in dat gebied worden gebruikt:</p>  <ul><li>[!UICONTROL **Projecten**]<p>Bevat segmenten die [ in de segmentbouwer ](/help/components/segmentation/segmentation-workflow/seg-build.md) werden gecreeerd en voor alle projecten beschikbaar zijn.</p></li><li>[!UICONTROL **Ad hoc componenten**]<p>Bevat segmenten die [ als snelle segmenten ](/help/analyze/analysis-workspace/components/segments/quick-segments.md) werden gecreeerd en beschikbaar slechts binnen één enkel project zijn.</p></li><li>[!UICONTROL **Geplande projecten**]</li><li>[!UICONTROL **Mobiele Scorecards**]</li><li>[!UICONTROL **Annotaties**]</li><li>[!UICONTROL **Waarschuwingen**]</li><li>[!UICONTROL **Berekende standaarden**]</li><li>[!UICONTROL **Report Builder**]<p>Als u deze optie selecteert, wordt een CSV-bestand gedownload met de volgende kolommen gegevens:</p><ul><li>Naam Report Builder</li><li>Laatst geopend</li><li>Laatst geopende IMS-gebruikersnaam</li><li>Laatst geopende gebruikersnaam</li></ul><p>Wanneer u informatie voor Report Builder bekijkt, zijn de gebruiksgegevens beschikbaar vanaf september 2024.</p></li></ul><p>Deze informatie kan u helpen bepalen of een component voor gebruikers in uw organisatie waardevol is, waar het wordt gebruikt, en of het moet worden geschrapt of worden gewijzigd.</p><p>Houd rekening met het volgende wanneer u deze kolom weergeeft:</p><ul><li>Deze informatie is alleen beschikbaar voor systeembeheerders.</li><li>[!UICONTROL **Gebruikt in**] kolom toont niet door gebrek. [ vorm kolommen ](#configure-columns) om het te tonen.</li><li>Als een segment een ander segment in zijn definitie omvat, wordt om het even welk gebruik van dat segment niet getoond in [!UICONTROL **Gebruikt in**] kolom. Als een segment in de definitie van een ander type van component (zoals berekend metrisch) inbegrepen is, dan wordt het gebruik getoond in [!UICONTROL **Gebruikt in**] kolom.</li><li>Deze informatie omvat geen gebruik van de API of Data Warehouse.</li><li>Als er geen gegevens in deze kolom voor een bepaalde component zijn maar het heeft a [!UICONTROL **laatst gebruikte**] datum, zou de component in een analyse kunnen worden gebruikt zonder worden bewaard.</li><li>Gebruiksgegevens zijn beschikbaar vanaf september 2023.</li></ul><p>U kunt het [ Woordenboek van Gegevens ](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) samen met deze informatie gebruiken om u spoor van te houden en beter te begrijpen hoe de componenten in uw organisatie worden gebruikt.</p> |
   | Laatst gebruikt | Hiermee geeft u de datum weer waarop het segment voor het laatst is gebruikt in een van de volgende componenttypen: <ul><li>Waarschuwingen</li><li>Berekende cijfers</li><li>Projecten</li><li>Geplande projecten</li><li>Segmenten</li></ul> <p>Deze informatie kan u helpen bepalen of een component voor gebruikers in uw organisatie waardevol is, waar het wordt gebruikt, en of het moet worden geschrapt of worden gewijzigd.</p><p>Houd rekening met het volgende wanneer u deze kolom weergeeft:</p><ul><li>Deze informatie omvat geen gebruik van API, Report Builder, of Data Warehouse.</li><li>Voor sommige componenten bevat deze kolom mogelijk geen gegevens als de component voor het laatst is gebruikt vóór september 2023.</li><li>Deze informatie is alleen beschikbaar voor systeembeheerders.</li></ul><p>U kunt het [ Woordenboek van Gegevens ](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) samen met deze informatie gebruiken om u spoor van te houden en beter te begrijpen hoe de componenten in uw organisatie worden gebruikt. |

   {style="table-layout:auto"}

## Hoe kan ik-video {#section_B3C5DA22DC5248DBA17C56E03DA2D4F2}

Deze [ video van Adobe Analytics ](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/components/segmentation/segment-management-and-sharing.html?lang=nl-NL) geeft een kort overzicht van hoe te om de Manager van het Segment te gebruiken.


