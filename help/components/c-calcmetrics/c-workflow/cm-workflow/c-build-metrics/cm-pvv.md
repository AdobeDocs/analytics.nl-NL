---
description: Leer hoe te om eenvoudige berekende metrisch te bouwen.
title: Een eenvoudige, berekende metrisch maken
feature: Calculated Metrics
exl-id: 2d1c4677-b07c-4eca-97b7-e5e4594daee1
source-git-commit: 35f2812c1a1a4eed090e04d67014fcebf88a80ec
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---

# Bouw eenvoudig berekende metrisch

De volgende informatie verklaart hoe te om tot een eenvoudige *Bekijken van de Pagina per metrisch bezoek* te leiden.

1. Begin om metrisch te bouwen, zoals die in [ wordt beschreven bouwt metriek ](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md).
1. Geef de metrische waarde `Page Views per Visit` of een vergelijkbare naam.
1. Geef metrisch gebruikersvriendelijk **[!UICONTROL Description]** om te tonen waar metrisch wordt gebruikt voor.
1. Selecteer rechts **[!UICONTROL Format]** . Kies voor dit voorbeeld **[!UICONTROL Decimal]** .
1. Bepaal hoeveel decimalen u het rapport wilt weergeven.
1. Selecteer **[!UICONTROL Show updward trend as]** ▲ in de vervolgkeuzelijst **[!UICONTROL Good (Green)]** .
1. Voeg een **[!UICONTROL Tag]** toe om uw metriek te organiseren.
1. Voor deze berekende metrische waarde sleept u **[!UICONTROL Page Views]** eerst van de **[!UICONTROL Metrics]** -componenten naar het **[!UICONTROL Definition]** -gedeelte van het canvas.
1. Vervolgens sleept u **[!UICONTROL Visits]** uit de **[!UICONTROL Metrics]** -componenten en zet u de metrische waarde onder **[!UICONTROL Page Views]** (wacht tot de blauwe lijn verschijnt voordat u de metrische waarde neerzet).
1. Selecteer de verdelings{![ exploitant 0} verdelen. ](/help/assets/icons/Divide.svg) (Splitsen is de standaardoperator.)
1. U kunt **[!UICONTROL Preview]** van metrisch zien terwijl u metrisch bouwt.
1. [ de verenigbaarheid van het Product ](../../../cm-compatibility.md) toont u of metrisch met Huidige Gegevens of slechts met volledig Verwerkte Gegevens compatibel is.

   ![ Eenvoudige berekende metrisch ](assets/simple-calculated-metric.png)
1. Selecteer **[!UICONTROL Save]** .

   De formule **[!UICONTROL Summary]** wordt altijd bijgewerkt wanneer u een wijziging aanbrengt in de definitie van de metrische waarde.

1. (Facultatief) om te delen, goed te keuren, (re-)markering, anders te noemen of te schrappen metrisch, kunt u naar de [ Berekende metriekmanager ](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-manager.md) gaan.

