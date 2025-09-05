---
description: Administratieve stappen voor vestiging real-time rapporten.
title: Configuratie van realtime rapporten
feature: Real-time
exl-id: e039ed67-3694-40fc-a4d9-3cb576e0535c
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 1%

---

# Configuratie van realtime rapporten

Administratieve stappen voor vestiging real-time rapporten.

Het instellen van realtime rapporten in Adobe Analytics bestaat uit het selecteren van de rapportsuite en het configureren van maximaal drie rapporten voor deze suite. Door gebrek, hebben alle gebruikers toegang tot Echt - tijd rapporten.

1. Selecteer de rapportsuite waarvoor u realtime rapporten wilt inschakelen.

   Ga naar **[!UICONTROL Analytics]** > **[!UICONTROL Admin > Report Suites]**.

1. Klik op **[!UICONTROL Edit Settings]** > **[!UICONTROL Real-Time]** .

1. Opstelling gegevensinzameling in real time voor maximaal drie rapporten, met één metrische en drie dimensies of classificaties per rapport.

   ![](/help/admin/tools/manage-rs/edit-settings/realtime/assets/real_time_admin.png)

   Voor informatie over gesteunde metriek in real time en dimensies, zie [ Gesteunde Metriek en Dimensies ](/help/admin/tools/manage-rs/edit-settings/realtime/realtime-metrics.md).

   Als u classificaties hebt gemaakt, worden deze ingesprongen weergegeven onder de dimensie waarvoor ze zijn gedefinieerd:

   ![](/help/admin/tools/manage-rs/edit-settings/realtime/assets/classifications.png)

   >[!NOTE]
   >
   >Voor één enkel rapport Real-Time, steunen wij momenteel niet toelatend dubbele dimensies, zelfs als een verschillende classificatie voor elke dimensie wordt geselecteerd.

   >[!NOTE]
   >
   >Sommige dimensies, zoals &#39;Trefwoord zoeken&#39; of &#39;Product&#39;, blijven niet in real-time behouden, zoals ze elders in Adobe Analytics doen. Wanneer u een niet-permanente metrische waarde selecteert, wordt de volgende waarschuwing weergegeven:

   ![](/help/admin/tools/manage-rs/edit-settings/realtime/assets/warning_dimensions.png)

1. Klik op **[!UICONTROL Save]**.

   Na deze eerste rapportinstelling kan het 20 minuten duren voordat de gegevens beginnen met streamen. Vanaf dat moment zijn de gegevens direct beschikbaar.

1. Navigeer naar:

   **[!UICONTROL Workspace]** > **[!UICONTROL Reports]** > **[!UICONTROL Engagement]** > **[!UICONTROL Real-Time]**

