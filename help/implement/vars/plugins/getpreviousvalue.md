---
title: getPreviousValue
description: Hiermee wordt de laatste waarde opgehaald die in een variabele is doorgegeven.
feature: Appmeasurement Implementation
exl-id: 235c504b-ba97-4399-a07b-b0bfc764f1ba
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 0%

---

# Adobe-insteekmodule: getPreviousValue

{{plug-in}}

Met de plug-in `getPreviousValue` kunt u een variabele instellen op een waarde die bij een vorige hit is ingesteld. Deze insteekmodule is niet nodig als de implementatie alle gewenste waarden in de huidige hit bevat.

## De insteekmodule installeren met de extensie Web SDK

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken voor de webversie van SDK.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op **[!UICONTROL Tags]** aan de linkerkant en klik op de gewenste eigenschap Tag.
1. Klik op **[!UICONTROL Extensions]** aan de linkerkant en klik vervolgens op de tab **[!UICONTROL Catalog]**
1. Zoek en installeer de extensie **[!UICONTROL Common Web SDK Plugins]** .
1. Klik op **[!UICONTROL Data Elements]** aan de linkerkant en klik op het gewenste gegevenselement.
1. Stel de gewenste naam van het gegevenselement in met de volgende configuratie:
   * Extensie: algemene SDK-plug-ins voor het web
   * Gegevenselement: `getPreviousValue`
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
   * Type handeling: Initialize getPreviousValue
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
/* Adobe Consulting Plugin: getPreviousValue v3.0 */
function getPreviousValue(v,c){var k=v,d=c;if("-v"===k)return{plugin:"getPreviousValue",version:"3.0"};var a=function(){if("undefined"!==typeof window.s_c_il)for(var c=0,b;c<window.s_c_il.length;c++)if(b=window.s_c_il[c],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof a&&(a.contextData.getPreviousValue="3.0");window.cookieWrite=window.cookieWrite||function(c,b,f){if("string"===typeof c){var h=window.location.hostname,a=window.location.hostname.split(".").length-1;if(h&&!/^[0-9.]+$/.test(h)){a=2<a?a:2;var e=h.lastIndexOf(".");if(0<=e){for(;0<=e&&1<a;)e=h.lastIndexOf(".",e-1),a--;e=0<e?h.substring(e):h}}g=e;b="undefined"!==typeof b?""+b:"";if(f||""===b)if(""===b&&(f=-60),"number"===typeof f){var d=new Date;d.setTime(d.getTime()+6E4*f)}else d=f;return c&&(document.cookie=encodeURIComponent(c)+"="+encodeURIComponent(b)+"; path=/;"+(f?" expires="+d.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof cookieRead)?cookieRead(c)===b:!1}};window.cookieRead=window.cookieRead||function(c){if("string"===typeof c)c=encodeURIComponent(c);else return"";var b=" "+document.cookie,a=b.indexOf(" "+c+"="),d=0>a?a:b.indexOf(";",a);return(c=0>a?"":decodeURIComponent(b.substring(a+2+c.length,0>d?b.length:d)))?c:""};var l;d=d||"s_gpv";a=new Date;a.setTime(a.getTime()+18E5);window.cookieRead(d)&&(l=window.cookieRead(d));k?window.cookieWrite(d,k,a):window.cookieWrite(d,l,a);return l};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De functie `getPreviousValue` gebruikt de volgende argumenten:

* **`v`** (tekenreeks, vereist): De variabele met de waarde die u wilt doorgeven aan de volgende afbeeldingsaanvraag. Een veelgebruikte variabele is `s.pageName` om de vorige paginawaarde op te halen.
* **`c`** (tekenreeks, optioneel): de naam van het cookie waarin de waarde wordt opgeslagen.  Als dit argument niet is ingesteld, wordt standaard ingesteld op `"s_gpv"` .

Wanneer u deze functie aanroept, wordt de tekenreekswaarde in het cookie geretourneerd. De insteekmodule stelt vervolgens de vervaldatum van het cookie opnieuw in en wijst hieraan de variabelewaarde toe vanuit het argument `v` . Het cookie verloopt na 30 minuten inactiviteit.

## Voorbeelden

```js
// 1. Sets prop7 to the cookie value contained in gpv_Page
// 2. Resets the gpv_Page cookie value to the page variable
// 3. If the page variable is not set, reset the gpv_Page cookie expiration
s.prop7 = getPreviousValue(s.pageName,"gpv_Page");

// Sets prop7 to the cookie value contained in gpv_Page, but only if event1 is in the events variable.
if(inList(s.events,"event1")) s.prop7 = getPreviousValue(s.pageName,"gpv_Page");

// Sets prop7 to the cookie value contained in gpv_Page, but only if the page variable is currently set on the page
if(s.pageName) s.prop7 = getPreviousValue(s.pageName,"gpv_Page");

// Sets eVar10 equal to the cookie value contained in s_gpv, then sets the s_gpv cookie to the current value of eVar1.
s.eVar10 = getPreviousValue(s.eVar1);
```

## Onwaarschijnlijke Kwartels

Als de variabele die aan het argument `v` is gekoppeld, op een nieuwe waarde is ingesteld en de `getPreviousValue` -insteekmodule MAAR tegelijkertijd een analytische serveraanroep wordt NIET verzonden, wordt de nieuwe argumentwaarde `v` de volgende keer dat de insteekmodule wordt uitgevoerd, nog steeds als de &quot;vorige waarde&quot; beschouwd.
Stel bijvoorbeeld dat de volgende code op de eerste pagina van het bezoek wordt uitgevoerd:

```js
s.pageName = "Home";
s.prop7 = getPreviousValue(s.pageName,"gpv_Page");
s.t();
```

Deze code genereert een serveraanroep waarbij `pageName` &quot;Home&quot; is en prop7 niet is ingesteld.  Bij het aanroepen van `getPreviousValue` wordt de waarde van `pageName` echter opgeslagen in het `gpv_Page` -cookie. Stel dat onmiddellijk daarna op dezelfde pagina de volgende code wordt uitgevoerd:

```js
s.pageName = "New value";
s.prop7 = getPreviousValue(s.pageName,"gpv_Page");
```

Aangezien de functie `t()` niet in dit codeblok wordt uitgevoerd, wordt geen andere afbeeldingsaanvraag verzonden.  Wanneer de functiecode `getPreviousValue` deze keer wordt uitgevoerd, wordt `prop7` echter ingesteld op de vorige waarde van `pageName` (&quot;Home&quot;) en wordt de nieuwe waarde van `pageName` (&quot;New value&quot;) in het `gpv_Page` -cookie opgeslagen. Ga er vervolgens van uit dat de bezoeker naar een andere pagina navigeert en dat de volgende code op deze pagina wordt uitgevoerd:

```js
s.pageName = "Page 2";
s.prop7 = getPreviousValue(s.pageName,"gpv_Page");
s.t();
```

Wanneer de functie `t()` wordt uitgevoerd, wordt een afbeeldingsaanvraag gemaakt waarbij `pageName` &quot;Page 2&quot; en `prop7` &quot;New value&quot; is. Dit was de waarde van `pageName` toen de laatste aanroep van `getPreviousValue` plaatsvond. De `prop7` waarde van `"Home"` was nooit opgenomen in een afbeeldingsaanvraag, ook al was &quot;Home&quot; de eerste waarde die aan `pageName` werd doorgegeven.

## Versiehistorie

### 3.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### v2.0 (7 oktober 2019)

* Puntrelease (volledige logica herschrijven).
