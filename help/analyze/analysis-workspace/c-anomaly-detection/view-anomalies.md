---
description: Begrijp hoe u gegevensanomalieën in Analysis Workspace kunt bekijken en analyseren.
title: Anomalies weergeven
feature: Anomaly Detection
role: User, Admin
exl-id: 32edc7f4-c9b9-472a-b328-246ea5b54d07
source-git-commit: b4c1636bdc9d5be522b16f945a46beabf4f7a733
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 0%

---

# anomalieën weergeven

U kunt anomalieën in Analysis Workspace in een lijst of in een lijngrafiek bekijken.

## anomalieën in een tabel weergeven {#section_869A87B92B574A38B017A980ED8A29C5}

U kunt anomalieën in een tijdreeks Freeform Lijst bekijken.

1. Selecteer het ![ Plaatsen ](/help/assets/icons/Setting.svg) in de kolomkopbal, dan zorg ervoor dat de **[!UICONTROL Anomalies]** optie in de lijst van opties wordt geselecteerd. Voor meer informatie, zie [ montages van de Kolom ](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md).

1. In de tabel worden als volgt anomen weergegeven:

   ![ ontdekte Anomalies ](assets/anomaly-detected.png)

   Een ◥ verschijnt in de hoger-juiste hoek van elke rij waar een gegevensanomalie wordt ontdekt.

   De **gekleurde verticale lijn** in elke rij ➋ wijst op de verwachte waarde. Het **gekleurde gearceerde gebied** in elke rij ➊ wijst op de daadwerkelijke waarde. Hoe de lijn (verwachte waarde) vergelijkt met het gearceerde gebied (werkelijke waarde) bepaalt of er een anomalie is. (Een observatie wordt beschouwd als anomalisch gebaseerd op de geavanceerde statistische technieken die in [ worden beschreven Statistische technieken die in anomalieopsporing ](/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md) worden gebruikt.)

1. Selecteer ◥ in de rechterbovenhoek van een rij om details over de anomalie weer te geven. Dit geeft de mate (als percentage) aan waarin de werkelijke waarde boven of onder de verwachte waarde afwijkt.
1. Selecteer [ Open Analyse van de Bijdrage ](run-contribution-analysis.md) om de bijdrageanalyse te beginnen.

## anomalieën weergeven in een lijndiagram

De grafieken van de lijn zijn de enige visualisatie die u toestaat om anomalieën te bekijken.

Om anomalieën in een lijngrafiek te bekijken:

1. Selecteer ![ Plaatsend ](/help/assets/icons/Setting.svg) in de visualisatiekop, dan zorg ervoor dat [!UICONTROL **anomalieën**] optie toont in de lijst van opties wordt geselecteerd. Voor meer informatie, zie [ Lijn ](/help/analyze/analysis-workspace/visualizations/line.md).

1. (Facultatief) om het betrouwbaarheidsinterval toe te staan om de grafiek te schrapen, uitgezochte ![ Plaatsend ](/help/assets/icons/Setting.svg) in de visualisatiekop, dan de optie, **[!UICONTROL Allow anomalies to Scale Y-axis]**.

   Deze optie is niet standaard geselecteerd, omdat het diagram hierdoor soms minder leesbaar wordt.

   Anomalies worden als volgt in het lijndiagram weergegeven:

   ![ Anomaly ontdekte lijnvisualisatie ](assets/anomaly-detected-line.gif)

   A **witte punt** verschijnt op de lijn waar een gegevensanomalie wordt ontdekt. (Een observatie wordt beschouwd als anomalisch gebaseerd op de geavanceerde statistische technieken die in [ worden beschreven Statistische technieken die in anomalieopsporing ](/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md) worden gebruikt.)

   Het **licht gearceerde gebied** is de vertrouwensband, of de verwachte waaier, waar de waarden zouden moeten voorkomen. Elke waarde die buiten dit verwachte bereik valt, is een anomalie.

   Als u veelvoudige metriek in het lijndiagram hebt, slechts worden de anomalieën getoond en u moet over elke anomalie bewegen om de betrouwbaarheidsband voor die metrisch te zien.

   De **gestippelde lijn** is de nauwkeurige verwachte waarde.

1. Selecteer een anomalie (witte punt) om de volgende informatie te bekijken:

   * De datum waarop de anomalie is opgetreden.

   * De ruwe waarde van de anomalie.

   * De percentagewaarde boven of onder de verwachte waarde, die door de stevige groene lijn wordt vertegenwoordigd.

   * De koppeling **[!UICONTROL Analyze]** om Contribute-analyse te starten






