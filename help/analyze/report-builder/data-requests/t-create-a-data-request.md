---
description: Stappen om een basisgegevensverzoek van de Report Builder tot stand te brengen.
title: Een data-aanvraag maken
uuid: 5d0151f1-e23d-43eb-84a4-96ae06c3a564
feature: Report Builder
role: Business Practitioner, Administrator
exl-id: 21d552a0-7a58-4217-ba8a-7c87eb4757f6
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 3%

---

# Een Report Builder-gegevensaanvraag maken

Stappen om een basisgegevensverzoek tot stand te brengen.

1. Klik in Excel op **[!UICONTROL Create]**.
1. Selecteer in het venster [!UICONTROL Request Wizard: Step 1] een [rapportsuite](/help/analyze/report-builder/data-requests/selecting-report-suites/t-select-report-suites.md).
1. (Optioneel) Selecteer een segment dat u op de aanvraag wilt toepassen. Als u een of meer segmenten hebt geselecteerd, worden deze boven aan de lijst geplaatst.

   Report Builder gebruikt segmenten op dezelfde manier als Adobe Analytics ze gebruikt. Zie [Handleiding voor analysesegment](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html). 1. (Optioneel) Selecteer een [publicatielijst](/help/analyze/report-builder/data-requests/allow-publishing-list-overrides.md) die u wilt gebruiken voor distributie.
1. Selecteer een [rapporttype](/help/analyze/report-builder/data-requests/c-report-types/select-report-types.md).
1. Geef een [datumbereik](/help/analyze/report-builder/data-requests/configuring-report-dates/custom-calendar.md) op en rapporteer [granularity](/help/analyze/report-builder/data-requests/configuring-report-dates/granularity.md).
1. Klik op **[!UICONTROL Next]**.
1. Geef een lay-out op in het venster [Layout - Wizard Verzoek Stap 2](/help/analyze/report-builder/layout/layout.md):

   | Element | Beschrijving |
   |---|---|
   | Draaiende layout | Verstrekt een rij, een kolom, en metrisch net voor lay-out, gelijkend op de standaardlijsten van Excel. Met behulp van deze indeling kunt u verzoeken om uitsplitsing toevoegen binnen een oorspronkelijke aanvraag. |
   | Aangepaste layout | Verstrekt het grootste deel van de functionaliteit van [!UICONTROL Pivot Layout] maar laat u kiezen waar elk punt in het net in spreadsheet zou moeten worden gevestigd. Deze indeling biedt de flexibiliteit die beschikbaar is in eerdere versies. |

1. Dubbelklik (of sleep) op het tabblad [!UICONTROL Metrics] op de metriek in de structuur om deze aan het [!UICONTROL Metrics]-raster toe te voegen.
1. Dubbelklik (of sleep) op het tabblad [!UICONTROL Dimensions] op de afmetingen in het [!UICONTROL Row Labels]-raster.

   [afmetingen](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/layout/filter-dimenson/filter-dimensions.html) beschikbaar in Stap 2 hangt van het basisrapport af u in Stap 1 selecteerde, en op de configuratie van uw rapportreeks selecteerde. De dimensies zijn punten die correleren, sub-verwant, of een classificatie van het originele rapporttype metrisch zijn u op het [!UICONTROL Request Wizard: Step 1] venster selecteerde. Het toevoegen van meer dan één afmeting in Stap 2 is hoe u een afbraak in uw gegevensverzoek creeert.

   Zie [Metriek en Dimension toevoegen](/help/analyze/report-builder/layout/c-metrics-dimensions/t-add-metrics-and-dimensions.md) voor meer informatie.
