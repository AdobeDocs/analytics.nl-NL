---
description: U kunt anomalieën in een lijst of in een lijngrafiek bekijken.
title: Anomalieën weergeven in Analysis Workspace
feature: Anomaly Detection
role: User, Admin
exl-id: 32edc7f4-c9b9-472a-b328-246ea5b54d07
source-git-commit: 984406d00e5a5ae966fff60ec9fcfcb000958696
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 2%

---

# Anomalieën weergeven in Analysis Workspace

U kunt anomalieën in een lijst of in een lijngrafiek bekijken.

## anomalieën in een tabel weergeven {#section_869A87B92B574A38B017A980ED8A29C5}

U kunt anomalieën in een tijdreeks Freeform Lijst bekijken.

1. Selecteer het pictogram voor kolominstellingen in de kolomkop en zorg ervoor dat de knop [!UICONTROL **Anomalies**] wordt geselecteerd in de lijst met opties. Zie voor meer informatie [Kolominstellingen](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md).

1. Klik buiten het instellingenmenu om de bijgewerkte tabel weer te geven.

   ![](assets/anomaly_detected.png)

1. In de tabel worden als volgt anomen weergegeven:

   A **donkergrijze driehoek** wordt in de rechterbovenhoek van elke rij weergegeven waarin een anomalie in de gegevens wordt gedetecteerd.

   De kleur **verticale lijn** in elke rij wordt de verwachte waarde aangegeven. De kleur **schaduwgebied** in elke rij wordt de werkelijke waarde aangegeven. Hoe de lijn (verwachte waarde) vergelijkt met het gearceerde gebied (werkelijke waarde) bepaalt of er een anomalie is. (Een waarneming wordt op basis van de in [Statistische technieken voor de opsporing van anomalieën](/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md).)

1. Selecteer het grijze driehoekje rechtsboven in een rij om details over de anomalie weer te geven. Dit geeft de mate (als percentage) aan waarin de werkelijke waarde boven of onder de verwachte waarde afwijkt.

## anomalieën weergeven in een lijndiagram {#section_7C1192AFDB4345A8A2CCFB3AE0C47D82}

De grafieken van de lijn zijn de enige visualisatie die u toestaat om anomalieën te bekijken.

Om anomalieën in een lijngrafiek te bekijken:

1. Selecteer het instellingenpictogram in de visualisatiekoptekst en zorg er vervolgens voor dat de optie [!UICONTROL **anomalieën tonen**] wordt geselecteerd in de lijst met opties. Zie voor meer informatie [Lijn](/help/analyze/analysis-workspace/visualizations/line.md).

1. (Optioneel) Als u wilt dat het betrouwbaarheidsinterval het diagram schaalt, selecteert u het instellingenpictogram in de visualisatiekop en selecteert u vervolgens de optie. **[!UICONTROL Allow anomalies to Scale Y-axis]**.

   Deze optie is niet standaard geselecteerd, omdat het diagram hierdoor soms minder leesbaar wordt.

1. Klik buiten het instellingenmenu om het bijgewerkte lijndiagram weer te geven.

   ![](assets/anomaly_linechart.png)

   Anomalies worden als volgt in het lijndiagram weergegeven:

   A **witte stip** verschijnt op de regel waar een anomalie in de gegevens wordt gedetecteerd. (Een waarneming wordt op basis van de in [Statistische technieken voor de opsporing van anomalieën](/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md).)

   De **lichtschaduwgebied** is de betrouwbaarheidsband, of het verwachte bereik, waar waarden moeten voorkomen. Elke waarde die buiten dit verwachte bereik valt, is een anomalie.

   Als u veelvoudige metriek in het lijndiagram hebt, slechts worden de anomalieën getoond en u moet over elke anomalie bewegen om de betrouwbaarheidsband voor die metrisch te zien.

   De **stippellijn** is de exacte verwachte waarde.

1. Klik op een anomalie (witte stip) om de volgende informatie weer te geven:

   * De datum waarop de anomalie is opgetreden

   * De onbewerkte waarde van de anomalie

   * De percentagewaarde boven of onder de verwachte waarde, die door de stevige groene lijn wordt vertegenwoordigd.

   * De koppeling Analyseren om Contribute-analyse te starten

     (Zie [Overzicht van anomalische detectie](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md) voor meer informatie .)





