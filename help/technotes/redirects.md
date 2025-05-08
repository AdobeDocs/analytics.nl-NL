---
description: Wijst de browser om naar een nieuwe locatie zonder tussenkomst van de gebruiker. Ze worden uitgevoerd in de webbrowser (omleiding client-side) of op de webserver (omleiding server-side).
keywords: Analyseimplementatie
title: Omleiding en aliassen
feature: Implementation Basics
exl-id: 0ed2aa9b-ab42-415d-985b-2ce782b6ab51
source-git-commit: a40f30bbe8fdbf98862c4c9a05341fb63962cdd1
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---

# Omleiding en aliassen

Wijst de browser om naar een nieuwe locatie zonder tussenkomst van de gebruiker. Ze worden uitgevoerd in de webbrowser (omleiding client-side) of op de webserver (omleiding server-side).

## Omleiding en aliassen {#aliases}

Wijst de browser om naar een nieuwe locatie zonder tussenkomst van de gebruiker. Ze worden uitgevoerd in de webbrowser (omleiding client-side) of op de webserver (omleiding server-side).

Omdat omleidingen geen gebruikersinteractie vereisen, worden omleidingen vaak uitgevoerd zonder dat de gebruiker dit merkt. Het enige wat aangeeft dat er een omleiding is opgetreden, is de adresbalk van de browser. Op de adresbalk wordt een URL weergegeven die afwijkt van de koppeling die de browser oorspronkelijk heeft aangevraagd.

Hoewel er slechts twee soorten omleidingen zijn, kunnen deze op verschillende manieren worden geïmplementeerd. Bijvoorbeeld, cliënt-zijomleiding kan voorkomen omdat de Web-pagina waaraan een gebruiker zijn of haar browser heeft gericht scripting of speciale code van HTML bevat die browser aan een andere URL opnieuw richt. Server-side omleidingen kunnen optreden omdat de pagina serverscripts bevat of omdat de webserver zo is geconfigureerd dat de gebruiker naar een andere URL wijst.

## Analyse en omleiding {#aa-redirects}

[!DNL Analytics] verzamelt enkele gegevens uit de browser en vertrouwt op bepaalde browsereigenschappen. Twee van deze eigenschappen, de &quot;Verwijzende URL&quot; (of &quot;verwijzende URL&quot;) en de &quot;Huidige URL&quot; kunnen worden gewijzigd door een omleiding aan de serverzijde. Omdat de browser weet dat er een URL is aangevraagd, maar een andere URL is geretourneerd, wist deze de URL waarnaar wordt verwezen. Het resultaat is dat de verwijzende URL leeg is en dat [!DNL Analytics] mogelijk aangeeft dat er geen referentie voor de pagina bestaat.

## Voorbeeld: bladeren zonder omleiding {#browse-without}

Overweeg het volgende hypothetische scenario waarin de gebruiker geen omleiding ontmoet:

