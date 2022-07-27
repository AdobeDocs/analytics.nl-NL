---
title: getPageName
description: Maak een eenvoudig te lezen pageName van het huidige websitepad.
feature: Variables
exl-id: a3aaeb5d-65cd-45c1-88bb-f3c0efaff110
source-git-commit: 7c7a7d8add9edb1538df12b440bc0a15f09efe5e
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---

# Adobe-plug-in: getPageName

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

De `getPageName` Met deze insteekmodule maakt u een leesvriendelijke, opgemaakte versie van de huidige URL. Adobe raadt u aan deze plug-in te gebruiken als u een [`pageName`](../page-vars/pagename.md) waarde die eenvoudig kan worden ingesteld en begrepen in de rapportage. Deze plug-in is niet nodig als u al een naamgevingsstructuur hebt voor de `pageName` variabele, zoals door een gegevenslaag. Het wordt het best gebruikt wanneer u geen andere oplossing hebt om te plaatsen `pageName` variabele.

<!--## Install the plug-in using the Web SDK or the Adobe Analytics extension

Adobe offers an extension that allows you to use most commonly-used plug-ins.

1. Log in to [Adobe Experience Platform Data Collection](https://experience.adobe.com/data-collection) using your AdobeID credentials.
1. Click the desired tag property.
1. Go to the [!UICONTROL Extensions] tab, then click on the [!UICONTROL Catalog] button
1. Install and publish the [!UICONTROL Common Analytics Plugins] extension
1. If you haven't already, create a rule labeled "Initialize Plug-ins" with the following configuration:
    * Condition: None
    * Event: Core – Library Loaded (Page Top)
1. Add an action to the above rule with the following configuration:
    * Extension: Common Analytics Plugins
    * Action Type: Initialize getPageName
1. Save and publish the changes to the rule.-->

## Plug-in installeren met aangepaste code-editor

Als u de extensie van de plug-in niet wilt gebruiken, kunt u de aangepaste code-editor gebruiken.

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
/* Adobe Consulting Plugin: getPageName v4.2 */
var getPageName=function(si,qv,hv,de){var a=si,b=qv,f=hv,e=de;if("-v"===a)return{plugin:"getPageName",version:"4.2"};a:{if("undefined"!==typeof window.s_c_il){var d=0;for(var g;d<window.s_c_il.length;d++)if(g=window.s_c_il[d],g._c&&"s_c"===g._c){d=g;break a}}d=void 0}"undefined"!==typeof d&&(d.contextData.getPageName="4.2");var c=location.hostname,h=location.pathname.substring(1).split("/"),l=h.length,k=location.search.substring(1).split("&"),m=k.length;d=location.hash.substring(1).split("&");g=d.length;e=e?e:"|";a=a?a:c;b=b?b:"";f=f?f:"";if(1===l&&""===h[0])a=a+e+"home";else for(c=0;c<l;c++)a=a+e+decodeURIComponent(h[c]);if(b&&(1!==m||""!==k[0]))for(h=b.split(","),l=h.length,c=0;c<l;c++)for(b=0;b<m;b++)if(h[c]===k[b].split("=")[0]){a=a+e+decodeURIComponent(k[b]);break}if(f&&(1!==g||""!==d[0]))for(f=f.split(","),k=f.length,c=0;c<k;c++)for(b=0;b<g;b++)if(f[c]===d[b].split("=")[0]){a=a+e+decodeURIComponent(d[b]);break}return a.substring(a.length-e.length)===e?a.substring(0,a.length-e.length):a};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `getPageName` function gebruikt de volgende argumenten:

* **`si`** (optioneel, tekenreeks): Een id die wordt ingevoegd aan het begin van de tekenreeks die de id van de site vertegenwoordigt. Deze waarde kan een numerieke id of een vriendelijke naam zijn. Wanneer deze niet is ingesteld, wordt standaard het huidige domein gebruikt.
* **`qv`** (optioneel, tekenreeks): Een door komma&#39;s gescheiden lijst met parameters van queryreeksen die, indien gevonden in de URL, worden toegevoegd aan de tekenreeks
* **`hv`** (optioneel, tekenreeks): Een door komma&#39;s gescheiden lijst met parameters gevonden in de URL-hash die, indien gevonden in de URL, aan de tekenreeks wordt toegevoegd
* **`de`** (optioneel, tekenreeks): Het scheidingsteken voor het opsplitsen van afzonderlijke delen van de tekenreeks. Heeft als standaardwaarde een pijp (`|`).

De functie retourneert een tekenreeks met een gebruiksvriendelijke versie van de URL. Deze tekenreeks wordt doorgaans toegewezen aan de `pageName` variabele, maar kan ook in andere variabelen worden gebruikt.

## Voorbeelden

```js
// Given the URL https://mail.example.com/mail/u/0/#inbox, sets the page variable to "mail.example.com|mail|u|0".
s.pageName = getPageName();

// Given the URL https://mail.example.com/mail/u/0/#inbox, sets the page variable to "example|mail|u|0".
s.pageName = getPageName("example");

// Given the URL https://www.example.com/, sets the page variable to "www.example.com|home".
// When the code runs on a URL that does not contain a path, it always adds the value of "home" to the end of the return value.
s.pageName = getPageName();

// Given the URL https://www.example.com/, sets the page variable to "example|home".
s.pageName = getPageName("example","","","|");

// Given the URL https://www.example.com/en/booking/room-booking.html?cid=1235#/step2&arrive=05-26&depart=05-27&numGuests=2
// Sets the page variable to "www.example.com|en|booking|room-booking.html".
s.pageName = getPageName();

// Given the URL https://www.example.com/en/booking/room-booking.html?cid=1235#/step2&arrive=05-26&depart=05-27&numGuests=2
// Sets the page variable to "example: en: booking: room-booking.html: cid=1235: arrive=05-26: numGuests=2"
s.pageName = getPageName("example","cid","arrive,numGuests",": ");
```

## Upgrade uitvoeren vanaf vorige versies

Versie 4.0+ van de `getPageName` De insteekmodule is niet afhankelijk van het bestaan van het object AppMeasurement van Adobe Analytics (dat wil zeggen de `s` object). Als u een upgrade uitvoert naar deze versie, wijzigt u de code waarmee de plug-in wordt aangeroepen door instanties van de `s` object van de aanroep. Bijvoorbeeld, wijzigen `s.getPageName();` tot `getPageName();`.

## Versiehistorie

### 4.2 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 4.1 (17 september 2019)

* Standaardwaarde voor scheidingstekens is gewijzigd in een pĳpteken (van een dubbele punt + spatie).

### 4.0 (22 mei 2018)

* Volledige heranalyse/herschrijven van plug-in
