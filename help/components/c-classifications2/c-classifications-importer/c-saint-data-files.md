---
description: Met de importer kunt u classificatiegegevens bulksgewijs uploaden naar analytische rapportage in een bestand. Voor het importeren van gegevens is een specifieke bestandsindeling vereist.
subtopic: Classifications
title: Classificatiegegevensbestanden
topic: Admin tools
uuid: f27bb812-56e0-472a-9993-d869f0fea700
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Classificatiegegevensbestanden

Met de importer kunt u classificatiegegevens bulksgewijs uploaden naar analytische rapportage in een bestand. Voor het importeren van gegevens is een specifieke bestandsindeling vereist.

Als u geldige gegevensbestanden wilt maken, kunt u een sjabloonbestand downloaden dat een bestandsstructuur biedt waarin u de classificatiegegevens kunt plakken. Zie [Classificatiesjabloon](/help/components/c-classifications2/c-classifications-importer/c-download-saint-data.md)downloaden voor meer informatie.

Zie [Algemene bestandsstructuur](/help/components/c-classifications2/c-classifications-importer/c-saint-data-files.md) voor meer informatie over tekenbeperkingen in classificaties.

Zie [Numerieke 2 classificaties](/help/components/c-classifications2/c-numeric-2/c-numeric-2-classifications.md) voor informatie over het uploaden van gegevens met numerieke 2 classificaties.

## Algemene bestandsstructuur

De volgende illustratie is een bestand met voorbeeldgegevens:

![](assets/completed-saint-file.png)

Een gegevensbestand moet aan de volgende structuurregels voldoen:

* Classificaties kunnen geen waarde 0 (nul) hebben.
* Adobe raadt u aan het aantal kolommen voor importeren en exporteren te beperken tot 30.
* Geüploade bestanden moeten UTF-8 gebruiken zonder BOM-tekencodering.
* Speciale tekens, zoals tabs, nieuwe regels en aanhalingstekens, kunnen in een cel worden ingesloten, op voorwaarde dat de bestandsindeling v2.1 is opgegeven en de cel op de juiste wijze is [beschermd](/help/components/c-classifications2/c-classifications-importer/t-classifications-escape-data.md). Speciale tekens zijn:

   ```
   \t     tab character 
   \r     form feed character 
   \n    newline character 
   "       double quote
   ```

   De komma is geen speciaal teken.

