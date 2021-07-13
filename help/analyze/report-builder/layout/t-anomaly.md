---
description: Stappen die beschrijven hoe te om een verzoek van de anomalieopsporing in rapportbouwer tot stand te brengen.
title: Een aanvraag voor anomaliedetectie configureren
uuid: 1e504ff9-df88-4fa7-95ea-1ca05a6f9c0d
feature: Report Builder
role: User, Admin
exl-id: 0a8b1971-8d32-424a-9d41-d7ab2af54d1e
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 8%

---

# Een aanvraag voor anomaliedetectie configureren

Stappen die beschrijven hoe te om een verzoek van de anomalieopsporing in rapportbouwer tot stand te brengen.

1. Selecteer een trended rapport, zoals een **[!UICONTROL Site Metrics]** > **[!UICONTROL Traffic]** rapport.
1. Selecteer **[!UICONTROL Day]** in het menu [!UICONTROL Apply Granularity].

   >[!NOTE]
   >
   >Het menu [!UICONTROL Anomaly Detection] is alleen beschikbaar wanneer u Daggranulariteit selecteert. De voorgaande 30 dagen met gegevens worden gebruikt als de trainingsperiode voor statistische gegevens, ongeacht het datumbereik dat u selecteert.

1. Na het vormen van datumwaaiers, klik **[!UICONTROL Next]**.

   Stap Resultaat 1. Op de wizard Verzoek: Stap 2 van 2, voeg metrisch, zoals **[!UICONTROL Visits]** toe.

   Stap Resultaat 1. Voor toegevoegde metrisch, klik **[!UICONTROL None]** verbinding.

   ![Stap Resultaat](assets/anomaly_select.png)

1. Selecteer **[!UICONTROL Anomaly Detection]** > **[!UICONTROL `<selection>`]**.

   ![Stapinfo](assets/anomaly_visit.png)

   Als u een van deze opties selecteert, maakt het systeem een kopie van de originele metrische waarde voor de anomaly-detectie. Bijvoorbeeld, voor metrisch Bezoek, wordt de Ondergrens metrische waarde van het Bezoek toegevoegd aan de [!UICONTROL Metric] groep.
1. Klik **[!UICONTROL Finish]** en selecteer de cel voor output aan Excel.

   Zie [Anomaly Detection](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md) voor definities.
