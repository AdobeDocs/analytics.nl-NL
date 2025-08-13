---
description: Met de importer kunt u classificatiegegevens bulksgewijs uploaden naar analytische rapportage in een bestand. Voor het importeren van gegevens is een specifieke bestandsindeling vereist.
title: Classificatiegegevensbestanden
feature: Classifications
exl-id: aa919a03-d461-4d12-adc1-6441fb467e63
source-git-commit: 4eea524bf95c9b6bc9ddc878c8c433bc1e60daee
workflow-type: tm+mt
source-wordcount: '1024'
ht-degree: 0%

---

# Classificatiegegevensbestanden (verouderd)

{{classification-importer-deprecation}}

Met de importer kunt u classificatiegegevens bulksgewijs uploaden naar analytische rapportage in een bestand. Voor het importeren van gegevens is een specifieke bestandsindeling vereist.

Als u geldige gegevensbestanden wilt maken, kunt u een sjabloonbestand downloaden dat een bestandsstructuur biedt waarin u de classificatiegegevens kunt plakken. Voor meer informatie, zie [ Malplaatje van de Classificaties van de Download ](/help/components/classifications/importer/c-download-saint-data.md).

Zie [ Algemene Structuur van het Dossier ](/help/components/classifications/importer/c-saint-data-files.md) voor meer informatie over karaktergrenzen in classificaties.

## Algemene bestandsstructuur

De volgende illustratie is een bestand met voorbeeldgegevens:

![](assets/completed-saint-file.png)

Een gegevensbestand moet aan de volgende structuurregels voldoen:

* Classificaties kunnen geen waarde 0 (nul) hebben.
* Adobe raadt u aan het aantal import- en exportkolommen te beperken tot 30.
* Geüploade bestanden moeten UTF-8 gebruiken zonder BOM-tekencodering.
* De speciale karakters, zoals lusjes, newlines, en citaten kunnen binnen een cel worden ingebed op voorwaarde dat het v2.1- dossierformaat wordt gespecificeerd en de cel behoorlijk [ ontsnapt ](/help/components/classifications/importer/importer-faq.md) is. Speciale tekens zijn:

  ```text
  \t     tab character 
  \r     form feed character 
  \n    newline character 
  "       double quote
  ```

  De komma is geen speciaal teken.