* Classificaties kunnen geen invoegpunt (^) bevatten omdat dit teken wordt gebruikt om een subclassificatie aan te duiden.
* Wees voorzichtig met het gebruik van een afbreekstreepje. Als u bijvoorbeeld een afbreekstreepje (-) gebruikt in een sociale term, wordt het afbreekstreepje herkend als een [!DNL Not] operator (het minteken). Als u bijvoorbeeld *`fragrance-free`* als een term opgeeft met behulp van de import, wordt de term &#39;geurvrij&#39; herkend en worden publicaties verzameld die *`minus`* wel, maar niet *`fragrance`**`free`*.
* De grenzen van het karakter worden afgedwongen om rapportgegevens te classificeren. Als u bijvoorbeeld een tekstbestand voor classificaties uploadt voor producten ( *`s.products`*) met productnamen van meer dan 100 tekens (bytes), worden de producten niet weergegeven in de rapportage. Met volgcodes en alle aangepaste conversievariabelen (eVars) zijn 255 bytes mogelijk.
* Door tabs gescheiden gegevensbestand (maak het sjabloonbestand met een spreadsheettoepassing of teksteditor).
* Een [!DNL .tab] of [!DNL .txt] bestandsextensie.
* Een hekje (#) identificeert de lijn als gebruikerscommentaar. Adobe negeert elke regel die begint met #.
* Een dubbel-pond teken dat door Sc wordt gevolgd (## SC) identificeert de lijn als pre-verwerkings kopbalcommentaar dat door het melden wordt gebruikt. Verwijder deze regels niet.
* De uitvoer van de classificatie kan dubbele sleutels hebben toe te schrijven aan newline karakters in de sleutel. In een FTP- of browserexport kan dit worden opgelost door aanhalingstekens voor de FTP-account in te schakelen. Hiermee plaatst u aanhalingstekens rondom elke toets met nieuwe-regeltekens.
* Cel C1 in de eerste regel van het importbestand bevat een versie-id die bepaalt hoe classificaties het gebruik van aanhalingstekens gedurende de rest van het bestand verwerken.

   * v2.0 negeert aanhalingstekens en gaat ervan uit dat deze allemaal deel uitmaken van de opgegeven sleutels en waarden. Neem bijvoorbeeld de volgende waarde: &quot;Dit is &quot;&quot;wat waarde&quot;&quot;&quot;. v2.0 interpreteert dit letterlijk als: &quot;Dit is &quot;&quot;wat waarde&quot;&quot;&quot;.
   * v2.1 geeft classificaties de opdracht aan te nemen dat aanhalingstekens deel uitmaken van de bestandsindeling die wordt gebruikt in Excel-bestanden. In v2.1 wordt het bovenstaande voorbeeld geformatteerd op: Dit is &quot;wat waarde&quot;.
   * Er kunnen problemen optreden wanneer v2.1 in het bestand is opgegeven, maar wat eigenlijk wordt gewild, is v2.0, namelijk wanneer aanhalingstekens worden gebruikt op een manier die onder Excel-opmaak niet is toegestaan. Als u bijvoorbeeld een waarde hebt: &quot;VP NO REPS&quot; S/l Dress w/Overlay. Met v2.1 is dit een onjuiste opmaak (de waarde moet worden omgeven door het openen en sluiten van aanhalingstekens en aanhalingstekens die deel uitmaken van de werkelijke waarde, moeten worden omzeild door aanhalingstekens) en classificaties werken niet na dit punt.
   * Voer een van de volgende handelingen uit: Wijzig de bestandsindeling in v2.0 door de koptekst (cel C1) te wijzigen in de bestanden die u uploadt, OF implementeer Excel op de juiste manier door uw bestanden heen.

* De eerste (niet-commentaar) rij van het gegevensbestand bevat de kolomkoppen die worden gebruikt om de classificatiegegevens in die kolom te identificeren. De importeur vereist een specifiek formaat voor kolomkoppen. Zie [Kolomkopindeling](/help/components/c-classifications2/c-classifications-importer/c-saint-data-files.md)voor meer informatie.
* Direct na de koptekstrij in een gegevensbestand staan de gegevensrijen. Elke gegevensregel moet een gegevensveld voor elke kolomkop bevatten.
* Het gegevensbestand ondersteunt de volgende besturingscodes, die door Adobe worden gebruikt om het bestand een structuur te geven en om classificatiegegevens correct te importeren:

<table id="table_0548F2E58B6644208147434EB9B3C21B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> BESTURINGSCODE </th> 
   <th colname="col2" class="entry"> BESCHRIJVING </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>&lt;Nieuwe regel&gt; </p> </td> 
   <td colname="col2"> <p>Een teken voor een nieuwe regel is het enige ondersteunde scheidingsteken tussen gegevensregels/records in het gegevensbestand. Doorgaans hoeft u deze tekens alleen specifiek in te voegen wanneer u een programma schrijft om automatisch gegevensbestanden te genereren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>~autogen~ </p> </td> 
   <td colname="col2"> <p>Verzoekt dat Adobe automatisch een unieke id voor dit element genereert. </p> <p>In de context van de campagne, instrueert deze controlewaarde Adobe om een herkenningsteken aan elk creatief element toe te wijzen. Zie <a href="/help/components/c-classifications2/c-classifications-importer/c-saint-data-files.md"  > Sleutel </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>~punt~ </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u aan dat de gegevenskolom het datumbereik vertegenwoordigt dat aan het item is gekoppeld. Zie <a href="/help/components/c-classifications2/c-classifications-importer/c-saint-data-files.md"  > Datum </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Leeg veld </p> </td> 
   <td colname="col2"> <p>Geeft een NULL-waarde aan voor het huidige veld. Gebruik dit als een bepaalde gegevenskolom niet van toepassing is op de huidige record. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>PER Modifiers </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u aan dat de gegevenskolom een <span class="wintitle"> veld PER Modifier </span> vertegenwoordigt. Zie <a href="/help/components/c-classifications2/c-classifications-importer/c-saint-data-files.md"  > PER Modifier-koppen </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!MORELIKETHIS]
>
>* [Veelvoorkomende uploadproblemen](https://helpx.adobe.com/analytics/kb/common-saint-upload-issues.html)


## Indeling kolomkop

>[!NOTE] Adobe raadt u aan het aantal kolommen voor importeren en exporteren te beperken tot 30.

Indelingsbestanden ondersteunen de volgende kolomkoppen:

### Sleutel

Elke waarde moet uniek zijn in het hele systeem. De waarde op dit gebied beantwoordt aan een waarde die aan de [!DNL Analytics] variabele in het [!DNL JavaScript] baken van uw Website wordt toegewezen. De gegevens in deze kolom zouden ~autogen~ of een andere unieke het volgen code kunnen omvatten.

### Rubriekskolom

Rapporten en analyses bevatten bijvoorbeeld automatisch twee classificaties voor [!UICONTROL Campaign] variabelen: [!UICONTROL Campaigns] en [!UICONTROL Creative Elements]. Om gegevens aan de [!UICONTROL Campaigns] classificatie toe te voegen, zou de kolomrubriek in het dossier van classificatiegegevens zijn [!UICONTROL Campaigns].

>[!NOTE] De waarden in de [!UICONTROL Classifications] kolomkop moeten exact overeenkomen met de naamgevingsconventie van de classificatie, anders mislukt het importeren. Als de beheerder bijvoorbeeld verandert in [!UICONTROL Campaigns] de [!UICONTROL Internal Campaign Names] [!UICONTROL Campaign Set-up Manager]kop van de bestandskolom, moet deze veranderen.

Bovendien ondersteunt het gegevensbestand de volgende extra kopconventies om subclassificaties en andere gespecialiseerde gegevenskolommen te identificeren:

### Subclassificatielijn

Dit [!UICONTROL Campaigns^Owner] is bijvoorbeeld een kolomkop voor de kolom die [!UICONTROL Campaign Owner] waarden bevat. Evenzo [!UICONTROL Creative Elements^Size] is dit een kolomkop voor de kolom die de [!UICONTROL Size] subclassificatie van de [!UICONTROL Creative Elements] indeling bevat.

### Metrische posten indelen

Verwijst bijvoorbeeld [!UICONTROL Campaigns^~Cost] naar de [!UICONTROL Cost] metrische waarde in de [!UICONTROL Campaigns] classificatie.

### kop PER modifier

*`Per Modifier`* de rubrieken worden aangegeven door toevoeging *`~per`* aan de metrische post van de classificatie. Als de *`Metric`* kop bijvoorbeeld *`Campaigns^~Cost`* is, is de kop PER-modifier *`Campaigns^~Cost~per`*. Adobe ondersteunt de volgende *`PER Modifier`* trefwoorden:

Deze tekens hebben een speciale betekenis in een gegevensbestand. Gebruik deze woorden waar mogelijk niet in kenmerknamen en -gegevens.

**VAST:** Vaste waarde. Voer geen schaling uit.

**DAG:** Vermenigvuldig de waarde met het aantal dagen in het rapport.

**VOLGORDE:** Vermenigvuldig de waarde met het aantal orden voor het lijnpunt in het rapport.

**UITCHECKEN:** Vermenigvuldig de waarde met het aantal controles voor het lijnpunt in het rapport.

**EENHEID:** Vermenigvuldig de waarde met het aantal eenheden voor het lijnpunt in het rapport.

**ONTVANGSTEN:** Vermenigvuldig de waarde met het inkomstenbedrag voor de post van het rapport.

**SCADD:** Vermenigvuldig de waarde met het aantal tijden de [!UICONTROL Shopping Cart Add] gebeurtenis per lijnpunt in het rapport werd geroepen.

**SCHUIVEN:** Vermenigvuldig de waarde met het aantal tijden de [!UICONTROL Shopping Cart Remove] gebeurtenis per lijnpunt in het rapport werd geroepen.

**INSTANTIE:** Vermenigvuldig de waarde met het aantal instanties voor het lijnpunt in het rapport.

**KLIK OP:** Vermenigvuldig de waarde met het aantal klikken voor het lijnpunt in het rapport.

**GEBEURTENIS:** Vermenigvuldig de waarde met het aantal tijden de gespecificeerde douanegebeurtenis per lijnpunt van het rapport voorkwam.

**Voorbeeld:** Als Campagne A $10.000 kostte, bevat de [!UICONTROL Campaigns^~Cost] kolom een waarde van 10000 en de [!UICONTROL Campaigns^~~kolom van de Koopper] bevat [!UICONTROL FIXED]. Wanneer het tonen van de Kosten voor Campagne A in de rapporten, zult u $10.000 als vaste kosten voor Campagne A voor de datumwaaier zien.

**Voorbeeld:** Als Campagne B die ongeveer $2 per klik kost, bevat de [!UICONTROL Campaigns^~Cost] kolom 2 en bevat de **[!UICONTROL Campaigns^~~kolom Kostper]** [!UICONTROL CLICK]. Wanneer Adobe de Kosten voor Campagne B weergeeft in de rapporten, berekent (2 * [aantal klikken]) op de vlucht voor het datumbereik van het rapport. Dit geeft u een totale kostenberekening die op het aantal kliks wordt gebaseerd met Campagne B wordt uitgevoerd.

### Datum

Campagnedatums zijn doorgaans bereiken (begin- en einddatum) die aan afzonderlijke campagnes zijn gekoppeld. Datums moeten worden weergegeven in de notatie JJJJ/MM/DD. Bijvoorbeeld 2013/06/15-2013/06/30.

Zie [Conversie-classificaties](https://marketing.adobe.com/resources/help/en_US/admin/index.html#Conversion%20Classifications)voor meer informatie.

>[!NOTE] In de [!DNL Analytics] onderhoudrelease van 10 mei 2018 is Adobe begonnen de functionaliteit van datums en numerieke classificaties te beperken. Deze classificatietypen zijn verwijderd uit de interfaces Admin en Classification Importer. Er kunnen geen nieuwe datums en numerieke classificaties worden toegevoegd. Bestaande classificaties kunnen nog steeds worden beheerd (geüpload naar, verwijderd) via de standaardclassificatieworkflow en blijven beschikbaar in de rapportage.

## Datums gebruiken in combinatie met [!UICONTROL classifications]{#section_966A07B228CD4643B258E73FB8BA150A}

[!UICONTROL Classifications] U kunt datumbereiken toewijzen aan uw campagnes of andere conversie [!UICONTROL classifications], zodat de campagne nauwkeuriger kan worden gemeten. Nadat u het datumbereik van een waarde hebt opgegeven, worden eventuele overeenkomende waarden die buiten het datumbereik vallen, niet geclassificeerd. Dit is handig voor het meten van campagnes die de exacte datums willen gebruiken waarop een campagne Live is geweest, en niet alle resultaten die overeenkomen met de campagne zelf. Als u een waarde met een datumbereik wilt classificeren, moet u aan het volgende voldoen:

* De variabele [!UICONTROL classification] moet gebaseerd zijn op een conversievariabele.
* Het [!UICONTROL classification] gebruikte bestand moet zijn ingesteld op Datum/Ingeschakeld of Numeriek 2.
* Het betrokken datumbereik moet een begindatum en (optioneel) een einddatum bevatten.

Campagnes classificeren op basis van datumbereik:

1. Meld u aan bij [!DNL Analytics] en ga naar Beheer > Classificaties.
1. Klik op het **[!UICONTROL Browser Export]** tabblad, controleer of de instellingen voor de classificatie waarvoor de datum is ingeschakeld correct zijn en klik vervolgens op Bestand exporteren.
1. Open dit bestand in Microsoft Excel of een andere spreadsheet-editor waarmee u bekend bent.
1. Een van de kolommen eindigt met

   ^~punt~dat de kolom is waarin het datumbereik moet worden ingevoerd.
1. Voer onder deze kolom het datumbereik van elke waarde in de volgende notatie in:

   `YYYY/MM/DD - YYYY/MM/DD`. Controleer het volgende:

   * Laat de spaties aan beide zijden van het streepje staan.
   * Gebruik een afbreekstreepje (-) om bereiken te scheiden, niet een en-streepje of een em-streepje.
   * Als de maand of dag één cijfer is, is er een voorloopnul.
   * Er is een begindatumbereik. het einddatumbereik is optioneel.

1. Sla het bestand op en upload het naar [!DNL Analytics] Beheer| Classificaties| Bestand importeren.

>[!NOTE] Een specifieke sleutelwaarde kan niet meer dan één datumbereik hebben.

## Problemen met classificaties oplossen

* [Veelvoorkomende uploadproblemen](https://helpx.adobe.com/analytics/kb/common-saint-upload-issues.html): Het artikel van de Kennisbank dat kwesties beschrijft die uit onjuiste dossierformaten en dossierinhoud voortvloeien.

