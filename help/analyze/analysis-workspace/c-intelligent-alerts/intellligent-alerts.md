---
description: Het nieuwe systeem van de Intelligente Alarm staat voor meer korrelige controle over alarm toe en integreert anomalieopsporing met het waakzame systeem.
title: Overzicht van intelligente waarschuwingen
feature: Alerts
role: User, Admin
exl-id: 49d47896-bf93-4960-b647-2765c935eb25
source-git-commit: d173a6c6c9751a86f4218ec842da17da14f8485b
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

---

# Overzicht van intelligente waarschuwingen

Intelligente waarschuwingen zorgen voor meer korrelige controle over waarschuwingen en integreren anomaliedetectie met het waarschuwingssysteem.

Hier volgt een videozelfstudie [Intelligente waarschuwingen](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/data-science/intelligent-alerts.html) (5:34)

## Overzicht

De nieuwe Alert Builder en de Manager van de Waarschuwing in Analysis Workspace vervangen de waakzame functionaliteit in Rapporten &amp; Analytics, die eind-van-opgeheven is. Met intelligente waarschuwingen kunt u:

* Waarschuwingen opbouwen op basis van anomalieën (90%, 95%, 99%, 99,75% en 99,9% drempels; procentuele wijziging; boven/onder))
* Voorbeeld van hoe vaak een waarschuwing wordt geactiveerd
* Waarschuwingen verzenden via e-mail of SMS met koppelingen naar automatisch gegenereerde Analysis Workspace-projecten
* &quot;gestapelde&quot; waarschuwingen maken die meerdere meetgegevens vastleggen in één waarschuwing

Er zijn drie manieren om naar de Waarschuwingsbouwer te gaan:

| Methode | Details |
| --- | --- |
| Ga rechtstreeks naar de Waarschuwingsbouwer | **[!UICONTROL Components]** > **[!UICONTROL Alerts]** |
| De sneltoets in Workspace gebruiken | `Ctrl + Shift + A` (Windows) of `Cmd + Shift + A` (Mac) |
| Selecteer een of meer vrije regelitems voor tabellen | Klik met de rechtermuisknop en selecteer **[!UICONTROL Create Alert from Selection]**. Hierdoor wordt het [!UICONTROL Alert Builder] en vult de juiste maateenheden en filters die uit de tabel zijn toegepast vooraf in. U kunt de waarschuwing desgewenst bewerken. ![Berichtgeving maken van selectie](assets/create-alert-from-selection.png) |

De percentagedrempels zijn standaardafwijkingen. 95% = 2 standaardafwijkingen en 99% = 3 standaardafwijkingen. Afhankelijk van de tijdsgranulariteit die u kiest, [verschillende modellen](/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md) worden gebruikt om te berekenen hoe ver weg (hoeveel standaardafwijkingen) elk gegevenspunt van de norm is. Als u een lagere drempel instelt (bijvoorbeeld 90%), krijgt u meer anomalieën dan wanneer u een hogere drempel instelt (99,75%).

>[!IMPORTANT]
>
>Het gebruik van tijdstempelgegevens voor het maken van waarschuwingen kan ervoor zorgen dat waarschuwingen onjuist worden afgespeeld. Adobe raadt u aan om niet-tijdstempelgegevens te gebruiken voor intelligente waarschuwingen.

## Anomalische zoekopdracht voor waarschuwingen

Als een waarschuwing afwijkende detectie gebruikt, varieert de trainingsperiode op basis van de voor de waarschuwing geselecteerde granulariteit.

* Maandelijkse granulariteit: 15 maanden + zelfde marge vorig jaar
* Wekelijkse granulariteit: 15 weken + zelfde bereik vorig jaar
* Dagelijkse granulariteit: 35 dagen + zelfde bereik vorig jaar
* Urogranulariteit: 336 uur

Zie [Statistische technieken voor anomalische detectie](/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md) voor meer informatie .
