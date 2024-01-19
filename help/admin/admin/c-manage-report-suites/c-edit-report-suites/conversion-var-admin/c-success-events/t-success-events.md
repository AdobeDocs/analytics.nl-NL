---
description: Stappen die beschrijven hoe te om succesgebeurtenissen te vormen.
title: Succesgebeurtenissen configureren
feature: Event
role: Admin
exl-id: 0e9a6d8f-2ce7-4551-885d-bd77ff131da0
source-git-commit: d173a6c6c9751a86f4218ec842da17da14f8485b
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 7%

---

# Succesgebeurtenissen configureren

Succesgebeurtenissen configureren:

1. Klik op **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. Selecteer een rapportsuite.
1. Klik op **[!UICONTROL Edit Settings]** > **[!UICONTROL Conversion]** > **[!UICONTROL Success Events]**.

   ![Stap Resultaat](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/assets/success_event_page.png)

1. In de **[!UICONTROL Name]** selecteert u het selectievakje naast elk item om bewerken in te schakelen en geeft u vervolgens de gewenste naam op.
1. In de **[!UICONTROL Type]** selecteert u het selectievakje naast elk item om de vervolgkeuzelijst in te schakelen en selecteert u het gewenste type.

   >[!NOTE]
   >
   >Voordat u een gebeurtenistype wijzigt, raadpleegt u [Gebeurtenistype wijzigen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/event-type.md).

   Zie [Pagina Gebeurtenissen geslaagd - beschrijvingen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/success-event.md) voor informatie over deze elementen.

1. In de **[!UICONTROL Polarity]** kolom, specificeer of een stijgende trend voor deze metrisch goed of slecht is.
1. In de **[!UICONTROL Visibility]** kolom, kunt u standaardmetriek (ingebouwde), douanegebeurtenissen, en ingebouwde gebeurtenissen in het Menu, Metrische Kiezers, Berekende Bouwer van Metriek, en de Bouwer van het Segment verbergen.

   Deze instelling heeft geen invloed op de gegevensverzameling voor die metrische waarde of gebeurtenis; deze instelling heeft alleen invloed op de zichtbaarheid in de gebruikersinterface, als volgt:


   | Instelling | Zichtbaar in | Niet zichtbaar in |
   |---------|----------|---------|
   | [!UICONTROL **Overal zichtbaar**] | <ul><li>Analysis Workspace</li><li>Segment Builder</li><li>Berekende metrische bouwer</li></ul> | N.v.t. |
   | [!UICONTROL **Opbouwmachines**] | <ul><li>Segment Builder</li><li>Berekende metrische bouwer</li><li>Analysis Workspace</li></ul> |
   | [!UICONTROL **Overal verborgen**] | N.v.t. | <ul><li>Analysis Workspace</li><li>Segment Builder</li><li>Berekende metrische bouwer</li></ul> |

1. Geef een beschrijving op.
1. Controleer of u de gebeurtenis altijd wilt opnemen.
1. Deelnemingsmetriek in- of uitschakelen.

   >[!NOTE]
   >
   >U kunt deelname inschakelen voor maximaal 100 aangepaste gebeurtenissen. Bovendien kunt u participatiemetriek maken in de [Berekende cijfers](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/participation-metric.md) bouwer.

1. Klik op **[!UICONTROL Save]**.