1. De gebruiker wijst zijn of haar browser aan `www.google.com`, en typt, &quot;kortings vliegtuigkaartjes&quot;in het onderzoeksgebied, en klikt dan de **[!UICONTROL Search]** knoop.
1. De browser geeft de zoekresultaten weer, inclusief een koppeling naar uw site, [!DNL https://www.example.com/] . Nadat de zoekresultaten zijn weergegeven, geeft de adresbalk van de browser de zoektermen weer die de gebruiker in het zoekveld heeft ingevoerd ( `https://www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets` ). U ziet dat de zoektermen zijn opgenomen in de volgende URL-querytekenreeksparameters `https://www.google.com/search?` .
1. De gebruiker klikt op de koppeling naar uw hypothetische site [!DNL https://www.example.com/] . Wanneer de gebruiker op deze koppeling klikt en op de [!DNL example.com] -website landt, gebruikt [!DNL Analytics] JavaScript om de verwijzende URL ( `https://www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets` ) en de huidige URL ( `https://www.example.com/` ) te verzamelen.
1. [!DNL Analytics] rapporteert de informatie die tijdens deze interactie is verzameld in diverse rapporten, zoals [!UICONTROL Referring Domains] , [!UICONTROL Search Engines] en [!DNL Search Keywords] .

## Voorbeeld: bladeren met omleidingen {#browse-with}

Omleiding kan ertoe leiden dat de browser de werkelijke verwijzende URL weglaat. Overweeg het volgende scenario:

1. De gebruiker wijst zijn of haar browser aan `https://www.google.com`, en types, *kaartjes van de kortingsluchtvaartmaatschappij* in het onderzoeksgebied, en klikt dan de **[!UICONTROL Search]** knoop.
1. Op de adresbalk van het browservenster worden de zoektermen weergegeven die de gebruiker in het zoekveld heeft getypt `https://www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets` . U ziet dat de zoektermen zijn opgenomen in de volgende URL-querytekenreeksparameters `https://www.google.com/search?` . De browser geeft ook een pagina weer die de zoekresultaten bevat, inclusief een koppeling naar een van uw domeinnamen: [!DNL https://www.flytohawaiiforfree.com/] . Dit *domein van 0&rbrace; vanity &lbrace;wordt gevormd om de gebruiker aan `https://www.example.com/` opnieuw te richten.*
1. De gebruiker klikt op de koppeling `https://www.flytohawaiiforfree.com/` en wordt door de server omgeleid naar de hoofdsite, `https://www.example.com` . Wanneer de omleiding plaatsvindt, gaan de gegevens die belangrijk zijn voor de gegevensverzameling van [!DNL Analytics] verloren omdat de browser de verwijzende URL wist. De oorspronkelijke zoekinformatie die in de [!DNL Analytics] -rapporten (bijvoorbeeld [!UICONTROL Referring Domains] , [!UICONTROL Search Engines], [!UICONTROL Search Keywords] ) wordt gebruikt, gaat dus verloren.

## Omleidingen implementeren {#implement}

Als u [!DNL Analytics] -gegevens uit omleidingen wilt vastleggen, moet u vier kleine wijzigingen aanbrengen in de code die de omleiding maakt en het bestand [!DNL AppMeasurement] for JavaScript.

Als u de volgende stappen uitvoert, blijft de informatie behouden die de oorspronkelijke referentie (bijvoorbeeld `https://www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets` in het bovenstaande scenario) aan uw site doorgeeft:

## JavaScript-code voor verwijzingsoverschrijving configureren {#override}

In het codefragment hieronder ziet u twee JavaScript-variabelen, *`s_referrer`* en *`s_pageURL`* . Deze code wordt op de laatste landingspagina van de omleiding geplaatst.

```js
<script language="JavaScript" src="//INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/AppMeasurement.js"></script> 
<script language="JavaScript"><!-- 
/* You may give each page an identifying name, server, and channel on 
the next lines. */ 
s.pageName="" 
s.server="" 
s.campaign="" 
s.referrer="" 
s.pageURL=""
```

>[!IMPORTANT]
>
>Stel *`s.referrer`* slechts eenmaal in op de pagina. Als u deze meer dan één keer instelt met elke volgende aanroep of met elke gekoppelde klik die wordt bijgehouden, worden de referentie en verwante afmetingen, zoals zoekmachines en trefwoorden, dubbelgeteld.

## Omleiden met getQueryParam {#getqueryparam}

Hoewel [!UICONTROL getQueryParam] een gemakkelijke manier is om [!DNL Analytics] variabelen met vraagkoordwaarden te bevolken, moet het in verband met een tijdelijke variabele worden uitgevoerd zodat de wettige verwijzingen niet worden beschreven wanneer het vraagkoord leeg is. De beste manier om [!UICONTROL getQueryParam] te gebruiken is in verbinding met de [!UICONTROL getValue] -plug-in, zoals wordt beschreven met de volgende pseudo-code.

```js
// AppMeasurement 1.x 
var tempVar=s.Util.getQueryParam('origref') 
if(tempVar) 
  s.referrer=tempVar;
```

```js
// H Code 
var tempVar=s.getQueryParam('origref') 
if(tempVar) 
  s.referrer=tempVar;
```

## Het omleidingsmechanisme wijzigen {#modify}

Omdat de browser stroken die URL verwijzen, moet u het mechanisme vormen dat omleiding (bijvoorbeeld, de Webserver, server-zijcode, cliënt-zijcode) behandelt om de originele verwijzingsinformatie over te gaan. Als u ook de URL van de aliaskoppeling wilt opnemen, moet dit ook worden doorgegeven aan de uiteindelijke bestemmingspagina. Gebruik de variabele *`s_pageURL`* om de huidige URL te overschrijven.

Omdat er vele manieren zijn om een omleiding uit te voeren, zou u met uw groep van Webverrichtingen of uw online advertentiepartner moeten controleren om de specifieke mechanismen te identificeren die omleidingen op uw website uitvoeren.

## De oorspronkelijke referentie vastleggen {#original}

Doorgaans haalt [!DNL Analytics] de verwijzende URL uit de eigenschap [!UICONTROL document.referrer] van de browser en de huidige URL uit de eigenschap [!UICONTROL document.location] . Als u waarden doorgeeft aan de variabelen *`referrer`* en *`pageURL`* , kunt u de standaardverwerking overschrijven. Door een waarde aan de verwijzende variabele door te geven, vertelt u [!DNL Analytics] om de verwijzingsinformatie in het [!UICONTROL document.referrer] bezit te negeren en een alternatieve waarde te gebruiken die u bepaalt.

Daarom zou de definitieve versie van de landingspagina de volgende code moeten bevatten om de problemen te verhelpen die in het scenario van &quot;kortingstickets&quot; zijn geïntroduceerd.

```js
<script language="JavaScript" src="https://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/AppMeasurement.js"></script> 
<script language="JavaScript"><!-- 
/* You may give each page an identifying name, server, and channel on 
the next lines. */ 
s.pageName="" 
s.server="" 
s.campaign="" 
s.referrer="https://www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets" 
// Setting the s.pageURL variable is optional.
s.pageURL="https://www.flytohawaiiforfree.com"
```

## De referentie verifiëren met de Adobe Debugger {#verify}

Voer een test uit om te controleren of de verwijzende, voortkomende URL ( *`s_server`*) en campagnevariabelen worden vastgelegd.

Deze variabelen zullen als volgende parameters in [ Zuiver van de Wolk van de Ervaring worden vertegenwoordigd ](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=nl-NL).

<table id="table_5F3B987D4D514CA283F7B9F52EBC2301"> 
 <thead> 
  <tr> 
   <th class="entry"> </th> 
   <th class="entry"> <b> URL of de Waarde van het Koord van de Vraag </b> </th> 
   <th class="entry"> <b> Waarde zoals aangetoond in Debugger DigitalPulse </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Oorspronkelijke verwijzing </p> </td> 
   <td> <p> <span class="filepath"> https://www.google.com/search%3F hl%3Den %26ie%3DUTF826q%3 Dkorting%2Baarlijn%2Btickets </span> </p> </td> 
   <td> <p> <span class="filepath"> r=https:/ref=www.google.com/search?hl=en&amp;ie=UTF -8&amp;q=disconto+air+tickets </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Pagina-URL </p> </td> 
   <td> <p> <span class="filepath"> https://www.flytohawaiiforfree.com </span> </p> </td> 
   <td> <p> <span class="filepath"> g=https://www.flytohawaiiforfree.com </span> </p> <p>Deze waarde wordt weergegeven in de DigitalPulse-foutopsporing als de variabele <span class="varname"> pageURL </span> wordt gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>URL Ultimate-bestemmingspagina </p> </td> 
   <td> <p> <span class="filepath"> https://www.example.com </span> </p> </td> 
   <td> <p>Deze waarde wordt NIET weergegeven in de DigitalPulse-foutopsporing als de variabele <span class="varname"> pageURL </span> wordt gebruikt. </p> </td> 
  </tr> 
 </tbody> 
</table>

De tekst die de debugger toont zou aan het volgende voorbeeld moeten beantwoorden:

```
Image 
 
https://examplecom.112.2o7.net/b/ss/examplecom/1/JS-1.4/s61944015791667?[AQB] 
ndh=1 
t=4/8/20XX 13:34:28 4 360 
pageName=Welcome to example.com 
r=https://ref=www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets 
cc=USD 
g=https://www.flytohawaiiforfree.com 
s=1280x1024 
c=32 
j=1.3 
v=Y 
k=Y 
bw=1029 
bh=716 
ct=lan 
hp=N 
[AQE]
```

Nadat u hebt gecontroleerd of de Adobe [!UICONTROL Debugger] deze variabelen weergeeft, is het altijd handig om te bevestigen dat de zoektermen en het oorspronkelijke verwijzende domein (vóór de omleiding) het verkeer registreren in rapporten.
