---
title: apl (appendToList)
description: Voeg waarden toe aan variabelen die meerdere waarden ondersteunen.
feature: Appmeasurement Implementation
exl-id: 08ca43f4-f2cc-43fb-a8eb-7c9dd237dfba
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 0%

---

# Adobe-insteekmodule: apl (appendToList)

{{plug-in}}

Met de plug-in `apl` kunt u veilig nieuwe waarden toevoegen aan door lijsten gescheiden variabelen, zoals [`events`](../page-vars/events/events-overview.md) , [`linkTrackVars`](../config-vars/linktrackvars.md) , [`list`](../page-vars/list.md) en andere.

* Als de waarde die u wilt toevoegen niet in de variabele bestaat, voegt de code de waarde aan het einde van de tekenreeks toe.
* Als de waarde die u wilt toevoegen al in de variabele bestaat, wijzigt deze plug-in de waarde niet. Hierdoor kan uw implementatie dubbele waarden voorkomen.
* Als de variabele die u wilt toevoegen leeg is, stelt de plug-in de variabele in op de nieuwe waarde.

Adobe raadt u aan deze plug-in te gebruiken als u nieuwe waarden wilt toevoegen aan bestaande variabelen die een reeks gescheiden waarden bevatten. Deze plug-in is niet nodig als u tekenreeksen wilt samenvoegen voor variabelen met gescheiden waarden.

## De insteekmodule installeren met de extensie Web SDK of Web SDK

Deze insteekmodule wordt nog niet ondersteund voor gebruik in de Web SDK.

## De insteekmodule installeren met de Adobe Analytics-extensie

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken in Adobe Analytics.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop [!UICONTROL Catalog]
1. De extensie [!UICONTROL Common Analytics Plugins] installeren en publiceren
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: geen
   * Event: Core - bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: veelgebruikte plug-ins voor Analytics
   * Type handeling: APL initialiseren (toevoegen aan lijst)
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met aangepaste code-editor

Als u niet de Gemeenschappelijke Insteekmodule van Analytics wilt gebruiken, kunt u de redacteur van de douanecode gebruiken.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste eigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder de extensie Adobe Analytics.
1. Vouw de accordeon [!UICONTROL Configure tracking using custom code] uit, zodat de knop [!UICONTROL Open Editor] zichtbaar wordt.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

## Plug-in installeren met AppMeasurement

Kopieer en plak de volgende code ergens in het AppMeasurement-bestand nadat het object Analytics tracking is geïnstantieerd (met [`s_gi`](../functions/s-gi.md) ). Door opmerkingen en versienummers van de code in uw implementatie te behouden, helpt Adobe bij het oplossen van mogelijke problemen.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: apl (appendToList) v4.0 */
function apl(lv,va,d1,d2,cc){var b=lv,d=va,e=d1,c=d2,g=cc;if("-v"===b)return{plugin:"apl",version:"4.0"};var h=function(){if("undefined"!==typeof window.s_c_il)for(var k=0,b;k<window.s_c_il.length;k++)if(b=window.s_c_il[k],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof h&&(h.contextData.apl="4.0");window.inList=window.inList||function(b,d,c,e){if("string"!==typeof d)return!1;if("string"===typeof b)b=b.split(c||",");else if("object"!==typeof b)return!1;c=0;for(a=b.length;c<a;c++)if(1==e&&d===b[c]||d.toLowerCase()===b[c].toLowerCase())return!0;return!1};if(!b||"string"===typeof b){if("string"!==typeof d||""===d)return b;e=e||",";c=c||e;1==c&&(c=e,g||(g=1));2==c&&1!=g&&(c=e);d=d.split(",");h=d.length;for(var f=0;f<h;f++)window.inList(b,d[f],e,g)||(b=b?b+c+d[f]:d[f])}return b};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De functie `apl` gebruikt de volgende argumenten:

* **`lv`** (required, string): De variabele die een gescheiden lijst met items bevat waaraan een nieuwe waarde moet worden toegevoegd
* **`vta`** (required, string): Een door komma&#39;s gescheiden lijst van de nieuwe waarde(n) die aan de waarde van het argument `lv` moet worden toegevoegd.
* **`d1`** (optioneel, tekenreeks): het scheidingsteken dat wordt gebruikt om de afzonderlijke waarden te scheiden die al in het argument `lv` staan.  Heeft als standaardwaarde een komma (`,`).
* **`d2`** (optioneel, tekenreeks): het uitvoerscheidingsteken. Heeft als standaardwaarde dezelfde waarde als `d1` als dit niet is ingesteld.
* **`cc`** (optioneel, Boolean): een markering die aangeeft of een hoofdlettergevoelige controle wordt gebruikt. Als `true` , is de duplicatiecontrole hoofdlettergevoelig. Indien `false` of niet ingesteld, is de duplicatiecontrole niet hoofdlettergevoelig. Wordt standaard ingesteld op `false` .

De functie `apl` retourneert de waarde van het argument `lv` plus eventuele niet-gedupliceerde waarden in het argument `vta` .

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

* Compatibiliteitsproblemen verholpen met aanroepen van `apl` naar oudere versies van de plug-in.
* Verwijderde consolewaarschuwingen om grootte te verminderen
* Toegevoegd `inList 2.1`

### 3.1 (22 april 2018)

* Het argument `d2` wordt nu standaard ingesteld op de waarde van het argument `d1` als dit niet is ingesteld

### 3.0 (16 april 2018)

* Volledige heranalyse/herschrijven van plug-in
* Geavanceerde foutcontrole toegevoegd
* Het argument `vta` accepteert nu meerdere waarden tegelijk
* Het argument `d2` toegevoegd om de geretourneerde waarde op te maken
* Het argument `cc` is gewijzigd in een Booleaanse waarde

### 2.5 (18 februari 2016)

* De functie `inList` wordt nu gebruikt voor vergelijkingsverwerking

### 2.0 (26 januari 2016)

* Het argument `d` (Scheidingsteken) is nu optioneel (de standaardwaarde is een komma)
* `u` (markering Hoofdlettergevoeligheid) argument nu optioneel (wordt standaard niet-hoofdlettergevoelig)
* Ongeacht het argument `u` (hoofdlettergevoeligheid) voegt de plug-in geen waarde meer toe aan een lijst als de waarde al in de lijst bestaat
