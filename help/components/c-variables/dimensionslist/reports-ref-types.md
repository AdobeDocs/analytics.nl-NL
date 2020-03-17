---
description: Door de bezoekersverwijzingssites voor elk bezoek bij te houden en op te nemen, kunt u bepalen hoe bezoekers uw site voor elk bezoek hebben gevonden.
title: Type referentie
topic: Reports
uuid: 7f63d327-d223-4537-a722-4780aae05c2b
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Type referentie

Door de bezoekersverwijzingssites voor elk bezoek bij te houden en op te nemen, kunt u bepalen hoe bezoekers uw site voor elk bezoek hebben gevonden.

In de onderstaande lijst worden de verschillende typen referenties gedefinieerd:

**Andere websites**: bezoekers worden opgenomen wanneer bezoekers op een koppeling op een pagina op een andere website (die niet als onderdeel van uw site is gedefinieerd) klikken en op uw website aankomen.

**Zoekprogramma**&#39;s: Zoekprogrammaverwijzingen worden opgenomen wanneer bezoekers uw site openen met een zoekprogramma. De verwijzingswaarde moet door Adobe als zoekmachine worden beschouwd en kan geen subdomein zijn dat niet als een zoekmachine wordt beschouwd ( [!DNL mail.yahoo.com] is bijvoorbeeld geen zoekmachine omdat dit domein voor e-mail wordt gebruikt).

**[!UICONTROL Social networks]**: De verwijzende waarde moet door Adobe als een sociaal netwerk worden beschouwd. Zie [Lijst met sociale netwerken](https://helpx.adobe.com/analytics/kb/list-social-networks.html).

**E-mail**: Een verwijzend domein wordt beschouwd als een e-mailverwijzend domein wanneer bezoekers op een e-mailberichtenkoppeling klikken die het protocol bevat [!DNL imap://] of [!DNL mail://] en bij uw plaats aankomen. Alles die bijvoorbeeld afkomstig [!DNL https://mail.yahoo.com] is, wordt niet als een e-mailreferentie geteld omdat het protocol [!DNL https://]is. E-mails van Outlook worden gerapporteerd in de regel Typed/Bookmarked, terwijl elke referentie met een HTTP-protocol waarbij het domein een bekende zoekmachine is, wordt gerapporteerd in de regel Zoekmachine.

**Getypte/bladwijzer**: verwijzingen worden opgenomen wanneer bezoekers de URL van uw site rechtstreeks in hun browser typen of als ze uw site openen door bladwijzers te selecteren. Mobiele apparaten rapporteren een referentietype van *`typed/bookmarked`* als er geen referentie is bij de eerste hit van het bezoek.

**[!UICONTROL Inside Your Site]**: Deze items zijn URL&#39;s die zijn gelabeld door de interne URL-filters. Deze posten worden niet geteld als *`referrer instances`* maar kunnen worden gezien bij de rapportage over andere cijfers.

## Typen referentie per interface {#section_4D8CE5E111DD48FBBDCF9B5A1F16E92E}

<table id="table_EC7423532C7E44DE97B7FC0321585A2B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry"> Marketingrapporten en -analyses (SiteCatalyst) </th> 
   <th colname="col3" class="entry"> Ad-hocanalyse </th> 
   <th colname="col4" class="entry"> Gegevenspakhuis </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Gerapporteerde verwijzingstypen </td> 
   <td colname="col2"> 
    <ul id="ul_EFC8E81EC6DF4CC2AC0E290244FD5859"> 
     <li id="li_686FCAEB04054B9F8A7D2434E8C49F04">Overige websites </li> 
     <li id="li_C232868230AA4A54958B524F3D8FDA35"> Zoekprogramma's </li> 
     <li id="li_A89BFD0468F74ED7822F64BE4A7332AE"> Sociaal </li> 
     <li id="li_C824E6F7F6E748DD827A95B105ADBADD"> Getypte/bladwijzer </li> 
    </ul> <p> Dit rapport geeft slechts twee vooraf gedefinieerde metriek weer: Instanties en unieke bezoekers. </p> </td> 
   <td colname="col3"> 
    <ul id="ul_FD81EB3C1BD949A39C5A9E9688D25271"> 
     <li id="li_6099E7E03F3843D484808258A332BBE9">Overige websites </li> 
     <li id="li_5AABC02DA7964D578BF8404DA819245D"> Zoekprogramma's </li> 
     <li id="li_B18907AC7FA1429A893B57634EB7DC6F"> Sociaal </li> 
     <li id="li_7674B67897994E1FA99BCD9B604BCB6E"> Getypte/bladwijzer </li> 
    </ul> </td> 
   <td colname="col4"> 
    <ul id="ul_C37ADBEC31D04295BF5CDEA25DB5191A"> 
     <li id="li_81A642C96C674669BA00B2DACA534B8A">Overige websites </li> 
     <li id="li_29B9DA9F2AAD46A69886D34D5E6E43D4"> Zoekprogramma's </li> 
     <li id="li_E381EEF111F248F99EE39600D616B7C2"> Sociaal </li> 
     <li id="li_596377F4D3C248BEA5191EE2985A2B13"> Getypte/bladwijzer </li> 
     <li id="li_A7A72D3D6B9A4CCFB43EDA77ABFDEDBC"> Binnen uw site </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Notities {#section_B83A3571D64E4E7792712FAF740D7955}

* Het verwijzende, verwijzende type, en verwijzende domein worden geplaatst bij de eerste klap van het bezoek, of tijdens een bezoek wanneer de verwijzende (bijvoorbeeld, als een bezoeker uw plaats verlaat, een onderzoeksmotor gebruikt, dan aan uw plaats terugkeert alvorens het eerste bezoek verloopt). Deze waarden worden tegelijkertijd ingesteld en blijven tijdens het bezoek behouden.
* Niet alle verwijzingstypes zijn vermeld in dit rapport. Dit betekent dat bezoeken voor de hele site niet overeenkomen met bezoeken voor dit rapport.

## Rapportgeschiedenis {#section_6C0FCEA9DAF04D97BA056E153B7E4628}

| Datum | Wijzigen |
|---|---|
| 1/16/2014 | Het pakhuis van gegevens werd bijgewerkt om de logica aan te passen die door marketing rapporten &amp; analyses wordt gebruikt. Vóór deze datum bleef het verwijzingstype tijdens het bezoek niet behouden. |

