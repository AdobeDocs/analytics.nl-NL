---
description: Administratieve stappen voor vestiging real-time rapporten.
title: Configuratie van realtimerapporten
topic: Admin tools
uuid: f48692a0-77c0-4ee4-b3ec-eaa842d06ac8
translation-type: tm+mt
source-git-commit: 6778dd290424651dc959224daa0eef8ebd8196e5
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 2%

---


# Configuratie van realtimerapporten

Administratieve stappen voor vestiging real-time rapporten.

Het instellen van realtime rapporten in Reports &amp; Analytics bestaat uit het selecteren van de rapportsuite en het configureren van maximaal drie rapporten voor deze suite.

1. Selecteer de rapportsuite waarvoor u realtime rapporten wilt inschakelen.

   Navigeer naar **[!UICONTROL Analytics]** > **[!UICONTROL Reports]** > **[!UICONTROL View All Reports > Site Metrics]** > **[!UICONTROL Real-Time]** en selecteer de rapportsuite in het keuzemenu bovenaan:

   ![](assets/report_suite_selector.png)

   Als u probeert om rapporten in real time voor een rapportreeks te bekijken die niet opstelling voor rapportering in real time is, een berichtvertoningen die u aan opstelling de rapportreeks toelaat.

   ![](assets/rep_suite_not_set_up.png)

1. Klik op **[!UICONTROL Configure]** (tandwielpictogram) om de [!UICONTROL Report Suite Manager]selectie uit te voeren.

   (Ook beschikbaar onder **[!UICONTROL Analytics]** > **[!UICONTROL Admin > Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Real-Time]**.)

1. Schakel de **[!UICONTROL Enable Real-Time]** instelling in.
1. Opstelling gegevensinzameling in real time voor maximaal drie rapporten, met één metrische en drie dimensies of classificaties per rapport.

   ![](assets/real_time_admin.png)

   Zie [Ondersteunde statistieken en Dimension](/help/admin/admin/realtime/realtime-metrics.md)voor informatie over ondersteunde realtime-meetgegevens en -afmetingen.

   Als u classificaties hebt gemaakt, worden deze ingesprongen weergegeven onder de dimensie waarvoor ze zijn gedefinieerd:

   ![](assets/classifications.png)

   >[!NOTE]
   >
   >Voor één enkel rapport Real-Time, steunen wij momenteel niet toelatend dubbele dimensies, zelfs als een verschillende classificatie voor elke dimensie wordt geselecteerd.

   Zie [Informatie over classificaties](/help/components/classifications/c-classifications.md)voor meer informatie over classificaties.

   >[!NOTE]
   >
   >Sommige dimensies, zoals &#39;Trefwoord zoeken&#39; of &#39;Product&#39;, blijven niet in real-time behouden, zoals elders in Adobe Analytics. Wanneer u een niet-permanente metrische waarde selecteert, wordt de volgende waarschuwing weergegeven:

   ![](assets/warning_dimensions.png)

1. Klik **[!UICONTROL Save]** of **[!UICONTROL Save and View Report]**.

   Na deze eerste rapportinstelling kan het 20 minuten duren voordat de gegevens beginnen met streamen. Vanaf dat moment zijn de gegevens direct beschikbaar. Voor informatie bij het bekijken van rapporten in real time, zie [Looppas een Rapport](https://docs.adobe.com/content/help/en/analytics/analyze/reports-analytics/t-running-report-types.html)in real time.

1. Door gebrek, hebben alle gebruikers toegang tot Echt - tijd rapporten.
