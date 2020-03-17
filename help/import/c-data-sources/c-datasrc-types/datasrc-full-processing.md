---
description: Gegevensbronnen ondersteunen de volgende variabelen bij het verwerken van gegevens als een standaardserveraanroep (Algemeen > Volledige verwerking).
subtopic: Data sources
title: Volledige verwerking
topic: Developer and implementation
uuid: 590ae89c-6e17-453b-b701-ce1adbea6fa4
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Volledige verwerking

Gegevensbronnen ondersteunen de volgende variabelen bij het verwerken van gegevens als een standaardserveraanroep (Algemeen > Volledige verwerking).

Gegevens van gegevensbronnen van volledige verwerking worden verwerkt alsof deze op het opgegeven tijdstip zijn ontvangen door Adobe-servers (elke hit bevat een tijdstempel).

* [Bezoekerprofiel](/help/import/c-data-sources/c-datasrc-types/datasrc-full-processing.md#section_6065627D0C144506965F562C80AE67F8)
* [Kolomverwijzing](/help/import/c-data-sources/c-datasrc-types/datasrc-full-processing.md#section_92BAE76639E3404E97276B1BE0581078)

## Bezoekerprofiel {#section_6065627D0C144506965F562C80AE67F8}

Gegevens van gegevensbronnen voor volledige verwerking worden verwerkt met afzonderlijke bezoekersprofielen. Zelfs als de bezoekersidentiteitskaart in geüploade gegevens overeenkomt met gegevens die zijn verzameld met JavaScript of een andere AppMeasurement-bibliotheek, worden de bezoekersprofielen niet verbonden vanuit een eVar-toewijzingsperspectief.

Bijvoorbeeld, een gebruiker met een bezoekersidentiteitskaart van `"user@example.com"` bezoeken uw plaats van een marketing campagne genoemd &quot;Verkoop van de Lente&quot;, die in de campagnevariabele wordt opgeslagen. Als u later een transactie uploadt met dezelfde bezoeker-id, ontvangt de campagne &quot;Verkoop voorjaar&quot; geen kredieten voor geüploade inkomsten- of succesgebeurtenissen met behulp van volledige verwerkingsgegevensbronnen.

## Kolomverwijzing {#section_92BAE76639E3404E97276B1BE0581078}

<table id="table_AAC04491D643467B9C80FDEF88130B13"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> JavaScript-variabele </th> 
   <th colname="col2" class="entry"> Variabele voor volledige verwerkingskolom </th> 
   <th colname="col3" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>campagne </p> </td> 
   <td colname="col2"> <p>campagne </p> </td> 
   <td colname="col3"> <p>Code voor bijhouden van conversiecampagne. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>kanaal </p> </td> 
   <td colname="col2"> <p>kanaal </p> </td> 
   <td colname="col3"> <p>Kanaaltekenreeks (bijvoorbeeld Sportsectie). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>currencyCode </p> </td> 
   <td colname="col2"> <p>currencyCode </p> <p>Opmerking:  Deze variabele wordt ook ondersteund door standaardgegevensbronnen als <code> currency code </code>. </p> </td> 
   <td colname="col3"> <p>Valutacode van de opbrengst (bijvoorbeeld, USD). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>tijdstempel </p> </td> 
   <td colname="col2"> <p>date </p> </td> 
   <td colname="col3"> <p>Gebruik de datumnotatie ISO 8601 van <code> YYYY-MM-DDThh:mm:ss±UTC_offset </code> (bijvoorbeeld <code> 2013-09-01T12:00:00-07:00 </code>) of Unix Time Format (het aantal seconden dat is verstreken sinds 1 januari 1970). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><i>eVarN</i> </p> </td> 
   <td colname="col2"> <p><i>eVarN</i>, d.w.z. &lt;eVar2&gt;...&lt;/eVar2&gt; </p> </td> 
   <td colname="col3"> <p>Naam conversie van var. U kunt maximaal 75 eVars ( <span class="varname"> eVar1 </span> - <span class="varname"> eVar75 </span>) hebben. </p> <p>U kunt de eVar naam (eVar12) of een vriendschappelijke naam (Advertentiecampagne 3) specificeren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>gebeurtenissen </p> </td> 
   <td colname="col2"> <p>gebeurtenissen </p> </td> 
   <td colname="col3"> <p>De koord van gebeurtenissen, geformatteerd gebruikend de zelfde syntaxis zoals de <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/events.html"  > s.events </a> variabele. </p> <p>Bijvoorbeeld: </p> 
    <code>
      scAdd,event1,event7 
    </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><i>hierN</i> </p> </td> 
   <td colname="col2"> <p><i>hierN</i>, d.w.z. &lt;hier2&gt;..&lt;/hier2&gt; </p> </td> 
   <td colname="col3"> <p>Hiërarchienaam. U kunt maximaal vijf hiërarchieën hebben ( <span class="varname"> hier1 </span> - <span class="varname"> hier5 </span>). </p> <p>U kunt de standaardhiërarchienaam ( <span class="varname"> hier2 </span>) of een vriendelijke naam ( <span class="term"> Yankees </span>) opgeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>linkName </p> </td> 
   <td colname="col2"> <p>linkName </p> </td> 
   <td colname="col3"> <p>Naam van koppeling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>linkType </p> </td> 
   <td colname="col2"> <p>linkType </p> </td> 
   <td colname="col3"> <p>Type koppeling. Tot de ondersteunde waarden behoren: </p> 
    <ul id="ul_E441013055A9447AB6C3FB05B6099F7D"> 
     <li id="li_A33F66F30B60479284F72AE3AD4BF499"> <b>d</b>: Koppeling downloaden </li> 
     <li id="li_182F695AA2D044DAB036BAFE38BC3915"> <b>e</b>: Koppeling afsluiten </li> 
     <li id="li_4FD4D542D1774607860BEF41C1B090D1"> <b>o</b>: Aangepaste koppeling. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>linkURL </p> </td> 
   <td colname="col2"> <p>linkURL </p> </td> 
   <td colname="col3"> <p>HREF of link. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pageName </p> </td> 
   <td colname="col2"> <p>pageName </p> </td> 
   <td colname="col3"> <p>Paginanaam </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pageType </p> </td> 
   <td colname="col2"> <p>pageType </p> </td> 
   <td colname="col3"> <p>Paginatype ("Foutpagina"). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pageURL </p> </td> 
   <td colname="col2"> <p>pageURL </p> </td> 
   <td colname="col3"> <p>Pagina-URL (bijvoorbeeld <code>https://www.mysite.com/index.html)</code>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>producten </p> </td> 
   <td colname="col2"> <p>producten </p> </td> 
   <td colname="col3"> <p>Productlijst (bijvoorbeeld <code> "Sports;Ball;1;5.95") </code>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>prop1 - prop75 </p> </td> 
   <td colname="col2"> <p><i>propN</i>, d.w.z. &lt;prop2&gt;..&lt;/prop2&gt; </p> </td> 
   <td colname="col3"> <p>Eigenschap#-tekenreeks (bijvoorbeeld <span class="term"> Sport Section </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>purchaseID </p> </td> 
   <td colname="col2"> <p>purchaseID </p> </td> 
   <td colname="col3"> <p>Aankoop-id-nummer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>s_account </p> </td> 
   <td colname="col2"> <p>reportSuiteID </p> </td> 
   <td colname="col3"> <p>ID(s) van suite rapporteren waaraan de hit moet worden toegewezen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>server </p> </td> 
   <td colname="col2"> <p>server </p> </td> 
   <td colname="col3"> <p>Servertekenreeks. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>state </p> </td> 
   <td colname="col2"> <p>state </p> </td> 
   <td colname="col3"> <p>Conversiestatekenreeks. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>zip </p> </td> 
   <td colname="col2"> <p>zip </p> </td> 
   <td colname="col3"> <p>ZIP-code conversie. </p> </td> 
  </tr> 
 </tbody> 
</table>

De volgende tabel bevat verkeersvariabelen die automatisch worden ingevuld wanneer de JavaScript-bibliotheken worden gebruikt. Deze eigenschappen hebben geen gekoppelde variabelen, maar kunnen worden geïmporteerd met behulp van gegevensbronnen.

<table id="table_FDBC5BD225644AA09078C0570BE709FE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Variabele voor volledige verwerkingskolom </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>browserHeight </p> </td> 
   <td colname="col2"> <p>Browserhoogte in pixels (bijvoorbeeld 768). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>browserWidth </p> </td> 
   <td colname="col2"> <p>Browserbreedte in pixels (bijvoorbeeld 1024). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>charSet </p> </td> 
   <td colname="col2"> <p>De ondersteunde tekenset voor uw website. Bijvoorbeeld UTF-8, ISO-8859-1 enzovoort. </p> <p>Zie de whitepaper over <a href="https://marketing.adobe.com/resources/help/en_US/whitepapers/multibyte/index.html"  > Multi-Byte Character Sets </a> (Internationalization) voor een volledige lijst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>clickAction </p> </td> 
   <td colname="col2"> <p>Object-id voor bezoeker op kaart klikken (oid) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>clickActionType </p> </td> 
   <td colname="col2"> <p>Type object-id voor bezoeker op kaart klikken (punt) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>clickContext </p> </td> 
   <td colname="col2"> <p>Pagina-id voor bezoeker klikt op kaart (pid) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>clickContextType </p> </td> 
   <td colname="col2"> <p>Type pagina-id voor bezoeker op kaart klikken (pidt) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>clickSourceID </p> </td> 
   <td colname="col2"> <p>Bronindex voor bezoeker op kaart klikken (oi) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>clickTag </p> </td> 
   <td colname="col2"> <p>Naam van objecttag voor bezoeker op kaart klikken (naar) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>colorDepth </p> </td> 
   <td colname="col2"> <p>Kleurdiepte van de monitor in bits (bijvoorbeeld 24). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>connectionType </p> </td> 
   <td colname="col2"> <p>Het verbindingstype van de bezoeker ( <span class="term"> lan </span> of <span class="term"> modem </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>cookiesEnabled </p> </td> 
   <td colname="col2"> <p>Y of N als de bezoeker cookies van de eerste sessie ondersteunt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>currencyCode </p> </td> 
   <td colname="col2"> <p>De standaardvalutacode die op uw Website wordt gebruikt. </p> <p>Bijvoorbeeld USD=U.S. dollars, EUR = EUR, JPY = Japanse yen, enz. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>homePage </p> </td> 
   <td colname="col2"> <p>Y of N — is de huidige pagina op de homepage van de bezoeker. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>javaEnabled </p> </td> 
   <td colname="col2"> <p>Y of N — Heeft de bezoeker Java ingeschakeld? </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>javaScriptVersion </p> </td> 
   <td colname="col2"> <p>JavaScript-versie (bijvoorbeeld 1.3). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>plug-ins </p> </td> 
   <td colname="col2"> <p>Lijst met namen van plug-ins voor browsers, gescheiden door puntkomma's. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>propN </p> </td> 
   <td colname="col2"> <p>Eigenschapswaarden voor uw eigenschappen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>referentie </p> </td> 
   <td colname="col2"> <p>URL voor paginaverwijzing. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>resolutie </p> </td> 
   <td colname="col2"> <p>Monitorresolutie (bijvoorbeeld 1024x768). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>scXmlVer </p> </td> 
   <td colname="col2"> <p>Marketingrapporten XML aanvraagversienummer (bijvoorbeeld 1.0). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>tijdzone </p> </td> 
   <td colname="col2"> <p>De tijdzone van de bezoeker verschuift van GMT in uren (bijvoorbeeld -8). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>bezoekerID </p> </td> 
   <td colname="col2"> <p>ID bezoeker. </p> </td> 
  </tr> 
 </tbody> 
</table>

