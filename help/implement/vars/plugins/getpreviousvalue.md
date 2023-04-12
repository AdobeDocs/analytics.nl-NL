---
title: getPreviousValue
description: Hiermee wordt de laatste waarde opgehaald die in een variabele is doorgegeven.
feature: Variables
exl-id: 235c504b-ba97-4399-a07b-b0bfc764f1ba
source-git-commit: bbb138d979968ec2536e53ff07001b43156df095
workflow-type: tm+mt
source-wordcount: '731'
ht-degree: 0%

---

# Adobe-plug-in: getPreviousValue

{{plug-in}}

De `getPreviousValue` kunt u een variabele instellen op een waarde die bij een vorige hit is ingesteld. Deze insteekmodule is niet nodig als de implementatie alle gewenste waarden in de huidige hit bevat.

## De plug-in installeren met de extensie Web SDK

Adobe biedt een uitbreiding aan die u toestaat om het meest algemeen gebruikte stop-ins met het Web SDK te gebruiken.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klikken **[!UICONTROL Tags]** klikt u links op de gewenste eigenschap tag.
1. Klikken **[!UICONTROL Extensions]** klikt u links op de knop **[!UICONTROL Catalog]** tab
1. Zoek en installeer de **[!UICONTROL Common Web SDK Plugins]** extensie.
1. Klikken **[!UICONTROL Data Elements]** klikt u links op het gewenste gegevenselement.
1. Stel de gewenste naam van het gegevenselement in met de volgende configuratie:
   * Extensie: Algemene insteekmodules voor Web SDK
   * Gegevenselement: `getPreviousValue`
1. Stel de gewenste parameters rechts in.
1. Sla de wijzigingen in het gegevenselement op en publiceer deze.

## De plug-in handmatig installeren met de implementatie van de Web SDK

Deze insteekmodule wordt nog niet ondersteund voor gebruik in een handmatige implementatie van de Web SDK.

## De insteekmodule installeren met de Adobe Analytics-extensie

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken in Adobe Analytics.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop [!UICONTROL Catalog] knop
1. Installeer en publiceer de [!UICONTROL Common Analytics Plugins] extension
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: Geen
   * Gebeurtenis: Kern - Bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: Gebruikelijke plug-ins voor Analytics
   * Type handeling: getPreviousValue initialiseren
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met aangepaste code-editor

Als u niet de Gemeenschappelijke Insteekmodule van Analytics wilt gebruiken, kunt u de redacteur van de douanecode gebruiken.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder de extensie Adobe Analytics.
1. Breid uit [!UICONTROL Configure tracking using custom code] accordion, die de [!UICONTROL Open Editor] knop.
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

De `getPreviousValue` function gebruikt de volgende argumenten:

* **`v`** (tekenreeks, vereist): De variabele met de waarde die u wilt doorgeven aan de volgende afbeeldingsaanvraag. Een veelgebruikte variabele is `s.pageName` om de vorige paginawaarde op te halen.
* **`c`** (tekenreeks, optioneel): De naam van het cookie waarin de waarde wordt opgeslagen.  Als dit argument niet is ingesteld, wordt standaard ingesteld op `"s_gpv"`.

Wanneer u deze functie aanroept, wordt de tekenreekswaarde in het cookie geretourneerd. De insteekmodule stelt vervolgens de vervaldatum van het cookie opnieuw in en wijst er de variabelewaarde aan toe vanuit de `v` argument. Het cookie verloopt na 30 minuten inactiviteit.

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

Als de variabele gekoppeld is aan de `v` wordt ingesteld op een nieuwe waarde en `getPreviousValue` de insteekmodule wordt uitgevoerd, MAAR er wordt NIET tegelijkertijd een analytische serveraanroep verzonden, de nieuwe `v` de argumentwaarde wordt nog steeds beschouwd als de &quot;vorige waarde&quot; de volgende keer dat de insteekmodule wordt uitgevoerd.
Stel bijvoorbeeld dat de volgende code op de eerste pagina van het bezoek wordt uitgevoerd:

```js
s.pageName = "Home";
s.prop7 = getPreviousValue(s.pageName,"gpv_Page");
s.t();
```

Deze code produceert een servervraag waar `pageName` is &quot;Home&quot; en prop7 is niet ingesteld.  De oproep tot `getPreviousValue` slaat de waarde van op `pageName` in de `gpv_Page` cookie. Stel dat onmiddellijk daarna op dezelfde pagina de volgende code wordt uitgevoerd:

```js
s.pageName = "New value";
s.prop7 = getPreviousValue(s.pageName,"gpv_Page");
```

Aangezien `t()` Deze functie wordt niet uitgevoerd in dit codeblok. Er wordt geen andere afbeeldingsaanvraag verzonden.  Wanneer echter `getPreviousValue` deze keer wordt de functiecode uitgevoerd, `prop7` wordt ingesteld op de vorige waarde van `pageName` (&quot;Huis&quot;), dan slaat de nieuwe waarde van op `pageName` (&quot;Nieuwe waarde&quot;) in het dialoogvenster `gpv_Page` cookie. Ga er vervolgens van uit dat de bezoeker naar een andere pagina navigeert en dat de volgende code op deze pagina wordt uitgevoerd:

```js
s.pageName = "Page 2";
s.prop7 = getPreviousValue(s.pageName,"gpv_Page");
s.t();
```

Wanneer de `t()` functie wordt uitgevoerd, wordt een afbeeldingsaanvraag gemaakt waar `pageName` is &quot;Pagina 2&quot; en `prop7` is &quot;Nieuwe waarde&quot;, wat de waarde was van `pageName` wanneer de laatste aanroep naar `getPreviousValue` heeft plaatsgevonden. De `prop7` waarde van `"Home"` is nooit opgenomen in een afbeeldingsaanvraag, ook al is &quot;Home&quot; de eerste waarde die is doorgegeven aan `pageName`.

## Versiehistorie

### 3.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### v2.0 (7 oktober 2019)

* Puntrelease (volledige logica herschrijven).
