---
title: getPageName
description: Maak een eenvoudig te lezen pageName van het huidige websitepad.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe-insteekmodule: getPageName

> [!IMPORTANT] Deze plug-in wordt geleverd door Adobe Consulting als een hoffelijkheid om u te helpen meer waarde te krijgen van Adobe Analytics. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `getPageName` insteekmodule kunt u de huidige URL gemakkelijk lezen en een gebruiksvriendelijke versie van de URL gebruiken. Adobe raadt u aan deze plug-in te gebruiken als u een [`pageName`](../page-vars/pagename.md) waarde wilt instellen die gemakkelijk te begrijpen is in de rapportage. Deze insteekmodule is niet nodig als u al een naamgevingsstructuur voor de `pageName` variabele hebt, bijvoorbeeld via een gegevenslaag. Het wordt best gebruikt wanneer u geen andere oplossing hebt om de `pageName` variabele te plaatsen.

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
   * Type handeling: Initialize getPageName
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
/* Adobe Consulting Plugin: getPageName v4.0 */
var getPageName=function(si,qv,hv,de){var c=location.hostname,f=location.pathname.substring(1).split("/"),h=f.length, g=location.search.substring(1).split("&"),l=g.length,k=location.hash.substring(1).split("&"),m=k.length;de=de?de:": ";si=si?si:c;qv= qv?qv:"";hv=hv?hv:"";if(1===h&&""===f[0])si=si+de+"home";else for(c=0;c<h;c++)si=si+de+decodeURIComponent(f[c]); if(qv&&(1!==l||""!== g[0]))for(f=qv.split(","),h=f.length,c=0;c<h;c++)for(qv=0;qv<l;qv++)if(f[c]===g[qv].split("=")[0]){si=si+de+decodeURIComponent(g[qv]);break}if(hv&&(1!==m||""!==k[0]))for(hv=hv.split(","),g=hv.length,c=0;c<g;c++)for(qv=0;qv<m;qv++)if(hv[c]===k[qv].split("=")[0]){si=si+de+decodeURIComponent(k[qv]);break}return si.substring(si.length-de.length)===de?si.substring(0,si.length-de.length):si};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `getPageName` methode gebruikt de volgende argumenten:

* **`si`** (optioneel, tekenreeks): Een id die wordt ingevoegd aan het begin van de tekenreeks die de id van de site vertegenwoordigt. Deze waarde kan een numerieke id of een vriendelijke naam zijn. Wanneer deze niet is ingesteld, wordt standaard het huidige domein gebruikt.
* **`qv`** (optioneel, tekenreeks): Een door komma&#39;s gescheiden lijst met parameters van queryreeksen die, indien gevonden in de URL, worden toegevoegd aan de tekenreeks
* **`hv`** (optioneel, tekenreeks): Een door komma&#39;s gescheiden lijst met parameters gevonden in de URL-hash die, indien gevonden in de URL, aan de tekenreeks wordt toegevoegd
* **`de`** (optioneel, tekenreeks): Het scheidingsteken voor het opsplitsen van afzonderlijke delen van de tekenreeks. Heeft als standaardwaarde een pijp (`|`).

De methode retourneert een tekenreeks met een gebruiksvriendelijke versie van de URL. Deze tekenreeks wordt doorgaans toegewezen aan de `pageName` variabele, maar kan ook in andere variabelen worden gebruikt.

## Voorbeelden van aanroepen

### Voorbeeld 1

Als de huidige URL...

```js
https://mail.google.com/mail/u/0/#inbox
```

...en de volgende code wordt uitgevoerd...

```js
s.pageName = getPageName()
```

...de definitieve waarde van s.pageName zal zijn:

```js
s.pageName = "mail.google.com|mail|u|0";
```

### Voorbeeld 2

Als de huidige URL...

```js
https://mail.google.com/mail/u/0/#inbox
```

...en de volgende code wordt uitgevoerd...

```js
s.pageName = getPageName("gmail")
```

...de definitieve waarde van s.pageName zal zijn:

```js
s.pageName = "gmail|mail|u|0";
```

### Voorbeeld 3

Als de huidige URL...

```js
https://www.google.com/
```

...en de volgende code wordt uitgevoerd...

```js
s.pageName = getPageName()
```

...de definitieve waarde van s.pageName zal zijn:

```js
s.pageName = "www.google.com|home"
```

**Opmerking**: Wanneer de code wordt uitgevoerd op een URL die geen pad bevat, wordt altijd de waarde &quot;home&quot; toegevoegd aan het einde van de geretourneerde waarde

### Voorbeeld 4

Als de huidige URL...

```js
https://www.google.com/
```

...en de volgende code wordt uitgevoerd...

```js
s.pageName = getPageName("google","","","|")
```

...de definitieve waarde van s.pageName zal zijn:

```js
s.pageName = "google|home"
```

### Voorbeeld 5

Als de huidige URL...

```js
https://www.hotelrooms.com/en/booking/room-booking.html?cid=1235#/step2&arrive=2018-05-26&depart=2018-05-27&numGuests=2
```

...en de volgende code wordt uitgevoerd...

```js
s.pageName = getPageName()
```

...de definitieve waarde van s.pageName zal zijn:

```js
s.pageName = "www.hotelrooms.com|en|booking|room-booking.html"
```

Als de volgende code echter wordt uitgevoerd...

```js
s.pageName = getPageName("hotelrooms","cid","arrive,numGuests",": ")
```

...de definitieve waarde van s.pageName zal zijn:

```js
s.pageName = "hotelrooms: en: booking: room-booking.html: cid=1235: arrive=2018-05-26: numGuests=2"
```

## Upgrade uitvoeren vanaf vorige versies

Versie 4.0+ van de insteekmodule getPageName is niet afhankelijk van het bestaan van het AppMeasurement-object van Adobe Analytics (dat wil zeggen het &#39;s&#39;-object) dat moet worden uitgevoerd.  Als u verkiest om aan deze versie te bevorderen, ben zeker om de code te veranderen die stop-binnen roept door om het even welke instanties van het &quot;s&quot;voorwerp uit de vraag te verwijderen.
Wijzig bijvoorbeeld het volgende:

```js
s.pageName = s.getPageName();
```

...op dit punt:

```js
s.pageName = getPageName();
```

## Versiehistorie

### 4.1 (17 september 2019)

* Standaardwaarde voor scheidingstekens is gewijzigd in een pĳpteken (van een dubbele punt + spatie).

### 4.0 (22 mei 2018)

* Volledige heranalyse/herschrijven van plug-in
