---
description: Administratieve stappen voor vestiging real-time rapporten.
title: Rapporten in real time configureren
feature: Real-time
exl-id: 9e7fc67c-71d5-465a-9553-5bb7e02a9bfd
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# Rapporten in real time configureren

De volgende informatie bevat administratieve stappen voor vestiging real-time rapporten.

Dit bestaat uit het selecteren van de rapportsuite en het configureren van maximaal drie rapporten voor deze suite.

1. Selecteer de rapportsuite waarvoor u realtime rapporten wilt inschakelen.

   1. In Analysis Workspace, selecteer het [!UICONTROL **Workspace**] lusje, dan uitgezochte [!UICONTROL **Rapporten**] > [!UICONTROL **Betrokkenheid**] > **[!UICONTROL Real-Time]**.

   1. Selecteer de rapportreeks van drop-down bij de bovenkant:

      ![](/help/admin/tools/manage-rs/edit-settings/realtime/assets/report_suite_selector.png)

      Als u probeert om rapporten in real time voor een rapportreeks te bekijken die niet opstelling voor rapportering in real time is, een berichtvertoningen die u aan opstelling de rapportreeks toelaat.

      ![](/help/admin/tools/manage-rs/edit-settings/realtime/assets/rep_suite_not_set_up.png)

1. Selecteer **[!UICONTROL Configure]** om de [!UICONTROL Report Suite Manager] uit te voeren.

   (Ook beschikbaar onder **[!UICONTROL Analytics]** > **[!UICONTROL Admin > Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Real-Time]** .)

1. Schakel de instelling **[!UICONTROL Enable Real-Time]** in.
1. Opstelling gegevensinzameling in real time voor maximaal drie rapporten, met één metrische en drie dimensies of classificaties per rapport.

   ![](assets/real_time_admin.png)

   Voor informatie over gesteunde metriek in real time en dimensies, zie [ Gesteunde Metriek en Dimensies ](/help/admin/tools/manage-rs/edit-settings/realtime/realtime-metrics.md).

   Als u classificaties hebt gemaakt, worden deze ingesprongen weergegeven onder de dimensie waarvoor ze zijn gedefinieerd:

   ![](assets/classifications.png)

   >[!NOTE]
   >
   >Voor één enkel rapport Real-Time, steunen wij momenteel niet toelatend dubbele dimensies, zelfs als een verschillende classificatie voor elke dimensie wordt geselecteerd.

   >[!NOTE]
   >
   >Sommige dimensies, zoals &#39;Trefwoord zoeken&#39; of &#39;Product&#39;, blijven niet in real-time behouden, zoals ze elders in Adobe Analytics doen. Wanneer u een niet-permanente metrische waarde selecteert, wordt de volgende waarschuwing weergegeven:

   ![](/help/admin/tools/manage-rs/edit-settings/realtime/assets/warning_dimensions.png)

1. Selecteer **[!UICONTROL Save]** of **[!UICONTROL Save and View Report]** .

   Na deze eerste rapportinstelling kan het 20 minuten duren voordat de gegevens beginnen met streamen. Vanaf dat moment zijn de gegevens direct beschikbaar.

1. Door gebrek, hebben alle gebruikers toegang tot Echt - tijd rapporten.
