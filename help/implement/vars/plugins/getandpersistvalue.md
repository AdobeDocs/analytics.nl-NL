---
title: getAndPersistValue
description: Sla een waarde op die later kan worden opgehaald.
feature: Variables
exl-id: b562f9ad-3844-4535-b729-bd3f63f6f0ae
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 0%

---

# Adobe-plug-in: getAndPersistValue

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

De `getAndPersistValue` kunt u een waarde opslaan in een cookie die later tijdens een bezoek kan worden opgehaald. Het vervult een soortgelijke rol als de [!UICONTROL Storage duration] gebruiken met tags in Adobe Experience Platform. Adobe raadt u aan deze plug-in te gebruiken als u automatisch een variabele Analytics tot dezelfde waarde wilt behouden in volgende hits nadat de variabele is ingesteld. Deze insteekmodule is niet nodig als de [!UICONTROL Storage duration] is voldoende. Het is ook niet nodig om deze plug-in te gebruiken als u variabelen niet op dezelfde waarde hoeft in volgende treffers in te stellen en te behouden. Voor de ingebouwde persistentie van eVars is het gebruik van deze plug-in niet vereist, aangezien eVars server-side voor Adobe blijft bestaan.

## Plug-in installeren met tags in Adobe Experience Platform

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop [!UICONTROL Catalog] knop
1. Installeer en publiceer de [!UICONTROL Common Analytics Plugins] extension
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: Geen
   * Gebeurtenis: Kern - Bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: Gebruikelijke plug-ins voor Analytics
   * Type handeling: getAndPersistValue initialiseren
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met aangepaste code-editor

Als u de extensie van de plug-in niet wilt gebruiken, kunt u de aangepaste code-editor gebruiken.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop [!UICONTROL Configure] onder de extensie Adobe Analytics.
1. Breid uit [!UICONTROL Configure tracking using custom code] accordion, die de [!UICONTROL Open Editor] knop.
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

De `getAndPersist` function gebruikt de volgende argumenten:

* **`vtp`** (vereist): De waarde die van pagina tot pagina moet worden behouden
* **`cn`** (optioneel): De naam van het cookie waarin de waarde wordt opgeslagen. Als dit argument niet is ingesteld, krijgt het cookie de naam `"s_gapv"`
* **`ex`** (optioneel): Het aantal dagen voordat de cookie vervalt. Als dit argument `0` of niet is ingesteld, verloopt het cookie aan het einde van het bezoek (30 minuten inactiviteit).

Als de variabele in de `vtp` wordt ingesteld, wordt de cookie vervolgens door de insteekmodule geretourneerd. Als de variabele in de `vtp` -argument niet is ingesteld, retourneert de insteekmodule alleen de waarde van het cookie.

## Voorbeelden

```js
// Sets eVar21 to "raccoon", and sets the ev21gapv cookie to "raccoon" (which expires in 28 days).
s.eVar21 = "raccoon";
s.eVar21 = getAndPersistValue(s.eVar21,"ev21gapv",28);

// Checks the "ev21gapv" cookie for a value and assigns it to eVar21. It does not set a cookie value or reset an existing cookie's expiration since the value is not set on the page.
// If there is a cookie, assigns eVar21 to that value. Otherwise, eVar21 is blank.
s.eVar21 = getAndPersistValue(s.eVar21,"ev21gapv",28);

// Checks the "ev21gapv" cookie for a value and assigns it to prop35. It does not set a cookie value or reset an existing cookie's expiration since eVar21 is not set on the page.
s.prop35 = getAndPersistValue(s.eVar21,"ev21gapv",28);

// Sets eVar21 to "panda", and sets the ev21gapv cookie to "panda" (which expires in 14 days). It then sets prop35 to the value contained in the ev21gapv cookie.
// Ultimately both eVar21 and prop35 contain the value "panda".
s.eVar21 = "panda";
s.prop35 = getAndPersistValue(s.eVar21,"ev21gapv",14);

// Sets eVar30 to "shopping", and sets the s_gapv cookie to "shopping" (which expires at the end of the browser session).
s.eVar30 = "shopping";
s.eVar30 = getAndPersistValue(s.eVar30);
```

## Versiehistorie

### 3.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 2.0 (16 april 2018)

* Puntrelease (kleinere codegrootte)
* 0 passeren naar de `ex` dit argument dwingt nu om een vervaldatum na 30 minuten inactiviteit in plaats van aan het einde van de browsersessie.

### 1.0 (18 januari 2016)

* Eerste release.
