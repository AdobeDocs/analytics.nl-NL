---
title: getVisitNum
description: Volg het huidige bezoeknummer van een bezoeker.
feature: Appmeasurement Implementation
exl-id: 05b3f57c-7268-4585-a01e-583f462ff8df
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# Adobe-insteekmodule: getVisitNum

{{plug-in}}

De plug-in `getVisitNum` retourneert het bezoeknummer voor alle bezoekers die binnen het gewenste aantal dagen naar de site komen. Analysis Workspace heeft een dimensie &#39;Visit Number&#39; die vergelijkbare functionaliteit biedt. Adobe raadt u aan deze plug-in te gebruiken als u meer controle wilt over de verhoging van het bezoeknummer. Deze insteekmodule is niet nodig als de ingebouwde dimensie Visit Number in Analysis Workspace voldoende is voor uw rapportagevereisten.

## De insteekmodule installeren met de extensie Web SDK

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken voor de webversie van SDK.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op **[!UICONTROL Tags]** aan de linkerkant en klik op de gewenste eigenschap Tag.
1. Klik op **[!UICONTROL Extensions]** aan de linkerkant en klik vervolgens op de tab **[!UICONTROL Catalog]**
1. Zoek en installeer de extensie **[!UICONTROL Common Web SDK Plugins]** .
1. Klik op **[!UICONTROL Data Elements]** aan de linkerkant en klik op het gewenste gegevenselement.
1. Stel de gewenste naam van het gegevenselement in met de volgende configuratie:
   * Extensie: algemene SDK-plug-ins voor het web
   * Gegevenselement: `getVisitNum`
1. Stel de gewenste parameters rechts in.
1. Sla de wijzigingen in het gegevenselement op en publiceer deze.

## De insteekmodule handmatig installeren voor de Web SDK

Deze insteekmodule wordt nog niet ondersteund voor gebruik in een handmatige implementatie van de Web SDK.

## De insteekmodule installeren met de Adobe Analytics-extensie

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken in Adobe Analytics.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop [!UICONTROL Catalog]
1. De extensie [!UICONTROL Common Analytics Plugins] installeren en publiceren
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: geen
   * Event: Core - bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: veelgebruikte plug-ins voor Analytics
   * Type handeling: initialiseren getVisitNum
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met aangepaste code-editor

Als u niet de Gemeenschappelijke Insteekmodule van Analytics wilt gebruiken, kunt u de redacteur van de douanecode gebruiken.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste eigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder de extensie Adobe Analytics.
1. Vouw de accordeon [!UICONTROL Configure tracking using custom code] uit, zodat de knop [!UICONTROL Open Editor] zichtbaar wordt.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

## Plug-in installeren met AppMeasurement

