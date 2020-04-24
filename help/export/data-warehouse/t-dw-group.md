---
description: Stappen die beschrijven hoe de beheerders de Warehouse van Gegevens kunnen toelaten die toegang tot een groep gebruikers melden.
title: Gebruikersgroep Data Warehouse toevoegen
topic: Data warehouse
uuid: d89294db-caa3-4044-b70d-65b512b0dc1c
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Gebruikersgroep Data Warehouse toevoegen

Stappen die beschrijven hoe de beheerders de Warehouse van Gegevens kunnen toelaten die toegang tot een groep gebruikers melden.

1. Klik op **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL User Management]**.
1. Klik op **[!UICONTROL Edit Groups]**.
1. Klik op **[!UICONTROL Add New User Group]**.
1. Typ in de **[!UICONTROL Define User Group]** sectie een naam in het veld Groepsnaam. Geef de volgende groepsinformatie:

   Bijvoorbeeld, `Data Warehouse Access`.
1. Typ een beschrijving in het **[!UICONTROL Group Description]** veld.
1. Selecteer in de **[!UICONTROL Report Suite Access]** sectie de rapportsuites waartoe u groepsleden toegang wilt geven.
1. Onder [!UICONTROL Tools], laat **[!UICONTROL All Tools]**. toe.

   U kunt ook klikken **[!UICONTROL Customize]** en vervolgens inschakelen **[!UICONTROL Custom Data Warehouse Report]**.

1. Voeg onder [!UICONTROL Assign User Logins]de gewenste gebruikersaanmeldingen toe.
1. Klik op **[!UICONTROL Save Group]**.

   De volgende keer dat de gebruikers aan deze groepsaanmelding hebben toegevoegd, wordt de optie Data Warehouse toegevoegd aan het [!UICONTROL Reports & Analytics] menu.

   >[!NOTE]
   >
   >In het geval van conflicterende toestemmingen (zoals een gebruiker die aan twee groepen wordt toegewezen, waarvan één toegang tot een eigenschap ontkent en andere verleent die zelfde toegang), beperkt het systeem toestemming. De gebruikers die tot groepen behoren die de toegang van het gegevenspakhuis ontkennen kunnen uit die groepen moeten worden verwijderd.

>[!MORELIKETHIS]
>
>* [Groepen](/help/admin/user-management2/c-user-groups/groups.md)

