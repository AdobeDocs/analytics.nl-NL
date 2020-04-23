---
description: Wat u moet weten over de migratie van gebruikers-id's voor Analytics naar de beheerconsole in de Adobe Experience Cloud.
title: Analyseer gebruikersmigratie naar de beheerconsole
uuid: 7d020713-693b-4945-aa52-3669a631aacb
translation-type: tm+mt
source-git-commit: 5e47974fcf95625def21a9011ad981197ae39c99

---


# Analyseer gebruikersmigratie naar de beheerconsole{#analytics-user-migration-to-the-admin-console}

Wat u moet weten over de migratie van gebruikers-id&#39;s voor Analytics naar de beheerconsole in de Adobe Experience Cloud.

Raadpleeg de gebruikershandleiding [van de](https://helpx.adobe.com/enterprise/administering/user-guide.html)beheerconsole voor algemene Help over de onderwerpen in de beheerconsole (die geen verband houden met de migratie van analysemogelijkheden).

Nadat u een migratie hebt uitgevoerd, kunt u gebruikers en producten [van de Experience Cloud](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/admin-getting-started.html) beheren in de beheerconsole.

## Wat is de migratie van de gebruikers-id voor Analytics? {#section-adbe49aba10c4e62afa836a97894107c}

Met de migratie van gebruikers-id&#39;s voor Analytics kunnen beheerders gebruikersaccounts in Analytics User Management eenvoudig migreren naar de Adobe Admin Console. Nadat uw gebruikers zijn gemigreerd, hebben ze toegang tot de oplossingen en kernservices die beschikbaar zijn in de Experience Cloud. De migratie wordt in fasen aan klanten uitgevoerd.

De voordelen van het gebruik van de beheerconsole zijn:

<table id="table_E4465796E224474680D750CAC5434ED3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Voordeel </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Single Sign-On </p> </td> 
   <td colname="col2"> <p>Gebruikers van Analytics kunnen zich aanmelden bij de Experience Cloud en alle oplossingen met hun Adobe-id of Enterprise-id. Met deze aanmelding hebt u toegang tot geïntegreerde oplossingen en kernservices in de Experience Cloud. </p> <p>Na de migratie worden gebruikers die proberen zich aan te melden via oude logins (<span class="filepath"> my.omniture.com</span> en <span class="filepath"> sc.omniture.com</span>) omgeleid naar <span class="filepath"> experienceCloud.adobe.com</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gebruikers-id en -machtigingen beheren </p> </td> 
   <td colname="col2"> <p>Analysebeheerders kunnen gebruikers en machtigingen uitsluitend beheren in de <a href="http://adminconsole.adobe.com/enterprise/"> beheerconsole</a> (http://adminconsole.adobe.com/enterprise/). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Producten en kernservices beheren </p> </td> 
   <td colname="col2"> 
    <ul id="ul_01043FEF271E4B27BF34980D629D1932"> 
     <li id="li_DC31AE8BAAB843F39A7CC9EB047265D5">Nieuwe gebruikers uitnodigen </li> 
     <li id="li_73724DD7D79E41F8A1D58C74E37674BA">Productprofielen maken </li> 
     <li id="li_7E75FC68E0F84873A9A211D2707B6DE7">Gebruikers toestemming geven voor specifieke producten en services </li> 
     <li id="li_9C8A340A7C9A45A98EC0BD4AF9E100FF">Toegang tot de kernservices <a href="https://docs.adobe.com/content/help/en/core-services/interface/experience-cloud.html"></a> voor meerdere oplossingen die beschikbaar zijn in de Adobe Experience Cloud </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Wat u moet weten (en doen) voordat u gebruikers-id&#39;s (FAQ) migreert {#section-b0fc7f0bbd4b488e95b0c8e77ff077a9}

Antwoorden op vragen die u vóór de migratie hebt.

<table id="table_36FD7EF1DAB44D359F4FC186D93147E5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Vraag/taak </th> 
   <th colname="col2" class="entry"> Antwoord </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Ik ben beheerder van Analytics en heb een e-mail voor migratie ontvangen. Wat doe ik eerst? </p> </td> 
   <td colname="col2"> <p>Controleer of u een Adobe-id hebt en toegang hebt tot de beheerconsole <a href="https://adminconsole.adobe.com/enterprise/"> van</a>Experience Cloud. </p> <p>Als dat niet het geval is, neemt u contact op met de <a href="https://helpx.adobe.com/marketing-cloud/contact-support.html"> klantenservice</a>van Adobe. (U moet eerst contact opnemen met de systeem- of productbeheerder die u kan uitnodigen voor de juiste organisatie.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>AEM-integratie met Analytics </p> </td> 
   <td colname="col2"> <p> AEM-gebruikers met een integratie in Analytics moeten hun configuratie wijzigen om het gedeelde geheim Analytics te gebruiken in plaats van het wachtwoord. </p> <p> Dit moet u doen voordat de migratie is ingeschakeld. Als de migratie eenmaal is uitgeschakeld, is het oorspronkelijk geconfigureerde wachtwoord niet meer geldig. </p> <p><b>Het gedeelde geheim in Analytics verkrijgen</b> </p> <p> Het gedeelde geheim kan worden verkregen uit Analytics (<span class="uicontrol"> Analytics</span> &gt; <span class="uicontrol"> User Management</span>) en is verschillend voor elke gebruiker. </p> <p><b>Om uw configuratie AEM met het gedeelde geheim bij te werken</b> </p> <p>Zie Verbinding maken met Adobe Analytics en Frameworks <a href="https://helpx.adobe.com/experience-manager/6-3/sites/administering/using/adobeanalytics-connect.html"></a>maken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Report Builder bijwerken </p> </td> 
   <td colname="col2"> <p> <p>Belangrijk: Werk uw installatie van <a href="https://marketing.adobe.com/resources/help/en_US/arb/t_install_arb.html"> de Bouwer</a> van het Rapport aan de recentste versie bij. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wanneer begint de migratie? </p> </td> 
   <td colname="col2"> <p>Adobe zal Analytics-beheerders via e-mail op de hoogte stellen van de datum waarop de migratie wordt gestart. </p> <p>Migraties naar de beheerconsole vinden plaats in golven. Op de dag van de migratie waarschuwt Adobe de Analytische beheerders en verleent hen toegang tot het migratiehulpmiddel. Nadat een aanmeldingsbedrijf voldoet aan de criteria die voor elke migratiegolf zijn gedefinieerd, doet Adobe het volgende: </p> 
    <ul id="ul_D7DDC62A08AB4407B122985EDEA6ABD1"> 
     <li id="li_BA0AD50DCDC14C90ADD513DEF6F78180">Stel de begin- en einddatum in voor de migratie van het bedrijf. </li> 
     <li id="li_C048A5C64FAA46C4BB41EF24F1CEDF62">Verzend een e-mailbericht naar de huidige analysebeheerders van het bedrijf, ongeveer 30 dagen voor de migratie. </li> 
     <li id="li_476265B24CE2404B995201170C75D674">Geef een productmelding weer om beheerders op de hoogte te brengen van de begindatum van de migratie. </li> 
    </ul> <p> Op de dag van de migratie worden de voormalige machtigingsgroepen automatisch naar de beheerconsole gekopieerd. U kunt geen nieuwe gebruikers meer uitnodigen of nieuwe groepen maken in Analytics Admin Tools. </p> <p>Na de migratie: </p> 
    <ul id="ul_4639963EB08F407F8C18ACE2B3D30223"> 
     <li id="li_7F24A3FC900146C3B2E988D399C859EA">Beheerders gebruiken de beheerconsole om hun gebruikers en machtigingen voor Analytics te beheren. (U gebruikt de gebruikersbeheerinterface niet meer in Analytics &gt; Admin &gt; User Management.) </li> 
     <li id="li_5B5234D4F94A4B96A8920F6A5831A64C">Gebruikers krijgen toegang tot Analytics met hun Adobe- of Enterprise-id via de Experience Cloud in plaats van via <span class="filepath"> my.omniture.com</span>. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wat gebeurt er op de begindatum van de migratie? </p> </td> 
   <td colname="col2"> <p>Om 10:00 uur UTC op de startdatum van de migratie: </p> 
    <ul id="ul_25D1DBDF5C804D048E741F31550FF5F3"> 
     <li id="li_418476105FE341229CE146E730AAB33D">Uw bestaande machtigingengroepen in Analytics worden automatisch gerepliceerd in de Admin Console als Productprofielen, met inbegrip van hun beschrijving en korrelige toestemmingen over rapportsuites, metriek, dimensies, Analytics, en de Hulpmiddelen van de Reeks van het Rapport. </li> 
     <li id="li_412F88C454B0455A8F3BC8016226855C">Als een van uw huidige Analytics-gebruikers is gemaakt in de beheerconsole (wat betekent dat ze een gekoppelde Adobe/Enterprise-id hebben), worden ze toegevoegd aan de desbetreffende productprofielen in de beheerconsole. </li> 
     <li id="li_8A05137EC05C4FD5910E73FE58300DCB">De sectie Gebruikersbeheer onder het tabblad Beheer in Analytics wordt ingesteld op alleen- <span class="term"> lezen</span>. U kunt hier geen nieuwe gebruikers of machtigingsgroepen meer maken en u moet beide functies in de beheerconsole uitvoeren. Raadpleeg de <a href="/help/admin/user-management2/user-migration/c-migration-tool.md#section-928ffba27a0446e0af575b720434ef56"> niet-ondersteunde analysefuncties in de beheerconsole</a> voor meer informatie. </li> 
     <li id="li_2742DE69E9B547198A58E1F33E908361">Als beheerder krijgt u toegang tot het migratiehulpprogramma <a href="https://marketing.adobe.com/resources/help/en_US/experience-cloud/admin-console/analytics-migration/t_migrate-users.html">voor</a>gebruikersnamen. Daarnaast wordt een melding in het product weergegeven met de einddatum van de migratie (doorgaans 60 dagen in de toekomst), naast koppelingen voor Help-inhoud en veelgestelde vragen. </li> 
     <li id="li_095D42E3A3544FC59A60A8C8F94C971B">U krijgt toegang tot het tabblad Machtigingen in de beheerconsole waarmee u productprofielen kunt maken met alle korrelige opties die u kent op het gebied van Analyse. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hoe kan ik gebruikers-id's migreren? </p> </td> 
   <td colname="col2"> <p> Klik onder Gebruikersbeheer op Gebruikersnamen <a href="/help/admin/user-management2/user-migration/t-migrate-users.md#task-f3355f3b14a340feae58cfa04c0ba1c9"> migreren</a> op de pagina Beheer. Gebruik het gereedschap om gebruikers toe te voegen aan productprofielen in de beheerconsole (die via machtigingsgroepen in Analytics wordt gerepliceerd). Je kunt gebruikersnamen in je eigen tempo migreren. </p> <p>Beheerdersrechten zijn vereist. Zodra de migratie is voltooid, kan deze niet worden teruggedraaid. </p> <p>Op de einddatum van de migratie wordt <span class="filepath"> mijn.omniture.com</span> -toegang uitgeschakeld voor gebruikers binnen hun aanmeldingsbedrijf. Gebruikers (inclusief gebruikers die nog moeten worden gemigreerd) worden omgeleid naar aanmelden via de nieuwe Experience Cloud-URL (<span class="filepath"> ExperienceCloud.adobe.com</span>) </p> <p>Opmerking:  Adobe raadt u aan de gelegenheid te baat te nemen om een audit van uw gebruikers en groepen uit te voeren voordat u gaat migreren. Oude en ongebruikte accounts verwijderen of accounts die geen toegang meer zouden moeten hebben tot het product (werknemers zijn bijvoorbeeld niet meer bij de organisatie). </p> <p>Verwant onderwerp: <a href="/help/admin/user-management2/user-migration/migrate-enterprise.md"> Migreer Analytics-gebruikersaccounts voor Enterprise- en Federated-id's</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zal de migratie invloed hebben op mijn analytische implementatie of hoe gegevens worden verzameld? </p> </td> 
   <td colname="col2"> <p>Nee. </p> <p>Het migratiehulpmiddel bestaat om u te helpen gebruikersidentiteitskaart en toestemmingen van Analytics Gebruikersbeheer aan de Console <a href="https://adminconsole.adobe.com/enterprise/"> van de Admin van de</a>Ervaring van de Wolk overgaan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hoe lang duurt het migratieproces? </p> </td> 
   <td colname="col2"> <p>Alle huidige analysebeheerders ontvangen vier weken vóór de migratie een e-mail met een melding vóór de migratie. (De werkelijke begindatum wordt weergegeven in de interface Analytics.) </p> <p>Wanneer de migratie begint, hebben beheerders 60 dagen om het proces te voltooien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kan ik mijn migratie versnellen? </p> </td> 
   <td colname="col2"> <p>Ja. Adobe raadt u echter aan de tijd te gebruiken voordat de migratie begint: </p> 
    <ul id="ul_52C7EC44A5534975BFD7A6F37A829C25"> 
     <li id="li_8CFFF72877E8456DAC3241143AD648AD">Controleer of u een productbeheerder voor Analytics in de beheerconsole bent. </li> 
     <li id="li_25DAA8D1EEDA45A0B5B59472BD8896C4">Deel aan uw gebruikersbasis mee dat hun login ervaring zal veranderen wanneer de migratie begint. </li> 
     <li id="li_5B50F942F6A8483FAFA500AFF428702C">Audit uw huidige gebruikers en toestemmingen en voer schoonmaakactiviteiten uit. </li> 
    </ul> <p>Als u de migratie wilt versnellen, neemt u contact op met de succesmanager van de klant op de klantenservice <a href="https://helpx.adobe.com/marketing-cloud/contact-support.html"></a> van Adobe en dient u een aanvraag in voor een eerdere begindatum. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Ik ben een beheerder van Analytics zonder toegang tot de Console Admin. Wie kan mij helpen toegang te krijgen tot de beheerconsole? </p> </td> 
   <td colname="col2"> <p>Elke systeem- of productbeheerder die toegang heeft tot de beheerconsole van uw organisatie kan u toegang geven. Als u niet zeker weet wie binnen uw organisatie beheerdersrechten heeft in de console, neemt u contact op met de <a href="https://helpx.adobe.com/marketing-cloud/contact-support.html"> klantenservice</a>van Adobe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kan ik de startdatum van de migratie uitstellen? </p> </td> 
   <td colname="col2"> <p>Ja. Neem contact op met de <a href="https://helpx.adobe.com/marketing-cloud/contact-support.html"> klantenservice</a>van Adobe. </p> 
    <draft-comment> 
     <p>Zie hieronder voor een beschrijving van de wijzigingen in uw huidige gebruikers- en machtigingenbeheer voor Analytics op de startdatum. </p> 
    </draft-comment> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Nu mijn bedrijf naar de beheerconsole migreert, waar maak ik nieuwe gebruikers en machtigingengroepen voor de begindatum van de migratie? </p> </td> 
   <td colname="col2"> <p>Voordat u de migratie start, kunt u gebruikers maken in de beheerconsole of in Analytics &gt; User Management. </p> <p>Nadat de migratie is begonnen, kunt u alleen gebruikers en machtigingsgroepen maken in de beheerconsole. </p> 
    <draft-comment> 
     <p>Zie de sectie Migratie hieronder voor meer informatie over wat er gebeurt op de startdatum van de migratie.) </p> 
    </draft-comment> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Wanneer kan ik enig teken-op uitvoeren gebruikend Federated IDs? </p> </td> 
   <td colname="col2"> <p> Binnenkort is in de beheerconsole een hulpprogramma beschikbaar waarmee u id-typen kunt wijzigen van Adobe-id's in federatieve id's. Tijdens de migratie kunt u gebruikers niet migreren als gefedereerde id's. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Wat u tijdens de migratie moet weten (FAQ) {#section-d394524aa6d046d79025bbd7499792bc}

Belangrijke informatie over het migratieproces en de invloed ervan op het huidige gebruikersbeheer.

<table id="table_0E37BB1DEA6143F0B5F4E861FCFA7189"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Vraag </th> 
   <th colname="col2" class="entry"> Antwoord </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Hoe worden machtigingsgroepen gerepliceerd naar de beheerconsole? En mijn gebruikers? </p> </td> 
   <td colname="col2"> <p>Een gemigreerde groep Analytics wordt in de beheerconsole een <i>productprofiel</i> genoemd. Machtigingsinstellingen voor de oorspronkelijke groep blijven behouden in de migratie. De gebruikers die aan de groep zijn toegewezen, worden echter niet gemigreerd. Wanneer een gebruiker die tot die groep behoort met het migratiehulpmiddel wordt gemigreerd, wordt die gebruiker toegewezen aan dat productprofiel. </p> <p>Bijvoorbeeld, zal een de toestemmingsgroep van de Verrichtingen van de West-kust die zijn leden aan de Werkruimte van de Bouwer en van de Analyse (met bepaalde rapportsuites, metriek, dimensies) het recht gaf om een het productprofiel van de Verrichtingen van de West-Kost te worden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kan ik de migratieinspanning aan een andere beheerder delegeren? </p> </td> 
   <td colname="col2"> <p>Zodra uw migratie begint, kan elke beheerder die via de Experience Cloud toegang krijgt tot uw Analytics-instantie, het migratiehulpmiddel gebruiken om te beginnen (of door te gaan) met migrerende gebruikers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kan ik het lidmaatschap van machtigingengroepen bijwerken voor niet-gemigreerde gebruikers? </p> </td> 
   <td colname="col2"> <p>Ja. U kunt het groepslidmaatschap van niet-gemigreerde gebruikers wijzigen vanuit de sectie Gebruikersbeheer voor Analytics. </p> 
    <draft-comment> 
     <p>In afwachting van een verduidelijking van Ashok over waar dat gebeurt. </p> 
    </draft-comment> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kan ik gebruikers en machtigingsgroepen maken in Analytics nadat mijn migratie is gestart en deze vervolgens met het migratiehulpprogramma naar de beheerconsole verplaatsen? </p> </td> 
   <td colname="col2"> <p> Nee. Wanneer de migratie is begonnen, moeten alle nieuwe gebruikers en machtigingsgroepen (productprofielen genoemd in de beheerconsole) worden gemaakt in de beheerconsole. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zouden gebruikers die ik met het migratiehulpmiddel migreer de zelfde toestemmingen worden toegewezen die zij in Analytics hadden? </p> </td> 
   <td colname="col2"> <p>Ja. Gebruikers die met het gereedschap zijn gemigreerd, krijgen de machtigingen die ze momenteel in Analytics hebben. Bovendien behouden ze toegang tot hun Analytics-middelen (zoals segmenten, projecten, berekende metriek, enzovoort) wanneer ze toegang krijgen tot Analytics via de Experience Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hebben gebruikers die ik naar de beheerconsole migreer toegang tot Analytics via <span class="filepath"> my.omniture.com</span>? </p> </td> 
   <td colname="col2"> <p>Ja. Gemigreerde gebruikers blijven toegang krijgen tot Analytics met hun bestaande gebruikersnaam en wachtwoord via <span class="filepath"> my.omniture.com</span> tot de einddatum van de migratie, tenzij u hun oudere aanmeldingsgegevens uitschakelt via het migratiehulpprogramma. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Twee of meer van mijn gebruikers hebben dezelfde e-mailid in hun analysebestand. Wat gebeurt er als ik ze migreer? </p> </td> 
   <td colname="col2"> <p>Omdat voor gebruikersaccounts in de beheerconsole unieke e-mailadressen nodig zijn, wordt een fout met de naam 'E-mailadres dupliceren' weergegeven wanneer u probeert meerdere van deze gebruikers te migreren. U kunt de e-mailadressen van niet-gemigreerde gebruikers bijwerken in de sectie Gebruikersbeheer (verouderd) voordat u de migratie opnieuw uitvoert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Wat doe ik na het migreren van mijn gebruikers? </p> </td> 
   <td colname="col2"> <p>Schakel de oudere aanmeldingstoegang tot <span class="filepath"> my.omniture.com</span>uit. U kunt de aanmelding voor oudere versies alleen uitschakelen als deze zijn gemigreerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kan ik het migratieproces volgen? </p> </td> 
   <td colname="col2"> <p>Het migratiehulpmiddel omvat een dashboard dat toont hoeveel van uw gebruikers met succes zijn gemigreerd, en hoeveel van hen hun erfenislogin gehandicapt hebben. </p> <p> In het ideale geval hebt u uw aanmeldingsbedrijf naar de beheerconsole gemigreerd wanneer een 100% van uw gebruikers de migratie heeft voltooid en de oudere aanmeldingen hebben uitgeschakeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tijdens de migratie moet ik gebruikers- en machtigingsbeheer uitvoeren. Met welk gereedschap kan ik deze taak uitvoeren? </p> </td> 
   <td colname="col2"> <p>Nadat de migratie is begonnen, gebruikt u de beheerconsole om nieuwe gebruikers en productprofielen te maken en te beheren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wat ervaren mijn gebruikers wanneer ik hen gebruikend het hulpmiddel migreer? </p> </td> 
   <td colname="col2"> <p>Ze zullen een welkomstbericht ontvangen dat is geadresseerd aan de e-mailadres in hun Analytics-gebruikersrecord en ze via de Experience Cloud op de hoogte stellen van hun nieuwe manier om toegang te krijgen tot Analytics. Als ze geen bestaande Adobe-id hebben, wordt hun gevraagd om er een te maken, waarna ze met hun Adobe-id toegang tot de oplossing kunnen krijgen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kan ik API's gebruiken om mijn gebruikers te migreren in plaats van het migratiehulpmiddel te gebruiken? </p> </td> 
   <td colname="col2"> <p>Nee. U moet het migratiehulpprogramma gebruiken om ervoor te zorgen dat alle bestaande gebruikers naar de beheerconsole worden gemigreerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Welke analysefuncties voor gebruikersbeheer zijn niet beschikbaar in de beheerconsole? </p> </td> 
   <td colname="col2"> 
    <ul id="ul_3F3747D4C1D3420699F7D28EC0CA1AA0"> 
     <li id="li_BD943B3245FF47E7A0DDA6107EA1EF89">Middelen overdragen </li> 
     <li id="li_2DF7004D67ED4C6CB40461EEFB038A5A">Vervaldatum gebruiker </li> 
     <li id="li_980E3F5B98F344A492B0EBAD7F1DA60C">Gebruikerslogboeken </li> 
    </ul> <p>Deze blijven beschikbaar in Analytics-gebruikersbeheer. </p> <p>Raadpleeg de <a href="/help/admin/user-management2/user-migration/c-migration-tool.md"> niet-ondersteunde analysefuncties in de beheerconsole</a> voor meer informatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>We hebben verschillende configuraties gemaakt in de beheerconsole en deze toegewezen aan machtigingsgroepen Analytics. Wat zal met die configuraties gebeuren wanneer de migratie begint? </p> </td> 
   <td colname="col2"> <p>In de beheerconsole worden machtigingsgroepen voor Analytics opnieuw gemaakt als productprofielen, net als in alle andere groepen. Dit betekent u twee productprofielen in de console zult zien die hoofdzakelijk dubbele toestemmingen hebben. U kunt dubbele productprofielen verwijderen uit de beheerconsole. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wat is mijn volgende stap na het migreren van gebruiker? </p> </td> 
   <td colname="col2"> <p>Nadat u de gebruiker of een reeks gebruikers hebt gemigreerd, bestaat de volgende stap uit het uitschakelen van de oude aanmelding via <span class="filepath"> my.omniture.com</span>. U kunt dit doen door deze gebruikers te selecteren in het migratiehulpmiddel en op de contextafhankelijke optie "Oudere aanmelding uitschakelen" te klikken die boven aan het scherm wordt weergegeven. Deze optie is alleen zichtbaar wanneer u een gebruiker of een set gebruikers selecteert die allemaal met succes naar de beheerconsole zijn gemigreerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wat gebeurt er op de einddatum van de migratie? </p> </td> 
   <td colname="col2"> <p>Na de einddatum van de migratie (60 dagen vanaf het begin van de migratie) worden alle gebruikers in uw aanmeldingsbedrijf omgeleid naar aanmelden via de aanmeldingspagina van de Experience Cloud met hun Adobe-id's. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ik heb niet al mijn gebruikers tegen de migratie-einddatum kunnen migreren. Zouden niet-gemigreerde gebruikers hun toegang tot Analytics verliezen? </p> </td> 
   <td colname="col2"> <p>Gebruikers die op de einddatum niet zijn gemigreerd, worden omgeleid naar de aanmeldingspagina van Experience Cloud (Experience Cloud.adobe.com) en hebben geen toegang tot Analytics. U blijft echter wel toegang hebben tot het migratiehulpprogramma, zodat u deze kunt zoeken en migreren om de toegang te herstellen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Wat te weten na de migratie (FAQ) {#section-9681baa01b8c41cdb9659b73b70b50ff}

<table id="table_F48CC9DFE3424AC9AD76A16882701C8F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Vraag/probleem </th> 
   <th colname="col2" class="entry"> Antwoorden </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Gebruikers verwijderen uit de beheerconsole </p> </td> 
   <td colname="col2"> <p> In Analytics wordt een verwijderde gebruiker ingesteld als <span class="term"> verlopen</span>, maar het account blijft bestaan. Het behouden van de rekening laat de overdragende activa, zoals segmenten, berekende metriek, geplande rapporten, projecten, etc. toe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verlopen van accounts </p> </td> 
   <td colname="col2"> <p> U kunt handmatig een vervaldatum van een account instellen in Analytics in Admin Tools. Als aan de vervaldatum is voldaan, heeft de gebruiker geen toegang tot Analytics, maar wel tot zijn of haar werkelijke gebruikersaccount voor Experience Cloud (bijvoorbeeld Adobe-id, Enterprise-id, Federated ID, enz.) verloopt niet. Ze kunnen zich nog steeds aanmelden bij Experience Cloud, maar ze kunnen alleen niet in Analytics klikken. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Niet-ondersteunde analysefuncties in de beheerconsole {#section-928ffba27a0446e0af575b720434ef56}

>[!IMPORTANT]
>
>Bekijk de volgende problemen die tijdens de migratie op u van toepassing kunnen zijn.

<table id="table_88E2FA03D5F241B79AB54D12F64B51DA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Vraag/probleem </th> 
   <th colname="col2" class="entry"> Antwoorden </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Aanmelden als </p> </td> 
   <td colname="col2"> <p> Beheerders die naar de beheerconsole migreren, kunnen de functie Aanmelden als niet-beheerdersaccounts die naar de beheerconsole zijn gemigreerd, niet meer openen. Deze functie is vervangen door Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vervaldatum gebruiker en overdracht van middelen </p> </td> 
   <td colname="col2"> <p> De beheerconsole biedt geen ondersteuning voor het verlopen van gebruikers of het overdragen van middelen. Beheerders gebruiken de sectie Analytics Users and Assets onder Admin Tools in Analytics voor beide functies. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Laatste toegang (laatste aanmelding) </p> </td> 
   <td colname="col2"> <p> Gegevens over de laatste aanmelddatum en -tijd van een gebruiker zijn beschikbaar via de koppeling Gebruikers en middelen voor analyse en niet via de beheerconsole. De laatste aanmeldingsdatum in Analytics is specifiek voor de datum waarop gebruikers vanuit Experience Cloud toegang hebben tot Analytics en geeft niet de datum/tijd weer waarop ze zich hebben aangemeld bij Experience Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gebruikersbeheer-API's Door <a href="https://helpx.adobe.com/enterprise/help/identity.html"> Adobe ondersteunde identiteitstypen</a> </p> </td> 
   <td colname="col2"> <p> Beheerders die naar de beheerconsole migreren, moeten API's voor gebruikersbeheer configureren<a href="https://www.adobe.io/apis/cloudplatform/usermanagement/docs/gettingstarted.html"></a> die bij Adobe I/O worden aangeboden voor programmatische toegang tot gebruikersaccounts in de beheerconsole. </p> <p>De API's voor analysebevoegdheden worden uitgeschakeld wanneer u de migratie wilt inschakelen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Webservicereferenties </p> </td> 
   <td colname="col2"> <p> De referenties van de webservice van gebruikers (en hun gedeelde geheim) zijn niet beschikbaar in de beheerconsole en kunnen worden geopend door in de sectie Analytics Users and Assets op de specifieke gebruiker te klikken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Single Sign-On </p> </td> 
   <td colname="col2"> <p> Configuraties met eenmalige aanmelding voor analysemogelijkheden worden verwijderd wanneer u de migratie hebt voltooid. Ze zullen actief blijven tijdens de migratie. Klanten die het eenmalige aanmelding voor Analytics gebruiken, dienen een upgrade naar de <a href="https://helpx.adobe.com/enterprise/help/identity.html"> Adobe Federated ID</a>uit te voeren. </p> <p>Analytics raadt u aan uw gebruikers eerst als Adobe-id te migreren om eenvoudig de Experience Cloud-accounts te maken en deze vervolgens om te zetten in gefedereerde gebruikers voor één ondertekening. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Machtigingsgroepen downloaden </p> </td> 
   <td colname="col2"> <p> Het downloaden van gegevens voor machtigingengroepen wordt niet meer ondersteund in de beheerprogramma's voor analysemogelijkheden of in de beheerconsole van Adobe. Klanten moeten de API's voor gebruikersbeheer van adobe.io gebruiken om informatie over machtigingengroepen bulksgewijs op te halen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aanmaakdatum account </p> </td> 
   <td colname="col2"> <p>Gegevens over de aanmaakdatum van accounts worden niet meer ondersteund in de hulpprogramma's voor Analysebeheer of de Adobe Admin Console. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bulkmail </p> </td> 
   <td colname="col2"> <p>Bulk-e-mail naar gebruikers wordt niet meer ondersteund in de beheerconsole voor analysemogelijkheden of in de beheerconsole van Adobe. Klanten kunnen hun e-mailadressen van hun gebruikers bulksgewijs exporteren vanuit Adobe Admin Console en een e-mail verzenden met een willekeurige e-mailclient die ze wensen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Uw gebruikers op de hoogte stellen van de migratie {#section-f3b25f672a3a4d03b0559656fd99d20a}

U kunt dit migratieplan proactief aan uw huidige gebruikers willen meedelen. Hier volgt een sjabloon die u kunt aanpassen om al uw huidige gebruikers van Analytics te verzenden:

Als u een e-mail wilt sturen naar alle gebruikers, navigeert u naar **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL User Management]** > [Gebruikers](https://marketing.adobe.com/resources/help/en_US/reference/t_email_users.html)e-mailen.

**Betreft:** Binnenkort verkrijgbaar - Een nieuwe manier om u aan te melden bij Adobe Analytics en Adobe Experience Cloud.

**Lichaam:** Hallo gebruikers van Adobe Analytics!

Ons bedrijf zal alle Adobe Analytics-accounts migreren van [!DNL https://my.omniture.com/login/] naar Adobe Experience Cloud ([experienceCloud.adobe.com](http://experiencecloud.adobe.com/)). Met deze migratie wordt uw Adobe Analytics-account bijgewerkt zodat u toegang hebt tot Analytics via de Adobe Experience Cloud. Terwijl de methode om tot Analytics toegang te hebben zal veranderen, zullen al uw bestaande toestemmingen aan uw rapportsuites en hulpmiddelen worden bewaard.

**Volgende stappen:** We beginnen gebruikers te migreren die op de **INSERT DATE** beginnen. Kijk naar een welkomstbericht met uw nieuwe aanmelding die is gericht aan de e-mailadres dat wordt vermeld onder uw analyseaccount. Als u geen [Adobe-id](https://helpx.adobe.com/x-productkb/global/adobe-id-account-change.html) hebt ingesteld die is gekoppeld aan uw e-mailadres, wordt u gevraagd een account in te stellen.

**Nuttige bronnen:**

[Meld u aan en beheer uw profielinstellingen](https://marketing.adobe.com/resources/help/en_US/mcloud/getting-started-experience-cloud.html).

[Clouds, Core Services en oplossingen](https://marketing.adobe.com/resources/help/en_US/mcloud/solutions_capability_names.html) in de Experience Cloud

Neem contact op met uw analysebeheerders als u vragen of problemen hebt.

Best

Analysebeheer
