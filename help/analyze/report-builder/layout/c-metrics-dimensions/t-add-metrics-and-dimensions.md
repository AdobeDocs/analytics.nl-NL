---
description: Stappen om metriek en afmetingen aan een verzoek toe te voegen.
title: Cijfers en dimensies toevoegen
uuid: 588ce96b-3a2d-42b7-8a8e-7e6f448a0115
feature: Report Builder
role: User, Admin
exl-id: d4e36b69-b5aa-43e5-b394-3b6d93143f15
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 2%

---

# Cijfers en dimensies toevoegen

Stappen om metriek en afmetingen aan een verzoek toe te voegen.

1. [Maak de ](/help/analyze/report-builder/data-requests/data-requests.md) gegevensaanvraag op de  [!UICONTROL Request Wizard: Step 1]pagina en klik op  **[!UICONTROL Next]**.
1. Dubbelklik op de metriek [!UICONTROL Request Wizard: Step 2] of sleep deze naar de gewenste positie.

   ![Stapinfo](assets/adding_metrics.png)

   Wanneer u metriek toevoegt, worden zij niet verwijderd uit [!UICONTROL Metrics] tabel, omdat u metriek veelvoudige tijden binnen een verzoek kunt tonen. U kunt bijvoorbeeld naast elke waarde het metrische subtotaal weergeven. De lijst met beschikbare metriek verandert echter telkens wanneer u een dimensie toevoegt of verwijdert.

   U kunt alleen metriek toevoegen aan de lay-outsectie [!UICONTROL Metrics]. Metrisch worden als [!UICONTROL Metric Header] toegevoegd aan de [!UICONTROL Column Label]-layout. Als u een [!UICONTROL Metric Header] van [!UICONTROL Column Layout] aan [!UICONTROL Row Layout] beweegt, wordt het daar getoond en als metrisch als onderbreking gebruikt.

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
   * Klik op het tabblad Dimension en ga terug naar het tabblad Metrisch.
   * U roept andere subformulieren (modaal of modeless) aan die bij uitgang aan Stap 2 van de Tovenaar van het Verzoek zullen terugkeren. Voorbeelden van deze formulieren zijn

      * Dimension Filter Forms
      * Opmaak datumbereik Forms
      * Formulier Indelingsopties
      * Tekstformulier voor voorloop uitstellen
      * Locatieformulier uitvoerbereik

1. (Optioneel) Als u een verzoek metrisch wilt sorteren, klikt u op het metrische label.
1. Voeg afmetingen toe op dezelfde manier als waarop u metriek toevoegt.

Op [!UICONTROL Dimensions] lusje, toont het systeem dimensies die onderverdelen of een classificatie van om het even welk basisrapport zijn u op Stap 1 selecteert, en op de configuratie van de rapportreeks selecteert. Wanneer u een dimensie neerzet in de layoutrasters, wordt deze verwijderd uit de structuurweergave en wordt de lijst met resterende beschikbare afmetingen opnieuw berekend.

De [!UICONTROL Date] dimensie wordt automatisch toegevoegd. De beschikbare datumafmetingen veranderen afhankelijk van de geselecteerde granulariteit in [!UICONTROL Request Wizard: Step 1]. (Geldige waarden zijn:

    * Uur
    * Dag
    * Week
    * Maand
    * Jaar
    * Datumbereik (wanneer geen granulariteit is opgegeven)

1. Wijzig metriek en afmetingen door [formaatopties](/help/analyze/report-builder/layout/t-format-display-headers.md) en filters te vormen.
1. Klik op **[!UICONTROL Finish]**.
In het volgende voorbeeld hebben de afmetingen betrekking op de metrische waarde [!UICONTROL Page]. Hier, leidt de [!UICONTROL Referring Domain] dimensie tot een verdelingsrapport tussen [!UICONTROL Page] en [!UICONTROL Referring Domain]. Het tabblad [!UICONTROL Dimension] wordt alleen bijgewerkt met dimensies die u kunt toevoegen aan een uitsplitsingsrapport.

![](assets/page_pageview_02.png)
