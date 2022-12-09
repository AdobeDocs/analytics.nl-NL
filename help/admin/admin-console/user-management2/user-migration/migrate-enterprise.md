---
description: Hoe te om de gebruikersrekeningen van de Analyse als Onderneming of Federated IDs aan de Admin Console te migreren.
title: Analytics-gebruikersaccounts voor Enterprise en Federated ID’s migreren
feature: Admin Tools
exl-id: 988ed685-4eca-4b0b-a653-9c6a156852f1
source-git-commit: a17297af84e1f5e7fe61f886eb3906c462229087
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 3%

---

# Analytics-gebruikersaccounts voor Enterprise en Federated ID’s migreren{#migrate-analytics-user-accounts-for-enterprise-and-federated-ids}

Hoe te om de gebruikersrekeningen van de Analyse als Onderneming of Federated IDs aan de Admin Console te migreren.

## Vereisten {#prereqs}

Vereisten voor het beheren van gebruikers in de Admin Console.

Voer de volgende stappen uit voor nieuwe domeinen en mappen:

* Een map instellen
* Domeinen instellen
* Domeinen koppelen aan mappen

Zie [Een identiteitssysteem instellen](https://helpx.adobe.com/enterprise/using/set-up-identity.html) voor hulp.

Als een folder reeds in een andere organisatie door een andere bedrijfseenheid of team werd gecreeerd, volg de stappen in [directory vertrouwen](https://helpx.adobe.com/enterprise/using/set-up-identity.html#Directorytrusting) om de directory in de organisatie te vestigen die u gebruikt voor Analytics.

## Gebruikersaccounts migreren voor Enterprise- en federatieve id&#39;s {#task-0cfb3e4400fd4ab58e4d9704528b05fa}

In deze procedure zult u:

* Download een gebruikerslogin lijst van **[!UICONTROL Analytics]** > **[!UICONTROL Analytics Users & Assets]**.

* Download een lijst met huidige gebruikers vanuit de **[!UICONTROL Admin Console]** > **[!UICONTROL Users]**.

* Vergelijk de lijsten (er wordt gezocht naar duplicaten zodat u geen overschrijvingen van accountgegevens in de Admin Console voorkomt).
* Een voltooide bewerking uploaden [!DNL .csv] (van **[!UICONTROL Admin Console]** > **[!UICONTROL Users]**) met Enterprise ID of Federated ID gebruikers aan de Admin Console.

Als u bestaande Adobe ID-gebruikersaccounts naar een Enterprise ID of Federated ID moet migreren, neemt u contact op met de klantenservice van de Adobe en vraagt u een [identiteitsschakelaar van bulkgebruiker](https://helpx.adobe.com/enterprise/using/bulk-operations.html).

**Gebruikersaccounts migreren**

1. Download het aanmeldingsbestand van de gebruiker Analytics ( [!DNL User Logins List.tab]) van Analytics User Management (Analytics User Management) met een van de volgende methoden (afhankelijk van of u al migreerde gebruikers).
   1. *Voor de migratie* navigeren naar **[!UICONTROL Admin]** > **[!UICONTROL User Management (Legacy)]** > **[!UICONTROL Edit Users]** en klik vervolgens op **[!UICONTROL Download Report]**.

      ![](/help/admin/admin-console/user-management2/user-migration/assets/download-report.png)

      De koppeling Rapport downloaden wordt alleen weergegeven voor klanten die geen migrerende gebruikers hebben.

   1. *Als u al gemigreerde gebruikers hebt,* navigeren naar **[!UICONTROL Analytics]** > **[!UICONTROL Analytics users and Assets]**.

      ![Stapinfo](/help/admin/admin-console/user-management2/user-migration/assets/admin-analytics-users-assets.png)

   1. Op de [!DNL Users] pagina, selecteert u gebruikers en klikt u op **[!UICONTROL Export to CSV]**.

      ![Stapinfo](/help/admin/admin-console/user-management2/user-migration/assets/export-csv-migrate.png)

   1. De gedownloade bestanden openen [!DNL User List.csv] in Excel.

      voorbereid zijn om de *`Email`*, *`First Name`*, en *`Last Name`* waarden aan een [!DNL sample.csv] bestand (beschreven in de volgende stap).

      >[!IMPORTANT]
      >
      >De waarden in het CSV-bestand moeten door komma&#39;s worden gescheiden.

      >[!TIP]
      >
      >Tijdens deze stap raadt Adobe aan uw gebruikerslijst te stroomlijnen om ervoor te zorgen dat alleen gebruikers met een geldige e-mailid worden opgenomen in de migratie naar Enterprise of Federated ID.

1. In de [!UICONTROL Admin Console]downloadt u een lijst met gebruikers van Admin Consoles:

   1. Navigeren naar [!UICONTROL Admin Console] > **[!UICONTROL Users]** en klik vervolgens op [Gebruikerslijst exporteren naar CSV](https://helpx.adobe.com/enterprise/using/users.html).

      ![](/help/admin/admin-console/user-management2/user-migration/assets/export-csv.png)

   1. Vergelijk de twee bestanden: de bestaande gebruikers van de Admin Console in het geëxporteerde [!DNL .csv] file ( [!DNL sample.csv], in dit voorbeeld) met de gebruikers in de Analyse [!DNL User Logins List.csv] bestand.

      >[!IMPORTANT]
      >
      >Als u duplicaten vindt, verwijdert u deze uit Analytics [!DNL User Logins List.csv] bestand. Met deze stap kunt u voorkomen dat bestaande Experience Cloud-gebruikersmachtigingen in de Admin Console worden overschreven. U krijgt dan een lijst met accounts die u wilt migreren.

1. Download het malplaatje CSV van de Admin Console:
   1. Klik op het tabblad Gebruikers op **[!UICONTROL Add users by CSV]** vervolgens **[!UICONTROL Download CSV Template]**.

      ![Stapinfo](/help/admin/admin-console/user-management2/user-migration/assets/add-users-csv.png)

   1. Kies **[!UICONTROL Standard Template]**.

      Deze stap downloadt een [!DNL sample.csv] sjabloonbestand.

      ![](/help/admin/admin-console/user-management2/user-migration/assets/download-csv-template.png)

1. Kopieer de *`Email`*, *`First Name`*, en *`Last Name`* kolomwaarden uit [!DNL User Logins List.tab] op de corresponderende kolommen in de [!DNL sample.csv] sjabloon.

   **Voorbeeld van sjabloonbestand**

   ![](/help/admin/admin-console/user-management2/user-migration/assets/sample.png)

1. In de template ( [!DNL sample.csv]), vult de volgende vereiste velden in:

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
   <td colname="col2"> <p>Gekopieerd van de <span class="filepath"> Lijst met gebruikersaanmeldingen.tab</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Voornaam </p> </td> 
   <td colname="col2"> <p>Gekopieerd van de <span class="filepath"> Lijst met gebruikersaanmeldingen.tab</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Achternaam </p> </td> 
   <td colname="col2"> <p>Gekopieerd van de <span class="filepath"> Lijst met gebruikersaanmeldingen.tab</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Identiteitstype </p> </td> 
   <td colname="col2"> <p><span class="term"> Federated ID</span> of <span class="term"> Enterprise ID</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Domein </p> </td> 
   <td colname="col2"> <p>Zorg ervoor dat domeinen in <span class="term"> Domein</span> en <span class="term"> E-mail</span> de kolom komt overeen met de in de eerste vereisten vastgestelde domeinen</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Landcode </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
 </tbody> 
</table>

Voor meer informatie over de velden in het dialoogvenster [!DNL .csv] bestand, zie [CSV-bestandsindeling](https://helpx.adobe.com/enterprise/using/users.html).

>[!NOTE]
>
>Andere kolommen, zoals [!UICONTROL Product Configurations] en [!UICONTROL Admin Roles] kan leeg zijn.

1. Upload het sjabloonbestand op het tabblad Gebruikers in de Admin Console door op **[!UICONTROL Add users by CSV]** (zoals weergegeven in Stap 3.)
1. Voer in Analytics het migratiehulpprogramma uit (zoals beschreven in [Gebruikersaccounts voor Analyse migreren](/help/admin/admin-console/user-management2/user-migration/t-migrate-users.md)).
1. Klik op **[!UICONTROL Migrate]** > **[!UICONTROL Migrate as Enterprise IDs]**.

   ![Stapinfo](/help/admin/admin-console/user-management2/user-migration/assets/migrate-as-enterprise.png)

   Wanneer u op **[!UICONTROL Migrate]**, wordt de gebruiker gekoppeld aan de Enterprise ID/Federated ID-account in Admin Console. De machtigingen voor het verouderde gebruikersaccount in Analytics komen overeen met de machtigingen die zijn verleend aan de Enterprise/Federated ID-aanmelding in **[!UICONTROL Admin Console]** > **[!UICONTROL Analytics]** > **[!UICONTROL Product Profiles]**. De gebruikers-id wordt weergegeven in het emmertje voor migratie voltooid. U kunt hun nalatenschap uitschakelen [!DNL my.omniture.com] toegang.

   Na het migreren van gebruikers verandert de status onder de kolom van de Status van de Migratie van **[!UICONTROL Not Initiated]** tot **[!UICONTROL Migrated]**.

   Adobe ID-gebruikers die in het migratiehulpprogramma worden weergegeven, kunnen ook in dit proces worden gemigreerd. Ze moeten zich nog steeds aanmelden bij hun Adobe ID totdat er een identiteitsschakelaar wordt uitgevoerd. Neem contact op met de klantenservice van Adobe voor hulp bij een identiteitsschakelaar.
