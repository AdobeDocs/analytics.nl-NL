---
title: getVisitNum
description: Volg het huidige bezoeknummer van een bezoeker.
exl-id: 05b3f57c-7268-4585-a01e-583f462ff8df
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '1040'
ht-degree: 0%

---

# Adobe-plug-in: getVisitNum

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

De `getVisitNum` plug-in retourneert het bezoeknummer voor alle bezoekers die binnen het gewenste aantal dagen naar de site komen. Analysis Workspace heeft een dimensie &#39;Visit Number&#39; die vergelijkbare functionaliteit biedt. Adobe raadt u aan deze plug-in te gebruiken als u meer controle wilt over de manier waarop het bezoeknummer wordt verhoogd. Deze insteekmodule is niet nodig als de ingebouwde dimensie Visit Number in Analysis Workspace voldoende is voor uw rapportagevereisten.

## Plug-in installeren met tags in Adobe Experience Platform

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar het tabblad [!UICONTROL Extensions] en klik op de knop [!UICONTROL Catalog]
1. De extensie [!UICONTROL Common Analytics Plugins] installeren en publiceren
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: Geen
   * Gebeurtenis: Kern - Bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: Gebruikelijke plug-ins voor Analytics
   * Type handeling: Initialiseren getVisitNum
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met aangepaste code-editor

Als u de extensie van de plug-in niet wilt gebruiken, kunt u de aangepaste code-editor gebruiken.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder de uitbreiding van Adobe Analytics.
1. Breid [!UICONTROL Configure tracking using custom code] accordeon uit, die [!UICONTROL Open Editor] knoop openbaart.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

## Installeer de plug-in met AppMeasurement

