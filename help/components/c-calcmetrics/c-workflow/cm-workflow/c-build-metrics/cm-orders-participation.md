---
description: Verklaart hoe te om metrisch tot stand te brengen die toont welke Kanalen van de Marketing in rijorden bijwonen. Dit kan aan om het even welke dimensie of succesgebeurtenis van belang worden aangepast.
title: Cijfers voor hulp bij bestellingen
feature: Calculated Metrics
exl-id: 33cb441d-d003-408d-ba67-1bcdd0e821ff
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 3%

---

# Cijfers voor hulp bij bestellingen

Verklaart hoe te om metrisch tot stand te brengen die toont welke Kanalen van de Marketing in rijorden bijwonen. Dit kan aan om het even welke dimensie of succesgebeurtenis van belang worden aangepast.

1. In de Berekende Bouwer van Metriek, noem metrische &quot;Begeleide Orders&quot;.
1. In het canvas van de Definitie, sleep in metrische orde. Pas vervolgens het toewijzingsmodel aan met het instellingenset door de **[!UICONTROL Use non-default attribution models]** selectievakje.

   ![](assets/attr-model.png)

1. Selecteren **[!UICONTROL Custom]** als het attributiemodel. Wijzig de gewichten in 0 (startpunt), 100 (speler) en 0 (dichter).

   ![](assets/custom-attr-model.png)

1. Sla de metrische waarde op.
1. Creeer een vrije vormlijst in Analysis Workspace met de afmeting van het Kanaal van de Marketing, Orders en uw nieuwe Begeleidende metrische Orden.

   ![](assets/mktg-channel-assists.png)

Dit is een eenvoudige manier om te zien welke marketingkanalen hebben geholpen bij het bestellen van rijbewijzen. U kunt ook vanuit een vrije-vormtabel met de rechtermuisknop op elke willekeurige meting klikken en het attributiemodel rechtstreeks vanuit de tabel aanpassen.
