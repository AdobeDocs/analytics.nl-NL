---
title: getVisitNum
description: Volg het huidige bezoeknummer van een bezoeker.
translation-type: tm+mt
source-git-commit: 180ad544541f25d02b3a257559bc045abed7387b

---


# Adobe-insteekmodule: getVisitNum

> [!IMPORTANT] Deze plug-in wordt geleverd door Adobe Consulting als een hoffelijkheid om u te helpen meer waarde te krijgen van Adobe Analytics. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

De `getVisitNum` insteekmodule retourneert het bezoeknummer voor alle bezoekers die binnen het gewenste aantal dagen naar de site komen. De Werkruimte van de analyse biedt een dimensie van het Aantal van het Bezoek aan die gelijkaardige functionaliteit verstrekt. Adobe raadt u aan deze plug-in te gebruiken als u meer controle wilt over de verhoging van het bezoeknummer. Deze insteekmodule is niet nodig als de ingebouwde dimensie &#39;Visit Number&#39; in de analysewerkruimte toereikend is voor uw rapportagevereisten.

## De plug-in installeren met de Adobe Experience Platform Launch-extensie

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Go to the [!UICONTROL Extensions] tab, then click on the [!UICONTROL Catalog] button
1. De [!UICONTROL Common Analytics Plugins] extensie installeren en publiceren
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: Geen
   * Gebeurtenis: Kern - Bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: Gebruikelijke plug-ins voor Analytics
   * Type handeling: Initialiseren getVisitNum
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met de aangepaste code-editor van Launch

Als u de extensie van de plug-in niet wilt gebruiken, kunt u de aangepaste code-editor gebruiken.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar het [!UICONTROL Extensions] tabblad en klik vervolgens op de [!UICONTROL Configure] knop onder de extensie Adobe Analytics.
1. Vouw de [!UICONTROL Configure tracking using custom code] accordeon uit, zodat de [!UICONTROL Open Editor] knop zichtbaar wordt.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

## De plug-in installeren met AppMeturement

Kopieer en plak de volgende code ergens in het AppMeasurement-bestand nadat het analytics tracking-object is geïnstantieerd (met `s_gi`). Door opmerkingen en versienummers van de code in uw implementatie te behouden, kan Adobe eventuele problemen oplossen.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getVisitNum v4.11 (Requires endOfDatePeriod plug-in) */
s.getVisitNum=function(rp,erp){var s=this,c=function(rp){return isNaN(rp)?!1:(parseFloat(rp)|0)===parseFloat(rp)};rp=rp?rp:365;erp= "undefined"!==typeof erp?!!erp:c(rp)?!0:!1;var e=(new Date).getTime(),b=endOfDatePeriod(rp);if(s.c_r("s_vnc"+rp))var g=s.c_r("s_vnc"+rp).split("&vn="),d=g[1];if(s.c_r("s_ivc"))return d?(b.setTime(e+18E5),s.c_w("s_ivc",!0,b),d):"unknown visit number";if("undefined"!==typeof d)return d++,c=erp&&c(rp)?e+864E5*rp:g[0],b.setTime(c),s.c_w("s_vnc"+rp,c+"&vn="+d,b),b.setTime(e+ 18E5),s.c_w("s_ivc",!0,b),d;c=c(rp)?e+864E5*rp:endOfDatePeriod(rp).getTime();s.c_w("s_vnc"+rp,c+"&vn=1",b);b.setTime(e+18E5); s.c_w("s_ivc",!0,b);return"1"};

/* Adobe Consulting Plugin: endOfDatePeriod v1.1 */
var endOfDatePeriod=function(dp){var a=new Date,b=isNaN(dp)?0:Math.floor(dp);a.setHours(23);a.setMinutes(59);a.setSeconds(59); "w"===dp&&(b=6-a.getDay());if("m"===dp){b=a.getMonth()+1;var d=a.getFullYear();b=(new Date(d?d:1970,b?b:1,0)).getDate()-a.getDate()}a.setDate(a.getDate()+b);"y"===dp&&(a.setMonth(11),a.setDate(31));return a};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `getVisitNum` methode gebruikt de volgende argumenten:

* **`rp`** (optioneel, geheel getal OF tekenreeks): Het aantal dagen voordat de teller van het bezoeknummer opnieuw wordt ingesteld.  Wordt standaard ingesteld `365` wanneer niet ingesteld.
   * Wanneer dit argument is `"w"`, stelt de teller aan het eind van de week (deze Zaterdag om 11:59 PM) opnieuw in
   * Wanneer dit argument is `"m"`, stelt de teller aan het eind van de maand (de laatste dag van deze maand) opnieuw in
   * Wanneer dit argument is `"y"`, wordt de teller aan het einde van het jaar opnieuw ingesteld (31 december)
* **`erp`** (optioneel, Booleaans): Wanneer het `rp` argument een getal is, bepaalt dit argument of de vervaldatum van het bezoeknummer moet worden verlengd. Als deze optie is ingesteld op `true`, wordt bij volgende treffers voor uw site de teller van het bezoeknummer opnieuw ingesteld. Als dit is ingesteld op `false`, worden volgende treffers voor uw site niet uitgebreid wanneer de teller van het bezoeknummer opnieuw wordt ingesteld. Wordt standaard ingesteld op `true`. Dit argument is niet geldig wanneer het `rp` argument een tekenreeks is.

