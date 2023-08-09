---
description: Leer de stappen om metriek en afmetingen aan een verzoek toe te voegen.
title: Metriek en afmetingen toevoegen
uuid: 588ce96b-3a2d-42b7-8a8e-7e6f448a0115
feature: Report Builder
role: User, Admin
exl-id: d4e36b69-b5aa-43e5-b394-3b6d93143f15
source-git-commit: fb39f906d6c08713e4dc8211c917b2942502868e
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# Cijfers en dimensies toevoegen

Stappen om metriek en afmetingen aan een verzoek toe te voegen.

1. Gebruik de [!UICONTROL Request Wizard: Step 1] formulier naar [De gegevensaanvraag maken](/help/analyze/report-builder/data-requests/data-requests.md)  klik vervolgens op **[!UICONTROL Next]**.
1. In de [!UICONTROL Request Wizard: Step 2] Dubbelklik op maateenheden of sleep deze naar de gewenste positie.

   ![Schermafbeelding met de wizard Verzoek: Stap 2 met een pijl die van de lijst Metriek naar de gewenste sectie Paginaweergave wijst.](assets/adding_metrics.png)

   Wanneer u metriek toevoegt, worden deze niet verwijderd uit de [!UICONTROL Metrics] , omdat u metriek in een aanvraag meerdere keren kunt weergeven. U kunt bijvoorbeeld naast elke waarde het metrische subtotaal weergeven. De lijst met beschikbare metriek verandert echter telkens wanneer u een dimensie toevoegt of verwijdert.

   U kunt alleen metriek toevoegen aan de [!UICONTROL Metrics] layoutsectie. De metriek wordt toegevoegd aan [!UICONTROL Column Label] layout als een [!UICONTROL Metric Header]. Als u een [!UICONTROL Metric Header] van [!UICONTROL Column Layout] tot [!UICONTROL Row Layout], wordt het daar getoond en als metrisch als onderbreking gebruikt.

   Een zoekbalk wordt weergegeven op het tabblad Metrisch, net boven de lijst Metrisch.

   ![Schermafbeelding met de zoekbalk voor statistieken.](assets/search_bar_metric.png)

## Richtsnoeren

Houd rekening met de volgende richtlijnen wanneer u metriek en afmetingen toevoegt.

* Wanneer u een zoekterm invoert, wordt de lijst automatisch bijgewerkt om metriek weer te geven die labels hebben die overeenkomen met de zoekterm.
* De overeenkomst is niet-gevoelig geval en gelijkwaardig aan a *contains* zoeken.
* Zoeken op volledige woorden en andere speciale zoekmarkeringen (begint met, eindigt met, AND, OR, enz.) worden niet ondersteund.

De zoekterm wordt gewist als u de wizard Verzoek afsluit wanneer u op [!UICONTROL Finish] of [!UICONTROL Cancel], of ga terug naar Stap 1 van de Tovenaar van het Verzoek, of verander de Metrische categorie.

De zoekterm wordt niet gewist:

* Wanneer u een metrisch item uit de lijst sleept en neerzet (of dubbelklikt), wordt dit item toegevoegd aan het deelvenster Metrische gegevens voor draaitalay-out/Aangepaste layout.
* Wanneer u een metrisch(e) item(s) verwijdert uit het deelvenster Metrisch van draaitout/aangepaste layout.
* Wanneer u op het tabblad Dimension klikt, gaat u terug naar het tabblad Metrisch.
* Wanneer u andere subformulieren (modaal of modeless) aanroept die bij uitgang aan Stap 2 van de Tovenaar van het Verzoek zal terugkeren. Voorbeelden van deze formulieren zijn

   * Dimension Filter Forms
   * Opmaak datumbereik Forms
   * Formulier Indelingsopties
   * Tekstformulier voor voorvoegen en uitstellen
   * Locatieformulier uitvoerbereik

## Sorteer een verzoek door metrisch

U kunt een verzoek naar keuze sorteren door metrisch.

Om een verzoek door metrisch te sorteren

1. Klik op het metrische label.
1. Afmetingen toevoegen. Voeg afmetingen toe op dezelfde manier als waarop u metriek toevoegt. Zie de stappen 1 en 2 hierboven.

   Op de [!UICONTROL Dimensions] tabblad, geeft het systeem afmetingen weer die zijn gesplitst of die een classificatie zijn van een basisrapport dat u selecteert [!UICONTROL Request Wizard: Step 1]en over de configuratie van de rapportsuite. Wanneer u een afmeting aan de lay-outrasters laat vallen, wordt het verwijderd uit de boomstructuurweergave en herberekent het overzicht van resterende beschikbare afmetingen.

   De [!UICONTROL Date] dimensie wordt automatisch toegevoegd. Welke datumafmetingen beschikbaar zijn, is afhankelijk van de geselecteerde granulariteit in het menu [!UICONTROL Request Wizard: Step 1]. Geldige waarden zijn:

   * Uur
   * Dag
   * Week
   * Maand
   * Jaar
   * Datumbereik (wanneer geen granulariteit is opgegeven)

1. Metriek en afmetingen wijzigen door configureren [opmaakopties](/help/analyze/report-builder/layout/t-format-display-headers.md) en filters.
1. Klik op **[!UICONTROL Finish]**.
In het volgende voorbeeld hebben de afmetingen betrekking op de [!UICONTROL Page] metrisch. De [!UICONTROL Referring Domain] dimensie creëert een uitsplitsingsrapport tussen [!UICONTROL Page] en [!UICONTROL Referring Domain]. De [!UICONTROL Dimension] wordt bijgewerkt met alleen dimensies die u kunt toevoegen aan een uitsplitsingsrapport.

   ![Screenshot met de afmetingen die betrekking hebben op de metrische waarde.](assets/page_pageview_02.png)
