---
description: Hoe u accounts van analysegebruikers als Enterprise- of federatieve id's naar de Adobe Admin Console migreert.
title: Analytische gebruikersaccounts migreren voor bedrijfs- en federatieve id's
feature: Admin Tools
exl-id: 988ed685-4eca-4b0b-a653-9c6a156852f1
role: Admin
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# Analytische gebruikersaccounts migreren voor bedrijfs- en federatieve id&#39;s

Hoe u accounts van analysegebruikers als Enterprise- of federatieve id&#39;s naar de Adobe Admin Console migreert.

## Vereisten {#prereqs}

Vereisten voor het beheren van gebruikers in de Adobe Admin Console.

Voer de volgende stappen uit voor nieuwe domeinen en mappen:

* Een map instellen
* Domeinen instellen
* Domeinen koppelen aan mappen

Zie [ Opstelling een identiteitssysteem ](https://helpx.adobe.com/nl/enterprise/using/set-up-identity.html) voor hulp.

Als een folder reeds in een andere organisatie door een andere bedrijfseenheid of een team werd gecreeerd, volg de stappen in [ folder die ](https://helpx.adobe.com/nl/enterprise/using/set-up-identity.html#Directorytrusting) vertrouwt om de folder in de organisatie te vestigen die u voor Analytics gebruikt.

## Gebruikersaccounts migreren voor Enterprise- en federatieve id&#39;s {#task-0cfb3e4400fd4ab58e4d9704528b05fa}

In deze procedure zult u:

* Download een gebruikerslogin lijst van **[!UICONTROL Analytics]** > **[!UICONTROL Analytics Users & Assets]**.

* Download een lijst met huidige gebruikers via **[!UICONTROL Admin Console]** > **[!UICONTROL Users]** .

* Vergelijk de lijsten (er wordt gezocht naar duplicaten zodat u geen overschrijvingen van accountgegevens in de Adobe Admin Console opneemt).
* Upload een voltooide [!DNL .csv] (van **[!UICONTROL Admin Console]** > **[!UICONTROL Users]** ) met Enterprise ID- of Federated ID-gebruikers naar de Adobe Admin Console.

Als u bestaande Adobe ID gebruikersrekeningen aan Enterprise ID of Federated ID moet migreren, de Zorg van de Klant van Adobe contacteren en de schakelaar van de a [ bulkgebruikersidentiteit ](https://helpx.adobe.com/nl/enterprise/using/bulk-operations.html) verzoeken.

**om gebruikersrekeningen** te migreren

1. Download het aanmeldingsbestand voor Analytics-gebruikers ( [!DNL User Logins List.tab] ) van Analytics User Management met een van de volgende methoden (afhankelijk van of u al migreerde gebruikers).
   1. *voorafgaand aan migratie,* navigeer aan **[!UICONTROL Admin]** > **[!UICONTROL User Management (Legacy)]** > **[!UICONTROL Edit Users]**, dan klik **[!UICONTROL Download Report]**.

      ![](/help/admin/tools/user-management/user-migration/assets/download-report.png)

      De koppeling Rapport downloaden wordt alleen weergegeven voor klanten die geen migrerende gebruikers hebben.

   1. *als u reeds gemigreerde gebruikers,* navigeer aan **[!UICONTROL Analytics]** > **[!UICONTROL Analytics users and Assets]**.

      ![ Info van de Stap ](/help/admin/tools/user-management/user-migration/assets/admin-analytics-users-assets.png)

   1. Selecteer gebruikers op de pagina [!DNL Users] en klik vervolgens op **[!UICONTROL Export to CSV]** .

      ![ Info van de Stap ](/help/admin/tools/user-management/user-migration/assets/export-csv-migrate.png)

   1. Open het gedownloade [!DNL User List.csv] bestand in Excel.

      Bereid u voor om de waarden *`Email`* , *`First Name`* en *`Last Name`* te kopiëren naar een [!DNL sample.csv] -bestand (zoals in de volgende stap wordt beschreven).

      >[!IMPORTANT]
      >
      >De waarden in het CSV-bestand moeten door komma&#39;s worden gescheiden.

      >[!TIP]
      >
      >Tijdens deze stap raadt Adobe aan uw gebruikerslijst te stroomlijnen om ervoor te zorgen dat alleen gebruikers met een geldige e-mailid worden opgenomen in de migratie naar Enterprise of Federated ID.

1. Download in de [!UICONTROL Admin Console] een lijst met Adobe Admin Console-gebruikers:

   1. Navigeer aan [!UICONTROL Admin Console] > **[!UICONTROL Users]**, dan klik [ de gebruikerslijst van de Uitvoer aan CSV ](https://helpx.adobe.com/nl/enterprise/using/users.html).

      ![](/help/admin/tools/user-management/user-migration/assets/export-csv.png)

   1. Vergelijk de twee bestanden: de bestaande Adobe Admin Console-gebruikers in het geëxporteerde [!DNL .csv] -bestand ( [!DNL sample.csv] in dit voorbeeld) met de gebruikers in het Analytics [!DNL User Logins List.csv] -bestand.

      >[!IMPORTANT]
      >
      >Als u duplicaten zoekt, verwijdert u deze uit het bestand Analytics [!DNL User Logins List.csv] . Deze stap helpt te voorkomen dat bestaande Experience Cloud-gebruikersmachtigingen in de Adobe Admin Console worden overschreven en geeft u een lijst met te migreren accounts.

1. Download de CSV-sjabloon van de Adobe Admin Console:
   1. Klik op het tabblad Gebruikers op **[!UICONTROL Add users by CSV]** en vervolgens op **[!UICONTROL Download CSV Template]** .

      ![ Info van de Stap ](/help/admin/tools/user-management/user-migration/assets/add-users-csv.png)

   1. Kies **[!UICONTROL Standard Template]** .

      Deze stap downloadt een [!DNL sample.csv] sjabloonbestand.

      ![](/help/admin/tools/user-management/user-migration/assets/download-csv-template.png)

1. Kopieer de kolomwaarden *`Email`* , *`First Name`* en *`Last Name`* van [!DNL User Logins List.tab] naar de overeenkomende kolommen in de sjabloon [!DNL sample.csv] .

   **Voorbeeld van het Dossier van het Malplaatje**

   ![](/help/admin/tools/user-management/user-migration/assets/sample.png)

1. Voer in de sjabloon ( [!DNL sample.csv] ) de volgende vereiste velden in:

<table id="table_1B5EEFDB5BD8436EB760BE5FFAB1CF02"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Veld </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>E-mail </p> </td> 
   <td colname="col2"> <p>Wordt gekopieerd uit <span class="filepath"> User Logins List.tab </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Voornaam </p> </td> 
   <td colname="col2"> <p>Wordt gekopieerd uit <span class="filepath"> User Logins List.tab </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Achternaam </p> </td> 
   <td colname="col2"> <p>Wordt gekopieerd uit <span class="filepath"> User Logins List.tab </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Identiteitstype </p> </td> 
   <td colname="col2"> <p><span class="term"> Federated ID </span> of <span class="term"> Enterprise ID </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Domein </p> </td> 
   <td colname="col2"> <p>Zorg ervoor dat domeinen in <span class="term"> Domein </span> en <span class="term"> E-mail </span> kolom de domein(s) aanpassen die in de eerste vereisten worden gevestigd </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Landcode </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
 </tbody> 
</table>

Voor meer informatie over de gebieden in het [!DNL .csv] dossier, zie [ Csv- dossierformaat ](https://helpx.adobe.com/nl/enterprise/using/users.html).

>[!NOTE]
>
>Andere kolommen, zoals [!UICONTROL Product Configurations] en [!UICONTROL Admin Roles] , kunnen leeg zijn.

1. Upload het sjabloonbestand op het tabblad Gebruikers in de Adobe Admin Console door op **[!UICONTROL Add users by CSV]** te klikken (zoals in Stap 3.).
1. In Analytics, stel het migratiehulpmiddel in werking (zoals die in [ wordt beschreven Migreer de gebruikersrekeningen van Analytics ](/help/admin/tools/user-management/user-migration/t-migrate-users.md).
1. Klik op **[!UICONTROL Migrate]** > **[!UICONTROL Migrate as Enterprise IDs]** .

   ![ Info van de Stap ](/help/admin/tools/user-management/user-migration/assets/migrate-as-enterprise.png)

   Wanneer u op **[!UICONTROL Migrate]** klikt, wordt de gebruiker gekoppeld aan de Enterprise ID/Federated ID-account in Adobe Admin Console. De machtigingen van de verouderde gebruikersaccount in Analytics komen overeen met de machtigingen die zijn verleend voor de Enterprise/Federated ID-aanmelding in **[!UICONTROL Admin Console]** > **[!UICONTROL Analytics]** > **[!UICONTROL Product Profiles]** . De gebruikers-id wordt weergegeven in het emmertje voor migratie voltooid. U kunt de oudere [!DNL my.omniture.com] -toegang uitschakelen.

   Na het migreren van gebruikers verandert de status onder de kolom Migratiestatus van **[!UICONTROL Not Initiated]** in **[!UICONTROL Migrated]** .

   Adobe ID-gebruikers die in het migratiehulpprogramma worden weergegeven, kunnen ook in dit proces worden gemigreerd. Ze moeten zich nog steeds aanmelden bij hun Adobe ID totdat er een identiteitsschakelaar wordt uitgevoerd. Neem contact op met de klantenservice van Adobe voor hulp bij een identiteitsschakelaar.
