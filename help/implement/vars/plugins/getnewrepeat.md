---
title: getNewRepeat
description: Traceeractiviteiten van nieuwe versus herhaalde bezoekers.
exl-id: 8f64e176-1926-4cb1-bfae-09d7e2c015ae
source-git-commit: 13060d08c8ffff01d8dae379e090c53e61fa6476
workflow-type: tm+mt
source-wordcount: '774'
ht-degree: 0%

---

# Adobe-plug-in: getNewRepeat

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de insteekmodule `getNewRepeat` kunt u bepalen of een bezoeker van de site een nieuwe bezoeker of een herhaalde bezoeker binnen een gewenst aantal dagen is. Adobe raadt u aan deze insteekmodule te gebruiken als u bezoekers wilt identificeren als &#39;nieuw&#39; met behulp van een aangepast aantal dagen. Deze insteekmodule is niet nodig als de afmetingen van de nieuwe bezoeker/de nieuwe bezoeker in Analysis Workspace voldoen aan de behoeften van uw organisatie.

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
   * Type handeling: getNewRepeat initialiseren
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
/* Adobe Consulting Plugin: getNewRepeat v3.0 (Requires AppMeasurement) */
function getNewRepeat(d){var a=d;if("-v"===a)return{plugin:"getNewRepeat",version:"3.0"};var d=function(){if("undefined"!==typeof window.s_c_il)for(var c=0,b;c<window.s_c_il.length;c++)if(b=window.s_c_il[c],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof d&&(d.contextData.getNewRepeat="3.0");window.cookieWrite=window.cookieWrite||function(c,b,f){if("string"===typeof c){var h=window.location.hostname,a=window.location.hostname.split(".").length-1;if(h&&!/^[0-9.]+$/.test(h)){a=2<a?a:2;var e=h.lastIndexOf(".");if(0<=e){for(;0<=e&&1<a;)e=h.lastIndexOf(".",e-1),a--;e=0<e?h.substring(e):h}}g=e;b="undefined"!==typeof b?""+b:"";if(f||""===b)if(""===b&&(f=-60),"number"===typeof f){var d=new Date;d.setTime(d.getTime()+6E4*f)}else d=f;return c&&(document.cookie=encodeURIComponent(c)+"="+encodeURIComponent(b)+"; path=/;"+(f?" expires="+d.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof cookieRead)?cookieRead(c)===b:!1}};window.cookieRead=window.cookieRead||function(c){if("string"===typeof c)c=encodeURIComponent(c);else return"";var b=" "+document.cookie,a=b.indexOf(" "+c+"="),d=0>a?a:b.indexOf(";",a);return(c=0>a?"":decodeURIComponent(b.substring(a+2+c.length,0>d?b.length:d)))?c:""};a=a?a:30;d="s_nr"+a;var k=new Date,m=cookieRead(d),n=m.split("-"),l=k.getTime();k.setTime(l+864E5*a);if(""===m||18E5>l-n[0]&&"New"===n[1])return cookieWrite(d,l+"-New",k),"New";cookieWrite(d,l+"-Repeat",k);return"Repeat"};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De methode `getNewRepeat` gebruikt de volgende argumenten:

* **`d`** (geheel getal, optioneel): Het minimumaantal dagen dat is vereist tussen bezoeken waarop bezoekers terugkeren naar  `"New"`. Als dit argument niet is ingesteld, wordt het standaard ingesteld op 30 dagen.

Deze methode retourneert de waarde van `"New"` als de cookie die door de plug-in is ingesteld, niet bestaat of is verlopen. De waarde `"Repeat"` wordt geretourneerd als het cookie dat door de plug-in is ingesteld, bestaat en de tijd sinds de huidige hit en de tijd die in het cookie is ingesteld, langer is dan 30 minuten. Deze methode keert de zelfde waarde voor een volledig bezoek terug.

Deze plug-in gebruikt een cookie met de naam `"s_nr[LENGTH]"`, waarbij `[LENGTH]` gelijk is aan het argument `d`. Het cookie bevat een Unix-tijdstempel die de huidige tijd en de huidige status van de bezoeker (`"New"` of `"Repeat"`) vertegenwoordigt.

## Voorbeelden van aanroepen

### Voorbeeld 1

De volgende code stelt `eVar1` in op de waarde van `"New"` voor nieuwe bezoekers en blijft `eVar1` instellen op de waarde van `"New"` (met elke nieuwe oproep) gedurende de rest van het bezoek van de bezoeker aan de site.

```js
s.eVar1 = getNewRepeat();
```

### Voorbeeld 2

Als de bezoeker op een willekeurig moment van 31 minuten tot 30 dagen sinds de laatste keer dat `getNewRepeat()` werd aangeroepen, terugkeert naar de site, stelt de volgende code `eVar1` in op de waarde van `"Repeat"` en blijft `eVar1` op de waarde van `"Repeat"` (met elke nieuwe aanroep) gedurende het resterende gedeelte van het bezoek van de bezoeker aan de site.

```js
s.eVar1 = getNewRepeat();
```

### Voorbeeld 3

Als de bezoeker niet minstens 30 dagen sinds de laatste keer `getNewRepeat()` werd geroepen is geweest, plaatst de volgende code `eVar1` aan de waarde van `"New"` en blijft `eVar1` aan de waarde van `"New"` (met elke nieuwe vraag) tijdens het resterende deel van het bezoek van de bezoeker aan de plaats plaatsen.

```js
s.eVar1 = getNewRepeat();
```

### Voorbeeld 4

Als de bezoeker 31 minuten tot 365 dagen (d.w.z. 1 jaar) sinds de laatste keer dat `getNewRepeat()` werd aangeroepen, terugkeert naar de site, stelt de volgende code `eVar1` in op de waarde van `"Repeat"` en blijft `eVar1` op de waarde van `"Repeat"` (met elke nieuwe aanroep) gedurende het resterende bezoek van de bezoeker aan de site.

```js
s.eVar1 = getNewRepeat(365);
```

### Voorbeeld 5

Als de bezoeker niet minstens 365 dagen (d.w.z. 1 jaar) sinds de laatste keer `getNewRepeat()` werd geroepen, plaatst de volgende code `eVar1` aan de waarde van `"New"` en blijft `eVar1` aan de waarde van `"New"` (met elke nieuwe vraag) tijdens het resterende deel van het bezoek van de bezoeker aan de plaats plaatsen.

```js
s.eVar1 = getNewRepeat(365);
```

## Versiehistorie

### 3.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 2.1 (30 september 2019)

* Herschikking van JavaScript-logica om de grootte van insteekmodules te verkleinen

### 2.0 (16 april 2018)

* Opnieuw gecompileerd met kleinere codegrootte
* De mogelijkheid om de cookie een naam te geven, is verwijderd. De plug-in geeft het cookie nu dynamisch een naam op basis van de waarde die is doorgegeven aan het argument `d`.
