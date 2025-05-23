---
description: Gebruikers, groepen en producten van Analytics beheren in de Adobe Admin Console.
subtopic: Users and groups
title: Gebruiker- en productbeheer
feature: Admin Tools
exl-id: c0fbbb3a-0011-49d2-89a2-70fce11e0fb2
role: Admin
source-git-commit: 938795c7378cb1f0537ff84eddeab3feddf8d073
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 0%

---

# Gebruiker- en productbeheer (verouderd)

Gebruikers, groepen en producten van Analytics beheren in de Adobe Admin Console.

>[!IMPORTANT]
>
>Gebruiker- en productbeheer is verplaatst naar de [Adobe Admin Console](https://helpx.adobe.com/nl/enterprise/using/admin-console.html). Ga voor meer informatie over het beheren van gebruikersmachtigingen voor Adobe Analytics-gebruikers naar [Analyses in de Adobe Admin Console](/help/admin/admin-console/home.md).

## Help-bronnen voor Adobe Admin Console-beheerders {#help}

| Taak of resource | Beschrijving |
| --- | --- |
| Gebruikers-id&#39;s voor Analyse migreren naar de Adobe Admin Console | Adobe helpt analysebeheerders om gebruikers-id&#39;s te migreren naar de Adobe Admin Console. Deze inspanning zal in golven voorkomen. Wanneer het uw beurt is om uw gebruikers te migreren, zal de Adobe Analysebeheerders via e-mail met instructies op de hoogte brengen. Een migratiehulpmiddel is beschikbaar in [Analysegebruikersbeheer](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html?lang=nl-NL) om deze taak te vereenvoudigen.<p>**Belangrijk**: Op de dag van de migratie van uw gebruikers worden uw voormalige machtigingsgroepen automatisch naar de Adobe Admin Console gekopieerd. U kunt geen nieuwe gebruikers meer uitnodigen of nieuwe groepen maken in Analytics Admin Tools. Raadpleeg de veelgestelde vragen en help bij het analyseren van de migratie van gebruikers naar de Adobe Admin Console voor informatie over de voorbereiding van de migratie en over de desbetreffende beheerfuncties. |
| Adobe Admin Console starten | Nadat uw gebruikersaccounts zijn gemigreerd, kunt u gebruikers en producten beheren voor alle oplossingen in de Adobe Admin Console. Navigeren naar: `https://adminconsole.adobe.com/enterprise/`. Zie ook [Gebruikers en producten van Experiencen Cloud beheren](https://experienceleague.adobe.com/docs/core-services/interface/administration/admin-getting-started.html?lang=nl-NL). |
| Adobe Analytics-productprofielen, -gebruikers en -machtigingen beheren | Zie [Analyses in de Adobe Admin Console](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/home.html?lang=nl-NL). |

<!---
## User Management Descriptions {#section_7C19842A3D4249109A9399D4DF18DE75}

The following table describes elements on the [!UICONTROL Users] tab in [!UICONTROL User Management].

<table id="table_6F81D1095EB945D8995FF971B65BA52A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Number of User Logins available</span> </td> 
   <td colname="col2"> The maximum number of user accounts you can create for this company. If necessary, you can contact your Account Representative or Customer Care to increase this number at no charge. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Number of User Logins in use</span> </td> 
   <td colname="col2"> The number of user accounts currently in use for this company. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Number of User Logins Remaining</span> </td> 
   <td colname="col2"> The difference between the user account maximum and the number of existing user accounts. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Add New User</span> </td> 
   <td colname="col2"> <p>Lets you add a user account to the company. This link is available only if the Number of User Logins Remaining is greater than 0. </p> <p>See <a href="/help/admin/user-management2/c-user-management/users.md"> Users</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Download Report</span> </td> 
   <td colname="col2">Exports the contents of the <span class="wintitle"> Users</span> table to a tab-delimited file. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Login</span> </td> 
   <td colname="col2"> <p>The user name. You can click the user name to edit the user account properties. </p> <p>See <a href="/help/admin/user-management2/c-user-management/users.md"> Users</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> First Name</span> </td> 
   <td colname="col2"> The user's first (given) name. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Last Name</span> </td> 
   <td colname="col2"> The user's surname (family name). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Title</span> </td> 
   <td colname="col2"> The user's job title. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Admin</span> </td> 
   <td colname="col2"> Specifies if the user account has administrative privileges. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Last Login</span> </td> 
   <td colname="col2"> Displays a timestamp of the last login for this user account. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="wintitle"> Create Time</span> </td> 
   <td colname="col2"> Shows the date and time when the login account was created. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Expires</span> </td> 
   <td colname="col2"> Displays the account expiration account, if applicable. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Manage</span> </td> 
   <td colname="col2"> Provides links for user account management. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Edit</span> </td> 
   <td colname="col2"> <p>Edit user account settings. </p> <p>See <a href="/help/admin/user-management2/c-user-management/users.md"> Users</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Delete</span> </td> 
   <td colname="col2"> Delete the user account. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Transfer</span> </td> 
   <td colname="col2">Assign the privileges (permissions and resource access) of one user account to another. <p>See <a href="/help/admin/user-management2/c-user-management/t-transfer-user-accout-privileges.md"> Transfer user account privileges</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="wintitle"> Login as this user</span> </td> 
   <td colname="col2"> <p>Allows admins to impersonate and log in as a non-admin account. Admin accounts cannot be impersonated. </p> </td> 
  </tr> 
 </tbody> 
</table>
-->