---
title: apl (appendToList)
description: Voeg waarden toe aan variabelen die meerdere waarden ondersteunen.
feature: Variables
exl-id: 08ca43f4-f2cc-43fb-a8eb-7c9dd237dfba
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# Adobe-plug-in: apl (appendToList)

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

De `apl` kunt u veilig nieuwe waarden toevoegen aan door lijsten gescheiden variabelen, zoals [`events`](../page-vars/events/events-overview.md), [`linkTrackVars`](../config-vars/linktrackvars.md), [`list`](../page-vars/list.md)en andere.

* Als de waarde die u wilt toevoegen niet in de variabele bestaat, voegt de code de waarde aan het einde van de tekenreeks toe.
* Als de waarde die u wilt toevoegen al in de variabele bestaat, wijzigt deze plug-in de waarde niet. Hierdoor kan uw implementatie dubbele waarden voorkomen.
* Als de variabele die u wilt toevoegen leeg is, stelt de plug-in de variabele in op de nieuwe waarde.

Adobe raadt u aan deze plug-in te gebruiken als u nieuwe waarden wilt toevoegen aan bestaande variabelen die een reeks gescheiden waarden bevatten. Deze plug-in is niet nodig als u tekenreeksen wilt samenvoegen voor variabelen met gescheiden waarden.

## Plug-in installeren met tags in Adobe Experience Platform

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop [!UICONTROL Catalog] knop
1. Installeer en publiceer de [!UICONTROL Common Analytics Plugins] extension
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: Geen
   * Gebeurtenis: Kern - Bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: Gebruikelijke plug-ins voor Analytics
   * Type handeling: APL initialiseren (toevoegen aan lijst)
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met aangepaste code-editor

Als u de extensie van de plug-in niet wilt gebruiken, kunt u de aangepaste code-editor gebruiken.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop [!UICONTROL Configure] onder de extensie Adobe Analytics.
1. Breid uit [!UICONTROL Configure tracking using custom code] accordion, die de [!UICONTROL Open Editor] knop.
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

De `apl` function gebruikt de volgende argumenten:

* **`lv`** (vereist, tekenreeks): De variabele die een lijst met gescheiden items bevat waaraan een nieuwe waarde moet worden toegevoegd
* **`vta`** (vereist, tekenreeks): Een door komma&#39;s gescheiden lijst met de nieuwe waarden die aan de `lv` waarde van het argument.
* **`d1`** (optioneel, tekenreeks): Het scheidingsteken dat wordt gebruikt om de afzonderlijke waarden te scheiden die al in het dialoogvenster `lv` argument.  Heeft als standaardwaarde een komma (`,`) wanneer niet ingesteld.
* **`d2`** (optioneel, tekenreeks): Het uitvoerscheidingsteken. Heeft standaard dezelfde waarde als `d1` wanneer niet ingesteld.
* **`cc`** (optioneel, Booleaans): Een markering die aangeeft of een hoofdlettergevoelige controle wordt gebruikt. Indien `true`De duplicatiecontrole is hoofdlettergevoelig. Indien `false` of niet ingesteld, is de duplicatiecontrole niet hoofdlettergevoelig. Standaardwaarden: `false`.

De `apl` functie retourneert de waarde van de `lv` plus eventuele niet-gedupliceerde waarden in het dialoogvenster `vta` argument.

## Voorbeelden

```js
// Set the events variable to "event22,event24,event23".
s.events = "event22,event24";
s.events = apl(s.events,"event23");

// The events variable remains unchanged because the apl function does not add duplicate values
s.events = "event22,event23";
s.events = apl(s.events,"event23");

// Set the events variable to "event23" if the events variable is blank
s.events = "";
s.events = apl(s.events,"event23");

// Append a value to eVar5. The value of prop4 remains unchanged.
// The value of eVar5 is "hello|people|today".
s.prop4 = "hello|people";
s.eVar5 = apl(s.prop4, "today", "|");

// Sets prop4 to "hello|people,today". Be mindful of correct delimiters!
s.prop4 = "hello|people";
s.prop4 = apl(s.prop4, "today");

// Sets the events variable to "event22,event23,EVentT23". Be mindful of capitalization when using the cc argument!
s.events = "event22,event23";
s.events = apl(s.events,"EVenT23", ",", ",", true);

// Sets the events variable to "event22,event23,event24,event25".
s.events = "event22,event23";
s.events = apl(s.events, "event23,event24,event25");

// Sets linkTrackVars to "events,eVar1,campaign".
// The last three arguments at the end of this apl call are not necessary because they match the default argument values.
s.linkTrackVars = "events,eVar1";
s.linkTrackVars = apl(s.linkTrackVars, "campaign", ",", ",", false);

// This apl call does not do anything because the code does not assign the returned value to a variable.
s.events = "event22,event24";
apl(s.events, "event23");

// Sets the list2 variable to "apple-APPLE-Apple".
// Since the two delimiter arguments are different, the value passed in is delimited by "|", then joined together by "-".
s.list2 = "apple|APPLE";
s.list2 = apl(s.list2, "Apple", "|", "-", true);

// Sets the list3 variable to "value1,value1,value1" (unchanged).
// Only new values are deduplicated. Existing duplicate values remain.
s.list3 = "value1,value1,value1";
s.list3 = apl(s.list3,"value1");
```

## Versiehistorie

### 4.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 3.2 (25 september 2019)

* Compatibiliteitsproblemen met `apl` aanroepen die oudere versies van de plug-in gebruikten
* Verwijderde consolewaarschuwingen om grootte te verminderen
* Toegevoegd `inList 2.1`

### 3.1 (22 april 2018)

* `d2` argument wordt nu standaard ingesteld op de waarde van de `d1` argument indien niet ingesteld

### 3.0 (16 april 2018)

* Volledige heranalyse/herschrijven van plug-in
* Geavanceerde foutcontrole toegevoegd
* De `vta` argument accepteert nu meerdere waarden tegelijk
* De `d2` argument om de geretourneerde waarde op te maken
* De `cc` argument naar een Booleaanse waarde

### 2.5 (18 februari 2016)

* Gebruikt nu de `inList` functie voor vergelijkingsverwerking

### 2.0 (26 januari 2016)

* `d` (Scheidingsteken) argument nu optioneel (wordt standaard een komma)
* `u` (Markering voor hoofdlettergevoeligheid) argument is nu optioneel (wordt standaard ingesteld op hoofdlettergevoelig)
* Ongeacht de `u` (Markering voor hoofdlettergevoeligheid) voegt de plug-in geen waarde meer toe aan een lijst als de waarde al in de lijst voorkomt
