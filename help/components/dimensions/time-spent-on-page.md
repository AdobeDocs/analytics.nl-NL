---
title: Tijd besteed aan pagina
description: De hoeveelheid tijd die een bezoeker op de pagina heeft doorgebracht.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '286'
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

Deze dimensie is gebaseerd op hit, wat betekent dat de waarde voor elke hit anders is. Vergelijk deze dimensie met [Tijd besteed per bezoek](time-spent-per-visit.md), die een op bezoek-gebaseerde dimensie is. Hogere doorgebrachte tijd betekent dat een bezoeker langer op een pagina bleef (hit).

![Tijd besteed aan pagina](../metrics/assets/time-spent2.png)

## Deze dimensie vullen met gegevens

Deze dimensie werkt uit de doos voor alle implementaties. Als een rapportsuite gegevens bevat, werkt deze dimensie.

## Dimensiewaarden

Er zijn meerdere afmetingen voor de tijd die aan de pagina wordt doorgebracht:

* **Tijd besteed aan pagina - gespaard**: De hoeveelheid tijd wordt opgesloten. Dimensiewaarden variëren van `"Less than 15 seconds"` tot `"More than 30 minutes"`. De tijd tussen paginaweergaven duurt gewoonlijk niet langer dan 30 minuten; de tijd tussen de paginaweergaven kan echter meer dan 30 minuten bedragen als u hits met een tijdstempel of gegevensbronnen gebruikt.
* **Tijd besteed aan pagina - korrelig**: Elk aantal seconden is een unieke afmetingswaarde.

Zie [Tijd besteed overzicht](../metrics/time-spent.md) voor meer algemene informatie over bestede tijd.
