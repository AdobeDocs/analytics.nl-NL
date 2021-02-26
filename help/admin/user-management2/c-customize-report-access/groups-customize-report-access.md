---
description: U kunt groepsmachtigingen aanpassen aan Analytics-programma's, rapportsuite-gereedschappen, meetgegevens en dimensies.
keywords: groepen;machtigingen
subtopic: Users and groups
title: Rapporttoegang aanpassen - overzicht
topic: Beheerprogramma's
uuid: 818a7196-8b43-4654-8d5f-800b3122aad3
translation-type: tm+mt
source-git-commit: d0fe97b9368cbc4c9e79f9e56adf9786b58dce1a
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 4%

---


# Rapporttoegang aanpassen - overzicht

>[!IMPORTANT]
>
>Gebruiker- en productbeheer is verplaatst naar de [Admin Console](https://helpx.adobe.com/nl/enterprise/using/admin-console.html). Nadat alle klanten zijn gemigreerd, wordt de Help-inhoud voor **[!UICONTROL Analytics]** > **[!UICONTROL Admin Tools]** > **[!UICONTROL User Management]** ingetrokken.

U kunt groepsmachtigingen aanpassen aan Analytics-programma&#39;s, rapportsuite-gereedschappen, meetgegevens en dimensies.

**[!UICONTROL Add New Group]** > **[!UICONTROL Report Access]**

De sectie [!UICONTROL Report Access] op de pagina [!UICONTROL Define User Group] verstrekt toegangscategorieën die u toelaten om toestemmingen op korrelniveau aan te passen.

![](assets/report-access.png)

U kunt bijvoorbeeld een groep maken met toegang tot meerdere analyseprogramma&#39;s ( [!UICONTROL Analysis Workspace], [!UICONTROL Reports & Analytics] en [!UICONTROL Report Builder]), met toestemming voor specifieke metriek en dimensies (inclusief eVars) en mogelijkheden zoals het maken van segmenten of berekende metriek.

## Wat u moet weten over machtigingen {#section_3D25D4A5BD044008870C5B98F696244E}

<table id="table_DB7806E05E2040EC9A4CB7C3596879EC"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Item </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Beheerderstoegang / vooraf gedefinieerde groepen </p> </td> 
   <td colname="col2"> <p> Voor beheerders zijn vooraf gedefinieerde groepen niet meer vereist. De beheerders hebben nu toegang tot alle punten (hulpmiddelen, metriek, dimensies), evenals de toegang van de Dienst van het Web, Report Builder, en Activity Map. </p> <p>Groepen hebben tot doel niet-administratieve gebruikers toegang te verlenen of te beperken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aangepaste groepen </p> </td> 
   <td colname="col2"> <p> Aangepaste groepen hebben vooraf gedefinieerde groepen vervangen. Bestaande, vooraf gedefinieerde groepen worden gemigreerd naar aangepaste groepen met dezelfde groepsnaam. Alle aangepaste groepen die u hebt gemaakt, inclusief de instellingen, blijven behouden. U zult echter zien dat de locatie van de instellingen is verplaatst. Bijvoorbeeld, zijn de montages van het Bedrijf (in Aanpassen Admin Console) nu in <a href="/help/admin/user-management2/c-customize-report-access/groups-analytics-tools.md"> Customize Analytics Tools</a>. </p> <p> De gebruikers die tot <span class="term"> Al Toegang van het Rapport</span> behoren zijn gemigreerd aan een douanegroep met toegang tot: </p> 
    <ul id="ul_7E1B443DEEF7452E85FEB30CA0BBC8BE"> 
     <li id="li_A510C2A4129340E0AB08EEBDBE4AEAD9">Alle Dimension </li> 
     <li id="li_8BA1D7A2527C4F10AC93108B9E87F418">Alle metriek </li> 
     <li id="li_265830A2C6B94AF28720DA99980EAA51">Alle rapportsets </li> 
     <li id="li_685B99DEAB814D7B9C11B14AA4CB8CD4">Kanaalrapport </li> 
     <li id="li_B35420302AAB42509BD6AF0FA6349BF8">Anomaliedetectie </li> 
     <li id="li_3787E4696C454D3ABD1D75F6C282A9A2">Rapport in realtime </li> 
     <li id="li_3797DF9C40D1426588819116362962F5">Analysis Workspace Access </li> 
    </ul> <p>Beheerders kunnen aangepaste groepen verwijderen en hun eigen groepen maken, aangezien alle instellingen die voorheen beschikbaar waren in vooraf gedefinieerde groepen, beschikbaar zijn voor aanpassing onder de instellingen <span class="wintitle"> Rapporttoegang</span> in Gebruikersgroepen definiëren.</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Machtigingen op Dimension-niveau </p> </td> 
   <td colname="col2"> <p>U kunt machtigingen aanpassen om toegang tot afmetingen op te nemen of uit te sluiten (naast metriek). </p> 
    <ul id="ul_DA5A54223673474E9151AF979DA50659"> 
     <li id="li_C3E82F7BC07A4F2F83A85D3D511292CC"> <p>Alle huidige afmetingen en metriek binnen aangepaste groepen zijn automatisch gemigreerd naar de nieuwe categorieën. Als metriek is ingeschakeld voor een bestaande groep, krijgt deze standaard alle nieuw toegestane afmetingen (eVars en inhoud behouden) en maatstaven. </p> </li> 
     <li id="li_CC56F9181CC14AB59318628E72F2E8C9"> Indelingsrechten (voorheen, SAINT): De toegang tot classificaties wordt bepaald door toegang tot <a href="https://docs.adobe.com/content/help/en/analytics/components/classifications/c-classifications.html"> variabele</a> waarop de classificatie is gebaseerd. </li> 
    </ul> <p>Zie <a href="/help/admin/user-management2/c-customize-report-access/groups-dimensions.md"> Dimension-machtigingen aanpassen</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="https://helpx.adobe.com/enterprise/using/admin-console.html"> Adobe Admin Console</a> </p> </td> 
   <td colname="col2"> <p>Wordt alleen aanbevolen voor nieuwe klanten of klanten met bedrijven <a href="https://docs.adobe.com/content/help/en/core-services/interface/about-core-services/core-services.html"> die zijn ingericht in de Experience Cloud</a>. Er is een migratie gepland voor bestaande <span class="keyword"> Analytics</span>-klanten naar het <span class="keyword"> Experience Cloud</span>-identiteitsbeheersysteem. </p> <p>Meer informatie is beschikbaar in <a href="https://docs.adobe.com/content/help/en/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html"> de Migratie van de Gebruiker van de Analyse aan de Admin Console</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Inhoud behouden </p> </td> 
   <td colname="col2"> <p>Met behoud van inhoud worden ook variabelen opgenomen waarmee u de machtigingen voor metriek voor integratie van Experience Cloud-oplossingen kunt beheren. U kunt toestemmingen op <span class="keyword"> Sociale </span>, <span class="keyword"> Mobiele </span>, of om het even welke andere gegevens beheren die door een <span class="keyword"> integratie van Experience Cloud</span> werden opgenomen. Deze worden standaard ingeschakeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Machtigingen/rapporten definiëren </p> </td> 
   <td colname="col2"> <p>Deze mislukte rapporten worden verwijderd: </p> 
    <ul id="ul_C0415CFF0562472297272EC58ECC0774"> 
     <li id="li_62B1CE33B1454987B878B321EB40D62E">Maandelijks overzicht </li> 
     <li id="li_71CD776D212540A18F9B083D2E11A296">Homepage van bezoeker </li> 
     <li id="li_406200AD68C74D11B5F53988A4E76A68">Netscape-plug-ins </li> 
     <li id="li_A124637D69C94C78921C8B028D890541">Belangrijke bezoekers </li> 
     <li id="li_5C26FF95371B4F3080FF75C7F8DE0F72">Pagina's weergegeven door belangrijke bezoekers </li> 
     <li id="li_E7E262BD0CF64E16B838F995F6A13B8A">Opname bezoeker </li> 
     <li id="li_0EDC74625C0D4B1A992FCA49B648E4C0">DRM </li> 
     <li id="li_ACC92E6EA188409486E7C943F26B9DAC">Netprotocollen </li> 
     <li id="li_6E18C4D12377416A8124BBD13164B03A">Java-versie </li> 
     <li id="li_1599265E59EF4F34BB406356410C9E68">Lengte bladwijzer-URL </li> 
     <li id="li_3035442010984C409089B21E03DB7BCC">Apparaatnummer verzenden </li> 
     <li id="li_6B2163ED8FC84EBF933D97A504B4D527">PTT </li> 
     <li id="li_0EB8A4A7619B45DF87109B183A7C69C8">Ondersteuning voor Decoration Mail </li> 
     <li id="li_989FAC662F7344E6BDDC517B79D4581E">Informatie </li> 
     <li id="li_F1FB7F8E415443F3B63F6D11D59A04AB">Informatiedienst </li> 
    </ul> <p>Deze rapporten: </p> 
    <ul id="ul_F71505C59F734EA9B541BF8AB9F9388F"> 
     <li id="li_7D461907B895447280E69CF1520DF47C">Kan nog steeds worden benaderd door bladwijzers. </li> 
     <li id="li_27BA2DD6BA4C446FBAA06B6C76CD171F">Deze worden niet opgenomen in de machtigingencategorie voor nieuwe Dimension. </li> 
     <li id="li_504E9D8421714406A0F37DEF1E10E34B">Kan de machtigingen niet meer bewerken. </li> 
     <li id="li_0022E8DCA07344C793847E8282EFBEEF">Hiermee behoudt u toegang voor aangepaste groepen met huidige toegang. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

