---
description: Hiermee geeft u de hoeveelheid tijd weer die bezoekers besteden aan de pagina
title: Tijd besteed op pagina
topic: Reports
translation-type: tm+mt
source-git-commit: ''

---


# Tijd besteed aan pagina

Adobe Analytics biedt verschillende manieren om de tijd in analyserapporten te bepalen. In de meeste gevallen wordt de doorgebrachte tijd als volgt berekend:

1. Voor een bepaalde hit bekijkt u de tijdstempel- en dimensiewaarde.
2. Vergelijk deze hit met de tijdstempel van de volgende hit in het bezoek.
3. De hoeveelheid tijd die tussen deze twee treffers is verstreken, draagt bij aan de tijd die voor die pagina wordt doorgebracht.

Houd rekening met het volgende wanneer u tijd doorbrengt met afmetingsgegevens:

* De tijd die wordt besteed houdt rekening met de toewijzing en de vervaldatum.
* Zowel paginaweergaven als raakvlaktypen worden in aanmerking genomen bij het berekenen van gegevens die tijd doorbrengen.
* De tijd die wordt doorgebracht wordt niet gemeten tijdens de laatste hit van het bezoek, aangezien er geen volgende afbeeldingsverzoek is om de verstreken tijd te meten.
* Bounces kan geen tijd meten die is besteed, aangezien het bezoek bestaat uit één enkele hit.

De tijd die aan pagina wordt doorgebracht meet de verstreken tijd tussen hits in een bezoek. Er bestaan verschillende afmetingen tussen **korrelig** en **gespet**.

* **Korrelig:** Elke waarde van de afmeting is een verschillend aantal seconden doorgebracht tussen twee treffers.
* **Emmerd:** Elke afmetingswaarde is een vooraf gedefinieerd emmertje:
   * Minder dan 15 seconden
   * 15 tot 29 seconden
   * 1 tot 3 minuten
   * 3 tot 5 minuten
   * 5 tot 10 minuten
   * 10 tot 15 minuten
   * 15 tot 20 minuten
   * 20 tot 30 minuten
   * Meer dan 30 minuten

Deze dimensie is gebaseerd op hit-based, wat als gebruikt als onderbreking zinvollere gegevens kan verstrekken. Vergelijk deze dimensie met [Tijd besteed per bezoek](reports-time-spent-per-visit.md), die een op bezoek-gebaseerde dimensie is.

![Tijd besteed](/help/components/c-variables/c-metrics/assets/time-spent1.png)
