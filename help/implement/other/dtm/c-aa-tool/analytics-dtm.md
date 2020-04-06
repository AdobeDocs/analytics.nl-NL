---
description: Implementeer Adobe Analytics met Dynamisch tagbeheer door het hulpprogramma Adobe Analytics te maken en de paginacode automatisch of handmatig te configureren. De automatische methode wordt aanbevolen voor de meeste gebruikers.
keywords: Analytics Implementation;implementation method;dynamic tag management;dtm;analytics tool;property;tool type;tool name;configuration method;analytics premium;evars;events
title: Gereedschap Adobe Analytics toevoegen
topic: Developer and implementation
uuid: 1c54331e-de03-4f44-8002-a19723c585b0
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Gereedschap Adobe Analytics toevoegen

Implementeer Adobe Analytics met Dynamisch tagbeheer door het hulpprogramma Adobe Analytics te maken en de paginacode automatisch of handmatig te configureren. De automatische methode wordt aanbevolen voor de meeste gebruikers.

>[!NOTE] Voor betere bezoekerscontrole, adviseren wij sterk dat u de Dienst [van de](https://marketing.adobe.com/resources/help/en_US/mcvid/)Identiteit toelaat.

## Add an Adobe Analytics Tool {#section_D5066B21581B4F7F811AD0027BF44EA5}

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
   <td colname="col2"> <p> <b>Automatisch</b> (aanbevolen): Gebruik dynamisch tagbeheer om de configuratie te beheren. Met deze methode wordt automatische synchronisatie van <span class="keyword"> Adobe Analytics</span> -rapportreeksen ingeschakeld via een aanmeldingsnaam voor de <span class="keyword"> Experience Cloud</span> of Web Services-id, en wordt de AppMeasurement-code beheerd. </p> <p>Nadat de accounts zijn verbonden, haalt Dynamic Tag Management de <span class="keyword"> Adobe Analytics</span> -rapportensuite-id's en -namen naar de interface van de gereedschapsconfiguratie, waardoor de implementatie van hulpprogramma's sneller verloopt en de kans op gebruikersfouten kleiner is. </p> <p> <p>Opmerking: U moet de optie <span class="wintitle"> Automatisch</span> kiezen als u een <span class="keyword"> Adobe Analytics Premium</span> -klant bent. </p> </p> <p>Vul de gebieden in specifiek voor automatische configuratie: </p> 
    <ul id="ul_8D9797B01E444B9C85B862A9F96B447C"> 
     <li id="li_0AC84C1F37B24C658F2178E50ECCC4B0"> <p> <b>Experience Cloud</b>: (Standaardinstelling) Gebruikt <span class="keyword"> Experience Cloud</span> Single Sign-On. Geef uw Experience Cloud-id en wachtwoord op. </p> </li> 
     <li id="li_6C80468835D04CC09F4AEC46D1300310"> <p><b>Webservices</b>: Specificeer uw gebruikersbenaming van de Diensten van het Web en gedeeld geheim. </p> <p>De gedeelde geheime geloofsbrieven worden gevestigd in <span class="uicontrol"> Admin </span> &gt; de Montages <span class="uicontrol"> van het Bedrijf &gt; de Diensten</span> van het <a href="https://docs.adobe.com/content/help/en/analytics/admin/company-settings/web-services-admin.html"></a>Web. </p> <p>De ontwikkelaars, zien de Toegang van de Dienst van het Web tot de Onderneming API <a href="https://marketing.adobe.com/developer/en_US/get-started/enterprise-api/c-get-web-service-access-to-the-enterprise-api"></a> voor hulp bij het verkrijgen van de geloofsbrieven van de Diensten van het Web krijgen. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <b>Handmatig</b>: Beheer manueel de code AppMeasurement. You can download the <span class="keyword"> Analytics</span><span class="keyword"> AppMeasurement</span> code from <span class="ignoretag"><span class="uicontrol"> Admin Tools</span> &gt; <span class="uicontrol"> Code Manager</span></span>. </p> <p>Klik op <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/appmeasure_mjs.html"> JavaScript (nieuw)</a> voor informatie over het lokaal downloaden van de code om deze te kopiëren en plakken in het veld <span class="wintitle"> Code</span> bewerken in <a href="/help/implement/other/dtm/c-aa-tool/library-management.md"> Bibliotheekbeheer</a>. </p> <p>Vul de gebieden in specifiek voor een handconfiguratie: </p> 
    <ul id="ul_CFB6CE78AEB743EF8B47BAAC42E2DB0A"> 
     <li id="li_5B7046CD95AB416F8C113B381A264D91"> <p><b>Productieaccount-id: </b>(Vereist) Uw productieaccount voor gegevensverzameling. Voor Analytics is dit uw rapportsuite-id. Met Dynamic Tag Management wordt automatisch het juiste account geïnstalleerd in de productie- en staging omgeving. </p> </li> 
     <li id="li_14E840FD79A0451BABEDD15DC0584768"> <p><b>Staging account-id: </b>(Vereist) Wordt gebruikt in uw ontwikkelings- of testomgeving. Voor Analytics is dit uw rapportsuite-id. Een staging account houdt uw testdata gescheiden van de productie. </p> </li> 
     <li id="li_69E6C6A41F5240E1ABE8ABE0B9D151FC"> <p><b>Trackingserver: </b>Geef de gegevens voor uw trackingserver op. </p> <p>De variabelen <span class="wintitle"> Tracking Server</span> en <span class="wintitle"> SSL Tracking Server</span> worden gebruikt voor cookie-implementatie van de eerste partij om het domein te specificeren waarop het beeldverzoek en het koekje worden geschreven. Voor meer informatie, zie Correct <a href="https://helpx.adobe.com/analytics/kb/determining-data-center.html"> trackingServer en trackingServerSecure het artikel van de Variabele</a> bevolken. </p> </li> 
     <li id="li_1A7271C68205428F8CA5548A96CACBEC"> <p><b>SSL-traceringsserver: </b>Geef de gegevens op voor uw SSL-tracking-server. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

1. Klik **[!UICONTROL Create Tool]** om het gereedschap te maken en weer te geven voor bewerking.

   De hulpmiddelen worden getoond op het [!UICONTROL Overview] lusje, onder [!UICONTROL Installed Tools].

1. (Voorwaardelijk) Vorm het hulpmiddel verder zonodig door de richtingen in de hieronder verbindingen ( [!UICONTROL General], [!UICONTROL Library Management], [!UICONTROL Global Variables], [!UICONTROL Pageviews & Content], [!UICONTROL Link Tracking], [!UICONTROL Referrers & Campaigns], [!UICONTROL Cookies], en [!UICONTROL Customize Page Code]) te volgen.

Zie [Veelgestelde vragen over het hulpprogramma](/help/implement/faq.md) Adobe Analytics voor meer informatie over dit hulpprogramma.

## Een bestaand hulpprogramma voor Adobe Analytics bewerken {#section_148B16AF429B4949B06238D90635B726}

U kunt een bestaand hulpprogramma voor Adobe Analytics bewerken om de configuratie-instellingen te wijzigen.

1. Klik op het ![](assets/settings_gear.png) [!UICONTROL Overview] tabblad op het pictogram naast een geïnstalleerd gereedschap.
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
   <td colname="col2"> <p>Opmerking: Het toelaten van dit plaatsen verandert manueel gevormde implementatie in de automatische die configuratiemethode in de Methode <span class="term"> van de</span>Configuratie wordt beschreven. </p> <p>Met deze optie kan Dynamic Tag Management automatisch de configuratie van uw <span class="keyword"> Adobe Analytics</span> -account ophalen. </p> <p>De meest recente beschikbare code voor AppMeasurement wordt gebruikt en de verbeteringsberichten worden getoond voor selectie aangezien de nieuwe versies beschikbaar worden. U kunt ook zo nodig terugdraaien naar vorige AppMeasurement-versies, bijvoorbeeld om compatibiliteitsredenen. Er worden maximaal vijf vorige versies weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Referenties bijwerken </p> </td> 
   <td colname="col2"> <p>Vernieuw bijvoorbeeld de API om rapportsuites bij te werken die aan een gebruiker zijn gekoppeld. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. (Voorwaardelijk) Vorm het hulpmiddel verder zonodig door de richtingen in de hieronder verbindingen ( [!UICONTROL General], [!UICONTROL Library Management], [!UICONTROL Global Variables], [!UICONTROL Pageviews & Content], [!UICONTROL Link Tracking], [!UICONTROL Referrers & Campaigns], [!UICONTROL Cookies], en [!UICONTROL Customize Page Code]) te volgen.
1. Klik op **[!UICONTROL Save Changes]**.
