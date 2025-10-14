---
title: rfl
description: Verwijder een specifieke waarde uit een tekenreeks met een teken als scheidingsteken.
feature: Appmeasurement Implementation
exl-id: d66b757e-b39f-4b6e-9999-6fbde87505af
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 0%

---

# Adobe-insteekmodule: rfl (Verwijderen uit lijst)

{{plug-in}}

Met de insteekmodule `rfl` kunt u &quot;veilig&quot; waarden verwijderen uit afgebakende tekenreeksen, zoals [`events`](../page-vars/events/events-overview.md) , [`products`](../page-vars/products.md) , [`list`](../page-vars/list.md) en andere. Deze plug-in is handig als u specifieke waarden uit een tekenreeks met scheidingstekens wilt verwijderen zonder dat u zich zorgen hoeft te maken over scheidingstekens. Verscheidene andere stop-ins hangen van deze code af correct in werking te stellen. Deze insteekmodule is niet nodig als u een specifieke functie niet hoeft uit te voeren voor meer dan één variabele Analytics tegelijk, of als u geen afhankelijke insteekmodules gebruikt.

De plug-in gebruikt de volgende logica:

* Als de waarde die u wilt verwijderen bestaat, blijft alles in de variabele behouden, behalve de waarde die u wilt verwijderen.
* Als de waarde die u wilt verwijderen niet bestaat, behoudt de plug-in de oorspronkelijke tekenreeks ongewijzigd.

## De insteekmodule installeren met de extensie Web SDK of Web SDK

Deze insteekmodule wordt nog niet ondersteund voor gebruik in de Web SDK.

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
   * Type handeling: RFP initialiseren (verwijderen uit lijst)
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
/* Adobe Consulting Plugin: rfl (removeFromList) v2.1  */
function rfl(lv,vr,d1,d2,df){var b=lv,f=vr,e=d1,h=d2,g=df;if("-v"===b)return{plugin:"rfl",version:"2.1"};a:{if("undefined"!==typeof window.s_c_il){var c=0;for(var a;c<window.s_c_il.length;c++)if(a=window.s_c_il[c],a._c&&"s_c"===a._c){c=a;break a}}c=void 0}"undefined"!==typeof c&&(c.contextData.rfl="2.1");if(!b||!f)return"";c=[];a="";e=e||",";h=h||e;g=g||!1;b=b.split(e);e=b.length;for(var d=0;d<e;d++)-1<b[d].indexOf(":")&&(a=b[d].split(":"),a[1]=a[0]+":"+a[1],b[d]=a[0]),-1<b[d].indexOf("=")&&(a=b[d].split("="),a[1]=a[0]+"="+a[1],b[d]=a[0]),b[d]!==f&&a?c.push(a[1]):b[d]!==f?c.push(b[d]):b[d]===f&&g&&(a?c.push(a[1]):c.push(b[d]),g=!1),a="";return c.join(h)};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De functie `rfl` gebruikt de volgende argumenten:

* **`lv`** (vereist, tekenreeks): een variabele (of tekenreeks) die een lijst met gescheiden waarden bevat
* **`vr`** (vereist, tekenreeks): de waarde die u uit het argument `lv` wilt verwijderen. Adobe raadt u af meerdere waarden te verwijderen tijdens een enkele `rfl` -aanroep.
* **`d1`** (optional, string): Het scheidingsteken dat het argument `lv` gebruikt. Heeft als standaardwaarde een komma (`,`).
* **`d2`** (optioneel, tekenreeks): het scheidingsteken dat u wilt gebruiken voor de geretourneerde tekenreeks. Heeft standaard dezelfde waarde als het argument `d1` .
* **`df`** (optioneel, Boolean): Indien `true` , worden alleen dubbele instanties van het argument `vr` geforceerd vanuit het argument `lv` in plaats van alle instanties. Wordt standaard ingesteld op `false` wanneer niet ingesteld.

Wanneer deze functie wordt aangeroepen, wordt een gewijzigde tekenreeks geretourneerd die het argument `lv` bevat, maar zonder instanties (of dubbele instanties) van de waarde die is opgegeven in het argument `vr` .

## Voorbeelden van aanroepen

### Voorbeeld 1

Indien...

```js
s.events = "event22,event24,event25";
```

...en de volgende code loopt..

```js
s.events = rfl(s.events,"event24");
```

...de uiteindelijke waarde van s.events is:

```js
s.events = "event22,event25";
```

### Voorbeeld 2

Indien...

```js
s.events = "event22,event24,event25";
```

...en de volgende code loopt..

```js
s.events = rfl(s.events,"event26");
```

...de uiteindelijke waarde van s.events is:

```js
s.events = "event22,event24,event25";
```

In dit voorbeeld heeft de rfl-aanroep geen wijzigingen aangebracht in s.events omdat s.events geen &quot;event26&quot; bevatte

### Voorbeeld 3

Indien...

```js
s.events = "event22,event24,event25";
```

...en de volgende code loopt..

```js
s.events = rfl(s.events);
```

...de uiteindelijke waarde van s.events is:

```js
s.events = "";
```

Als het argument `lv` of het argument `vr` leeg zijn in een `rfl` -aanroep, retourneert de plug-in niets.

### Voorbeeld 4

Indien...

```js
s.prop4 = "hello|people|today";
```

...en de volgende code loopt..

```js
s.eVar5 = rfl(s.prop4,"people","|");
```

...de definitieve waarde van s.prop4 zal nog zijn...

```js
s.prop4 = "hello|people|today";
```

