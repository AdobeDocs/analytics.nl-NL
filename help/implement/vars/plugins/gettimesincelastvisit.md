---
title: getTimeSinceLastVisit
description: Meet de hoeveelheid tijd die tussen twee bezoeken is verstreken.
translation-type: tm+mt
source-git-commit: 15e7ebe21413d6a56dac2c95dbdaf73efde3991e
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 1%

---


# Adobe-plug-in: getTimeSinceLastVisit

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `getTimeSinceLastVisit`-plug-in kunt u bijhouden hoelang een bezoeker na zijn laatste bezoek naar uw site is teruggekeerd.

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
   * Type handeling: getTimeSinceLastVisit initialiseren
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
/* Adobe Consulting Plugin: getTimeSinceLastVisit v2.0 */
function getTimeSinceLastVisit(){if(arguments&&"-v"===arguments[0])return{plugin:"getTimeSinceLastVisit",version:"2.0"};var h=function(){if("undefined"!==typeof window.s_c_il)for(var c=0,b;c<window.s_c_il.length;c++)if(b=window.s_c_il[c],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof h&&(h.contextData.getTimeSinceLastVisit="2.0");window.formatTime=window.formatTime||function(c,b,d){function f(b,d,c,e){if("string"!==typeof d)return!1;if("string"===typeof b)b=b.split(c||",");else if("object"!==typeof b)return!1;c=0;for(a=b.length;c<a;c++)if(1==e&&d===b[c]||d.toLowerCase()===b[c].toLowerCase())return!0;return!1}if(!("undefined"===typeof c||isNaN(c)||0>Number(c))){var e="";"string"===typeof b&&"d"===b||("string"!==typeof b||!f("h,m,s",b))&&86400<=c?(b=86400,e="days",d=isNaN(d)?1:b/(d*b)):"string"===typeof b&&"h"===b||("string"!==typeof b||!f("m,s",b))&&3600<=c?(b=3600,e="hours",d=isNaN(d)?4:b/(d*b)):"string"===typeof b&&"m"===b||("string"!==typeof b||!f("s",b))&&60<=c?(b=60,e="minutes",d=isNaN(d)?2:b/(d*b)):(b=1,e="seconds",d=isNaN(d)?.2:b/d);e=Math.round(c*d/b)/d+" "+e;0===e.indexOf("1 ")&&(e=e.substring(0,e.length-1));return e}};window.cookieWrite=window.cookieWrite||function(c,b,d){if("string"===typeof c){var f=window.location.hostname,e=window.location.hostname.split(".").length-1;if(f&&!/^[0-9.]+$/.test(f)){e=2<e?e:2;var k=f.lastIndexOf(".");if(0<=k){for(;0<=k&&1<e;)k=f.lastIndexOf(".",k-1),e--;k=0<k?f.substring(k):f}}g=k;b="undefined"!==typeof b?""+b:"";if(d||""===b)if(""===b&&(d=-60),"number"===typeof d){var h=new Date;h.setTime(h.getTime()+6E4*d)}else h=d;return c&&(document.cookie=encodeURIComponent(c)+"="+encodeURIComponent(b)+"; path=/;"+(d?" expires="+h.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof cookieRead)?cookieRead(c)===b:!1}};window.cookieRead=window.cookieRead||function(c){if("string"===typeof c)c=encodeURIComponent(c);else return"";var b=" "+document.cookie,d=b.indexOf(" "+c+"="),f=0>d?d:b.indexOf(";",d);return(c=0>d?"":decodeURIComponent(b.substring(d+2+c.length,0>f?b.length:f)))?c:""};h=new Date;var m=h.getTime(),n=cookieRead("s_tslv")||0,l=Math.round((m-n)/1E3);h.setTime(m+63072E6);cookieWrite("s_tslv",m,h);return n?1800<l||cookieRead("s_inv")?(cookieRead("s_inv")&&(l=cookieRead("s_inv")),cookieWrite("s_inv",l,30),"0"!==l?formatTime(l):"New Visitor"):"":(cookieWrite("s_inv","0",30),"New Visitor")};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De methode `getTimeSinceLastVisit` gebruikt geen argumenten. Het retourneert de hoeveelheid tijd die is verstreken sinds de bezoeker voor het laatst naar de site is gekomen. Deze tijd wordt als volgt geplakt:

* De tijd tussen 30 minuten en een uur sinds het laatste bezoek is ingesteld op de dichtstbijzijnde halftijdse benchmark. Bijvoorbeeld, `"30.5 minutes"`, `"53 minutes"`
* De tijd tussen een uur en een dag wordt afgerond aan de dichtstbijzijnde benchmark van kwartier. Bijvoorbeeld, `"2.25 hours"`, `"7.5 hours"`
* Tijd langer dan een dag wordt afgerond naar de dichtstbijzijnde dagbenchmark. Bijvoorbeeld, `"1 day"`, `"3 days"`, `"9 days"`, `"372 days"`
* Als een bezoeker niet eerder heeft bezocht of de verstreken tijd langer is dan twee jaar, wordt de waarde geplaatst aan `"New Visitor"`.

>[!NOTE]
>
>Deze insteekmodule retourneert alleen een waarde bij de eerste aanraking van een bezoek.

Deze plug-in maakt een cookie van de eerste partij met de naam `"s_tslv"` die is ingesteld op een Unix-tijdstempel van de huidige tijd. Het cookie verloopt na twee jaar inactiviteit.

## Voorbeelden van aanroepen

### Voorbeeld 1

Als een gloednieuwe bezoeker naar de site komt en de volgende code op de eerste pagina van het bezoek wordt uitgevoerd...

```javascript
s.prop1 = s.getTimeSinceLastVisit();
s.linkTrackVars = s.apl(s.linkTrackVars, "prop1") //ensures that prop1 will be included on the first hit of the visit
```

...de waarde van s.prop1 zal aan &quot;Nieuwe Bezoeker&quot;worden geplaatst.

Als dezelfde code op hetzelfde domein wordt uitgevoerd na 35 minuten inactiviteit, wordt de waarde van s.prop1 ingesteld op &quot;35 minuten&quot;.

Als dezelfde code op hetzelfde domein wordt uitgevoerd na 4 dagen van verdere inactiviteit, wordt de waarde van s.prop1 ingesteld op &quot;4 dagen&quot;.

## Versiehistorie

### 2.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 1.0 (16 april 2018)

* Puntrelease (opnieuw gecompileerde code en kleinere grootte).
* Code die is afgeleid van de `getDaysSinceLastVisit`-plug-in (nu vervangen en hernoemd).
* Gebruikt nu `formatTime` en `inList` stop-ins voor de terugkeerwaarde.
