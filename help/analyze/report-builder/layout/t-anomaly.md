---
description: Stappen die beschrijven hoe te om een verzoek van de anomalieopsporing in rapportbouwer tot stand te brengen.
title: Een aanvraag voor anomaliedetectie configureren
uuid: 1e504ff9-df88-4fa7-95ea-1ca05a6f9c0d
feature: Report Builder
role: User, Admin
exl-id: 0a8b1971-8d32-424a-9d41-d7ab2af54d1e
source-git-commit: ce7f953b8f7f1f7d0616074454e4401937fcc0c7
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 7%

---

# Een aanvraag voor anomaliedetectie configureren

Een verzoek voor afwijkingsdetectie maken in de rapportbuilder:

1. Selecteer een trended-rapport, zoals een **[!UICONTROL Site Metrics]** > **[!UICONTROL Traffic]** verslag.
1. In de [!UICONTROL Apply Granularity] menu, selecteert u **[!UICONTROL Day]**.

   >[!NOTE]
   >
   >De [!UICONTROL Anomaly Detection] is alleen beschikbaar als u Daggranulariteit selecteert. De voorgaande 30 dagen met gegevens worden gebruikt als de trainingsperiode voor statistische gegevens, ongeacht het datumbereik dat u selecteert.

1. Na het configureren van datumbereiken klikt u op **[!UICONTROL Next]**.

   Stap Resultaat 1. Op de wizard Verzoek: Stap 2 van 2, voeg metrisch toe, zoals **[!UICONTROL Visits]**.

   Stap Resultaat 1. Voor toegevoegde metrisch, klik **[!UICONTROL None]** koppeling.

   ![Stap Resultaat](assets/anomaly_select.png)

1. Selecteren **[!UICONTROL Anomaly Detection]** > **[!UICONTROL `<selection>`]**.

   ![Stapinfo](assets/anomaly_visit.png)

   Als u een van deze opties selecteert, maakt het systeem een kopie van de originele metrische waarde voor de anomaly-detectie. Voor de metrische weergave Bezoek wordt bijvoorbeeld een metrische waarde voor Boundbezoek toegevoegd aan de metrische waarde [!UICONTROL Metric] groep.
1. Klikken **[!UICONTROL Finish]** en selecteer de cel voor uitvoer naar Excel.

   Zie [Anomaly Detection](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md) voor definities.
