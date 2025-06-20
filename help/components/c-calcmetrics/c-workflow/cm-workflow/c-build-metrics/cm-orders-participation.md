---
description: Verklaart hoe te om metrisch tot stand te brengen die toont welke Kanalen van de Marketing in rijorden bijwonen. Dit kan aan om het even welke dimensie of succesgebeurtenis van belang worden aangepast.
title: Assistentie bij bestelling metrisch
feature: Calculated Metrics
exl-id: 33cb441d-d003-408d-ba67-1bcdd0e821ff
source-git-commit: bf58da2a39e8b9fd298356f23a9bf8f6c394d3de
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---

# Bouw complexere berekende metrisch

Dit artikel verklaart een complexer voorbeeld van berekende metrisch. Deze berekende maatstaven laten zien welke marketingkanalen helpen bij het besturen van bestellingen. Dit type van berekende metrisch kan aan om het even welke afmeting of succesgebeurtenis worden aangepast.

1. Begin om berekende metrisch te bouwen, zoals die in [ wordt beschreven bouwt metriek ](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md).

1. Geef in de builder Berekende metriek de naam van de metrische waarde `Assisted Orders` of iets gelijkaardigs.

1. Selecteer de metrische waarde **[!UICONTROL Online Orders]** in de **[!UICONTROL Metrics]** -componenten en sleep de metrische waarde naar het **[!UICONTROL Definition]** -gebied.

   1. Selecteer ![ Plaatsend ](/help/assets/icons/Setting.svg) voor metrisch.
   1. Selecteer **[!UICONTROL Use non-default attribution model]** .
   1. Pas het attributiemodel aan in **[!UICONTROL Column attribution model]** .
      1. Selecteer **[!UICONTROL Custom]** voor **[!UICONTROL Model]** . Stel **[!UICONTROL Starter]** in op `0` , **[!UICONTROL Player]** op `100` en **[!UICONTROL Closer]** op `0` .
      1. Selecteer **[!UICONTROL Visitor]** voor **[!UICONTROL Container]** .
      1. Selecteer **[!UICONTROL 30 Days]** voor **[!UICONTROL Lookback window]** .

      1. Selecteer **[!UICONTROL Apply]** .

      ![ de attributiemodel van de Kolom ](assets/complex-calculated-metric.png)

1. Selecteer **[!UICONTROL Save]** om de berekende metrische waarde op te slaan.

De berekende metrische waarde gebruiken:

1. Maak in Analysis Workspace een vrije-vormtabel met de **[!UICONTROL Marketing Channel]** -dimensie **[!UICONTROL Online Orders]** en de nieuwe **[!UICONTROL Assisted Online Orders]** -metrische waarde.

   ![ het Marketing Kanaal steunde Online Orden ](assets/marketing-channel-assists.png)

1. (Facultatief) deel metrisch met andere gebruikers in uw organisatie, zoals die in [ wordt beschreven aandeel berekende metriek ](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-sharing.md).

Dit is een gemakkelijke manier om te zien welke Marketing Channels hebben geholpen bij het bestellen van rijorders. U kunt ook vanuit een vrije-vormtabel met de rechtermuisknop op elke willekeurige meting klikken en het attributiemodel rechtstreeks vanuit de tabel aanpassen.
