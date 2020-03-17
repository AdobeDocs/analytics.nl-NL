---
description: Als u aan het werken met de Bouwer van het Segment in Ad hoc Analyse wordt gebruikt, verklaart dit FAQ wat aan bestaande segmenten en omslagen gebeurt en welke acties u moet nemen.
keywords: segmentation;segments
title: Overgangshandleiding voor ad-hocanalyse
topic: Segments
uuid: d409d71a-f8d9-42a2-add2-37d426cd40d1
translation-type: tm+mt
source-git-commit: ''

---


# Overgangshandleiding voor ad-hocanalyse

Als u aan het werken met de Bouwer van het Segment in Ad hoc Analyse wordt gebruikt, verklaart dit FAQ wat aan bestaande segmenten en omslagen gebeurt en welke acties u moet nemen.

## Functies {#section_BD58629D1A9346BF879E229FA6BEC7A2}

* De segmenten zijn universeel aan alle rapportseries. Eerder, waren de segmenten rapport-reeks specifiek.
* De ad hoc Analyse omvat updates aan de Bouwer van het Segment en een volledige update van de Manager van het Segment.
* U kunt nu segmenten labelen om deze later te ordenen en te doorzoeken in plaats van mappen te gebruiken. Eerder hebt u mappen gebruikt om uw segmenten [!DNL Ad Hoc Analysis] te ordenen.

## Wat gebeurde er met mijn bestaande segmenten? {#section_76CF47142D1A4FB6A0718AD9073049FE}

Uw bestaande segmenten blijven werken zoals voorheen. Om het even welke rapporten die deze toegepaste segmenten hebben zullen blijven correct werken.

De meeste vroegere vooraf bepaalde en reekssegmenten zullen over als segmentmalplaatjes in de segmentbouwer worden gemigreerd. Segmentsjablonen worden gebruikt om snel aangepaste segmenten te maken met een veel voorkomend publiek. De malplaatjes van het segment kunnen niet rechtstreeks op een rapport worden toegepast, maar zij kunnen gemakkelijk aan een douanesegment worden bewaard.

Segmentsjablonen worden gemarkeerd met een speciaal pictogram in Segment Builder.

## Wat gebeurde er met mijn bestaande segmentmappen? {#section_FB04DCF775694E69B761DCA53F301C30}

In plaats van mappen voor ad-hocanalyse gebruikt Segmentbeheer tags. De mapnamen worden automatisch omgezet in tags en deze tags worden toegepast op de respectievelijke segmenten.

## Wat gebeurde met geplande rapporten die toegepaste segmenten hebben? {#section_81D1B215533C46E99E17BAE7A3376FDF}

De geplande rapporten blijven behoorlijk met de segmenten lopen die u bepaalde.

Wanneer u een segment schrapt, blijven de geplande rapporten en de dashboards die dit segment hebben toegepast normaal werken, d.w.z. het segment of dashboard blijft het geschrapte segment gebruiken.

## Wat is een container Actief? Is het anders dan een container voor paginaweergave? {#section_65BBE60A836C4001938830DDA15DC256}

De naam van de container Paginaweergave is gewijzigd in de container Actief om aan te geven dat in deze container alle typen gegevens worden gesegmenteerd, en niet alleen de paginaweergaven. De aanroepen voor het bijhouden van koppelingen en trackhandelingen van de mobiele SDK&#39;s worden bijvoorbeeld allemaal opgenomen of uitgesloten in de aanraakcontainer.

Merk op dat er geen verandering in de manier was deze container werkt, het eenvoudig werd anders genoemd.

## Welke rechten en voorrechten moet ik gebruiken, creëren, en segmenten beheren? {#section_648DFA3A882146C485A84ED014EEC707}

Alle gebruikers kunnen persoonlijke segmenten maken en bewerken. Deze segmenten kunnen rechtstreeks met andere gebruikers van Analytics worden gedeeld. Gebruikers van ad-hocanalyse kunnen de segmenten zien die elk zijn gemaakt en de segmenten die rechtstreeks met de gebruiker worden gedeeld.

In de Verenigde het Webconsole van de Segmentatie, kunnen Admins om het even welk segment uitgeven, en segmenten met groepen en met iedereen in de organisatie delen.

## Kan ik alle segmenten in mijn bedrijf zien? {#section_AC2D328C7410419E80C7C17971CD95B3}

Alle ad-hocanalysesegmenten die u bezit en segmenten die specifiek met u worden gedeeld, worden weergegeven.

## Kan ik alle segmenten Analytics in de Manager van het Segment beheren? {#section_AF5EDD72C74A4739BD40C4AF125CE489}

