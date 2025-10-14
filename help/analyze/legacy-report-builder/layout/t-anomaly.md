---
description: Leer hoe u een verzoek voor afwijkingsdetectie maakt in Report Builder.
title: Hoe te om een verzoek van de anomalische opsporing te vormen
uuid: 1e504ff9-df88-4fa7-95ea-1ca05a6f9c0d
feature: Report Builder
role: User, Admin
exl-id: 0a8b1971-8d32-424a-9d41-d7ab2af54d1e
source-git-commit: fcecc8a493852f5682fd7fbd5b9bb484a850922c
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# Een verzoek voor afwijkingsdetectie configureren

{{legacy-arb}}

Een verzoek voor afwijkingsdetectie in Report Builder maken:

1. Selecteer een trended-rapport, zoals een **[!UICONTROL Site Metrics]** > **[!UICONTROL Traffic]** -rapport.
1. Selecteer **[!UICONTROL Day]** in het menu [!UICONTROL Apply Granularity] .

   >[!NOTE]
   >
   >Het menu [!UICONTROL Anomaly Detection] is alleen beschikbaar wanneer u Daggranulariteit selecteert. De voorgaande 30 dagen met gegevens worden gebruikt als de trainingsperiode voor statistische gegevens, ongeacht het datumbereik dat u selecteert.

1. Klik op **[!UICONTROL Next]** nadat u datumbereiken hebt geconfigureerd.

   Voor de Tovenaar van het Verzoek: Stap 2 van 2, voeg metrisch, zoals **[!UICONTROL Visits]** toe.

   Voor toegevoegde metrisch, klik de **[!UICONTROL None]** verbinding.

   ![&#x200B; Schermafbeelding die Anomaly Detection toont dan Tussenvoegsel en neem dan opties voor Onderste en Bovengrens op en verwacht.](assets/anomaly_select.png)

1. Selecteer **[!UICONTROL Anomaly Detection]** > **[!UICONTROL `<selection>`]** .

   ![&#x200B; Screenshot die Stap 2 van de Tovenaar van het Verzoek toont - het Rapport van het Verkeer.](assets/anomaly_visit.png)

   Als u een van deze opties selecteert, maakt het systeem een kopie van de originele metrische waarde voor de anomaly-detectie. Voor de metrische bezoekmethode wordt bijvoorbeeld een maatstaf Bond lager bezoek toegevoegd aan de groep [!UICONTROL Metric] .
1. Klik op **[!UICONTROL Finish]** en selecteer de cel voor uitvoer naar Excel.

   Zie [&#x200B; Anomaly Detection &#x200B;](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md) voor definities.
