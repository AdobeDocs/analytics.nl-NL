---
description: Wijst de browser om naar een nieuwe locatie zonder tussenkomst van de gebruiker. Ze worden uitgevoerd in de webbrowser (omleiding client-side) of op de webserver (omleiding server-side).
keywords: Analyseimplementatie
title: Omleiding en aliassen
feature: Implementation Basics
exl-id: 0ed2aa9b-ab42-415d-985b-2ce782b6ab51
source-git-commit: d3d5b01fe17f88d07a748fac814d2161682837c2
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---

# Omleiding en aliassen

Wijst de browser om naar een nieuwe locatie zonder tussenkomst van de gebruiker. Ze worden uitgevoerd in de webbrowser (omleiding client-side) of op de webserver (omleiding server-side).

## Omleiding en aliassen {#aliases}

Wijst de browser om naar een nieuwe locatie zonder tussenkomst van de gebruiker. Ze worden uitgevoerd in de webbrowser (omleiding client-side) of op de webserver (omleiding server-side).

Omdat omleidingen geen gebruikersinteractie vereisen, worden omleidingen vaak uitgevoerd zonder dat de gebruiker dit merkt. Het enige wat aangeeft dat er een omleiding is opgetreden, is de adresbalk van de browser. Op de adresbalk wordt een URL weergegeven die afwijkt van de koppeling die de browser oorspronkelijk heeft aangevraagd.

Hoewel er slechts twee soorten omleidingen zijn, kunnen deze op verschillende manieren worden geïmplementeerd. Bijvoorbeeld, cliënt-zijomleiding kan voorkomen omdat de Web-pagina waaraan een gebruiker zijn of haar browser heeft gericht scripting of speciale HTML code bevat die browser aan een andere URL opnieuw richt. Server-side omleidingen kunnen optreden omdat de pagina serverscripts bevat of omdat de webserver zo is geconfigureerd dat de gebruiker naar een andere URL wijst.

## Analyse en omleiding {#aa-redirects}

[!DNL Analytics] verzamelt enkele gegevens uit de browser en vertrouwt op bepaalde browsereigenschappen. Twee van deze eigenschappen, de &quot;Verwijzende URL&quot; (of &quot;verwijzende URL&quot;) en de &quot;Huidige URL&quot; kunnen worden gewijzigd door een omleiding aan de serverzijde. Omdat de browser weet dat er een URL is aangevraagd, maar een andere URL is geretourneerd, wist deze de URL waarnaar wordt verwezen. Het resultaat is dat de verwijzende URL leeg is, en [!DNL Analytics] zou kunnen melden dat geen verwijzer voor de pagina bestond.

## Voorbeeld: bladeren zonder omleiding {#browse-without}

Overweeg het volgende hypothetische scenario waarin de gebruiker geen omleiding ontmoet:

