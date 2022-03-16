---
title: Tijd besteed per bezoek (afmetingen)
description: De totale duur van het bezoek.
feature: Dimensions
exl-id: f241eb2d-7e22-47ee-ade8-8aeb7b2b9694
source-git-commit: 10ff98f7ca4697afe5c2dae66be415c0d68c4aac
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---

# Tijd besteed per bezoek

*Deze Help-pagina beschrijft hoe &#39;Tijd besteed per bezoek&#39; werkt als hun respectievelijke afmetingen. Zie de [Tijd besteed per bezoek](../metrics/time-spent-per-visit.md) metrisch voor meer informatie.*

In de afmetingen van de &#39;Tijd besteed per bezoek&#39; wordt de hoeveelheid tijd vastgelegd die een bezoeker aan het hele bezoek heeft doorgebracht. Hierbij worden de volgende stappen gebruikt om de berekening te meten:

1. Kijk naar de tijdstempel van de eerste hit van het bezoek.
2. Vergelijk deze hit met de tijdstempel van de laatste hit van het bezoek.
3. De hoeveelheid tijd die tussen deze twee hits is verstreken, draagt bij aan de tijd die is besteed.

Deze afmetingen zijn handig als u wilt weten hoe lang bezoekers uw site in het algemeen gebruiken.

>[!TIP]
>
>De tijd die besteed wordt vereist minstens twee hits in een bezoek om tijd te meten. Bezoeken die bestaan uit één hit worden niet weergegeven in deze dimensie.

Deze dimensie is gebaseerd op bezoeken. Dit betekent dat de waarde van toepassing is op elke hit tijdens het bezoek en niet verandert. Vergelijk deze dimensie met [Tijd besteed aan pagina](time-spent-on-page.md), een op raakvlakken gebaseerde dimensie.

Deze dimensie houdt verband met de [Gemiddelde tijd besteed aan site](../metrics/average-time-on-site.md) en [Tijd besteed per bezoek](../metrics/time-spent-per-visit.md) metriek.

## Deze dimensie vullen met gegevens

Deze dimensies werken uit de doos voor alle implementaties. Als een rapportsuite gegevens bevat, werken deze dimensies.

## Dimension-items

Er zijn meerdere afmetingen voor de tijd die per bezoek wordt doorgebracht:

* **Tijd doorgebracht per bezoek - ingekapseld**: De hoeveelheid tijd wordt opgesloten. Dimension-items kunnen variëren van `"Less than 1 minute"` tot `"More than 15 hours"`. Bezoekingen duren gewoonlijk niet langer dan 12 uur; de bezoeken kunnen echter meer dan 12 uur duren wanneer gebruik wordt gemaakt van tijdstempels of gegevensbronnen .
* **Tijd besteed per bezoek - korrelig**: Elk aantal seconden is een uniek afmetingsitem. Deze dimensie is niet beschikbaar in Rapporten &amp; Analytics of Data Warehouse.

Zie [Overzicht van de tijd](../metrics/time-spent.md) voor meer algemene informatie over de bestede tijd.
