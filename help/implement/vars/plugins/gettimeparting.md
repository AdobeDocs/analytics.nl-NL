---
title: getTimeParting
description: Meet het tijdstip waarop een specifieke actie plaatsvindt.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Adobe-insteekmodule: getTimeParting

>[!IMPORTANT] Deze plug-in wordt geleverd door Adobe Consulting als een hoffelijkheid om u te helpen meer waarde te krijgen van Adobe Analytics. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `getTimeParting` insteekmodule kunt u de details vastleggen van het tijdstip waarop een meetbare activiteit op uw site plaatsvindt. Deze insteekmodule is waardevol wanneer u metriek door om het even welke herhaalbare verdeling van tijd over een bepaalde datumwaaier wilt breken. U kunt bijvoorbeeld de conversiekoersen vergelijken tussen twee verschillende dagen van de week, zoals alle zondag en alle donderdag. U kunt periodes van de dag ook vergelijken, zoals alle ochtenden tegenover alle avonden.

De analysewerkruimte biedt vergelijkbare, kant-en-klare afmetingen die iets anders zijn opgemaakt dan deze plug-in. Zie de afmetingen voor [tijdpartering](/help/analyze/analysis-workspace/components/dimensions/time-parting-dimensions.md) in de gebruikershandleiding Analyseren voor meer informatie. Sommige organisaties vinden dat de uit-van-de-doos afmetingen van de Werkruimte van de Analyse voldoende zijn.

>[Belangrijke] versie 4.0+ van deze plug-in wijkt sterk af van eerdere versies. Adobe raadt u ten zeerste aan deze plug-in volledig te implementeren. Code die verwijst naar de insteekmodule vóór versie 4.0 is niet compatibel met de huidige versie van deze insteekmodule.

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
   * Type handeling: getTimeParting initialiseren
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
/* Adobe Consulting Plugin: getTimeParting v6.2 */
var getTimeParting=function(a){a=document.documentMode?void 0:a||"Etc/GMT";a=(new Date).toLocaleDateString("en-US",{timeZone:a, minute:"numeric",hour:"numeric",weekday:"long",day:"numeric",year:"numeric",month:"long"});a=/([a-zA-Z]+).*?([a-zA-Z]+).*?([0-9]+).*?([0-9]+)(.*?)([0-9])(.*)/.exec(a);return"year="+a[4]+" | month="+a[2]+" | date="+a[3]+" | day="+a[1]+" | time="+(a[6]+a[7])};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `getTimeParting` methode gebruikt het volgende argument:

**`t`** (Optioneel maar aanbevolen, tekenreeks): De naam van de tijdzone waarnaar de lokale tijd van de bezoeker moet worden omgezet.  Wordt standaard ingesteld op UTC/GMT-tijd. Zie [Lijst van de tijdzones](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones) van de TZ- gegevensbestandtijd op Wikipedia voor een volledige lijst van geldige waarden.

Veelvoorkomende geldige waarden zijn:

* `"America/New_York"` voor Oost Tijd
* `"America/Chicago"` voor Central Time
* `"America/Denver"` voor Mountain Time
* `"America/Los_Angeles"` voor Pacific Time

Wanneer deze methode wordt aangeroepen, wordt een tekenreeks geretourneerd die de volgende door een pipe (`|`) gescheiden tekens bevat:

* Het lopende jaar
* De huidige maand
* De dag van de maand
* De dag van de week
* De huidige tijd (AM/PM)

## Voorbeelden van aanroepen

### Voorbeelden voor specifieke tijdzones

Gebruik de volgende voorbeeldcode als de cliënt in Parijs, Frankrijk is:

```js
s.eVarX = getTimeParting("Europe/Paris");
```

Als de client zich in San Jose, Californië bevindt:

```js
s.eVarX = getTimeParting("America/Los_Angeles");
```

Als de klant zich in het Afrikaanse land Ghana bevindt:

```js
s.eVarX = getTimeParting();
```

Ghana bevindt zich binnen de tijdzone UTC/GMT.  In dit voorbeeld wordt getoond dat onder dergelijke omstandigheden geen insteekmoduleargument nodig is.

### Boekhouding voor Internet Explorer-browsers

Gebruik het volgende voorbeeld als u parting van gegevens bij tijd wilt uitsluiten van Internet Explorer-bezoekers (aangezien de waarde die wordt geretourneerd door IE-browsers alleen in de lokale tijd van de bezoeker kan worden weergegeven)

```js
if(!document.documentMode) s.eVarX = getTimeParting("America/New_York");
else s.eVarX = "Internet Explorer Visitors";
```

### Resultaten van vraag

Als een bezoeker uit Denver, Colorado, op 31 augustus 2020 om 9:15 uur een site bezoekt,

De volgende code uitvoeren...

```js
s.eVar10 = getTimeParting("Europe/Athens");
```

...zou s.eVar10 gelijk stellen aan &quot;year=2020| month=August| date=31| day=vrijdag| time=6:15 PM&quot;

De volgende code...

```js
s.eVar10 = getTimeParting("America/Nome");
```

...zou s.eVar10 gelijk stellen aan &quot;year=2020| month=August| date=31| day=vrijdag| time=6:15 AM&quot;

De volgende code...

```js
s.eVar10 = getTimeParting("Asia/Calcutta");
```

...zou s.eVar10 gelijk stellen aan &quot;year=2020| month=August| date=31| day=vrijdag| time=8:45 PM&quot;

En de volgende code...

```js
s.eVar10 = getTimeParting("Australia/Sydney");
```

...zou s.eVar10 gelijk stellen aan &quot;year=2020| month=September| date=1| day=zaterdag| time=1:15 AM&quot;

## Versiehistorie

### 6.2 (5 november 2019)

* Kleine opgeloste problemen
* Verminderde algemene codegrootte

### 6.1 (26 november 2018)

* Oplossen voor Internet Explorer-browsers. Ze kunnen de tijd retourneren, maar alleen in de lokale tijd van de bezoeker.

### 6.0 (14 augustus 2018)

* Volledig herschrijven om aan internationale normen te voldoen. Hiermee converteert u nu zomertijd en alle tijdzones op de juiste wijze.

### 5.0 (17 april 2018)

* Point Release (opnieuw gecompileerd, kleinere codegrootte)
* De noodzaak van de `tpDST` parameter is verwijderd, omdat de begin- en einddatum van de zomertijd nu automatisch worden gedetecteerd

### 4.0 (22 augustus 2016)

* Verstrekt een gloednieuwe oplossing en omvat nu jaar, maand, en datuminformatie.
