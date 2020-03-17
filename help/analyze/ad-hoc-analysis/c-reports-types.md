---
description: Beschrijvingen van rapporttypen die in Experience Cloud worden gebruikt.
title: Rapporttypen
topic: Ad hoc analysis
uuid: 357102eb-a172-40ec-a302-01c87abaacb5
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Rapporttypen

Beschrijvingen van rapporttypen die in Experience Cloud worden gebruikt.

## Gerangschikte rapporten {#concept_E1710FFFBB334F3D9DB63A1626DBCB01}

Hiermee geeft u een tabel met gerangschikte items weer, waarbij getallen en percentages in cijfers worden gebruikt. Bijvoorbeeld, [!UICONTROL Pages Report] rangschikt a de pagina&#39;s op uw plaats die op verkeer wordt gebaseerd, en de detaillijst toont percentages en aantallen voor metriek zoals de Weergaven van de Pagina en Opbrengst. Een horizontaal staafdiagram is het standaardgrafiektype. In grafieken wordt voor elke meting een kleur weergegeven. De gerangschikte rapporten kunnen veelvoudige metriek in een rapport tonen.

<!-- 

c_reports_ranked.xml

 -->

Willekeurige grafieken zijn standaard vijf items, maar u kunt maximaal dertig items in de grafiekopties opnemen.

## Gedetailleerde rapporten {#concept_65FEA92704024232BB21A5952939711F}

Laat u onderzoeken hoe omzettingen en gebeurtenissen over een geselecteerde tijdgranulariteit (Uur, Dag, Week, Maand, Kwart, of Jaar) tijdens een rapporteringsperiode trenderen.

<!-- 

c_reports_trended.xml

 -->

In de grafiek worden de bijgehouden items weergegeven op de verticale as. Op de horizontale as wordt de tijdgranulariteit weergegeven. In de tabel kunt u een trend volgen vanuit een specifieke cel en een volledig rapport van de cel starten. De gebruikte datum of tijd is gebaseerd op de waarde van de cel.

U kunt ook meerdere cellen selecteren en een trended-rapport starten op basis van een geselecteerde granulariteit. Wanneer u zich van veelvoudige cellen ontwikkelt, tonen de rapportkolommen gegevens voor de volledige rapporteringsperiode.

Een [!UICONTROL Products Report] voorbeeld is een trended rapport. U kunt zien hoeveel omzet een product tijdens de geselecteerde periode maakte. Als uw verslagperiode een week is, kunt u zien hoeveel opbrengst dat product voor elke dag van de tijdspanne produceerde, kunt u een trendgrafiek voor een specifiek product op die dag tonen, of een afzonderlijk trended rapport voor de selectie openen.

## Trend uit cellen {#task_AD9275BED5CE4D61AC25778D144406A4}

Stappen die beschrijven hoe te om een trendrapport van één of meerdere cellen in een lijst te lanceren.

<!-- 

t_trend_row.xml

 -->

**Tendens van cellen**

1. Open een gerangschikt rapport.
1. Zoek in de tabel de cel en klik op **[!UICONTROL Trend]**.

   ![](assets/TrendInspector_Buttcon.png)

1. Klik op een volledig rapport in de cel om het te bekijken. **[!UICONTROL Launch Trend Report]**

   U kunt ook met de rechtermuisknop op de cel klikken en vervolgens op de cel klikken **[!UICONTROL Trend Cell]**. U kunt deze taak ook uitvoeren nadat u meerdere cellen hebt geselecteerd.

## Totalapport {#concept_48E23FB3BCCD43DFB486A048960800A8}

<!-- 

c_reports_totals.xml

 -->

Een verslag op uitvoeringsniveau met cijfers van onderaf. Het bevat gegevens voor totale opbrengst, paginameningen, en orden. U kunt het rapport segmenteren en extra metriek toevoegen om extra gegevens te bekijken.

## Stroomrapporten {#concept_3E417D018F1B4566973F694B01E6439F}

In stroomrapporten worden de meest gangbare paden weergegeven die gebruikers gebruiken voor pagina&#39;s, sitesecties en servers.

<!-- 

c_reports_flow.xml

 -->

**Volgende stroom**

