---
title: rfl
description: Verwijder een specifieke waarde uit een tekenreeks met een teken als scheidingsteken.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe-insteekmodule: rfl (verwijderen uit lijst)

> [!IMPORTANT] Deze plug-in wordt geleverd door Adobe Consulting als een hoffelijkheid om u te helpen meer waarde te krijgen van Adobe Analytics. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `rfl` insteekmodule kunt u &quot;veilig&quot; waarden verwijderen uit afgebakende tekenreeksen, zoals [`events`](../page-vars/events/events-overview.md), [`products`](../page-vars/products.md), [`list`](../page-vars/list.md)en andere. Deze plug-in is handig als u specifieke waarden uit een tekenreeks met scheidingstekens wilt verwijderen zonder dat u zich zorgen hoeft te maken over scheidingstekens. Verscheidene andere stop-ins hangen van deze code af correct in werking te stellen. Deze insteekmodule is niet nodig als u een specifieke functie niet hoeft uit te voeren voor meer dan één variabele Analytics tegelijk, of als u geen afhankelijke insteekmodules gebruikt.

De plug-in gebruikt de volgende logica:

* Als de waarde die u wilt verwijderen bestaat, blijft alles in de variabele behouden, behalve de waarde die u wilt verwijderen.
* Als de waarde die u wilt verwijderen niet bestaat, behoudt de plug-in de oorspronkelijke tekenreeks ongewijzigd.

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
   * Type handeling: RFP initialiseren (verwijderen uit lijst)
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
/* Adobe Consulting Plugin: rfl (removeFromList) v2.01 */
s.rfl=function(lv,vr,d1,d2,df){if(!lv||!vr)return"";var d=[],b="";d2=d2?d2:d1;df=df?!0:!1;lv=lv.split(d1?d1:",");d1=lv.length;for(var c=0;c<d1;c++)-1<lv[c].indexOf(":")&&(b=lv[c].split(":"),b[1]=b[0]+":"+b[1],lv[c]=b[0]),-1<lv[c].indexOf("=")&&(b=lv[c].split("="), b[1]=b[0]+"="+b[1],lv[c]=b[0]),lv[c]!==vr&&b?d.push(b[1]):lv[c]!==vr?d.push(lv[c]):lv[c]===vr&&df&&(b?d.push(b[1]):d.push(lv[c]),df=!1),b="";return d.join(d2)};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `rfl` methode gebruikt de volgende argumenten:

* **`lv`** (vereist, tekenreeks): Een variabele (of tekenreeks) die een lijst met gescheiden waarden bevat
* **`vr`** (vereist, tekenreeks): De waarde die u uit het `lv` argument wilt verwijderen. Adobe raadt u af meerdere waarden tijdens één `rfl` aanroep te verwijderen.
* **`d1`** (optioneel, tekenreeks): Het scheidingsteken dat het `lv` argument gebruikt. Heeft als standaardwaarde een komma (`,`).
* **`d2`** (optioneel, tekenreeks): Het scheidingsteken dat u de retourtekenreeks wilt gebruiken. Heeft standaard dezelfde waarde als het `d1` argument.
* **`df`** (optioneel, Booleaans): Indien `true`, slechts dubbele instanties van het `vr` argument van het `lv` argument in plaats van alle instanties. Wordt standaard ingesteld `false` wanneer niet ingesteld.

Wanneer deze methode wordt aangeroepen, wordt een gewijzigde tekenreeks geretourneerd die het `lv` argument bevat, maar zonder instanties (of dubbele instanties) van de waarde die in het `vr` argument is opgegeven.

## Voorbeelden van aanroepen

### Voorbeeld 1

Indien...

```js
s.events = "event22,event24,event25";
```

...en de volgende code wordt uitgevoerd...

```js
s.events = s.rfl(s.events,"event24");
```

...de uiteindelijke waarde van s.events zal zijn :

```js
s.events = "event22,event25";
```

### Voorbeeld 2

Indien...

```js
s.events = "event22,event24,event25";
```

...en de volgende code wordt uitgevoerd...

```js
s.events = s.rfl(s.events,"event26");
```

...de uiteindelijke waarde van s.events zal zijn :

```js
s.events = "event22,event24,event25";
```

In dit voorbeeld heeft de rfl-aanroep geen wijzigingen aangebracht in s.events omdat s.events geen &quot;event26&quot; bevatte

### Voorbeeld 3

Indien...

```js
s.events = "event22,event24,event25";
```

...en de volgende code wordt uitgevoerd...

```js
s.events = s.rfl(s.events);
```

...de uiteindelijke waarde van s.events zal zijn :

```js
s.events = "";
```

Als het argument lv of het argument vr in een s.rfl vraag leeg zijn, dan zal de stop - binnen niets terugkeren

### Voorbeeld 4

Indien...

```js
s.prop4 = "hello|people|today";
```

...en de volgende code wordt uitgevoerd...

```js
s.eVar5 = s.rfl(s.prop4,"people","|");
```

...de definitieve waarde van s.prop4 zal nog zijn...

```js
s.prop4 = "hello|people|today";
```

...maar de uiteindelijke waarde van s.eVar5 is:

```js
s.eVar5 = "hello|today";
```

Houd er rekening mee dat de insteekmodule alleen een waarde retourneert. de variabele die via het lv - argument wordt doorgegeven , wordt niet opnieuw ingesteld .

### Voorbeeld 5

Indien...

```js
s.prop4 = "hello|people|today";
```

