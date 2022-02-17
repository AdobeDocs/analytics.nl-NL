---
description: Dit onderwerp verstrekt antwoorden op gemeenschappelijke vragen.
subtopic: Data sources
title: Veelgestelde vragen over gegevensbronnen
topic-fix: Developer and implementation
feature: Data Sources
exl-id: 2a5d38fe-5c5b-4275-bc44-e9cb02ec2f5d
source-git-commit: 79294cfc6f86e5a41a39504099cd730f53668725
workflow-type: tm+mt
source-wordcount: '1494'
ht-degree: 0%

---

# Veelgestelde vragen over gegevensbronnen

Dit onderwerp verstrekt antwoorden op gemeenschappelijke vragen.

## Hoe kunnen wij off-line gegevens aan online gebeurtenissen binden? {#offline}

Als u de gegevensbronnen van de transactie-id wilt koppelen aan online gebeurtenissen, moet u de Opname van de Transactie-id inschakelen. Zie [Transactie-id-opname](/help/import/c-data-sources/datasrc-integrating-offline-data.md#section_30D6D47AEC0F4A36B87EBFE4C858F20C) voor meer informatie .

## Hoeveel kost het om de eigenschap van de Gegevensbron te gebruiken? {#cost}

De Bronnen van gegevens dragen geen extra kosten voorbij de standaardservervraag. De vraagkosten van de server zijn slechts op volledig-verwerkings gegevensbrontypes van toepassing, waar de individuele klappen binnen als rijen van gegevens worden verzonden. Verkeer en gegevensbronnen op geaggregeerd niveau brengen geen extra kosten met zich mee.

## Hoe neem ik commentaren in de dossiers van Gegevensbronnen op? {#comments}

Elke rij in een Gegevensbrondossier dat met een hekje (#) begint wordt behandeld als commentaar.

## Moet ik een datumkolom in mijn spreadsheetgegevens omvatten? {#date}

Ja. Omdat vele marketing rapporten van de datumkolom worden gehouden, vereist de Gegevensbronnen een datumkolom.

## Kan ik gegevens opslaan in bestaande variabelen die ik al gebruik? {#variables}

Adobe raadt u aan nieuwe, ongebruikte variabelen te selecteren om gegevens te importeren met behulp van Gegevensbronnen. Neem contact op met de klantenservice als u niet zeker weet wat de configuratie van uw gegevensbestand is of als u meer inzicht wilt krijgen in de risico&#39;s van het opnieuw gebruiken van variabelen.

## Kan ik gegevens schrappen die gebruikend Gegevensbronnen werden ingevoerd? {#imported}

Nee. Gegevens die met behulp van gegevensbronnen in rapporten zijn geüpload, kunnen niet worden verwijderd, zelfs niet door Adobe-technici, nadat ze zijn geïmporteerd. Het wordt permanent in uw bestaande gegevens opgenomen, en wordt van uw gegevens die door traditionele gegevensinzamelingsmiddelen (d.w.z. JavaScript, ActionSource, de Invoegings API van Gegevens, enz.) worden ingegaan niet van elkaar onderscheiden. Daarom adviseert Adobe sterk het uploaden van de gegevens van Gegevensbronnen in een reeks van het testrapport alvorens in een productiereeks te uploaden.

## Hoeveel gegevens kan ik tegelijkertijd importeren? {#amount}

De verwerking wordt gepauzeerd als de grootte groter is dan 50 MB en pas wordt hervat als het totaal kleiner is dan 50 MB. Als u vertragingen bij het genereren van rapporten wilt beperken, mag u niet meer dan 90 dagen gegevens per dag uploaden.

## Wanneer ik gegevens door Gegevensbronnen invoert, worden de bestaande gegevens beschreven? {#overwrite}

De gegevensbronnen van gegevens beschrijven nooit bestaande rapportgegevens. In plaats daarvan, worden de gegevens geupload gebruikend Gegevensbronnen toegevoegd aan de bestaande gegevens.

## Wanneer ik mijn gegevens via Gegevensbronnen upload, waarom krijg ik niet ook mijn metriek? {#metrics}

Wanneer u de gegevens van Gegevensbronnen uploadt, uploadt u de metriek die in de rapportinterface beschikbaar zal zijn.

Bijvoorbeeld, als u de Ontvangsten van het Centrum van de Vraag voor producten uploadt u op uw plaats verkoopt, kunt u die Ontvangsten van het Centrum van de Vraag in het zelfde rapport hebben zoals Online Ontvangsten. U kunt het echter niet gebruiken in combinatie met Bezoekopdrachten omdat u het aantal bezoeken niet hebt geüpload. Adobe kan slechts over de metriek en de elementen rapporteren die u door Gegevensbronnen (naast de regelmatige metriek van het marketingrapport) uploadde.

## Wat gebeurt als ik negatieve waarden in rapportering door Gegevensbronnen overga? {#negative}

De waarde wordt dienovereenkomstig verlaagd.

## Wat is het verschil tussen een Verkeer en een (Generische) Gegevensbron van de Omzetting? {#traffic}

De bron van de Gegevens van het Verkeer uploadt veel sneller aangezien het slechts de summiere waarden in de aangewezen lijsten bijwerkt. De generieke gegevensbron met conversiegegevens (gebeurtenissen, enz.) maakt een hit voor elke waarde in de kolom die moet worden verwerkt.

Voorbeeldbestand:

<table id="table_D5408E0BDB984229B4C60A66BB53CEBB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code> Date </code> </p> </td> 
   <td colname="col2"> <p> <code> Event15 </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code> 01/01/2013 </code> </p> </td> 
   <td colname="col2"> <p> <code> 553 </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

In het bovenstaande voorbeeld worden 553 hits gemaakt die in het cachesysteem moeten worden verwerkt.

## Houden gegevensbronnen rekening met subrelaties, correlaties en paden? {#breakdown}

Aangezien het proces van de Gegevensbron (&quot;voor Generische DS, niet-Verkeer&quot;) individuele klappen bouwt die door geheim voorgeheugen worden verwerkt, wordt het subrelatieproces gebruikt, maar niet het correlatieproces. Pathing heeft de mogelijkheid om te worden verwerkt, maar elke hit zou zijn eigen bezoek zijn, dus er wordt geen schilderij gegenereerd. Er worden padgegevens gegenereerd voor weblogimport.

## Zijn de dossieruitbreidingen hoofdlettergevoelig voor een Gegevensbron uploadt of een classificatiedossier? {#case}

Als de extensies van een uploadbestand voor een gegevensbron of een classificatiebestand met hoofdletters worden weergegeven, worden de bestanden niet verwerkt. Bestandsextensies voor het uploaden van gegevensbron moeten in kleine letters worden weergegeven. Bijvoorbeeld: [!DNL file.TXT] en [!DNL file.FIN] wordt niet verwerkt. Evenzo [!DNL .TAB] en [!DNL .FIN] wordt niet verwerkt. Maar [!DNL .txt] en [!DNL .fin] worden verwerkt.

## Kan ik extra gebeurtenissen aan het geproduceerde malplaatje toevoegen of ben ik beperkt tot drie? {#template}

U kunt zoveel gebeurtenissen toevoegen als u wilt. De wizard staat echter slechts drie gebeurtenissen toe. Nadat het sjabloonbestand is gemaakt, kunt u naar wens meer gebeurtenissen toevoegen.

## Wat gebeurt er met een gegevensbronbestand waarbij een of meer records niet hetzelfde aantal kolommen hebben als de headerrecord? {#header}

Als u een Gegevensbrondossier hebt waar één of meerdere verslagen niet het zelfde aantal kolommen zoals kopbalverslag hebben, zal het volgende voorkomen.

* Er wordt een e-mail verzonden naar de maker van de gegevensbron, waarin deze op de hoogte wordt gesteld van een fout.
* Het bestand wordt niet verwerkt omdat de kolommen niet overeenkomen.

## Is de informatie van Gegevensbronnen omhoog opgerold? {#rollup}

Gegevensbroninformatie kan worden opgerold; De klantenservice van Adobe moet de rollup echter vanaf de historische datum opnieuw verwerken om de historische gegevens op te nemen. Als de huidige datum bijvoorbeeld 31 oktober 2015 is en u gegevens voor 1-15 augustus 2015 uploadt met behulp van gegevensbronnen, moet de rollup worden ingesteld om vanaf 1 augustus 2015 opnieuw te worden verwerkt, zodat de nieuw geïmporteerde gegevens worden opgenomen.

Merk ook op dat de gegevens niet direct in een het rapportreeks van de rollup gebruikend Gegevensbronnen zouden moeten worden geupload. Als u deze gegevens in een rollup moet opnemen, moet u deze importeren in een standaard rapportsuite, ook wel een *`child suite`* naar de rollup. Neem contact op met de klantenservice van Adobe voor meer informatie.

## Waarom toont het Rapport van de Weergaven van de Pagina geen gegevens van Gegevensbronnen voor één enkele dag, maar het toont de correcte gegevens voor een week? {#week}

Gegevensbronnen rapporteren geen gegevens per uur. Wanneer u probeert om een rapport voor een bepaalde dag in werking te stellen, kunnen de gegevens slechts tegen het uur worden verdeeld zodat toont niets in het rapport. U kunt gegevens slechts zien wanneer het door een niveau van granulariteit van dagelijks of hoger wordt verdeeld, dat door een wekelijks of maandrapport in werking te stellen kan worden verwezenlijkt.

## Hoe worden de Unieke Bezoekers berekend in een Bron van de Bron van het Logboek van de Webserver uploadt? {#unique}

Het aantal unieke bezoekers in een webserverlogboek wordt berekend als de verschillende combinaties van *`IP Address`* en *`User Agent`* in het weblogbestand. Elke unieke combinatie van deze twee items wordt berekend als een unieke bezoeker. Als de [!UICONTROL User Agent] de kolom is leeg (of niet inbegrepen in het Weblogboek) dan kunnen wij de Unieke tellingen van de Bezoeker niet identificeren, en het volledige uploaden zal tellen als enkel één Unieke Bezoeker (zelfs als er veelvoudige IP adressen zijn).

## In Gegevensbronnen, hoe kan ik zien welke login tot welke rapportreeks behoort? {#login}

In Gegevensbronnen, is identiteitskaart van de rapportreeks het eerste deel van login die door een willekeurig aantal wordt toegevoegd dat de specifieke gegevensbron identificeert die opstelling was. Bijvoorbeeld, `RSID-drmossdev5 Login-drmossdev5_0001343430`.

## Hoe beïnvloeden versie 15 en segmentatie gegevensbronnen? {#segmentation}

In versie 15, gedragen de Gegevensbronnen zich verschillend gebaseerd op het brontype:

* Volledige gegevensbronnen voor verwerking, weblogbestanden en transactie-id&#39;s worden normaal weergegeven. Wanneer de segmenten worden toegepast, worden de gegevens gefiltreerd volgens de segmentregels.
* De standaard of omzettingsgegevensbronnen (advertentiecampagnes, CRM, klantentevredenheid, plaatsprestaties, generieke summiere gegevens, online aankopen, lood en citaten, en off-line kanaalgegevens) verschijnen in versie 15. Omdat deze gegevensbronnen echter niet aan bezoeken of bezoekers zijn gekoppeld, worden ze uitgefilterd wanneer segmenten worden toegepast.

## Zijn metriek die gebruikend een transactieID beschikbaar in de gegevensvoer van de Clickstream en gegevenspakhuis worden ingevoerd? {#clickstream}

De gegevensinvoer bevat alle gegevens van transactie-id&#39;s die zijn ontvangen. Als u echter transactie-id-gegevens uploadt voor een datum in het verleden, kunt u die gegevens alleen ophalen door de gegevensinvoer voor die dag opnieuw te downloaden.

## Zijn eVars die momenteel in het profiel van de Bezoeker blijven toegewezen aan metriek die met gegevensbronnen wordt geüpload? {#visitor}

Nee voor volledige verwerking, ja voor transactie-id. Volledige verwerkingsgegevensbronnen worden verwerkt met behulp van aparte bezoekersprofielen, dus zelfs als de bezoeker-id&#39;s overeenkomen, worden ze vanuit het oogpunt van eVar-toewijzing niet aan elkaar gekoppeld. De gegevensbronnen van transactie-id zijn gekoppeld aan het hoofdbezoekersprofiel, zodat persisterende eVars worden toegewezen aan gebeurtenissen die met transactie-id zijn geüpload.

## Blijven eVars die zijn geüpload met gebruik van gegevensbronnen tot later online gedrag? {#evars}

Nee. eVars die via gegevensbronnen voor transactie-id zijn geüpload, kunnen alleen lezen van de opgeslagen profielgegevens, niet het profiel bijwerken.
Nee. Vars zijn de enige variabelen die in de momentopname van het bezoekersprofiel worden opgeslagen.

## Hoe werken numerieke gebeurtenissen en valutamarkten met gegevensbronnen? {#numeric}

Volledige verwerking biedt alleen ondersteuning voor oudere gebeurtenislijstindelingen, exclusief de waarde voor numerieke gebeurtenissen/valuta&#39;s/tellers (meer dan 1) rechtstreeks in de lijst met gebeurtenissen, dat wil zeggen `"eventNN,eventKK"` niet `"eventNN=#.##"`. Dit betekent dat deze alleen ondersteuning biedt voor een tellergebeurtenis als deze wordt doorgegeven in de kolom Gebeurtenissen in het gegevensbronbestand en dat de waarde met 1 wordt verhoogd.

Als er numerieke, valuta- of tellergebeurtenissen (meer dan 1) vereist zijn, gebruikt u de productlijst:

```js
s.products="Footwear;Running Shoes;1;99.99;event1=4.50";
s.products="Footwear;Running Shoes;1;99.99;event1=4.50|event4=1.99";
```
