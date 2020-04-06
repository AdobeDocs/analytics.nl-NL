---
title: addProductEvent
description: Voegt aangepaste gebeurtenissen toe aan de variabele producten en gebeurtenissen.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Adobe-insteekmodule: addProductEvent

>[!IMPORTANT] Deze plug-in wordt geleverd door Adobe Consulting als een hoffelijkheid om u te helpen meer waarde te krijgen van Adobe Analytics. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `addProductEvent` insteekmodule wordt een numerieke gebeurtenis of valutagebeurtenis aan de [`products`](../page-vars/products.md) variabele toegevoegd. Adobe raadt u aan deze plug-in te gebruiken als u een numerieke of valutagebeurtenis aan de `products` variabele wilt toevoegen zonder dat u zich zorgen hoeft te maken over de indeling van de productreeks. Deze insteekmodule is niet nodig als u geen numerieke of valutagebeurtenissen in de `products` variabele gebruikt.

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
   * Type handeling: AddProductEvent initialiseren
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
/* Adobe Consulting Plugin: addProductEvent v1.0 (Requires apl v3.1 and inList v2.0+ plug-ins) */
s.addProductEvent=function(en,ev,ap){var s=this;if("string"===typeof en)if(ev=isNaN(ev)?"1":String(ev),ap=ap||!1,s.events= s.apl(s.events,en),s.products){var e=s.products.split(",");ap=ap?0:e.length-1;for(var a;ap<e.length;ap++)a=e[ap].split(";") ,a[4]&&a[4].includes("event")?a[4]=a[4]+"|"+en+"="+ev:a[5]?a[4]=en+"="+ev:a[4]||(a[3]||(a[3]=""),a[2]||(a[2]=""),a[1]||(a[1]=""),a[4]=en+"="+ev),e[ap]=a.join(";");s.products=e.join(",")}else s.products=";;;;"+en+"="+ev};

/* Adobe Consulting Plugin: apl (appendToList) v3.2 (Requires inList v2.0 or higher) */
s.apl=function(lv,vta,d1,d2,cc){if(!lv||"string"===typeof lv){if("undefined"===typeof this.inList||"string"!==typeof vta||""===vta)return lv;d1=d1||",";d2=d2||d1;1==d2&&(d2=d1,cc||(cc=1));2==d2&&1!=cc&&(d2=d1);vta=vta.split(",");for(var g=vta.length,e=0;e<g;e++)this.inList(lv,vta[e],d1,cc)||(lv=lv?lv+d2+vta[e]:vta[e])}return lv};

/* Adobe Consulting Plugin: inList v2.1 */
s.inList=function(lv,vtc,d,cc){if("string"!==typeof vtc)return!1;if("string"===typeof lv)lv=lv.split(d||",");else if("object"!== typeof lv)return!1;d=0;for(var e=lv.length;d<e;d++)if(1==cc&&vtc===lv[d]||vtc.toLowerCase()===lv[d].toLowerCase())return!0;return!1};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `addProductEvent` methode gebruikt de volgende argumenten:

* **`en`** (vereist, tekenreeks): De gebeurtenis die aan de laatste ingang in de `products` variabele moet worden toegevoegd. Als de `products` variabele leeg is, wordt een &quot;lege&quot; productitem gemaakt met de gebeurtenis (en de waarde ervan) gekoppeld.
* **`ev`** (vereist, tekenreeks): De waarde die is toegewezen aan de gebeurtenis numeric of currency in het `en` argument.  Wordt standaard ingesteld `1` wanneer niet ingesteld.
* **`ap`** (optioneel, Booleaans): Als de productvariabele momenteel meer dan één productvermelding bevat, voegt een waarde van `true` (of `1`) de gebeurtenis aan alle productvermeldingen toe.  Wordt standaard ingesteld `false` wanneer niet ingesteld.

De `addProductEvent` geeft niets. In plaats daarvan worden de gebeurtenis en de waarde ervan toegevoegd aan de `products` variabele. De insteekmodule voegt de gebeurtenis ook automatisch toe aan de [`events`](../page-vars/events/events-overview.md) variabele, aangezien deze daar ook verplicht is.

## Cookies

Met de insteekmodule addProductEvent worden geen cookies gemaakt of gebruikt

## Voorbeelden van aanroepen

### Voorbeeld 1

Met de volgende code wordt de `s.products` variabele ingesteld op `";product1;3;300,;product2;2;122,;product3;1;25;event35=25"`.

```js
s.products=";product1;3;300,;product2;2;122,;product3;1;25"
s.events="purchase";
s.addProductEvent("event35", "25");
```

De bovenstaande code stelt de `s.events` variabele ook in op `"purchase,event35"`

### Voorbeeld 2

Met de volgende code wordt de `s.products` variabele ingesteld op `";product1;3;300;event35=25,;product2;2;122;event35=25,;product3;1;25;event35=25"`

```js
s.products=";product1;3;300,;product2;2;122,;product3;1;25";
s.addProductEvent("event35", 25, 1);
```

Wanneer het derde argument in de `addProductEvent` vraag `true` (of `1`) is, heeft elke productingang de gebeurtenis die in de vraag wordt gespecificeerd die aan zijn waarde wordt toegevoegd.

### Voorbeeld 3

Met de volgende code wordt de `s.products` variabele ingesteld op `";product1;3;300;event2=10;eVar33=large|eVar34=men|eVar35=blue,;product2;2;122,;product3;1;25;event33= 12|event34=10|event35=15"`

```js
s.products=";product1;3;300;event2=10;eVar33=large|eVar34=men|eVar35=blue,;product2;2;122,;product3;1;25";
s.events="purchase,event2";
s.addProductEvent("event33", "12");
s.addProductEvent("event34", "10");
s.addProductEvent("event35", "15");
```

De bovenstaande code stelt de `s.events` variabele ook in op `"purchase,event2,event33,event34,event35"`

### Voorbeeld 4

Met de volgende code wordt de `s.products` variabele ingesteld op `";product1;3;300;event2=10|event33=12|event34=10|event35=15;eVar33=large|eVar34=men|eVar35=blue, ;product2;2;122;event33=12|event34=10|event35=15,;product3;1;25;event33=12|event34=10|event35=15"`

```js
s.products=";product1;3;300;event2=10;eVar33=large|eVar34=men|eVar35=blue,;product2;2;122,;product3;1;25"
s.events="purchase,event2"
s.addProductEvent("event33", "12", 1);
s.addProductEvent("event34", 10, 1);
s.addProductEvent("event35", "15", 1);
```

De bovenstaande code stelt de `s.events` variabele ook in op `"purchase,event2,event33,event34,event35"`.

>[!NOTE] Het tweede argument in de aanroep kan een geheel getal zijn **of** een tekenreeks die een geheel getal/getal vertegenwoordigt

### Voorbeeld 5

Indien `s.products` nog niet ingesteld, wordt deze door de volgende code ingesteld op `";;;;event35=25"`

```js
s.addProductEvent("event35", "25");
```

Bovenstaande code voegt ook toe `"event35"` aan het einde van `s.events` of **, als** deze nog niet is ingesteld, wordt de bovenstaande code ingesteld `s.events` `s.events` op `"event35"`

## Versiehistorie

### 1.0 (7 oktober 2019)

* Eerste release.
