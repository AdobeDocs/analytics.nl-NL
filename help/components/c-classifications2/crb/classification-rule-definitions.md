---
description: Definities van interface-elementen op de pagina's in de opbouwfunctie voor classificatieregel.
subtopic: Classifications
title: Classificatieregels - definities
topic: Admin tools
uuid: 77af8669-6e11-435c-9cc3-b03eb627c855
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Classificatieregels - definities

Definities van interface-elementen op de pagina&#39;s in de opbouwfunctie voor classificatieregel.

## Regelpagina {#section_4A5BF384EEEE4994B6DC888339833529}

Op deze pagina worden de regels in een regelset weergegeven.

![](assets/classification_rules_page.png)

**Definities**

<table id="table_2B3A8BB7BDE14836ACA6A1D444B011CD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Selecteer rapportsets en -variabelen </p> </td> 
   <td colname="col2"> <p><b>Rapportsuite</b> </p> <p>Het rapport is geschikt voor de toepassing van de regel. </p> <p><b>Variabele</b> </p> <p>U kunt slechts één variabele toepassen wanneer u een set classificatieregel maakt. Als u veelvoudige regelreeksen voor één variabele wilt tot stand brengen, moet u elke regel toepassen die op veelvoudige rapportreeksen wordt geplaatst. </p> <p>Opmerking: U kunt slechts de variabelen gebruiken u tot in uw rapportreeksen toegang hebt. Variabelen worden pas in het deelvenster <span class="wintitle"> Nieuwe regelset</span> weergegeven nadat voor die variabele ten minste één classificatie is gedefinieerd. </p> <p>Bijvoorbeeld, om Pagina <span class="term"> 's</span> als variabele aan de regelreeks ter beschikking te stellen, zorg ervoor dat de rapportreeks <a href="https://marketing.adobe.com/resources/help/en_US/reference/traffic_classifications.html"  > verkeersclassificaties</a> heeft die voor <span class="term"> Pagina</span>worden uitgevoerd. </p> <p> U kunt classificaties maken voor een variabele in <span class="uicontrol"> Admin</span> &gt; <span class="uicontrol"> Report Suites</span> &gt; <span class="uicontrol"> Traffic</span> &gt; <span class="uicontrol"> Traffic Classifications</span> (of <span class="uicontrol"> Conversion</span> <span class="uicontrol"></span>&gt; Conversion Classifications). Selecteer vervolgens de variabele en klik op <span class="uicontrol"> Classificatie</span>toevoegen. </p> <p>Zie <a href="https://marketing.adobe.com/resources/help/en_US/reference/traffic_classification_admin.html"  > Verkeersklassificaties</a> en <a href="https://marketing.adobe.com/resources/help/en_US/reference/conversion_classifications.html"  > Conversie-classificaties</a> in de Help bij Admin. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="wintitle"> Activeren</span> </p> </td> 
   <td colname="col2"> <p>Valideert en activeert een regel. De actieve regels verwerken dagelijks, onderzoek classificatiegegevens die typisch één maand teruggaan. De regels controleren automatisch op nieuwe waarden en uploaden de classificaties. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="wintitle"> Deactiveren</span> </p> </td> 
   <td colname="col2"> <p>Hiermee deactiveert u de regels, zodat u deze kunt bewerken en testen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Configureer rapportsets en -variabelen </p> </td> 
   <td colname="col2"> <p>Toont de <span class="wintitle"> Beschikbare pagina van de Reeksen</span> van het Rapport, waar u één of meerdere beschikbare rapportreeksen kunt selecteren voor al uw regelreeksen te gebruiken. (Deze pagina wordt ook weergegeven wanneer u de <span class="wintitle"> Classificatieregel Builder</span>voor het eerst uitvoert.) </p> <p>Deze functie is bedoeld om de laadtijd van de rapportsuite te verminderen, voor het geval dat er honderden beschikbare rapportageopensets zijn. </p> <p>De rapportsuites u hier selecteert worden ter beschikking gesteld op het regelniveau, wanneer u klikt <span class="uicontrol"> voeg Correcties</span> toe wanneer het creëren van een regel. </p> <p>Opmerking: Een rapportsuite wordt <span class="term"> alleen</span> beschikbaar wanneer voor de rapportsuite ten minste één classificatie is gedefinieerd voor de variabele in <span class="wintitle"> Admin Tools</span>. <p>(Zie <span class="term"> Variabele</span> in <a href="/help/components/c-classifications2/crb/classification-rule-set.md"  > classificatiereeksen</a> voor een uitleg van deze voorwaarde.) </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Regels overschrijven bestaande waarden </p> </td> 
   <td colname="col2"> <p> (Standaardinstelling) Overschrijf altijd bestaande classificatietoetsen, inclusief classificaties die via de importer (SAINT) zijn geüpload. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Regels overschrijven alleen ongestelde waarden </p> </td> 
   <td colname="col2"> <p>Vul alleen lege (niet-ingestelde) cellen in. Bestaande classificaties worden niet gewijzigd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Venster Opzoeken </p> </td> 
   <td colname="col2"> <p>Wanneer u regels activeert en valideert, kunt u opgeven of de regels bestaande classificaties voor de betreffende toetsen moeten overschrijven. (Dit heeft alleen invloed op geclassificeerde toetsen die eerder binnen de opgegeven tijdsperiode zijn doorgegeven aan <span class="keyword"> Adobe Analytics</span> .) </p> <p>Als u geen <span class="term"> raadplegingsvenster</span>specificeert, kijken de regels ongeveer één maand terug (afhankelijk van huidige dag van de maand.) Bestaande classificaties worden alleen overschreven als u deze optie inschakelt. </p> <p><b>Dev Center</b>: De partners kunnen classificatieregels in het <span class="wintitle"> Dev Centrum</span>tot stand brengen. Deze regels worden opgesteld wanneer de klant een integratie activeert. In het <span class="wintitle"> Dev Centrum</span>, laat de optie <span class="uicontrol"> Overschrijven aangezien</span> de partner specificeren of de klant de overschrijvingswaarde kan bepalen wanneer het activeren van of het uitgeven van een integratie. </p> <p>Zie <a href="/help/components/c-classifications2/crb/classification-quickstart-rules.md"  > hoe de Regels voor meer informatie over regelverwerking worden verwerkt</a> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="/help/components/c-classifications2/crb/classification-quickstart-rules.md"  > Regel toevoegen </a> </td> 
   <td colname="col2"> <p>Hiermee kunt u regels toevoegen aan de regelset. </p> <p>Opmerking:  Als een waarde tweemaal of meer in een reeks regels wordt aangepast, gebruikt het systeem de laatste regel om de waarde te classificeren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Concept</span> </td> 
   <td colname="col2"> Hier kunt u opgeven dat een regel in de conceptmodus is. De status van het ontwerp laat u de regel testen alvorens het in werking te stellen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Dupliceren</span> </td> 
   <td colname="col2"> Dupliceert (kopieert) een regelreeks, zodat u de regel kunt toepassen die aan een andere variabele, of aan de zelfde variabele in een verschillende rapportreeks wordt geplaatst. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="/help/components/c-classifications2/crb/classification-quickstart-rules.md"  > Testregelset </a> </p> </td> 
   <td colname="col2"> <p>Hiermee kunt u de geldigheid van een regelset testen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Overeenkomende voorwaarde</span> </td> 
   <td colname="col2"> Hiermee geeft u de voorwaarden op waaraan de regel moet voldoen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Classificatiehandeling</span> </td> 
   <td colname="col2"> <p>Hiermee geeft u de actie op die moet worden uitgevoerd wanneer de voorwaarde Afstemmen plaatsvindt. </p> <p>U stelt bijvoorbeeld een campagnenaam in op $2, waarmee positie 2 in een trackingcode wordt aangeduid als de naam van de campagne. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> #</span> </td> 
   <td colname="col2"> <p>Het regelnummer. </p> <p>Zie <a href="/help/components/c-classifications2/crb/classification-quickstart-rules.md"  > Hoe regels worden verwerkt</a> voor meer informatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Regeltype selecteren</span> </td> 
   <td colname="col2"> <p>Elke regelset is van toepassing op een specifieke variabele. Geldige selecties zijn: </p> 
    <ul id="ul_6A8E06BB4AF2402B99C215823CB3D59D"> 
     <li id="li_5C702D4F460841D38A59621A5161A3BC">Begint met </li> 
     <li id="li_8052A741D9F34A2FBC136C181600193E">Eindigt met </li> 
     <li id="li_D0FA6EA4F09644FFBC9E6BC568BE80AC">Bevat </li> 
     <li id="li_48675FE5253942ED887C6A72D1DCEF54"> <a href="/help/components/c-classifications2/crb/classification-quickstart-rules.md"  > Gewone uitdrukking </a> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Overeenkomstcriteria invoeren</span> </td> 
   <td colname="col2"> Het tekstpatroon dat u zoekt in een sleutel. Deze criteria kunnen zoektermen, tekens of reguliere expressies zijn. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Classificatie instellen</span> </td> 
   <td colname="col2"> De classificatiekolom die u wilt instellen als aan de criteria wordt voldaan. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Naar</span> </td> 
   <td colname="col2"> De waarde die u voor de geselecteerde classificatiekolom wilt opgeven als aan de criteria wordt voldaan. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Filter </td> 
   <td colname="col2"> Hiermee kunt u naar regels zoeken. </td> 
  </tr> 
 </tbody> 
