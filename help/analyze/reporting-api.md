---
description: Bronnen en koppelingen voor de API voor rapportage.
title: API voor analyserapportage
uuid: 68ec3490-6e47-4606-860d-dd5e89c574a1
feature: API
role: Developer
exl-id: 003a8b83-6ef0-4313-903a-b76078558d55
source-git-commit: d173a6c6c9751a86f4218ec842da17da14f8485b
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 5%

---

# API voor analyserapportage

Documentatie voor de Adobe Analytics API&#39;s is ingeschakeld [Adobe Developer](https://developer.adobe.com/analytics-apis/docs/2.0/).

## Vergelijking van analyse-API&#39;s

| **API-type** | **Volledig verwerkt** | **Real-time** | **Livestream** | **Data Warehouse** |
| --- | --- | --- | --- | --- |
| **Beschrijving** | Volledig verwerkte, voltooide gegevens die in alle interfaces van Analytics beschikbaar zijn. | Gedeeltelijk verwerkte, beperkte metriek beschikbaar binnen seconden van inzameling. | Gedeeltelijk verwerkte raakgegevens beschikbaar binnen seconden na verzameling. | Volledig verwerkte, afgeronde gegevens die worden gebruikt om grote gegevensuitvoer te trekken. |
| [**Latentie**](/help/technotes/latency.md) | 30-90 minuten | Seconden - 10 minuten | Seconden - 10 minuten | 90+ minuten |
| **Verwerking voltooid** | Volledig | Gedeeltelijk | Gedeeltelijk | Volledig |
| **Rapportageinterfaces** | Analysis Workspace, Report Builder, API | Real-Time rapport in Report Builder, 1.4 API | Alleen API | Data Warehouse, API |
| **Korreligheid gegevens** | Samengevat | Samengevat | Niveau aanpassen | Samengevat |
| **Bezoekersprofiel verwerken** | Ja | Nee | Nee | Ja |
| **Segmentondersteuning** | Ja | Nee | Nee | Gedeeltelijk |
