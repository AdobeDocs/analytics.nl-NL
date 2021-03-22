---
title: getPageName
description: Maak een eenvoudig te lezen pageName van het huidige websitepad.
translation-type: tm+mt
source-git-commit: 063da38c105072944a46ec0ab31930623b7974c8
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 0%

---


# Adobe-plug-in: getPageName

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de insteekmodule `getPageName` kunt u de huidige URL gemakkelijk lezen en een vriendelijke versie met opmaak gebruiken. Adobe raadt u aan deze insteekmodule te gebruiken als u een waarde [`pageName`](../page-vars/pagename.md) wilt instellen die gemakkelijk te begrijpen is in de rapportage. Deze insteekmodule is niet nodig als u al een naamgevingsstructuur hebt voor de variabele `pageName`, bijvoorbeeld via een gegevenslaag. Het wordt best gebruikt wanneer u geen andere oplossing hebt om `pageName` variabele te plaatsen.

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
   * Type handeling: Initialize getPageName
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
/* Adobe Consulting Plugin: getPageName v4.2 */
var getPageName=function(si,qv,hv,de){var a=si,b=qv,f=hv,e=de;if("-v"===a)return{plugin:"getPageName",version:"4.2"};a:{if("undefined"!==typeof window.s_c_il){var d=0;for(var g;d<window.s_c_il.length;d++)if(g=window.s_c_il[d],g._c&&"s_c"===g._c){d=g;break a}}d=void 0}"undefined"!==typeof d&&(d.contextData.getPageName="4.2");var c=location.hostname,h=location.pathname.substring(1).split("/"),l=h.length,k=location.search.substring(1).split("&"),m=k.length;d=location.hash.substring(1).split("&");g=d.length;e=e?e:"|";a=a?a:c;b=b?b:"";f=f?f:"";if(1===l&&""===h[0])a=a+e+"home";else for(c=0;c<l;c++)a=a+e+decodeURIComponent(h[c]);if(b&&(1!==m||""!==k[0]))for(h=b.split(","),l=h.length,c=0;c<l;c++)for(b=0;b<m;b++)if(h[c]===k[b].split("=")[0]){a=a+e+decodeURIComponent(k[b]);break}if(f&&(1!==g||""!==d[0]))for(f=f.split(","),k=f.length,c=0;c<k;c++)for(b=0;b<g;b++)if(f[c]===d[b].split("=")[0]){a=a+e+decodeURIComponent(d[b]);break}return a.substring(a.length-e.length)===e?a.substring(0,a.length-e.length):a};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De methode `getPageName` gebruikt de volgende argumenten:

* **`si`** (optioneel, tekenreeks): Een id die wordt ingevoegd aan het begin van de tekenreeks die de id van de site vertegenwoordigt. Deze waarde kan een numerieke id of een vriendelijke naam zijn. Wanneer deze niet is ingesteld, wordt standaard het huidige domein gebruikt.
* **`qv`** (optioneel, tekenreeks): Een door komma&#39;s gescheiden lijst met parameters van queryreeksen die, indien gevonden in de URL, worden toegevoegd aan de tekenreeks
* **`hv`** (optioneel, tekenreeks): Een door komma&#39;s gescheiden lijst met parameters gevonden in de URL-hash die, indien gevonden in de URL, aan de tekenreeks wordt toegevoegd
* **`de`** (optioneel, tekenreeks): Het scheidingsteken voor het opsplitsen van afzonderlijke delen van de tekenreeks. Heeft als standaardwaarde een pipe (`|`).

De methode retourneert een tekenreeks met een gebruiksvriendelijke versie van de URL. Deze tekenreeks wordt doorgaans toegewezen aan de variabele `pageName`, maar kan ook in andere variabelen worden gebruikt.

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

### Voorbeeld 2

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

Versie 4.0+ van de insteekmodule getPageName is niet afhankelijk van het bestaan van het te gebruiken object AppMeasurement van Adobe Analytics (d.w.z. het object &#39;s&#39;).  Als u verkiest om aan deze versie te bevorderen, ben zeker om de code te veranderen die stop-binnen roept door om het even welke instanties van het &quot;s&quot;voorwerp uit de vraag te verwijderen.
Wijzig bijvoorbeeld het volgende:

```js
s.pageName = s.getPageName();
```

...op dit punt:

```js
s.pageName = getPageName();
```

## Versiehistorie

### 4.2 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 4.1 (17 september 2019)

* Standaardwaarde voor scheidingstekens is gewijzigd in een pĳpteken (van een dubbele punt + spatie).

### 4.0 (22 mei 2018)

* Volledige heranalyse/herschrijven van plug-in
