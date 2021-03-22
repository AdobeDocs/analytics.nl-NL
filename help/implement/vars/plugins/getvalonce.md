---
title: getValOnce
description: Voorkomen dat een variabele Analytics tweemaal achter elkaar op dezelfde waarde wordt ingesteld.
translation-type: tm+mt
source-git-commit: 5a81754ca6137d7bc1e790fe537acbb4bbdb8efb
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 1%

---


# Adobe-plug-in: getValOnce

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de insteekmodule `getValOnce` voorkomt u dat een variabele meer dan één keer dezelfde waarde heeft. Adobe raadt u aan deze plug-in te gebruiken als u gevallen wilt dedupliceren waarin een bezoeker een pagina vernieuwt of een bepaalde pagina meerdere keren bezoekt. Deze plug-in is niet nodig als u zich geen zorgen maakt over de metrische waarde &#39;Voorvallen&#39; in Analysis Workspace.

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
   * Type handeling: getValOnce initialiseren
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
/* Adobe Consulting Plugin: getValOnce v3.0 (Requires AppMeasurement) */
function getValOnce(vtc,cn,et,ep){var e=vtc,k=cn,l=et,m=ep;if(arguments&&"-v"===arguments[0])return{plugin:"getValOnce",version:"3.0"};var c=function(){if("undefined"!==typeof window.s_c_il)for(var b=0,a;b<window.s_c_il.length;b++)if(a=window.s_c_il[b],a._c&&"s_c"===a._c)return a}();"undefined"!==typeof c&&(c.contextData.getValOnce="3.0");window.cookieWrite=window.cookieWrite||function(b,a,d){if("string"===typeof b){var h=window.location.hostname,c=window.location.hostname.split(".").length-1;if(h&&!/^[0-9.]+$/.test(h)){c=2<c?
c:2;var f=h.lastIndexOf(".");if(0<=f){for(;0<=f&&1<c;)f=h.lastIndexOf(".",f-1),c--;f=0<f?h.substring(f):h}}g=f;a="undefined"!==typeof a?""+a:"";if(d||""===a)if(""===a&&(d=-60),"number"===typeof d){var e=new Date;e.setTime(e.getTime()+6E4*d)}else e=d;return b&&(document.cookie=encodeURIComponent(b)+"="+encodeURIComponent(a)+"; path=/;"+(d?" expires="+e.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof cookieRead)?cookieRead(b)===a:!1}};window.cookieRead=window.cookieRead||function(b){if("string"===
typeof b)b=encodeURIComponent(b);else return"";var a=" "+document.cookie,d=a.indexOf(" "+b+"="),c=0>d?d:a.indexOf(";",d);return(b=0>d?"":decodeURIComponent(a.substring(d+2+b.length,0>c?a.length:c)))?b:""};return e&&(k=k||"s_gvo",l=l||0,m="m"===m?6E4:864E5,e!==this.c_r(k))?(c=new Date,c.setTime(c.getTime()+l*m),cookieWrite(k,e,0===l?0:m),e):""};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De methode `getValOnce` gebruikt de volgende argumenten:

* **`vtc`** (vereist, tekenreeks): De variabele die moet worden gecontroleerd en gecontroleerd of deze eerder is ingesteld op een identieke waarde
* **`cn`** (optioneel, tekenreeks): De naam van het cookie dat de te controleren waarde bevat. Heeft als standaardwaarde `"s_gvo"`
* **`et`** (optioneel, geheel getal): De vervaldatum van de cookie in dagen (of minuten, afhankelijk van het  `ep` argument). Wordt standaard ingesteld op `0`, die aan het einde van de browsersessie vervalt
* **`ep`** (optioneel, tekenreeks): Stel dit argument alleen in als het  `et` argument ook is ingesteld. Stel dit argument in op `"m"` als u het argument `et` in minuten in plaats van dagen wilt laten verlopen. Standaard ingesteld op `"d"`, die het argument `et` in dagen instelt.

Wanneer het argument `vtc` en de waarde van het cookie overeenkomen, retourneert deze methode een lege tekenreeks. Wanneer het argument `vtc` en de waarde van het cookie niet overeenkomen, retourneert de methode het argument `vtc` als een tekenreeks.

## Voorbeelden van aanroepen

### Voorbeeld 1

Gebruik deze vraag om de zelfde waarde te verhinderen binnen aan s.campagne meer dan eens in een rij voor volgende 30 dagen wordt overgegaan:

```js
s.campaign=s.getValOnce(s.campaign,"s_campaign",30);
```

In de bovengenoemde vraag, zal het elektrische toestel eerst de waarde reeds in het s_campagne koekje met de waarde vergelijken die uit de huidige s.campagne variabele komt.   Als een gelijke niet wordt gemaakt, zal de stop-binnen het s_campagne koekje gelijk aan de nieuwe waarde plaatsen die uit s.campagne komt en dan de nieuwe waarde terugkeren.   Deze vergelijking vindt plaats in de komende 30 dagen

### Voorbeeld 2

Gebruik deze aanroep om te voorkomen dat dezelfde waarde tijdens de gehele sessie wordt ingesteld:

```js
s.eVar2=s.getValOnce(s.eVar2,"s_ev2",0,"m");
```

Met deze code wordt voorkomen dat dezelfde waarde meerdere keren achter een gebruikerssessie in s.eVar2 wordt doorgegeven.  Het negeert ook de &quot;m&quot;waarde in het argument (aan het eind van de vraag) aangezien de vervaltijd aan 0 wordt geplaatst.   De code slaat ook de vergelijkingswaarde in het s_ev2 koekje op.

## Versiehistorie

### 3.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 2,01

* Probleem verholpen met het schrijven van cookies.

### 2,0

* Puntrelease (opnieuw gecompileerd, kleiner codeformaat).

### 1,1

* De optie voor het kiezen van minuten of dagen voor de vervaldatum is toegevoegd via de parameter `t`.
* Correctie van het bereik van de variabele `k` die wordt gebruikt om het tot stop-binnen slechts te beperken. Deze wijziging voorkomt mogelijke interferentie met andere code op de pagina.
