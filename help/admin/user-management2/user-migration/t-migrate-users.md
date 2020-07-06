---
description: Gebruikers migreren van het oude Analytics-gebruikersbeheersysteem naar de Admin Console.
title: Analytics-gebruikersaccounts voor Adobe ID’s migreren
uuid: 734e9f14-ef8d-44de-8ff3-3ee6dfe0a214
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 6%

---


# Analytics-gebruikersaccounts voor Adobe ID’s migreren{#migrate-analytics-user-accounts-for-adobe-ids}

Gebruikers migreren van het oude Analytics-gebruikersbeheersysteem naar de Admin Console.

## Analytics-gebruikersaccounts voor Adobe ID’s migreren {#task-f3355f3b14a340feae58cfa04c0ba1c9}

Gebruikers migreren van het oude Analytics-gebruikersbeheersysteem naar de Admin Console.

>[!NOTE]
>
>Als een beheerder die niet via de Experience Cloud is aangemeld, toegang probeert te krijgen tot het migratiehulpprogramma voor gebruikers-id, wordt hij of zij omgeleid naar de aanmeldingspagina van Experience Cloud.

**Analytics-gebruikers migreren**

1. Ga naar **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL User ID Migration]**.

   ![](assets/migration-progress.png)

   De pagina voor migratie van gebruikers-id bestaat uit twee gedeelten: *Voortgang* van migratie en *gebruikersgegevens*.

   **Voortgang van migratie**

   <table id="table_F9F1CFF762C745E198CB075A02BA2DDA"> 
   <thead> 
   <tr> 
      <th colname="col1" class="entry"> Fase </th> 
      <th colname="col2" class="entry"> Beschrijving </th> 
   </tr>
   </thead>
   <tbody> 
   <tr> 
      <td colname="col1"> <p>Migratie voltooid </p> </td> 
      <td colname="col2"> <p>De gebruikers hebben de uitnodiging geaccepteerd. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> <p>Oudere aanmelding uitgeschakeld </p> </td> 
      <td colname="col2"> <p>Aanmelden met de oude bedrijfs-id is uitgeschakeld. Gebruikers hebben nu toegang tot de Experience Cloud via hun Adobe ID of Enterprise ID. Wanneer al uw gebruikers deze fase hebben bereikt, hebt u de migratie voltooid. </p> <p>In de migratie is de oudere aanmelding uitgeschakeld. Gebruikers worden omgeleid naar <span class="filepath"> experience.adobe.com</span> en moeten zich aanmelden met de Adobe ID of de Enterprise ID. </p> </td> 
   </tr> 
   </tbody> 
   </table>

   **Gebruikersgegevens**

   De Informatie van de gebruiker schetst de gebruikers in uw organisatie, die door domeinnaam wordt gescheiden.

   <table id="table_3822E27AF81E4A188562FEB5131548A5"> 
   <thead> 
   <tr> 
      <th colname="col1" class="entry"> Element </th> 
      <th colname="col2" class="entry"> Beschrijving </th> 
   </tr>
   </thead>
   <tbody> 
   <tr> 
      <td colname="col1"> <p>Domein </p> </td> 
      <td colname="col2"> <p>Domeinen zijn specifiek voor de e-mailadressen van de huidige Analytics-gebruikersbasis. Een domein kan slechts door één enkele organisatie worden geclaimd, en slechts kunnen de systeembeheerders een domein eisen. Zie Toegang tot een geclaimd domein <a href="https://helpx.adobe.com/enterprise/help/request-access-to-claimed-domain.html"></a>aanvragen voor meer informatie. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> <p>Gevraagd domein </p> </td> 
      <td colname="col2"> <p>Als u gebruikers als Onderneming of Federated IDs wilt migreren, moet u een Beheerder van het Systeem zijn en een beschikbaar domein via de Admin Console claimen alvorens gebruikers te migreren. Meer weten <a href="https://helpx.adobe.com/enterprise/help/identity.html"> hier</a>? </p> <p>Als u geen domeinen wilt claimen voor Enterprise- of federatieve id's, slaat u deze stap over en migreert u gebruikers als Adobe-id's. Meer informatie over id-typen vindt u <a href="https://helpx.adobe.com/enterprise/help/identity.html"> hier</a>. </p> </td> 
   </tr> 
   </tbody> 
   </table>

1. Zoek het domein met de gebruikers-id&#39;s die u wilt migreren en klik vervolgens onder **[!UICONTROL Requiring Migration]** op **[!UICONTROL Select Users]**.
1. Selecteer op de [!DNL Users] pagina de gebruikers die u wilt migreren en klik op **[!UICONTROL Migrate]**.

   Wanneer u klikt **[!UICONTROL Migrate]**, ontvangen gebruikers een uitnodiging (Migratie gestart) en moeten ze deze accepteren. Hiermee wordt de gebruikersnaam verplaatst naar de voltooide migratie. U kunt hun erfenistoegang vervolgens uitschakelen `[!DNL my.omniture.com].`

   ![](assets/user-info.png)

1. Geef het type id op dat u wilt migreren voor de gebruikers (Adobe ID of Enterprise ID)

   Na het migreren van gebruikers, verandert de status onder de kolom van de Status van de Migratie van *`Not Initiated`* aan *`Migrated`*.

   Als deze optie wordt *`Failed`* weergegeven, plaatst u de muisaanwijzer op het pictogram voor een beschrijving van de oorzaak van de fout.
