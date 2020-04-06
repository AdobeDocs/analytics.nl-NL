---
title: getPreviousValue
description: Hiermee wordt de laatste waarde opgehaald die in een variabele is doorgegeven.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Adobe-insteekmodule: getPreviousValue

>[!IMPORTANT] Deze plug-in wordt geleverd door Adobe Consulting als een hoffelijkheid om u te helpen meer waarde te krijgen van Adobe Analytics. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `getPreviousValue` plug-in kunt u een variabele instellen op een waarde die bij een vorige hit is ingesteld. Deze insteekmodule is niet nodig als de implementatie alle gewenste waarden in de huidige hit bevat.

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
   * Type handeling: getPreviousValue initialiseren
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
/* Adobe Consulting Plugin: getPreviousValue v2.0 */
s.getPreviousValue=function(v,c){var s=this,d;c=c||"s_gpv";var b=new Date;b.setTime(b.getTime()+18E5);s.c_r(c)&&(d=s.c_r(c)); v?s.c_w(c,v,b):s.c_w(c,d,b);return d};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `getPreviousValue` methode gebruikt de volgende argumenten:

* **`v`** (tekenreeks, vereist): De variabele met de waarde die u wilt doorgeven aan de volgende afbeeldingsaanvraag. Een veelgebruikte variabele is het ophalen van de vorige paginawaarde. `s.pageName`
* **`c`** (tekenreeks, optioneel): De naam van het cookie waarin de waarde wordt opgeslagen.  Als dit argument niet is ingesteld, wordt standaard ingesteld op `"s_gpv"`.

Wanneer u deze methode aanroept, wordt de tekenreekswaarde in het cookie geretourneerd. De insteekmodule stelt vervolgens de vervaldatum van het cookie opnieuw in en wijst er de waarde van de variabele aan toe vanuit het `v` argument. Het cookie verloopt na 30 minuten inactiviteit.

## Voorbeelden van aanroepen

### Voorbeeld 1

De volgende code...

```js
s.prop7=s.getPreviousValue(s.pageName,"gpv_Page")
```

* Stelt s.prop7 eerst in op de waarde die in s.pageName is doorgegeven in het vorige afbeeldingsverzoek (dat wil zeggen de waarde die is opgeslagen in het cookie &quot;gpv_Page&quot;).
* De code herstelt vervolgens het cookie &quot;gpv_Page&quot;, waardoor deze gelijk is aan de huidige waarde van s.pageName
* Als s.pageName niet op het tijdstip wordt geplaatst deze code loopt, dan zal de code de vervaldatum voor de huidige waarde van het koekje terugstellen

### Voorbeeld 2

De volgende codesets s.prop7 is gelijk aan de laatste waarde die in s.pageName wordt overgegaan, maar slechts als event1 ook bevat binnen s.events is, zoals die via de insteekmodule inList wordt bepaald, op het tijdstip dat de vraag plaatsvindt.

```js
if(s.inList(s.events,"event1")) s.prop7=s.getPreviousValue(s.pageName,"gpv_Page");
```

### Voorbeeld 3

De volgende codesets s.prop7 is gelijk aan de laatste waarde die in s.pageName wordt doorgegeven, maar alleen als s.pageName momenteel op de pagina tegelijkertijd is ingesteld.

```js
if(s.pageName) s.prop7=s.getPreviousValue(s.pageName,"gpv_Page");
```

### Voorbeeld 4

De volgende codesets s.eVar10 is gelijk aan de waarde die in s.eVar1 in de vorige afbeeldingsaanvraag is doorgegeven.   De vorige eVar1-waarde zou in het cookie &quot;s_gpv&quot; zijn opgenomen.  De code stelt vervolgens het cookie &#39;s_gpv&#39; in op de huidige waarde van s.eVar1.

```js
s.eVar10 = s.getPreviousValue(s.eVar1)
```

## Onwaarschijnlijke Kwartels

Als de variabele die aan het v-argument is gekoppeld, op een nieuwe waarde is ingesteld en de insteekmodule getPreviousValue wordt uitgevoerd MAAR een aanroep van de Analytics-server NIET tegelijkertijd wordt verzonden, wordt de nieuwe v-argumentwaarde de volgende keer dat de insteekmodule wordt uitgevoerd, nog steeds als de &quot;vorige waarde&quot; beschouwd.
Stel bijvoorbeeld dat de volgende code op de eerste pagina van het bezoek wordt uitgevoerd:

```js
s.pageName="home"
s.prop7=s.getPreviousValue(s.pageName,"gpv_Page")
s.t();
```

Deze code zou een servervraag veroorzaken waar het pageName argument aan &quot;huis&quot;gelijk is en het p7 (prop7) argument niet wordt geplaatst.  Nochtans, zou de vraag aan s.getPreviousValue de waarde van s.pageName (d.w.z. &quot;home&quot;) in het cookie dat in de aanroep is opgegeven (bijvoorbeeld het cookie &quot;gpv_Page&quot;).
Ga er nu van uit dat onmiddellijk daarna op dezelfde pagina de volgende code wordt uitgevoerd (om welke reden dan ook):

```js
s.pageName="happy value"
s.prop7=s.getPreviousValue(s.pageName,"gpv_Page")
```

Aangezien de functie s.t() niet in dit codeblok wordt uitgevoerd, wordt er geen andere afbeeldingsaanvraag gemaakt.  Wanneer de functiecode s.getPreviousValue() deze keer wordt uitgevoerd, wordt s.prop7 echter ingesteld op de vorige waarde van s.pageName (dat wil zeggen: &quot;home&quot;) en slaat vervolgens de nieuwe waarde van s.pageName (d.w.z. &quot;happy value&quot;) in het cookie &quot;gpv_Page&quot;.
Stel dat de bezoeker naar een andere pagina navigeert en de volgende code op deze pagina wordt uitgevoerd:

```js
s.pageName="page 2"
s.prop7=s.getPreviousValue(s.pageName,"gpv_Page")
s.t();
```

Wanneer de s.t () vraagfunctie loopt, zal het tot een beeldverzoek leiden waar s.pageName=&quot;pagina 2&quot;en s.prop7 aan &quot;gelukkig waarde&quot;is, die de waarde van s.pageName was toen de laatste vraag aan getPreviousValue plaatsvond.   De s.prop7 waarde van &quot;huis&quot;was nooit in om het even welk echt beeldverzoek ingesloten alhoewel &quot;huis&quot;de eerste waarde was die in s.pageName wordt overgegaan.

## Versiehistorie

### v2.0 (7 oktober 2019)

* Puntrelease (volledige logica herschrijven).
