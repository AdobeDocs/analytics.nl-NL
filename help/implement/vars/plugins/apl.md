---
title: apl (appendToList)
description: Voeg waarden toe aan variabelen die meerdere waarden ondersteunen.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe-insteekmodule: apl (appendToList)

> [!IMPORTANT] Deze plug-in wordt geleverd door Adobe Consulting als een hoffelijkheid om u te helpen meer waarde te krijgen van Adobe Analytics. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `apl` insteekmodule kunt u veilig nieuwe waarden toevoegen aan door lijsten gescheiden variabelen, zoals [`events`](../page-vars/events/events-overview.md), [`linkTrackVars`](../config-vars/linktrackvars.md), [`list`](../page-vars/list.md)en andere.

* Als de waarde die u wilt toevoegen niet in de variabele bestaat, voegt de code de waarde aan het einde van de tekenreeks toe.
* Als de waarde die u wilt toevoegen al in de variabele bestaat, wijzigt deze plug-in de waarde niet. Hierdoor kan uw implementatie dubbele waarden voorkomen.
* Als de variabele die u wilt toevoegen leeg is, stelt de plug-in de variabele in op de nieuwe waarde.

Adobe raadt u aan deze plug-in te gebruiken als u nieuwe waarden wilt toevoegen aan bestaande variabelen die een reeks gescheiden waarden bevatten. Deze plug-in is niet nodig als u tekenreeksen wilt samenvoegen voor variabelen met gescheiden waarden.

## De plug-in installeren met de Adobe Experience Platform Launch-extensie

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Go to the [!UICONTROL Extensions] tab, then click on the [!UICONTROL Catalog] button
1. De [!UICONTROL Common Analytics Plugins] extensie installeren en publiceren
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: Geen
   * Gebeurtenis: Kern - Bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: Gebruikelijke plug-ins voor Analytics
   * Type handeling: APL initialiseren (toevoegen aan lijst)
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met de aangepaste code-editor van Launch

Als u de extensie van de plug-in niet wilt gebruiken, kunt u de aangepaste code-editor gebruiken.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar het [!UICONTROL Extensions] tabblad en klik vervolgens op de [!UICONTROL Configure] knop onder de extensie Adobe Analytics.
1. Vouw de [!UICONTROL Configure tracking using custom code] accordeon uit, zodat de [!UICONTROL Open Editor] knop zichtbaar wordt.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

## De plug-in installeren met AppMeturement

Kopieer en plak de volgende code ergens in het AppMeasurement-bestand nadat het analytics tracking-object is geïnstantieerd (met [`s_gi`](../functions/s-gi.md)). Door opmerkingen en versienummers van de code in uw implementatie te behouden, kan Adobe eventuele problemen oplossen.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: apl (appendToList) v3.2 (Requires inList v2.0 or higher) */
s.apl=function(lv,vta,d1,d2,cc){if(!lv||"string"===typeof lv){if("undefined"===typeof this.inList||"string"!==typeof vta||""===vta)return lv;d1=d1||",";d2=d2||d1;1==d2&&(d2=d1,cc||(cc=1));2==d2&&1!=cc&&(d2=d1);vta=vta.split(",");for(var g=vta.length,e=0;e<g;e++)this.inList(lv,vta[e],d1,cc)||(lv=lv?lv+d2+vta[e]:vta[e])}return lv};

/* Adobe Consulting Plugin: inList v2.1 */
s.inList=function(lv,vtc,d,cc){if("string"!==typeof vtc)return!1;if("string"===typeof lv)lv=lv.split(d||",");else if("object"!== typeof lv)return!1;d=0;for(var e=lv.length;d<e;d++)if(1==cc&&vtc===lv[d]||vtc.toLowerCase()===lv[d].toLowerCase())return!0;return!1};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `apl` methode gebruikt de volgende argumenten:

* **`lv`** (vereist, tekenreeks): De variabele die een lijst met gescheiden items bevat waaraan een nieuwe waarde moet worden toegevoegd
* **`vta`** (vereist, tekenreeks): Een door komma&#39;s gescheiden lijst met de nieuwe waarden die aan de waarde van het `lv` argument moeten worden toegevoegd.
* **`d1`** (optioneel, tekenreeks): Het scheidingsteken dat wordt gebruikt om de afzonderlijke waarden te scheiden die al in het `lv` argument staan.  Heeft als standaardwaarde een komma (`,`).
* **`d2`** (optioneel, tekenreeks): Het uitvoerscheidingsteken. De standaardwaarde is dezelfde waarde als `d1` wanneer deze niet is ingesteld.
* **`cc`** (optioneel, Booleaans): Een markering die aangeeft of een hoofdlettergevoelige controle wordt gebruikt. Indien `true`de duplicatiecontrole hoofdlettergevoelig is. Indien `false` of niet ingesteld, is de duplicatiecontrole niet hoofdlettergevoelig. Wordt standaard ingesteld op `false`.

De `apl` methode retourneert de waarde van het `lv` argument plus eventuele niet-gedupliceerde waarden in het `vta` argument.

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

### Voorbeeld 2

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

### Voorbeeld 3

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

...maar de definitieve waarde van s.eVar5 zal zijn

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

### 3.2 (25 september 2019)

* Compatibiliteitsproblemen verholpen met `apl` aanroepen waarbij oudere versies van de plug-in werden gebruikt
* Verwijderde consolewaarschuwingen om grootte te verminderen
* Toegevoegd `inList 2.1`

### 3.1 (22 april 2018)

* `d2` argument wordt nu standaard ingesteld op de waarde van het `d1` argument

### 3.0 (16 april 2018)

* Volledige heranalyse/herschrijven van plug-in
* Geavanceerde foutcontrole toegevoegd
* Het `vta` argument accepteert nu meerdere waarden tegelijk
* Het `d2` argument toegevoegd om de geretourneerde waarde op te maken
* Het `cc` argument is gewijzigd in een Booleaanse waarde

### 2.5 (18 februari 2016)

* Gebruikt nu de `inList` vergelijkingsmethode

### 2.0 (26 januari 2016)

* `d` (Scheidingsteken) argument nu optioneel (wordt standaard een komma)
* `u` (Markering voor hoofdlettergevoeligheid) argument is nu optioneel (wordt standaard ingesteld op hoofdlettergevoelig)
* Ongeacht het argument `u` (hoofdlettergevoeligheid) voegt de plug-in geen waarde meer toe aan een lijst als de waarde al in de lijst bestaat