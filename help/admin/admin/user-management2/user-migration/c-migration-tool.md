---
description: Wat u moet weten over de migratie van de gebruikers-id voor Analytics naar de Admin Console in de Adobe Experience Cloud.
title: Analyse van gebruikersmigratie naar de Admin Console
feature: Admin Tools
exl-id: f4bc0e92-af53-40db-8138-44d29e4b25fe
role: Admin
source-git-commit: b90356050a6ff39e1688a10f6aa0af284284e2a6
workflow-type: tm+mt
source-wordcount: '3077'
ht-degree: 0%

---

# Analyseer gebruikersmigratie naar de Adobe Admin Console{#analytics-user-migration-to-the-admin-console}

Wat u moet weten over de migratie van gebruikers-id&#39;s voor Analytics naar de Adobe Admin Console in de Adobe Experience Cloud.

Voor algemene hulp op de onderwerpen van Adobe Admin Console (niet verwant met de migratie van Analytics), zie {de Gids van de Gebruiker van de Admin Console 0} [&#128279;](https://helpx.adobe.com/nl/enterprise/administering/user-guide.html).

Nadat u migreert, kunt u [ Experiencen Cloud gebruikers en producten ](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html?lang=nl-NL) in Adobe Admin Console beheren.

## Wat is de migratie van de gebruikers-id voor Analytics? {#section-adbe49aba10c4e62afa836a97894107c}

Met de migratie van gebruikers-id&#39;s voor Analytics kunnen beheerders gebruikersaccounts in Analytics User Management eenvoudig migreren naar de Adobe Admin Console. Nadat uw gebruikers zijn gemigreerd, hebben zij toegang tot de oplossingen en de kerndiensten beschikbaar in het Experience Cloud. De migratie wordt in fasen aan klanten uitgevoerd.

De voordelen van het gebruik van de Adobe Admin Console zijn:

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
   <td colname="col2"> <p>Gebruikers van analysemogelijkheden kunnen zich aanmelden bij het Experience Cloud en alle oplossingen met hun Adobe ID of Enterprise ID. Deze aanmelding maakt toegang tot geïntegreerde oplossingen en kernservices in de Experience Cloud mogelijk. </p> <p>Na de migratie, worden de gebruikers die proberen binnen via erfenislogins (<span class="filepath"> my.omniture.com </span> en <span class="filepath"> sc.omniture.com </span>) te ondertekenen opnieuw gericht aan <span class="filepath"> experienceCloud.adobe.com </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gebruikers-id en -machtigingen beheren </p> </td> 
   <td colname="col2"> <p>Analysebeheerders kunnen gebruikers en toestemmingen uitsluitend in de <a href="https://adminconsole.adobe.com/enterprise/"> Admin Console </a> beheren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Producten en kernservices beheren </p> </td> 
   <td colname="col2"> 
    <ul id="ul_01043FEF271E4B27BF34980D629D1932"> 
     <li id="li_DC31AE8BAAB843F39A7CC9EB047265D5">Nieuwe gebruikers uitnodigen </li> 
     <li id="li_73724DD7D79E41F8A1D58C74E37674BA">Productprofielen maken </li> 
     <li id="li_7E75FC68E0F84873A9A211D2707B6DE7">Gebruikers toestemming geven voor specifieke producten en services </li> 
     <li id="li_9C8A340A7C9A45A98EC0BD4AF9E100FF">Verbeter toegang tot <a href="https://experienceleague.adobe.com/docs/core-services/interface/experience-cloud.html?lang=nl-NL"> de dwars-oplossing kerndiensten </a> beschikbaar in Adobe Experience Cloud </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Wat u moet weten (en doen) voordat u gebruikers-id&#39;s (FAQ) migreert {#section-b0fc7f0bbd4b488e95b0c8e77ff077a9}

Antwoorden op vragen die u mogelijk hebt vóór de migratie.

<table id="table_36FD7EF1DAB44D359F4FC186D93147E5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Vraag/taak </th> 
   <th colname="col2" class="entry"> Antwoord </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Ik ben beheerder van Analytics en heb een e-mail voor migratie ontvangen. Wat moet ik eerst doen? </p> </td> 
   <td colname="col2"> <p>Controleer of u een Adobe ID hebt en of u toegang hebt tot de Admin Console <a href="https://adminconsole.adobe.com/enterprise/"> Experience Cloud </a> . </p> <p>Als dat niet het geval is, neemt u contact op met de <a href="https://helpx.adobe.com/nl/marketing-cloud/contact-support.html"> klantenservice van de Adobe </a> . (U moet eerst contact opnemen met de systeem- of productbeheerder die u kan uitnodigen voor de juiste organisatie.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>AEM integratie met Analytics </p> </td> 
   <td colname="col2"> <p> AEM gebruikers met een integratie in Analytics moeten hun configuratie wijzigen om het gedeelde geheim Analytics te gebruiken in plaats van het wachtwoord. </p> <p> Dit moet u doen voordat de migratie is ingeschakeld. Als de migratie eenmaal is uitgeschakeld, is het oorspronkelijk geconfigureerde wachtwoord niet meer geldig. </p> <p><b> om het gedeelde geheim in Analytics </b> te verkrijgen </p> <p> Het gedeelde geheim kan uit Analytics (<span class="uicontrol"> Analytics </span> worden verkregen &gt; <span class="uicontrol"> Gebruikersbeheer </span>) en is verschillend voor elke gebruiker. </p> <p><b> om uw AEM configuratie met het gedeelde geheim </b> bij te werken </p> <p>Zie <a href="https://helpx.adobe.com/nl/experience-manager/6-3/sites/administering/using/adobeanalytics-connect.html"> Verbinding maken met Adobe Analytics en Frameworks maken </a> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Report Builder bijwerken </p> </td> 
   <td colname="col2"> <p> <p>Belangrijk: werk de installatie van <a href="https://experienceleague.adobe.com/nl/docs/analytics/analyze/report-builder/report-builder-setup"> Report Builder </a> bij tot de meest recente versie. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wanneer begint de migratie? </p> </td> 
   <td colname="col2"> <p>Adobe zal Analytics-beheerders via e-mail op de hoogte stellen van de datum waarop de migratie zal beginnen. </p> <p>Migraties naar de Adobe Admin Console vinden plaats in golven. Op de dag van migratie, brengt de Adobe de beheerders van Analytics op de hoogte en verleent hen toegang tot het migratiehulpmiddel. Nadat een login bedrijf aan de criteria voldoet die voor elke migratiegolf worden bepaald, zal de Adobe: </p> 
    <ul id="ul_D7DDC62A08AB4407B122985EDEA6ABD1"> 
     <li id="li_BA0AD50DCDC14C90ADD513DEF6F78180">Stel de begin- en einddatum in voor de migratie van het bedrijf. </li> 
     <li id="li_C048A5C64FAA46C4BB41EF24F1CEDF62">Verzend een e-mailbericht naar de huidige analysebeheerders van het bedrijf, ongeveer 30 dagen voor de migratie. </li> 
     <li id="li_476265B24CE2404B995201170C75D674">Geef een productmelding weer om beheerders op de hoogte te brengen van de begindatum van de migratie. </li> 
    </ul> <p> Op de dag van de migratie worden uw voormalige machtigingsgroepen automatisch naar de Adobe Admin Console gekopieerd. U kunt geen nieuwe gebruikers meer uitnodigen of nieuwe groepen maken in Analytics Admin Tools. </p> <p>Na de migratie: </p> 
    <ul id="ul_4639963EB08F407F8C18ACE2B3D30223"> 
     <li id="li_7F24A3FC900146C3B2E988D399C859EA">Beheerders gebruiken de Adobe Admin Console om hun Analytics-gebruikers en -machtigingen te beheren. (U gebruikt de gebruikersbeheerinterface niet meer in Analytics &gt; Admin &gt; User Management.) </li> 
     <li id="li_5B5234D4F94A4B96A8920F6A5831A64C">De gebruikers zullen tot Analytics toegang hebben gebruikend hun Adobe of Enterprise ID door het Experience Cloud in plaats van <span class="filepath"> my.omniture.com </span>. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wat gebeurt er op de begindatum van de migratie? </p> </td> 
   <td colname="col2"> <p>Om 10:00 uur UTC op de startdatum van de migratie: </p> 
    <ul id="ul_25D1DBDF5C804D048E741F31550FF5F3"> 
     <li id="li_418476105FE341229CE146E730AAB33D">Uw bestaande machtigingengroepen in Analytics worden automatisch gerepliceerd in de Adobe Admin Console als productprofielen, met inbegrip van hun beschrijving en korrelige machtigingen voor de verschillende rapportsuites, maateenheden, Analytics en Report Suite-gereedschappen. </li> 
     <li id="li_412F88C454B0455A8F3BC8016226855C">Als een van uw huidige analytische gebruikers in de Adobe Admin Console is gemaakt (wat betekent dat ze een gekoppelde Adobe/Enterprise ID hebben), worden ze toegevoegd aan de desbetreffende productprofielen in de Adobe Admin Console. </li> 
     <li id="li_8A05137EC05C4FD5910E73FE58300DCB">De sectie Gebruikersbeheer onder het tabblad Beheer in Analytics wordt ingesteld op <span class="term"> alleen-lezen </span> . U kunt hier geen nieuwe gebruikers of machtigingsgroepen meer maken en u moet beide functies in de Adobe Admin Console uitvoeren. Zie <a href="/help/admin/admin/user-management2/user-migration/c-migration-tool.md#section-928ffba27a0446e0af575b720434ef56"> Niet-ondersteunde analysefuncties in de Adobe Admin Console </a> voor meer informatie. </li> 
     <li id="li_2742DE69E9B547198A58E1F33E908361">Als beheerder, zult u toegang tot het <a href="https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/user-management/migrate-users/t-migrate-users.html?lang=nl-NL"> hulpmiddel van de Migratie van identiteitskaart van de Gebruiker </a> worden verleend. Daarnaast wordt een melding in het product weergegeven met de einddatum van de migratie (doorgaans 60 dagen in de toekomst), naast koppelingen naar Help-inhoud en veelgestelde vragen. </li> 
     <li id="li_095D42E3A3544FC59A60A8C8F94C971B">U krijgt toegang tot het tabblad Machtigingen in de Adobe Admin Console waarmee u productprofielen kunt maken met alle korrelige opties die u kent in Analytics. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hoe kan ik gebruikersnamen migreren? </p> </td> 
   <td colname="col2"> <p> Klik op <a href="/help/admin/admin/user-management2/user-migration/t-migrate-users.md#task-f3355f3b14a340feae58cfa04c0ba1c9"> Gebruikersnamen migreren </a> op de beheerpagina onder Gebruikersbeheer. Gebruik het gereedschap om gebruikers toe te voegen aan productprofielen in de Adobe Admin Console (gerepliceerd uit machtigingsgroepen in Analytics). Je kunt gebruikersnamen in je eigen tempo migreren. </p> <p>Beheerdersrechten zijn vereist. Zodra de migratie is voltooid, kan deze niet worden teruggedraaid. </p> <p>Op de einddatum van de migratie, <span class="filepath"> my.omniture.com </span> toegang zal voor gebruikers binnen hun login bedrijf worden onbruikbaar gemaakt. De gebruikers (met inbegrip van die die nog moeten worden gemigreerd) zullen aan login via het nieuwe Experience Cloud URL (<span class="filepath"> ervarencecloud.adobe.com </span>) worden opnieuw gericht </p> <p>Opmerking: Adobe raadt u aan de mogelijkheid te baat te nemen om een controle van uw gebruikers en groepen uit te voeren voordat u gaat migreren. Oude en ongebruikte accounts verwijderen of accounts die geen toegang meer zouden moeten hebben tot het product (werknemers zijn bijvoorbeeld niet meer bij de organisatie). </p> <p>Verwante onderwerp: <a href="/help/admin/admin/user-management2/user-migration/migrate-enterprise.md"> Migreer de gebruikersrekeningen van de Analyse voor Onderneming en Federated IDs </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zal de migratie invloed hebben op mijn analytische implementatie of hoe gegevens worden verzameld? </p> </td> 
   <td colname="col2"> <p>Nee. </p> <p>Het migratiehulpmiddel bestaat om u te helpen gebruikersidentiteitskaart en toestemmingen van het Beheer van de Gebruiker van de Analyse aan de <a href="https://adminconsole.adobe.com/enterprise/"> Admin Console van het Experience Cloud </a> overgaan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hoe lang duurt het migratieproces? </p> </td> 
   <td colname="col2"> <p>Alle huidige analysebeheerders ontvangen vier weken vóór de migratie een e-mail met een melding vóór de migratie. (De werkelijke begindatum wordt weergegeven in de interface Analytics.) </p> <p>Wanneer de migratie begint, hebben beheerders 60 dagen om het proces te voltooien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kan ik mijn migratie versnellen? </p> </td> 
   <td colname="col2"> <p>Ja. De Adobe raadt u echter aan de tijd te gebruiken voordat de migratie begint: </p> 
    <ul id="ul_52C7EC44A5534975BFD7A6F37A829C25"> 
     <li id="li_8CFFF72877E8456DAC3241143AD648AD">Controleer of u een productbeheerder voor Analytics in de Adobe Admin Console bent. </li> 
     <li id="li_25DAA8D1EEDA45A0B5B59472BD8896C4">Deel aan uw gebruikersbasis mee dat hun login ervaring zal veranderen wanneer de migratie begint. </li> 
     <li id="li_5B50F942F6A8483FAFA500AFF428702C">Audit uw huidige gebruikers en toestemmingen en voer schoonmaakactiviteiten uit. </li> 
    </ul> <p>Als u uw migratie wilt versnellen, neemt u contact op met het accountteam van de Adobe op de <a href="https://helpx.adobe.com/nl/marketing-cloud/contact-support.html"> klantenservice van de Adobe </a> en dient u een aanvraag voor een eerdere begindatum in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Ik ben een beheerder van Analytics zonder toegang tot de Adobe Admin Console. Wie kan mij helpen toegang te krijgen tot de Adobe Admin Console? </p> </td> 
   <td colname="col2"> <p>Elke systeem- of productbeheerder die toegang heeft tot de Adobe Admin Console van uw organisatie, kan u toegang geven. Als u niet zeker bent wie binnen uw organisatie beheerdervoorrechten in de console heeft, contacteer de <a href="https://helpx.adobe.com/nl/marketing-cloud/contact-support.html"> Zorg van de Klant van de Adobe </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kan ik de startdatum van de migratie uitstellen? </p> </td> 
   <td colname="col2"> <p>Ja. Neem contact op met de <a href="https://helpx.adobe.com/nl/marketing-cloud/contact-support.html"> klantenservice van de Adobe </a> . </p><p>Zie hieronder voor een beschrijving van de wijzigingen in uw huidige gebruikers- en machtigingenbeheer voor Analytics op de startdatum. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Nu mijn bedrijf naar de Adobe Admin Console migreert, waar maak ik nieuwe gebruikers en machtigingengroepen voor de begindatum van de migratie? </p> </td> 
   <td colname="col2"> <p>Voordat u de migratie start, kunt u gebruikers maken in de Adobe Admin Console of in Analytics &gt; User Management (Analyse &gt; Gebruikersbeheer). </p> <p>Nadat de migratie is begonnen, kunt u alleen gebruikers en machtigingsgroepen maken in de Adobe Admin Console. </p><p>Zie de sectie Migratie hieronder voor meer informatie over wat er gebeurt op de startdatum van de migratie. </p>
   </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Wanneer kan ik enig teken-op uitvoeren gebruikend Federated IDs? </p> </td> 
   <td colname="col2"> <p> In de Adobe Admin Console is binnenkort een hulpprogramma beschikbaar waarmee u id-typen kunt wijzigen van Adobe-id's in federatieve id's. Tijdens de migratie kunt u gebruikers niet migreren als gefedereerde id's. </p> </td> 
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
   <td colname="col1"> <p>Hoe worden machtigingsgroepen gerepliceerd naar de Adobe Admin Console? Hoe zit het met mijn gebruikers? </p> </td> 
   <td colname="col2"> <p>Een gemigreerde groep van Analytics is a genoemd het Profiel van het a <i> Product </i> in Adobe Admin Console. Machtigingsinstellingen voor de oorspronkelijke groep blijven behouden in de migratie. De gebruikers die aan de groep zijn toegewezen, worden echter niet gemigreerd. Wanneer een gebruiker die tot die groep behoort met het migratiehulpmiddel wordt gemigreerd, wordt die gebruiker toegewezen aan dat productprofiel. </p> <p>Bijvoorbeeld, zal een de toestemmingsgroep van de Verrichtingen van het Westen die zijn leden aan Report Builder en Analysis Workspace (met bepaalde rapportsuites, metriek, dimensies) machtigde een het productprofiel van de Verrichtingen van het Westen worden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kan ik de migratieinspanning aan een andere beheerder delegeren? </p> </td> 
   <td colname="col2"> <p>Zodra uw migratie begint, kan om het even welke beheerder die tot uw instantie Analytics via het Experience Cloud toegang heeft het migratiehulpmiddel gebruiken beginnen (of verdergaan) migrerende gebruikers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kan ik het lidmaatschap van machtigingengroepen bijwerken voor niet-gemigreerde gebruikers? </p> </td> 
   <td colname="col2"> <p>Ja. U kunt het groepslidmaatschap van niet-gemigreerde gebruikers wijzigen vanuit de sectie Gebruikersbeheer voor Analytics. </p><p>In afwachting van een verduidelijking van Ashok over waar dat gebeurt. </p>
   </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kan ik gebruikers en machtigingsgroepen maken in Analytics nadat mijn migratie is begonnen en deze vervolgens met het migratiehulpprogramma naar de Adobe Admin Console verplaatsen? </p> </td> 
   <td colname="col2"> <p> Nee. Zodra de migratie begint, moeten alle nieuwe gebruikers en toestemmingsgroepen (genoemd Profielen van het Product in de Adobe Admin Console) in Adobe Admin Console worden gecreeerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zouden gebruikers die ik met het migratiehulpmiddel migreer de zelfde toestemmingen worden toegewezen die zij in Analytics hadden? </p> </td> 
   <td colname="col2"> <p>Ja. Gebruikers die met dit gereedschap zijn gemigreerd, krijgen de machtigingen die ze momenteel in Analytics hebben. Bovendien zullen zij toegang tot hun activa van Analytics (zoals segmenten, projecten, berekende metriek, etc.) behouden wanneer zij tot Analytics via het Experience Cloud toegang hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hebben gebruikers die ik naar de Adobe Admin Console migreer toegang tot Analytics gebruikend <span class="filepath"> my.omniture.com </span> nog steeds? </p> </td> 
   <td colname="col2"> <p>Ja. Gemigreerde gebruikers zullen tot de einddatum van de migratie toegang tot Analytics kunnen blijven gebruikend hun bestaand gebruikersnaam en wachtwoord via <span class="filepath"> my.omniture.com </span>, tenzij u hun erfenislogin toegang via het migratiehulpmiddel onbruikbaar maakt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Twee of meer van mijn gebruikers hebben dezelfde e-mailid in hun analysebestand. Wat gebeurt er als ik ze migreer? </p> </td> 
   <td colname="col2"> <p>Omdat gebruikersaccounts in de Adobe Admin Console unieke e-mailadressen nodig hebben, wordt een fout met de naam 'E-mailadres dupliceren' weergegeven wanneer u meerdere van deze gebruikers probeert te migreren. U kunt de e-mailadressen van niet-gemigreerde gebruikers bijwerken in de sectie Gebruikersbeheer (verouderd) voordat u de migratie opnieuw uitvoert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Wat doe ik na het migreren van mijn gebruikers? </p> </td> 
   <td colname="col2"> <p>Schakel hun oudere aanmeldingstoegang tot <span class="filepath"> my.omniture.com </span> uit. U kunt de aanmeldingsgegevens voor oudere versies alleen uitschakelen als deze zijn gemigreerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kan ik het migratieproces volgen? </p> </td> 
   <td colname="col2"> <p>Het migratiehulpmiddel omvat een dashboard dat toont hoeveel van uw gebruikers met succes zijn gemigreerd, en hoeveel van hen hun erfenislogin gehandicapt hebben. </p> <p> In het ideale geval hebt u uw aanmeldingsbedrijf naar de Adobe Admin Console gemigreerd wanneer een 100% van uw gebruikers de migratie heeft voltooid en hun oudere aanmeldingspogingen heeft uitgeschakeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tijdens de migratie moet ik gebruikers- en machtigingsbeheer uitvoeren. Met welk gereedschap kan ik deze taak uitvoeren? </p> </td> 
   <td colname="col2"> <p>Nadat de migratie is begonnen, gebruikt u de Adobe Admin Console om nieuwe gebruikers en productprofielen te maken en te beheren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wat ervaren mijn gebruikers wanneer ik hen gebruikend het hulpmiddel migreer? </p> </td> 
   <td colname="col2"> <p>Ze zullen een welkomstbericht ontvangen dat is geadresseerd aan de e-mailadres in hun Analytics-gebruikersrecord en waarin ze via het Experience Cloud op de hoogte worden gesteld van hun nieuwe manier om toegang te krijgen tot Analytics. Als ze geen bestaande Adobe ID hebben, wordt hun gevraagd om er een te maken, waarna ze via hun Adobe ID toegang tot de oplossing kunnen krijgen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kan ik API's gebruiken om mijn gebruikers te migreren in plaats van het migratiehulpmiddel te gebruiken? </p> </td> 
   <td colname="col2"> <p>Nee. U moet het migratiehulpprogramma gebruiken om ervoor te zorgen dat al uw bestaande gebruikers naar de Adobe Admin Console worden gemigreerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Welke analysefuncties voor gebruikersbeheer zijn niet beschikbaar in de Adobe Admin Console? </p> </td> 
   <td colname="col2"> 
    <ul id="ul_3F3747D4C1D3420699F7D28EC0CA1AA0"> 
     <li id="li_BD943B3245FF47E7A0DDA6107EA1EF89">Middelen overdragen </li> 
     <li id="li_2DF7004D67ED4C6CB40461EEFB038A5A">Vervaldatum gebruiker </li> 
     <li id="li_980E3F5B98F344A492B0EBAD7F1DA60C">Gebruikerslogboeken </li> 
    </ul> <p>Deze blijven beschikbaar in Analytics-gebruikersbeheer. </p> <p>Zie <a href="/help/admin/admin/user-management2/user-migration/c-migration-tool.md"> Niet-ondersteunde analysefuncties in de Adobe Admin Console </a> voor meer informatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>We hebben verschillende configuraties gemaakt in de Adobe Admin Console en ze toegewezen aan machtigingsgroepen Analytics. Wat zal met die configuraties gebeuren wanneer de migratie begint? </p> </td> 
   <td colname="col2"> <p>In de Adobe Admin Console worden machtigingsgroepen voor Analytics opnieuw gemaakt als productprofielen, net als in alle andere groepen. Dit betekent u twee productprofielen in de console zult zien die hoofdzakelijk dubbele toestemmingen hebben. U kunt dubbele productprofielen verwijderen uit de Adobe Admin Console. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wat is mijn volgende stap na het migreren van gebruiker? </p> </td> 
   <td colname="col2"> <p>Zodra u de gebruiker of een reeks gebruikers hebt gemigreerd, is uw volgende stap hun erfenislogin via <span class="filepath"> my.omniture.com onbruikbaar te maken </span>. U kunt dit doen door deze gebruikers te selecteren in het migratiehulpmiddel en op de contextafhankelijke optie "Oudere aanmelding uitschakelen" te klikken die boven aan het scherm wordt weergegeven. Deze optie is alleen zichtbaar wanneer u een gebruiker of een set gebruikers selecteert die allemaal naar de Adobe Admin Console zijn gemigreerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wat gebeurt er op de einddatum van de migratie? </p> </td> 
   <td colname="col2"> <p>Na de einddatum van de migratie (60 dagen vanaf het begin van de migratie) worden alle gebruikers binnen uw aanmeldingsbedrijf omgeleid naar aanmelding via de aanmeldingspagina van het Experience Cloud met hun Adobe-id's. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ik heb niet al mijn gebruikers tegen de migratie-einddatum kunnen migreren. Zouden niet-gemigreerde gebruikers hun toegang tot Analytics verliezen? </p> </td> 
   <td colname="col2"> <p>Gebruikers die op de einddatum niet zijn gemigreerd, worden omgeleid naar de aanmeldingspagina voor het Experience Cloud (experiencecloud.adobe.com) en hebben geen toegang tot Analytics. U blijft echter wel toegang hebben tot het migratiehulpprogramma, zodat u deze kunt zoeken en migreren om de toegang te herstellen. </p> </td> 
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
   <td colname="col1"> <p>Gebruikers verwijderen uit de Adobe Admin Console </p> </td> 
   <td colname="col2"> <p> In Analytics, wordt een geschrapte gebruiker geplaatst aangezien <span class="term"> verlopen </span>, maar de rekening blijft bestaan. Het behouden van de rekening laat de overdragende activa, zoals segmenten, berekende metriek, geplande rapporten, projecten, etc. toe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verlopen van accounts </p> </td> 
   <td colname="col2"> <p> U kunt handmatig een vervaldatum van een account instellen in Analytics in Admin Tools. Zodra aan de vervaldatum wordt voldaan, zal de gebruiker tot Analytics niet kunnen toegang hebben, maar hun daadwerkelijke gebruikersrekening van het Experience Cloud (b.v. Adobe ID, Enterprise ID, Federated ID, enz.) verloopt niet. Ze kunnen zich nog steeds aanmelden bij Experience Cloud, ze kunnen alleen niet in Analytics klikken. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Niet-ondersteunde analysefuncties in de Adobe Admin Console {#section-928ffba27a0446e0af575b720434ef56}

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
   <td colname="col2"> <p> Beheerders die naar de Adobe Admin Console migreren, kunnen de functie Aanmelden als niet-beheerdersaccounts die naar de Adobe Admin Console zijn gemigreerd, niet meer gebruiken. Deze functie is uitgeschakeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vervaldatum gebruiker en overdracht van middelen </p> </td> 
   <td colname="col2"> <p> De Adobe Admin Console biedt geen ondersteuning voor het verlopen van gebruikers of het overdragen van middelen. Beheerders gebruiken de sectie Analytics Users en Assets onder Admin Tools in Analytics voor beide functies. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Laatste toegang (laatste aanmelding) </p> </td> 
   <td colname="col2"> <p> Details over de laatste aanmeldingsdatum en -tijd van een gebruiker zijn beschikbaar via de koppeling Analytics Users en Assets en niet via de Adobe Admin Console. De laatste-login datum in Analytics is specifiek voor wanneer de gebruikers werkelijk Analytics van binnen Experience Cloud betreden en wijst niet op de datum/de tijd toen zij in het Experience Cloud registreerden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gebruikersbeheer-API's <a href="https://helpx.adobe.com/nl/enterprise/help/identity.html"> Door Adobe ondersteunde identiteitstypen </a> </p> </td> 
   <td colname="col2"> <p> Beheerders die naar de Adobe Admin Console migreren, moeten API's voor gebruikersbeheer configureren die op Adobe Developer worden aangeboden voor programmatische toegang tot gebruikersaccounts in de Adobe Admin Console. </p> <p>De API's voor analysebevoegdheden worden uitgeschakeld wanneer u de migratie wilt inschakelen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Webservicereferenties </p> </td> 
   <td colname="col2"> <p> De referenties van de webservice van gebruikers (en hun gedeelde geheim) zijn niet beschikbaar in de Adobe Admin Console en kunnen worden geopend door in de sectie Analytics Users and Assets op de specifieke gebruiker te klikken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Single Sign-On </p> </td> 
   <td colname="col2"> <p> Configuraties met eenmalige aanmelding voor analysemogelijkheden worden verwijderd wanneer u de migratie hebt voltooid. Ze zullen actief blijven tijdens de migratie. Klanten die de enige teken-op van de Analyse gebruiken zouden aan <a href="https://helpx.adobe.com/nl/enterprise/help/identity.html"> Federated ID van de Adobe </a> moeten bevorderen. </p> <p>Analytics raadt u aan om uw gebruikers als Adobe-id's eerst te migreren om eenvoudig de Experience Cloud-accounts te maken en deze vervolgens om te zetten in gefedereerde single-sign gebruikers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Machtigingsgroepen downloaden </p> </td> 
   <td colname="col2"> <p> Het downloaden van gegevens voor machtigingsgroepen wordt niet meer ondersteund in de hulpprogramma's voor Analysebeheer of de Adobe Admin Console. Klanten moeten de API's voor gebruikersbeheer van adobe.io gebruiken om informatie over machtigingengroepen bulksgewijs op te halen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aanmaakdatum account </p> </td> 
   <td colname="col2"> <p>Gegevens over aanmaakdatum van account worden niet meer ondersteund in de hulpprogramma's van Analytics Admin of de Adobe Admin Console. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bulkmail </p> </td> 
   <td colname="col2"> <p>Bulk-e-mailberichten aan gebruikers worden niet meer ondersteund in de hulpprogramma's voor analysebeheer of in de Adobe Admin Console. Klanten kunnen hun e-mailadressen van hun gebruikers bulksgewijs vanuit Adobe Admin Console exporteren en een e-mailbericht verzenden met elke gewenste e-mailclient. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Uw gebruikers op de hoogte stellen van de migratie {#section-f3b25f672a3a4d03b0559656fd99d20a}

U kunt dit migratieplan proactief aan uw huidige gebruikers willen meedelen. Hier volgt een sjabloon die u kunt aanpassen om al uw huidige gebruikers van Analytics te verzenden:

Om alle gebruikers te e-mailen, navigeer aan **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL All admin]** > **[!UICONTROL User management]** > [ E-mailgebruikers ](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/t-email-users.html?lang=nl-NL).

**Onderwerp:** Binnenkort - een nieuwe manier aan login aan Adobe Analytics en Adobe Experience Cloud.

**Lichaam:** de gebruikers van Hello Adobe Analytics!

Ons bedrijf zal beginnen migrerend alle rekeningen van Adobe Analytics vanaf [!DNL https://my.omniture.com/login/] aan Adobe Experience Cloud ([ experience.adobe.com ](https://experiencecloud.adobe.com/)). Met deze migratie wordt uw Adobe Analytics-account geüpgraded om toegang tot Analytics via de Adobe Experience Cloud mogelijk te maken. Terwijl de methode om tot Analytics toegang te hebben zal veranderen, zullen al uw bestaande toestemmingen aan uw rapportsuites en hulpmiddelen worden bewaard.

**Volgende stappen:** wij zullen beginnen om gebruikers te migreren die op **DATUM VAN HET TUSSENVOEGSEL** beginnen. Kijk naar een welkomstbericht met uw nieuwe aanmelding die is gericht aan de e-mailadres dat wordt vermeld onder uw analyseaccount. Als u geen opstelling een [ Adobe ID ](https://helpx.adobe.com/nl/x-productkb/global/adobe-id-account-change.html) verbonden aan uw e-mailadres hebt, zult u worden gevraagd om een rekening te vestigen.

**Nuttige middelen:**

[ Teken binnen en beheer uw profielmontages ](https://helpx.adobe.com/nl/enterprise/admin-guide.html/enterprise/using/manage-products.ug.html).

Neem contact op met uw analysebeheerders als u vragen of problemen hebt.

Best

Analysebeheer