De [!UICONTROL Next Flow] rapportgroep heeft drie rapporten: [!UICONTROL Next Page Flow], [!UICONTROL Next Section Flow], en [!UICONTROL Next Server Flow]. De rapporten in deze groep tonen u de gemeenschappelijkste pagina&#39;s, de plaatssecties, en de servers die een bezoeker na de toegang tot van de pagina, de plaatssectie, of de server betreedde u specificeert. Deze rapporten tonen u de gemeenschappelijkste wegen die door uw website worden genomen.

**Vorige stroom**

Eerdere stroomrapporten zijn vergelijkbaar met de rapporten Volgende stroom, behalve dat u ziet waar bezoekers na een geselecteerde pagina naartoe zijn gegaan en waar bezoekers zijn geweest voordat ze een opgegeven pagina bezoeken. De controles voor het gebruiken van het rapport zijn identiek aan de controles voor de Volgende rapporten van de Stroom.

## Volgende pagina&#39;s {#concept_F7565234927942BEAF75D5D94A7AB47D}

Hiermee geeft u padweergaven weer, of het aantal keren en percentages dat een pagina is weergegeven binnen de beperkingen van de paden. Een pagina met privacybeleid kan bijvoorbeeld in totaal 10.000 paginaweergaven bevatten, maar slechts 500 van deze paginaweergaven vond plaats vlak voor een startpagina. In dit geval worden er 500 padweergaven weergegeven. U kunt het rapport bekijken op het bezoek of bezoekersniveau. De percentages voor elke pagina worden weergegeven naast de naam van de pagina. De breedte van een regel die is verbonden met een pagina, geeft het relatieve percentage van de bezoeken aan.

<!-- 

c_reports_next_page_flow.xml

 -->

Standaard worden in dit rapport de bovenste 10 pagina&#39;s weergegeven die gebruikers hebben gevolgd na de pagina die u hebt geselecteerd. U kunt op elke onderstreepte pagina klikken om de grafiek verder uit te breiden. Het aantal pagina&#39;s in de grafiek is onbeperkt en u kunt de muisaanwijzer boven een pagina houden om de bezoekgegevens en de inkomstengegevens van de pagina te bekijken.

Gebruik dit rapport om:

* Begrijp welke stappen het vaakst na het bekijken van een geselecteerde pagina worden genomen.
* Optimaliseer uw ontwerp van de plaatsweg om uw verkeer aan een gewenste doelpagina te trechter.
* Bepaal waar bezoekers naartoe gaan in plaats van de gewenste doelpagina&#39;s.

## Volgende serverstroom {#concept_DB8C20E18AEA4051903C47A16C0E9C4E}

Hiermee geeft u de navigatiegegevens weer tussen de servers op uw site. Wanneer u een servernaam op uw site selecteert, wordt in het rapport het aantal bezoekers weergegeven dat van die server naar elk van de andere servers op uw site is gegaan tijdens één bezoek of tijdens verschillende bezoeken.

<!-- 

c_reports_next_server_flow.xml

 -->

Bijvoorbeeld, als u specifieke gegevens op verschillende servers hebt of gespiegelde gegevens op afzonderlijke servers hebt, toont het rapport u de weg tussen servers die de gebruikers raken. Dit geldt ook voor domeinen binnen uw website. U kunt bijvoorbeeld zien hoeveel gebruikers van een `https://www.mysite.com` naar `https://info.mysite.com` of `https://sales.mysite.com`.

## Volgende sectie {#concept_7C9C8567E7DF477DA186E47DD3FD47A4}

