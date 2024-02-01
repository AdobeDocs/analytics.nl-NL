---
description: Het systeem van de Intelligente Alarm staat voor meer korrelige controle over alarm toe en integreert anomalieopsporing met het waakzame systeem.
title: Intelligente waarschuwingen
feature: Alerts
exl-id: 1b23211e-7632-4b33-a27d-c58b3bbbbab1
source-git-commit: be5a73347d417c8dc6667d4059e7d46ef5f0f5cd
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 6%

---

# Intelligente waarschuwingen

Het systeem van de Intelligente Alarm staat voor meer korrelige controle over alarm toe en integreert anomalieopsporing met het waakzame systeem.

Hier volgt een video-overzicht:

>[!VIDEO](https://video.tv.adobe.com/v/25446/?quality=12)

## Overzicht {#section_6AC8CA81DEA94E99B0F192B60D0FDF03}

>[!IMPORTANT]
>
>Intelligente waarschuwingen zijn beschikbaar voor Adobe [!DNL Analytics] Eerste en Adobe [!DNL Analytics] Alleen ultieme klanten.

Met intelligente waarschuwingen kunt u

* Berichten opbouwen op basis van anomalieën (90%, 95%, 99%, 99,75% en 99,9% drempelwaarden; procentuele verandering; boven/onder).
* Een voorvertoning bekijken van het aantal keren dat een melding is geactiveerd.
* Een melding sturen via e-mail of sms, met koppelingen naar automatisch gegenereerde Analysis Workspace-projecten.
* &#39;Gestapelde&#39; meldingen maken waarbij meerdere metrics zijn opgenomen in één waarschuwing.

De componenten van het waakzame systeem omvatten: De Bouwer van de alarm, Manager van de Alarm, Voorproef van de Alarm, en betere in-context toegang tot het creëren van alarm. De oude gebruikersinterface van het waarschuwingssysteem is niet meer beschikbaar, maar de waarschuwingen worden gemigreerd. Enkele oude waarschuwingsfuncties [zijn niet meer beschikbaar](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/alerts.html).

Er zijn drie manieren om naar de Waarschuwingsbouwer te gaan:

* Met de volgende sneltoets in Analysis Workspace:

  `ctrl (or cmd) + shift + a`
* Door rechtstreeks naar de waarschuwingsBuilder te gaan:  **[!UICONTROL Workspace]** > **[!UICONTROL Components]** > **[!UICONTROL New Alert]** .
* Door een of meer vrije regelitems voor tabellen te selecteren, klikt u met de rechtermuisknop en selecteert u **[!UICONTROL Create Alert from Selection]**. Hiermee wordt de waarschuwingsBuilder geopend en wordt de builder vooraf gevuld met de juiste maateenheden en filters die uit de tabel zijn toegepast. U kunt de waarschuwing vervolgens bewerken, indien nodig.

  ![](assets/create-alert-from-selection.png)


## Veelgestelde vragen: hoe waarschuwingen worden berekend en geactiveerd {#trigger}

De procentuele drempels zijn standaardafwijkingen. 95% = 2 standaardafwijkingen en 99% = 3 standaardafwijkingen. Afhankelijk van de tijdsgranulariteit die u kiest, [verschillende modellen](/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md) worden gebruikt om te berekenen hoe ver weg (hoeveel standaardafwijkingen) elk gegevenspunt van de norm is. Als u een lagere drempel instelt (bijvoorbeeld 90%), krijgt u meer anomalieën dan wanneer u een hogere drempel instelt (99%). 99,75% &amp; 99,99% drempels werden ingevoerd specifiek voor de uurgranulariteit zodat het niet zoveel anomalieën zou veroorzaken.

+++ Hoe ver gaat de anomaliedetectie van de waarschuwing om anomalieën in de gegevens vast te stellen?

De trainingsperiode is afhankelijk van de geselecteerde korreligheid. Zie Statistische technieken gebruikt in <a href="/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md">Anomaly Detection</a> voor meer details. Hier volgt een overzicht:

* Maandelijks = 15 maanden + zelfde marge vorig jaar
* Wekelijks = 15 weken + zelfde marge vorig jaar
* Dagelijks = 35 dagen + zelfde waaier vorig jaar
* Uur = 336 uur

+++

+++ Mag ik de functie voor anomalie gebruiken of moet ik een absolute waarde gebruiken om alleen te worden gewaarschuwd voor een dip in gedrag of alleen voor een piek in gedrag?

Het gebruiken van de absolute waarde zou alarm op dips evenals pieken nog teweegbrengen. U kunt waarschuwingen niet isoleren voor alleen dips of alleen pieken.

+++

+++ Kan ik alarm vormen om slechts tijdens bepaalde uren van de dag (zoals kantooruren vs. niet-bedrijfsuren) teweeg te brengen?

Op dit moment, nee.

+++

+++ Kan ik een tabel krijgen van de &quot;verwachte waarden&quot; die de stippellijn vormen, of een soort output van wat die waarden zijn?

Niet in Workspace, maar in Report Builder. Zie [deze video](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/exporting/report-builder/anomaly-detection-in-report-builder.html) over Anomaly Detection in Report Builder.

Houd er rekening mee dat Report Builder minder geavanceerde afwijkingsdetectiemethoden gebruikt. Het gebruikt een vaste opleidingsperiode van 30 dagen, vaste 95% interval.

+++
