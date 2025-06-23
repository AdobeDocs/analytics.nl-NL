---
title: getTimeParting
description: Meet het tijdstip waarop een specifieke actie plaatsvindt.
feature: Appmeasurement Implementation
exl-id: 3fab36c8-a006-405a-9ef1-2547c2b36b0d
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

---

# Adobe plug-in: getTimeParting

{{plug-in}}

Met de insteekmodule `getTimeParting` kunt u de details vastleggen van het tijdstip waarop een meetbare activiteit op uw site plaatsvindt. Deze insteekmodule is waardevol wanneer u metriek door om het even welke herhaalbare verdeling van tijd over een bepaalde datumwaaier wilt breken. U kunt bijvoorbeeld de conversiekoersen vergelijken tussen twee verschillende dagen van de week, zoals alle zondag en alle donderdag. U kunt periodes van de dag ook vergelijken, zoals alle ochtenden tegenover alle avonden.

Analysis Workspace biedt vergelijkbare, kant-en-klare afmetingen die iets anders zijn opgemaakt dan deze plug-in. Zie [ tijd het ontleden dimensies ](/help/analyze/analysis-workspace/components/dimensions/time-parting-dimensions.md) in de Analysegebruikersgids voor meer informatie. Sommige organisaties vinden dat de Analysis Workspace-afmetingen buiten de doos voldoende zijn.

>[!IMPORTANT]
>
>Versie 4.0+ van deze plug-in wijkt sterk af van eerdere versies. Adobe raadt u ten zeerste aan deze plug-in volledig te implementeren. Code die verwijst naar de insteekmodule vóór versie 4.0 is niet compatibel met de huidige versie van deze insteekmodule.

## De insteekmodule installeren met de extensie Web SDK

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken voor de webversie van SDK.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op **[!UICONTROL Tags]** aan de linkerkant en klik op de gewenste eigenschap Tag.
1. Klik op **[!UICONTROL Extensions]** aan de linkerkant en klik vervolgens op de tab **[!UICONTROL Catalog]**
1. Zoek en installeer de extensie **[!UICONTROL Common Web SDK Plugins]** .
1. Klik op **[!UICONTROL Data Elements]** aan de linkerkant en klik op het gewenste gegevenselement.
1. Stel de gewenste naam van het gegevenselement in met de volgende configuratie:
   * Extensie: algemene SDK-plug-ins voor het web
   * Gegevenselement: `getTimeParting`
1. Stel de parameter `Time Zone` rechts in.
1. Sla de wijzigingen in het gegevenselement op en publiceer deze.

## De insteekmodule handmatig installeren voor de Web SDK

Deze insteekmodule wordt nog niet ondersteund voor gebruik in een handmatige implementatie van de Web SDK.

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
   * Type handeling: getTimeParting initialiseren
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
/* Adobe Consulting Plugin: getTimeParting v6.3 (No Prerequisites Needed) */
function getTimeParting(t){var c=t;if("-v"===t)return{plugin:"getTimeParting",version:"6.3"};a:{if("undefined"!==typeof window.s_c_il){var a=0;for(var b;a<window.s_c_il.length;a++)if(b=window.s_c_il[a],b._c&&"s_c"===b._c){a=b;break a}}a=void 0}"undefined"!==typeof a&&(a.contextData.getTimeParting="6.3");c=document.documentMode?void 0:c||"Etc/GMT";a=(new Date).toLocaleDateString("en-US",{timeZone:c,minute:"numeric",hour:"numeric",weekday:"long",day:"numeric",year:"numeric",month:"long"});a=/([a-zA-Z]+).*?([a-zA-Z]+).*?([0-9]+).*?([0-9]+)(.*?)([0-9])(.*)/.exec(a);return"year="+a[4]+" | month="+a[2]+" | date="+a[3]+" | day="+a[1]+" | time="+(a[6]+a[7])};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De functie `getTimeParting` gebruikt het volgende argument:

**`t`** (Optioneel maar aanbevolen, tekenreeks): de naam van de tijdzone waarnaar de lokale tijd van de bezoeker moet worden omgezet.  Wordt standaard ingesteld op UTC/GMT. Zie [ Lijst van de streken van de gegevensbestandtijd van TZ ](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones) op Wikipedia voor een volledige lijst van geldige waarden.

Veelvoorkomende geldige waarden zijn:

* `"America/New_York"` for Eastern Time
* `"America/Chicago"` voor Central Time
* `"America/Denver"` voor Mountain Time
* `"America/Los_Angeles"` voor Pacific Time

Het roepen van deze functie keert een koord terug dat het volgende door een pijp (`|`) wordt afgebakend:

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

* Oplossen voor Internet Explorer-browsers. Ze kunnen de tijd teruggeven, maar alleen in de lokale tijd van de bezoeker.

### 6.0 (14 augustus 2018)

* Volledig herschrijven om aan internationale normen te voldoen. Hiermee converteert u nu zomertijd en alle tijdzones op de juiste wijze.

### 5.0 (17 april 2018)

* Point Release (opnieuw gecompileerd, kleinere codegrootte)
* De parameter `tpDST` is overbodig geworden omdat de begin- en einddatum van de zomertijd nu automatisch worden gedetecteerd

>[!CAUTION]
>
>In eerdere versies van deze plug-in konden niet alle jaren in de toekomst worden opgenomen. Als u een vorige versie van deze plug-in gebruikt, raadt Adobe u ten zeerste aan om de upgrade naar de nieuwste versie uit te voeren om JavaScript-fouten en gegevensverlies te voorkomen. Als het niet mogelijk is deze plug-in te upgraden, controleert u of de variabele `s._tpdst` in de plug-incode in de toekomst de juiste jaren bevat.

### 4.0 (22 augustus 2016)

* Verstrekt een gloednieuwe oplossing en omvat nu jaar, maand, en datuminformatie.
