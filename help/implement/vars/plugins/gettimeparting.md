---
title: getTimeParting
description: Meet het tijdstip waarop een specifieke actie plaatsvindt.
exl-id: 3fab36c8-a006-405a-9ef1-2547c2b36b0d
source-git-commit: ab078c5da7e0e38ab9f0f941b407cad0b42dd4d1
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 0%

---

# Adobe-plug-in: getTimeParting

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `getTimeParting`-plug-in kunt u de details vastleggen van het tijdstip waarop een meetbare activiteit op uw site plaatsvindt. Deze insteekmodule is waardevol wanneer u metriek door om het even welke herhaalbare verdeling van tijd over een bepaalde datumwaaier wilt breken. U kunt bijvoorbeeld de conversiekoersen vergelijken tussen twee verschillende dagen van de week, zoals alle zondag en alle donderdag. U kunt periodes van de dag ook vergelijken, zoals alle ochtenden tegenover alle avonden.

Analysis Workspace biedt vergelijkbare, kant-en-klare afmetingen die iets anders zijn opgemaakt dan deze plug-in. Zie [afmetingen voor tijdpartering](/help/analyze/analysis-workspace/components/dimensions/time-parting-dimensions.md) in de gebruikershandleiding Analyseren voor meer informatie. Sommige organisaties vinden dat de Analysis Workspace-afmetingen buiten de doos voldoende zijn.

>[!IMPORTANT]
>
>Versie 4.0+ van deze plug-in wijkt sterk af van eerdere versies. Adobe raadt u ten zeerste aan deze plug-in volledig te implementeren. Code die verwijst naar de insteekmodule vóór versie 4.0 is niet compatibel met de huidige versie van deze insteekmodule.

## Plug-in installeren met tags in Adobe Experience Platform

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar het tabblad [!UICONTROL Extensions] en klik op de knop [!UICONTROL Catalog]
1. De extensie [!UICONTROL Common Analytics Plugins] installeren en publiceren
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: Geen
   * Gebeurtenis: Kern - Bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: Gebruikelijke plug-ins voor Analytics
   * Type handeling: getTimeParting initialiseren
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met aangepaste code-editor

Als u de extensie van de plug-in niet wilt gebruiken, kunt u de aangepaste code-editor gebruiken.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder de uitbreiding van Adobe Analytics.
1. Breid [!UICONTROL Configure tracking using custom code] accordeon uit, die [!UICONTROL Open Editor] knoop openbaart.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

## Installeer de plug-in met AppMeasurement

Kopieer en plak de volgende code ergens in het AppMeasurement-bestand nadat het analytics tracking-object is geïnstantieerd (met [`s_gi`](../functions/s-gi.md)). Door opmerkingen en versienummers van de code in uw implementatie te behouden, kunt u Adobe doen met het oplossen van mogelijke problemen.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getTimeParting v6.3 (No Prerequisites Needed) */
function getTimeParting(t){var c=t;if("-v"===t)return{plugin:"getTimeParting",version:"6.3"};a:{if("undefined"!==typeof window.s_c_il){var a=0;for(var b;a<window.s_c_il.length;a++)if(b=window.s_c_il[a],b._c&&"s_c"===b._c){a=b;break a}}a=void 0}"undefined"!==typeof a&&(a.contextData.getTimeParting="6.3");c=document.documentMode?void 0:c||"Etc/GMT";a=(new Date).toLocaleDateString("en-US",{timeZone:c,minute:"numeric",hour:"numeric",weekday:"long",day:"numeric",year:"numeric",month:"long"});a=/([a-zA-Z]+).*?([a-zA-Z]+).*?([0-9]+).*?([0-9]+)(.*?)([0-9])(.*)/.exec(a);return"year="+a[4]+" | month="+a[2]+" | date="+a[3]+" | day="+a[1]+" | time="+(a[6]+a[7])};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De functie `getTimeParting` gebruikt het volgende argument:

**`t`** (Optioneel maar aanbevolen, tekenreeks): De naam van de tijdzone waarnaar de lokale tijd van de bezoeker moet worden omgezet.  Wordt standaard ingesteld op UTC/GMT-tijd. Zie [Lijst met tijdzones van de TZ-database](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones) op Wikipedia voor een volledige lijst met geldige waarden.

Veelvoorkomende geldige waarden zijn:

* `"America/New_York"` voor Oost Tijd
* `"America/Chicago"` voor Central Time
* `"America/Denver"` voor Mountain Time
* `"America/Los_Angeles"` voor Pacific Time

Als deze functie wordt aangeroepen, wordt een tekenreeks geretourneerd die het volgende door een pipe (`|`) gescheiden bevat:

* Het lopende jaar
* De huidige maand
* De dag van de maand
* De dag van de week
* De huidige tijd (AM/PM)

## Voorbeelden

```js
// Use the following code if the visitor resides in Paris, France
s.eVar8 = getTimeParting("Europe/Paris");

// Use the following code if the visitor resides in San Jose, California
s.eVar17 = getTimeParting("America/Los_Angeles");

// Use the following code if the visitor resides in Ghana.
// Note that Ghana is in GMT time, the default time zone that the plug-in uses with no argument
s.eVar22 = getTimeParting();

// Internet Explorer only returns the visitor's local time. Use this conditional statement to accommodate IE visitors
if(!document.documentMode) s.eVar39 = getTimeParting("America/New_York");
else s.eVarX = "Internet Explorer Visitors";

// Given a visitor from Denver Colorado visits a site on August 31, 2020 at 9:15 AM
// Returns the string value "year=2020 | month=August | date=31 | day=Friday | time=6:15 PM"
s.eVar10 = getTimeParting("Europe/Athens");

// Returns the string value "year=2020 | month=August | date=31 | day=Friday | time=6:15 AM"
s.eVar11 = getTimeParting("America/Nome");

// Returns the string value "year=2020 | month=August | date=31 | day=Friday | time=8:45 PM"
s.eVar12 = getTimeParting("Asia/Calcutta");

// Returns the string value "year=2020 | month=September | date=1 | day=Saturday | time=1:15 AM"
s.eVar13 = getTimeParting("Australia/Sydney");
```

## Versiehistorie

### 6.3 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 6.2 (5 november 2019)

* Kleine opgeloste problemen
* Verminderde algemene codegrootte

### 6.1 (26 november 2018)

* Oplossen voor Internet Explorer-browsers. Ze kunnen de tijd retourneren, maar alleen in de lokale tijd van de bezoeker.

### 6.0 (14 augustus 2018)

* Volledig herschrijven om aan internationale normen te voldoen. Hiermee converteert u nu zomertijd en alle tijdzones op de juiste wijze.

### 5.0 (17 april 2018)

* Point Release (opnieuw gecompileerd, kleinere codegrootte)
* De noodzaak voor de parameter `tpDST` is verwijderd, omdat de begin- en einddatum van de zomertijd nu automatisch worden gedetecteerd

>[!CAUTION]
>
>In eerdere versies van deze plug-in konden niet alle jaren in de toekomst worden opgenomen. Als u een vorige versie van deze plug-in gebruikt, raadt Adobe u ten zeerste aan om de upgrade naar de nieuwste versie uit te voeren om JavaScript-fouten en gegevensverlies te voorkomen. Als het bijwerken van deze plug-in niet mogelijk is, moet u ervoor zorgen dat de variabele `s._tpdst` in de plug-incode in de toekomst de juiste jaren bevat.

### 4.0 (22 augustus 2016)

* Verstrekt een gloednieuwe oplossing en omvat nu jaar, maand, en datuminformatie.
