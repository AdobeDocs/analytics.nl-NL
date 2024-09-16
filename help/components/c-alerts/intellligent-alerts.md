---
description: Het systeem van de Intelligente Alarm staat voor meer korrelige controle over alarm toe en integreert anomalieopsporing met het waakzame systeem.
title: Intelligente waarschuwingen
feature: Alerts
exl-id: 1b23211e-7632-4b33-a27d-c58b3bbbbab1
source-git-commit: 2b8688da1400857b7f5093197d06c04681cd87ff
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Overzicht van intelligente waarschuwingen

Met intelligente waarschuwingen (of alleen &#39;waarschuwingen&#39;) in Adobe Analytics kunt u direct op de hoogte worden gesteld wanneer zich abnormale gebeurtenissen in uw gegevens voordoen.

U kunt waarschuwingen instellen die moeten worden geactiveerd op basis van afwijkende drempelwaarden, gewijzigde percentages of specifieke gegevenspunten. Het alarm verstrekt korrelige controles die met [ Anomaly Detectie ](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md) integreren, die teweegbrengen wanneer u hen het meest nodig hebt.

Met intelligente waarschuwingen kunt u:

* Waarschuwingen opbouwen op basis van anomalieën (90%, 95%, 99%, 99,75% en 99,9% drempels; procentuele wijziging; boven/onder))
* Voorbeeld van hoe vaak een waarschuwing wordt geactiveerd
* Waarschuwingen verzenden via e-mail of SMS met koppelingen naar automatisch gegenereerde Analysis Workspace-projecten
* &quot;gestapelde&quot; waarschuwingen maken die meerdere meetgegevens vastleggen in één waarschuwing

Het volgende videoleerprogramma verstrekt een basisoverzicht van alarm: [ Intelligente Alarm ](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/data-science/intelligent-alerts.html) (5:34)

## Anomalische zoekopdracht voor waarschuwingen

Als een waarschuwing afwijkende detectie gebruikt, varieert de trainingsperiode op basis van de voor de waarschuwing geselecteerde granulariteit.

* Maandelijkse granulariteit: 15 maanden + zelfde marge vorig jaar
* Wekelijkse granulariteit: 15 weken + zelfde bereik vorig jaar
* Dagelijkse granulariteit: 35 dagen + zelfde bereik vorig jaar
* Urogranulariteit: 336 uur

Voor meer informatie, zie [ Statistische technieken die in Anomaly Detection ](/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md) worden gebruikt.

## Waarschuwingen maken

Voor informatie over hoe te om alarm in Adobe Analytics tot stand te brengen, zie [ alarm ](/help/components/c-alerts/alert-builder.md) creëren.

>[!IMPORTANT]
>
>Het gebruik van tijdstempelgegevens voor het maken van waarschuwingen kan ervoor zorgen dat waarschuwingen onjuist worden afgespeeld. Adobe raadt u aan om niet-tijdstempelgegevens te gebruiken voor intelligente waarschuwingen.

## Waarschuwingen beheren

U kunt bestaande waarschuwingen beheren in het venster Waarschuwingen. U kunt verschillende beheertaken uitvoeren voor waarschuwingen, zoals labelen, hernoemen, verwijderen en meer.

Voor meer informatie over hoe te om bestaand alarm in Adobe Analytics te beheren, zie [ alarm ](/help/components/c-alerts/alert-manager.md) leiden.
