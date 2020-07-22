---
title: Dynamische of statische dimensie-items
description: Hoe te met dynamische en statische afmetingspunten in lijsten in wisselwerking te staan.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 2%

---


# Dynamische versus statische dimensie-items in vrije-vormtabellen

In Freeform-tabellen kunnen de rijen en kolommen verschillende componentwaarden bevatten. Deze waarden kunnen dynamisch (verandering met tijd) of statisch (veranderen niet met tijd) zijn, afhankelijk van de analyse die u wilt bouwen.

## Dynamische dimensie-items

De dynamische afmetingspunten veranderen met tijd en zijn afhankelijk van metrisch die door in de vrije vormlijst wordt gesorteerd. Items met een dynamische dimensie hebben de voorkeur wanneer u de bovenste items gedurende een bepaalde tijdsperiode wilt analyseren.

Wanneer u een dimensie in een vrije vormlijst laat vallen, zijn de dynamische rijen teruggekeerd. Zij vertegenwoordigen de hoogste punten die aan de afmeting voor een bepaalde metrisch en tijdspanne beantwoorden. U kunt ook een dimensie neerzetten in vrije tabelkolommen en de dimensie wordt automatisch uitgebreid naar de bovenste 5 dimensieitems.

Als u bijvoorbeeld de dimensie Browsertype naar de tabel sleept, worden de bovenste dimensie Browsertype weergegeven (bijvoorbeeld Microsoft, Apple, Google, enz.) Hiermee gaat u dynamisch terug naar de tabelrijen. Indien neergezet in een kolom, de hoogste 5 Browser de afmetingspunten van het Type dynamisch terugkeren.

Items van dynamische dimensies hebben de optie voor het filter van de rij en beschikken **niet** over vergrendelingspictogrammen en X-pictogrammen.

## Statische dimensie-items

Statische dimensie-items veranderen niet met de tijd; het zijn vaste componenten die altijd worden geretourneerd in een vrije-vormtabel. De statische afmetingspunten worden geprefereerd wanneer u altijd het zelfde punt wilt analyseren, of het specifieke campagnes of specifieke dagen in de week zijn.

Wanneer u handmatig bepaalde componentwaarden (afmetingen, metrisch, segment, datumbereik) in een tabel selecteert en neerzet, is het resultaat een statische lijst met rijen of kolommen. De statische afmetingspunten kunnen ook tot stand worden gebracht als u verkiest:

* Van rijen, klik met de rechtermuisknop > [!UICONTROL Display only selected rows]
* Van kolommen, klik met de rechtermuisknop > [!UICONTROL Make item static]

Wanneer u bijvoorbeeld over specifieke BrowserType-items sleept, zoals Microsoft en Apple, worden die twee specifieke items altijd in de tabel geplaatst.

De statische afmetingspunten hebben **niet** de optie van de rijfilter. In plaats daarvan worden op elk item de pictogrammen Vergrendelen en X weergegeven. Klik op het X-pictogram om dat dimensie-item uit de tabel te verwijderen.

## Items met gemengde dimensies

Dimensie-items van verschillende afmetingen kunnen aan dezelfde tabel worden toegevoegd. De rijkopbal zegt &quot;Gemengde Afmetingen&quot;in deze gevallen. Deze dimensie-items zijn statisch. Bijvoorbeeld, toevoegend specifieke afmetingspunten van de Browser dimensie van het Type en andere afmetingspunten van de Browser afmeting.

## Totaal aantal rijen vrije vorm

Dynamische en statische rijen gedragen zich anders in de vrije-vormtotale rij. Standaard:

* Dynamische rijen worden samengevat op de server en worden niet-gedupliceerde afmetingen zoals bezoeken of bezoekers
* Statische rijen worden als client-side opgeteld en dedupliceren **niet** metriek.

[Meer informatie over de totale](https://docs.adobe.com/content/help/nl-NL/analytics/analyze/analysis-workspace/build-workspace-project/workspace-totals.html) opties van de Werkruimte voor dynamische en statische rijen.
