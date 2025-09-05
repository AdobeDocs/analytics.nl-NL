---
description: Migreer gebruikers van het verouderde systeem van het de gebruikersbeheer van Analytics aan de Admin Console.
title: Gebruikersaccounts voor Analyse migreren voor Adobe-id's
feature: Admin Tools
exl-id: 198367a1-8156-4cc3-af8a-d92c61699eda
role: Admin
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 1%

---

# Gebruikersaccounts voor Analyse migreren voor Adobe-id&#39;s

Migreer gebruikers van het verouderde systeem van het de gebruikersbeheer van Analytics aan de Admin Console.

>[!NOTE]
>
>Als een beheerder die niet via de Experience Cloud is aangemeld, toegang probeert te krijgen tot het migratiehulpprogramma voor gebruikers-id, wordt hij of zij omgeleid naar de aanmeldingspagina van Experience Cloud.

1. Navigeer naar **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL User ID Migration]** .

   ![](/help/admin/tools/user-management/user-migration/assets/migration-progress.png)

   De pagina van de Migratie van identiteitskaart van de Gebruiker heeft twee secties: *de Voortgang van de Migratie* en *Informatie van de Gebruiker*.

## Voortgang van migratie

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
      <td colname="col2"> <p>Aanmelden met de oude bedrijfs-id is uitgeschakeld. Gebruikers hebben nu toegang tot de Experience Cloud via hun Adobe ID of Enterprise ID. Wanneer al uw gebruikers deze fase hebben bereikt, hebt u de migratie voltooid. </p> <p>In de migratie is de oudere aanmelding uitgeschakeld. Gebruikers worden omgeleid naar <span class="filepath"> experienceCloud.adobe.com </span> en moeten zich aanmelden met de Adobe ID of Enterprise ID. </p> </td> 
   </tr> 
   </tbody> 
   </table>

## Gebruikersgegevens

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
   <td colname="col2"> <p>Domeinen zijn specifiek voor de e-mailadressen van de huidige gebruikersbasis voor Analytics. Een domein kan slechts door één enkele organisatie worden geclaimd, en slechts kunnen de systeembeheerders een domein eisen. Zie <a href="https://helpx.adobe.com/enterprise/help/request-access-to-claimed-domain.html"> Toegang aanvragen tot een geclaimd domein </a> voor meer informatie. </p> </td> 
</tr> 
<tr> 
   <td colname="col1"> <p>Gevraagd domein </p> </td> 
   <td colname="col2"> <p>Als u gebruikers wilt migreren als Enterprise- of federatieve id's, moet u een systeembeheerder zijn en een beschikbaar domein claimen via de Adobe Admin Console voordat u gebruikers gaat migreren. Meer informatie <a href="https://helpx.adobe.com/enterprise/help/identity.html"> hier </a> . </p> <p>Als u geen domeinen wilt claimen voor Enterprise- of federatieve id's, slaat u deze stap over en migreert u gebruikers als Adobe-id's. Meer informatie over id-typen vindt u <a href="https://helpx.adobe.com/enterprise/help/identity.html"> hier </a> . </p> </td> 
</tr> 
</tbody> 
</table>

1. Zoek het domein met de gebruikers-id&#39;s die u wilt migreren en klik vervolgens onder **[!UICONTROL Requiring Migration]** op **[!UICONTROL Select Users]** .
1. Selecteer op de pagina [!DNL Users] de gebruikers die u wilt migreren en klik op **[!UICONTROL Migrate]** .

   Wanneer u op **[!UICONTROL Migrate]** klikt, ontvangen gebruikers een uitnodiging (Migratie gestart) en moeten ze deze accepteren. Hiermee wordt de gebruikersnaam verplaatst naar de voltooide migratie. Vervolgens kunt u de oudere toegang uitschakelen tot `[!DNL my.omniture.com].`

   ![](/help/admin/tools/user-management/user-migration/assets/user-info.png)

1. Geef het type id op dat u wilt migreren voor de gebruikers (Adobe ID of Enterprise ID)

   Na het migreren van gebruikers verandert de status onder de kolom Migratiestatus van *`Not Initiated`* in *`Migrated`* .

   Als *`Failed`* wordt weergegeven, plaatst u de muisaanwijzer op het pictogram voor een beschrijving van de oorzaak van de fout.
