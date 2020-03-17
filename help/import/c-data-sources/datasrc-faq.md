---
description: Dit onderwerp verstrekt antwoorden op gemeenschappelijke vragen.
subtopic: Data sources
title: Veelgestelde vragen over gegevensbronnen
topic: Developer and implementation
uuid: 394a627f-093c-400a-bfb3-c2aa24568deb
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Veelgestelde vragen over gegevensbronnen

Dit onderwerp verstrekt antwoorden op gemeenschappelijke vragen.

## Hoe kunnen wij off-line gegevens aan online gebeurtenissen binden? {#section_F48A9474A70D4CB8B449DE305F199AD6}

Als u de gegevensbronnen van de transactie-id wilt koppelen aan online gebeurtenissen, moet u de Opname van de Transactie-id inschakelen. Zie Opname [van](/help/import/c-data-sources/datasrc-integrating-offline-data.md#section_30D6D47AEC0F4A36B87EBFE4C858F20C) transactie-id voor meer informatie.

## Hoeveel kost het om de eigenschap van de Gegevensbron te gebruiken? {#section_0B84E3E8891B45E8970EA9D8AAD1ADEC}

De Bronnen van gegevens dragen geen extra kosten voorbij de standaardservervraag. De vraagkosten van de server zijn slechts op volledig-verwerkings gegevensbrontypes van toepassing, waar de individuele klappen binnen als rijen van gegevens worden verzonden. Verkeer en gegevensbronnen op geaggregeerd niveau brengen geen extra kosten met zich mee.

## Hoe neem ik commentaren in de dossiers van Gegevensbronnen op? {#section_AA42152C7B30425EA541A7BA274E78ED}

Elke rij in een Gegevensbrondossier dat met een hekje (#) begint wordt behandeld als commentaar.

## Moet ik een datumkolom in mijn spreadsheetgegevens omvatten? {#section_EA37F5FFB13446C497B3C64943F7084E}

Ja. Omdat vele marketing rapporten van de datumkolom worden gehouden, vereist de Gegevensbronnen een datumkolom.

## Kan ik gegevens opslaan in bestaande variabelen die ik al gebruik? {#section_AB557C2997D04EAFBDC61398B13D13C6}

Adobe raadt u aan nieuwe, ongebruikte variabelen te selecteren om gegevens te importeren met behulp van gegevensbronnen. Neem contact op met de klantenservice als u niet zeker weet wat de configuratie van uw gegevensbestand is of als u meer inzicht wilt krijgen in de risico&#39;s van het opnieuw gebruiken van variabelen.

## Kan ik gegevens schrappen die gebruikend Gegevensbronnen werden ingevoerd? {#section_DB73BC06BD774738BF019B347D9DED96}

Nee. Gegevens die met behulp van gegevensbronnen in rapporten zijn geüpload, kunnen niet worden verwijderd, zelfs niet door Adobe-technici, nadat ze zijn geïmporteerd. Het wordt permanent in uw bestaande gegevens opgenomen, en wordt van uw gegevens die door traditionele gegevensinzamelingsmiddelen (d.w.z. JavaScript, ActionSource, de Invoeging API van Gegevens, enz.) worden ingevoerd. Daarom raadt Adobe ten zeerste aan gegevensbronnen te uploaden naar een testrapportsuite voordat deze in een productieset worden geüpload.

## Hoeveel gegevens kan ik tegelijkertijd importeren? {#section_7A76D59E2C5B434D9BDBD2ABD2873168}

De verwerking wordt gepauzeerd als de grootte groter is dan 50 MB en pas wordt hervat als het totaal kleiner is dan 50 MB. Als u vertragingen bij het genereren van rapporten wilt beperken, mag u niet meer dan 90 dagen gegevens per dag uploaden.

## Wanneer ik gegevens door Gegevensbronnen invoert, worden de bestaande gegevens beschreven? {#section_BDBD16D0AFD54D55AFDB8AC77D35FE77}

De gegevensbronnen van gegevens beschrijven nooit bestaande rapportgegevens. In plaats daarvan, worden de gegevens geupload gebruikend Gegevensbronnen toegevoegd aan de bestaande gegevens.

## Wanneer ik mijn gegevens via Gegevensbronnen upload, waarom krijg ik niet ook mijn metriek? {#section_33176B39744F4F5A861E69AD87B99B78}

Wanneer u de gegevens van Gegevensbronnen uploadt, uploadt u de metriek die in de rapportinterface beschikbaar zal zijn.

Bijvoorbeeld, als u de Ontvangsten van het Centrum van de Vraag voor producten uploadt u op uw plaats verkoopt, kunt u die Ontvangsten van het Centrum van de Vraag in het zelfde rapport hebben zoals Online Ontvangsten. U kunt het echter niet gebruiken in combinatie met Bezoekopdrachten omdat u het aantal bezoeken niet hebt geüpload. Adobe kan alleen de metriek en elementen rapporteren die u via Gegevensbronnen hebt geüpload (naast de standaardmaatstaven voor marketingrapporten).

## Wat gebeurt als ik negatieve waarden in rapportering door Gegevensbronnen overga? {#section_77E5F37F3CFB4407BA32A91E6F3132B2}

De waarde wordt dienovereenkomstig verlaagd.

## Wat is het verschil tussen een Verkeer en een (Generische) Gegevensbron van de Omzetting? {#section_A34C952490814D4FB802F22D9FB3E9F8}

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

## Houden gegevensbronnen rekening met subrelaties, correlaties en paden? {#section_7ABAE2F3C4DD48E18FB8CB20AE8AFD14}

Aangezien het proces van de Gegevensbron (&quot;voor Generische DS, niet-Verkeer&quot;) individuele klappen bouwt die door geheim voorgeheugen worden verwerkt, wordt het subrelatieproces gebruikt, maar niet het correlatieproces. Pathing heeft de mogelijkheid om te worden verwerkt, maar elke hit zou zijn eigen bezoek zijn, dus er wordt geen schilderij gegenereerd. Er worden padgegevens gegenereerd voor weblogimport.

## Zijn de dossieruitbreidingen hoofdlettergevoelig voor een Gegevensbron uploadt of een classificatiedossier? {#section_710787BA4D8C403D8326D666807832B8}

Als de extensies van een uploadbestand voor een gegevensbron of een classificatiebestand met hoofdletters worden weergegeven, worden de bestanden niet verwerkt. Bestandsextensies voor het uploaden van gegevensbron moeten in kleine letters worden weergegeven. Bijvoorbeeld, [!DNL file.TXT] en [!DNL file.FIN] wordt niet verwerkt. Evenzo, [!DNL .TAB] en [!DNL .FIN] zal niet worden verwerkt. Maar [!DNL .txt] en [!DNL .fin] worden verwerkt.

## Kan ik extra gebeurtenissen aan het geproduceerde malplaatje toevoegen of ben ik beperkt tot drie? {#section_F184913926DD43B1872956CED308ADB5}

U kunt zoveel gebeurtenissen toevoegen als u wilt. De wizard staat echter slechts drie gebeurtenissen toe. Nadat het sjabloonbestand is gemaakt, kunt u naar wens meer gebeurtenissen toevoegen.

## Wat gebeurt er met een gegevensbronbestand waarbij een of meer records niet hetzelfde aantal kolommen hebben als de headerrecord? {#section_2666949CB11B49768774C904C93A16D4}

Als u een Gegevensbrondossier hebt waar één of meerdere verslagen niet het zelfde aantal kolommen zoals kopbalverslag hebben, zal het volgende voorkomen.

* Er wordt een e-mail verzonden naar de maker van de gegevensbron, waarin deze op de hoogte wordt gesteld van een fout.
* Het bestand wordt niet verwerkt omdat de kolommen niet overeenkomen.

## Is de informatie van Gegevensbronnen omhoog opgerold? {#section_E0E44C55A84245918E7CF5A4232F5C88}

Gegevensbroninformatie kan worden opgerold; De klantenservice van Adobe moet de rollup echter vanaf de historische datum opnieuw verwerken om de historische gegevens op te nemen. Als de huidige datum bijvoorbeeld 31 oktober 2015 is en u gegevens voor 1-15 augustus 2015 uploadt met behulp van gegevensbronnen, moet de rollup worden ingesteld om vanaf 1 augustus 2015 opnieuw te worden verwerkt, zodat de nieuw geïmporteerde gegevens worden opgenomen.

Merk ook op dat de gegevens niet direct in een het rapportreeks van de rollup gebruikend Gegevensbronnen zouden moeten worden geupload. Als u deze gegevens in een rollup moet opnemen, moet u deze importeren in een standaardrapportenpakket, ook wel een *`child suite`* naar de rollup genoemd. Neem contact op met de klantenservice van Adobe voor meer informatie.

## Waarom toont het Rapport van de Weergaven van de Pagina geen gegevens van Gegevensbronnen voor één enkele dag, maar het toont de correcte gegevens voor een week? {#section_E361A93AFDE1487989B4B0C4438EEDF7}

Gegevensbronnen rapporteren geen gegevens per uur. Wanneer u probeert om een rapport voor een bepaalde dag in werking te stellen, kunnen de gegevens slechts tegen het uur worden verdeeld zodat toont niets in het rapport. U kunt gegevens slechts zien wanneer het door een niveau van granulariteit van dagelijks of hoger wordt verdeeld, dat door een wekelijks of maandrapport in werking te stellen kan worden verwezenlijkt.

## Hoe worden de Unieke Bezoekers berekend in een Bron van de Bron van het Logboek van de Webserver uploadt? {#section_477FEDFD1DBE45278E7D09AFBD59CDAC}

Het aantal Unieke Bezoekers in een web-server logboek wordt berekend als verschillende verschillende combinaties van *`IP Address`* en *`User Agent`* in het logboek van het Web. Elke unieke combinatie van deze twee items wordt berekend als een unieke bezoeker. Als de [!UICONTROL User Agent] kolom leeg is (of niet is opgenomen in het weblogbestand), kunnen we de tellingen van de unieke bezoeker niet identificeren en telt de volledige upload slechts als één unieke bezoeker (zelfs als er meerdere IP-adressen zijn).

## In Gegevensbronnen, hoe kan ik zien welke login tot welke rapportreeks behoort? {#section_8EF9D22D5BE14C218724B06E78EF7DF4}

In Gegevensbronnen, is identiteitskaart van de rapportreeks het eerste deel van login die door een willekeurig aantal wordt toegevoegd dat de specifieke gegevensbron identificeert die opstelling was. Bijvoorbeeld, `RSID-drmossdev5 Login-drmossdev5_0001343430`.

## Hoe beïnvloeden versie 15 en segmentatie gegevensbronnen? {#section_7E9E541DB73C49CDAADC031B678F8678}

In versie 15, gedragen de Gegevensbronnen zich verschillend gebaseerd op het brontype:

* Volledige gegevensbronnen voor verwerking, weblogbestanden en transactie-id&#39;s worden normaal weergegeven. Wanneer de segmenten worden toegepast, worden de gegevens gefiltreerd volgens de segmentregels.
* De standaard of omzettingsgegevensbronnen (advertentiecampagnes, CRM, klantentevredenheid, plaatsprestaties, generieke summiere gegevens, online aankopen, lood en citaten, en off-line kanaalgegevens) verschijnen in versie 15. Omdat deze gegevensbronnen echter niet aan bezoeken of bezoekers zijn gekoppeld, worden ze uitgefilterd wanneer segmenten worden toegepast.

## Zijn metriek die gebruikend een transactieID beschikbaar in de gegevensvoer van de Clickstream en gegevenspakhuis worden ingevoerd? {#section_01CD14CA3E11490CB2CBA433C649029E}

De gegevensinvoer bevat alle gegevens van transactie-id&#39;s die zijn ontvangen. Als u echter transactie-id-gegevens uploadt voor een datum in het verleden, kunt u die gegevens alleen ophalen door de gegevensinvoer voor die dag opnieuw te downloaden.

## Zijn eVars die momenteel in het profiel van de Bezoeker blijven toegewezen aan metriek die met gegevensbronnen wordt geüpload? {#section_1748BD5C6A12467F8082E07D6A9CD595}

Nee voor volledige verwerking, ja voor transactie-id. Volledige verwerkingsgegevensbronnen worden verwerkt met behulp van afzonderlijke bezoekersprofielen, dus zelfs als de bezoeker-id&#39;s overeenkomen, worden ze vanuit een eVar-toewijzingsperspectief niet aan elkaar gekoppeld. De gegevensbronnen van transactie-id zijn gekoppeld aan het hoofdbezoekersprofiel, zodat blijvende eVars worden toegewezen aan gebeurtenissen die met transactie-id zijn geüpload.

## Blijven eVars die zijn geüpload met gebruik van gegevensbronnen tot later online gedrag? {#section_0B490CEAAB604826AFD3E8B2531C8F2D}

Nee. eVars die via gegevensbronnen voor transactie-id zijn geüpload, kunnen alleen lezen van de opgeslagen profielgegevens, niet het profiel bijwerken.
Nee. Vars zijn de enige variabelen die in de momentopname van het bezoekersprofiel worden opgeslagen.
