---
description: Informatie over de vereisten voor uw rapportreeks alvorens Gegevensbronnen te gebruiken.
subtopic: Data sources
title: Vereisten en uploadlimieten
topic: Developer and implementation
uuid: d79fca77-fa0e-4171-b978-cdee5c67d9df
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Vereisten en uploadlimieten

Informatie over de vereisten voor uw rapportreeks alvorens Gegevensbronnen te gebruiken.

De volgende secties maken een lijst van beperkingen die op Gegevensbronnen en gegevens van toepassing zijn die in marketing rapporten en analyses worden ingevoerd.

* [Groottebeperkingen](/help/import/c-data-sources/datasrc-requirements.md#section_77B06D82CB374FFABD39F7D9A49D8E18)
* [Datums](/help/import/c-data-sources/datasrc-requirements.md#section_2B8E69BA1E0B4DEAB4E2034C2B9E16C2)
* [Algemeen](/help/import/c-data-sources/datasrc-requirements.md#section_1CD337F660484ABDB7D8CAE96FF46ACF)
* [Ondersteuning voor meerdere bytes](/help/import/c-data-sources/datasrc-requirements.md#section_96C8D26B21184C3E839865DB6F23EA22)
* [Weblogbestanden uploaden](/help/import/c-data-sources/datasrc-requirements.md#section_DD736FC971FE45C89AB310BEDC1FE707)

## Groottebeperkingen {#section_77B06D82CB374FFABD39F7D9A49D8E18}

* Elk FTP-account is beperkt tot 50 MB aan totale gegevens voor alle bestanden. De verwerking wordt gepauzeerd als de grootte groter is dan 50 MB en pas wordt hervat als het totaal kleiner is dan 50 MB.

## Datums {#section_2B8E69BA1E0B4DEAB4E2034C2B9E16C2}

* Elke kalenderdag kunt u gegevens uploaden voor 90 unieke datums. Als u deze limiet overschrijdt, mislukt het uploaden en verschijnt er een foutbericht met de mededeling dat u de maximale unieke dagen hebt overschreden.
* Alleen gegevens met huidige of eerdere datums kunnen worden geïmporteerd. Probeer niet om toekomstige data in uw gegevens van Gegevensbronnen te gebruiken.
* Voor alle rijen moet een datum worden opgegeven om mogelijkheden voor het maken van rapporten mogelijk te maken. Als een rij geen datum omvat, produceren de Gegevensbronnen een fout en verwerpt het dossier. De datum-/tijdnotatie verschilt per type gegevensbron:

   * **Volledige gegevensbronnen** voor verwerking: Gebruik de datumnotatie ISO 8601 van `YYYY-MM-DDThh:mm:ss±UTC_offset` (bijvoorbeeld `2013-09-01T12:00:00-07:00`) of Unix Time Format (het aantal seconden dat is verstreken sinds 1 januari 1970).

   * **Gegevensbronnen** voor standaard en integratie: Gebruik de volgende datumnotatie: `MM/DD/YYYY/HH/mm/SS` (bijvoorbeeld `01/01/2013/06/00/00`)

## Algemeen {#section_1CD337F660484ABDB7D8CAE96FF46ACF}

* Wanneer u een Gegevensbrondossier uploadt, voeren de Gegevensbronnen basisgegevensbevestiging uit om ervoor te zorgen het dossier geen het formatteren fouten bevat. Als een fout in een bestand wordt aangetroffen, wordt een e-mailmelding verzonden en wordt de verwerking gestopt.
* Gegevensvelden mogen geen puntkomma&#39;s bevatten. Gegevensbronnen slaan records over die een puntkomma bevatten.
* De gegevens van het Logboek van het Web, het Verkeer, en sommige Generische groeperingen van Gegevensbronnen zijn niet beschikbaar in het Pakhuis van Gegevens of ontdekken. Zie [Gegevenstypen en Categorieën](/help/import/c-data-sources/c-datasrc-types/datasrc-categories.md)voor meer informatie.
* Gegevensbronnen ondersteunen geserialiseerde gebeurtenissen niet.

## Ondersteuning voor meerdere bytes {#section_96C8D26B21184C3E839865DB6F23EA22}

Gegevensbronnen ondersteunen multibyte-codering. De Bronnen van gegevens proberen om het formaat van het inkomende Gegevensbrondossier te ontdekken, en wanneer noodzakelijk, zet het in een gesteund formaat om. In de volgende tabel vindt u een overzicht van veelgebruikte tekenopmaak en hun ondersteuningsstatus.

<table id="table_F9E685D7EEAB49A9ABAD622AE630EC21"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Tekenindeling </th> 
   <th colname="col2" class="entry"> Ondersteuning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> UTF-8 </td> 
   <td colname="col2"> <p>Ondersteund. De rapportreeks die met Gegevensbronnen wordt gebruikt moet toegelaten multibyte karaktersteun hebben. </p> <p>Zie <a href="https://marketing.adobe.com/resources/help/en_US/reference/new_report_suite.html"  > Nieuwe rapportsuite</a> in Help </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> UTF-8 met Byte Order Mark (EF BB BF) </td> 
   <td colname="col2"> <p>Ondersteund. Deze indeling is niet standaard, maar veel Windows-toepassingen worden in deze indeling opgeslagen. </p> <p>WordPad slaat bijvoorbeeld op in deze indeling als u "UTF-8" kiest. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ISO-8859-1 (ook bekend als Latin-1 of Windows-1252) </td> 
   <td colname="col2"> Ondersteund. Microsoft Excel slaat in deze indeling op wanneer u een "door tabs gescheiden" export kiest. De rapportsuite moet de landinstelling ISO-8859-1 gebruiken. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> UTF-16 Little-endian, met Byte Order Mark (FF FE) </td> 
   <td colname="col2"> Omgezet in ISO-8859-1 of UTF-8, zoals bepaald door uw configuratie van de rapportsuite. Microsoft Excel slaat in deze indeling op wanneer u een unicode-export kiest. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> UTF-16 Big-endian, met Byte Order Mark (EF FF) </td> 
   <td colname="col2"> Omgezet in ISO-8859-1 of UTF-8, zoals bepaald door uw configuratie van de rapportsuite. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> UTF-16 zonder byte-orde markering </td> 
   <td colname="col2"> Niet ondersteund. </td> 
  </tr> 
 </tbody> 
</table>

Als u een UTF-8 of ISO-8859-1 dossier indient en uw rapportreeks niet wordt gevormd om het te steunen, één van het volgende gebeurt:

* De fout wordt ontdekt tijdens omzetting, in welk geval u een bericht als &quot;Gevonden slecht karakter in dossier op positie 18 terwijl het omzetten van UTF-8 in ISO-8859-1&quot;ontvangt.
* Het bestand wordt verwerkt zonder fouten, maar er staan onjuiste gegevens in het rapport.

## Weblogbestanden uploaden {#section_DD736FC971FE45C89AB310BEDC1FE707}

* De nuttigste rapporten voor het bekijken van de gegevens van het Logboek van het Web zijn verkeersrapporten, zoals paginameningen.
* Paginanamen worden weergegeven als de volledige URL, inclusief de queryreeks.
* Elk bestandsverzoek wordt weergegeven als een afzonderlijke paginaweergave, inclusief stijlpagina&#39;s en afbeeldingsbestanden.
* Als u informatie aan URL toevoegt, zouden de dossiers als afzonderlijke pagina&#39;s kunnen worden geregistreerd. In marketingrapporten worden bijvoorbeeld de volgende URL&#39;s opgenomen als twee afzonderlijke pagina&#39;s:

[!DNL /jokes/misc/snail_joke.html?userid=12345]

[!DNL /jokes/misc/snail_joke.html?userid=98765]