Het [!UICONTROL Next Section Flow] verslag lijkt op het [!UICONTROL Next Page Flow] verslag. Er worden gegevens weergegeven voor sitesecties (groepen gerelateerde webpagina&#39;s). Als een pagina in meer dan één plaatssectie bevat is, toont het rapport gegevens voor alle plaatssecties.

<!-- 

c_reports_next_section_flow.xml

 -->

Een online detailhandelaar kan bijvoorbeeld sitesecties voor zijn producten en sitesecties voor productmerken hebben. In dit geval kan een productwebpagina onder meerdere zichtsecties vallen. Hoewel een productpagina slechts één keer is bekeken, geeft het [!UICONTROL Next Section Flow] rapport een paginaweergave weer voor elke zichtsectie die aan de pagina is gekoppeld.

## Vorige paginastroom {#concept_ADEAEBAE3F37401B977A27E03B5A523B}

Vergelijkbaar met het [!UICONTROL Next Page Flow] verslag. Het [!UICONTROL Previous Page Flow] rapport bevat meerdere niveaus van de populairste pagina&#39;s die uw bezoekers vóór de geselecteerde pagina bekijken. Het rapport markeert ook pagina&#39;s van waaruit bezoekers uw site betreden.

<!-- 

c_reports_previous_page_flow.xml

 -->

Gebruik dit rapport om:

* Begrijp welke stappen het vaakst worden genomen alvorens een geselecteerde pagina te bekijken.
* Optimaliseer uw ontwerp van de plaatsweg om uw verkeer aan een gewenste doelpagina te trechter.

## Vorige sectie {#concept_30688D97B48449E1958866BAF376FA8C}

Het [!UICONTROL Previous Section Flow] verslag lijkt op het [!UICONTROL Previous Page Flow] verslag. Er worden gegevens weergegeven voor sitesecties (groepen gerelateerde webpagina&#39;s). Als een pagina in meer dan één plaatssectie bevat is, dan toont het rapport gegevens voor alle plaatssecties.

<!-- 

c_reports_previous_section_flow.xml

 -->

Een online detailhandelaar kan bijvoorbeeld sitesecties voor zijn producten en sitesecties voor productmerken hebben. In dit geval kan een productwebpagina onder meerdere zichtsecties vallen. Hoewel een productpagina slechts één keer is bekeken, geeft het [!UICONTROL Previous Section Flow] rapport een paginaweergave weer voor elke zichtsectie die aan de pagina is gekoppeld.

## Vorige serverstroom {#concept_8E43208CAF2C4C358F19D4669B73822F}

Dit rapport geeft u navigatiegegevens weer tussen servers op uw site. Wanneer u een servernaam op uw site selecteert, wordt in het rapport het aantal bezoekers weergegeven dat van elk van de andere servers op uw site naar die server is gegaan tijdens één bezoek of tijdens verschillende bezoeken.

<!-- 

c_reports_previous_server_flow.xml

 -->

Bijvoorbeeld, als u specifieke gegevens op verschillende servers hebt of gespiegelde gegevens op afzonderlijke servers hebt, toont het rapport u de weg tussen servers die de gebruikers raken. Dit geldt ook voor domeinen binnen uw website. U kunt bijvoorbeeld zien hoeveel gebruikers van een `www.mysite.com` naar `info.mysite.com` of `sales.mysite.com`.

## Conversietrechter-rapporten {#concept_35A2EB61E84441CBB670C2E02CA26F81}

Conversie de rapporten van het Kanaal van de Omzetting tonen omzettingspercentages tussen specifieke metrische gebeurtenissen. U kunt dit rapport gebruiken om het aantal klikcontroles te begrijpen die verkoop, en het aantal verkochte eenheden produceren. Bijvoorbeeld, toont een [!UICONTROL Products Conversion] rapport het percentage gebeurtenissen van Kaarten met betrekking tot de gebeurtenissen van Bezoekingen, en toont dan totalen voor Orders, Inkomsten, en Eenheden die op die gebeurtenissen worden gebaseerd.

<!-- 

c_reports_conversion_funnel.xml

 -->

De volgende rapporten over de trechter zijn beschikbaar:

* [!UICONTROL Purchase Conversion Funnel]: Toont bezoeken (rapport-specifiek), Houtskaarten, orden, Eenheden, en Ontvangsten.
* [!UICONTROL Cart Conversion Funnel]: Hiermee geeft u bezoeken (rapportspecifiek), kaarten, kassa&#39;s, bestellingen en inkomsten weer.
* [!UICONTROL Custom Event Funnel]: Hiermee geeft u aangepaste gebeurtenissen op uw site weer. Aangepaste gebeurtenissen 1-5 worden standaard weergegeven.
* [!UICONTROL Campaign Conversion Funnel]: Toont klikdoorhalingen, Checkouts, Orders, en Inkomsten.

De rapportlijst toont statistieken voor gemiddelde verkoop per klik-door, en gemiddelde eenheden verkocht per klik-door. U kunt metriek en douanegebeurtenissen van andere rapporteringsgroepen aan deze rapporten toevoegen. Deze kanalen hebben veel gelijkenissen, maar zijn gebaseerd op verschillende variabelen en gebeurtenissen. U kunt deze rapporten gebruiken om te zien welke percentages en algemene tendensen van gebruikers specifieke gebeurtenissen in brand steken u specificeert. U kunt zien waar de gebruikers niet door aan gebeurtenissen volgen, die inzicht aan dat specifieke punt in het omzettingsproces verstrekken.

## Rapport voor siteanalyse {#concept_65694C6BDE424714B7975764F95497A4}

[!UICONTROL Site Analysis] geeft weer hoe bezoekers door opgegeven pagina&#39;s en gebeurtenissen bladeren. U kunt bijvoorbeeld de verkeersstroom tussen pagina&#39;s zien, de affiniteit tussen producten en marketingkanalen en de manier waarop campagnes en kanalen naar productorders stromen. U kunt pagina&#39;s, dimensiepunten (en lijsten), en metrische gebeurtenissen slepen. Elke cilinder vertegenwoordigt één of meerdere afmetingspunten (pagina&#39;s) of een gebeurtenis. Pijlen geven de stroom tussen de cilinderwaarden aan. De metriek worden toegewezen aan cilinderposities (X en Y), cilinderbreedte, cilinderhoogte en kleur. De positie, grootte en kleur veranderen afhankelijk van de metrische waarden.

<!-- 

c_reports_site_analysis.xml

 -->

Sleep items van gereedschapsvensters om deze toe te voegen aan de grafiek of het veld Dimensies.

Klik met de rechtermuisknop op cilinders om deze te bewerken of te verwijderen.

<!-- Meike, UICONTROL and DNL stripped from tables. Re-add. -->

| Option | Beschrijving |
|--- |--- |
| Site-analyse tonen bij (bezoek of bezoeker) | Hiermee kunt u schakelen tussen Bezoek en Bezoeker om het plakken van bezoekers te analyseren. Met deze instellingen kunt u de betrokkenheid van bezoekers op bezoekersniveau en bij verschillende bezoeken begrijpen. De rapporten van de Analyse van de plaats, Stroom, en van de Vallout worden toegelaten voor bezoekerspatie. Als u deze instelling wijzigt, wordt het rapport opnieuw uitgevoerd en blijven de gegevens beperkt tot de selectie. |
| Controlepunt toevoegen | Hiermee geeft u de Checkpoint Editor weer, waarin u afmetingen of gebeurtenissen kunt selecteren die u aan de weergave wilt toevoegen. |
| Diagram vervangen | Vervangt het diagram van de Analyse van de Plaats met de controlepunten u aan de redacteur toevoegt. |
| Aanpassen aan scherm | Hiermee herstelt u de oorspronkelijke weergave van een diagram. |
| Luchtweergave | Verstrekt een onderaan mening van de grafiek. |
| Raster schakelen | Hiermee schakelt u het raster in of uit. |
| Dimensie | Het item waarop u rapporteert. Sleep het item vanuit Afmetingen. |

| Option | Beschrijving |
|--- |--- |
| Bewerken | Hiermee kunt u pagina&#39;s aan een cilinder toevoegen of eruit verwijderen. |
| Verwijderen | Hiermee kunt u een cilinder verwijderen. |
| Rapporten | Laat u een ander rapport van de cilinder lanceren. |
| Diagram opslaan als | Hiermee kunt u het diagram opslaan als .png of .jpg. Als u de diagrambesturingselementen (grafiekhoek, grootte) wijzigt voordat u het bestand opslaat, blijven de wijzigingen behouden in de uitvoer. |
| Diagram kopiëren naar klembord | Hiermee kopieert u het diagram voor plakken naar een andere toepassing. Als u de diagrambesturingselementen (grafiekhoek, grootte) wijzigt voordat u het bestand opslaat, blijven de wijzigingen behouden in de uitvoer. |
