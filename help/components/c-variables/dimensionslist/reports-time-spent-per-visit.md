---
description: 'null'
title: Tijd besteed per bezoek
topic: Reports
uuid: 76441e36-b7fe-4cf3-8d72-c51d558afa13
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Tijd besteed per bezoek

Adobe Analytics biedt verschillende manieren om de tijd in analyserapporten te bepalen. In de meeste gevallen wordt de doorgebrachte tijd als volgt berekend:

1. Kijk voor een bepaald bezoek naar de tijdstempel van de eerste hit.
2. Vergelijk deze hit met de tijdstempel van de laatste hit van het bezoek.
3. De hoeveelheid tijd die tussen deze twee treffers is verstreken bepaalt hoeveel tijd voor dat bezoek wordt besteed.

Houd rekening met het volgende wanneer u tijd doorbrengt met afmetingsgegevens:

* Zowel paginaweergaven als raakvlaktypen worden in aanmerking genomen bij het berekenen van gegevens die tijd doorbrengen.
* De tijd die wordt doorgebracht wordt niet gemeten tijdens de laatste hit van het bezoek, aangezien er geen volgende afbeeldingsverzoek is om de verstreken tijd te meten.
* Bounces kan geen tijd meten die is besteed, aangezien het bezoek bestaat uit één enkele hit.

De tijd die per bezoek wordt doorgebracht, meet de totale verstreken tijd tijdens een bezoek. Er bestaan verschillende afmetingen tussen **korrelig** en **gespet**.

* **Korrelig:** Elke afmetingswaarde is een verschillend aantal seconden die omhoog een bezoek maken.
* **Emmerd:** Elke afmetingswaarde is een vooraf gedefinieerd emmertje:
   * Minder dan 1 minuut
   * 1-5 minuten
   * 5-10 minuten
   * 30-60 minuten
   * 1-2 uur
   * 2-5 uur
   * 5-10 uur
   * 10-15 uur
   * 15+ uur

>[!NOTE] De [bezoeken](../c-metrics/metrics-visit.md) eindigen gewoonlijk na 12 uur activiteit. Bezoeken kunnen echter meer dan 12 uur duren als gebruik wordt gemaakt van tijdstempels of gegevensbronnen.

Deze dimensie is gebaseerd op bezoeken. Vergelijk deze dimensie met [Tijd besteed aan pagina](reports-time-spent-on-page.md), die een op hit-Gebaseerde dimensie is.