Bij een ad-hocanalyse worden alleen segmenten weergegeven die door u zijn gemaakt of segmenten die specifiek met u zijn gedeeld. Alleen voor ad-hocanalyse kunt u de Segmentbeheer (Segmenten indelen) gebruiken om ad-hocanalysesegmenten te beheren. Gebruik de Manager van het Segment in Verenigde Segmentatie om alle segmenten van Analytics te beheren.

## Wat zou ik met dubbele segmenten moeten doen die de zelfde naam hebben maar verschillende definities kunnen hebben? {#section_E2C3A1B4B4274D1B86CAA9C0359D049C}

Nu de segmenten in veelvoudige rapportreeksen werken, zou u kunnen vinden dat u veelvoudige segmenten met de zelfde naam hebt. We raden u aan

* Naam wijzigen van segmenten met dezelfde naam, maar met andere definities, of
* Segmenten verwijderen die niet meer nodig zijn.

## Hoe raadt Adobe aan segmenten op te schonen? {#section_3AC2D265F9084557A24C6FB39DC6EE49}

* Label alle segmenten met verouderde tag.
* Bekijk de segmenten die u hebt.
* Voeg deze waar van toepassing toe aan de segmentbibliotheek.
* Goedkeuren van canonieke segmenten.

## Waarom kan ik dit segment niet verwijderen? {#section_0FEB6711031A4ABCA915CDA745ECF38D}

Als het segment is gepubliceerd naar de Experience Cloud, kunt u het niet verwijderen of bewerken. U kunt de gekopieerde versie echter wel kopiëren en bewerken.

## Meer informatie over wat er met uw bestaande segmenten gebeurt {#section_83ACAB256F394DCD8B424D8920BDD853}

<table id="table_0AE814A64D2A48ABB28402C4303F420E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Segmentcategorie </th> 
   <th colname="col2" class="entry"> Wat gebeurt er met deze segmenten? </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Favorietensegmenten in ad-hocanalyse </td> 
   <td colname="col2">Deze ad hoc segmenten van de Analyse worden getoond als regelmatige segmenten in de Analytics van Adobe. <p>Zij zouden niet met de eigenschap van Favorieten in de Manager van het Segment moeten worden verward die u segmenten als favorieten laat merken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Vooraf geconfigureerde segmenten in ad-hocanalyse: 
    <ul id="ul_BBF3C3F4D41A40AF98DA9DA6D299AD03"> 
     <li id="li_B65A004BDF8743FDABCD3332AEB8A010">Bezoeken van één pagina </li> 
     <li id="li_908CF5F964154C9D9EBBAC2A900DCB49">Bezoeken van mobiele apparaten </li> 
     <li id="li_4A715F49AA374463B501D731261A3A4C">Bezoeken van Natuurlijk zoeken </li> 
     <li id="li_67CE51237EC34FD4B33942BA14584EBF">Bezoeken van Betaalde zoekopdracht </li> 
     <li id="li_C3820743178A4E9F9E5E5B5C47401DF2">Bezoeken met cookie van bezoeker-id </li> 
    </ul> </td> 
   <td colname="col2"> <p>Deze segmenten zullen over als segmentmalplaatjes in de segmentbouwer worden gemigreerd. </p> <p>Bestaande rapporten waarop deze segmenten zijn toegepast, blijven correct werken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Experience Cloud (Suite)-segmenten: 
    <ul id="ul_6968AFF6DEDA4BC8A7885B07CC1F57DF"> 
     <li id="li_073D9496F0C64AEB855855D01E65C1BA">Niet-aankoopcentrales </li> 
     <li id="li_8958FD4272A14E16A9AA08216E8BC573">Aankopers </li> 
     <li id="li_1436D7C9651D4AC38E10662DEDDD2B95">Eerste bezoeken </li> 
     <li id="li_69F42B4F6107407792B0014804A8AF7B">Bezoeken van sociale sites </li> 
     <li id="li_29CA111186BE475C943E9F8450BDE8C8">Bezoeken van meer dan 10 minuten* </li> 
     <li id="li_1FEF207959DC4D2E9FC925DD43177AA0">Bezoeken met 5+ vorige bezoeken* </li> 
     <li id="li_219AB1D4FD7E469C9076A23D2CCC7C2C">Bezoeken van Facebook* </li> 
    </ul> </td> 
   <td colname="col2"> <p> De meeste van deze segmenten (met uitzondering van de segmenten die met een asterisk * zijn gemarkeerd) worden als segmentsjablonen gemigreerd naar de segmentbuilder. Bovendien zijn verscheidene nieuwe segmentmalplaatjes toegevoegd. </p> <p>Bestaande rapporten waarop deze segmenten zijn toegepast, blijven correct werken. </p> </td> 
  </tr> 
 </tbody> 
</table>

