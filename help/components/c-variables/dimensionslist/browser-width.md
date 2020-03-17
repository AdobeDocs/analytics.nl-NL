---
description: Metrische gegevens die alleen in het browservenster verwijzen naar de horizontale/verticale afstand van de gegevens. Meer specifiek, browser
title: Breedte/hoogte browser
topic: Metrics
uuid: 1c0d3ea9-e001-4152-9bfc-8fe6406bc755
translation-type: tm+mt
source-git-commit: ''

---


# Breedte/hoogte browser

Metrische gegevens die alleen in het browservenster verwijzen naar de horizontale/verticale afstand van de gegevens. Meer specifiek, browser

Adobe Analytics gebruikt de browserhoogte en -breedte alleen vanaf de eerste hit van een bezoek. De rest van de treffers krijgt niet de attributie voor hetzelfde bezoek.
De breedte/hoogte van de browser legt vergelijkbare maar duidelijke waarden vast in vergelijking met de grootte [van het](/help/components/c-variables/dimensionslist/reports-mobile.md#topic_D306EA4558194488AC47A45B9C570150)mobiele scherm.

Als u bijvoorbeeld de breedte of hoogte van de browser indeelt op mobiele resolutie, moet u rekening houden met het volgende:

* De resoluties van het mobiele apparaat zijn de fysieke waarden die aan het apparaat zijn gekoppeld. Onder Resolutie van mobiel apparaat zou de Galaxy S8 bijvoorbeeld verschijnen als 2.960 x 1.440. De resolutie van het mobiele apparaat wordt opgehaald van een service van derden nadat het apparaat is geïdentificeerd.
* Bij de waarden voor Browserhoogte en Breedte ziet u daarentegen de (logische) CSS-waarden van 740 x 360. De browserwaarden zijn afhankelijk van de Javascript-/CSS-gegevens.
* Voor een korte bespreking, zie [deze draad](https://stackoverflow.com/questions/8785643/what-exactly-is-device-pixel-ratio).

