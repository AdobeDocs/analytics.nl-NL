---
title: getPreviousValue
description: Hiermee wordt de laatste waarde opgehaald die in een variabele is doorgegeven.
translation-type: tm+mt
source-git-commit: a58e57438fdbac6f2e84c5f85388dff3a43dbd3b
workflow-type: tm+mt
source-wordcount: '881'
ht-degree: 0%

---


# Adobe-plug-in: getPreviousValue

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `getPreviousValue`-plug-in kunt u een variabele instellen op een waarde die bij een vorige hit is ingesteld. Deze insteekmodule is niet nodig als de implementatie alle gewenste waarden in de huidige hit bevat.

## De insteekmodule installeren met de Adobe Experience Platform Launch-extensie

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken.

1. Meld u met uw Adobe-id aan bij [launch.adobe.com](https://launch.adobe.com).
1. Klik op de gewenste eigenschap.
1. Ga naar het tabblad [!UICONTROL Extensions] en klik op de knop [!UICONTROL Catalog]
1. De extensie [!UICONTROL Common Analytics Plugins] installeren en publiceren
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: Geen
   * Gebeurtenis: Kern - Bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: Gebruikelijke plug-ins voor Analytics
   * Type handeling: getPreviousValue initialiseren
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met de aangepaste code-editor van Launch

Als u de extensie van de plug-in niet wilt gebruiken, kunt u de aangepaste code-editor gebruiken.

1. Meld u met uw Adobe-id aan bij [launch.adobe.com](https://launch.adobe.com).
1. Klik op de gewenste eigenschap.
1. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder de uitbreiding van Adobe Analytics.
1. Breid [!UICONTROL Configure tracking using custom code] accordeon uit, die [!UICONTROL Open Editor] knoop openbaart.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

## Installeer de plug-in met AppMeasurement

Kopieer en plak de volgende code ergens in het AppMeasurement-bestand nadat het analytics tracking-object is geïnstantieerd (met [`s_gi`](../functions/s-gi.md)). Door opmerkingen en versienummers van de code in uw implementatie te behouden, kunt u Adobe doen met het oplossen van mogelijke problemen.

```js
/* Adobe Consulting Plugin: getPreviousValue v3.0 */
function getPreviousValue(v,c){var k=v,d=c;if("-v"===k)return{plugin:"getPreviousValue",version:"3.0"};var a=function(){if("undefined"!==typeof window.s_c_il)for(var c=0,b;c<window.s_c_il.length;c++)if(b=window.s_c_il[c],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof a&&(a.contextData.getPreviousValue="3.0");window.cookieWrite=window.cookieWrite||function(c,b,f){if("string"===typeof c){var h=window.location.hostname,a=window.location.hostname.split(".").length-1;if(h&&!/^[0-9.]+$/.test(h)){a=2<a?a:2;var e=h.lastIndexOf(".");if(0<=e){for(;0<=e&&1<a;)e=h.lastIndexOf(".",e-1),a--;e=0<e?h.substring(e):h}}g=e;b="undefined"!==typeof b?""+b:"";if(f||""===b)if(""===b&&(f=-60),"number"===typeof f){var d=new Date;d.setTime(d.getTime()+6E4*f)}else d=f;return c&&(document.cookie=encodeURIComponent(c)+"="+encodeURIComponent(b)+"; path=/;"+(f?" expires="+d.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof cookieRead)?cookieRead(c)===b:!1}};window.cookieRead=window.cookieRead||function(c){if("string"===typeof c)c=encodeURIComponent(c);else return"";var b=" "+document.cookie,a=b.indexOf(" "+c+"="),d=0>a?a:b.indexOf(";",a);return(c=0>a?"":decodeURIComponent(b.substring(a+2+c.length,0>d?b.length:d)))?c:""};var l;d=d||"s_gpv";a=new Date;a.setTime(a.getTime()+18E5);window.cookieRead(d)&&(l=window.cookieRead(d));k?window.cookieWrite(d,k,a):window.cookieWrite(d,l,a);return l};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De methode `getPreviousValue` gebruikt de volgende argumenten:

* **`v`** (tekenreeks, vereist): De variabele met de waarde die u wilt doorgeven aan de volgende afbeeldingsaanvraag. Een veelgebruikte variabele is `s.pageName` om de vorige paginawaarde terug te winnen.
* **`c`** (tekenreeks, optioneel): De naam van het cookie waarin de waarde wordt opgeslagen.  Als dit argument niet is ingesteld, wordt standaard `"s_gpv"` ingesteld.

Wanneer u deze methode aanroept, wordt de tekenreekswaarde in het cookie geretourneerd. De insteekmodule herstelt dan de vervaldatum van het cookie en wijst er de variabelewaarde aan toe vanuit het argument `v`. Het cookie verloopt na 30 minuten inactiviteit.

## Voorbeelden van aanroepen

### Voorbeeld 1

De volgende code...

```js
s.prop7=s.getPreviousValue(s.pageName,"gpv_Page")
```

* Stelt s.prop7 eerst in op de waarde die in s.pageName is doorgegeven in het vorige afbeeldingsverzoek (dat wil zeggen de waarde die is opgeslagen in het cookie &quot;gpv_Page&quot;).
* De code herstelt vervolgens het cookie &quot;gpv_Page&quot;, waardoor deze gelijk is aan de huidige waarde van s.pageName
* Als s.pageName niet op het tijdstip wordt geplaatst deze code loopt, dan zal de code de vervaldatum voor de huidige waarde van het koekje terugstellen

### Voorbeeld 2

De volgende codesets s.prop7 is gelijk aan de laatste waarde die in s.pageName wordt overgegaan, maar slechts als event1 ook bevat binnen s.events is, zoals die via de insteekmodule inList wordt bepaald, op het tijdstip dat de vraag plaatsvindt.

```js
if(s.inList(s.events,"event1")) s.prop7=s.getPreviousValue(s.pageName,"gpv_Page");
```

### Voorbeeld 3

De volgende codesets s.prop7 is gelijk aan de laatste waarde die in s.pageName wordt doorgegeven, maar alleen als s.pageName momenteel op de pagina tegelijkertijd is ingesteld.

```js
if(s.pageName) s.prop7=s.getPreviousValue(s.pageName,"gpv_Page");
```

### Voorbeeld 4

De volgende codesets s.eVar10 is gelijk aan de waarde die in s.eVar1 is doorgegeven in de vorige afbeeldingsaanvraag.   De vorige eVar1-waarde zou zijn opgenomen in het cookie &quot;s_gpv&quot;.  De code stelt vervolgens het &#39;s_gpv&#39;-cookie in op de huidige waarde van s.eVar1.

```js
s.eVar10 = s.getPreviousValue(s.eVar1)
```

## Onwaarschijnlijke Kwartels

Als de variabele die aan het v-argument is gekoppeld, op een nieuwe waarde is ingesteld en de insteekmodule getPreviousValue wordt uitgevoerd MAAR een aanroep van de Analytics-server NIET tegelijkertijd wordt verzonden, wordt de nieuwe v-argumentwaarde de volgende keer dat de insteekmodule wordt uitgevoerd, nog steeds als de &quot;vorige waarde&quot; beschouwd.
Stel bijvoorbeeld dat de volgende code op de eerste pagina van het bezoek wordt uitgevoerd:

```js
s.pageName="home"
s.prop7=s.getPreviousValue(s.pageName,"gpv_Page")
s.t();
```

Deze code zou een servervraag veroorzaken waar het pageName argument aan &quot;huis&quot;gelijk is en het p7 (prop7) argument niet wordt geplaatst.  Nochtans, zou de vraag aan s.getPreviousValue de waarde van s.pageName (d.w.z. &quot;home&quot;) in het cookie dat in de aanroep is opgegeven (bijvoorbeeld het cookie &quot;gpv_Page&quot;).
Ga er nu van uit dat onmiddellijk daarna op dezelfde pagina de volgende code wordt uitgevoerd (om welke reden dan ook):

```js
s.pageName="happy value"
s.prop7=s.getPreviousValue(s.pageName,"gpv_Page")
```

Aangezien de functie s.t() niet in dit codeblok wordt uitgevoerd, wordt er geen andere afbeeldingsaanvraag gemaakt.  Wanneer de functiecode s.getPreviousValue() deze keer wordt uitgevoerd, wordt s.prop7 echter ingesteld op de vorige waarde van s.pageName (dat wil zeggen: &quot;home&quot;) en slaat vervolgens de nieuwe waarde van s.pageName (d.w.z. &quot;happy value&quot;) in het cookie &quot;gpv_Page&quot;.
Stel dat de bezoeker naar een andere pagina navigeert en de volgende code op deze pagina wordt uitgevoerd:

```js
s.pageName="page 2"
s.prop7=s.getPreviousValue(s.pageName,"gpv_Page")
s.t();
```

Wanneer de s.t () vraagfunctie loopt, zal het tot een beeldverzoek leiden waar s.pageName=&quot;pagina 2&quot;en s.prop7 aan &quot;gelukkig waarde&quot;is, die de waarde van s.pageName was toen de laatste vraag aan getPreviousValue plaatsvond.   De s.prop7 waarde van &quot;huis&quot;was nooit in om het even welk echt beeldverzoek ingesloten alhoewel &quot;huis&quot;de eerste waarde was die in s.pageName wordt overgegaan.

## Versiehistorie

### 3.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### v2.0 (7 oktober 2019)

* Puntrelease (volledige logica herschrijven).
