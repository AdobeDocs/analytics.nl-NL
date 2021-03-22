---
title: getVisitDuration
description: Houd bij hoeveel tijd een bezoeker tot dusver op de site is geweest.
translation-type: tm+mt
source-git-commit: ca8e563118dcc74dfa718bd203db295faf4e9aa6
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---


# Adobe-plug-in: getVisitDuration

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `getVisitDuration`-plug-in wordt de hoeveelheid tijd in minuten bijgehouden die de bezoeker tot dan toe op de site heeft doorgebracht. Adobe raadt u aan deze plug-in te gebruiken als u de cumulatieve tijd op de site tot dat moment wilt bijhouden of als u wilt bijhouden hoeveel tijd het kost om een activiteit uit te voeren. Deze plug-in houdt de hoeveelheid tijd tussen gebeurtenissen niet bij; Als u deze functionaliteit wilt gebruiken, gebruikt u de [`getTimeBetweenEvents`](gettimebetweenevents.md) plug-in.

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
   * Type handeling: getVisitDuration initialiseren
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
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getVisitDuration v2.1 */
function getVisitDuration(){if(arguments&&"-v"===arguments[0])return{plugin:"getVisitDuration",version:"2.1"};var d=function(){if("undefined"!==typeof window.s_c_il)for(var c=0,b;c<window.s_c_il.length;c++)if(b=window.s_c_il[c],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof d&&(d.contextData.getVisitDuration="2.1");window.cookieWrite=window.cookieWrite||function(c,b,f){if("string"===typeof c){var h=window.location.hostname,a=window.location.hostname.split(".").length-1;if(h&&!/^[0-9.]+$/.test(h)){a=2<a?a:2;var e=h.lastIndexOf(".");if(0<=e){for(;0<=e&&1<a;)e=h.lastIndexOf(".",e-1),a--;e=0<e?h.substring(e):h}}g=e;b="undefined"!==typeof b?""+b:"";if(f||""===b)if(""===b&&(f=-60),"number"===typeof f){var d=new Date;d.setTime(d.getTime()+6E4*f)}else d=f;return c&&(document.cookie=encodeURIComponent(c)+"="+encodeURIComponent(b)+"; path=/;"+(f?" expires="+d.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof cookieRead)?cookieRead(c)===b:!1}};window.cookieRead=window.cookieRead||function(c){if("string"===typeof c)c=encodeURIComponent(c);else return"";var b=" "+document.cookie,a=b.indexOf(" "+c+"="),d=0>a?a:b.indexOf(";",a);return(c=0>a?"":decodeURIComponent(b.substring(a+2+c.length,0>d?b.length:d)))?c:""};d=(new Date).getTime();var k=cookieRead("s_dur"),a=0;if(isNaN(k)||18E5<d-k)k=d;a=d-k;cookieWrite("s_dur",k+"",30);if(0===a)return"first hit of visit";a=Math.floor(a/6E4);return 0===a?"less than a minute":1===a?"1 minute":a+" minutes"};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De methode `getVisitDuration` gebruikt geen argumenten. Deze geeft een van de volgende waarden:

* `"first hit of visit"`
* `"less than a minute"`
* `"1 minute"`
* `"[x] minutes"` (waarbij  `[x]` het aantal minuten is dat is verstreken sinds de bezoeker op de locatie is aangeland)

Deze plug-in maakt een cookie van de eerste partij met de naam `"s_dur"`. Dit is het aantal milliseconden dat is verstreken sinds de bezoeker op de site is beland. Het cookie verloopt na 30 minuten inactiviteit.

## Voorbeelden van aanroepen

### Voorbeeld 1

De volgende code...

```js
s.eVar10 = s.getVisitDuration();
```

...stelt eVar10 altijd in op het aantal minuten dat is verstreken sinds de bezoeker de site heeft aangeland

### Voorbeeld 2

De volgende code...

```js
if(s.inList(s.events, "purchase")) s.eVar10 = s.getVisitDuration();
```

...gebruikt de insteekmodule inList om te controleren of de variabele events de aankoopgebeurtenis bevat.  In dat geval wordt eVar10 ingesteld op het aantal minuten tussen het begin van het bezoek van de bezoeker en het tijdstip van aankoop.

### Voorbeeld 3

De volgende code...

```js
s.prop10 = s.getVisitDuration();
```

...stelt prop10 altijd in op het aantal minuten dat is verstreken sinds de bezoeker de site heeft aangeland.  Dit is handig als voor prop10 het plakken is ingeschakeld.  Als u de metrische waarde ‘exits’ toevoegt aan het rapport prop10, wordt een korrelig, ‘scatterplot’ weergegeven met de melding hoe lang een bezoek duurde in minuten voordat een bezoeker de site verliet.

## Versiehistorie

### 2.1 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 2.0 (2 mei 2018)

* Puntrelease (volledige heranalyse/herschrijven van plug-in).