...en de volgende code wordt uitgevoerd...

```js
s.prop4 = s.rfl(s.prop4,"people");
```

...de definitieve waarde van s.prop4 zal nog zijn...

```js
s.prop4 = "hello|people|today";
```

U moet het argument d1 instellen wanneer de waarde van het argument lv een ander scheidingsteken bevat dan de standaardwaarde (dus komma).

### Voorbeeld 6

Indien...

```js
s.events = "event22,event23,event25";
```

...en de volgende code wordt uitgevoerd...

```js
s.events = s.rfl(s.events,"EVenT23");
```

...de uiteindelijke waarde van s.events zal zijn :

```js
s.events = "event22,event23,event25";
```

Hoewel dit voorbeeld niet praktisch is, toont het de behoefte aan om in case-sensitive waarden over te gaan.

### Voorbeeld 7

Indien...

```js
s.events = "event22,event23:12345,event25";
```

...en de volgende code wordt uitgevoerd...

```js
s.events = s.rfl(s.events,"event23");
```

...de uiteindelijke waarde van s.events zal zijn :

```js
s.events = "event22,event25";
```

### Voorbeeld 8

Indien...

```js
s.events = "event22,event23:12345,event25";
```

...en de volgende code wordt uitgevoerd...

```js
s.events = s.rfl(s.events,"event23:12345");
```

...de uiteindelijke waarde van s.events zal zijn :

```js
s.events = "event22,event23:12345,event25";
```

Wanneer u een gebeurtenis moet verwijderen die rangschikking en/of numerieke/muntsyntaxis gebruikt, zou u slechts de gebeurtenis zelf (d.w.z. zonder de rangschikking/numerieke/muntwaarden) in de s.rfl vraag moeten specificeren.

### Voorbeeld 9

Indien...

```js
s.events = "event22,event23,event23,event23,event24,event25";
```

...en de volgende code wordt uitgevoerd...

```js
s.events = s.rfl(s.events,"event23");
```

...de uiteindelijke waarde van s.events zal zijn :

```js
s.events = "event22,event24,event25");
```

### Voorbeeld 10

Indien...

```js
s.events = "event22,event23,event23,event23,event24,event25";
```

...en de volgende code wordt uitgevoerd...

```js
s.events = s.rfl(s.events,"event23", "", "",true);
```

...de uiteindelijke waarde van s.events zal zijn :

```js
s.events = "event22,event23,event24,event25");
```

### Voorbeeld 11

Indien...

```js
s.events = "event22,event23,event23,event23,event24,event25";
```

...en de volgende code wordt uitgevoerd...

```js
s.events = s.rfl(s.events,"event23", "", "|",true);
```

...de uiteindelijke waarde van s.events zal zijn :

```js
s.events = "event22|event23|event24|event25");
```

### Voorbeeld 12

Indien...

```js
s.events = "event22,event23,event24,event25";
```

...en de volgende code wordt uitgevoerd...

```js
s.events = s.rfl(s.events,"event23,event24");
```

...de uiteindelijke waarde van s.events zal zijn :

```js
s.events = "event22,event23,event24,event25";
```

Het instellen van meerdere waarden in het vr-argument wordt niet ondersteund. De rfl-logica in het bovenstaande voorbeeld zou eerst de waarden in het lv-argument (d.w.z. s.events) opsplitsen en vervolgens proberen om elke gescheiden waarde te koppelen aan de volledige waarde van het vr-argument (d.w.z. &quot;event23,event24&quot;).

### Voorbeeld 13

Indien...

```js
s.events = "event22,event23,event24,event25";
```

...en de volgende code wordt uitgevoerd...

```js
s.events = s.rfl(s.events,"event23");
s.events = s.rfl(s.events,"event24");
```

...de uiteindelijke waarde van s.events zal zijn :

```js
s.events = "event22,event25");
```

Elke waarde die uit de lijst moet worden verwijderd, moet zich binnen de eigen aanroep s.rfl bevinden.

### Voorbeeld 14

Indien...

```js
s.linkTrackVars = "events,eVar1,eVar2,eVar3";
```

...en de volgende code wordt uitgevoerd...

```js
s.linkTrackVars = s.rfl(s.linkTrackVars,"eVar2", ",", ",", false);
```

...de uiteindelijke waarde van s.linkTrackVars is:

```js
s.linkTrackVars = "events,eVar1,eVar3";
```

De laatste drie argumenten (d.w.z. &quot;,&quot;,&quot;,&quot;, vals) aan het eind van deze s.rfl vraag zijn niet noodzakelijk maar &quot;richten ook niets&quot;door daar te zijn aangezien zij de standaardmontages aanpassen.

### Voorbeeld 15

Indien...

```js
s.events = "event22,event23,event24";
```

...en de volgende code wordt uitgevoerd...

```js
s.rfl(s.events,"event23");
```

...de definitieve waarde van s.events zal nog zijn:

```js
s.events = "event22,event23,event24";
```

Vergeet ook niet dat de insteekmodule alleen een waarde retourneert. de variabele die via het lv - argument wordt doorgegeven , wordt niet opnieuw ingesteld .

## Versiehistorie

### 2.01 (17 september 2019)

* Kleine bug-correctie voor de standaardwaarde van het scheidingsteken

### 2.0 (16 april 2018)

* Puntrelease (opnieuw gecompileerd, kleiner codeformaat).
* De noodzaak voor de `join` plug-in is verwijderd.

### 1.0 (18 juli 2016)

* Eerste release.
