---
description: Stappen om een basis de gegevensverzoek van de Bouwer van het Rapport tot stand te brengen.
title: Een gegevensaanvraag maken
topic: Report builder
uuid: 5d0151f1-e23d-43eb-84a4-96ae06c3a564
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Creeer een de gegevensverzoek van de Bouwer van het Rapport

Stappen om een basisgegevensverzoek tot stand te brengen.

1. Klik in Excel op **[!UICONTROL Create]**.
1. Selecteer in het [!UICONTROL Request Wizard: Step 1] venster een [rapportsuite](/help/analyze/report-builder/data-requests/selecting-report-suites/t-select-report-suites.md).
1. (Optioneel) Selecteer een segment dat u op de aanvraag wilt toepassen. Als u een of meer segmenten hebt geselecteerd, worden deze boven aan de lijst geplaatst.

   De Bouwer van het rapport gebruikt segmenten op de zelfde manier de Analytics van Adobe hen. Zie de [handleiding](https://marketing.adobe.com/resources/help/en_US/analytics/segment/)Analytics Segmentation. 1. (Optioneel) Selecteer een [publicatielijst](/help/analyze/report-builder/data-requests/allow-publishing-list-overrides.md) die u wilt gebruiken voor distributie.
1. Selecteer een [rapporttype](/help/analyze/report-builder/data-requests/c-report-types/select-report-types.md).
1. Geef een [datumbereik](/help/analyze/report-builder/data-requests/configuring-report-dates/custom-calendar.md) op en geef de [granulariteit](/help/analyze/report-builder/data-requests/configuring-report-dates/granularity.md)van het rapport op.
1. Klik op **[!UICONTROL Next]**.
1. Geef in het venster [Layout - Wizard Verzoek Stap 2](/help/analyze/report-builder/layout/layout.md) een lay-out op:

   | Element | Beschrijving |
   |---|---|
   | Draaiende layout | Verstrekt een rij, een kolom, en metrisch net voor lay-out, gelijkend op de standaardlijsten van Excel. Met behulp van deze indeling kunt u verzoeken om uitsplitsing toevoegen binnen een oorspronkelijke aanvraag. |
   | Aangepaste layout | Verstrekt het grootste deel van de functionaliteit van het [!UICONTROL Pivot Layout] maar laat u kiezen waar elk punt in het net in spreadsheet zou moeten worden gevestigd. Deze indeling biedt de flexibiliteit die beschikbaar is in eerdere versies. |

1. Dubbelklik (of sleep) op het [!UICONTROL Metrics] tabblad metriek in de structuur om deze aan het [!UICONTROL Metrics] raster toe te voegen.
1. Dubbelklik op het [!UICONTROL Dimensions] tabblad (of sleep) de afmetingen naar het [!UICONTROL Row Labels] raster.

   De [afmetingen](https://marketing.adobe.com/resources/help/en_US/reference/dimensions.html) beschikbaar in Stap 2 hangen van het basisrapport af u in Stap 1 selecteerde, en op de configuratie van uw rapportreeks. De dimensies zijn punten die correleren, sub-verwant, of een classificatie van het originele rapporttype metrisch zijn u op het [!UICONTROL Request Wizard: Step 1] venster selecteerde. Het toevoegen van meer dan één afmeting in Stap 2 is hoe u een afbraak in uw gegevensverzoek creeert.

   Zie Metriek en afmetingen [toevoegen](/help/analyze/report-builder/layout/c-metrics-dimensions/t-add-metrics-and-dimensions.md) voor meer informatie.
