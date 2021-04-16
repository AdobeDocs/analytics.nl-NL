---
description: Implementeer Adobe Analytics met Dynamisch tagbeheer door het Adobe Analytics-gereedschap te maken en de paginacode automatisch of handmatig te configureren. De automatische methode wordt aanbevolen voor de meeste gebruikers.
keywords: Analyse - implementatie;implementatiemethode;dynamisch tagbeheer;dtm;analyseprogramma;eigenschap;gereedschapstype;naam van gereedschap;configuratiemethode;analytische premie;gebeurtenissen;gebeurtenissen
title: Adobe Analytics-tool toevoegen
topic-fix: Developer and implementation
uuid: 1c54331e-de03-4f44-8002-a19723c585b0
exl-id: 3f5e13f6-19d1-46b9-9011-6010b455007e
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 8%

---

# Adobe Analytics-tool toevoegen

Implementeer Adobe Analytics met Dynamisch tagbeheer door het Adobe Analytics-gereedschap te maken en de paginacode automatisch of handmatig te configureren. De automatische methode wordt aanbevolen voor de meeste gebruikers.

>[!NOTE]
>
>Voor betere bezoekerscontrole, adviseren wij sterk dat u [Identiteitsdienst ](https://docs.adobe.com/content/help/nl-NL/id-service/using/home.html) toelaat.

## Een Adobe Analytics-gereedschap toevoegen {#section_D5066B21581B4F7F811AD0027BF44EA5}

1. Klik op  **[!UICONTROL  *`Web Property Name`*]** > **[!UICONTROL Overview]** > **[!UICONTROL Add a Tool]** > **[!UICONTROL Adobe Analytics]** .

   ![](assets/dtm-add-analytics-tool.png)

1. Vul de velden in:

<table id="table_1CFB53FE72E74CCB8CAA5D4E3873D286"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Gereedschapstype </p> </td> 
   <td colname="col2">Het type gereedschap, zoals <span class="keyword"> Adobe Analytics</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Naam gereedschap </p> </td> 
   <td colname="col2">Een beschrijvende naam voor dit gereedschap. Deze naam wordt weergegeven op het tabblad <span class="wintitle"> Overzicht</span> onder <span class="wintitle"> Geïnstalleerde gereedschappen</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="1"> <p>Configuratiemethode </p> </td> 
   <td colname="col2"> <p> <b>Automatisch</b>  (aanbevolen): Gebruik dynamisch tagbeheer om de configuratie te beheren. Deze methode laat automatische synchronisatie van <span class="keyword"> Adobe Analytics</span> rapportreeksen via een <span class="keyword"> Experience Cloud </span> login of identiteitskaart van de Diensten van het Web toe, en beheert de code AppMeasurement. </p> <p>Nadat de accounts zijn verbonden, haalt Dynamic Tag Management de <span class="keyword"> Adobe Analytics</span>-rapportenreeks-id's en -namen naar de interface voor gereedschapsconfiguratie, waardoor de implementatie van tools sneller verloopt en gebruikersfouten minder mogelijk zijn. </p> <p> <p>Opmerking: U moet de optie <span class="wintitle"> Automatisch</span> kiezen als u een <span class="keyword"> Adobe Analytics Premium</span> klant bent. </p> </p> <p>Vul de gebieden in specifiek voor automatische configuratie: </p> 
    <ul id="ul_8D9797B01E444B9C85B862A9F96B447C"> 
     <li id="li_0AC84C1F37B24C658F2178E50ECCC4B0"> <p> <b>Experience Cloud</b>: (Standaard) Maakt gebruik van  <span class="keyword"> Experience </span> Cloudsingle-aanmelding. Geef uw Experience Cloud-id en wachtwoord op. </p> </li> 
     <li id="li_6C80468835D04CC09F4AEC46D1300310"> <p><b>Webservices</b>: Specificeer uw gebruikersbenaming van de Diensten van het Web en gedeeld geheim. </p> <p>De gedeelde geheime geloofsbrieven worden gevestigd in <span class="uicontrol"> Admin </span> &gt; <span class="uicontrol"> Bedrijfsinstellingen</span> &gt; <a href="https://docs.adobe.com/content/help/en/analytics/admin/company-settings/web-services-admin.html"> Webservices</a>. </p> <p>Ontwikkelaars, zie <a href="https://marketing.adobe.com/developer/en_US/get-started/enterprise-api/c-get-web-service-access-to-the-enterprise-api"> de Toegang van de Dienst van het Web tot de Onderneming API</a> voor hulp met het verkrijgen van de geloofsbrieven van de Diensten van het Web krijgen. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <b>Handmatig</b>: Beheer manueel de code AppMeasurement. U kunt de <span class="keyword"> Analytics</span><span class="keyword"> AppMeasurement</span> code van &lt;a4 downloaden/&gt;<span class="uicontrol"> Admin Tools</span> &gt; <span class="uicontrol"> Code Manager</span></span>.<span class="ignoretag"> </span></p> <p>Klik <a href="https://docs.adobe.com/content/help/en/analytics/implementation/js/migrate-from-hcode.html"> JavaScript (nieuw)</a> voor informatie over het downloaden van de code plaatselijk om code te kopiëren en te kleven in <span class="wintitle"> uitgeef Code</span> gebied in <a href="/help/implement/other/dtm/c-aa-tool/library-management.md"> Bibliotheekbeheer</a>. </p> <p>Vul de gebieden in specifiek voor een handconfiguratie: </p> 
    <ul id="ul_CFB6CE78AEB743EF8B47BAAC42E2DB0A"> 
     <li id="li_5B7046CD95AB416F8C113B381A264D91"> <p><b>Productieaccount-id:  </b>(Vereist) Uw productieaccount voor gegevensverzameling. Voor Analytics is dit uw rapportsuite-id. Met Dynamic Tag Management wordt automatisch het juiste account geïnstalleerd in de productie- en staging omgeving. </p> </li> 
     <li id="li_14E840FD79A0451BABEDD15DC0584768"> <p><b>Staging account-id:  </b>(Vereist) Wordt gebruikt in uw ontwikkelings- of testomgeving. Voor Analytics is dit uw rapportsuite-id. Een staging account houdt uw testdata gescheiden van de productie. </p> </li> 
     <li id="li_69E6C6A41F5240E1ABE8ABE0B9D151FC"> <p><b>Trackingserver:  </b>Geef de gegevens voor uw trackingserver op. </p> <p>De variabelen <span class="wintitle"> Tracking Server</span> en <span class="wintitle"> SSL Tracking Server</span> worden gebruikt voor de implementatie van cookies van de eerste partij om het domein te specificeren waarop het beeldverzoek en het koekje worden geschreven. Voor meer informatie, zie <a href="https://helpx.adobe.com/analytics/kb/determining-data-center.html"> correct bevolken trackingServer en trackingServerSecure Variable</a> artikel. </p> </li> 
     <li id="li_1A7271C68205428F8CA5548A96CACBEC"> <p><b>SSL-traceringsserver:  </b>Geef de gegevens voor uw SSL-tracking-server op. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

1. Klik **[!UICONTROL Create Tool]** om het hulpmiddel tot stand te brengen en het voor het uitgeven te tonen.

   De hulpmiddelen worden getoond op [!UICONTROL Overview] tabel, onder [!UICONTROL Installed Tools].

1. (Voorwaardelijk) Vorm het hulpmiddel verder zonodig door de richtingen in de hieronder verbindingen ( [!UICONTROL General], [!UICONTROL Library Management], [!UICONTROL Global Variables], [!UICONTROL Pageviews & Content], [!UICONTROL Link Tracking], [!UICONTROL Referrers & Campaigns], [!UICONTROL Cookies], en [!UICONTROL Customize Page Code]) te volgen.

Zie [Veelgestelde vragen over het gereedschap Adobe Analytics](/help/implement/faq.md) voor meer informatie over dit gereedschap.

## Een bestaand Adobe Analytics-gereedschap bewerken {#section_148B16AF429B4949B06238D90635B726}

U kunt een bestaand Adobe Analytics-gereedschap bewerken om de configuratie-instellingen te wijzigen.

1. Klik op het pictogram ![](assets/settings_gear.png) naast een geïnstalleerd gereedschap op het tabblad [!UICONTROL Overview].
1. Bewerk de velden naar wens.

   De volgende tabel bevat alleen de elementen die afwijken van de elementen die beschikbaar zijn wanneer u een analyseprogramma maakt, zoals hierboven beschreven. U kunt echter elk element op de pagina wijzigen, zoals in beide tabellen wordt beschreven.

<table id="table_2B60CD109CFF4839AB7F91D61125EDFF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Automatische configuratie inschakelen </p> </td> 
   <td colname="col2"> <p>Opmerking: Als u deze instelling inschakelt, wordt een handmatig geconfigureerde implementatie gewijzigd in de automatische configuratiemethode die wordt beschreven in <span class="term"> Configuration Method</span>. </p> <p>Met deze optie kan Dynamic Tag Management automatisch de configuratie van uw <span class="keyword"> Adobe Analytics</span>-account ophalen. </p> <p>De meest recente beschikbare code voor AppMeasurement wordt gebruikt en de verbeteringsberichten worden getoond voor selectie aangezien de nieuwe versies beschikbaar worden. U kunt ook zo nodig terugdraaien naar vorige AppMeasurement-versies, bijvoorbeeld om compatibiliteitsredenen. Er worden maximaal vijf vorige versies weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Referenties bijwerken </p> </td> 
   <td colname="col2"> <p>Vernieuw bijvoorbeeld de API om rapportsuites bij te werken die aan een gebruiker zijn gekoppeld. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. (Voorwaardelijk) Vorm het hulpmiddel verder zonodig door de richtingen in de hieronder verbindingen ( [!UICONTROL General], [!UICONTROL Library Management], [!UICONTROL Global Variables], [!UICONTROL Pageviews & Content], [!UICONTROL Link Tracking], [!UICONTROL Referrers & Campaigns], [!UICONTROL Cookies], en [!UICONTROL Customize Page Code]) te volgen.
1. Klik op **[!UICONTROL Save Changes]**.
