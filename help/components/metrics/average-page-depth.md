---
title: Gemiddelde paginadiepte
description: Hoeveel pagina's gemiddeld bestaat de dimensie.
feature: Metrics
exl-id: 6625405a-bda5-4723-8d22-4bc5b7e44d4e
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Gemiddelde paginadiepte

De &#39;Gemiddelde paginadiepte&#39; [metrisch](overview.md) toont hoe ver een afmetingspunt zich in een bepaald bezoek, gemiddeld uitbreidt. De startpagina (die een dimensie-item is voor de pagina-dimensie) geeft bijvoorbeeld doorgaans een kleinere gemiddelde paginadiepte dan de pagina Bevestiging van aankoop, die waarschijnlijk verder gaat naar een bezoek. Met deze informatie kunt u bepaalde pagina&#39;s optimaliseren voor nieuwe bezoekers als de pagina gemiddeld een lage diepte heeft.

>[!TIP]
>
>Gebruik deze metrische waarde naast een andere metrische waarde, zoals [Bezoeken](visits.md), om betere inzichten te krijgen. Als u deze metrisch op zich gebruikt, zou u afmetingspunten kunnen krijgen die afwijkende paginadiepten bevatten, die typisch geen waardevol inzicht is.

## Hoe deze metrische waarde wordt berekend

De eerste pagina van een bezoek heeft een paginadiepte van `0`. De volgende pagina heeft een paginadiepte van 1 en verhoogt elke paginaweergave tot het einde van het bezoek. Deze metrische waarde neemt alleen toe met de paginaweergave ([`t()`](/help/implement/vars/functions/t-method.md)) vraag, en niet met verbinding het volgen ([`tl()`](/help/implement/vars/functions/tl-method.md)) oproepen.

Voor een bepaald afmetingspunt, voeg alle paginadiepten voor dat afmetingspunt toe, en verdeel het door bezoeken. Het resulterende getal is de gemiddelde paginadiepte, afgerond naar het dichtstbijzijnde gehele getal. Items Dimensionen met een gemiddelde paginadiepte van `0` het betekent dat het vaak op de eerste pagina van het bezoek stond.

Neem bijvoorbeeld het volgende voorbeeld van een bezoek:

```text
Page1 > Page2 > Page2 > Page3 > Page4 > Page2
```

Als we een gemiddelde paginadiepte voor het dimensie-item wilden `Page2`, wordt deze als volgt berekend:

```text
If 'Count repeat instances' is enabled:
(1 + 2 + 5) / 3 = 2.67, rounded up to 3

If 'Count repeat instances' is disabled:
(1 + 4) / 2 = 2.5, rounded up to 3
```

>[!TIP]
>
>Als u de gemiddelde paginadiepte met een decimaal wilt zien, creeer berekende metrisch gebruikend dit metrisch als enig element binnen de formule. Verhoog de decimale posities in berekende metrisch tot het gewenste decimaal.

## Percentage boven 100%

Deze metrische waarde bevat vaak percentages boven 100%. De noemer is de gemiddelde paginadiepte van de gehele dimensie en de teller is de gemiddelde paginadiepte van het dimensie-item.

Als de gemiddelde paginadiepte van de gehele dimensie lager is dan de gemiddelde paginadiepte van een bepaald dimensie-item, ziet u percentages boven 100%. Als u gerangschikte rapporten op basis van deze norm sorteert, worden afwijkende gemiddelde dieptewaarden van de pagina weergegeven. Dit is doorgaans niet waardevol. Adobe beveelt sorteren met een andere metrische waarde aan, zoals [Bezoeken](visits.md), in gerangschikte verslagen.
