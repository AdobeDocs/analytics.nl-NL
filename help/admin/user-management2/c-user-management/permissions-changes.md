---
description: Inhoud met verouderde machtigingen
keywords: groepen;machtigingen
subtopic: Users and groups
title: Wijzigingen in gebruikers- en groepstoestemmmingen
feature: Admin Tools
uuid: 94f2727b-17e4-4003-a222-35c821d6959e
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '1546'
ht-degree: 1%

---


# Wijzigingen in gebruikers- en groepstoestemmmingen

>[!IMPORTANT]
>
>Gebruiker- en productbeheer zijn verplaatst naar de [Admin Console](https://helpx.adobe.com/nl/enterprise/using/admin-console.html). Adobe geeft een melding wanneer het uw tijd is om gebruikers te migreren. Nadat alle klanten zijn gemigreerd, wordt Help-inhoud voor **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL All admin]** > **[!UICONTROL User management]** ingetrokken.

## Wat is er veranderd? {#section_2C205DE94155441B9E9D3E4C46CCF2EE}

**[!UICONTROL Admin]** > **[!UICONTROL User Management]** > **[!UICONTROL Groups]**

>[!NOTE]
>
>Vanwege het grote aantal mogelijke machtigingscombinaties dat beschikbaar is, kunnen we geen documentatie verschaffen met een beschrijving van alle API-methoden die in elke machtigingscombinatie kunnen worden gebruikt. Over het algemeen, zullen niet-beheerders die de toegang van de Diensten van het Web worden verleend slechts Gelezen toegang tot API methodes hebben. Zij zullen geen Schrijftoegang tot methodes hebben.

Omdat de API en de interface het zelfde machtigingssysteem gebruiken, zullen welke toestemmingen een bepaalde niet-beheerder door een beheerder in de interface (Adobe Admin Console) is verleend, de zelfde toestemmingen zijn die de gebruiker in API heeft.

<table id="table_D1DB0DE37752450BBCCA44DB760BB505"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Verbetering </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p id="reportaccess">Veranderingen in <span class="uicontrol"> de Toegang van het Rapport</span> (Pas Groepen aan) </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> Nieuwe groep</span>  toevoegen &gt; Toegang  <span class="uicontrol"> rapporteren</span> </p> <p>De <span class="wintitle"> sectie van de Toegang van het Rapport</span> op <span class="wintitle"> bepaalt de pagina van de Gebruiker van de Groep</span> is gestroomlijnd aan vier categorieën, die u toelaten om toestemmingen op een korrelig niveau aan te passen. </p> <p><img  src="assets/report-access.png" id="image_CB83E5C7DB4343619421A1FAA61478D0"> </img> </p> <p>Items eerder in </p> 
    <ul id="ul_16D5EF18D57D4608AEEDEC40D90D8828"> 
     <li id="li_F29E84C6228A464C8807F09205AEAAC6"> <p> <a href="/help/admin/user-management2/c-customize-report-access/groups-analytics-tools.md"> Analytische gereedschappen</a>: Schakel gebruikersmachtigingen in voor algemene items (facturering, logbestanden, enz.), bedrijfsbeheer, tools, webservicetoegang, Report Builder en integratie van gegevensconnectors. </p> <p> <b>Opmerking: </b> bedrijfsinstellingen uit de categorie Admin Console aanpassen zijn verplaatst naar Analytics Tools. </p> </li> 
     <li id="li_A6EB788162A2455E94CE54B9279A854D"> <p> <a href="/help/admin/user-management2/c-customize-report-access/groups-report-suite-tools.md"> Rapportsuite-gereedschappen</a>: Schakel gebruikersmachtigingen in voor webservices, rapportbeheer, tools en rapporten en dashboarditems. </p> </li> 
     <li id="li_EDB0255E009B4F1CAFAF53966B41363C"> <p> <a href="/help/admin/user-management2/c-customize-report-access/groups-metrics.md"> Metrisch</a>: Laat toestemmingen voor verkeer, omzetting, douanegebeurtenissen, oplossingsgebeurtenissen, bewuste inhoud toe, etc. </p> </li> 
     <li id="li_8DAE87D1DEF54803A9C6FE31C01F0FB0"> <p> <a href="/help/admin/user-management2/c-customize-report-access/groups-dimensions.md"> Dimension</a>: Pas gebruikerstoegang op een korrelig niveau, met inbegrip van eVars, verkeersrapporten, oplossingsrapporten, en het kleven rapporten aan. </p> </li> 
    </ul> <p>U kunt bijvoorbeeld een groep maken met toegang tot meerdere analyseprogramma's (<span class="wintitle"> Analysis Workspace</span>, <span class="wintitle"> Rapporten &amp; Analytics</span> en <span class="wintitle"> Report Builder</span>), met toestemming voor specifieke metriek en dimensies (inclusief eVars) en mogelijkheden zoals het maken van segmenten of berekende metriek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wijzigingen in vooraf gedefinieerde groepen </p> </td> 
   <td colname="col2"> <p> <b>Beheerderstoegang:</b> vooraf gedefinieerde groepen zijn niet meer vereist voor beheerders. De beheerders hebben nu toegang tot alle punten (hulpmiddelen, metriek, dimensies), evenals de toegang van de Dienst van het Web, Report Builder, en Activity Map. </p> <p>Het doel van groepen is om niet-administratieve gebruikers toegang te verlenen of te beperken. </p> <p> <b>Aangepaste groepen:</b> aangepaste groepen hebben vooraf gedefinieerde groepen vervangen. Bestaande, vooraf gedefinieerde groepen worden gemigreerd naar aangepaste groepen met dezelfde groepsnaam. Alle aangepaste groepen die u hebt gemaakt, inclusief de instellingen, blijven behouden. U zult echter zien dat de locatie van de instellingen is verplaatst. Bijvoorbeeld, zijn de montages van het Bedrijf (in Aanpassen Admin Console) nu in <a href="/help/admin/user-management2/c-customize-report-access/groups-analytics-tools.md"> Customize Analytics Tools</a>. </p> <p> De gebruikers die tot <span class="term"> Al Toegang van het Rapport</span> behoren zijn gemigreerd aan een douanegroep met toegang tot: </p> 
    <ul id="ul_696A9243F5FD4AF187352C2F4B1CFDC2"> 
     <li id="li_683A0A3BB7214CFFBC61D5A4CD237F48">Alle Dimension </li> 
     <li id="li_D8FDBF6A32224731AB706315DEA0A03E">Alle metriek </li> 
     <li id="li_65ABE5C95D43444D88E63EE95C9AED05">Alle rapportsets </li> 
     <li id="li_7ED1505590144B38B3B9851BAA6BBB49">Toestemming voor kanaalrapport </li> 
     <li id="li_F718FE1FCF9A4B05AB933CA3F105F3EC">Toestemming voor anomaly-detectierapport </li> 
     <li id="li_527BD52007E846FE8B5F71AB3C12F695">Machtiging voor realtime rapport </li> 
     <li id="li_AFFB58C7FB644AC8A85E2D76BA7D51F5">Analysis Workspace Access-machtiging </li> 
    </ul> <p>Beheerders kunnen aangepaste groepen verwijderen en hun eigen groepen maken, aangezien alle instellingen die voorheen beschikbaar waren in vooraf gedefinieerde groepen, beschikbaar zijn voor aanpassing onder de instellingen <span class="wintitle"> Rapporttoegang</span> in <a href="/help/admin/user-management2/c-user-groups/groups.md"> Gebruikersgroepen definiëren</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Machtigingen op Dimension-niveau </p> </td> 
   <td colname="col2"> <p>U kunt machtigingen aanpassen om toegang tot afmetingen op te nemen of uit te sluiten (naast metriek). </p> 
    <ul id="ul_DA5A54223673474E9151AF979DA50659"> 
     <li id="li_C3E82F7BC07A4F2F83A85D3D511292CC"> <p>Alle huidige afmetingen en metriek binnen aangepaste groepen zijn automatisch gemigreerd naar de nieuwe categorieën. Als metriek is ingeschakeld voor een bestaande groep, krijgt deze standaard alle nieuw toegestane afmetingen (eVars en inhoud behouden) en maatstaven. </p> </li> 
     <li id="li_CC56F9181CC14AB59318628E72F2E8C9"> Indelingsrechten (voorheen, SAINT): De toegang tot classificaties wordt bepaald door toegang tot <a href="https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html"> variabele</a> waarop de classificatie is gebaseerd. </li> 
    </ul> <p>Zie <a href="/help/admin/user-management2/c-customize-report-access/groups-dimensions.md"> Dimension-machtigingen aanpassen</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Admin Console </p> </td> 
   <td colname="col2"> <p>Wordt alleen aanbevolen voor nieuwe klanten of klanten met bedrijven <a href="https://experienceleague.adobe.com/docs/core-services/interface/about-core-services/core-services.html"> die zijn ingericht in de Experience Cloud</a>. Er is een migratie gepland voor bestaande <span class="keyword"> Analytics</span>-klanten naar het <span class="keyword"> Experience Cloud</span>-identiteitsbeheersysteem. </p> <p>Meer informatie is beschikbaar in <a href="https://helpx.adobe.com/enterprise/using/manage-permissions-and-roles.html"> Beheer producttoestemmingen in de Admin Console</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Veelgestelde vragen over wijzigingen in machtigingen {#section_02809EFC95054B40A089E6C6E4FACA13}

Hier is belangrijke nieuwe informatie over nieuwe en geplande updates en hoe zij uw administratieve milieu beïnvloeden.

<table id="table_1E93F45C66E841E6882FB602509F30A3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Vraag </th> 
   <th colname="col2" class="entry"> Antwoord </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1">Welke toestemmingenveranderingen kwamen in <b>juli 2016</b> versie? </td> 
   <td colname="col2"> <p> <b>Alle rapporttoegang</b> </p> <p>Wanneer het toevoegen van rapportreeksen om in een groep te omvatten, kunt u <span class="uicontrol"> Al Toegang van de Reeks van het Rapport </span> specificeren. Deze instelling past groepsmachtigingen toe op alle huidige en toekomstige rapportsuites. </p> <p>Als u deze functie wilt inschakelen, navigeert u naar <span class="uicontrol"> Gebruikersbeheer</span> &gt; <span class="uicontrol"> Groepen</span> &gt; <span class="uicontrol"> Nieuwe gebruikersgroep toevoegen</span> en selecteert u <span class="uicontrol"> Alle rapportsuite Access</span>. </p> <p><img placement="break"  src="assets/all-report-suites.png" width="300px" id="image_9E814D412E87484C940F1100D6DE2B0F" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Moet ik de Admin Console gebruiken om gebruikers te beheren, of het bestaande Gebruikersbeheer Analytics? </p> </td> 
   <td colname="col2"> <p>Wijzigingen die zijn aangebracht in Analytics &gt; Admin &gt; User Management (Analyse &gt; Beheer van gebruikers) worden niet weergegeven in de Admin Console. Daarom zouden slechts nieuwe klanten die reeds de Admin Console voor gebruiker en groepsbeheer gebruiken dit moeten blijven doen. Er is een migratie gepland naar de Admin Console van het bestaande groepsbeheer Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Welke toestemmingswijzigingen zijn aangebracht in de <b>Oktober 2016</b> versie? </p> </td> 
   <td colname="col2"> <p>De volgende verbeteringen aan de huidige <span class="wintitle"> interface Admin Tools</span> zijn beschikbaar: </p> <p> 
     <ul id="ul_2A31E8DC17A94B7FABDBA9C87C3947EF"> 
      <li id="li_AE2ECCA01CC64D30B109BE74379EE474">Wijzigingen in machtigingen zoals beschreven in <a href="/help/admin/user-management2/c-user-management/permissions-changes.md"> Administratieve wijzigingen - Herfst 2016</a>. </li> 
      <li id="li_33CB2B6A2E5F45BE97CC5E0983AF280E">Verwijderde dode verkeersrapporten die niet meer in het menu waren. </li> 
      <li id="li_57234CF27E1D405987DE89312CD62C52">Machtigingen voor classificaties: De toegang tot classificaties wordt bepaald door toegang tot de variabele waarvoor de classificatie geldt. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Is er iets dat ik moet doen om gebruikers te migreren? </p> </td> 
   <td colname="col2"> <p>Nee, alle machtigingen voor migraties worden transparant uitgevoerd. </p> <p> 
     <ul id="ul_654F85286EC04416B3E0BA725EBE10AD"> 
      <li id="li_8050B8941F794103B82A0ADF0930D216">Alle huidige verkeersrapporten in een Groep van de Douane zullen automatisch aan de nieuwe Categorie van Dimension worden gemigreerd. </li> 
      <li id="li_B97079DB29A346B98D066F11AB7F94AF">Als een Groep van de Douane om het even welke reeds toegelaten metriek heeft, zal het automatisch alle onlangs toegestane afmetingen (eVars en de variabelen van de Oplossing) worden gegeven. </li> 
      <li id="li_F1219EF490DA473BA15F2B215F2995AE"> Een douanegroep met minstens één metrisch zal automatisch toegang tot alle eVars en andere inhoud-bewuste afmetingen <b>behalve</b> de onlangs beschikbare verkeersdimensies (vroeger verkeersrapporten) worden verleend. </li> 
      <li id="li_F494CE6144A04A6199CFBBA1D7BEA32B">Elke vooraf gedefinieerde groep wordt gewijzigd in een machtiging. Deze nieuwe machtigingen worden toegevoegd aan de nieuwe categorie <span class="uicontrol"> Analytics Tools</span>. </li> 
      <li id="li_2FCD9254FC3C4FD7871EEF9453E5CE1E">Elke Groep van de Douane met om het even welke metriek zal alle gebeurtenissen van de Oplossing van de Analyse hebben als nieuwe metriek worden toegevoegd. </li> 
      <li id="li_34C4560769B64F28A4E83BAE71065DCC">Elke gebruiker die vroeger in Al Toegang van het Rapport was zal aan de nieuwe douanegroep worden toegevoegd. Alle Toegang van het Rapport zal niet meer bestaan. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wat verandert er niet? </p> </td> 
   <td colname="col2"> <p>Kenmerken van bezoekers blijven niet toegestaan. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Snelle naslaggids voor machtigingen {#section_A3FDD8259F524B21A5489833533D1B28}

De volgende tabel bevat een overzicht van taken en de plaats waar deze kunnen plaatsvinden (afhankelijk van de status van een bedrijf).

>[!NOTE]
>
>Een *`migrated user`* en *`Experience Cloud user`* verwijzen naar gebruikers die een e-mailuitnodiging hebben geaccepteerd om deel te nemen aan de Experience Cloud. Als de e-mailuitnodiging niet wordt geaccepteerd, zijn gebruikers nog steeds Analytische gebruikers en kunnen ze niet in de Admin Console worden beheerd. (De uitzondering is als de migratie [onderneming of gefedereerde IDs](https://helpx.adobe.com/enterprise/using/set-up-identity.html) gebruikt. In dit geval wordt de gebruiker gemigreerd wanneer de beheerder gebruikers op een gebruiker-door-gebruiker basis migreert.)

<table id="table_B68FD00FC5D24823A86BB69558C0327C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Taak </th> 
   <th colname="col2" class="entry"> Niet-migrerende Login Company </th> 
   <th colname="col3" class="entry"> Momenteel migrerend Bedrijf </th> 
   <th colname="col4" class="entry"> Voltooid migrerende Login Bedrijf </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Een gebruiker maken </td> 
   <td colname="col2"> <p>Admin Console (het creëren van een gebruiker en het toevoegen van hem of haar aan een Analytics <a href="https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html"> productconfiguratie</a> leidt ook tot de gebruikersrekening in Analytics). </p> <p> <a href="/help/admin/user-management2/c-user-management/t-add-user-account.md"> Admin Tools</a> </p> </td> 
   <td colname="col3"> <p> <a href="https://adminconsole.adobe.com/enterprise/"> Admin Console</a> </p> </td> 
   <td colname="col4"> <p> <a href="https://adminconsole.adobe.com/enterprise/"> Admin Console</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Een gebruiker bewerken </td> 
   <td colname="col2"> <p> <a href="/help/admin/user-management2/c-user-management/t-add-user-account.md"> Admin Tools</a> </p> </td> 
   <td colname="col3"> <p> <a href="https://adminconsole.adobe.com/enterprise/"> Admin Console</a> </p> <p> Hulpmiddelen Admin - het uitgeven in de Hulpmiddelen Admin voor gemigreerde gebruikers is beperkt tot API-zeer belangrijk beheer, en het schrappen van/het overbrengen van activa. </p> </td> 
   <td colname="col4"> <p> <a href="https://adminconsole.adobe.com/enterprise/"> Admin Console</a> </p> <p> Hulpmiddelen Admin - het uitgeven is beperkt tot API-zeer belangrijk beheer, en het schrappen van/het overbrengen activa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Een gebruiker verwijderen </td> 
   <td colname="col2"> <p>Admin Console - Voor Experience Cloud-gebruikers </p> <p>Hulpmiddelen Admin - voor alle gebruikers, maar voor gebruikers van Experience Cloud, schrapt slechts de in kaart gebrachte gebruiker van de Analyse, niet de rekening van de Experience Cloud. </p> </td> 
   <td colname="col3"> <p>Admin Console - voor gemigreerde gebruikers. </p> <p>Admin Tools - alleen voor gebruikers met analysemogelijkheden. </p> </td> 
   <td colname="col4"> <p>Admin Console </p> <p> Hulpprogramma's voor beheerders - Nadat u een gebruiker van een Experience Cloud hebt verwijderd of nadat u de koppeling van zijn account in de Admin Console hebt opgeheven, kunt u de aanmeldingsgegevens voor Analytics verwijderen uit de beheerprogramma's. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Aanmelden bij Analytics </td> 
   <td colname="col2"> <p> <b>Experience Cloud:  </b> <span class="filepath"> marketing.adobe.com</span>. Alleen beschikbaar voor Experience Cloud-gebruikers. </p> <p> <b>Analytics (legacy):</b> <span class="filepath"> sc.omniture.com</span>. Alleen voor gebruikers van Analytics en voor gebruikers van Experience Cloud met hun analysegegevens </p> </td> 
   <td colname="col3"> <p> <span class="filepath"> marketing.adobe.com</span>  - alleen beschikbaar voor Experience Cloud-gebruikers. </p> <p> <span class="filepath"> sc.omniture.com</span>  - Alleen voor gebruikers van analysemogelijkheden en voor gebruikers van Experience Cloud met hun analysegegevens. </p> <p>Tijdens migratie kunnen beheerders <span class="filepath"> omniture.com</span> aanmeldingscapaciteit voor specifieke gebruikers uitschakelen. </p> </td> 
   <td colname="col4"> <p>Admin Console </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Een groep maken </td> 
   <td colname="col2"> <p>Admin Console - Wanneer een groep in Admin Console wordt gecreeerd, zal een in kaart gebrachte groep in Analytics in de Hulpmiddelen Admin verschijnen, maar deze in kaart gebrachte groep kan zijn naam niet hebben veranderd van Hulpmiddelen Admin, of uit Hulpmiddelen Admin worden geschrapt. </p> <p>Admin Tools. </p> </td> 
   <td colname="col3"> <p>Admin Console (<a href="https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html"> creeer productconfiguratie</a>) </p> </td> 
   <td colname="col4"> <p>Admin Console (<a href="https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html"> creeer productconfiguratie</a>) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebruikers in een groep bewerken </td> 
   <td colname="col2"> <p>Admin Console - Alleen voor Experience Cloud-gebruikers </p> <p>Hulpprogramma's voor beheerders - gebruikers met alleen analyse en gebruikers van de Experience Cloud-kunnen via de beheerhulpprogramma's worden bewerkt. Als een gebruiker van de Experience Cloud echter deel uitmaakt van een groep in de Admin Console, kan hij of zij niet uit de groep worden verwijderd in de beheerprogramma's. </p> </td> 
   <td colname="col3"> <p>Admin Console - alleen Experience Cloud-gebruikers </p> <p> Hulpmiddelen Admin - de analytische-slechts logins kunnen nog aan/uit groepen in Hulpmiddelen worden toegevoegd Admin. </p> </td> 
   <td colname="col4"> <p>Admin Console </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Machtigingen voor een groep bewerken </td> 
   <td colname="col2"> <p>Admin Console - U kunt groepen bewerken die in de Admin Console zijn gemaakt. </p> <p>Gereedschappen voor beheerders - U kunt machtigingen voor elke groep bewerken. </p> </td> 
   <td colname="col3"> <p>Admin Console </p> </td> 
   <td colname="col4"> <p>Admin Console </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Groep verwijderen </td> 
   <td colname="col2"> <p>Admin Console - U kunt alleen groepen verwijderen die in de Admin Console zijn gemaakt. </p> <p>Hulpmiddelen Admin - U kunt slechts groepen schrappen die van de Hulpmiddelen van Admin worden gecreeerd. </p> </td> 
   <td colname="col3"> <p>Admin Console </p> </td> 
   <td colname="col4"> <p>Admin Console </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Beheerdersstatus voor gebruiker wijzigen </td> 
   <td colname="col2"> <p>Admin Console - Alleen voor Experience Cloud-gebruikers. </p> <p>Admin Tools </p> </td> 
   <td colname="col3"> <p>Admin Console - Alleen voor Experience Cloud-gebruikers. </p> <p>Admin Tools - Alleen voor Analytics-gebruikers. </p> </td> 
   <td colname="col4"> <p>Admin Console </p> </td> 
  </tr> 
 </tbody> 
</table>
