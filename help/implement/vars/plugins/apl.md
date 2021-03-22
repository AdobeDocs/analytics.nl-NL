---
title: apl (appendToList)
description: Voeg waarden toe aan variabelen die meerdere waarden ondersteunen.
translation-type: tm+mt
source-git-commit: d84d53dd237f5bba729c902c8c4980c0288dbbb0
workflow-type: tm+mt
source-wordcount: '1022'
ht-degree: 0%

---


# Adobe-plug-in: apl (appendToList)

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `apl`-plug-in kunt u veilig nieuwe waarden toevoegen aan door lijsten gescheiden variabelen, zoals [`events`](../page-vars/events/events-overview.md), [`linkTrackVars`](../config-vars/linktrackvars.md), [`list`](../page-vars/list.md) en andere.

* Als de waarde die u wilt toevoegen niet in de variabele bestaat, voegt de code de waarde aan het einde van de tekenreeks toe.
* Als de waarde die u wilt toevoegen al in de variabele bestaat, wijzigt deze plug-in de waarde niet. Hierdoor kan uw implementatie dubbele waarden voorkomen.
* Als de variabele die u wilt toevoegen leeg is, stelt de plug-in de variabele in op de nieuwe waarde.

Adobe raadt u aan deze plug-in te gebruiken als u nieuwe waarden wilt toevoegen aan bestaande variabelen die een reeks gescheiden waarden bevatten. Deze plug-in is niet nodig als u tekenreeksen wilt samenvoegen voor variabelen met gescheiden waarden.

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
   * Type handeling: APL initialiseren (toevoegen aan lijst)
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
/* Adobe Consulting Plugin: apl (appendToList) v4.0 */
function apl(lv,va,d1,d2,cc){var b=lv,d=va,e=d1,c=d2,g=cc;if("-v"===b)return{plugin:"apl",version:"4.0"};var h=function(){if("undefined"!==typeof window.s_c_il)for(var k=0,b;k<window.s_c_il.length;k++)if(b=window.s_c_il[k],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof h&&(h.contextData.apl="4.0");window.inList=window.inList||function(b,d,c,e){if("string"!==typeof d)return!1;if("string"===typeof b)b=b.split(c||",");else if("object"!==typeof b)return!1;c=0;for(a=b.length;c<a;c++)if(1==e&&d===b[c]||d.toLowerCase()===b[c].toLowerCase())return!0;return!1};if(!b||"string"===typeof b){if("string"!==typeof d||""===d)return b;e=e||",";c=c||e;1==c&&(c=e,g||(g=1));2==c&&1!=g&&(c=e);d=d.split(",");h=d.length;for(var f=0;f<h;f++)window.inList(b,d[f],e,g)||(b=b?b+c+d[f]:d[f])}return b};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De methode `apl` gebruikt de volgende argumenten:

* **`lv`** (vereist, tekenreeks): De variabele die een lijst met gescheiden items bevat waaraan een nieuwe waarde moet worden toegevoegd
* **`vta`** (vereist, tekenreeks): Een door komma&#39;s gescheiden lijst met de nieuwe waarden die aan de waarde van het  `lv` argument moeten worden toegevoegd.
* **`d1`** (optioneel, tekenreeks): Het scheidingsteken dat wordt gebruikt om de afzonderlijke waarden te scheiden die al in het  `lv` argument staan.  Heeft als standaardwaarde een komma (`,`).
* **`d2`** (optioneel, tekenreeks): Het uitvoerscheidingsteken. Wordt standaard ingesteld op dezelfde waarde als `d1` wanneer deze niet is ingesteld.
* **`cc`** (optioneel, Booleaans): Een markering die aangeeft of een hoofdlettergevoelige controle wordt gebruikt. Bij `true` is de duplicatiecontrole hoofdlettergevoelig. Als `false` of niet ingesteld, is de duplicatiecontrole niet hoofdlettergevoelig. Wordt standaard ingesteld op `false`.

De methode `apl` retourneert de waarde van het argument `lv` plus eventuele niet-gedupliceerde waarden in het argument `vta`.

## Voorbeelden van aanroepen

### Voorbeeld 1

Indien...

```js
s.events = "event22,event24";
```

...en de volgende code wordt uitgevoerd...

```js
s.events = s.apl(s.events, "event23");
```

... de uiteindelijke waarde van s.events zal zijn :

```js
s.events = "event22,event24,event23";
```

### Voorbeeld 3

Indien...

```js
s.events = "event22,event23";
```

...en de volgende code wordt uitgevoerd...

```js
s.events = s.apl(s.events, "event23");
```

... de definitieve waarde van s.events zal nog zijn:

```js
s.events = "event22,event23";
```

In dit voorbeeld heeft de apl-aanroep geen wijzigingen aangebracht in s.events aangezien s.events al &quot;event23&quot; bevatte

### Voorbeeld 2

Indien...

```js
s.events = ""; //blank value
```

...en de volgende code wordt uitgevoerd...

```js
s.events = s.apl(s.events, "event23");
```

... de uiteindelijke waarde van s.events is..

```js
s.events = "event23";
```

### Voorbeeld 4

Indien...

```js
s.prop4 = "hello|people";
```

...en de volgende code wordt uitgevoerd...

```js
s.eVar5 = s.apl(s.prop4, "today", "|");
```

... de definitieve waarde van s.prop4 zal nog zijn...

```js
s.prop4 = "hello|people";
```

...maar de uiteindelijke waarde van s.eVar5 zal

```js
s.eVar5 = "hello|people|today";
```

Houd er rekening mee dat de insteekmodule alleen een waarde retourneert. de variabele die door het lv - argument wordt doorgegeven , wordt niet noodzakelijkerwijs &quot; opnieuw ingesteld &quot; .

### Voorbeeld 5

Indien...

```js
s.prop4 = "hello|people";
```

...en de volgende code wordt uitgevoerd...

```js
s.prop4 = s.apl(s.prop4, "today");
```

... de definitieve waarde van s.prop4 zal zijn..

```js
s.prop4 = "hello|people,today";
```

Zorg ervoor dat het scheidingsteken consistent blijft tussen wat er in de waarde van het argument lv staat en wat er in de argumenten d1/d2 staat

### Voorbeeld 6

Indien...

```js
s.events = "event22,event23";
```

...en de volgende code wordt uitgevoerd...

```js
s.events = s.apl(s.events,"EVenT23", ",", ",", true);
```

... de uiteindelijke waarde van s.events zal zijn :

```js
s.events = "event22,event23,EVentT23";
```

Hoewel dit voorbeeld niet praktisch is, toont het de behoefte aan gebruiksvoorzichtigheid wanneer het gebruiken van de case gevoelige vlag aan.

### Voorbeeld 7

Indien...

```js
s.events = "event22,event23";
```

...en de volgende code wordt uitgevoerd...

```js
s.events = s.apl(s.events, "event23,event24,event25");
```

... de uiteindelijke waarde van s.events zal zijn :

```js
s.events = "event22,event23,event24,event25");
```

De plug-in voegt &quot;event23&quot; niet toe aan s.events omdat deze al bestaat in s.events.  Nochtans, zal het zowel event24 als event25 aan s.events toevoegen omdat geen van beiden eerder in s.events bevatte.

### Voorbeeld 8

Indien...

```js
s.linkTrackVars = "events,eVar1";
```

...en de volgende code wordt uitgevoerd...

```js
s.linkTrackVars = s.apl(s.linkTrackVars, "campaign", ",", ",", false);
```

... de uiteindelijke waarde van s.linkTrackVars is:

```js
s.linkTrackVars = "events,eVar1,campaign";
```

De laatste drie argumenten (d.w.z. &quot;,&quot;, &quot;,&quot;, false) aan het einde van deze appel-aanroep zijn niet nodig, maar hebben ook geen &quot;nadelige invloed&quot; doordat deze worden ingesteld omdat deze overeenkomen met de standaardargumentwaarden.

### Voorbeeld 9

Indien...

```js
s.events = "event22,event24";
```

...en de volgende code wordt uitgevoerd...

```js
s.apl(s.events, "event23");
```

... de definitieve waarde van s.events zal nog zijn:

```js
s.events = "event22,event24";
```

Als u de plug-in helemaal zelf uitvoert (zonder de geretourneerde waarde aan een variabele toe te wijzen), wordt de variabele die door het lv-argument is doorgegeven, niet opnieuw ingesteld.

### Voorbeeld 10

Indien...

```js
s.list2 = "casesensitivevalue|casesensitiveValue"
```

...en de volgende code wordt uitgevoerd...

```js
s.list2 = s.apl(s.list2, "CasESensiTiveValuE", "|", "-", true);
```

... de definitieve waarde van s.list2 zal zijn:

```js
s.list2 = "casesensitivevalue-casesensitiveValue-CasESensiTiveValuE"
```

Aangezien de twee delimiter argumenten verschillend zijn, zal de binnen overgegaan waarde door het eerste delimiter argument (&quot;|&quot;) worden afgebakend en dan samengevoegd door het tweede delimiter argument (&quot;-&quot;)

## Versiehistorie

### 4.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 3.2 (25 september 2019)

* De compatibiliteitsproblemen met `apl` aanroepen waarbij oudere versies van de plug-in werden gebruikt, zijn opgelost.
* Verwijderde consolewaarschuwingen om grootte te verminderen
* `inList 2.1` toegevoegd

### 3.1 (22 april 2018)

* `d2` argument wordt nu standaard ingesteld op de waarde van het  `d1` argument

### 3.0 (16 april 2018)

* Volledige heranalyse/herschrijven van plug-in
* Geavanceerde foutcontrole toegevoegd
* Het argument `vta` accepteert nu meerdere waarden tegelijk
* Het argument `d2` toegevoegd om de geretourneerde waarde op te maken
* Het argument `cc` is gewijzigd in een booleaanse waarde

### 2.5 (18 februari 2016)

* Gebruikt nu de `inList` methode voor vergelijkingsverwerking

### 2.0 (26 januari 2016)

* `d` (Scheidingsteken) argument nu optioneel (wordt standaard een komma)
* `u` (Markering voor hoofdlettergevoeligheid) argument is nu optioneel (wordt standaard ingesteld op hoofdlettergevoelig)
* Ongeacht het argument `u` (hoofdlettergevoeligheid) voegt de plug-in geen waarde meer toe aan een lijst als de waarde al in de lijst bestaat
