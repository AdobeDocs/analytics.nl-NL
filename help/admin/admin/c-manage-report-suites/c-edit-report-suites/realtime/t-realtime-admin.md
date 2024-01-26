---
description: Administratieve stappen voor vestiging real-time rapporten.
title: Configuratie van realtime rapporten
feature: Real-time
exl-id: e039ed67-3694-40fc-a4d9-3cb576e0535c
source-git-commit: b8efacacf7fca792b4a4fa41dd3f9d6ac1448578
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# Configuratie van realtime rapporten

Administratieve stappen voor vestiging real-time rapporten.

Het instellen van realtime rapporten in Adobe Analytics bestaat uit het selecteren van de rapportsuite en het configureren van maximaal drie rapporten voor deze suite. Door gebrek, hebben alle gebruikers toegang tot Echt - tijd rapporten.

1. Selecteer de rapportsuite waarvoor u realtime rapporten wilt inschakelen.

   Navigeren naar **[!UICONTROL Analytics]** > **[!UICONTROL Reports]** > **[!UICONTROL View All Reports > Site Metrics]** > **[!UICONTROL Real-Time]** en selecteer de rapportreeks van drop-down bij de bovenkant:

   ![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/assets/report_suite_selector.png)

   Als u probeert om rapporten in real time voor een rapportreeks te bekijken die niet opstelling voor rapportering in real time is, een berichtvertoningen die u aan opstelling de rapportreeks toelaat.

   ![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/assets/rep_suite_not_set_up.png)

1. Klikken **[!UICONTROL Configure]** (tandwielpictogram) om het [!UICONTROL Report Suite Manager].

   (Ook beschikbaar onder **[!UICONTROL Analytics]** > **[!UICONTROL Admin > Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Real-Time]**.)

1. De knop **[!UICONTROL Enable Real-Time]** instellen.
1. Opstelling gegevensinzameling in real time voor maximaal drie rapporten, met één metrische en drie dimensies of classificaties per rapport.

   ![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/assets/real_time_admin.png)

   Voor informatie over ondersteunde realtime metriek en dimensies raadpleegt u [Ondersteunde maateenheden en Dimensionen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/realtime-metrics.md).

   Als u classificaties hebt gemaakt, worden deze ingesprongen weergegeven onder de dimensie waarvoor ze zijn gedefinieerd:

   ![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/assets/classifications.png)

   >[!NOTE]
   >
   >Voor één enkel rapport Real-Time, steunen wij momenteel niet toelatend dubbele dimensies, zelfs als een verschillende classificatie voor elke dimensie wordt geselecteerd.

   Zie voor meer informatie over classificaties [Over classificaties](/help/components/classifications/c-classifications.md).

   >[!NOTE]
   >
   >Sommige dimensies, zoals &#39;Trefwoord zoeken&#39; of &#39;Product&#39;, blijven niet in real-time behouden, zoals ze elders in Adobe Analytics doen. Wanneer u een niet-permanente metrische waarde selecteert, wordt de volgende waarschuwing weergegeven:

   ![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/assets/warning_dimensions.png)

1. Klik op **[!UICONTROL Save]**.

   Na deze eerste rapportinstelling kan het 20 minuten duren voordat de gegevens beginnen met streamen. Vanaf dat moment zijn de gegevens direct beschikbaar.

1. Navigeer naar:

   **[!UICONTROL Workspace]** > **[!UICONTROL Reports]** > **[!UICONTROL Engagement]** > **[!UICONTROL Real-Time]**.

