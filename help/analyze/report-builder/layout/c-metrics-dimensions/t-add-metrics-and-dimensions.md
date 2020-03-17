---
description: Stappen om metriek en afmetingen aan een verzoek toe te voegen.
title: Metriek en afmetingen toevoegen
topic: Report builder
uuid: 588ce96b-3a2d-42b7-8a8e-7e6f448a0115
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Metriek en afmetingen toevoegen

Stappen om metriek en afmetingen aan een verzoek toe te voegen.

1. [Maak de gegevensaanvraag](/help/analyze/report-builder/data-requests/data-requests.md) op de [!UICONTROL Request Wizard: Step 1]pagina en klik op **[!UICONTROL Next]**.
1. Dubbelklik op de metriek [!UICONTROL Request Wizard: Step 2]of sleep deze naar de gewenste positie.

   ![Stapinfo](assets/adding_metrics.png)

   Wanneer u metriek toevoegt, worden deze niet verwijderd van het [!UICONTROL Metrics] tabblad, omdat u metriek meerdere keren kunt weergeven binnen een aanvraag. U kunt bijvoorbeeld naast elke waarde het metrische subtotaal weergeven. De lijst met beschikbare metriek verandert echter telkens wanneer u een dimensie toevoegt of verwijdert.

   U kunt alleen metriek toevoegen aan de [!UICONTROL Metrics] layoutsectie. Metrisch worden als een [!UICONTROL Column Label] geheel aan de layout toegevoegd [!UICONTROL Metric Header]. Als u een [!UICONTROL Metric Header] van [!UICONTROL Column Layout] naar [!UICONTROL Row Layout]beweegt, wordt het daar getoond en als metrisch als onderbreking gebruikt.

   Een zoekbalk wordt weergegeven op het tabblad Metrisch, net boven de lijst Metrisch.

   ![](assets/search_bar_metric.png)

   Houd dit in gedachten:

   * Terwijl u een zoekterm invoert, wordt de lijst automatisch bijgewerkt en worden alleen de metriek weergegeven waarvan het label overeenkomt met de zoekterm.
   * De overeenkomst is niet-hoofdlettergevoelig en is gelijk aan een zoekopdracht &quot;bevat&quot;.
   * zoekopdrachten in het hele woord of andere speciale zoekvlag (begint met, eindigt met, AND, OR, enz.) worden niet ondersteund.

      De termijn van het Onderzoek zal worden ontruimd als u de Tovenaar van het Verzoek weggaat (d.w.z., klik Afwerking of annuleer), of ga terug naar Stap 1 van de Tovenaar van het Verzoek, of verander de Metrische categorie.

      De zoekterm wordt in de volgende gevallen niet gewist:

   * U sleept een metrisch item uit de lijst en zet het neer (of dubbelklikt), zodat het wordt toegevoegd aan het deelvenster Metrische gegevens voor draaitalayout/aangepaste layout.
   * U verwijdert een of meer metrische items uit het deelvenster Metrisch voor draaitout/aangepaste layout.
   * Klik op het tabblad Dimensie en ga terug naar het tabblad Metrisch.
   * U roept andere subformulieren (modaal of modeless) aan die bij uitgang aan Stap 2 van de Tovenaar van het Verzoek zullen terugkeren. Voorbeelden van deze formulieren zijn

      * Dimensie-filterformulieren
      * Formulieren opmaken datumbereik
      * Formulier Indelingsopties
      * Tekstformulier voor voorloop uitstellen
      * Locatieformulier uitvoerbereik

1. (Optioneel) Als u een verzoek metrisch wilt sorteren, klikt u op het metrische label.
1. Voeg afmetingen toe op dezelfde manier als waarop u metriek toevoegt.

Op het [!UICONTROL Dimensions] lusje, toont het systeem dimensies die onderverdelen of een classificatie van om het even welk basisrapport zijn u op Stap 1 selecteert, en op de configuratie van de rapportreeks. Wanneer u een dimensie neerzet in de layoutrasters, wordt deze verwijderd uit de structuurweergave en wordt de lijst met resterende beschikbare afmetingen opnieuw berekend.

De [!UICONTROL Date] dimensie wordt automatisch toegevoegd. De beschikbare datumafmetingen veranderen afhankelijk van de geselecteerde granulariteit van de [!UICONTROL Request Wizard: Step 1]. (Geldige waarden zijn:

    * Uur
    * Dag
    * Week
    * Maand
    * Jaar
    * Datumbereik (wanneer geen granulariteit is opgegeven)

1. Metriek en afmetingen wijzigen door [opmaakopties](/help/analyze/report-builder/layout/t-format-display-headers.md) en filters te configureren.
1. Klik op **[!UICONTROL Finish]**.
In het volgende voorbeeld hebben afmetingen betrekking op de [!UICONTROL Page] metrische waarde. Hier leidt de [!UICONTROL Referring Domain] dimensie tot een uitsplitsingsrapport tussen [!UICONTROL Page] en [!UICONTROL Referring Domain]. Het [!UICONTROL Dimension] tabblad wordt alleen bijgewerkt met afmetingen die u kunt toevoegen aan een uitsplitsingsrapport.

![](assets/page_pageview_02.png)
