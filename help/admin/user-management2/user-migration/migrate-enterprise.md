---
description: Hoe u accounts van Analytics-gebruikers als Enterprise- of federatieve id's naar de beheerconsole migreert.
title: Analytische gebruikersaccounts migreren voor bedrijfs- en federatieve id's
uuid: f90bf78a-5603-4bef-b714-13215301187c
translation-type: tm+mt
source-git-commit: 3db8481434f3db43732f0b54a58c6d4a29bce652

---


# Analytische gebruikersaccounts migreren voor bedrijfs- en federatieve id&#39;s{#migrate-analytics-user-accounts-for-enterprise-and-federated-ids}

Hoe u accounts van Analytics-gebruikers als Enterprise- of federatieve id&#39;s naar de beheerconsole migreert.

## Vereisten {#prereqs}

Vereisten voor het beheren van gebruikers in de beheerconsole.

Voer de volgende stappen uit voor nieuwe domeinen en mappen:

* Een map instellen
* Domeinen instellen
* Domeinen koppelen aan mappen

Zie [Een identiteitssysteem](https://helpx.adobe.com/enterprise/using/set-up-identity.html) instellen voor hulp.

Als een folder reeds in een andere organisatie door een andere bedrijfseenheid of team werd gecreeerd, volg de stappen in [folder het vertrouwen](https://helpx.adobe.com/enterprise/using/set-up-identity.html#Directorytrusting) om de folder in de organisatie te vestigen die u voor Analytics gebruikt.

## Gebruikersaccounts migreren voor Enterprise- en federatieve id&#39;s {#task-0cfb3e4400fd4ab58e4d9704528b05fa}

In deze procedure zult u:

* Download een gebruikerslogin lijst van **[!UICONTROL Analytics]** > **[!UICONTROL Analytics Users & Assets]**.

* Download een lijst met huidige gebruikers via **[!UICONTROL Admin Console]** > **[!UICONTROL Users]**.

* Vergelijk de lijsten (u zoekt naar duplicaten zodat u accountgegevens niet overschrijft in de beheerconsole).
* Upload een voltooide [!DNL .csv] (van **[!UICONTROL Admin Console]** > **[!UICONTROL Users]**) gebruiker met een Enterprise-id of een federatieve id naar de beheerconsole.

Als u bestaande Adobe-id-gebruikersaccounts wilt migreren naar een Enterprise-id of federated-id, neemt u contact op met de klantenservice van Adobe en vraagt u een [bulksgewijs identiteitsoverzicht](https://helpx.adobe.com/enterprise/using/bulk-operations.html).

**Gebruikersaccounts migreren**

1. Download het bestand Analytics user logins ( [!DNL User Logins List.tab]) van Analytics User Management met een van de volgende methoden (afhankelijk van of u al migreerde gebruikers).
   1. *Navigeer vóór de migratie* naar **[!UICONTROL Admin]** > **[!UICONTROL User Management (Legacy)]** > **[!UICONTROL Edit Users]** en klik op **[!UICONTROL Download Report]**.

      ![](assets/download-report.png)

      De koppeling Rapport downloaden wordt alleen weergegeven voor klanten die geen migrerende gebruikers hebben.

   1. *Als u al gemigreerde gebruikers hebt,* navigeert u naar **[!UICONTROL Analytics]** > **[!UICONTROL Analytics users and Assets]**.

      ![Stapinfo](assets/admin-analytics-users-assets.png)

   1. Selecteer gebruikers op de [!DNL Users] pagina en klik op **[!UICONTROL Export to CSV]**.

      ![Stapinfo](assets/export-csv-migrate.png)

   1. Open het gedownloade [!DNL User List.csv] bestand in Excel.

      Ben bereid om de *`Email`*, *`First Name`*, en de *`Last Name`* waarden aan een [!DNL sample.csv] dossier (die in de volgende stap wordt beschreven) te kopiëren.

      > [!IMPORTANT] De waarden in het CSV-bestand moeten door komma&#39;s worden gescheiden.

      > [!TIP] Tijdens deze stap raadt Adobe aan uw gebruikerslijst te stroomlijnen om ervoor te zorgen dat alleen gebruikers met een geldige e-mailid worden opgenomen in de migratie naar een Enterprise- of federatieve id.

1. Download in het [!UICONTROL Admin Console]dialoogvenster een lijst met gebruikers van de beheerconsole:

   1. Navigeer naar [!UICONTROL Admin Console] > **[!UICONTROL Users]** en klik vervolgens op Lijst met gebruikers [exporteren naar CSV](https://helpx.adobe.com/enterprise/using/users.html).

      ![](assets/export-csv.png)

   1. Vergelijk de twee bestanden: de bestaande Admin Console-gebruikers in het geëxporteerde [!DNL .csv] bestand ( [!DNL sample.csv]in dit voorbeeld) met de gebruikers in het Analytics- [!DNL User Logins List.csv] bestand.

      > [!IMPORTANT] Als u duplicaten zoekt, verwijdert u deze uit het Analytics- [!DNL User Logins List.csv] bestand. Met deze stap kunt u voorkomen dat bestaande Live Experience Cloud-gebruikersmachtigingen in de beheerconsole worden overschreven. U krijgt dan een lijst met accounts die u wilt migreren.

1. Download de CSV-sjabloon uit de beheerconsole:
   1. Klik op het tabblad Gebruikers **[!UICONTROL Add users by CSV]** en klik vervolgens **[!UICONTROL Download CSV Template]**.

      ![Stapinfo](assets/add-users-csv.png)

   1. Kies **[!UICONTROL Standard Template]**.

      Deze stap downloadt een [!DNL sample.csv] sjabloonbestand.

      ![](assets/download-csv-template.png)

1. Kopieer de *`Email`*, *`First Name`*, en *`Last Name`* kolomwaarden van [!DNL User Logins List.tab] aan de overeenkomstige kolommen in het [!DNL sample.csv] malplaatje.

   **Voorbeeld van sjabloonbestand**

   ![](assets/sample.png)

1. Vul in de sjabloon ( [!DNL sample.csv]) de volgende vereiste velden in:

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
   <td colname="col2"> <p>Gekopieerd van de Logins List.tab <span class="filepath"> van de</span>Gebruiker. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Voornaam </p> </td> 
   <td colname="col2"> <p>Gekopieerd van de Logins List.tab <span class="filepath"> van de</span>Gebruiker. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Achternaam </p> </td> 
   <td colname="col2"> <p>Gekopieerd van de Logins List.tab <span class="filepath"> van de</span>Gebruiker. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Identiteitstype </p> </td> 
   <td colname="col2"> <p><span class="term"> Federatieve id</span> of <span class="term"> Enterprise-id</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Domein </p> </td> 
   <td colname="col2"> <p>Zorg ervoor dat domeinen in de kolom <span class="term"> Domein</span> en <span class="term"> E-mail</span> overeenkomen met de domeinen die in de eerste vereisten</a>zijn vastgelegd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Landcode </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
 </tbody> 
</table>

Zie [!DNL .csv] CSV-bestandsindeling [voor meer informatie over de velden in het](https://helpx.adobe.com/enterprise/using/users.html)bestand.

> [!NOTE] Andere kolommen, zoals [!UICONTROL Product Configurations] en [!UICONTROL Admin Roles] kunnen leeg zijn.

1. Upload het sjabloonbestand op het tabblad Gebruikers in de beheerconsole door te klikken **[!UICONTROL Add users by CSV]** (zoals in stap 3.).
1. Voer bij Analytics het migratiehulpprogramma uit (zoals beschreven in [Analytics-gebruikersaccounts](/help/admin/user-management2/user-migration/t-migrate-users.md)migreren).
1. Klik op **[!UICONTROL Migrate]** > **[!UICONTROL Migrate as Enterprise IDs]**.

   ![Stapinfo](assets/migrate-as-enterprise.png)

   Wanneer u klikt **[!UICONTROL Migrate]**, wordt de gebruiker gekoppeld aan het account Enterprise-id/Federated ID in de beheerconsole. De machtigingen van de verouderde gebruikersaccount in Analytics komen overeen met de machtigingen die zijn verleend aan de Enterprise/Federated ID-aanmelding in **[!UICONTROL Admin Console]** > **[!UICONTROL Analytics]** > **[!UICONTROL Product Profiles]**. De gebruikers-id wordt weergegeven in het emmertje voor migratie voltooid. U kunt de [!DNL my.omniture.com] toegang tot deze systemen uitschakelen.

   Na het migreren van gebruikers, verandert de status onder de kolom van de Status van de Migratie van **[!UICONTROL Not Initiated]** aan **[!UICONTROL Migrated]**.

   Gebruikers van Adobe-id die in het migratiehulpprogramma worden weergegeven, kunnen ook in dit proces worden gemigreerd. Ze moeten zich nog steeds aanmelden met hun Adobe-id totdat er een identiteitswijziging wordt uitgevoerd. Neem contact op met de klantenservice van Adobe voor hulp bij een identiteitsschakelaar.