</table>

## Standaardexpressiepagina {#section_C932A5469E774841B2229965A154163C}

U kunt reguliere expressies op de [!UICONTROL Regular Expression] pagina bewerken.

![](assets/regex_tracking_code.png)

**Definities**

| Element | Beschrijving |
|---|---|
| Voorbeeldtoets | De testtekenreeks die moet worden gebruikt. U kunt bijvoorbeeld een classificatie maken van specifieke tekens in een trackingcode. U kunt bepaalde tekens, woorden of tekenpatronen met elkaar in overeenstemming brengen. |
| Groepen afstemmen | Toont hoe de reguliere expressie overeenkomt met de campagne-id-tekens, zodat u een positie in de campagne-id kunt classificeren. |
| Resultaat afstemmen | Geeft de delen van een tekenreeks weer die overeenkomen met de reguliere expressie. |

Zie [Reguliere expressies in classificatieregels](/help/components/c-classifications2/crb/classification-quickstart-rules.md).

## Testpagina {#section_EC926F97901C4E65901413F9683AA70A}

Met deze pagina kunt u regels in een set testen.

**Definities**

| Element | Beschrijving |
|---|---|
| Test uitvoeren | Wanneer u de regelreeks test, gebruik sleutels van het rapport om te zien hoe zij door de regelreeks zullen worden beïnvloed. |
| Filter | Hiermee filtert u de waarden in het [!UICONTROL Results] deelvenster. |

