---
title: getGeoCoordinates
description: De geoLocation van een bezoeker volgen.
feature: Variables
exl-id: 8620d083-7fa6-432b-891c-e24907e7c466
source-git-commit: bbb138d979968ec2536e53ff07001b43156df095
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 0%

---

# Adobe-plug-in: getGeoCoordinates

{{plug-in}}

De `getGeoCoordinates` kunt u de breedte en lengte van bezoekersapparaten vastleggen. Adobe raadt u aan deze plug-in te gebruiken als u geo-locatiegegevens wilt vastleggen in variabelen van Analytics.

## De plug-in installeren met de extensie Web SDK

Adobe biedt een uitbreiding aan die u toestaat om het meest algemeen gebruikte stop-ins met het Web SDK te gebruiken.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klikken **[!UICONTROL Tags]** klikt u links op de gewenste eigenschap tag.
1. Klikken **[!UICONTROL Extensions]** klikt u links op de knop **[!UICONTROL Catalog]** tab
1. Zoek en installeer de **[!UICONTROL Common Web SDK Plugins]** extensie.
1. Klikken **[!UICONTROL Data Elements]** klikt u links op het gewenste gegevenselement.
1. Stel de gewenste naam van het gegevenselement in met de volgende configuratie:
   * Extensie: Algemene insteekmodules voor Web SDK
   * Gegevenselement: `getGeoCoordinates`
1. Sla de wijzigingen in het gegevenselement op en publiceer deze.

## De plug-in handmatig installeren met de implementatie van de Web SDK

Deze insteekmodule wordt nog niet ondersteund voor gebruik in een handmatige implementatie van de Web SDK.

## De insteekmodule installeren met de Adobe Analytics-extensie

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken in Adobe Analytics.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop [!UICONTROL Catalog] knop
1. Installeer en publiceer de [!UICONTROL Common Analytics Plugins] extension
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: Geen
   * Gebeurtenis: Kern - Bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: Gebruikelijke plug-ins voor Analytics
   * Type handeling: getGeoCoordinates initialiseren
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met aangepaste code-editor

Als u niet de Gemeenschappelijke Insteekmodule van Analytics wilt gebruiken, kunt u de redacteur van de douanecode gebruiken.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder de extensie Adobe Analytics.
1. Breid uit [!UICONTROL Configure tracking using custom code] accordion, die de [!UICONTROL Open Editor] knop.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

## Installeer de plug-in met AppMeasurement

Kopieer en plak de volgende code ergens in het AppMeasurement-bestand nadat het analytics tracking-object is geïnstantieerd (met [`s_gi`](../functions/s-gi.md)). Door opmerkingen en versienummers van de code in uw implementatie te behouden, kunt u Adobe doen met het oplossen van mogelijke problemen.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getGeoCoordinates v2.0  */
function getGeoCoordinates(){if(arguments&&"-v"===arguments[0])return{plugin:"getGeoCoordinates",version:"2.0"};var b=function(){if("undefined"!==typeof window.s_c_il)for(var a=0,c;a<window.s_c_il.length;a++)if(c=window.s_c_il[a],c._c&&"s_c"===c._c)return c}();"undefined"!==typeof b&&(b.contextData.getGeoCoordinates="2.0");window.cookieWrite=window.cookieWrite||function(a,c,f){if("string"===typeof a){var h=window.location.hostname,b=window.location.hostname.split(".").length-1;if(h&&!/^[0-9.]+$/.test(h)){b=2<b?b:2;var e=h.lastIndexOf(".");if(0<=e){for(;0<=e&&1<b;)e=h.lastIndexOf(".",e-1),b--;e=0<e?h.substring(e):h}}g=e;c="undefined"!==typeof c?""+c:"";if(f||""===c)if(""===c&&(f=-60),"number"===typeof f){var d=new Date;d.setTime(d.getTime()+6E4*f)}else d=f;return a&&(document.cookie=encodeURIComponent(a)+"="+encodeURIComponent(c)+"; path=/;"+(f?" expires="+d.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof cookieRead)?cookieRead(a)===c:!1}};window.cookieRead=window.cookieRead||function(a){if("string"===typeof a)a=encodeURIComponent(a);else return"";var c=" "+document.cookie,b=c.indexOf(" "+a+"="),d=0>b?b:c.indexOf(";",b);return(a=0>b?"":decodeURIComponent(c.substring(b+2+a.length,0>d?c.length:d)))?a:""};var d="";b=cookieRead("s_ggc").split("|");var k={timeout:5E3,maximumAge:0},l=function(a){a=a.coords;cookieWrite("s_ggc",parseFloat(a.latitude.toFixed(4))+"|"+parseFloat(a.longitude.toFixed(4)),30);d="latitude="+parseFloat(a.latitude.toFixed(4))+" | longitude="+parseFloat(a.longitude.toFixed(4))},m=function(a){d="error retrieving geo coordinates"};1<b.length&&(d="latitude="+b[0]+" | longitude="+b[1]);navigator.geolocation&&navigator.geolocation.getCurrentPosition(l,m,k);""===d&&(d="geo coordinates not available");return d};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `getGeoCoordinates` gebruiken geen argumenten. Deze geeft een van de volgende waarden:

* `"geo coordinates not available"`: Voor apparaten waarvoor geen gegevens over de geolocatie beschikbaar zijn op het moment dat de plug-in wordt uitgevoerd. Deze waarde komt vaak voor bij de eerste treffer van het bezoek, vooral wanneer bezoekers eerst toestemming moeten geven om hun locatie te volgen.
* `"error retrieving geo coordinates"`: Wanneer de plug-in fouten aantreft bij het ophalen van de locatie van het apparaat
* `"latitude=[LATITUDE] | longtitude=[LONGITUDE]"`: Wanneer [LATITUDE]/[LONGITUDE] zijn respectievelijk de lengte- en breedtegraad

>[!NOTE]
>
>Coördinaatwaarden worden afgerond tot op het dichtstbijzijnde vierde decimaal. De waarde van bijvoorbeeld `"40.438635333"` is afgerond naar `"40.4386"` om het aantal unieke waarden te beperken dat moet worden vastgelegd. De waarden zijn dicht genoeg om de exacte locatie van het apparaat binnen ongeveer 10 meter te bepalen.

Deze plug-in gebruikt een cookie met de naam `"s_ggc"` om coördinaten tussen treffers op te slaan indien nodig.

## Voorbeelden

```js
// Sets eVar1 to one of the above return values depending on the visitor's device status.
s.eVar1 = getGeoCoordinates();

// Extracts latitude and longitude into their own variables called finalLatitude and finalLongitude for use in other code/applications.
var coordinates = getGeoCoordinates();
if(coordinates.indexOf("latitude") > -1)
{
  var finalLatitude = Number(coordinates.split("|")[0].trim().split("=")[1]),
  finalLongitude = Number(coordinates.split("|")[1].trim().split("=")[1]);
}

// From there, you can determine whether a visitor is at, for example, the Statue of Liberty:
if(finalLatitude >= 40.6891 && finalLatitude <= 40.6893 && finalLongitude >= -74.0446 && finalLongitude <= -74.0444)
{
  var visitorAtStatueOfLiberty = true;
}
else
{
  var visitorAtStatueOfLiberty = false;
}
```

## Versiehistorie

### 2.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 1.0 (25 mei 2015)

* Eerste release.
