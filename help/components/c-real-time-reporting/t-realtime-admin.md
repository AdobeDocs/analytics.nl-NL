---
description: Administratieve stappen voor vestiging real-time rapporten.
title: Realtimerapporten configureren
feature: Real-time
exl-id: 9e7fc67c-71d5-465a-9553-5bb7e02a9bfd
source-git-commit: ee55349a8c676023a5ce33b56592cad7642199b8
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 2%

---

# Realtimerapporten configureren

De volgende informatie bevat administratieve stappen voor vestiging real-time rapporten.

Dit bestaat uit het selecteren van de rapportsuite en het configureren van maximaal drie rapporten voor deze suite.

1. Selecteer de rapportsuite waarvoor u realtime rapporten wilt inschakelen.

   1. Selecteer in Analysis Workspace de optie [!UICONTROL **Werkruimte**] tab, dan selecteren [!UICONTROL **Rapporten**] > [!UICONTROL **Betrokkenheid**] > **[!UICONTROL Real-Time]**.

   1. Selecteer de rapportreeks van drop-down bij de bovenkant:

      ![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/assets/report_suite_selector.png)

      Als u probeert om rapporten in real time voor een rapportreeks te bekijken die niet opstelling voor rapportering in real time is, een berichtvertoningen die u aan opstelling de rapportreeks toelaat.

      ![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/assets/rep_suite_not_set_up.png)

1. Selecteren **[!UICONTROL Configure]** om de [!UICONTROL Report Suite Manager].

   (Ook beschikbaar onder **[!UICONTROL Analytics]** > **[!UICONTROL Admin > Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Real-Time]**.)

1. De knop **[!UICONTROL Enable Real-Time]** instellen.
1. Opstelling gegevensinzameling in real time voor maximaal drie rapporten, met één metrische en drie dimensies of classificaties per rapport.

   ![](assets/real_time_admin.png)

   Voor informatie over ondersteunde realtime metriek en dimensies raadpleegt u [Ondersteunde maateenheden en Dimensionen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/realtime-metrics.md).

   Als u classificaties hebt gemaakt, worden deze ingesprongen weergegeven onder de dimensie waarvoor ze zijn gedefinieerd:

   ![](assets/classifications.png)

   >[!NOTE]
   >
   >Voor één enkel rapport Real-Time, steunen wij momenteel niet toelatend dubbele dimensies, zelfs als een verschillende classificatie voor elke dimensie wordt geselecteerd.

   Zie voor meer informatie over classificaties [Over classificaties](/help/components/classifications/c-classifications.md).

   >[!NOTE]
   >
   >Sommige dimensies, zoals &#39;Trefwoord zoeken&#39; of &#39;Product&#39;, blijven niet in real-time behouden, zoals ze elders in Adobe Analytics doen. Wanneer u een niet-permanente metrische waarde selecteert, wordt de volgende waarschuwing weergegeven:

   ![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/assets/warning_dimensions.png)

1. Selecteren **[!UICONTROL Save]** of **[!UICONTROL Save and View Report]**.

   Na deze eerste rapportinstelling kan het 20 minuten duren voordat de gegevens beginnen met streamen. Vanaf dat moment zijn de gegevens direct beschikbaar. Voor informatie bij het bekijken van Real-Time rapporten, zie [Een real-time rapport uitvoeren](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/t-running-report-types.html).

1. Door gebrek, hebben alle gebruikers toegang tot Echt - tijd rapporten.
