---
title: Tijd besteed aan pagina
description: De hoeveelheid tijd die een bezoeker op de pagina heeft doorgebracht.
feature: Dimensions
exl-id: 55af7286-7c37-48d2-925e-8b7ecb390e7f
source-git-commit: 8700abf6db565cf3a85fb64ee0db1a1634616f59
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Tijd besteed aan pagina

Met de dimensie &#39;Tijd besteed aan pagina&#39; wordt de hoeveelheid tijd vastgelegd die een bezoeker heeft besteed aan de pagina. Hierbij worden de volgende stappen gebruikt om de berekening te meten:

1. Kijk voor een bepaalde hit naar de tijdstempel.
2. Vergelijk deze hit met de tijdstempel van de volgende hit in het bezoek. In zowel de paginaweergave als het bijhouden van koppelingen wordt het aantal treffers weergegeven.
3. De hoeveelheid tijd die tussen deze twee hits is verstreken, draagt bij aan de tijd die is besteed.

Deze dimensie is waardevol wanneer u wilt begrijpen hoe lang bezoekers op uw site op een bepaalde metrische waarde werken.

>[!TIP]
>
>De tijd die wordt besteed wordt niet gemeten voor de laatste hit van het bezoek aangezien er geen volgende beeldverzoek is om verstreken tijd te meten. Dit concept geldt ook voor bezoeken die bestaan uit één enkele hit (een stuit).

Deze dimensie is gebaseerd op hit, wat betekent dat de waarde voor elke hit anders is. Vergelijk deze dimensie met [Tijd besteed per bezoek](time-spent-per-visit.md), een op bezoeken gebaseerde dimensie. Hogere doorgebrachte tijd betekent dat een bezoeker langer op een pagina bleef (hit).

![Tijd besteed aan pagina](../metrics/assets/time-spent2.png)

## Deze dimensie vullen met gegevens

Deze dimensie werkt uit de doos voor alle implementaties. Als een rapportsuite gegevens bevat, werkt deze dimensie.

## Dimension-items

Er zijn meerdere afmetingen voor de tijd die aan de pagina wordt doorgebracht:

* **Tijd doorgebracht op pagina - ingesloten**: De hoeveelheid tijd wordt opgesloten. Dimension-items kunnen variëren van `"Less than 15 seconds"` tot `"More than 30 minutes"`. De tijd tussen treffers duurt gewoonlijk niet langer dan 30 minuten; de tijd tussen hits kan echter meer dan 30 minuten bedragen als u gebruik maakt van tijdstempels of gegevensbronnen .
* **Tijd besteed aan pagina - korrelig**: Elk aantal seconden is een uniek afmetingsitem.

Zie [Overzicht van de tijd](../metrics/time-spent.md) voor meer algemene informatie over de bestede tijd.
