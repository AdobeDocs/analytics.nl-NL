---
title: Dynamische versus statische dimensie-items in vrije-vormtabellen
description: Hoe te met dynamische en statische afmetingspunten in lijsten in wisselwerking te staan.
feature: Freeform Tables
role: User, Admin
exl-id: 4cdc93b5-67ed-46a4-ba9f-a96e640da9d9
source-git-commit: 7f5fca4f7c3641d47e5d1d929a196d5e380c1e6b
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 0%

---

# Dynamische versus statische dimensie-items in vrije-vormtabellen

In Freeform-tabellen kunnen de rijen en kolommen verschillende componentwaarden bevatten. Deze waarden kunnen dynamisch (verandering met tijd) of statisch (veranderen niet met tijd) zijn, afhankelijk van de analyse die u wilt bouwen.

## Dynamische dimensie-items

De dynamische afmetingspunten veranderen met tijd en zijn afhankelijk van metrisch die door in de vrije vormlijst wordt gesorteerd. Items met een dynamische dimensie hebben de voorkeur wanneer u de bovenste items gedurende een bepaalde tijdsperiode wilt analyseren.

Wanneer u een dimensie in een vrije vormlijst laat vallen, zijn de dynamische rijen teruggekeerd. Zij vertegenwoordigen de hoogste punten die aan de afmeting voor een bepaalde metrisch en tijdspanne beantwoorden. U kunt ook een dimensie neerzetten in vrije tabelkolommen en de dimensie wordt automatisch uitgebreid naar de bovenste 5 dimensieitems.

Als u bijvoorbeeld de afmetingen Browsertype naar de tabel sleept, worden de bovenste dimensie van Browsertype weergegeven (bijvoorbeeld Microsoft, Apple, Google, enz.) Hiermee gaat u dynamisch terug naar de tabelrijen. Indien neergezet in een kolom, de top 5 Browser de afmetingspunten van het Type dynamisch terugkeren.

Items voor dynamische afmetingen hebben de optie Rijfilter en de X-pictogrammen en doen dit **niet** hebben vergrendelingspictogram aanwezig. <!--do they have the lock icon? --> Wanneer u op de x naast een element met een dynamische dimensie klikt, wordt automatisch een filter toegepast. Zie voor meer informatie over het toepassen van filters op tabellen [Tabellen filteren en sorteren](/help/analyze/analysis-workspace/visualizations/freeform-table/filter-and-sort.md).

![](assets/dynamic-items.png)

## Statische dimensie-items

Statische dimensie-items veranderen niet met de tijd; het zijn vaste componenten die altijd worden geretourneerd in een vrije-vormtabel. De statische afmetingspunten worden geprefereerd wanneer u altijd het zelfde punt wilt analyseren, of het specifieke campagnes of specifieke dagen in de week zijn.

Wanneer u handmatig bepaalde componentwaarden (afmetingen, metrisch, segment, datumbereik) in een tabel selecteert en neerzet, is het resultaat een statische lijst met rijen of kolommen. De statische afmetingspunten kunnen ook worden gecreeerd als u verkiest:

* Van rijen, klik met de rechtermuisknop > [!UICONTROL Display only selected rows]
* Van kolommen, klik met de rechtermuisknop > [!UICONTROL Make item static]

Wanneer u bijvoorbeeld over specifieke BrowserType-items sleept, zoals Microsoft en Apple, worden die twee specifieke items altijd in de tabel geplaatst.

Statische dimensie-items doen dit **niet** hebben de optie Rijfilter. In plaats daarvan worden op elk item de pictogrammen Vergrendelen en X weergegeven. Klik op het X-pictogram om dat dimensie-item uit de tabel te verwijderen.

![](assets/static-items.png)

## Items met gemengde dimensies

Items van het type Dimension van verschillende afmetingen kunnen aan dezelfde tabel worden toegevoegd. In deze gevallen staat in de rijkop &quot;Gemengd Dimension&quot;. Deze dimensie-items zijn statisch. Bijvoorbeeld, toevoegend specifieke afmetingspunten van de Browser dimensie van het Type en andere afmetingspunten van de Browser afmeting.

![](assets/mixed-dimensions.png)

## Totaal aantal rijen vrije vorm

Dynamische en statische rijen gedragen zich anders in de vrije-vormtotale rij. Standaard:

* Dynamische rijen worden samengevat op de server en worden niet-gedupliceerde cijfers zoals bezoeken of bezoekers
* Statische rijen worden als client samengevoegd en wel **niet** deduplicatie van metingen. Als u de totale rijserver wilt berekenen, wijzigt u de rijinstelling in **Totaal-generaal tonen**. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-table/workspace-totals.html)

## Statische rijen opnieuw ordenen

Hier volgt een video over het onderwerp:

>[!VIDEO](https://video.tv.adobe.com/v/31319/?quality=12)
