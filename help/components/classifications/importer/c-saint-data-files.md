---
description: Met de importer kunt u classificatiegegevens bulksgewijs uploaden naar analytische rapportage in een bestand. Voor het importeren van gegevens is een specifieke bestandsindeling vereist.
title: Classificatiegegevensbestanden
feature: Classifications
exl-id: aa919a03-d461-4d12-adc1-6441fb467e63
source-git-commit: eb6703dc4079678020954984905ee210cbcbbf8f
workflow-type: tm+mt
source-wordcount: '1746'
ht-degree: 0%

---

# Classificatiegegevensbestanden

Met de importer kunt u classificatiegegevens bulksgewijs uploaden naar analytische rapportage in een bestand. Voor het importeren van gegevens is een specifieke bestandsindeling vereist.

Als u geldige gegevensbestanden wilt maken, kunt u een sjabloonbestand downloaden dat een bestandsstructuur biedt waarin u de classificatiegegevens kunt plakken. Zie voor meer informatie [Classificatiesjabloon downloaden](/help/components/classifications/importer/c-download-saint-data.md).

Zie [Algemene bestandsstructuur](/help/components/classifications/importer/c-saint-data-files.md) voor meer informatie over tekenlimieten in classificaties.

## Algemene bestandsstructuur

De volgende illustratie is een bestand met voorbeeldgegevens:

![](assets/completed-saint-file.png)

Een gegevensbestand moet aan de volgende structuurregels voldoen:

* Classificaties kunnen geen waarde 0 (nul) hebben.
* Adobe raadt u aan het aantal import- en exportkolommen te beperken tot 30.
* Geüploade bestanden moeten UTF-8 gebruiken zonder BOM-tekencodering.
* Speciale tekens, zoals tabs, nieuwe regels en aanhalingstekens, kunnen in een cel worden ingesloten op voorwaarde dat de bestandsindeling v2.1 is opgegeven en de cel juist is [ontsnapt](/help/components/classifications/importer/t-classifications-escape-data.md). Speciale tekens zijn:

  ```text
  \t     tab character 
  \r     form feed character 
  \n    newline character 
  "       double quote
  ```

  De komma is geen speciaal teken.

