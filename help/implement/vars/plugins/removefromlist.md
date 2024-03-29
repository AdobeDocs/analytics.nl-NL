---
title: rfl
description: Verwijder een specifieke waarde uit een tekenreeks met een teken als scheidingsteken.
feature: Variables
exl-id: d66b757e-b39f-4b6e-9999-6fbde87505af
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 0%

---

# Adobe-insteekmodule: rfl (Verwijderen uit lijst)

{{plug-in}}

De `rfl` Met de insteekmodule kunt u &quot;veilig&quot; waarden verwijderen uit afgebakende tekenreeksen, zoals [`events`](../page-vars/events/events-overview.md), [`products`](../page-vars/products.md), [`list`](../page-vars/list.md)en andere. Deze plug-in is handig als u specifieke waarden uit een tekenreeks met scheidingstekens wilt verwijderen zonder dat u zich zorgen hoeft te maken over scheidingstekens. Verscheidene andere stop-ins hangen van deze code af correct in werking te stellen. Deze insteekmodule is niet nodig als u een specifieke functie niet hoeft uit te voeren voor meer dan één variabele Analytics tegelijk, of als u geen afhankelijke insteekmodules gebruikt.

De plug-in gebruikt de volgende logica:

* Als de waarde die u wilt verwijderen bestaat, blijft alles in de variabele behouden, behalve de waarde die u wilt verwijderen.
* Als de waarde die u wilt verwijderen niet bestaat, behoudt de plug-in de oorspronkelijke tekenreeks ongewijzigd.

## De insteekmodule installeren met de extensie Web SDK of Web SDK

Deze plug-in wordt nog niet ondersteund voor gebruik in de Web SDK.

## De insteekmodule installeren met de Adobe Analytics-extensie

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken met Adobe Analytics.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop [!UICONTROL Catalog] knop
1. Installeer de [!UICONTROL Common Analytics Plugins] extension
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: geen
   * Event: Core - bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: veelgebruikte plug-ins voor Analytics
   * Type handeling: RFP initialiseren (verwijderen uit lijst)
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met aangepaste code-editor

Als u niet de Gemeenschappelijke Insteekmodule van Analytics wilt gebruiken, kunt u de redacteur van de douanecode gebruiken.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder de extensie Adobe Analytics.
1. Breid uit [!UICONTROL Configure tracking using custom code] accordion, die de [!UICONTROL Open Editor] knop.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

## Plug-in installeren met AppMeasurement

Kopieer en plak de volgende code ergens in het bestand AppMeasurement nadat het object Analytics tracking is geïnstantieerd (met [`s_gi`](../functions/s-gi.md)). Door opmerkingen en versienummers van de code in uw implementatie te behouden, kunt u Adoben met het oplossen van mogelijke problemen.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: rfl (removeFromList) v2.1  */
function rfl(lv,vr,d1,d2,df){var b=lv,f=vr,e=d1,h=d2,g=df;if("-v"===b)return{plugin:"rfl",version:"2.1"};a:{if("undefined"!==typeof window.s_c_il){var c=0;for(var a;c<window.s_c_il.length;c++)if(a=window.s_c_il[c],a._c&&"s_c"===a._c){c=a;break a}}c=void 0}"undefined"!==typeof c&&(c.contextData.rfl="2.1");if(!b||!f)return"";c=[];a="";e=e||",";h=h||e;g=g||!1;b=b.split(e);e=b.length;for(var d=0;d<e;d++)-1<b[d].indexOf(":")&&(a=b[d].split(":"),a[1]=a[0]+":"+a[1],b[d]=a[0]),-1<b[d].indexOf("=")&&(a=b[d].split("="),a[1]=a[0]+"="+a[1],b[d]=a[0]),b[d]!==f&&a?c.push(a[1]):b[d]!==f?c.push(b[d]):b[d]===f&&g&&(a?c.push(a[1]):c.push(b[d]),g=!1),a="";return c.join(h)};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `rfl` function gebruikt de volgende argumenten:

* **`lv`** (vereist, tekenreeks): een variabele (of tekenreeks) die een lijst met gescheiden waarden bevat
* **`vr`** (vereist, tekenreeks): de waarde die u uit het dialoogvenster wilt verwijderen `lv` argument. Adobe raadt u af meerdere waarden tijdens één bewerking te verwijderen `rfl` vraag.
* **`d1`** (optioneel, tekenreeks): het scheidingsteken dat de `lv` argument gebruikt. Heeft als standaardwaarde een komma (`,`).
* **`d2`** (optioneel, tekenreeks): het scheidingsteken dat u wilt gebruiken voor de geretourneerde tekenreeks. Heeft als standaardwaarde dezelfde waarde als de `d1` argument.
* **`df`** (optioneel, Boolean): Indien `true`, dwingt alleen dubbele instanties van de `vr` argument van de `lv` in plaats van alle instanties. Standaardwaarden: `false` wanneer niet ingesteld.

Als deze functie wordt aangeroepen, wordt een gewijzigde tekenreeks geretourneerd die de `lv` , maar zonder instanties (of dubbele instanties) van de waarde die is opgegeven in het dialoogvenster `vr` argument.

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

Als een van de `lv` argument of `vr` argument is leeg in een `rfl` en retourneert de plug-in niets.

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

Houd er rekening mee dat de insteekmodule alleen een waarde retourneert; de variabele die door de `lv` argument.

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

Zorg ervoor dat u de `d1` in gevallen waarin `lv` argumentwaarde bevat een ander scheidingsteken dan de standaardwaarde (d.w.z. komma).

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

Wanneer u een gebeurtenis moet verwijderen die serienummering en/of numerieke/valutasyntaxis gebruikt, moet u alleen de gebeurtenis zelf opgeven (dat wil zeggen zonder de serienummering/numerieke/valutawaarden) in het dialoogvenster `rfl` vraag.

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

Meerdere waarden instellen in het dialoogvenster `vr` argument wordt niet ondersteund. De `rfl` logica in het bovenstaande voorbeeld zou eerst de waarden in de `lv` argument (d.w.z. s.events) probeert dan om elke afgebakende waarde aan volledige overeen te stemmen `vr` argumentwaarde (d.w.z. `"event23,event24"`).

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

Elke waarde die uit de lijst moet worden verwijderd, moet binnen de eigen waarde vallen `rfl` vraag.

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

De laatste drie argumenten (d.w.z. &quot;,&quot;,&quot;,&quot;, false) aan het einde van dit `rfl` de vraag is niet noodzakelijk maar ook &quot; doet niets pijn &quot; door daar te zijn aangezien zij de standaardmontages aanpassen.

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

Onthoud nogmaals dat de insteekmodule alleen een waarde retourneert; de variabele die door de `lv` argument.

## Versiehistorie

### 2.1 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 2.01 (17 september 2019)

* Kleine bug-correctie voor de standaardwaarde van het scheidingsteken

### 2.0 april 2018

* Puntrelease (opnieuw gecompileerd, kleiner codeformaat).
* De noodzaak van de `join` insteekmodule.

### 1.0 (18 juli 2016)

* Eerste release.