Kopieer en plak de volgende code ergens in het AppMeasurement-bestand nadat het analytics tracking-object is geïnstantieerd (met [`s_gi`](../functions/s-gi.md)). Door opmerkingen en versienummers van de code in uw implementatie te behouden, kunt u Adobe doen met het oplossen van mogelijke problemen.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getVisitNum v4.2 */
function getVisitNum(rp,erp){var a=rp,l=erp;function m(c){return isNaN(c)?!1:(parseFloat(c)|0)===parseFloat(c)}function n(c){var b=new Date,e=isNaN(c)?0:Math.floor(c);b.setHours(23);b.setMinutes(59);b.setSeconds(59);"w"===c&&(e=6-b.getDay());if("m"===c){e=b.getMonth()+1;var a=b.getFullYear();e=(new Date(a?a:1970,e?e:1,0)).getDate()-b.getDate()}b.setDate(b.getDate()+e);"y"===c&&(b.setMonth(11),b.setDate(31));return b}if("-v"===a)return{plugin:"getVisitNum",version:"4.2"};var f=function(){if("undefined"!==typeof window.s_c_il)for(var c=0,b;c<window.s_c_il.length;c++)if(b=window.s_c_il[c],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof f&&(f.contextData.getVisitNum="4.2");window.cookieWrite=window.cookieWrite||function(c,b,e){if("string"===typeof c){var a=window.location.hostname,d=window.location.hostname.split(".").length-1;if(a&&!/^[0-9.]+$/.test(a)){d=2<d?d:2;var h=a.lastIndexOf(".");if(0<=h){for(;0<=h&&1<d;)h=a.lastIndexOf(".",h-1),d--;h=0<h?a.substring(h):a}}g=h;b="undefined"!==typeof b?""+b:"";if(e||""===b)if(""===b&&(e=-60),"number"===typeof e){var f=new Date;f.setTime(f.getTime()+6E4*e)}else f=e;return c&&(document.cookie=encodeURIComponent(c)+"="+encodeURIComponent(b)+"; path=/;"+(e?" expires="+f.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof window.cookieRead)?window.cookieRead(c)===b:!1}};window.cookieRead=window.cookieRead||function(c){if("string"===typeof c)c=encodeURIComponent(c);else return"";var b=" "+document.cookie,a=b.indexOf(" "+c+"="),d=0>a?a:b.indexOf(";",a);return(c=0>a?"":decodeURIComponent(b.substring(a+2+c.length,0>d?b.length:d)))?c:""};a=a?a:365;l="undefined"!==typeof l?!!l:m(a)?!0:!1;var p=(new Date).getTime();f=n(a);if(window.cookieRead("s_vnc"+a))var d=window.cookieRead("s_vnc"+a).split("&vn="),k=d[1];if(window.cookieRead("s_ivc"))return k?(window.cookieWrite("s_ivc",!0,30),k):"unknown visit number";if("undefined"!==typeof k)return k++,d=l&&m(a)?p+864E5*a:d[0],f.setTime(d),window.cookieWrite("s_vnc"+a,d+"&vn="+k,f),window.cookieWrite("s_ivc",!0,30),k;d=m(a)?p+864E5*a:n(a).getTime();window.cookieWrite("s_vnc"+a,d+"&vn=1",f);window.cookieWrite("s_ivc",!0,30);return"1"};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De methode `getVisitNum` gebruikt de volgende argumenten:

* **`rp`** (optioneel, geheel getal OF tekenreeks): Het aantal dagen voordat de teller van het bezoeknummer opnieuw wordt ingesteld.  Wordt standaard ingesteld op `365` wanneer niet ingesteld.
   * Wanneer dit argument `"w"` is, stelt de teller aan het eind van de week (deze Zaterdag om 11:59 PM) terug
   * Wanneer dit argument `"m"` is, stelt de teller aan het eind van de maand (de laatste dag van deze maand) terug
   * Als dit argument `"y"` is, wordt de teller aan het einde van het jaar opnieuw ingesteld (31 december)
* **`erp`** (optioneel, Booleaans): Wanneer het  `rp` argument een getal is, bepaalt dit argument of de vervaldatum van het bezoeknummer moet worden verlengd. Als de set wordt ingesteld op `true`, worden volgende hits op uw site de teller van het bezoeknummer opnieuw ingesteld. Indien ingesteld op `false`, worden volgende treffers voor uw site niet uitgebreid wanneer de teller van het bezoeknummer opnieuw wordt ingesteld. Wordt standaard ingesteld op `true`. Dit argument is niet geldig wanneer het argument `rp` een tekenreeks is.

Het aantal bezoekers neemt toe wanneer de bezoeker na 30 minuten inactiviteit terugkeert naar uw site. Als deze methode wordt aangeroepen, wordt een geheel getal geretourneerd dat het huidige bezoeknummer van de bezoeker vertegenwoordigt.

Deze plug-in stelt een cookie van de eerste fabrikant met de naam `"s_vnc[LENGTH]"` in, waarbij `[LENGTH]` de waarde is die wordt doorgegeven aan het argument `rp`. Bijvoorbeeld `"s_vncw"`, `"s_vncm"`, of `"s_vnc365"`. De waarde van het cookie is een combinatie van een Unix-tijdstempel die aangeeft wanneer de bezoekteller opnieuw wordt ingesteld, zoals het einde van de week, het einde van de maand of na 365 dagen inactiviteit. Het bevat ook het huidige bezoeknummer. Met deze insteekmodule wordt een ander cookie met de naam `"s_ivc"` ingesteld op `true` en vervalt het cookie na 30 minuten inactiviteit.

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

### 4.2 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 4.11 (30 september 2019)

* Probleem verholpen waarbij het argument `erp` expliciet werd ingesteld op `false`.

### 4.1 (21 mei 2018)

* De `endOfDatePeriod`-plug-in is bijgewerkt naar v1.1.

### 4.0 (17 april 2018)

* Puntrelease (opnieuw gecompileerd, kleiner codeformaat).
* Cookieargumenten zijn verwijderd omdat de plug-in nu dynamisch cookies genereert op basis van het argument `rp`)

### 3.0 (5 juni 2016)

* Volledige revisie
* Gecombineerd alle vorige oplossingen beschikbaar in diverse versies van de `getVisitNum` stop-in.