* Classificaties kunnen geen invoegpunt (^) bevatten omdat dit teken wordt gebruikt om een subclassificatie aan te duiden.
* Wees voorzichtig met het gebruik van een afbreekstreepje. Als u bijvoorbeeld een afbreekstreepje (-) gebruikt in een sociale term, wordt het afbreekstreepje herkend als een [!DNL Not] operator (het minteken). Als u bijvoorbeeld *`fragrance-free`* Als term die de invoer gebruikt, erkent Social de term als geurstof *`minus`* gratis en verzamelt publicaties die *`fragrance`*, maar niet *`free`*.
* De grenzen van het karakter worden afgedwongen om rapportgegevens te classificeren. Als u bijvoorbeeld een tekstbestand voor classificaties uploadt voor producten ( *`s.products`*) met productnamen van meer dan 100 tekens (bytes), worden de producten niet weergegeven in de rapportage. Met volgcodes en alle aangepaste conversievariabelen (eVars) zijn 255 bytes mogelijk. Dit beleid strekt zich ook tot classificatie en sub-classificatie kolomwaarden uit, die aan de zelfde 255 bytelimiet onderworpen zijn.
* Door tabs gescheiden gegevensbestand (maak het sjabloonbestand met een spreadsheettoepassing of teksteditor).
* Ofwel [!DNL .tab] of [!DNL .txt] bestandsextensie.
* Een hekje (#) identificeert de lijn als gebruikerscommentaar. Adobe negeert om het even welke lijn die met # begint.
* Een dubbel-pond teken dat door Sc wordt gevolgd (## SC) identificeert de lijn als pre-verwerkings kopbalcommentaar dat door het melden wordt gebruikt. Verwijder deze regels niet.
* De uitvoer van de classificatie kan dubbele sleutels hebben toe te schrijven aan newline karakters in de sleutel. In een FTP- of browserexport kan dit worden opgelost door aanhalingstekens voor de FTP-account in te schakelen. Hiermee plaatst u aanhalingstekens rondom elke toets met nieuwe-regeltekens.
* Cel C1 in de eerste regel van het importbestand bevat een versie-id die bepaalt hoe classificaties het gebruik van aanhalingstekens gedurende de rest van het bestand verwerken.

   * v2.0 negeert aanhalingstekens en gaat ervan uit dat deze allemaal deel uitmaken van de opgegeven sleutels en waarden. Neem bijvoorbeeld de volgende waarde: &quot;Dit is &quot;&quot;een waarde&quot;&quot;&quot;. v2.0 interpreteert dit letterlijk als: &quot;Dit is &quot;&quot;wat waarde&quot;&quot;&quot;.
   * v2.1 geeft classificaties de opdracht aan te nemen dat aanhalingstekens deel uitmaken van de bestandsindeling die wordt gebruikt in Excel-bestanden. Dus v2.1 zou het bovenstaande voorbeeld opmaken naar: Dit is &quot;een waarde&quot;.
   * Er kunnen problemen optreden wanneer v2.1 in het bestand is opgegeven, maar wat eigenlijk wordt gewild, is v2.0, namelijk wanneer aanhalingstekens worden gebruikt op een manier die onder Excel-opmaak niet is toegestaan. Als u bijvoorbeeld een waarde hebt: &quot;VP NO REPS&quot; S/l Dress met Bedekking. Met v2.1 is dit een onjuiste opmaak (de waarde moet worden omgeven door het openen en sluiten van aanhalingstekens en aanhalingstekens die deel uitmaken van de werkelijke waarde, moeten worden omzeild door aanhalingstekens) en classificaties werken niet na dit punt.
   * Zorg ervoor dat u een van de volgende handelingen uitvoert: wijzig de bestandsindeling in v2.0 door de koptekst (cel C1) te wijzigen in de bestanden die u uploadt, OF implementeer Excel door de bestanden heen.

* De eerste (niet-commentaar) rij van het gegevensbestand bevat de kolomkoppen die worden gebruikt om de classificatiegegevens in die kolom te identificeren. De importeur vereist een specifiek formaat voor kolomkoppen. Zie voor meer informatie [Indeling kolomkop](/help/components/classifications/importer/c-saint-data-files.md).
* Direct na de koptekstrij in een gegevensbestand staan de gegevensrijen. Elke gegevensregel moet een gegevensveld voor elke kolomkop bevatten.
* Het gegevensbestand steunt de volgende controlecodes, die de Adobe gebruikt om structuur aan het dossier te verstrekken, en correct de gegevens van de invoerclassificaties in te voeren:

<table id="table_0548F2E58B6644208147434EB9B3C21B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> BESTURINGSCODE </th> 
   <th colname="col2" class="entry"> BESCHRIJVING </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>&lt;New Line&gt; </p> </td> 
   <td colname="col2"> <p>Een teken voor een nieuwe regel is het enige ondersteunde scheidingsteken tussen gegevensregels/records in het gegevensbestand. Doorgaans hoeft u deze tekens alleen specifiek in te voegen wanneer u een programma schrijft om automatisch gegevensbestanden te genereren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>~autogen~ </p> </td> 
   <td colname="col2"> <p>Verzoekt dat Adobe automatisch een unieke id voor dit element genereert. </p> <p>In de campagnecontext, instrueert deze controlewaarde Adobe om een herkenningsteken aan elk creatief element toe te wijzen. Zie <a href="/help/components/classifications/importer/c-saint-data-files.md"  > Sleutel </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>~punt~ </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u aan dat de gegevenskolom het datumbereik vertegenwoordigt dat aan het item is gekoppeld. Zie <a href="/help/components/classifications/importer/c-saint-data-files.md"  > Datum </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Leeg veld </p> </td> 
   <td colname="col2"> <p>Geeft een NULL-waarde aan voor het huidige veld. Gebruik dit als een bepaalde gegevenskolom niet van toepassing is op de huidige record. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>PER Modifiers </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u aan dat de gegevenskolom een <span class="wintitle"> PER Modifier </span> veld. Zie <a href="/help/components/classifications/importer/c-saint-data-files.md"  > PER Modifier-koppen </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!MORELIKETHIS]
>
>* [Veelvoorkomende uploadproblemen](https://helpx.adobe.com/nl/analytics/kb/common-saint-upload-issues.html)

## Indeling kolomkop

>[!NOTE]
>
>Adobe raadt u aan het aantal import- en exportkolommen te beperken tot 30.

Indelingsbestanden ondersteunen de volgende kolomkoppen:

### Sleutel

Elke waarde moet uniek zijn in het hele systeem. De waarde in dit veld komt overeen met een waarde die is toegewezen aan de [!DNL Analytics] variabele in uw Website [!DNL JavaScript] baken. Gegevens in deze kolom kunnen het volgende bevatten ~autogeen~ of een andere unieke trackingcode.

### Rubriekskolom

>[!NOTE]
>
>De waarden in het dialoogvenster [!UICONTROL Classifications] de kolomkop moet exact overeenkomen met de naamgevingsconventie van de classificatie, anders mislukt het importeren. Bijvoorbeeld als de beheerder verandert [!UICONTROL Campaigns] tot [!UICONTROL Internal Campaign Names] in de [!UICONTROL Campaign Set-up Manager], moet de kop van de bestandskolom worden gewijzigd om overeen te komen. &quot;Key&quot; is een gereserveerde indelingswaarde (header). Nieuwe classificaties met de naam &quot;Key&quot; worden niet ondersteund.

Bovendien ondersteunt het gegevensbestand de volgende extra kopconventies om subclassificaties en andere gespecialiseerde gegevenskolommen te identificeren:

### Subclassificatielijn

Bijvoorbeeld: [!UICONTROL Campaigns^Owner] is een kolomkop voor de kolom die [!UICONTROL Campaign Owner] waarden. Op dezelfde manier [!UICONTROL Creative Elements^Size] is een kolomkop voor de kolom die de [!UICONTROL Size] subclassificatie van de [!UICONTROL Creative Elements] indeling.

### Metrische posten indelen

Bijvoorbeeld: [!UICONTROL Campaigns^~Cost] verwijst naar de [!UICONTROL Cost] metrisch in de [!UICONTROL Campaigns] indeling.

### kop PER modifier

*`Per Modifier`* koppen worden aangeduid door *`~per`* op de metrische post van de indeling. Als de *`Metric`* kop is *`Campaigns^~Cost`*, de kop PER-modificatie is *`Campaigns^~Cost~per`*. Adobe ondersteunt het volgende *`PER Modifier`* trefwoorden:

Deze tekens hebben een speciale betekenis in een gegevensbestand. Gebruik deze woorden waar mogelijk niet in kenmerknamen en -gegevens.

**VAST:** Vaste waarde. Voer geen schaling uit.

**DAG:** Vermenigvuldig de waarde met het aantal dagen in het rapport.

**ORDER:** Vermenigvuldig de waarde met het aantal orden voor het lijnpunt in het rapport.

**UITCHECKEN:** Vermenigvuldig de waarde met het aantal controles voor het lijnpunt in het rapport.

**EENHEID:** Vermenigvuldig de waarde met het aantal eenheden voor het lijnpunt in het rapport.

**ONTVANGSTEN:** Vermenigvuldig de waarde met het inkomstenbedrag voor de post van het rapport.

**SCADD:** Vermenigvuldig de waarde met het aantal keer de [!UICONTROL Shopping Cart Add] gebeurtenis werd geroepen per lijnpunt in het rapport.

**SCHUIVEN:** Vermenigvuldig de waarde met het aantal keer de [!UICONTROL Shopping Cart Remove] gebeurtenis werd geroepen per lijnpunt in het rapport.

**INSTANTIE:** Vermenigvuldig de waarde met het aantal instanties voor het lijnpunt in het rapport.

**KLIK OP:** Vermenigvuldig de waarde met het aantal klikken voor het lijnpunt in het rapport.

**GEBEURTENIS** Vermenigvuldig de waarde met het aantal tijden de gespecificeerde douanegebeurtenis per lijnpunt van het rapport voorkwam.

**Voorbeeld:** Als Campagne A $10.000 kost, [!UICONTROL Campaigns^~Cost] bevat een waarde van 10000 en de [!UICONTROL Campaigns^~Kosten~per] column contains [!UICONTROL FIXED]. Wanneer het tonen van de Kosten voor Campagne A in de rapporten, zult u $10.000 als vaste kosten voor Campagne A voor de datumwaaier zien.

**Voorbeeld:** Als Campagne B die ongeveer $2 per klik kost, [!UICONTROL Campaigns^~Cost] bevat 2 en de **[!UICONTROL Campaigns^~Kosten~per]** column contains [!UICONTROL CLICK]. Wanneer het tonen van de Kosten voor Campagne B in de rapporten, berekent de Adobe (2 &#42; [aantal klikken]) ter plaatse voor het datumbereik van het rapport. Dit geeft u een totale kostenberekening die op het aantal kliks wordt gebaseerd met Campagne B wordt uitgevoerd.

### Datum

Campagnedatums zijn doorgaans bereiken (begin- en einddatum) die aan afzonderlijke campagnes zijn gekoppeld. Datums moeten worden weergegeven in de notatie JJJJ/MM/DD. Bijvoorbeeld 2013/06/15-2013/06/30.

Zie voor meer informatie [Conversie-classificaties](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/conversion-variables/conversion-classifications.html?lang=nl-NL).

>[!NOTE]
>
>In mei 2018 [!DNL Analytics] De onderhoudsversie, Adobe begon de functionaliteit van datum-toegelaten en numerieke classificaties te beperken. Deze classificatietypen zijn verwijderd uit de interfaces Admin en Classification Importer. Er kunnen geen nieuwe datums en numerieke classificaties worden toegevoegd. Bestaande classificaties kunnen nog steeds worden beheerd (geüpload naar, verwijderd) via de standaardclassificatieworkflow en blijven beschikbaar in de rapportage.

## Datums gebruiken in combinatie met [!UICONTROL classifications] {#section_966A07B228CD4643B258E73FB8BA150A}

[!UICONTROL Classifications] kan worden gebruikt om datumbereiken toe te wijzen aan uw campagnes of andere conversie [!UICONTROL classifications], zodat de campagne nauwkeuriger kan worden gemeten. Nadat u het datumbereik van een waarde hebt opgegeven, worden eventuele overeenkomende waarden die buiten het datumbereik vallen, niet geclassificeerd. Dit is handig voor het meten van campagnes die de exacte datums willen gebruiken waarop een campagne Live is geweest, en niet alle resultaten die overeenkomen met de campagne zelf. Als u een waarde met een datumbereik wilt classificeren, moet u aan het volgende voldoen:

* De [!UICONTROL classification] moet gebaseerd zijn op een conversievariabele.
* De [!UICONTROL classification] moet worden ingesteld op Datum-Ingeschakeld of Numeriek 2.
* Het betrokken datumbereik moet een begindatum en (optioneel) een einddatum bevatten.

Campagnes classificeren op datumbereik:

>[!IMPORTANT]
>Deze optie is niet beschikbaar voor rapportsuites die zijn ingeschakeld voor de nieuwe classificatiearchitectuur.

1. Aanmelden bij [!DNL Analytics] en ga naar Beheer > Classificaties.
1. Klik op de knop **[!UICONTROL Browser Export]** , controleert u of de instellingen voor de classificatie waarvoor de datum is ingeschakeld correct zijn en klikt u op Bestand exporteren.
1. Open dit bestand in Microsoft Excel of een andere spreadsheet-editor waarmee u bekend bent.
1. Een van de kolommen eindigt met

   ^~periode~
Dit is de kolom waarin het datumbereik moet worden ingevoerd.
1. Voer onder deze kolom het datumbereik van elke waarde in de volgende notatie in:

   `YYYY/MM/DD - YYYY/MM/DD`. Controleer het volgende:

   * Laat de spaties aan beide zijden van het streepje staan.
   * Gebruik een afbreekstreepje (-) om bereiken te scheiden, niet een en-streepje of een em-streepje.
   * Als de maand of dag één cijfer is, is er een voorloopnul.
   * Er is een begindatumbereik; het einddatumbereik is optioneel.

1. Sla het bestand op en upload het naar [!DNL Analytics] door naar Admin te gaan | Classificaties | Bestand importeren.

>[!NOTE]
>
>Een specifieke sleutelwaarde kan niet meer dan één datumbereik hebben.

## Problemen met classificaties oplossen

* [Veelvoorkomende uploadproblemen](https://helpx.adobe.com/nl/analytics/kb/common-saint-upload-issues.html): Het artikel in de Knowledge Base bevat een beschrijving van problemen die het gevolg zijn van onjuiste bestandsindelingen en bestandsinhoud.
