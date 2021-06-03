---
description: U kunt gegevensanomalieën contextafhankelijk weergeven en analyseren in Analysis Workspace.
title: Overzicht van anomaliedetectie
uuid: 991fde08-198c-4410-9606-d5a4f3dd8339
feature: AI-gereedschappen
role: Business Practitioner, Administrator
exl-id: b1625206-c774-40ef-9d92-25ee8ff1478d
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 8%

---

# Overzicht van anomaliedetectie

U kunt gegevensanomalieën contextafhankelijk weergeven en analyseren in Analysis Workspace.

[Zelfstudie over](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/data-science/anomaly-detection-in-analysis-workspace.html)  Anomaly Detection (4:53)

[Videozelfstudie](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/data-science/contribution-analysis-workspace.html)  bijdrageanalyse (3:20)

>[!IMPORTANT]
>
>Anomaly Detection is removed from the Reports &amp; Analytics feature set and is now available only via Analysis Workspace. Klanten van Adobe Analytics Select en Adobe Analytics Foundation hebben voortaan alleen via Workspace toegang tot anomaliedetectie voor dagelijkse granulariteit. Voor meer informatie, zie [Anomaly Detection and Contribution Analysis Entitlements](/help/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.md#section_9278D58F21A840AA9B1ED1BD07A1EF0A).

Anomaly Detection biedt een statistische methode om te bepalen hoe een bepaalde metrische waarde is gewijzigd ten opzichte van eerdere gegevens.

Met Anomaly Detection kunt u &quot;echte signalen&quot; scheiden van &quot;ruis&quot; en vervolgens mogelijke factoren identificeren die tot die signalen of anomalieën hebben bijgedragen. Met andere woorden, het laat je zien welke statistische fluctuaties belangrijk zijn en welke niet. U kunt dan de worteloorzaak van een ware anomalie identificeren. Bovendien kunt u betrouwbare metrische (KPI) prognoses krijgen.

Voorbeelden van anomalieën die u kunt onderzoeken zijn:

* Drastische afname in gemiddelde orderwaarde
* Pieken in orders met lage inkomsten
* Spikes of druppels in proefregistraties
* Druppels in weergaven van openingspagina&#39;s
* Spikes in videobuffergebeurtenissen
* Spikes in lage videobitsnelheden

Zowel Anomaly Detection als [Contribution Analysis](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/anomaly-detection/anomaly-detection.html) zijn kernworkflows in Analysis Workspace. U kunt de Analyse van de Bijdrage tegen om het even welke dagelijkse anomalie in werking stellen en het resultaat in uw project van Analysis Workspace inbedden.

Analysis Workspace-algoritme voor het opsporen van anomalieën bevat

* Naast de bestaande dagelijkse granulariteit wordt ook ondersteuning geboden voor granulariteit per uur, week en maand.
* Bewustzijn van seizoensgebondenheid (zoals &quot;Zwarte Vrijdag&quot;) en feestdagen.
