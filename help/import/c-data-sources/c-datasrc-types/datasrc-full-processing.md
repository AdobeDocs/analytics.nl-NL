---
description: Gegevensbronnen ondersteunen de volgende variabelen bij het verwerken van gegevens als een standaardserveraanroep (Algemeen > Volledige verwerking).
title: Volledige verwerking
topic-fix: Developer and implementation
exl-id: 9eb8c754-f4de-4483-934e-3f79134516ca
source-git-commit: 0b31585f5a928d68083764b80f3a08927b407387
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 7%

---

# Volledige verwerking

>[!IMPORTANT]
>
>Adobe raadt u aan de [BDIA (Bulk Data Insertion API)](https://www.adobe.io/apis/experiencecloud/analytics/docs.html) in plaats van volledige verwerkingsgegevensbronnen. Adobe heeft volledige verwerkingsgegevensbronnen vervangen op 31 januari 2022. [Meer informatie](/help/import/c-data-sources/c-datasrc-types/datasrc-fullproc-eol.md)

Gegevensbronnen ondersteunen de volgende variabelen bij het verwerken van gegevens als een standaardserveraanroep (Algemeen > Volledige verwerking).

Gegevens van gegevensbronnen van volledige verwerking worden verwerkt alsof deze zijn ontvangen door Adobe-servers op het opgegeven tijdstip (elke hit bevat een tijdstempel).

* [Bezoekersprofiel](/help/import/c-data-sources/c-datasrc-types/datasrc-full-processing.md#section_6065627D0C144506965F562C80AE67F8)
* [Kolomverwijzing](/help/import/c-data-sources/c-datasrc-types/datasrc-full-processing.md#section_92BAE76639E3404E97276B1BE0581078)

## Bezoekersprofiel {#section_6065627D0C144506965F562C80AE67F8}

Gegevens van gegevensbronnen voor volledige verwerking worden verwerkt met behulp van afzonderlijke bezoekersprofielen. Zelfs als de bezoekersidentiteitskaart in geüploade gegevens overeenkomt met gegevens die zijn verzameld met JavaScript of een andere AppMeasurement-bibliotheek, worden de bezoekersprofielen niet verbonden vanuit het oogpunt van eVar-toewijzing.

Bijvoorbeeld een gebruiker met een bezoeker-id van `"user@example.com"` bezoekt uw site vanuit een marketingcampagne met de naam &quot;Spring Sale&quot;, die is opgeslagen in de variabele campagne. Als u later een transactie uploadt met dezelfde bezoeker-id, ontvangt de campagne &quot;Verkoop voorjaar&quot; geen kredieten voor geüploade inkomsten- of succesgebeurtenissen met behulp van volledige verwerkingsgegevensbronnen.

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
   <td colname="col1"> <p>campaign </p> </td> 
   <td colname="col2"> <p>campagne </p> </td> 
   <td colname="col3"> <p>Code voor bijhouden van conversiecampagne. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>channel </p> </td> 
   <td colname="col2"> <p>kanaal </p> </td> 
   <td colname="col3"> <p>Kanaaltekenreeks (bijvoorbeeld Sportsectie). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>currencyCode </p> </td> 
   <td colname="col2"> <p>currencyCode </p> <p>Opmerking: Deze variabele wordt ook ondersteund door standaardgegevensbronnen als <code> currency code </code>. </p> </td> 
   <td colname="col3"> <p>Valutacode van de opbrengst (bijvoorbeeld, USD). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>timestamp </p> </td> 
   <td colname="col2"> <p>date </p> </td> 
   <td colname="col3"> <p>De ISO 8601-datumnotatie gebruiken van <code> YYYY-MM-DDThh:mm:ss±UTC_offset </code> (bijvoorbeeld <code> 2013-09-01T12:00:00-07:00 </code>) of Unix Time Format (het aantal seconden dat is verstreken sinds 1 januari 1970). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eVar<i>N</i> </p> </td> 
   <td colname="col2"> <p>eVar<i>N</i>, d.w.z. &lt;evar2&gt;...&lt;/evar2&gt; </p> </td> 
   <td colname="col3"> <p>Naam van conversie-eVar. U kunt maximaal 75 eVars ( <span class="varname"> eVar1 </span> - <span class="varname"> eVar75 </span>). </p> <p>U kunt de naam van de eVar (eVar12) of een vriendelijke naam (Advertentiecampagne 3) opgeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>events </p> </td> 
   <td colname="col2"> <p>gebeurtenissen </p> </td> 
   <td colname="col3"> <p>De koord van gebeurtenissen, geformatteerd gebruikend de zelfde syntaxis zoals <a href="https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/events/event-serialization.html"  > s.events </a> variabele. </p> <p>Bijvoorbeeld: </p> 
    <code>
      scAdd,event1,event7 
    </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>kassier<i>N</i> </p> </td> 
   <td colname="col2"> <p>kassier<i>N</i>, d.w.z. &lt;hier2&gt;...&lt;/hier2&gt; </p> </td> 
   <td colname="col3"> <p>Hiërarchienaam. U kunt maximaal vijf hiërarchieën gebruiken ( <span class="varname"> hier1 </span> - <span class="varname"> hier5 </span>). </p> <p>U kunt de standaardhiërarchienaam opgeven ( <span class="varname"> hier2 </span>) of een vriendelijke naam ( <span class="term"> Yankees </span>). </p> </td> 
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
   <td colname="col3"> <p>Pagina-URL (bijvoorbeeld <code>https://www.example.com/index.html)</code>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>products </p> </td> 
   <td colname="col2"> <p>producten </p> </td> 
   <td colname="col3"> <p>Productlijst (bijvoorbeeld <code> "Sports;Ball;1;5.95"</code>). Kan maximaal 4096 bytes per rij bevatten.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>prop1 - prop75 </p> </td> 
   <td colname="col2"> <p>prop<i>N</i>, d.w.z. &lt;prop2&gt;...&lt;/prop2&gt; </p> </td> 
   <td colname="col3"> <p>Eigenschap#-tekenreeks (bijvoorbeeld <span class="term"> Sectie Sport </span>). </p> </td> 
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
   <td colname="col2"> <p>De ondersteunde tekenset voor uw website. Bijvoorbeeld UTF-8, ISO-8859-1 enzovoort. </p> <p>Zie de <a href="https://experienceleague.adobe.com/docs/analytics/implementation/vars/config-vars/configuration-variables.html#concept_E65B9A8F75C3482C87D0D455805F89BD"  > Tekensets met meerdere bytes </a> (Internationalisatie) whitepaper voor een volledige lijst. </p> </td> 
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
   <td colname="col2"> <p>Verbindingstype van bezoeker ( <span class="term"> lan </span> of <span class="term"> modem </span>). </p> </td> 
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
   <td colname="col1"> <p>referrer </p> </td> 
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
   <td colname="col1"> <p>visitorID </p> </td> 
   <td colname="col2"> <p>ID bezoeker. </p> </td> 
  </tr> 
 </tbody> 
</table>
