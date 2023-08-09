---
description: Leer hoe u een verzoek voor afwijkingsdetectie maakt in Report Builder.
title: Hoe te om een verzoek van de anomalische opsporing te vormen
uuid: 1e504ff9-df88-4fa7-95ea-1ca05a6f9c0d
feature: Report Builder
role: User, Admin
exl-id: 0a8b1971-8d32-424a-9d41-d7ab2af54d1e
source-git-commit: fb39f906d6c08713e4dc8211c917b2942502868e
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---

# Een aanvraag voor anomaliedetectie configureren

Een verzoek voor afwijkingsdetectie maken in Report Builder:

1. Selecteer een trended-rapport, zoals een **[!UICONTROL Site Metrics]** > **[!UICONTROL Traffic]** verslag.
1. In de [!UICONTROL Apply Granularity] menu, selecteert u **[!UICONTROL Day]**.

   >[!NOTE]
   >
   >De [!UICONTROL Anomaly Detection] is alleen beschikbaar als u Daggranulariteit selecteert. De voorgaande 30 dagen met gegevens worden gebruikt als de trainingsperiode voor statistische gegevens, ongeacht het datumbereik dat u selecteert.

1. Na het configureren van datumbereiken klikt u op **[!UICONTROL Next]**.

   Op de Tovenaar van het Verzoek: Stap 2 van 2, voeg metrisch, zoals toe **[!UICONTROL Visits]**.

   Voor toegevoegde metrisch, klik **[!UICONTROL None]** koppeling.

   ![Screenshot met Anomaly Detection, vervolgens Insert en insert options for Lower and Upper Bound and expected.](assets/anomaly_select.png)

1. Selecteren **[!UICONTROL Anomaly Detection]** > **[!UICONTROL `<selection>`]**.

   ![Schermafbeelding met aanvraagwizard Stap 2 - Verkeersrapport.](assets/anomaly_visit.png)

   Als u een van deze opties selecteert, maakt het systeem een kopie van de originele metrische waarde voor de anomaly-detectie. Voor de metrische weergave Bezoek wordt bijvoorbeeld een metrische waarde voor Boundbezoek toegevoegd aan de metrische waarde [!UICONTROL Metric] groep.
1. Klikken **[!UICONTROL Finish]** en selecteer de cel voor uitvoer naar Excel.

   Zie [Anomaly Detection](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md) voor definities.
