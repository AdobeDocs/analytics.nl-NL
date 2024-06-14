---
description: Het nieuwe systeem van de Intelligente Alarm staat voor meer korrelige controle over alarm toe en integreert anomalieopsporing met het waakzame systeem.
title: Overzicht van intelligente waarschuwingen
feature: Alerts
role: User, Admin
exl-id: 49d47896-bf93-4960-b647-2765c935eb25
source-git-commit: a012aca08740428671f216793dbd12aa15f21448
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# Overzicht van intelligente waarschuwingen

Met intelligente waarschuwingen (of alleen &#39;waarschuwingen&#39;) in Adobe Analytics kunt u direct op de hoogte worden gesteld wanneer zich abnormale gebeurtenissen in uw gegevens voordoen.

U kunt waarschuwingen instellen die moeten worden geactiveerd op basis van afwijkende drempelwaarden, gewijzigde percentages of specifieke gegevenspunten. Alarm verstrekt korrelige controles die met integreren [Anomaly Detection](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md), activeren wanneer je ze het meest nodig hebt.

Met intelligente waarschuwingen kunt u:

* Waarschuwingen opbouwen op basis van anomalieën (90%, 95%, 99%, 99,75% en 99,9% drempels; procentuele wijziging; boven/onder))
* Voorbeeld van hoe vaak een waarschuwing wordt geactiveerd
* Waarschuwingen verzenden via e-mail of SMS met koppelingen naar automatisch gegenereerde Analysis Workspace-projecten
* &quot;gestapelde&quot; waarschuwingen maken die meerdere meetgegevens vastleggen in één waarschuwing

De volgende videozelfstudie biedt een eenvoudig overzicht van waarschuwingen: [Intelligente waarschuwingen](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/data-science/intelligent-alerts.html) (5:34)

## Anomalische zoekopdracht voor waarschuwingen

Als een waarschuwing afwijkende detectie gebruikt, varieert de trainingsperiode op basis van de voor de waarschuwing geselecteerde granulariteit.

* Maandelijkse granulariteit: 15 maanden + zelfde marge vorig jaar
* Wekelijkse granulariteit: 15 weken + zelfde bereik vorig jaar
* Dagelijkse granulariteit: 35 dagen + zelfde bereik vorig jaar
* Urogranulariteit: 336 uur

Zie voor meer informatie [Statistische technieken voor anomalische detectie](/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md).

## Waarschuwingen maken

Voor informatie over het maken van waarschuwingen in Adobe Analytics raadpleegt u [Waarschuwingen maken](/help/analyze/analysis-workspace/c-intelligent-alerts/alert-builder.md).

>[!IMPORTANT]
>
>Het gebruik van tijdstempelgegevens voor het maken van waarschuwingen kan ervoor zorgen dat waarschuwingen onjuist worden afgespeeld. Adobe raadt u aan om niet-tijdstempelgegevens te gebruiken voor intelligente waarschuwingen.

## Waarschuwingen beheren

U kunt bestaande waarschuwingen beheren in het venster Waarschuwingen. U kunt verschillende beheertaken uitvoeren voor waarschuwingen, zoals labelen, hernoemen, verwijderen en meer.

Ga voor meer informatie over het beheren van bestaande waarschuwingen in Adobe Analytics naar [Waarschuwingen beheren](/help/analyze/analysis-workspace/c-intelligent-alerts/alert-manager.md).