* Indelingsnamen mogen geen invoegpunt (^) bevatten, omdat dit teken wordt gebruikt om een subclassificatie aan te duiden.
* Wees voorzichtig met het gebruik van een afbreekstreepje. Als u bijvoorbeeld een afbreekstreepje (-) gebruikt in een sociale term, wordt het afbreekstreepje herkend als een [!DNL Not] -operator (het minteken). Als u bijvoorbeeld *`fragrance-free`* opgeeft als een term die gebruikmaakt van import, herkent Social de term als geurstof *`minus`* free en worden posts verzameld die *`fragrance`* wel, maar niet *`free`* vermelden.
* De grenzen van het karakter worden afgedwongen om rapportgegevens te classificeren. Als u bijvoorbeeld een tekstbestand voor classificaties uploadt voor producten ( *`s.products`*) met productnamen van meer dan 100 tekens (bytes), worden de producten niet weergegeven in de rapportage. Met volgcodes en alle aangepaste conversievariabelen (eVars) zijn 255 bytes mogelijk. Dit beleid is ook van toepassing op de waarden van classificatiekolom en subclassificatiekolom, waarvoor dezelfde limiet van 255 bytes geldt.
* Door tabs gescheiden gegevensbestand (maak het sjabloonbestand met een spreadsheettoepassing of teksteditor).
* Een `.tab` - of `.txt` -bestandsextensie.
* Een hekje (#) identificeert de lijn als gebruikerscommentaar. Adobe negeert regels die beginnen met #.
* Een dubbel-pond teken dat door Sc wordt gevolgd (`## SC`) identificeert de lijn als pre-verwerkings kopbalcommentaar dat door het melden wordt gebruikt. Verwijder deze regels niet.
* De uitvoer van de classificatie kan dubbele sleutels hebben toe te schrijven aan newline karakters in de sleutel. In een FTP- of browserexport kan dit worden opgelost door aanhalingstekens voor de FTP-account in te schakelen. Hiermee plaatst u aanhalingstekens rondom elke toets met nieuwe-regeltekens.
* Cel C1 in de eerste regel van het importbestand bevat een versie-id die bepaalt hoe classificaties het gebruik van aanhalingstekens gedurende de rest van het bestand verwerken.

   * v2.0 negeert aanhalingstekens en gaat ervan uit dat deze allemaal deel uitmaken van de opgegeven sleutels en waarden. Neem bijvoorbeeld de volgende waarde: &quot;Dit is &quot;&quot;een waarde&quot;&quot;&quot;. v2.0 interpreteert dit letterlijk als: &quot;Dit is &quot;&quot;wat waarde&quot;&quot;&quot;.
   * v2.1 geeft classificaties de opdracht aan te nemen dat aanhalingstekens deel uitmaken van de bestandsindeling die wordt gebruikt in Excel-bestanden. Dus v2.1 zou het bovenstaande voorbeeld opmaken naar: Dit is &quot;een waarde&quot;.
   * Er kunnen problemen optreden wanneer v2.1 in het bestand is opgegeven, maar wat eigenlijk wordt gewild, is v2.0, namelijk wanneer aanhalingstekens worden gebruikt op een manier die onder Excel-opmaak niet is toegestaan. Als u bijvoorbeeld een waarde hebt: &quot;VP NO REPS&quot; S/l Dress met Bedekking. Met v2.1 is dit een onjuiste opmaak (de waarde moet worden omgeven door het openen en sluiten van aanhalingstekens en aanhalingstekens die deel uitmaken van de werkelijke waarde, moeten worden omzeild door aanhalingstekens) en classificaties werken niet na dit punt.
   * Zorg ervoor dat u een van de volgende handelingen uitvoert: wijzig de bestandsindeling in v2.0 door de koptekst (cel C1) te wijzigen in de bestanden die u uploadt, OF implementeer Excel door de bestanden heen.

* De eerste (niet-commentaar) rij van het gegevensbestand bevat de kolomkoppen die worden gebruikt om de classificatiegegevens in die kolom te identificeren. De importeur vereist een specifiek formaat voor kolomkoppen. Voor meer informatie, zie [ het Formaat van de Kop van de Kolom ](/help/components/classifications/importer/c-saint-data-files.md).
* Direct na de koptekstrij in een gegevensbestand staan de gegevensrijen. Elke gegevensregel moet een gegevensveld voor elke kolomkop bevatten.
* Het gegevensbestand ondersteunt de volgende besturingscodes, die Adobe gebruikt om het bestand een structuur te geven en classificatiegegevens correct te importeren:

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
   <td colname="col2"> <p>Verzoekt dat Adobe automatisch een unieke id voor dit element genereert. </p> <p>In de campagnecontext, instrueert deze controlewaarde Adobe om een herkenningsteken aan elk creatief element toe te wijzen. Zie <a href="/help/components/classifications/importer/c-saint-data-files.md"  > Sleutel </a> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>~punt~ </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u aan dat de gegevenskolom het datumbereik vertegenwoordigt dat aan het item is gekoppeld. Zie <a href="/help/components/classifications/importer/c-saint-data-files.md"  > Datum </a> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Leeg veld </p> </td> 
   <td colname="col2"> <p>Geeft een NULL-waarde aan voor het huidige veld. Gebruik dit als een bepaalde gegevenskolom niet van toepassing is op de huidige record. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>PER Modifiers </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u aan dat de gegevenskolom een veld <span class="wintitle"> PER Modifier </span> vertegenwoordigt. Zie <a href="/help/components/classifications/importer/c-saint-data-files.md"  > PER Modifier-koppen </a> . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Indeling kolomkop

>[!NOTE]
>
>Adobe raadt u aan het aantal import- en exportkolommen te beperken tot 30.

Indelingsbestanden ondersteunen de volgende kolomkoppen:

### Sleutel

Elke waarde moet uniek zijn in het hele systeem. De waarde in dit veld komt overeen met een waarde die is toegewezen aan de variabele [!DNL Analytics] in het [!DNL JavaScript] -baken van uw website. De gegevens in deze kolom zouden ~ autogen ~ of een andere unieke volgende code kunnen omvatten.

### Rubriekskolom

>[!NOTE]
>
>De waarden in de kolomkop [!UICONTROL Classifications] moeten exact overeenkomen met de naamgevingsconventie van de classificatie, anders mislukt het importeren. Als de beheerder bijvoorbeeld [!UICONTROL Campaigns] in [!UICONTROL Internal Campaign Names] in de [!UICONTROL Campaign Set-up Manager] verandert, moet de kop van de bestandskolom worden aangepast. &quot;Key&quot; is een gereserveerde indelingswaarde (header). Nieuwe classificaties met de naam &quot;Key&quot; worden niet ondersteund.

Bovendien ondersteunt het gegevensbestand de volgende extra kopconventies om subclassificaties en andere gespecialiseerde gegevenskolommen te identificeren:

### Subclassificatiepost

`Campaigns^Owner` is bijvoorbeeld een kolomkop voor de kolom die `Campaign Owner` -waarden bevat. Op dezelfde manier is `Creative Elements^Size` een kolomkop voor de kolom die de `Size` subclassificatie van de `Creative Elements` -classificatie bevat.

## Problemen met classificaties oplossen

* [ Gemeenschappelijke upload Kwesties ](https://helpx.adobe.com/analytics/kb/common-saint-upload-issues.html): Het artikel van de Kennisbank dat kwesties beschrijft die uit onjuiste dossierformaten en dossierinhoud voortvloeien.