...maar de uiteindelijke waarde van s.eVar5 is:

```js
s.eVar5 = "hello|today";
```

Houd er rekening mee dat de insteekmodule alleen een waarde retourneert; de variabele die door het argument `lv` wordt doorgegeven, wordt niet opnieuw ingesteld.

### Voorbeeld 5

Indien...

```js
s.prop4 = "hello|people|today";
```

...en de volgende code loopt..

```js
s.prop4 = rfl(s.prop4,"people");
```

...de definitieve waarde van s.prop4 zal nog zijn...

```js
s.prop4 = "hello|people|today";
```

Stel het argument `d1` in als de argumentwaarde van `lv` een ander scheidingsteken bevat dan de standaardwaarde (dus een komma).

### Voorbeeld 6

Indien...

```js
s.events = "event22,event23,event25";
```

...en de volgende code loopt..

```js
s.events = rfl(s.events,"EVenT23");
```

...de uiteindelijke waarde van s.events is:

```js
s.events = "event22,event23,event25";
```

Hoewel dit voorbeeld niet praktisch is, toont het de behoefte aan om in case-sensitive waarden over te gaan.

### Voorbeeld 7

Indien...

```js
s.events = "event22,event23:12345,event25";
```

...en de volgende code loopt..

```js
s.events = rfl(s.events,"event23");
```

...de uiteindelijke waarde van s.events is:

```js
s.events = "event22,event25";
```

### Voorbeeld 8

Indien...

```js
s.events = "event22,event23:12345,event25";
```

...en de volgende code loopt..

```js
s.events = rfl(s.events,"event23:12345");
```

...de uiteindelijke waarde van s.events is:

```js
s.events = "event22,event23:12345,event25";
```

Wanneer u een gebeurtenis moet verwijderen die serienummering en/of numerieke/valutasyntaxis gebruikt, zou u slechts de gebeurtenis zelf (d.w.z. zonder de serienummering/numerieke/valutawaarden) in de `rfl` vraag moeten specificeren.

### Voorbeeld 9

Indien...

```js
s.events = "event22,event23,event23,event23,event24,event25";
```

...en de volgende code loopt..

```js
s.events = rfl(s.events,"event23");
```

...de uiteindelijke waarde van s.events is:

```js
s.events = "event22,event24,event25");
```

### Voorbeeld 10

Indien...

```js
s.events = "event22,event23,event23,event23,event24,event25";
```

...en de volgende code loopt..

```js
s.events = rfl(s.events,"event23", "", "",true);
```

...de uiteindelijke waarde van s.events is:

```js
s.events = "event22,event23,event24,event25");
```

### Voorbeeld #11

Indien...

```js
s.events = "event22,event23,event23,event23,event24,event25";
```

...en de volgende code loopt..

```js
s.events = rfl(s.events,"event23", "", "|",true);
```

...de uiteindelijke waarde van s.events is:

```js
s.events = "event22|event23|event24|event25");
```

### Voorbeeld 12

Indien...

```js
s.events = "event22,event23,event24,event25";
```

...en de volgende code loopt..

```js
s.events = rfl(s.events,"event23,event24");
```

...de uiteindelijke waarde van s.events is:

```js
s.events = "event22,event23,event24,event25";
```

Het instellen van meerdere waarden in het argument `vr` wordt niet ondersteund. De `rfl` -logica in het bovenstaande voorbeeld splitst eerst de waarden in het `lv` -argument (d.w.z. s.events) en probeert vervolgens elke gescheiden waarde te koppelen aan de volledige argumentwaarde `vr` (d.w.z. `"event23,event24"`).

### Voorbeeld 13

Indien...

```js
s.events = "event22,event23,event24,event25";
```

...en de volgende code loopt..

```js
s.events = rfl(s.events,"event23");
s.events = rfl(s.events,"event24");
```

...de uiteindelijke waarde van s.events is:

```js
s.events = "event22,event25");
```

Elke waarde die uit de lijst moet worden verwijderd, moet zich binnen de eigen `rfl` -aanroep bevinden.

### Voorbeeld 14

Indien...

```js
s.linkTrackVars = "events,eVar1,eVar2,eVar3";
```

...en de volgende code loopt..

```js
s.linkTrackVars = rfl(s.linkTrackVars,"eVar2", ",", ",", false);
```

...de definitieve waarde van s.linkTrackVars zal zijn:

```js
s.linkTrackVars = "events,eVar1,eVar3";
```

De laatste drie argumenten (d.w.z. &quot;,&quot;,&quot;,&quot;, false) aan het einde van deze `rfl` -aanroep zijn niet nodig, maar doen er ook niets mee omdat ze overeenkomen met de standaardinstellingen.

### Voorbeeld 15

Indien...

```js
s.events = "event22,event23,event24";
```

...en de volgende code loopt..

```js
rfl(s.events,"event23");
```

...de definitieve waarde van s.events zal nog zijn:

```js
s.events = "event22,event23,event24";
```

Vergeet niet dat de insteekmodule alleen een waarde retourneert; de variabele die door het argument `lv` wordt doorgegeven, wordt niet opnieuw ingesteld.

## Versiehistorie

### 2.1 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 2.01 (17 september 2019)

* Kleine bug-correctie voor de standaardwaarde van het scheidingsteken

### 2.0 april 2018

* Puntrelease (opnieuw gecompileerd, kleiner codeformaat).
* De plug-in `join` is verwijderd.

### 1.0 (18 juli 2016)

* Eerste release.
