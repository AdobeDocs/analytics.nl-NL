---
title: getNewRepeat
description: Traceeractiviteiten van nieuwe versus herhaalde bezoekers.
translation-type: tm+mt
source-git-commit: 180ad544541f25d02b3a257559bc045abed7387b

---


# Adobe-insteekmodule: getNewRepeat

> [!IMPORTANT] Deze plug-in wordt geleverd door Adobe Consulting als een hoffelijkheid om u te helpen meer waarde te krijgen van Adobe Analytics. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `getNewRepeat` insteekmodule kunt u bepalen of een bezoeker van de site een nieuwe bezoeker of een herhaalde bezoeker is binnen een gewenst aantal dagen. Adobe raadt u aan deze insteekmodule te gebruiken als u bezoekers wilt identificeren als &#39;nieuw&#39; met behulp van een aangepast aantal dagen. Deze insteekmodule is niet nodig als de afmetingen voor nieuwe bezoekers/herhalingsbezoekers in de analysewerkruimte voldoen aan de behoeften van uw organisatie.

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
   * Type handeling: getNewRepeat initialiseren
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

Kopieer en plak de volgende code ergens in het AppMeasurement-bestand nadat het analytics tracking-object is geïnstantieerd (met `s_gi`). Door opmerkingen en versienummers van de code in uw implementatie te behouden, kan Adobe eventuele problemen oplossen.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getNewRepeat v2.1 */
s.getNewRepeat=function(d){d=d?d:30;var s=this,p="s_nr"+d,b=new Date,e=s.c_r(p),f=e.split("-"),c=b.getTime();b.setTime(c+864E5*d); if(""===e||18E4>c-f[0]&&"New"===f[1])return s.c_w(p,c+"-New",b),"New";s.c_w(p,c+"-Repeat",b);return"Repeat"};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `getNewRepeat` methode gebruikt de volgende argumenten:

* **`d`** (geheel getal, optioneel): Het minimumaantal dagen dat is vereist tussen bezoeken waarop bezoekers terugkeren naar `"New"`. Als dit argument niet is ingesteld, wordt het standaard ingesteld op 30 dagen.

Deze methode retourneert de waarde van `"New"` als de cookie die door de plug-in is ingesteld, niet bestaat of is verlopen. De waarde van `"Repeat"` als de cookie die door de plug-in is ingesteld, bestaat en de tijd sinds de huidige hit en de tijd die in de cookie is ingesteld, meer dan 30 minuten bedraagt. Deze methode keert de zelfde waarde voor een volledig bezoek terug.

Deze insteekmodule gebruikt een cookie met de naam `"s_nr[LENGTH]"` waar `[LENGTH]` het `d` argument gelijk is. Het cookie bevat een Unix-tijdstempel die de huidige tijd en de huidige status van de bezoeker (`"New"` of `"Repeat"`) vertegenwoordigt.

## Voorbeelden van aanroepen

### Voorbeeld 1

Met de volgende code wordt s.eVar1 ingesteld op de waarde &quot;New&quot; voor nieuwe bezoekers en wordt s.eVar1 ingesteld op de waarde &quot;New&quot; (met elke nieuwe aanroep) gedurende de rest van het bezoek van de bezoeker aan de site.

```js
s.eVar1=s.getNewRepeat();
```

### Voorbeeld 2

Als de bezoeker vanaf 31 minuten tot 30 dagen na de laatste keer dat s.getNewRepeat() werd aangeroepen, terugkeert naar de site, stelt de volgende code s.eVar1 in op de waarde &quot;Repeat&quot; en blijft s.eVar1 gelijk aan de waarde &quot;Repeat&quot; (met elke nieuwe aanroep) gedurende het resterende bezoek van de bezoeker aan de site.

```js
s.eVar1=s.getNewRepeat();
```

### Voorbeeld 3

Als de bezoeker niet minstens 30 dagen sinds de laatste tijd s.getNewRepeat() is geroepen geweest, zal de volgende code s.eVar1 aan de waarde van &quot;Nieuw&quot;plaatsen en zal s.eVar1 gelijk aan de waarde van &quot;Nieuw&quot;(met elke nieuwe vraag) blijven plaatsen gedurende het resterende gedeelte van het bezoek van de bezoeker aan de plaats.

```js
s.eVar1=s.getNewRepeat();
```

### Voorbeeld 4

Als de bezoeker 31 minuten tot 365 dagen (d.w.z. 1 jaar) sinds de laatste keer dat s.getNewRepeat() werd aangeroepen, terugkeert naar de site, zal de volgende code s.eVar1 gelijk stellen aan de waarde van &quot;Repeat&quot; en zal s.eVar1 gelijk blijven aan de waarde van &quot;Repeat&quot; (met elke nieuwe vraag) gedurende de rest van bezoek van de bezoeker aan de site .

```js
s.eVar1=s.getNewRepeat(365);
```

### Voorbeeld 5

Als de bezoeker niet minstens 365 dagen (d.w.z. 1 jaar) sinds de laatste tijd s.getNewRepeat() is geroepen geweest, zal de volgende code s.eVar1 gelijk aan de waarde van &quot;Nieuw&quot;plaatsen en s.eVar1 gelijk aan de waarde van &quot;Nieuw&quot;(met elke nieuwe vraag) door het restant van de bezoeker blijft plaatsen bezoek aan de site .

```js
s.eVar1=s.getNewRepeat(365);
```

## Versiehistorie

### 2.1 (30 september 2019)

* Herschikking van JavaScript-logica om de grootte van insteekmodules te verkleinen

### 2.0 (16 april 2018)

* Opnieuw gecompileerd met kleinere codegrootte
* De mogelijkheid om de cookie een naam te geven, is verwijderd. De insteekmodule geeft de cookie nu dynamisch een naam op basis van de waarde die aan het `d` argument is doorgegeven.
