---
description: Stappen die beschrijven hoe de beheerders Data Warehouse kunnen toelaten meldend toegang tot een groep gebruikers.
title: Gebruikersgroep Data Warehouse toevoegen
feature: Data Warehouse
uuid: d89294db-caa3-4044-b70d-65b512b0dc1c
exl-id: 8737ab60-2ad1-4795-808b-d0200078a333
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 10%

---

# Gebruikersgroep Data Warehouse toevoegen

Stappen die beschrijven hoe de beheerders Data Warehouse kunnen toelaten meldend toegang tot een groep gebruikers.

1. Klik op **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL User Management]**.
1. Klik op **[!UICONTROL Edit Groups]**.
1. Klik op **[!UICONTROL Add New User Group]**.
1. Typ in de sectie **[!UICONTROL Define User Group]** een naam in het veld Groepsnaam. Geef de volgende groepsinformatie:

   Bijvoorbeeld, `Data Warehouse Access`.
1. Typ een beschrijving in het veld **[!UICONTROL Group Description]**.
1. Selecteer in de sectie **[!UICONTROL Report Suite Access]** de rapportsuites waartoe u groepsleden toegang wilt geven.
1. Schakel onder [!UICONTROL Tools] **[!UICONTROL All Tools]** in.

   U kunt ook op **[!UICONTROL Customize]** klikken en **[!UICONTROL Custom Data Warehouse Report]** inschakelen.

1. Voeg onder [!UICONTROL Assign User Logins] de gewenste gebruikersaanmeldingen toe.
1. Klik op **[!UICONTROL Save Group]**.

   De volgende keer dat gebruikers aan deze groepsaanmelding zijn toegevoegd, wordt de optie Data Warehouse toegevoegd aan het menu [!UICONTROL Reports & Analytics].

   >[!NOTE]
   >
   >In het geval van conflicterende toestemmingen (zoals een gebruiker die aan twee groepen wordt toegewezen, waarvan één toegang tot een eigenschap ontkent en andere verleent die zelfde toegang), beperkt het systeem toestemming. De gebruikers die tot groepen behoren die de toegang van het gegevenspakhuis ontkennen kunnen uit die groepen moeten worden verwijderd.

>[!MORELIKETHIS]
>
>* [Groepen](/help/admin/user-management2/c-user-groups/groups.md)

