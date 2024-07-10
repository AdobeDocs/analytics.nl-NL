---
description: Gebruikers van Analytics en hun middelen beheren in de Adobe Admin Console.
title: Gebruikers en middelen voor Analyse beheren
feature: Admin Tools
exl-id: 849a8279-4850-4458-bdd2-85052a17ee21
role: Admin
source-git-commit: 869b44b826de5cb35d13000133092397cb16ccaa
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 0%

---

# Oudere gebruikersaccounts, middelen, verlopen beheren

U kunt accounts van oudere gebruikers, hun migratiestatus, de vervalgegevens, de overdracht van elementen naar andere gebruikers en meer beheren met **[!UICONTROL Admin]> [!UICONTROL All Admin] >[!UICONTROL Analytics users & admin]**.

Het scherm Gebruikers toont een lijst van huidige gebruikers van Adobe Analytics, met de volgende kolommen:

| Kolom | Beschrijving |
|---|---|
| [!UICONTROL User ID] | De gebruikers-id die de gebruiker gebruikt om zich aan te melden bij Adobe Analytics. |
| [!UICONTROL Name] | De naam van de gebruiker. |
| [!UICONTROL Migration status] | De status van de migratie van een verouderde gebruikersaccount naar een Enterprise ID of Adobe ID.  De status kan niet worden gestart, in de wachtrij worden geplaatst of worden gemigreerd. |
| [!UICONTROL Email] | De e-mail van de gebruiker. |
| [!UICONTROL Legacy login] | De status van oudere aanmelding, die kan worden ingeschakeld of uitgeschakeld. |
| [!UICONTROL Date created] | Tijdstempel wanneer de gebruikersaccount in de Adobe Analytics is gemaakt. |
| [!UICONTROL Last Analytics access] | Tijdstempel voor de laatste toegang van de gebruikersaccount tot Adobe Analytics; |
| [!UICONTROL Expiration] | Datum waarop de gebruikersaccount vervalt, of Geen als de gebruikersaccount niet vervalt. |

![Gebruikers](assets/users.png)

- Als u naar een bepaalde gebruiker wilt zoeken, gebruikt u de opdracht ![Zoeken](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Search_18_N.svg) *Zoeken op titel* veld.
- Selecteer ![Chevron](https://spectrum.adobe.com/static/icons/ui_18/ChevronSize100.svg) **[!UICONTROL Migration status]**.
- Selecteer ![Chevron](https://spectrum.adobe.com/static/icons/ui_18/ChevronSize100.svg) **[!UICONTROL Legacy login]**.
- Selecteer ![Kolominstellingen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ColumnSettings_18_N.svg) en selecteer de kolommen uit popup.

U kunt verschillende acties toepassen wanneer u een of meer gebruikers in de lijst selecteert:

| Handeling | Beschrijving |
|---|---|
| ![Migreren](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Briefcase_18_N.svg) **[!UICONTROL Migrate]** | U kunt een of meer gebruikers migreren naar Enterprise-id&#39;s of Adobe-id&#39;s. |
| ![Kalender vergrendeld](https://spectrum.adobe.com/static/icons/workflow_18/Smock_CalendarLocked_18_N.svg) **[!UICONTROL Set expiration]** | U kunt een vervaldatum instellen voor het gebruik van de oudere Adobe Analytics-aanmelding voor de geselecteerde gebruikers.  Selecteer de datum die u wilt gebruiken voor een kalenderpop-up om de datum op te geven. Selecteren **[!UICONTROL Done]** om de vervaldatum te bevestigen. |
| ![Overdrachtsmiddelen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Switch_18_N.svg) **[!UICONTROL Transfer assets]** | Deze actie is alleen beschikbaar als u één gebruiker selecteert. Als de gebruiker elementen heeft die kunnen worden overgedragen, kunt u de accountitems selecteren (zoals bladwijzers, dashboards en meer). Selecteren **[!UICONTROL Transfer]** om de overdracht te voltooien.<br/>![Activa overdragen](assets/transfer-assets.png) |
| ![Accounts verwijderen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Delete_18_N.svg) **[!UICONTROL Delete accounts]** | Er wordt een dialoogvenster weergegeven waarin wordt bevestigd dat de geselecteerde accounts zijn verwijderd. Selecteren **[!UICONTROL OK]** om de accounts te verwijderen. Selecteren **[!UICONTROL Cancel]** om te annuleren. |
| ![Exporteren naar CSV](https://spectrum.adobe.com/static/icons/workflow_18/Smock_FileCSV_18_N.svg) **[!UICONTROL Export to CSV]** | Met deze actie downloadt u direct een bestand met een lijst met door komma&#39;s gescheiden waarden van de geselecteerde gebruikers met hun gegevens (naam, migratiestatus, e-mail, enzovoort). |

