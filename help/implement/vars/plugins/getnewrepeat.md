---
title: getNewRepeat
description: Traceeractiviteiten van nieuwe versus herhaalde bezoekers.
feature: Appmeasurement Implementation
exl-id: 8f64e176-1926-4cb1-bfae-09d7e2c015ae
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '617'
ht-degree: 0%

---

# Adobe-insteekmodule: getNewRepeat

{{plug-in}}

Met de insteekmodule `getNewRepeat` kunt u bepalen of een bezoeker van de site binnen een gewenst aantal dagen een nieuwe bezoeker of een herhaalde bezoeker is. Adobe raadt u aan deze insteekmodule te gebruiken als u bezoekers wilt identificeren als &#39;nieuw&#39; met behulp van een aangepast aantal dagen. Deze insteekmodule is niet nodig als de afmetingen van de nieuwe bezoeker/de nieuwe bezoeker in Analysis Workspace voldoen aan de behoeften van uw organisatie.

## De insteekmodule installeren met de extensie Web SDK

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken voor de webversie van SDK.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op **[!UICONTROL Tags]** aan de linkerkant en klik op de gewenste eigenschap Tag.
1. Klik op **[!UICONTROL Extensions]** aan de linkerkant en klik vervolgens op de tab **[!UICONTROL Catalog]**
1. Zoek en installeer de extensie **[!UICONTROL Common Web SDK Plugins]** .
1. Klik op **[!UICONTROL Data Elements]** aan de linkerkant en klik op het gewenste gegevenselement.
1. Stel de gewenste naam van het gegevenselement in met de volgende configuratie:
   * Extensie: algemene SDK-plug-ins voor het web
   * Gegevenselement: `getNewRepeat`
1. Stel de parameter `daysBeforeReset` rechts in.
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
   * Type handeling: Initialize getNewRepeat
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
/* Adobe Consulting Plugin: getNewRepeat v3.0 (Requires AppMeasurement) */
function getNewRepeat(d){var a=d;if("-v"===a)return{plugin:"getNewRepeat",version:"3.0"};var d=function(){if("undefined"!==typeof window.s_c_il)for(var c=0,b;c<window.s_c_il.length;c++)if(b=window.s_c_il[c],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof d&&(d.contextData.getNewRepeat="3.0");window.cookieWrite=window.cookieWrite||function(c,b,f){if("string"===typeof c){var h=window.location.hostname,a=window.location.hostname.split(".").length-1;if(h&&!/^[0-9.]+$/.test(h)){a=2<a?a:2;var e=h.lastIndexOf(".");if(0<=e){for(;0<=e&&1<a;)e=h.lastIndexOf(".",e-1),a--;e=0<e?h.substring(e):h}}g=e;b="undefined"!==typeof b?""+b:"";if(f||""===b)if(""===b&&(f=-60),"number"===typeof f){var d=new Date;d.setTime(d.getTime()+6E4*f)}else d=f;return c&&(document.cookie=encodeURIComponent(c)+"="+encodeURIComponent(b)+"; path=/;"+(f?" expires="+d.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof cookieRead)?cookieRead(c)===b:!1}};window.cookieRead=window.cookieRead||function(c){if("string"===typeof c)c=encodeURIComponent(c);else return"";var b=" "+document.cookie,a=b.indexOf(" "+c+"="),d=0>a?a:b.indexOf(";",a);return(c=0>a?"":decodeURIComponent(b.substring(a+2+c.length,0>d?b.length:d)))?c:""};a=a?a:30;d="s_nr"+a;var k=new Date,m=cookieRead(d),n=m.split("-"),l=k.getTime();k.setTime(l+864E5*a);if(""===m||18E5>l-n[0]&&"New"===n[1])return cookieWrite(d,l+"-New",k),"New";cookieWrite(d,l+"-Repeat",k);return"Repeat"};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De functie `getNewRepeat` gebruikt de volgende argumenten:

* **`d`** (geheel getal, optioneel): Het minimale aantal dagen dat is vereist tussen bezoeken waarbij bezoekers worden teruggezet naar `"New"` . Als dit argument niet is ingesteld, wordt het standaard ingesteld op 30 dagen.

Deze functie retourneert de waarde van `"New"` als de cookie die door de plug-in is ingesteld, niet bestaat of is verlopen. De waarde `"Repeat"` wordt geretourneerd als de cookie die door de plug-in is ingesteld, bestaat en de tijd sinds de huidige hit en de tijd die in de cookie is ingesteld, langer is dan 30 minuten. Deze functie retourneert dezelfde waarde voor een volledig bezoek.

Deze plug-in gebruikt een cookie met de naam `"s_nr[LENGTH]"` , waarbij `[LENGTH]` gelijk is aan het argument `d` . Het cookie bevat een Unix-tijdstempel die de huidige tijd en de huidige status van de bezoeker (`"New"` of `"Repeat"`) vertegenwoordigt.

## Voorbeelden

```js
// Sets eVar1 to "New" if it is the visitor's first visit to the site, or they have not visited in at least 30 days. Otherwise, sets eVar1 to "Repeat".
s.eVar1 = getNewRepeat();

// Sets eVar2 to "New" if it is the visitor's first visit to the site, or they have not visited in at least a year (365 days). Otherwise, sets eVar2 to "Repeat".
s.eVar2 = getNewRepeat(365);
```

## Versiehistorie

### 3.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 2.1 (30 september 2019)

* JavaScript-logica opnieuw rangschikken om de grootte van de plug-in te verkleinen

### 2.0 april 2018

* Opnieuw gecompileerd met kleinere codegrootte
* De mogelijkheid om de cookie een naam te geven, is verwijderd. De insteekmodule krijgt nu dynamisch de naam van het cookie op basis van de waarde die aan het argument `d` wordt doorgegeven.
