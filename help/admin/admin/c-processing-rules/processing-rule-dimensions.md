---
description: De afmetingen die u kunt lezen en schrijven (tenzij anders vermeld) gebruikend verwerkingsregels.
subtopic: Processing rules
title: Beschikbare dimensies voor verwerkingsregels
feature: Processing Rules
exl-id: ffd7a1d6-2c9d-41e7-9c75-9e47b6f9c283
source-git-commit: 71b3b1937e7fa272f0497008e8e510204bbb4418
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 3%

---

# Beschikbare dimensies voor verwerkingsregels

De afmetingen die u kunt lezen en schrijven (tenzij anders vermeld) gebruikend verwerkingsregels.

## Aangepaste waarden en contextgegevens {#section_7A5E1810CAC34B0BBC69F8F5F7C75AA5}

<table id="table_5011C501D5DC489E87A42FFC51DEB40D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Waarde </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Aangepaste waarde </p> </td> 
   <td colname="col2"> <p>Aangepaste tekst of waarden die rechtstreeks in een verwerkingsregel worden getypt. Deze waarden zijn beschikbaar in volgende voorwaarden en regels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Samengevoegde waarde </p> </td> 
   <td colname="col2"> <p>Waarden die worden gemaakt door twee waarden te combineren. U kunt bijvoorbeeld de categorie en de paginanaam combineren om een subcategorie te maken. Deze waarden zijn beschikbaar in volgende voorwaarden en regels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gewijzigde waarden </p> </td> 
   <td colname="col2"> <p>Als een veranderlijke waarde gebruikend verwerkingsregels wordt veranderd, wordt de veranderde waarde gebruikt in verdere voorwaarden en regels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Contextgegevensvariabelen </p> </td> 
   <td colname="col2"> <p>Benoemde variabelen die met een hit worden verzonden. </p> <p>Opmerking: Om het even welke gegevens in een Variabele van de Gegevens van de Context moeten aan een rapporteringsvariabele worden gekopieerd om in een rapport te verschijnen. De Variabelen van de Gegevens van de context zijn niet viewable in om het even welke rapporteringsinterface, met inbegrip van de Gegevensvoer ClickStream. </p> <p> <a href="/help/admin/admin/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data.md"> Een contextgegevensvariabele naar een eVar kopiëren </a> </p> <p> <a href="/help/admin/admin/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data-event.md"> Een gebeurtenis instellen met een Context Data-variabele </a> </p> <p> <a href="/help/implement/vars/page-vars/contextdata.md"> Contextgegevensvariabelen</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Verkeersvariabelen {#section_225156106F8B41F8BC1E68D58DDC2652}

<table id="table_575F618C59DC4933BC77F935518EAE39"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Variabele </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>prop 1-75 </p> </td> 
   <td colname="col2"> <p> <code> prop1 - prop75</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hiërarchie 1-5 </p> </td> 
   <td colname="col2"> <p> <code> hier1 - hier5</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sectie Site </p> </td> 
   <td colname="col2"> <p> <code> s.channel </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Server </p> </td> 
   <td colname="col2"> <p> <code> s.server </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Kenmerken Actief {#section_07E69A86A47741A083FD84F112EB80D0}

<table id="table_9011B1FA462B4DBBAA58FC2D6D638DA1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Kenmerk </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>ID rapportsuite (alleen-lezen) </p> </td> 
   <td colname="col2"> <p>De rapportsuite waarop de verwerkingsregel wordt uitgevoerd, is mogelijk niet de oorspronkelijke rapportsuite die in AppMeasurement is opgegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Paginanaam </p> </td> 
   <td colname="col2"> <p> <code> s.pageName</code> </p> <p>Opmerking: De het volgen van de verbinding vraag ontdoet <code>pageName</code> variabel voordat zij verwerkingsregels bereiken. Als u een waarde van de paginanaam opnieuw opneemt gebruikend verwerkingsregels, wordt de klap beschouwd als een paginamening in plaats van een verbinding die vraag volgt. Adobe raadt u aan te controleren of de paginanaam al is ingesteld voordat u deze wijzigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pagina-URL </p> </td> 
   <td colname="col2"> <code> s.pageURL</code> of de URL van de huidige pagina als <code> s.pageURL</code> is niet opgegeven. <p>Opmerking: De het volgen van de verbinding vraag ontdoet <code>pageURL</code> variabel voordat zij verwerkingsregels bereiken. Als u een pagina-URL-waarde opnieuw invoegt met verwerkingsregels, wordt de treffer beschouwd als een paginaweergave in plaats van een aanroep voor het bijhouden van koppelingen. Adobe raadt aan te controleren of de pagina-URL al is ingesteld voordat u deze wijzigt. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Parameter querytekenreeks </p> </td> 
   <td colname="col2"> <p>De waarde van een opgegeven parameter voor een querytekenreeks in de huidige URL of null als er geen parameter bestaat. Voor de URL <b>https://www.example.com/a.html?cid=ad1&amp;node=4</b>, de waarde van de Parameter van het Koord van de Vraag <span class="syntax codeph"> cid</span> is <b>ad1</b>, en de waarde van de Parameter van het Koord van de Vraag <span class="syntax codeph"> node</span> is <b>4</b>. </p> <p>Als u JavaScript AppMeasurement H.25.2 of eerder uitvoert, kan de pagina-URL na 255 tekens worden afgekapt. JavaScript AppMeasurement H.25.3 (uitgebracht in januari 2013) en geef de volledige URL naar de verwerkingsregels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pad naar pagina </p> </td> 
   <td colname="col2"> <p>Het pad van de pagina-URL. Het pad van de URL <b>https://www.example.com/news/a.html?cid=ad1</b> is <span class="syntax codeph"> news/a.html</span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Paginadomein </p> </td> 
   <td colname="col2"> <p>De volledige hostnaam, opgegeven in de URL. https://<span class="syntax codeph"> en.main.example.co.uk</span>/index.jsp?q=value </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hoofddomein van pagina </p> </td> 
   <td colname="col2"> <p>De laatste twee secties van hostname van de pagina. https://en.main.example.<span class="syntax codeph"> co.uk</span>/index.jsp?q=value </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tekenreeks paginaquery </p> </td> 
   <td colname="col2"> <p>De volledige queryreeks van de URL. https://en.main.example.co.uk/index.jsp?<span class="syntax codeph"> q=value</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Referrer* (alleen-lezen) </p> </td> 
   <td colname="col2"> <p>HTTP-referentie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Refering Query String Parameter (alleen-lezen) </p> </td> 
   <td colname="col2"> <p>De waarde van een opgegeven parameter voor een querytekenreeks in de verwijzende URL of null als er geen parameter bestaat. Voor de URL <b>https://www.example.com/a.html?cid=ad1&amp;node=4</b>, de waarde van de Parameter van het Koord van de Vraag <span class="syntax codeph"> cid</span> is <b>ad1</b>, en de waarde van de Parameter van het Koord van de Vraag <span class="syntax codeph"> node</span> is <b>4</b>. </p> <p>Als u JavaScript AppMeasurement H.25.2 of eerder uitvoert, kan de pagina-URL na 255 tekens worden afgekapt. JavaScript AppMeasurement H.25.3 (uitgebracht in januari 2013) en geef de volledige URL naar de verwerkingsregels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Refering Domain (alleen-lezen) </p> </td> 
   <td colname="col2"> <p>De volledige hostnaam van de verwijzende. https://<span class="syntax codeph"> en.main.example.co.uk</span>/index.jsp?q=value </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Refering Root Domain (alleen-lezen) </p> </td> 
   <td colname="col2"> <p>De laatste twee secties van hostname van de verwijzende. https://en.main.example.<span class="syntax codeph"> co.uk</span>/index.jsp?q=value </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verwijzen naar queryreeks (alleen-lezen) </p> </td> 
   <td colname="col2"> <p>Parameters van de queryreeks in de verwijzende URL. https://en.main.example.co.uk/index.jsp?<span class="syntax codeph"> q=value</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>IP-adres (alleen-lezen) </p> </td> 
   <td colname="col2"> <p>IP-adres zoals opgegeven door de browser. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gebruikersagent (alleen-lezen) </p> </td> 
   <td colname="col2"> <p>Gebruikersagent zoals gemeld door de browser. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Versie toepassingsmeetcode (alleen-lezen) </p> </td> 
   <td colname="col2"> <p>De versie van de appMeturement-bibliotheek die is gebruikt om de aanvraag in te dienen. Wanneer u beacons voor afbeeldingen gebruikt, kunt u deze vullen met een aangepaste waarde die wordt gelezen met verwerkingsregels. Deze waarde wordt op de volgende locatie in de URL weergegeven: </p> <p>https://server.net/b/ss/report-suite-ID/1/<span class="syntax codeph"> CODEVERSION</span>/... </p> </td> 
  </tr> 
 </tbody> 
</table>

## Conversievariabelen {#section_311856B21B3B49DBAA0539CFA06C409F}

<table id="table_E28729026EDA485989178A3B887B5983"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Variabele </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>eVar 1-N </p> </td> 
   <td colname="col2"> <p> <code> evar1</code> - <code> evarN</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Code bijhouden campagne </p> </td> 
   <td colname="col2"> <p> <code> s.campaign</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Valutacode </p> </td> 
   <td colname="col2"> <p> <code> s.currencyCode</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Variabelen1-3 weergeven </p> </td> 
   <td colname="col2"> <p> <code> s.list1</code> - <code> s.list3</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aankoop-id </p> </td> 
   <td colname="col2"> <p> <code> s.purchaseID</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Transactie-id </p> </td> 
   <td colname="col2"> <p> <code> s.transactionID </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bezoekende staat </p> </td> 
   <td colname="col2"> <p> <code> s.state</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Postcode bezoeker </p> </td> 
   <td colname="col2"> <p> <code> s.zip</code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Gebeurtenissen geslaagd {#section_C1946FEB64FC4F579671EC5E0D06AE8A}

Met verwerkingsregels kunnen gebeurtenissen worden ingesteld, maar deze kunnen niet als voorwaarden worden gelezen.

<table id="table_926ED12B58CA4FB685D799DC6EE567C0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Gebeurtenis </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Gebeurtenis 1-1000 </p> <p>(Voor klanten van SiteCatalyst 15, gebeurtenis 1-100.) </p> </td> 
   <td colname="col2"> <p> <code> event1</code> - <code> event1000</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>aankoop, scView, scAdd, en andere kartgebeurtenissen </p> </td> 
   <td colname="col2"> <p>Vooraf gedefinieerde gebeurtenissen. </p> </td> 
  </tr> 
 </tbody> 
</table>
