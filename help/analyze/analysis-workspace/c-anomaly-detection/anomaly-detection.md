---
description: Meer informatie over de detectie van anomalieën in Analysis Workspace.
title: Overzicht van anomalische detectie
feature: Anomaly Detection
role: User, Admin
exl-id: b1625206-c774-40ef-9d92-25ee8ff1478d
source-git-commit: b4c1636bdc9d5be522b16f945a46beabf4f7a733
workflow-type: tm+mt
source-wordcount: '1280'
ht-degree: 1%

---

# Overzicht van anomalische detectie

U kunt gegevensanomalieën contextafhankelijk weergeven en analyseren in Analysis Workspace. De Analyse van de Bijdrage werkt met Anomaly Detection helpen identificeren wat tot de anomalie heeft bijgedragen.


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Anomaly opsporing ](https://video.tv.adobe.com/v/25444?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>Adobe Analytics Uitgezochte en de klanten van Adobe Analytics Foundation hebben toegang slechts tot *dagelijkse granularity* Anomaly Detection in Workspace. Voor meer informatie, zie {de Entitlements van de Analyse van de Anomaly van de Opsporing en van de Bijdrage [.](#anomaly-detection-and-contribution-analysis-entitlements)

## Anomalische detectie

Anomaly Detection biedt een statistische methode om te bepalen hoe een bepaalde metrische waarde is gewijzigd ten opzichte van eerdere gegevens.

Met Anomaly Detection kunt u &quot;echte signalen&quot; scheiden van &quot;ruis&quot; en vervolgens mogelijke factoren identificeren die tot die signalen of anomalieën hebben bijgedragen. Met andere woorden, het laat je zien welke statistische fluctuaties belangrijk zijn en welke niet. U kunt dan de worteloorzaak van een ware anomalie identificeren. Bovendien kunt u betrouwbare metrische (KPI) prognoses krijgen.

Voorbeelden van anomalieën die u kunt onderzoeken zijn:

* Drastische afname in gemiddelde orderwaarde
* Pieken in orders met lage inkomsten
* Spikes of druppels in proefregistraties
* Druppels in weergaven van openingspagina&#39;s
* Spikes in videobuffergebeurtenissen
* Spikes in lage videobitsnelheden

Zowel zijn de Anomaly Opsporing en [ Analyse van de Bijdrage ](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/anomaly-detection/anomaly-detection) kernwerkschema&#39;s in Analysis Workspace. U kunt de Analyse van de Bijdrage tegen om het even welke dagelijkse anomalie in werking stellen en het resultaat in uw project van Analysis Workspace inbedden.

Analysis Workspace-algoritme voor het opsporen van anomalieën bevat

* Naast de bestaande dagelijkse granulariteit wordt ook ondersteuning geboden voor granulariteit per uur, week en maand.
* Bewustzijn van seizoensgebondenheid (zoals &quot;Zwarte Vrijdag&quot;) en feestdagen.

## Contributieanalyse

Met Contribute Analysis worden verborgen patronen in uw gegevens gedetecteerd om statistische anomalieën te verklaren en correlaties achter elkaar te identificeren

* onverwachte acties van de klant;
* niet-gebonden waarden, en
* plotselinge pieken of vallen

voor geselecteerde metriek over convergerende publiekssegmenten.


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ analyse van de Bijdrage ](https://video.tv.adobe.com/v/25443?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


Er is iets gebeurd. Waarom? Uw Anomaly Detection-rapport laat een ongewone spike in orders zien en u wilt weten waarom. Wat gebeurde er met het gewone? Wie reageert op welke campagne of verwijzing? Is er iets viraal gegaan? Wat zijn de specifieke factoren die aan deze anomalie hebben bijgedragen? En misschien het belangrijkste: Hoe kan ik belangrijke informatie over mijn klant vangen en deze prestaties herhalen? (Of, als een daling in metrisch of een toename in negatieve metrisch voorkwam, hoe kan ik het in de toekomst vermijden?)

Met de functie Analyse van bijdrage kunt u uw gegevens direct evalueren om te bepalen waarom er een anomalie is opgetreden. Het verdeelt de bijdragen aan een anomalie in seconden in wat vroeger weken nam, die patronen voor publiekssegmenten verstrekken en u helpen een verhaal voor klanteninteractie ontwikkelen. U kunt de Analyse van de Bijdrage strategisch gebruiken om zinvolle verenigingen te identificeren en te vangen. Dan gebruik die verenigingen strategisch om nieuwe publiekssegmenten te ontwikkelen, of tactisch om uit-van-gebonden of frauduleuze activiteit te identificeren die een alarm teweegbrengt.

[ Anomaly Detectie ](#anomaly-detection) identificeert gegevenspikes en extreme statistische dips die op geselecteerde metriek en geselecteerde publiekssegmenten worden gebaseerd. Anomaly-detectie stelt een historische norm in op basis van een trainingsperiode en zet vervolgens extreme verschuivingen in die verband houden met specifieke gebeurtenissen. Anomaly-detectie kan een precipitatieve stijging in een positieve Orders-metrische waarde of een toename in een negatieve Bounces-metrische waarde, of in beide gevallen een daling melden, waarbij statistisch relevante gegevenspunten worden vastgelegd die door de bijdrageanalyse moeten worden geëvalueerd. Zodra een statistische anomalie is vastgesteld, kunt u met de analyse van de Bijdrage de relevante marketing- en campagnevariabelen over alle afwijkende gegevenspunten uitboren en evalueren. Het voert geavanceerde algoritmen en machine-leert processen uit om verenigingen te evalueren die tot een significante piek of een dip hebben bijgedragen. Deze berekeningen worden vervolgens weergegeven in interactieve visualisaties die zijn ontworpen om u verschillende perspectieven te bieden om te helpen antwoorden waarom er iets is gebeurd en wat er aan moet worden gedaan.

Met de functie Analyse van bijdrage kunt u een beschrijving maken van de oorzaak van een anomalie. En hoe te om aan anomalieën te antwoorden, die relevante metriek vangen en verborgen punten identificeren die u een algemene reden voor publieksinteractie en trending klantenbelangen geven. Soms is een anomalie gemakkelijk te zien en te corrigeren, zoals een foutorder voor 2.000 kajaks. Soms is het complex, zoals het identificeren van een opkomende trend over een tijdsperiode in een regio die alleen reageert op een specifieke gerichte campagne. Door bijdragende items voor verschillende afmetingen en hun koppelingen te bundelen, krijgt u een algemeen idee van de interacties van uw publiek en kunt u context bieden voor afwijkende gegevenspunten.

Hier volgen enkele gebruiksgevallen:

* Identificeer hermarketingpotentieel door veranderingen in de productvraag te controleren.
* Verbeter klantenervaring door op specifieke publieksbelangen te antwoorden.
* Identificeer frauduleuze bestellingen in een vroeg stadium als buiten-de-grenzenrapport.
* Bescherm uzelf tegen bedrijfsspionage door hoog gebruik en downloads te identificeren.
* Bewaking van bewerkingen zoals het rapporteren van ontbrekende JavaScript-tags.

Na een uitgebreide analyse van een anomalie wordt een overzicht van de bijdrage gegenereerd voor de bovenste items die zijn geordend op basis van het totale aantal voorvallen en het percentage van de bijdragende waarden van de post. Met een genormaliseerde bijdragenscore kunt u eenvoudig andere belangrijke dimensieitems vergelijken, vergelijken en koppelen.

## Tokens voor bijdrageanalyse

Alle klanten met een machtiging voor een bijdrageanalyse kunnen een beperkt aantal keren per maand een volledige bijdrageanalyse uitvoeren in Analysis Workspace. De Analyse van de bijdrage **sluit** klanten van het puntproduct (SiteCatalyst 15), klanten van de Stichting van Analytics, en de Analyse Uitgezochte klanten uit, die niet gerechtigd zijn tot de Analyse van de Bijdrage.

Het aantal runtimes per bedrijf wordt beperkt door maandelijkse tokens die worden toegekend op basis van het Adobe Analytics-product dat uw bedrijf heeft aangeschaft. Het aantal looppas per bedrijf omvat de capaciteit om de toegang van de Analyse van de Bijdrage te beperken om symbolisch misbruik te vermijden.

## Veelgestelde vragen

| Vraag | Antwoord |
| --- | --- |
| Waarom introduceerde Adobe tokens? | De bijdrageanalyse is een van de meest representatieve mogelijkheden in Adobe Analytics geweest. Door een klein aantal volledige reeksen per maand (in plaats van slechts 3 dimensies voor sommige producten van Analytics) te geven, kunt u zien wat de onbeperkte volledige Analyse van de Bijdrage voor u kan doen. |
| Hoe werken tokens in Bijdrage-analyse? Kosten het een token om een project te laden met een bestaande bijdrageanalyse, of alleen wanneer een gloednieuwe wordt uitgevoerd? | Elk login bedrijf (niet elke gebruiker) krijgt een bepaald aantal tokens per maand, die u toestaan om &quot;volledige&quot;Analyse van de Bijdrage in Analysis Workspace in werking te stellen.  Elke keer dat u een nieuwe bijdrageanalyse genereert, betaalt u één token. Het laden van projecten met vooraf uitgevoerde Analyses van de Bijdrage kost geen teken. |
| Als mijn bedrijf uit tokens is en extra Analyses van de Bijdrage wil in werking stellen, wat te doen? | U kunt een upgrade uitvoeren naar een ander Adobe Analytics-product, bijvoorbeeld van Standaard (2 tokens/maand) naar Ultimate (20 tokens/maand). Je kunt niet meer tokens kopen. U moet een upgrade uitvoeren binnen het bestaande pakketframework. |
| Hoe beperk ik toegang tot de Analyse van de Bijdrage? | Standaard hebben alleen beheerders toegang tot Contribute-analyses. Nochtans, kunnen beheerders toegang tot andere gebruikers verlenen door een toestemmingsgroep in [ Adobe Admin Console ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-console/home) tot stand te brengen. Geef alleen toestemming om de Contribute-analyse te gebruiken voor gebruikers die een legitieme reden hebben om deze te gebruiken en die vertrouwd zijn om hun toegang niet te misbruiken. De machtiging wordt [!UICONTROL Contribution Analysis] onder [!UICONTROL Report Suite Tools] genoemd. [Meer informatie](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-console/permissions/report-suite-tools) |
| Hoe weet ik hoeveel tokens mijn bedrijf per maand mag gebruiken en hoeveel tokens mijn bedrijf deze maand heeft gebruikt? | Ga naar [!UICONTROL Admin] > [!UICONTROL All admin] > [!UICONTROL Company settings Home] > [!UICONTROL View Feature Access Levels]. Zoeken onder<ul><li>Bijdrage-analyse: aantal tokens voor maandgebruik</li><li>Bijdrage-analyse: aantal gebruikstokens dat deze maand is gebruikt</li></ul> |

## Toeslagrechten voor anomalische detectie en analyse van bijdragen

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
   <td colname="col1"> <p><a href="https://business.adobe.com/products/analytics/compare-adobe-analytics-packages.html?promoid=B4XQ3X7G&amp;mv=other"  > Selecteren </a> </p> </td> 
   <td colname="col2"> <p>Alleen dagelijkse granulariteit </p> </td> 
   <td colname="col3"> <p>Geen tokens </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="https://business.adobe.com/products/analytics/compare-adobe-analytics-packages.html?promoid=91BF51TR&amp;mv=other"  > Prime </a> </p> </td> 
   <td colname="col2"> <p>Ja </p> </td> 
   <td colname="col3"> <p>10 tokens per maand </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="https://business.adobe.com/products/analytics/compare-adobe-analytics-packages.html?promoid=8N4B5F1V&amp;mv=other"  > Ultimate </a> </p> </td> 
   <td colname="col2"> <p>Ja </p> </td> 
   <td colname="col3"> <p>20 tokens per maand </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Predictive Workbench-invoegtoepassing </p> </td> 
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
   <td colname="col1"> <p>Premium (volledige, <a href="https://business.adobe.com/products/analytics/predictive-analytics.html"  > voorspellende intelligentie </a> ) </p> </td> 
   <td colname="col2"> <p>Ja </p> </td> 
   <td colname="col3"> <p>Onbeperkte tokens </p> </td> 
  </tr> 
 </tbody> 
</table>