Kopieer en plak de volgende code ergens in het AppMeasurement-bestand nadat het object Analytics tracking is geïnstantieerd (met [`s_gi`](../functions/s-gi.md) ). Door opmerkingen en versienummers van de code in uw implementatie te behouden, helpt Adobe bij het oplossen van mogelijke problemen.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getVisitNum v4.2 */
function getVisitNum(rp,erp){var a=rp,l=erp;function m(c){return isNaN(c)?!1:(parseFloat(c)|0)===parseFloat(c)}function n(c){var b=new Date,e=isNaN(c)?0:Math.floor(c);b.setHours(23);b.setMinutes(59);b.setSeconds(59);"w"===c&&(e=6-b.getDay());if("m"===c){e=b.getMonth()+1;var a=b.getFullYear();e=(new Date(a?a:1970,e?e:1,0)).getDate()-b.getDate()}b.setDate(b.getDate()+e);"y"===c&&(b.setMonth(11),b.setDate(31));return b}if("-v"===a)return{plugin:"getVisitNum",version:"4.2"};var f=function(){if("undefined"!==typeof window.s_c_il)for(var c=0,b;c<window.s_c_il.length;c++)if(b=window.s_c_il[c],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof f&&(f.contextData.getVisitNum="4.2");window.cookieWrite=window.cookieWrite||function(c,b,e){if("string"===typeof c){var a=window.location.hostname,d=window.location.hostname.split(".").length-1;if(a&&!/^[0-9.]+$/.test(a)){d=2<d?d:2;var h=a.lastIndexOf(".");if(0<=h){for(;0<=h&&1<d;)h=a.lastIndexOf(".",h-1),d--;h=0<h?a.substring(h):a}}g=h;b="undefined"!==typeof b?""+b:"";if(e||""===b)if(""===b&&(e=-60),"number"===typeof e){var f=new Date;f.setTime(f.getTime()+6E4*e)}else f=e;return c&&(document.cookie=encodeURIComponent(c)+"="+encodeURIComponent(b)+"; path=/;"+(e?" expires="+f.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof window.cookieRead)?window.cookieRead(c)===b:!1}};window.cookieRead=window.cookieRead||function(c){if("string"===typeof c)c=encodeURIComponent(c);else return"";var b=" "+document.cookie,a=b.indexOf(" "+c+"="),d=0>a?a:b.indexOf(";",a);return(c=0>a?"":decodeURIComponent(b.substring(a+2+c.length,0>d?b.length:d)))?c:""};a=a?a:365;l="undefined"!==typeof l?!!l:m(a)?!0:!1;var p=(new Date).getTime();f=n(a);if(window.cookieRead("s_vnc"+a))var d=window.cookieRead("s_vnc"+a).split("&vn="),k=d[1];if(window.cookieRead("s_ivc"))return k?(window.cookieWrite("s_ivc",!0,30),k):"unknown visit number";if("undefined"!==typeof k)return k++,d=l&&m(a)?p+864E5*a:d[0],f.setTime(d),window.cookieWrite("s_vnc"+a,d+"&vn="+k,f),window.cookieWrite("s_ivc",!0,30),k;d=m(a)?p+864E5*a:n(a).getTime();window.cookieWrite("s_vnc"+a,d+"&vn=1",f);window.cookieWrite("s_ivc",!0,30);return"1"};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De functie `getVisitNum` gebruikt de volgende argumenten:

* **`rp`** (optioneel, geheel getal OF tekenreeks): Het aantal dagen voordat de teller van het bezoeknummer opnieuw wordt ingesteld.  Wordt standaard ingesteld op `365` wanneer niet ingesteld.
   * Wanneer dit argument `"w"` is, wordt de teller aan het einde van de week opnieuw ingesteld (deze zaterdag om 23:59 uur)
   * Wanneer dit argument `"m"` is, wordt de teller aan het einde van de maand (de laatste dag van deze maand) opnieuw ingesteld
   * Wanneer dit argument `"y"` is, wordt de teller aan het einde van het jaar opnieuw ingesteld (31 december)
* **`erp`** (optioneel, Boolean): Wanneer het argument `rp` een getal is, bepaalt dit argument of de vervaldatum van het bezoeknummer moet worden verlengd. Als deze optie is ingesteld op `true` , worden bij volgende treffers naar uw site de teller van het bezoeknummer opnieuw ingesteld. Indien ingesteld op `false` , worden volgende treffers voor uw site niet uitgebreid wanneer de teller van het bezoeknummer opnieuw wordt ingesteld. Wordt standaard ingesteld op `true` . Dit argument is niet geldig wanneer het argument `rp` een tekenreeks is.

Het aantal bezoekers neemt toe wanneer de bezoeker na 30 minuten inactiviteit terugkeert naar uw site. Als deze functie wordt aangeroepen, wordt een geheel getal geretourneerd dat het huidige bezoeknummer van de bezoeker vertegenwoordigt.

Deze plug-in stelt een cookie van de eerste partij in met de naam `"s_vnc[LENGTH]"` , waarbij `[LENGTH]` de waarde is die aan het argument `rp` wordt doorgegeven. Bijvoorbeeld `"s_vncw"` , `"s_vncm"` of `"s_vnc365"` . De waarde van het cookie is een combinatie van een Unix-tijdstempel die aangeeft wanneer de bezoekteller opnieuw wordt ingesteld, zoals het einde van de week, het einde van de maand of na 365 dagen inactiviteit. Het bevat ook het huidige bezoeknummer. Deze plug-in stelt een andere cookie met de naam `"s_ivc"` in die op `true` is ingesteld en na 30 minuten inactiviteit vervalt.

## Voorbeelden

```js
// Sets prop4 to the visit number, storing the value in a cookie that expires in 365 days
// The cookie value is reset only if there are 365+ days of inactivity or the visitor clears their cookies.
s.prop4 = getVisitNum();

// Sets eVar4 to the visit number, storing the value in a cookie that expires in 200 days
// The cookie value is reset only if there are 200+ days of inactivity or the visitor clears their cookies.
s.eVar4 = getVisitNum(200);

// Sets eVar16 to the visit number, storing the value in a cookie that expires in 90 days.
// The cookie value is reset after 90 days, regardless of how many visits that happen in those 90 days.
s.eVar16 = getVisitNum(90,false);

// Track the visit number unique to the week, month, and year, all in separate variables
// The plug-in automatically creates three separate cookies to track these values
s.prop1 = getVisitNum("w");
s.prop2 = getVisitNum("m");
s.prop3 = getVisitNum("y");
```

## Versiehistorie

### 4.2 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 4.11 (30 september 2019)

* Probleem verholpen waarbij het argument `erp` expliciet was ingesteld op `false` .

### 4.1 (21 mei 2018)

* De plug-in `endOfDatePeriod` is bijgewerkt naar v1.1.

### 4.0 (17 april 2018)

* Puntrelease (opnieuw gecompileerd, kleiner codeformaat).
* Cookieargumenten zijn verwijderd omdat de plug-in nu dynamisch cookies genereert op basis van het argument `rp` .)

### 3.0 (5 juni 2016)

* Volledige revisie
* Gecombineerd alle vorige oplossingen die beschikbaar zijn in verschillende versies van de `getVisitNum` plug-in.
