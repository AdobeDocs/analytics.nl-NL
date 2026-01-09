---
description: Begrijp hoe te om alarm te gebruiken TCP voor korrelige controle over berichten, en integratie met anomalieopsporing toestaat.
title: Overzicht van waarschuwingen
feature: Alerts
exl-id: 1b23211e-7632-4b33-a27d-c58b3bbbbab1
source-git-commit: f02b660b551f5291443b8f7c5c51179a06b22eb9
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 3%

---

# Overzicht van waarschuwingen

Met waarschuwingen in Adobe Analytics kunt u op basis van gewijzigde percentages of specifieke gegevenspunten op de hoogte worden gesteld.

Afhankelijk van het Adobe Analytics-pakket kunt u ook waarschuwingen gebruiken die op basis van afwijkende drempelwaarden moeten worden geactiveerd. Deze alarm (die ook als *wordt bekend Intelligente Alarm*) verstrekt korrelige controles die met [&#x200B; Anomaly Detection &#x200B;](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md) integreren, die teweegbrengen wanneer u hen het meest nodig hebt.

Met waarschuwingen kunt u:

* Geef een voorvertoning weer van hoe vaak een waarschuwing wordt geactiveerd.
* Een melding sturen via e-mail of sms, met koppelingen naar automatisch gegenereerde Analysis Workspace-projecten.
* Creeer *gestapelde* alarm dat veelvoudige metriek in één enkel alarm vangt.
* Berichten maken op basis van:
   * Anomalies in metriek die bestaan, boven, of onder verwachte drempelwaarden zijn.

     [&#x200B; Anomaly opsporing &#x200B;](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md) bouwt een verwachte waarde plus een bovengrens en ondergrens gebruikend historische gegevens. Als de werkelijke metrische waarde boven de bovengrens ligt of onder de ondergrens die als drempelwaarde is gedefinieerd, wordt die gebeurtenis beschouwd als een anomalie op het niveau van het betrouwbaarheidsniveau van de drempelwaarde en wordt de waarschuwing geactiveerd. Een hogere drempelwaarde (bijvoorbeeld 99% of 99,9%) impliceert een bredere bandbreedte, wat leidt tot minder waarschuwingen die worden veroorzaakt door meer extreme anomalieën. Een lagere drempelwaarde (bijvoorbeeld: 90%) impliceert een kleinere bandbreedte, wat leidt tot meer waarschuwingen die worden veroorzaakt door minder extreme anomalieën.
   * Veranderingen in metriek met een specifiek percentage.
   * Metrisch die boven, onder of gelijk aan een bepaalde waarde zijn. (alleen beschikbaar voor Adobe Analytics-klanten met een Select-, Prime- of Ultimate-pakket)

Dit [&#x200B; videoleerprogramma &#x200B;](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/data-science/intelligent-alerts) verstrekt een basisoverzicht van alarm.


## Anomalische zoekopdracht voor waarschuwingen

>[!NOTE]
>
>Het gebruiken van alarm met anomalieopsporing (die ook als _Intelligente Alarm_ wordt bekend) is beschikbaar slechts aan organisaties met een pakket van Adobe Analytics Prime of van Ultimate.

Als een waarschuwing afwijkende detectie gebruikt, varieert de trainingsperiode op basis van de voor de waarschuwing geselecteerde granulariteit.

* Maandelijkse granulariteit: 15 maanden + zelfde marge vorig jaar
* Wekelijkse granulariteit: 15 weken + zelfde bereik vorig jaar
* Dagelijkse granulariteit: 35 dagen + zelfde bereik vorig jaar
* Urogranulariteit: 336 uur

Voor meer informatie, zie [&#x200B; Statistische technieken die in Anomaly Detection &#x200B;](/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md) worden gebruikt.

## Waarschuwingen maken

Voor informatie over hoe te om alarm in Adobe Analytics tot stand te brengen, zie [&#x200B; alarm &#x200B;](/help/components/alerts/alert-builder.md) creëren.

>[!IMPORTANT]
>
>Het gebruik van tijdstempelgegevens voor het maken van waarschuwingen kan ervoor zorgen dat waarschuwingen onjuist worden afgespeeld. Adobe raadt aan om niet-tijdstempelgegevens te gebruiken voor waarschuwingen.

## Waarschuwingen beheren

U kunt bestaande waarschuwingen beheren in het venster Waarschuwingen. U kunt verschillende beheertaken uitvoeren voor waarschuwingen, zoals labelen, hernoemen, verwijderen en meer.

Voor meer informatie over hoe te om bestaand alarm in Adobe Analytics te beheren, zie [&#x200B; alarm &#x200B;](/help/components/alerts/alert-manager.md) leiden.
