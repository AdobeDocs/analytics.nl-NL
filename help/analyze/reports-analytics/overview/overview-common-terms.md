---
description: Een inleiding tot algemeen gebruikte termen van marketinganalyse die in Rapporten & Analytics worden gebruikt.
title: Algemene voorwaarden
uuid: 0560dc7d-9f92-46d4-848b-3cf297073382
feature: Reports & Analytics Basics
role: User, Admin
exl-id: 78ad3e11-2bfa-49bd-b17a-c586701b56ad
source-git-commit: 4ddc2640aa8b3a22411c86ff8bfe0ecf345a3d63
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 3%

---

# Algemene voorwaarden

{{ra-eol}}

Een inleiding op algemeen gebruikte Adobe Analytics termen gebruikt.

<table id="table_58F5D292485F45F9902B372E4E1E3103"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Term </th> 
   <th colname="col2" class="entry"> Definitie </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Rapportsuite </p> </td> 
   <td colname="col2"> <p>Een rapportsuite definieert de volledige, onafhankelijke rapportage op een gekozen website, een set websites of een subset van websitepagina's. Doorgaans is een rapportenpakket één website, maar het kan een globaal segment zijn waar u verscheidene aantallen van plaatsen hebt gecombineerd om totalen te krijgen. Bovendien kan een rapportsuite kleiner zijn dan een website als u rapporten voor een gedeelte van uw site wilt uitvoeren. </p> <p>Bijvoorbeeld, als het programma geopende gebruikers en niet-het programma geopende gebruikers uw plaats verschillend gebruiken, en u verschillende mensen hebt die de rapporten voor elke groep bekijken, kunt u rapportreeksen categoriseren die op pagina's worden gebaseerd die authentificatie en pagina's vereisen die niet. </p> <p>Wanneer u login, selecteert u één rapportreeks aan gebruik (behalve wanneer u roll-ups gebruikt die rapportreeksen combineren). </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Metrisch </p> </td> 
   <td> <p>Kwantitatieve informatie over activiteiten op uw website, zoals Weergaven, Doorklikken, Opnieuw laden, Gemiddelde bestede tijd, Datum, Eenheden, enzovoort. </p> <p>Zie voor meer informatie <a href="/help/analyze/reports-analytics/metrics.md">Metrisch</a>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Dimension </p> </td> 
   <td> <p>Beschrijvingen of kenmerken van metrische gegevens die kunnen worden bekeken en vergeleken, zoals geslacht, maand, leeftijd, loyaliteit, monitorresolutie, etc. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Rapport </p> </td> 
   <td> <p>De basis van de functionaliteit van het marketingrapport. U kunt online rapporten uitvoeren over alle verzamelde gegevens. </p> <p>Zie voor meer informatie <a href="/help/analyze/reports-analytics/reports.md"> Rapporttypen</a>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Paginaweergave </p> </td> 
   <td> <p>Eén webpagina die in de browser van een bezoeker wordt geladen. Een paginaweergave is één uitvoering van het JavaScript voor die pagina. Het systeem telt nauwkeurig hoeveel keer een pagina wordt geladen, zelfs als de bezoeker de pagina regelmatig vernieuwt of de pagina gebruikt <span class="uicontrol"> Vorige</span> en <span class="uicontrol"> Opnieuw laden</span> browserknoppen. Een paginaweergave telt de gehele pagina, niet de afzonderlijke elementen of treffers. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Bezoek </p> </td> 
   <td> <p>Een reeks paginaweergaven tijdens een sessie. Het bezoek eindigt slechts na 30 minuten inactiviteit of na 12 uur ononderbroken activiteit. (Deze tijdmeting is de industriestandaard voor marketinganalyse.) Bezoeken worden bijgehouden door cookies. Een bezoek begint wanneer een kijker tot een pagina toegang heeft. Een bezoek wordt soms aangeduid als een <span class="term"> sessie</span>, maar het is geen browsersessie. Als u naar een andere site gaat, de browser sluit of de computer opnieuw opstart, wordt het bezoek niet beëindigd. </p> <p> Als de time-out bij inactiviteit optreedt terwijl een bezoeker een pagina leest, wordt het bezoek gesloten en verwerkt. Een nieuw bezoek begint wanneer de bezoeker door aan een andere pagina klikt. </p> <p>Als de datum tijdens een bezoek verandert, bijvoorbeeld wanneer u om middernacht een site bezoekt, wordt het bezoek toegeschreven aan de dag waarop het bezoek is begonnen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Unieke bezoeker </p> </td> 
   <td> <p>Unieke bezoekersrapporten geven het aantal verschillende personen aan die uw site gedurende een gekozen tijd bezoeken. Er zijn zes verschillende Unieke Bezoekersrapporten: </p> 
    <ul id="ul_863B8DE8B9E74DE4A93C2C2931EEFB6D"> 
     <li id="li_21C835B71EF64B4DA821B674416C8B85">Uurlijks </li> 
     <li id="li_36A498AE7D7A455C8DEB3AA0F025B597">Dagelijks </li> 
     <li id="li_30F26F8DAC664E1FA823B7BDDB7B0F8B">Wekelijks </li> 
     <li id="li_09263F6B1E114A8DB477793B560A0417">Maandelijks </li> 
     <li id="li_A0B2CA3D44564045B02B55AF6E392F76">Driemaandelijks </li> 
     <li id="li_296BC5B02921460690F35128B1192800">Jaarlijks </li> 
    </ul> <p>Hoewel één persoon uw site meerdere keren kan bezoeken en tijdens een bepaalde periode meerdere pagina's kan bekijken, worden in het rapport Unieke bezoekers die persoon geregistreerd als één unieke bezoeker. </p> <p> <b>Bezoeker deduplicatie</b>: Met gegevensverzameling worden bezoekers gedupliceerd op basis van de rapporttitel, onafhankelijk van de kalenderselectie. Een bezoeker die bijvoorbeeld vier aparte dagen in een rapportweek bezoekt, wordt als één bezoeker in de <span class="wintitle"> Wekelijks uniek bezoekersrapport</span>. In een <span class="wintitle"> Dagelijks uniek bezoekersrapport</span> tijdens die week wordt dezelfde bezoeker vier keer meegeteld . </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Conversiegebeurtenissen (geslaagd) </p> </td> 
   <td> <p>Conversiegebeurtenissen zijn de activiteiten op uw site die u wilt uitvoeren (belangrijke prestatie-indicatoren). Voor een e-commercesite kunnen conversiegebeurtenissen een gedetailleerde productweergave, een kassa of een aankoop zijn. Voor een productielocatie voor leads kan de gebeurtenis een formuliervoltooiing zijn. Conversiegebeurtenissen worden op de site geteld en hebben hun eigen rapporten waaruit blijkt hoeveel van deze gebeurtenissen hebben plaatsgevonden. Deze gebeurtenissen worden ook metriek om in andere rapporten te zetten en kunnen tonen waarom de omzettingsgebeurtenissen plaatsvonden, of wat tot hun het gebeuren bijdroeg. </p> <p>De uitzondering op de regel van één gebeurtenis die één metrisch wordt is de gebeurtenis van de Aankoop, die drie metriek voortbrengt: Ontvangsten, bestellingen en eenheden. </p> <p>Er zijn meer omzettingsmetriek die hier niet worden bepaald, maar omzettingsmetriek vormen de stichting van uw marketing analyses, waarop andere metriek en rapporten worden gebouwd. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Kanaal </p> </td> 
   <td> <p> Gedefinieerde secties of categorieën van uw site. Websites die twee hoofdcategorieën hebben, zoals <span class="term"> weer</span> en <span class="term"> nieuws</span>, twee kanalen hebben. U kunt statistieken groeperen voor alle paginaweergaven die binnen elk kanaal in uw site voorkomen. </p> </td> 
  </tr> 
 </tbody> 
</table>
