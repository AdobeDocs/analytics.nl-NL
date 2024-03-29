---
title: getTimeParting
description: Meet het tijdstip waarop een specifieke actie plaatsvindt.
feature: Variables
exl-id: 3fab36c8-a006-405a-9ef1-2547c2b36b0d
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

---

# Adobe plug-in: getTimeParting

{{plug-in}}

De `getTimeParting` kunt u de details vastleggen van het tijdstip waarop een meetbare activiteit op uw site plaatsvindt. Deze insteekmodule is waardevol wanneer u metriek door om het even welke herhaalbare verdeling van tijd over een bepaalde datumwaaier wilt breken. U kunt bijvoorbeeld de conversiekoersen vergelijken tussen twee verschillende dagen van de week, zoals alle zondag en alle donderdag. U kunt periodes van de dag ook vergelijken, zoals alle ochtenden tegenover alle avonden.

Analysis Workspace biedt vergelijkbare, kant-en-klare afmetingen die iets anders zijn opgemaakt dan deze plug-in. Zie [time-paring, afmetingen](/help/analyze/analysis-workspace/components/dimensions/time-parting-dimensions.md) in de gebruikershandleiding Analyseren voor meer informatie. Sommige organisaties vinden dat de Analysis Workspace-afmetingen buiten de doos voldoende zijn.

>[!IMPORTANT]
>
>Versie 4.0+ van deze plug-in wijkt sterk af van eerdere versies. Adobe raadt u ten zeerste aan deze insteekmodule helemaal vanaf het begin te implementeren. Code die verwijst naar de insteekmodule vóór versie 4.0 is niet compatibel met de huidige versie van deze insteekmodule.

## De plug-in installeren met de extensie Web SDK

De Adobe biedt een uitbreiding aan die u toestaat om het meest algemeen gebruikte stop-ins met het Web SDK te gebruiken.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klikken **[!UICONTROL Tags]** klikt u links op de gewenste eigenschap tag.
1. Klikken **[!UICONTROL Extensions]** klikt u links op de knop **[!UICONTROL Catalog]** tab
1. Zoek en installeer de **[!UICONTROL Common Web SDK Plugins]** extensie.
1. Klikken **[!UICONTROL Data Elements]** klikt u links op het gewenste gegevenselement.
1. Stel de gewenste naam van het gegevenselement in met de volgende configuratie:
   * Extension: Common Web SDK-plug-ins
   * Gegevenselement: `getTimeParting`
1. Stel de `Time Zone` parameter aan de rechterkant.
1. Sla de wijzigingen in het gegevenselement op en publiceer deze.

## De plug-in handmatig installeren met de implementatie van de Web SDK

Deze insteekmodule wordt nog niet ondersteund voor gebruik in een handmatige implementatie van de Web SDK.

## De insteekmodule installeren met de Adobe Analytics-extensie

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken met Adobe Analytics.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop [!UICONTROL Catalog] knop
1. Installeer de [!UICONTROL Common Analytics Plugins] extension
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: geen
   * Event: Core - bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: veelgebruikte plug-ins voor Analytics
   * Type handeling: getTimeParting initialiseren
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met aangepaste code-editor

Als u niet de Gemeenschappelijke Insteekmodule van Analytics wilt gebruiken, kunt u de redacteur van de douanecode gebruiken.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder de extensie Adobe Analytics.
1. Breid uit [!UICONTROL Configure tracking using custom code] accordion, die de [!UICONTROL Open Editor] knop.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

## Plug-in installeren met AppMeasurement

Kopieer en plak de volgende code ergens in het bestand AppMeasurement nadat het object Analytics tracking is geïnstantieerd (met [`s_gi`](../functions/s-gi.md)). Door opmerkingen en versienummers van de code in uw implementatie te behouden, kunt u Adoben met het oplossen van mogelijke problemen.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getTimeParting v6.3 (No Prerequisites Needed) */
function getTimeParting(t){var c=t;if("-v"===t)return{plugin:"getTimeParting",version:"6.3"};a:{if("undefined"!==typeof window.s_c_il){var a=0;for(var b;a<window.s_c_il.length;a++)if(b=window.s_c_il[a],b._c&&"s_c"===b._c){a=b;break a}}a=void 0}"undefined"!==typeof a&&(a.contextData.getTimeParting="6.3");c=document.documentMode?void 0:c||"Etc/GMT";a=(new Date).toLocaleDateString("en-US",{timeZone:c,minute:"numeric",hour:"numeric",weekday:"long",day:"numeric",year:"numeric",month:"long"});a=/([a-zA-Z]+).*?([a-zA-Z]+).*?([0-9]+).*?([0-9]+)(.*?)([0-9])(.*)/.exec(a);return"year="+a[4]+" | month="+a[2]+" | date="+a[3]+" | day="+a[1]+" | time="+(a[6]+a[7])};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `getTimeParting` function gebruikt het volgende argument:

**`t`** (Optioneel, maar aanbevolen, tekenreeks): de naam van de tijdzone waarnaar de lokale tijd van de bezoeker moet worden omgezet.  Wordt standaard ingesteld op UTC/GMT. Zie [Lijst met tijdzones van TZ-databases](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones) op Wikipedia voor een volledige lijst van geldige waarden.

Veelvoorkomende geldige waarden zijn:

* `"America/New_York"` voor Oost-Tijd
* `"America/Chicago"` voor Central Time
* `"America/Denver"` voor Mountain Time
* `"America/Los_Angeles"` voor Pacific Time

Wanneer deze functie wordt aangeroepen, wordt een tekenreeks geretourneerd die het volgende bevat dat door een pipe wordt gescheiden (`|`):

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
* De noodzaak van de `tpDST` parameter, omdat start/end-datums van zomertijd nu automatisch worden gedetecteerd

>[!CAUTION]
>
>In eerdere versies van deze plug-in konden niet alle jaren in de toekomst worden opgenomen. Als u een vorige versie van deze plug-in gebruikt, wordt u door Adobe ten zeerste aangeraden de nieuwste versie te gebruiken om JavaScript-fouten en gegevensverlies te voorkomen. Als het bijwerken van deze plug-in niet mogelijk is, controleert u of de `s._tpdst` bevat in de plug-incode de desbetreffende jaren in de toekomst.

### 4.0 (22 augustus 2016)

* Verstrekt een gloednieuwe oplossing en omvat nu jaar, maand, en datuminformatie.
