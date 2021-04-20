---
description: Gebruik de analyse van de Bijdrage om statistische anomalieën en correlaties in gegevens te identificeren.
title: Overzicht van bijdrageanalyse
uuid: 2bd295b0-c5ce-4443-86af-024efd20c021
feature: AI Tools
role: Business Practitioner, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '1161'
ht-degree: 6%

---


# Overzicht van bijdrageanalyse

De Analyse van de bijdrage ontdekt verborgen patronen binnen uw gegevens om statistische anomalieën te verklaren en correlaties achter onverwachte klantenacties, uit-van-verbindende waarden, en plotselinge pieken of vallen voor geselecteerde metriek over convergent publiekssegmenten te identificeren.

Er is iets gebeurd. Waarom? Uw Anomaly Detection-rapport laat een ongewone spike in orders zien en u wilt weten waarom. Wat gebeurde er met het gewone? Wie reageert op welke campagne of verwijzing? Is er iets viraal gegaan? Wat zijn de specifieke factoren die aan deze anomalie hebben bijgedragen? En misschien nog belangrijker: Hoe kan ik belangrijke informatie over mijn klant vangen en deze prestaties herhalen? (Of, als een daling in metrisch of een toename in negatieve metrisch voorkwam, hoe kan ik het in de toekomst vermijden?)

Met de functie Analyse van bijdrage kunt u uw gegevens direct evalueren om te bepalen waarom er een anomalie is opgetreden. Het verdeelt de bijdragen aan een anomalie in seconden in wat vroeger weken nam, die patronen voor publiekssegmenten verstrekken en u helpen een verhaal voor klanteninteractie ontwikkelen. U kunt de Analyse van de Bijdrage strategisch gebruiken om zinvolle verenigingen te identificeren en te vangen om nieuwe publiekssegmenten te ontwikkelen, of het tactisch te gebruiken om uit-van-gebonden of frauduleuze activiteit te identificeren die een alarm teweegbrengt.

[Met Anomaly ](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md) Detectionering worden gegevenspikes en extreme statistische dips geïdentificeerd op basis van geselecteerde metriek en geselecteerde publiekssegmenten. Het bepaalt een historische norm die op een opleidingsperiode wordt gebaseerd en zet dan extreme compensaties in kaart die met specifieke gebeurtenissen correleren. Het kan een precipitatieve stijging in een positieve Metrische Orders of een stijging in een negatieve Metrische Stuiterwaarden, of een daling in allebei melden, die statistisch relevante gegevenspunten vangen die door de Analyse van de Bijdrage moeten worden geëvalueerd. Zodra een statistische anomalie is vastgesteld, kunt u met de analyse van de Bijdrage de relevante marketing- en campagnevariabelen over alle afwijkende gegevenspunten uitboren en evalueren. Het voert geavanceerde algoritmen en machine-leert processen uit om verenigingen te evalueren die tot een significante piek of een dip hebben bijgedragen. Deze berekeningen worden vervolgens weergegeven in interactieve visualisaties die zijn ontworpen om u verschillende perspectieven te bieden om te helpen antwoorden waarom er iets is gebeurd en wat er aan moet worden gedaan.

De Analyse van de bijdrage helpt u een verhaal ontwikkelen om te beschrijven waarom een anomalie voorkwam en hoe te om aan het te antwoorden, die relevante metriek vangen en verborgen punten identificeren die u een algemene reden voor publieksinteractie en trending klantenbelangen geven. Soms is een anomalie gemakkelijk te zien en te corrigeren, zoals een foutorder voor 2.000 kajaks. Soms is het complex, zoals het identificeren van een opkomende trend over een tijdsperiode in een regio die alleen reageert op een specifieke gerichte campagne. Door bijdragende items voor verschillende afmetingen en hun koppelingen te bundelen, krijgt u een algemeen idee van de interacties van uw publiek en kunt u context bieden voor afwijkende gegevenspunten.

Hier volgen enkele gebruiksgevallen:

* Identificeer hermarketingpotentieel door veranderingen in de productvraag te controleren.
* Verbeter klantenervaring door op specifieke publieksbelangen te antwoorden.
* Identificeer frauduleuze bestellingen in een vroeg stadium als buiten-de-grenzenrapport.
* Protect zelf van bedrijfsspionage door hoog gebruik en downloads te identificeren.
* Bewaking van bewerkingen zoals ontbrekende javascript-tags rapporteren.

