---
title: Dynamische en statische Dimension-items
description: Leer hoe u dynamische en statische dimensie-items gebruikt in vrije-vormtabellen in Analysis Workspace.
feature: Freeform Tables
role: User, Admin
exl-id: 4cdc93b5-67ed-46a4-ba9f-a96e640da9d9
source-git-commit: f258a1150a4bee11f5922d058930dc38b1ddfa14
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Dynamische en statische dimensie-items

In Freeform-tabellen kunnen de rijen en kolommen verschillende componentwaarden bevatten. Deze waarden kunnen dynamisch (verandering in tijd) of statisch (veranderen niet in tijd) zijn, afhankelijk van de analyse die u wilt bouwen.

## Dynamische dimensie-items

De dynamische afmetingspunten veranderen in tijd en zijn afhankelijk van metrisch die door in de vrije vormlijst wordt gesorteerd. Items met een dynamische dimensie hebben de voorkeur wanneer u de bovenste items gedurende een bepaalde tijdsperiode wilt analyseren.

Wanneer u een dimensie in een vrije vormlijst laat vallen, zijn de dynamische rijen teruggekeerd. De dynamische rijen vertegenwoordigen de hoogste punten die aan de afmeting voor een bepaalde metrisch en tijdspanne beantwoorden. U kunt ook een dimensie neerzetten in vrije tabelkolommen en de dimensie wordt automatisch uitgebreid naar de bovenste 5 dimensieitems.

Wanneer u bijvoorbeeld de afmetingen Browsertype naar de tabel sleept, worden de bovenste elementen voor Browsertype (bijvoorbeeld Microsoft, Apple, Google, enz.) dynamisch teruggezet naar de tabelrijen. Indien neergezet in een kolom, de top 5 Browser de afmetingspunten van het Type dynamisch terugkeren.

De dynamische afmetingspunten hebben de optie van de rijfilter ![ Filter ](/help/assets/icons/Filter.svg) en a ![ dicht ](/help/assets/icons/Close.svg), en hebben **niet** een slot ![ LockClosed ](/help/assets/icons/LockClosed.svg) aanwezig. <!--do they have the lock icon? --> wanneer u ![ dicht ](/help/assets/icons/Close.svg) naast een dynamisch afmetingspunt klikt, wordt een filter automatisch toegepast. Voor meer informatie over het toepassen van filters op lijsten, zie [ Filter en sorteerlijsten ](/help/analyze/analysis-workspace/visualizations/freeform-table/filter-and-sort.md).


![ A Freeform Lijst die het filterpictogram benadrukt.](assets/dynamic-items.png)

## Statische dimensie-items

De statische afmetingspunten veranderen niet met tijd; zij zijn vaste componenten die altijd in een vrije vormlijst zijn teruggekeerd. De statische afmetingspunten worden geprefereerd wanneer u altijd het zelfde punt wilt analyseren, of het specifieke campagnes of specifieke dagen in de week zijn.

Wanneer u handmatig bepaalde componentwaarden (afmetingen, metrisch, filter, datumbereik) in een tabel selecteert en neerzet, bestaat het resultaat uit een statische lijst met rijen of kolommen.

Wanneer u bijvoorbeeld over specifieke BrowserType-items sleept, zoals Microsoft en Apple, worden die twee specifieke items altijd in de tabel geplaatst.

Er kunnen ook statische dimensie-items worden gemaakt als u ervoor kiest om **[!UICONTROL Display only selected rows]** te selecteren in het contextmenu voor geselecteerde rijen.

De statische afmetingspunten hebben **** niet de optie van de rijfilter. In plaats daarvan, zijn a ![ LockClosed ](/help/assets/icons/LockClosed.svg) en ![ dicht ](/help/assets/icons/Close.svg) aanwezig op elk punt. Selecteer ![ dicht ](/help/assets/icons/Close.svg) om dat afmetingspunt uit de lijst te verwijderen.

![ A Freeform Lijst die de Browser Type en de rij van Microsoft met een slotpictogramnota toont: Dit afmetingspunt is statisch en zal niet met tijd veranderen.](assets/static-items.png)

## Items met gemengde dimensies

Dimension-items van verschillende afmetingen kunnen aan dezelfde tabel worden toegevoegd. In deze gevallen staat de rijkop op **[!UICONTROL Mixed Dimensions]** . Deze dimensie-items zijn statisch. Bijvoorbeeld, toevoegend specifieke afmetingspunten van de Browser afmeting van de Groep en andere afmetingspunten van de Browser afmeting van de Naam.

![ A Freeform Lijst die de Gemengde kolom van Afmetingen benadrukt.](assets/mixed-dimensions.png)

## Totaal aantal rijen vrije vorm

Dynamische en statische rijen gedragen zich anders in de vrije-vormtotale rij. Standaard:

* Dynamische rijen zijn optellende server-kant en de-dubbele metriek zoals zittingen of personen.
* De statische rijen worden samengevat cliënt-kant en **niet** de-dubbele metriek. Om de totale rij server-kant te berekenen, verander de Rij die aan **plaatsen toont groot totaal**. [Meer informatie](/help/analyze/analysis-workspace/visualizations/freeform-table/workspace-totals.md)


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ statische rijen ](https://video.tv.adobe.com/v/31319?quality=12&learn=on){target="_blank"} voor een demo video opnieuw ordenen.

>[!ENDSHADEBOX]


