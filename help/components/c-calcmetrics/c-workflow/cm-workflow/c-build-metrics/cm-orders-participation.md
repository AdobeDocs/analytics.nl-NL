---
description: Verklaart hoe te om metrisch tot stand te brengen die toont welke Kanalen van de Marketing in rijorden bijwonen. Dit kan aan om het even welke dimensie of succesgebeurtenis van belang worden aangepast.
title: Assistentie bij bestelling metrisch
feature: Calculated Metrics
exl-id: 33cb441d-d003-408d-ba67-1bcdd0e821ff
source-git-commit: 4bf8397ee979614539baf21b36363eb03357567a
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# Een metrische &#39;Order Assists&#39; maken

De volgende informatie verklaart hoe te om metrisch tot stand te brengen die toont welke Kanalen van de Marketing in rijorden bijwonen. Dit kan aan om het even welke dimensie of succesgebeurtenis van belang worden aangepast.

1. Beginnen met het maken van een berekende metrische waarde, zoals beschreven in [Metrische gegevens samenstellen](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md).

1. Geef in de builder Berekende metriek de naam van de metrische &quot;Assisted Orders&quot;.

1. In het canvas van de Definitie, sleep in metrische orde. Pas vervolgens het toewijzingsmodel aan met het instellingenset door de **[!UICONTROL Use non-default attribution models]** selectievakje.

   ![](assets/attr-model.png)

1. Selecteren **[!UICONTROL Custom]** als het attributiemodel. Wijzig de gewichten in 0 (startpunt), 100 (speler) en 0 (dichter).

   ![](assets/custom-attr-model.png)

1. Selecteren [!UICONTROL **Toepassen**] > [!UICONTROL **Opslaan**].

1. In Analysis Workspace, creeer een freeform lijst met de afmeting van het Kanaal van de Marketing, de Orden, en uw nieuwe Begeleidende metrische Orden.

   ![](assets/mktg-channel-assists.png)

   Dit is een eenvoudige manier om te zien welke marketingkanalen hebben geholpen bij het bestellen van rijbewijzen. U kunt ook vanuit een vrije-vormtabel met de rechtermuisknop op elke willekeurige meting klikken en het attributiemodel rechtstreeks vanuit de tabel aanpassen.

1. (Optioneel) Deel de metrische gegevens met andere gebruikers in uw organisatie, zoals beschreven in [Berekende maatstaven delen](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-sharing.md).
