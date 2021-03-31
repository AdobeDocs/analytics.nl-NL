---
description: Het nieuwe systeem voor intelligente waarschuwingen biedt meer gedetailleerde controle over waarschuwingen en integreert de detectie van anomalieën met het waarschuwingssysteem.
title: Overzicht van intelligente waarschuwingen
uuid: b9bf75ad-bb6f-49fe-8c55-355ea3c50a71
feature: AI-gereedschappen
role: Bedrijfs Praktijk, Beheerder
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 7%

---


# Overzicht van intelligente waarschuwingen

Intelligente waarschuwingen zorgen voor meer korrelige controle over waarschuwingen en integreren anomaliedetectie met het waarschuwingssysteem.

Hier volgt een videozelfstudie op [Intelligente waarschuwingen](https://docs.adobe.com/content/help/en/analytics-learn/tutorials/data-science/intelligent-alerts.html) (5:34)

## Overzicht

De nieuwe Alert Builder en Alert Manager in Analysis Workspace vervangen de bestaande waarschuwingsfunctionaliteit in Rapporten &amp; Analytics. Met intelligente waarschuwingen kunt u:

* Berichten opstellen op basis van anomalieën (90%, 95%, 99%, 99,75% en 99,9% drempelwaarden; % wijziging; boven/onder)
* Een voorvertoning bekijken van het aantal keren dat een melding is geactiveerd
* Een melding sturen via e-mail of sms, met koppelingen naar automatisch gegenereerde Analysis Workspace-projecten
* &quot;gestapelde&quot; waarschuwingen maken die meerdere meetgegevens vastleggen in één waarschuwing

Er zijn vier manieren om naar de Waarschuwingsbouwer te gaan:

* Ga rechtstreeks naar de Alert Builder:  **[!UICONTROL Components]** > **[!UICONTROL Alerts]**
* De sneltoets in Workspace gebruiken: `Ctrl + Shift + A` (Windows) of `Cmd + Shift + A` (Mac)
* Het selecteren van één of meerdere punt/s van de vrije lijstlijn van de vrije vorm, het met de rechtermuisknop klikken en het selecteren **[!UICONTROL Create Alert from Selection]**. Hiermee opent u de waarschuwingsfunctie en vult u de juiste metingen en filters die uit de tabel zijn toegepast, vooraf in. U kunt de waarschuwing desgewenst bewerken.

   ![Berichtgeving maken van selectie](assets/create-alert-from-selection.png)

* Vanuit een rapport Rapporten &amp; Analytics door naar **[!UICONTROL More]** > **[!UICONTROL Add Alert]** te gaan. Dit opent de waakzame bouwer en vult vooraf de aangewezen metriek en de filters die van het rapport worden toegepast. U kunt de waarschuwing desgewenst bewerken.

   ![Waarschuwing toevoegen](assets/add-alert.png)

De percentagedrempels zijn standaardafwijkingen. 95% = 2 standaardafwijkingen en 99% = 3 standaardafwijkingen. Afhankelijk van de tijdsgranulariteit die u kiest, worden [verschillende modellen](../virtual-analyst/c-anomaly-detection/statistics-anomaly-detection.md) gebruikt om te berekenen hoe ver weg (hoeveel standaardafwijkingen) elk gegevenspunt van de norm is. Als u een lagere drempel instelt (bijvoorbeeld 90%), krijgt u meer anomalieën dan wanneer u een hogere drempel instelt (99,75%).

>[!IMPORTANT]
>
>Het gebruik van tijdstempelgegevens voor het maken van waarschuwingen kan ervoor zorgen dat waarschuwingen onjuist worden afgespeeld. Adobe raadt u aan niet-tijdstempelgegevens te gebruiken voor Intelligent Alerts.

## Anomalische zoekopdracht voor waarschuwingen

Als een waarschuwing afwijkende detectie gebruikt, varieert de trainingsperiode op basis van de voor de waarschuwing geselecteerde granulariteit.

* Maandelijkse granulariteit: 15 maanden + zelfde waaier vorig jaar
* Wekelijkse korreligheid: 15 weken + zelfde marge vorig jaar
* Dagelijkse granulariteit: 35 dagen + zelfde waaier vorig jaar
* Uurgranulariteit: 336 uur

Zie [Statistische technieken gebruikt in Anomaly Detection](../virtual-analyst/c-anomaly-detection/statistics-anomaly-detection.md) voor meer informatie.
