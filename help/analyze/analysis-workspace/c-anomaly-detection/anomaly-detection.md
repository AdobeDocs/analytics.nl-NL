---
description: U kunt gegevensanomalieën contextafhankelijk weergeven en analyseren in Analysis Workspace.
title: Overzicht van anomalische detectie
feature: Anomaly Detection
role: User, Admin
exl-id: b1625206-c774-40ef-9d92-25ee8ff1478d
source-git-commit: d7a6867796f97f8a14cd8a3cfad115923b329c7c
workflow-type: tm+mt
source-wordcount: '1276'
ht-degree: 1%

---

# Overzicht van anomalische detectie

U kunt gegevensanomalieën contextafhankelijk weergeven en analyseren in Analysis Workspace. De analyse van de bijdrage werkt samen met Anomaly Detection om te helpen identificeren wat tot de anomalie heeft bijgedragen.


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Anomaly opsporing ](https://video.tv.adobe.com/v/25444?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>Adobe Analytics Select- en Adobe Analytics Foundation-klanten hebben alleen toegang tot Anomaly Detection (dagelijkse granulariteit) in Workspace. Voor meer informatie, zie &lbrace;de Entitlements van de Analyse van de Anomaly van de Opsporing en van de Bijdrage [&#128279;](#anomaly-detection-and-contribution-analysis-entitlements).

## Anomaliedetectie

Anomaly Detection biedt een statistische methode om te bepalen hoe een bepaalde metrische waarde is gewijzigd ten opzichte van eerdere gegevens.

Met Anomaly Detection kunt u &quot;echte signalen&quot; scheiden van &quot;ruis&quot; en vervolgens mogelijke factoren identificeren die tot die signalen of anomalieën hebben bijgedragen. Met andere woorden, het laat je zien welke statistische fluctuaties belangrijk zijn en welke niet. U kunt dan de worteloorzaak van een ware anomalie identificeren. Bovendien kunt u betrouwbare metrische (KPI) prognoses krijgen.

Voorbeelden van anomalieën die u kunt onderzoeken zijn:

* Drastische afname in gemiddelde orderwaarde
* Pieken in orders met lage inkomsten
* Spikes of druppels in proefregistraties
* Druppels in weergaven van openingspagina&#39;s
* Spikes in videobuffergebeurtenissen
* Spikes in lage videobitsnelheden

Zowel zijn de Anomaly Opsporing en [ Analyse van de Bijdrage ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/anomaly-detection/anomaly-detection.html?lang=nl-NL) kernwerkschema&#39;s in Analysis Workspace. U kunt de Analyse van de Bijdrage tegen om het even welke dagelijkse anomalie in werking stellen en het resultaat in uw project van Analysis Workspace inbedden.

Analysis Workspace-algoritme voor het opsporen van anomalieën bevat

* Naast de bestaande dagelijkse granulariteit wordt ook ondersteuning geboden voor granulariteit per uur, week en maand.
* Bewustzijn van seizoensgebondenheid (zoals &quot;Zwarte Vrijdag&quot;) en feestdagen.

## Contributieanalyse

De Analyse van de bijdrage ontdekt verborgen patronen binnen uw gegevens om statistische anomalieën te verklaren en correlaties achter onverwachte klantenacties, uit-van-verbindende waarden, en plotselinge pieken of vallen voor geselecteerde metriek over convergent publiekssegmenten te identificeren.


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ analyse van de Bijdrage ](https://video.tv.adobe.com/v/25443?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


Er is iets gebeurd. Waarom? Uw Anomaly Detection-rapport laat een ongewone spike in orders zien en u wilt weten waarom. Wat gebeurde er met het gewone? Wie reageert op welke campagne of verwijzing? Is er iets viraal gegaan? Wat zijn de specifieke factoren die aan deze anomalie hebben bijgedragen? En misschien het belangrijkste: Hoe kan ik belangrijke informatie over mijn klant vangen en deze prestaties herhalen? (Of, als een daling in metrisch of een toename in negatieve metrisch voorkwam, hoe kan ik het in de toekomst vermijden?)

Met de functie Analyse van bijdrage kunt u uw gegevens direct evalueren om te bepalen waarom er een anomalie is opgetreden. Het verdeelt de bijdragen aan een anomalie in seconden in wat vroeger weken nam, die patronen voor publiekssegmenten verstrekken en u helpen een verhaal voor klanteninteractie ontwikkelen. U kunt de Analyse van de Bijdrage strategisch gebruiken om zinvolle verenigingen te identificeren en te vangen om nieuwe publiekssegmenten te ontwikkelen, of het tactisch te gebruiken om uit-van-gebonden of frauduleuze activiteit te identificeren die een alarm teweegbrengt.

[ Anomaly Detectie ](#anomaly-detection) identificeert gegevenspikes en extreme statistische dips die op geselecteerde metriek en geselecteerde publiekssegmenten worden gebaseerd. Het bepaalt een historische norm die op een opleidingsperiode wordt gebaseerd en zet dan extreme compensaties in kaart die met specifieke gebeurtenissen correleren. Het kan een precipitatieve stijging in een positieve Metrische Orders of een stijging in een negatieve Metrische Stuiterwaarden, of een daling in allebei melden, die statistisch relevante gegevenspunten vangen die door de Analyse van de Bijdrage moeten worden geëvalueerd. Zodra een statistische anomalie is vastgesteld, kunt u met de analyse van de Bijdrage de relevante marketing- en campagnevariabelen over alle afwijkende gegevenspunten uitboren en evalueren. Het voert geavanceerde algoritmen en machine-leert processen uit om verenigingen te evalueren die tot een significante piek of een dip hebben bijgedragen. Deze berekeningen worden vervolgens weergegeven in interactieve visualisaties die zijn ontworpen om u verschillende perspectieven te bieden om te helpen antwoorden waarom er iets is gebeurd en wat er aan moet worden gedaan.

De Analyse van de bijdrage helpt u een verhaal ontwikkelen om te beschrijven waarom een anomalie voorkwam en hoe te om aan het te antwoorden, die relevante metriek vangen en verborgen punten identificeren die u een algemene reden voor publieksinteractie en trending klantenbelangen geven. Soms is een anomalie gemakkelijk te zien en te corrigeren, zoals een foutorder voor 2.000 kajaks. Soms is het complex, zoals het identificeren van een opkomende trend over een tijdsperiode in een regio die alleen reageert op een specifieke gerichte campagne. Door bijdragende items voor verschillende afmetingen en hun koppelingen te bundelen, krijgt u een algemeen idee van de interacties van uw publiek en kunt u context bieden voor afwijkende gegevenspunten.

Hier volgen enkele gebruiksgevallen:

* Identificeer hermarketingpotentieel door veranderingen in de productvraag te controleren.
* Verbeter klantenervaring door op specifieke publieksbelangen te antwoorden.
* Identificeer frauduleuze bestellingen in een vroeg stadium als buiten-de-grenzenrapport.
* Protect zelf van bedrijfsspionage door hoog gebruik en downloads te identificeren.
* Bewaking van bewerkingen zoals ontbrekende javascript-tags rapporteren.

Na een uitgebreide analyse van een anomalie wordt een overzicht van de bijdrage gegenereerd voor de bovenste items die zijn geordend op basis van het totale aantal voorvallen en het percentage van de bijdragende waarden van de post. Met een genormaliseerde bijdragenscore kunt u eenvoudig andere belangrijke dimensieitems vergelijken, vergelijken en koppelen.

## Tokens van bijdrageanalyse - overzicht {#section_3EF8D2BBCE6E4C309D753BCF04A453D0}

Alle klanten met een machtiging voor een bijdrageanalyse kunnen een beperkt aantal keren per maand een volledige bijdrageanalyse uitvoeren in Analysis Workspace. Dit **sluit** klanten van het puntproduct (SiteCatalyst 15), klanten van de Stichting van Analytics, en de Analyse Uitgezochte klanten uit, die de Analyse van de Bijdrage helemaal niet krijgen.

Het aantal runtimes per bedrijf wordt beperkt door maandelijkse tokens die worden toegekend op basis van het Adobe Analytics-product dat uw bedrijf heeft aangeschaft. Dit omvat de capaciteit om de toegang van de Analyse van de Bijdrage te beperken om symbolisch misbruik te vermijden.

## Veelgestelde vragen {#section_11D0431AD2014B96AB9561CA66A367CE}

| Vraag | Antwoord |
| --- | --- |
| Waarom introduceerde Adobe tokens? | De bijdrageanalyse is een van de meest representatieve mogelijkheden in Adobe Analytics geweest. Als u een klein aantal &quot;volledige&quot; reeksen per maand krijgt (in plaats van slechts 3 dimensies voor sommige Analyseproducten), kunt u beter zien wat een onbeperkte volledige Analyse van de Bijdrage voor u kan doen. |
| Hoe werkt het tokeren in bijdrageanalyse? Kosten het een token om een project te laden met een bestaande bijdrageanalyse, of alleen wanneer een gloednieuwe wordt uitgevoerd? | Elk login bedrijf (niet elke gebruiker) krijgt een bepaald aantal tokens per maand, die u toestaan om &quot;volledige&quot;Analyse van de Bijdrage in Analysis Workspace in werking te stellen.  Elke keer dat u een nieuwe bijdrageanalyse genereert, betaalt u één token. Het laden van projecten met vooraf uitgevoerde Analyses van de Bijdrage kost geen teken. |
| Als mijn bedrijf uit tokens is en extra Analyses van de Bijdrage wil in werking stellen, wat kunnen wij doen? | U kunt een upgrade uitvoeren naar een ander Adobe Analytics-product, bijvoorbeeld van Standaard (2 tokens/maand) naar Ultimate (20 tokens/maand). U kunt niet alleen meer tokens kopen. U moet een upgrade uitvoeren binnen het bestaande pakketframework. |
| Hoe beperk ik toegang tot de Analyse van de Bijdrage? | Standaard hebben alleen beheerders toegang tot Contribute-analyses. Nochtans, kunnen beheerders toegang tot andere gebruikers verlenen door een toestemmingsgroep in [ Adobe Admin Console ](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/home.html?lang=nl-NL) tot stand te brengen. U zou toestemming moeten geven om de Analyse van de Bijdrage slechts aan gebruikers te gebruiken die een wettige reden hebben om het te gebruiken en worden vertrouwd om hun toegang niet te misbruiken. De machtiging wordt [!UICONTROL Contribution Analysis] onder [!UICONTROL Report Suite Tools] genoemd. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/permissions/report-suite-tools.html?lang=nl-NL) |
| Hoe weet ik hoeveel tokens mijn bedrijf per maand mag gebruiken en hoeveel tokens we in de huidige maand hebben gebruikt? | Ga naar [!UICONTROL Admin] > [!UICONTROL All admin] > [!UICONTROL Company settings Home] > [!UICONTROL View Feature Access Levels]. Zoeken onder<ul><li>Bijdrage-analyse: aantal tokens voor maandgebruik</li><li>Bijdrage-analyse: aantal gebruikstokens dat deze maand is gebruikt</li></ul> |

## Toeslagrechten voor anomalische detectie en analyse van bijdragen {#section_9278D58F21A840AA9B1ED1BD07A1EF0A}

Hieronder volgt een lijst van de gedetailleerde rechten voor de analyse van Anomaly Detection and Contribution in Analysis Workspace.

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
   <td colname="col1"> <p><a href="https://www.adobe.com/data-analytics-cloud/analytics/select.html?promoid=B4XQ3X7G&amp;mv=other"  > Selecteren </a> </p> </td> 
   <td colname="col2"> <p>Alleen dagelijkse granulariteit </p> </td> 
   <td colname="col3"> <p>Geen tokens </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="https://www.adobe.com/data-analytics-cloud/analytics/prime.html?promoid=91BF51TR&amp;mv=other"  > Prime </a> </p> </td> 
   <td colname="col2"> <p>Ja </p> </td> 
   <td colname="col3"> <p>10 tokens per maand </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="https://www.adobe.com/data-analytics-cloud/analytics/ultimate.html?promoid=8N4B5F1V&amp;mv=other"  > Ultimate </a> </p> </td> 
   <td colname="col2"> <p>Ja </p> </td> 
   <td colname="col3"> <p>20 tokens per maand </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>+Predictive Workbench </p> </td> 
   <td colname="col2"> <p>Ja </p> </td> 
   <td colname="col3"> <p>Onbeperkte tokens </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Standard </p> 
    <ul id="ul_73D52020793B44868C9CE0F90893075D"> 
     <li id="li_21EE0871C87E43C8B781219B2BA0FA74">Adobe Analytics Core </li> 
     <li id="li_AB3593200F33439BAEE8FEB13CAE57F4">ADOBE ANALYTICS OD </li> 
     <li id="li_2B7D625519BC4A4CB598C95F15D3029B">ADOBE ANALYTICS MA </li> 
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
   <td colname="col1"> <p>Premium (volledige, <a href="https://www.adobe.com/data-analytics-cloud/analytics/predictive-intelligence.html"  > voorspellende intelligentie </a> ) </p> </td> 
   <td colname="col2"> <p>Ja </p> </td> 
   <td colname="col3"> <p>Onbeperkte tokens </p> </td> 
  </tr> 
 </tbody> 
</table>
