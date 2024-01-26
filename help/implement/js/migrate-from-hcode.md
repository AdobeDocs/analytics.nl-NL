---
title: Migreren naar AppMeasurement voor JavaScript
description: Bepaal wat nodig is om uw implementatie van H Code te migreren.
feature: Implementation Basics
exl-id: ed606ab4-bd7d-4871-baa1-77e30fdd419e
role: Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---

# Migreren naar AppMeasurement voor JavaScript

Als uw implementatie nog steeds H-code gebruikt, wordt Adobe sterk aangeraden te migreren naar de nieuwste versie van het AppMeasurement. Analyses implementeren via [tags in Adobe Experience Platform](../launch/overview.md) wordt aangeraden, maar een bijgewerkte JavaScript-implementatie kan worden gebruikt.

De volgende opmerkelijke veranderingen zijn aanwezig in AppMeasurement wanneer vergeleken met de Code van H:

* 3-7 keer sneller dan H-code.
* Lichter dan H-code - 21kB niet gecomprimeerd versus H-code, die 33kB ongecomprimeerd is.
* De bibliotheek en paginacode kunnen binnen worden opgesteld `<head>` -tag.
* Bestaande H-code op paginaniveau is compatibel met AppMeasurement.
* De bibliotheek biedt native hulpprogramma&#39;s voor het ophalen van queryparameters, het lezen en schrijven van cookies en het uitvoeren van geavanceerde koppelingen.
* De bibliotheek ondersteunt geen dynamische accountconfiguratievariabelen (waaronder `dynamicAccountSelection`, `dynamicAccountMatch`, en `dynamicAccountList`).

In de volgende stappen wordt een typische migratieworkflow beschreven.

1. **Het nieuwe AppMeasurement-bestand downloaden**: Open het nieuwe bestand door u aan te melden bij Adobe Analytics en navigeer vervolgens naar Beheer > Alle beheerders > Codebeheer. Het gedownloade gecomprimeerde bestand bevat een miniatuur `AppMeasurement.js` samen met de modules Media en Integrate.
1. **Kopieer uw `s_code.js` aanpassingen aan`AppMeasurement.js`**: Verplaats alle code voor de `DO NOT ALTER ANYTHING BELOW THIS LINE` sectie in `s_code.js` tot het begin van `AppMeasurement.js`.
1. **Alle plug-ins bijwerken**: Gebruik de nieuwste versie van elke plug-in die in uw `s_code.js` bestand. Deze stap omvat de modules Media en Integrate.
1. **Het bestand AppMeasurement.js implementeren**: Upload uw `AppMeasurement.js` bestand naar uw webserver.
1. **Scriptverwijzingen bijwerken naar punt`AppMeasurement.js`**: zorg ervoor dat alle paginaverwijzingen `AppMeasurement.js` in plaats van `s_code.js`.

## Voorbeeld van toepassingscode

Een standaard `AppMeasurement.js` bestand. Zorg ervoor dat de configuratievariabelen boven de `doPlugins` functie.

```js
// Initialize AppMeasurement
var s = s_gi("examplersid");

/******** VISITOR ID SERVICE CONFIG - REQUIRES VisitorAPI.js ********/;
s.visitor=Visitor.getInstance("INSERT-MCORG-ID-HERE");

/************************** CONFIG SECTION **************************/;
/* You may add or alter any code config here. */
s.trackDownloadLinks = true;
s.trackExternalLinks = true;
s.trackInlineStats = true;
s.linkDownloadFileTypes = "exe,zip,wav,mp3,mov,mpg,avi,wmv,pdf,doc,docx,xls,xlsx,ppt,pptx";
s.linkInternalFilters = "javascript:,example.com";

s.usePlugins = true;
function s_doPlugins(s) {

// Use implementation plug-ins that are defined below in this section

}
s.doPlugins = s_doPlugins;

/* WARNING: Changing any of the below variables will cause drastic
changes to how your visitor data is collected.  Changes should only be
made when instructed to do so by your Adobe Account Team.*/
s.trackingServer="example.data.adobedc.net";

/************************** PLUGINS SECTION *************************/

// Copy and paste implementation plug-ins here. Plug-ins can then be used in the s_doPlugins(s) function above

/****************************** MODULES *****************************/

// Copy and paste implementation modules (Media, Integrate) here.

/* ============== DO NOT ALTER ANYTHING BELOW THIS LINE ! ===============  */
```

## Voorbeeld van paginacode

Typische code die op elke pagina wordt geladen.

```html
<script src="AppMeasurement.js"></script>
<script language="JavaScript" type="text/javascript">
s.pageName = "Example page name";
s.eVar1 = "Example eVar value";
s.events = "event1";
s.t();
</script>
```

Zorg ervoor dat u ook een verwijzing naar `AppMeasurement.js` en `VisitorAPI.js` op elke pagina. Zie [JavaScript-implementatie](/help/implement/js/overview.md) voor meer informatie .
