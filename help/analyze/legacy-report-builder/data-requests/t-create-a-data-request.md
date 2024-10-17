---
description: Stappen om een verzoek van basisgegevens van de Report Builder te creëren.
title: Een gegevensaanvraag maken
feature: Report Builder
role: User, Admin
exl-id: 21d552a0-7a58-4217-ba8a-7c87eb4757f6
source-git-commit: ae6ffed05f5a33f032d0c7471ccdb1029154ddbd
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---

# Een verzoek om Report Builder-gegevens maken

{{legacy-arb}}

Stappen om een basisgegevensverzoek te creëren.

1. Klik in Excel op **[!UICONTROL Create]** .
1. In het [!UICONTROL Request Wizard: Step 1] venster, selecteer a [ rapportreeks ](/help/analyze/legacy-report-builder/data-requests/selecting-report-suites/t-select-report-suites.md).
1. (Optioneel) Selecteer een segment dat u op de aanvraag wilt toepassen. Als u een of meer segmenten hebt geselecteerd, worden deze boven aan de lijst geplaatst.

   Report Builder gebruikt segmenten op dezelfde manier als Adobe Analytics ze gebruikt. Zie de [ Gids van de Segmentatie van Analytics ](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html).
1. Selecteer het type van a [ rapport ](/help/analyze/legacy-report-builder/data-requests/c-report-types/select-report-types.md).
1. Specificeer a [ datumwaaier ](/help/analyze/legacy-report-builder/data-requests/configuring-report-dates/custom-calendar.md) en rapport [ granularity ](/help/analyze/legacy-report-builder/data-requests/configuring-report-dates/granularity.md).
1. Klik op **[!UICONTROL Next]**.
1. In het [ Lay-out - Stap 2 van de Tovenaar van het Verzoek ](/help/analyze/legacy-report-builder/layout/layout.md) venster, specificeer een lay-out:

   | Element | Beschrijving |
   |---|---|
   | Draaiende layout | Verstrekt een rij, een kolom, en metrisch net voor lay-out, gelijkend op de standaardlijsten van Excel. Met behulp van deze indeling kunt u verzoeken om uitsplitsing toevoegen binnen een oorspronkelijke aanvraag. |
   | Aangepaste layout | Biedt de meeste functionaliteit van de [!UICONTROL Pivot Layout] , maar laat u kiezen waar elk item in het raster zich in het werkblad moet bevinden. Deze indeling biedt de flexibiliteit die beschikbaar is in eerdere versies. |

1. Dubbelklik (of sleep) op het tabblad [!UICONTROL Metrics] in de boomstructuur op cijfers om deze aan het [!UICONTROL Metrics] -raster toe te voegen.
1. Dubbelklik (of sleep) de afmetingen op het tabblad [!UICONTROL Dimensions] naar het [!UICONTROL Row Labels] -raster.

   De [ afmetingen ](https://experienceleague.adobe.com/docs/analytics/analyze/legacy-report-builder/layout/filter-dimenson/filter-dimensions.html) beschikbaar in Stap 2 hangen van het basisrapport af u in Stap 1, en op de configuratie van uw rapportreeks selecteerde. De dimensies zijn punten die correleren, sub-verwant, of een classificatie van het originele rapporttype metrisch zijn u op het [!UICONTROL Request Wizard: Step 1] venster selecteerde. Het toevoegen van meer dan één afmeting in Stap 2 is hoe u een afbraak in uw gegevensverzoek creeert.

   Zie [ Metriek en Dimensionen ](/help/analyze/legacy-report-builder/layout/c-metrics-dimensions/t-add-metrics-and-dimensions.md) voor meer informatie toevoegen.