Na een uitgebreide analyse van een anomalie wordt een overzicht van de bijdrage gegenereerd voor de bovenste items die zijn geordend op basis van het totale aantal voorvallen en het percentage van de bijdragende waarden van de post. Met een genormaliseerde bijdragenscore kunt u eenvoudig andere belangrijke dimensieitems vergelijken, vergelijken en koppelen.

## Tokens van bijdrageanalyse - overzicht {#section_3EF8D2BBCE6E4C309D753BCF04A453D0}

>[!IMPORTANT]
>
>De analyse van de bijdrage is verwijderd uit de reeks van de eigenschappen van Rapporten &amp; van Analyse en is nu beschikbaar slechts via Analysis Workspace.

Alle klanten met een machtiging voor een bijdrageanalyse kunnen een beperkt aantal keren per maand een volledige bijdrageanalyse uitvoeren in Analysis Workspace. Dit **sluit** klanten van het puntproduct (SiteCatalyst 15), klanten van de Stichting van Analytics, en Analytics Uitgezochte klanten uit, die helemaal geen Analyse van de Bijdrage krijgen.

Het aantal runtimes per bedrijf wordt beperkt door maandelijkse tokens die worden toegekend op basis van het Adobe Analytics-product dat uw bedrijf heeft aangeschaft. Dit omvat de capaciteit om de toegang van de Analyse van de Bijdrage te beperken om symbolisch misbruik te vermijden.

## Veelgestelde vragen {#section_11D0431AD2014B96AB9561CA66A367CE}

<table id="table_357775E5058644099E26B15A6790E8AF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Vraag </th> 
   <th colname="col2" class="entry"> Antwoord </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Waarom introduceerde Adobe tokens?  </b> </p> </td> 
   <td colname="col2"> <p>De bijdrageanalyse is een van de meest representatieve mogelijkheden in Adobe Analytics geweest. Als u een klein aantal "volledige" reeksen per maand krijgt (in plaats van slechts 3 dimensies voor sommige Analyseproducten), kunt u beter zien wat een onbeperkte volledige Analyse van de Bijdrage voor u kan doen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Hoe werkt het tokeren in bijdrageanalyse? Kosten het een teken om een project met een bestaande Analyse van de Bijdrage te laden, of slechts wanneer het runnen van gloednieuwe?</b> </p> </td> 
   <td colname="col2"> <p>Elk login bedrijf (niet elke gebruiker) krijgt een bepaald aantal tokens per maand, die u toestaan om "volledige"Analyse van de Bijdrage in Analysis Workspace in werking te stellen. </p> <p>Elke keer dat u een nieuwe bijdrageanalyse genereert, betaalt u één token. Het laden van projecten met vooraf uitgevoerde Analyses van de Bijdrage kost geen teken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Zijn tokens van toepassing op de Analyse van de Bijdrage in Rapporten &amp; Analytics?</b> </p> </td> 
   <td colname="col2"> <p>Nee. In de release van april 2018 worden geen bijdrageanalyse meer aangeboden in Reports &amp; Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Als mijn bedrijf uit tokens is en extra Analyses van de Bijdrage wil in werking stellen, wat kunnen wij doen?</b> </p> </td> 
   <td colname="col2"> <p>U kunt een upgrade uitvoeren naar een ander Adobe Analytics-product, bijvoorbeeld van Standaard (2 tokens/maand) naar Ultimate (20 tokens/maand). U kunt niet alleen meer tokens kopen. U moet een upgrade uitvoeren binnen het bestaande pakketframework. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Hoe beperk ik toegang tot de Analyse van de Bijdrage?</b> </p> </td> 
   <td colname="col2"> <p>Door gebrek, slechts hebben de beheerders toegang om de Analyses van de Bijdrage in werking te stellen, maar de beheerders kunnen toegang tot andere gebruikers verlenen door een toestemmingengroep in <a href="https://docs.adobe.com/content/help/nl-NL/core-services/interface/manage-users-and-products/admin-getting-started.html"  > Admin Console </a> te creëren. U zou toestemming moeten geven om de Analyse van de Bijdrage slechts aan gebruikers te gebruiken die een wettige reden hebben om het te gebruiken en worden vertrouwd om hun toegang niet te misbruiken. </p> <p>De toestemming wordt genoemd "Analyse van de Bijdrage"onder <span class="ignoretag"><span class="uicontrol"> Analytics</span> &gt; <span class="uicontrol"> Admin</span> &gt; <span class="uicontrol"> Gebruikersbeheer</span> &gt; <span class="uicontrol"> geeft Groepen</span> uit &gt; <span class="uicontrol"> geeft Al Toegang van het Rapport</span> &gt; <span class="uicontrol"> a12/&gt; &gt; <span class="uicontrol"> Gereedschappen en rapporten</span></span>.</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Hoe weet ik hoeveel tokens mijn bedrijf per maand mag gebruiken en hoeveel tokens we in de huidige maand hebben gebruikt?</b> </p> </td> 
   <td colname="col2"> <p>Ga naar <span class="ignoretag"><span class="uicontrol"> Admin</span> &gt; <span class="uicontrol"> Bedrijfsinstellingen</span> &gt; <span class="uicontrol"> De Niveaus van de Toegang van de Eigenschap van de Mening</span></span>. Deze pagina bevat twee nieuwe objecten: </p> <p><img placement="break"  src="assets/ca_access_level.png" id="image_16012FE1162C485EA768D175F43D7563" width="500px" /> </p> </td> 
  </tr> 
 </tbody> 