1. Gebruiker wijst zijn of haar browser aan `www.google.com`en typt u &quot;tickets met korting&quot; in het zoekveld en klikt u vervolgens op de knop **[!UICONTROL Search]** knop.
1. In de browser worden de zoekresultaten weergegeven, inclusief een koppeling naar uw site. [!DNL https://www.example.com/]. Nadat de zoekresultaten zijn weergegeven, ziet u op de adresbalk van de browser de zoektermen die de gebruiker in het zoekveld heeft ingevoerd ( `https://www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets`). U ziet dat de zoektermen zijn opgenomen in de volgende URL-parameters voor queryreeksen `https://www.google.com/search?`.
1. De gebruiker klikt op de koppeling naar uw hypothetische site [!DNL https://www.example.com/]. Wanneer de gebruiker op deze koppeling klikt en op de koppeling landt [!DNL example.com] website, [!DNL Analytics] gebruikt JavaScript om de verwijzende URL te verzamelen ( `https://www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets`) en de huidige URL ( `https://www.example.com/`).
1. [!DNL Analytics] rapporteert de informatie die tijdens deze interactie in diverse rapporten wordt verzameld, zoals [!UICONTROL Referring Domains], [!UICONTROL Search Engines], en [!DNL Search Keywords].

## Voorbeeld: bladeren met omleidingen {#browse-with}

Omleiding kan ertoe leiden dat de browser de werkelijke verwijzende URL weglaat. Overweeg het volgende scenario:

1. Gebruiker wijst zijn of haar browser aan `https://www.google.com`en typen *korting op vliegtickets* in het zoekveld en klik vervolgens op de knop **[!UICONTROL Search]** knop.
1. De adresbalk van het browservenster bevat de zoektermen die de gebruiker in het zoekveld heeft getypt `https://www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets`. U ziet dat de zoektermen zijn opgenomen in de volgende URL-parameters voor queryreeksen `https://www.google.com/search?`. De browser geeft ook een pagina weer die de zoekresultaten bevat, inclusief een koppeling naar een van uw domeinnamen: [!DNL https://www.flytohawaiiforfree.com/]. Dit *ijdelheid* domein wordt gevormd om de gebruiker aan om te leiden `https://www.example.com/`.
1. De gebruiker klikt op de koppeling `https://www.flytohawaiiforfree.com/` en wordt door de server omgeleid naar uw hoofdsite, `https://www.example.com`. Wanneer de omleiding plaatsvindt, zijn de gegevens die belangrijk zijn voor [!DNL Analytics] gegevensverzameling gaat verloren omdat de browser de verwijzende URL wist. De oorspronkelijke zoekinformatie die in het dialoogvenster [!DNL Analytics] rapporten (bijvoorbeeld [!UICONTROL Referring Domains], [!UICONTROL Search Engines], [!UICONTROL Search Keywords]) is verloren.

## Omleidingen implementeren {#implement}

Om vast te leggen [!DNL Analytics] gegevens uit omleidingen, moeten vier kleine wijzigingen worden aangebracht in de code die leidt tot omleiding en de [!DNL AppMeasurement] voor JavaScript-bestand.

Als u de volgende stappen uitvoert, blijft de informatie behouden die de oorspronkelijke referentie bevat (bijvoorbeeld `https://www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets` in het bovenstaande scenario) naar uw site wordt verzonden:

## JavaScript-code overschrijven door verwijzing configureren {#override}

In het onderstaande codefragment worden twee JavaScript-variabelen weergegeven. *`s_referrer`* en *`s_pageURL`*. Deze code wordt op de laatste landingspagina van de omleiding geplaatst.

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
>Set *`s.referrer`* maar één keer op de pagina. Als u deze meer dan één keer instelt met elke volgende aanroep of met elke gekoppelde klik die wordt bijgehouden, worden de referentie en verwante afmetingen, zoals zoekmachines en trefwoorden, dubbelgeteld.

## Omleiden met getQueryParam {#getqueryparam}

Terwijl de [!UICONTROL getQueryParam] is een gemakkelijke manier om te vullen [!DNL Analytics] variabelen met de waarden van het vraagkoord, moet het in verband met een tijdelijke variabele worden uitgevoerd zodat de wettige verwijzers niet worden beschreven wanneer het vraagkoord leeg is. De beste manier om [!UICONTROL getQueryParam] in verband met de [!UICONTROL getValue] zoals beschreven met de volgende pseudo-code.

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

Omdat de browser stroken die URL verwijzen, moet u het mechanisme vormen dat omleiding (bijvoorbeeld, de Webserver, server-zijcode, cliënt-zijcode) behandelt om de originele verwijzingsinformatie over te gaan. Als u ook de URL van de aliaskoppeling wilt opnemen, moet dit ook worden doorgegeven aan de uiteindelijke bestemmingspagina. Gebruik de *`s_pageURL`* variabele om de huidige URL te overschrijven.

Omdat er vele manieren zijn om een omleiding uit te voeren, zou u met uw groep van Webverrichtingen of uw online advertentiepartner moeten controleren om de specifieke mechanismen te identificeren die omleidingen op uw website uitvoeren.

## De oorspronkelijke referentie vastleggen {#original}

Normaal gesproken, [!DNL Analytics] ontvangt de verwijzende URL van de browser [!UICONTROL document.referrer] en de huidige URL vanuit de [!UICONTROL document.location] eigenschap. Door waarden door te geven aan de *`referrer`* en *`pageURL`* variabelen kunt u de standaardverwerking overschrijven. Door een waarde aan de verwijzende variabele door te geven, vertelt u [!DNL Analytics] om de verwijzende informatie in te negeren [!UICONTROL document.referrer] en om een alternatieve waarde te gebruiken die u definieert.

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

Voer een test uit om te controleren of de verwijzende URL ( *`s_server`*) en campagnevariabelen worden vastgelegd.

Deze variabelen worden als de volgende parameters in de [Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html).

<table id="table_5F3B987D4D514CA283F7B9F52EBC2301"> 
 <thead> 
  <tr> 
   <th class="entry"> </th> 
   <th class="entry"> <b>Waarde URL- of queryreeks</b> </th> 
   <th class="entry"> <b>Waarde zoals wordt weergegeven in de DigitalPulse-foutopsporing</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Oorspronkelijke verwijzing </p> </td> 
   <td> <p> <span class="filepath"> https://www.google.com/search%3F hl%3Den %26ie%3DUTF826q%3 Dkorting%2Baarlijn%2Btickets </span> </p> </td> 
   <td> <p> <span class="filepath"> r=https:/ref=www.google.com/search?hl=en&amp;ie=UTF -8&amp;q=discon+air+tickets </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Pagina-URL </p> </td> 
   <td> <p> <span class="filepath"> https://www.flytohawaiiforfree.com </span> </p> </td> 
   <td> <p> <span class="filepath"> g=https://www.flytohawaiiforfree.com </span> </p> <p>Deze waarde wordt weergegeven in de DigitalPulse-foutopsporing als de <span class="varname"> pageURL </span> variable wordt gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>URL van laatste bestemmingspagina </p> </td> 
   <td> <p> <span class="filepath"> https://www.example.com </span> </p> </td> 
   <td> <p>Deze waarde wordt NIET weergegeven in de DigitalPulse-foutopsporing als de <span class="varname"> pageURL </span> variable wordt gebruikt. </p> </td> 
  </tr> 
 </tbody> 
</table>

De tekst die de debugger toont zou aan het volgende voorbeeld moeten beantwoorden:

```
Image 
 
https://examplecom.112.2o7.net/b/ss/examplecom/1/JS-1.4/s61944015791667?[AQB] 
ndh=1 
t=4/8/2014 13:34:28 4 360 
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

Na te hebben geverifieerd dat de Adobe [!UICONTROL Debugger] Hiermee geeft u deze variabelen weer. Het is altijd handig om te bevestigen dat de zoektermen en het oorspronkelijke verwijzende domein (vóór de omleiding) het verkeer in rapporten registreren.
