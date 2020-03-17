---
description: Administratieve stappen voor vestiging real-time rapporten.
title: Rapporten in real time configureren
topic: Admin tools
uuid: a2c3c515-55f2-4c64-ac92-a86d75e78a86
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Rapporten in real time configureren

Administratieve stappen voor vestiging real-time rapporten.

Het opzetten van rapporten in real time binnen [!UICONTROL Reports & Analytics] bestaat uit het selecteren van de rapportreeks en het vormen van tot drie rapporten voor het.

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

   Zie [Ondersteunde metriek en afmetingen](/help/components/c-real-time-reporting/realtime-metrics.md)voor informatie over ondersteunde realtime metriek en afmetingen.

   Als u classificaties hebt gemaakt, worden deze ingesprongen weergegeven onder de dimensie waarvoor ze zijn gedefinieerd:

   ![](assets/classifications.png)

   >[!NOTE]
   >
   >Voor één enkel rapport Real-Time, steunen wij momenteel niet toelatend dubbele dimensies, zelfs als een verschillende classificatie voor elke dimensie wordt geselecteerd.

   Zie [Informatie over classificaties](/help/components/c-classifications2/c-classifications.md)voor meer informatie over classificaties.

   >[!NOTE]
   >
   >Bepaalde afmetingen, zoals &#39;Trefwoord zoeken&#39; of &#39;Product&#39;, blijven niet in real-time behouden, zoals elders in Adobe Analytics. Wanneer u een niet-permanente metrische waarde selecteert, wordt de volgende waarschuwing weergegeven:

   ![](assets/warning_dimensions.png)

1. Klik **[!UICONTROL Save]** of **[!UICONTROL Save and View Report]**.

   Na deze eerste rapportinstelling kan het 20 minuten duren voordat de gegevens beginnen met streamen. Vanaf dat moment zijn de gegevens direct beschikbaar. Voor informatie bij het bekijken van rapporten in real time, zie [Looppas een Rapport](https://marketing.adobe.com/resources/help/en_US/sc/user/reports_realtime.html)in real time.

1. Door gebrek, hebben alle gebruikers toegang tot Echt - tijd rapporten.