</table>


## Toeslagrechten voor anomalische detectie en bijdrageanalyse {#section_9278D58F21A840AA9B1ED1BD07A1EF0A}

Hieronder volgt een lijst van de gedetailleerde rechten voor de analyse van Anomaly Detection and Contribution in Analysis Workspace.

>[!IMPORTANT]
>
>Anomaliedetectie en bijdrage-analyses zijn verwijderd uit de functieset met rapporten en analytics, en nu dus alleen beschikbaar via Analysis Workspace. Klanten van Adobe Analytics Select en Adobe Analytics Foundation hebben voortaan alleen via Workspace toegang tot anomaliedetectie voor dagelijkse granulariteit.

<table id="table_5C9B7E4AE82640B5A913519E576889B5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Adobe Analytics Entitlement </th> 
   <th colname="col2" class="entry"> Anomaliedetectie </th> 
   <th colname="col3" class="entry"> Contributieanalyse </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Stichting </p> </td> 
   <td colname="col2"> <p>Alleen dagelijkse granulariteit </p> </td> 
   <td colname="col3" colsep="1"> <p>Geen tokens </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="https://www.adobe.com/data-analytics-cloud/analytics/select.html?promoid=B4XQ3X7G&amp;mv=other"  > Selecteren  </a> </p> </td> 
   <td colname="col2"> <p>Alleen dagelijkse granulariteit </p> </td> 
   <td colname="col3"> <p>Geen tokens </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="https://www.adobe.com/data-analytics-cloud/analytics/prime.html?promoid=91BF51TR&amp;mv=other"  > Eerste  </a> </p> </td> 
   <td colname="col2"> <p>Ja </p> </td> 
   <td colname="col3"> <p>10 tokens per maand </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="https://www.adobe.com/data-analytics-cloud/analytics/ultimate.html?promoid=8N4B5F1V&amp;mv=other"  > Ultieme</a> </p> </td> 
   <td colname="col2"> <p>Ja </p> </td> 
   <td colname="col3"> <p>20 tokens per maand </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>+Predictive Workbench </p> </td> 
   <td colname="col2"> <p>Ja </p> </td> 
   <td colname="col3"> <p>Onbeperkte tokens </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Standaard </p> 
    <ul id="ul_73D52020793B44868C9CE0F90893075D"> 
     <li id="li_21EE0871C87E43C8B781219B2BA0FA74">Adobe Analytics Core </li> 
     <li id="li_AB3593200F33439BAEE8FEB13CAE57F4">Adobe Analytics OD </li> 
     <li id="li_2B7D625519BC4A4CB598C95F15D3029B">Adobe Analytics MA </li> 
    </ul> </td> 
   <td colname="col2"> <p>Ja </p> </td> 
   <td colname="col3"> <p>2 tokens per maand </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Premium (360, kenmerk) </p> </td> 
   <td colname="col2"> <p>Ja </p> </td> 
   <td colname="col3"> <p>2 tokens per maand </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Premium (voltooid, <a href="https://www.adobe.com/data-analytics-cloud/analytics/predictive-intelligence.html"  > voorspellende intelligentie</a>) </p> </td> 
   <td colname="col2"> <p>Ja </p> </td> 
   <td colname="col3"> <p>Onbeperkte tokens </p> </td> 
  </tr> 
 </tbody> 
</table>
