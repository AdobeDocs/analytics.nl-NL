---
title: Intelligente gegevens vloeiend maken
description: Leer hoe Intelligent Gegevens Vloeiend maken historische tendensen analyseert om de waarde van metrisch binnen een beïnvloede tijdspanne te voorspellen.
feature: AI-gereedschappen
role: User, Admin
source-git-commit: a9d892ab8caaeb797fbbd9b5aa136c5dab76f8bd
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 1%

---

# Intelligente gegevens vloeiend maken

In zeldzame gevallen kunnen sommige factoren de gegevenskwaliteit beïnvloeden. Het verkeer, de implementatieveranderingen, of de dienstverstoringen kunnen allen de integriteit van de verzamelde gegevens beïnvloeden. Zij maken ook een analyse ingewikkelder van de manier waarop de gebeurtenis de volledigheid van de gegevens kan hebben beïnvloed.

Intelligente gegevenseffening is een prototype in [Analytics Labs](/help/analyze/labs.md) dat kan helpen deze mening te voltooien door historische tendensen te analyseren om de waarde van metrisch binnen de beïnvloede tijdspanne te voorspellen. Het prototype past geavanceerde machine het leren algoritmen toe om de verwachte waarden voor metriek over de tijdspanne te plotten die wordt geanalyseerd.

## Intelligente gegevens vloeiend maken

1. Ga naar Adobe Analytics Labs:
   ![Labs](assets/labs.png)
1. Start het prototype Intelligent Data Smoothing.
   ![Prototype starten](assets/intelligent-ds.png)
1. Voeg metrisch toe die aan de lijst moet worden geanalyseerd Freeform. Het prototype werkt alleen met een dagelijkse korreligheid, dus zorg ervoor dat de afmeting in de tabel Dag is.
   ![Metrisch toevoegen](assets/add-metric.png)
1. Kies een datumbereik dat breder is dan het venster van de gebeurtenis, maar zorg ervoor dat dit de gebeurtenis bevat.
   ![Datumbereik](assets/date-range.png)
1. Klik op het tandwielpictogram voor de metrische waarde in de tabel Vrije vorm.
   ![Tandwiel](assets/gear-icon.png)
1. Selecteer onder [!UICONTROL Data Settings] de optie [!UICONTROL Data smoothing].
   ![Gegevens vloeiend maken](assets/column-setting.png)
1. Selecteer het datum-/datumbereik dat overeenkomt met de gebeurtenis en klik op [!UICONTROL Apply].
Zorg ervoor dat het gegevensbereik voor het vloeiend maken van gegevens een subset is van het datumbereik dat is geselecteerd voor het deelvenster. De metrische waarde in de tabel en grafiek wordt vervangen door de voorspelde waarden.
   ![Voorspelde waarden](assets/predictive-values.png)
