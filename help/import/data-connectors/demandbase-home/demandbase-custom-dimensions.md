---
description: Vermeldt optionele dimensie-id's die kunnen worden gegeven in stap 4 van de wizard Adobe Integration.
title: Aangepaste afmetingen op basis van vereisten
uuid: d1621046-3aa2-46b9-a536-4a8fb792b69f
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Aangepaste afmetingen op basis van vereisten{#demandbase-custom-dimensions}

Vermeldt optionele dimensie-id&#39;s die kunnen worden gegeven in stap 4 van de wizard Adobe Integration.

Als u niet zeker weet welke exacte API-id u voor de wizard moet gebruiken, neemt u contact op met uw demandasevertegenwoordiger.

>[!IMPORTANT]
>
>Het wordt sterk geadviseerd dat u NIET IP Adres als douanedimensie omvat. Het extreem hoge aantal unieke waarden kan prestatieproblemen met rapportage veroorzaken. Bovendien wordt IP het Adres reeds aangeboden als rapporteringsoptie door de gegevenspakaarrapportering van Adobe.

<table id="table_3B44A18BE5FE45BC83389F89B48D9B97"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Dimensie </th> 
   <th colname="col2" class="entry"> API-id's </th> 
   <th colname="col3" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> ISP </td> 
   <td colname="col2"> isp </td> 
   <td colname="col3"> Wijst erop of de geïdentificeerde organisatie als ISP wordt geclassificeerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Marketingalias </td> 
   <td colname="col2"> marketing_alias </td> 
   <td colname="col3"> De schoongemaakte en/of verkorte organisatienaam (32 karakters of minder) voor gebruik in advertenties, berichten of marketing exemplaar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Accountcontroletags </td> 
   <td colname="col2"> watch_list (aangepast) </td> 
   <td colname="col3">Onbeperkte set tags gedefinieerd door client die per organisatie kan worden toegevoegd aan de API-responsgegevens. <p><b>Voorbeeld</b>: Als u een controletag genoemd Q4 Doel hebt, zou het API gebied zijn </p> <code> watch_list_q4_target</code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Fortune 1000 </td> 
   <td colname="col2"> fortune_1000 </td> 
   <td colname="col3"> Geeft aan of de organisatie op de lijst Fortune 1000 staat. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Forbes 2000 </td> 
   <td colname="col2"> forbes_2000 </td> 
   <td colname="col3"> Geeft aan of de organisatie op de lijst Forbes 2000 staat. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Aantal werknemers </td> 
   <td colname="col2"> employee_count </td> 
   <td colname="col3"> Het aantal werknemers van de organisatie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Jaarlijkse verkoop </td> 
   <td colname="col2"> year_sales </td> 
   <td colname="col3"> Voor overheidsinstanties zijn de jaarlijkse inkomsten gebaseerd op door ondernemingen gerapporteerde openbare gegevens over het mondiale hoofdkwartier op alle locaties. Voor particuliere organisaties is de raming gebaseerd op een consensusschatting van het jaarlijkse aantal verkoopopbrengsten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Telefoonnummer </td> 
   <td colname="col2"> telefoon </td> 
   <td colname="col3"> Het telefoonnummer van de geïdentificeerde organisatie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Adres </td> 
   <td colname="col2"> street_address </td> 
   <td colname="col3"> Het adres van de geïdentificeerde organisatie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Plaats </td> 
   <td colname="col2"> stad </td> 
   <td colname="col3"> De stad van de geïdentificeerde organisatie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Staat </td> 
   <td colname="col2"> state </td> 
   <td colname="col3"> De status van de geïdentificeerde organisatie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Landcode </td> 
   <td colname="col2"> country_code </td> 
   <td colname="col3"> De ISO-landcode van twee tekens van de geïdentificeerde organisatie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Landnaam </td> 
   <td colname="col2"> country_name </td> 
   <td colname="col3"> De naam van het land van de tekenreekswaarde voor de geïdentificeerde organisatie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Postcode </td> 
   <td colname="col2"> zip </td> 
   <td colname="col3"> De postcode van het land/de staat voor de geïdentificeerde organisatie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Website </td> 
   <td colname="col2"> web_site </td> 
   <td colname="col3"> De URL die wordt gebruikt door de geïdentificeerde organisatie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Stock Ticker </td> 
   <td colname="col2"> stock_ticker </td> 
   <td colname="col3"> De beurs indien de geïdentificeerde organisatie openbaar wordt verhandeld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Primaire SIC-code </td> 
   <td colname="col2"> primary_sic </td> 
   <td colname="col3"> Consensus SIC-code toegewezen voor de geïdentificeerde organisatie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Breedte </td> 
   <td colname="col2"> breedtegraad </td> 
   <td colname="col3"> Latitude voor de locatie van de geïdentificeerde organisatie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Lengtegraad </td> 
   <td colname="col2"> lengtegraad </td> 
   <td colname="col3"> Lengtegraad voor de locatie van de geïdentificeerde organisatie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verkeer </td> 
   <td colname="col2"> verkeer </td> 
   <td colname="col3"> De hoeveelheid websiteverkeer, geschat op laag, middelgroot, hoog of zeer hoog. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> B2B </td> 
   <td colname="col2"> b2b </td> 
   <td colname="col3"> Geeft aan dat het geïdentificeerde bedrijf hoofdzakelijk aan andere ondernemingen verkoopt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> B2C </td> 
   <td colname="col2"> b2c </td> 
   <td colname="col3"> Geeft aan dat de geïdentificeerde onderneming hoofdzakelijk aan consumenten of particulieren verkoopt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Technology Insight </td> 
   <td colname="col2"> ??? </td> 
   <td colname="col3"> Tot 75 technologiecategorieën die door klanten via categorie, verkoper en producten worden bepaald voor het gebruiken van het richten en/of het aanpassen van advertenties, berichten of marketing exemplaar. </td> 
  </tr> 
 </tbody> 
</table>

