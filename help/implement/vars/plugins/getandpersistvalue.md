---
title: getAndPersistValue
description: Sla een waarde op die later kan worden opgehaald.
translation-type: tm+mt
source-git-commit: a2970e05abf0d1f963175db6e3554aa0e3034a70
workflow-type: tm+mt
source-wordcount: '916'
ht-degree: 0%

---


# Adobe-plug-in: getAndPersistValue

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `getAndPersistValue`-plug-in kunt u een waarde opslaan in een cookie die later tijdens een bezoek kan worden opgehaald. Deze rol komt overeen met de functie [!UICONTROL Storage duration] in Adobe Experience Platform Launch. Adobe raadt u aan deze plug-in te gebruiken als u automatisch een variabele Analytics tot dezelfde waarde wilt behouden in volgende hits nadat de variabele is ingesteld. Deze plug-in is niet nodig als de functie [!UICONTROL Storage duration] van Launch voldoende is of als u variabelen niet op dezelfde waarde hoeft in te stellen en aan te houden bij volgende treffers. Voor de ingebouwde persistentie van eVars is het gebruik van deze plug-in niet vereist, omdat deze variabelen de server-side voor-Adobe blijven.

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
   * Type handeling: getAndPersistValue initialiseren
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
/* Adobe Consulting Plugin: getAndPersistValue v3.0 (Requires AppMeasurement) */
function getAndPersistValue(vtp,cn,ex){var d=vtp,k=cn,l=ex;if("undefined"!==typeof d&&"-v"===d)return{plugin:"getAndPersistValue",version:"3.0"};var a=function(){if("undefined"!==typeof window.s_c_il)for(var c=0,b;c<window.s_c_il.length;c++)if(b=window.s_c_il[c],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof a&&(a.contextData.getAndPersistValue="3.0");window.cookieWrite=window.cookieWrite||function(c,b,f){if("string"===typeof c){var h=window.location.hostname,a=window.location.hostname.split(".").length-1;if(h&&!/^[0-9.]+$/.test(h)){a=2<a?a:2;var e=h.lastIndexOf(".");if(0<=e){for(;0<=e&&1<a;)e=h.lastIndexOf(".",e-1),a--;e=0<e?h.substring(e):h}}g=e;b="undefined"!==typeof b?""+b:"";if(f||""===b)if(""===b&&(f=-60),"number"===typeof f){var d=new Date;d.setTime(d.getTime()+6E4*f)}else d=f;return c&&(document.cookie=encodeURIComponent(c)+"="+encodeURIComponent(b)+"; path=/;"+(f?" expires="+d.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof cookieRead)?cookieRead(c)===b:!1}};window.cookieRead=window.cookieRead||function(c){if("string"===typeof c)c=encodeURIComponent(c);else return"";var b=" "+document.cookie,a=b.indexOf(" "+c+"="),d=0>a?a:b.indexOf(";",a);return(c=0>a?"":decodeURIComponent(b.substring(a+2+c.length,0>d?b.length:d)))?c:""};a=new Date;k=k?k:"s_gapv";(l=l?l:0)?a.setTime(a.getTime()+864E5*l):a.setTime(a.getTime()+18E5);"undefined"!==typeof d&&d||(d=cookieRead(k));cookieWrite(k,d,a);return d};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De methode `getAndPersist` gebruikt de volgende argumenten:

* **`vtp`** (vereist): De waarde die van pagina tot pagina moet worden behouden
* **`cn`** (optioneel): De naam van het cookie waarin de waarde wordt opgeslagen. Als dit argument niet is ingesteld, krijgt het cookie de naam `"s_gapv"`
* **`ex`** (optioneel): Het aantal dagen voordat de cookie vervalt. Als dit argument `0` is of niet wordt geplaatst, verloopt het koekje aan het eind van het bezoek (30 minuten van inactiviteit).

Als de variabele in het argument `vtp` wordt geplaatst, dan plaatst het elektrische toestel het koekje dan keert de koekjeswaarde terug. Als de variabele in het argument `vtp` niet wordt geplaatst, dan keert de stop-binnen slechts de koekjeswaarde terug.

## Voorbeelden

### Voorbeeld 1

Met de volgende code wordt eVar21 ingesteld op de waarde &quot;hello&quot;.  De code zal dan ev21gapv koekje, dat over 28 dagen zal verlopen, gelijk aan de waarde van eVar21 (d.w.z. &quot;hallo&quot;).  De code stelt vervolgens (re)eVar21 in op de waarde van het ev21gapv-cookie.

```js
s.eVar21 = "hello";
s.eVar21 = s.getAndPersistValue(s.eVar21,"ev21gapv",28);
```

### Voorbeeld 2

Stel dat eVar21 nog niet is ingesteld op de huidige pagina, maar in de afgelopen 28 dagen is ingesteld op &quot;hello&quot; op een vorige pagina.   Met de volgende code wordt alleen eVar21 ingesteld op de waarde van het ev21gapv-cookie (d.w.z. &quot;hallo&quot;).  De ev21gapv-cookie wordt niet opnieuw ingesteld omdat eVar21 niet is ingesteld op de huidige pagina voordat de functie werd aangeroepen.

```js
s.eVar21 = s.getAndPersistValue(s.eVar21,"ev21gapv",28);
```

### Voorbeeld 2

Stel dat eVar21 nog niet is ingesteld op de huidige pagina, maar in de afgelopen 28 dagen is ingesteld op &quot;hello&quot; op een vorige pagina.  Met de volgende code wordt alleen prop35 ingesteld op de waarde van het ev21gapv-cookie (d.w.z. &quot;hallo&quot;).  Er wordt geen eVar21 ingesteld.

```js
s.prop35 = s.getAndPersistValue(s.eVar21,"ev21gapv",28);
```

### Voorbeeld 4

Met de volgende code wordt eVar21 gelijk ingesteld aan de waarde &quot;howdy&quot;.  De code stelt vervolgens de ev21gapv-cookie, die over 28 dagen verloopt, in (of herstelt deze) op de waarde van eVar21 (d.w.z. &quot;howdy&quot;).  De code stelt dan prop35 in op de waarde van het ev21gapv-cookie (dat wil zeggen &quot;howdy&quot;).

```js
s.eVar21 = "howdy";
s.prop35 = s.getAndPersistValue(s.eVar21,"ev21gapv",28);
```

### Voorbeeld 5

Stel dat s.eVar21 de laatste 28 dagen op geen enkele pagina is ingesteld.  De volgende code stelt s.eVar21 gelijk aan niets omdat het ev21gapv-cookie 28 dagen na de laatste set zou zijn verlopen.

```js
s.eVar21 = s.getAndPersistValue(s.eVar21,"ev21gapv",28);
```

### Voorbeeld 6

Met de volgende code wordt eVar30 gelijk gesteld aan &quot;shopping&quot;.  Vervolgens wordt het s_gapv-cookie, dat aan het einde van de browsersessie vervalt, ingesteld op de waarde van s.eVar30 (dus &quot;winkelen&quot;).  Vervolgens wordt s.eVar30 ingesteld op de waarde van het s_gapv-cookie (de aanroep getAndPersistValue retourneert de waarde van het s_gapv-cookie, die in dit geval &#39;shopping&#39; is).

```js
s.eVar30 = "shopping";
s.eVar30 = s.getAndPersistValue(s.eVar30);
```

Als s.eVar30 niet aan een expliciete waarde op om het even welke extra pagina&#39;s wordt geplaatst die tijdens de zitting worden gezien maar (in doPlugins) via de volgende code wordt geplaatst...

```js
s.eVar30 = s.getAndPersistValue(s.eVar30);
```

...s.eVar30 wordt ingesteld op &quot;shopping&quot; (d.w.z. de aanhoudend waarde van het s_gapv cookie)

## Versiehistorie

### 3.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 2.0 (16 april 2018)

* Puntrelease (kleinere codegrootte)
* Als u 0 in het argument `ex` doorgeeft, wordt de vervaldatum na 30 minuten inactiviteit gedwongen en niet na afloop van de browsersessie.

### 1.0 (18 januari 2016)

* Eerste release.