Het aantal bezoekers neemt toe wanneer de bezoeker na 30 minuten inactiviteit terugkeert naar uw site. Als deze methode wordt aangeroepen, wordt een geheel getal geretourneerd dat het huidige bezoeknummer van de bezoeker vertegenwoordigt.

Deze plug-in stelt een cookie van de eerste fabrikant in, die wordt aangeroepen `"s_vnc[LENGTH]"` waar de waarde `[LENGTH]` is die aan het `rp` argument wordt doorgegeven. For example, `"s_vncw"`, `"s_vncm"`, or `"s_vnc365"`. De waarde van het cookie is een combinatie van een Unix-tijdstempel die aangeeft wanneer de bezoekteller opnieuw wordt ingesteld, zoals het einde van de week, het einde van de maand of na 365 dagen inactiviteit. Het bevat ook het huidige bezoeknummer. Met deze insteekmodule wordt een ander cookie met de naam ingesteld `"s_ivc"` die na 30 minuten inactiviteit wordt ingesteld `true` en verlopen.

## Voorbeelden van aanroepen

### Voorbeeld 1

Voor een bezoeker die niet binnen de laatste 365 dagen aan de plaats is geweest, zal de volgende code s.prop1 aan de waarde van 1 plaatsen:

```js
s.prop1=s.getVisitNum();
```

### Voorbeeld 2

Voor een bezoeker die binnen 364 dagen na zijn/haar eerste bezoek naar de site terugkeert, zal de volgende code s.prop1 gelijk aan 2 plaatsen:

```js
s.prop1=s.getVisitNum(365);
```

Als deze bezoeker binnen 364 dagen na zijn/haar tweede bezoek terugkeert naar de site, stelt de volgende code s.prop1 in op 3:

```js
s.prop1=s.getVisitNum(365);
```

### Voorbeeld 3

Voor een bezoeker die binnen 179 dagen na zijn/haar eerste bezoek naar de site terugkeert, zal de volgende code s.prop1 gelijk aan 2 plaatsen:

```js
s.prop1=s.getVisitNum(180,false);
```

Als deze bezoeker echter 1 of meer dagen na zijn/haar tweede bezoek terugkeert naar de site, stelt de volgende code s.prop1 in op 1:

```js
s.prop1=s.getVisitNum(180,false);
```

Wanneer het tweede argument in de vraag aan vals is, zal de routine die bepaalt wanneer het bezoekaantal &quot;teruggesteld&quot;aan 1 zou moeten zijn &quot;x&quot;aantal dagen - in dit voorbeeld, 365 dagen - na het eerste bezoek van de bezoeker aan de plaats doen.

Wanneer het tweede argument gelijk is aan true (of helemaal niet is ingesteld), stelt de plug-in het bezoeknummer pas in op 1 na het aantal &quot;x&quot; dagen - in dit voorbeeld 365 dagen - van inactiviteit van de bezoeker.

### Voorbeeld 4

Voor alle bezoekers die voor het eerst in de huidige week - die op zondag begint - naar de site komen, zal de volgende code s.prop1 gelijk aan 1 plaatsen:

```js
s.prop1=s.getVisitNum("w");
```

### Voorbeeld 5

Voor alle bezoekers die voor het eerst in de huidige maand - die op de eerste dag van elke maand begint - naar de plaats komen zal de volgende code s.prop1 aan 1 plaatsen:

```js
s.prop1=s.getVisitNum("m");
```

Houd er rekening mee dat de getVisitNum-plug-in geen rekening houdt met op de detailhandel gebaseerde kalenders (bijvoorbeeld 4-5-4, 4-4-5, enz.)

### Voorbeeld 6

Voor alle bezoekers die voor het eerst in het huidige jaar - dat op 1 Januari begint - naar de plaats komen zal de volgende code s.prop1 aan 1 plaatsen:

```js
s.prop1=s.getVisitNum("y");
```

### Voorbeeld 7

Als u het bezoeknummer van een bezoeker voor de week, het bezoeknummer van een bezoeker voor de maand, en het bezoeknummer van een bezoeker voor het jaar - allen binnen verschillende variabelen van de Analyse - wilt volgen, zou u code moeten gebruiken die op het volgende lijkt:

```js
s.prop1=s.getVisitNum("w");
s.prop2=s.getVisitNum("m");
s.prop3=s.getVisitNum("y");
```

In dit geval maakt de plug-in drie verschillende cookies - één voor elk van de verschillende tijdsperioden - om het individuele bezoeknummer per tijdsperiode bij te houden.

## Versiehistorie

### 4.11 (30 september 2019)

* Probleem verholpen waarbij het `erp` argument expliciet was ingesteld op `false`.

### 4.1 (21 mei 2018)

* De plug-in `endOfDatePeriod` voor versie 1.1 is bijgewerkt.

### 4.0 (17 april 2018)

* Puntrelease (opnieuw gecompileerd, kleiner codeformaat).
* Cookieargumenten zijn verwijderd omdat de plug-in nu dynamisch cookies genereert op basis van het `rp` argument)

### 3.0 (5 juni 2016)

* Volledige revisie
* Alle eerdere oplossingen die beschikbaar zijn in verschillende versies van de `getVisitNum` plug-in, zijn gecombineerd.
