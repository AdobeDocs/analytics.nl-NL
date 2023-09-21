---
title: Gemiddelde paginaweergaven per bezoek
description: Het gemiddelde aantal keren dat een dimensie-item tijdens een bezoek werd weergegeven.
feature: Metrics
exl-id: fef6e803-e819-4f0f-8cb0-c565328a8bea
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Gemiddelde paginaweergaven per bezoek

De afmeting &#39;Gemiddelde paginaweergaven per bezoek&#39; toont hoeveel paginaweergaven er gemiddeld tegen de gewenste afmeting zijn weergegeven. Voor op tijd gebaseerde afmetingen kunt u zien hoe het gemiddelde aantal pagina&#39;s in een bezoek in de loop der tijd wordt weergegeven. Dit [metrisch](overview.md) is handig als u wilt weten hoe vaak items met dimensies tijdens een bezoek worden weergegeven.

>[!TIP]
>
>Deze metrische waarde gebruiken naast een andere metrische waarde (zoals [Bezoeken](visits.md)) om betere inzichten te verkrijgen. Als u deze metrisch op zich gebruikt, krijgt u afmetingspunten die anomalische paginameningen per bezoek bevatten, die typisch niet waardevol is.

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde wordt berekend met behulp van de formule [`Page views`](page-views.md)` divided by `[`Visits`](visits.md).

## Percentage boven 100%

Deze metrische waarde bevat vaak percentages boven 100%. De noemer is de gemiddelde paginaweergaven van de hele dimensie per bezoek. De teller is de gemiddelde paginaweergaven per bezoek van het dimensie-item. Als de gemiddelde paginaweergaven van de gehele dimensie per bezoek lager zijn dan de gemiddelde paginaweergaven per bezoek van een bepaald dimensie-item, ziet u percentages boven 100%. Als u gerangschikte rapporten sorteert op basis van deze maateenheid, worden afwijkende gemiddelde paginaweergaven per bezoek weergegeven. Dit is doorgaans niet waardevol. Adobe beveelt sorteren met een andere metrische waarde aan, zoals [Bezoeken](visits.md), in gerangschikte verslagen.
