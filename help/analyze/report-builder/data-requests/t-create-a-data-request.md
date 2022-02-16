---
description: Stappen om een basisgegevensverzoek van de Report Builder tot stand te brengen.
title: Een data-aanvraag maken
feature: Report Builder
role: User, Admin
exl-id: 21d552a0-7a58-4217-ba8a-7c87eb4757f6
source-git-commit: 1ee50c6a2231795b2ad0015a79e09b7c1c74d850
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 2%

---

# Een Report Builder-gegevensaanvraag maken

Stappen om een basisgegevensverzoek tot stand te brengen.

1. Klik in Excel op **[!UICONTROL Create]**.
1. In de [!UICONTROL Request Wizard: Step 1] venster, selecteert u een [rapportsuite](/help/analyze/report-builder/data-requests/selecting-report-suites/t-select-report-suites.md).
1. (Optioneel) Selecteer een segment dat u op de aanvraag wilt toepassen. Als u een of meer segmenten hebt geselecteerd, worden deze boven aan de lijst geplaatst.

   Report Builder gebruikt segmenten op dezelfde manier als Adobe Analytics ze gebruikt. Zie de [Handleiding voor analysegmentatie](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html). 1. (Optioneel) Selecteer een [publicatielijst](/help/analyze/report-builder/data-requests/allow-publishing-list-overrides.md) te gebruiken voor distributie.
1. Selecteer een [rapporttype](/help/analyze/report-builder/data-requests/c-report-types/select-report-types.md).
1. Geef een [datumbereik](/help/analyze/report-builder/data-requests/configuring-report-dates/custom-calendar.md) en rapporteren [granulariteit](/help/analyze/report-builder/data-requests/configuring-report-dates/granularity.md).
1. Klik op **[!UICONTROL Next]**.
1. In de [Layout - Wizard Verzoek, stap 2](/help/analyze/report-builder/layout/layout.md) Geef een indeling op:

   | Element | Beschrijving |
   |---|---|
   | Draaiende layout | Verstrekt een rij, een kolom, en metrisch net voor lay-out, gelijkend op de standaardlijsten van Excel. Met behulp van deze indeling kunt u verzoeken om uitsplitsing toevoegen binnen een oorspronkelijke aanvraag. |
   | Aangepaste layout | Biedt de meeste functionaliteit van het [!UICONTROL Pivot Layout] maar hiermee kunt u kiezen waar elk item in het raster zich in het werkblad moet bevinden. Deze indeling biedt de flexibiliteit die beschikbaar is in eerdere versies. |

1. Op de [!UICONTROL Metrics] dubbelklikt (of sleept) u op de maateenheden in de boomstructuur om deze aan de [!UICONTROL Metrics] raster.
1. Op de [!UICONTROL Dimensions] kunt u dubbelklikken (of slepen) op de afmetingen van [!UICONTROL Row Labels] raster.

   De [afmetingen](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/layout/filter-dimenson/filter-dimensions.html) beschikbaar in Stap 2 hangt van het basisrapport af u in Stap 1, en op de configuratie van uw rapportreeks selecteerde. De afmetingen zijn punten die correleren, subreleren, of zijn een classificatie van het originele rapporttype metrisch u op selecteerde [!UICONTROL Request Wizard: Step 1] venster. Het toevoegen van meer dan één afmeting in Stap 2 is hoe u een afbraak in uw gegevensverzoek creeert.

   Zie [Metriek en Dimension toevoegen](/help/analyze/report-builder/layout/c-metrics-dimensions/t-add-metrics-and-dimensions.md) voor meer informatie .
