---
title: getResponsiveLayout
description: Bepaal welke lay-out van een website momenteel wordt weergegeven.
feature: Variables
exl-id: 5b192d02-fc3c-4b82-acb4-42902202ab5f
source-git-commit: 7c7a7d8add9edb1538df12b440bc0a15f09efe5e
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Adobe-plug-in: getResponsiveLayout

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

De `getResponsiveLayout` Met de insteekmodule kunt u bijhouden naar welke versie van uw responsieve, op ontwerpen gebaseerde website een bezoeker momenteel kijkt. Adobe raadt u aan deze plug-in te gebruiken als uw site gebruikmaakt van een responsief ontwerp en u de versie van de site wilt bijhouden die door een bezoeker wordt weergegeven. Deze insteekmodule is niet nodig als uw site geen responsief ontwerp gebruikt.

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
    * Action Type: Initialize getResponsiveLayout
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
/* Adobe Consulting Plugin: getResponsiveLayout v1.1 (Requires AppMeasurement) */
var getResponsiveLayout=function(ppw,plw,tw){var c=ppw,b=plw,e=tw;if("-v"===c)return{plugin:"getResponsiveLayout",version:"1.1"};a:{if("undefined"!==typeof window.s_c_il){var a=0;for(var d;a<window.s_c_il.length;a++)if(d=window.s_c_il[a],d._c&&"s_c"===d._c){a=d;break a}}a=void 0}"undefined"!==typeof a&&(a.contextData.getResponsiveLayout="1.1");if(!(isNaN(c)||isNaN(b)||isNaN(e)||b<c||e<b))return a=window.innerWidth||document.documentElement.clientWidth||document.body.clientWidth,(c<b&&a<=b?a<=c?"phone portrait layout":"phone landscape layout":a<=b?"phone layout":a<=e?"tablet layout":"desktop layout")+":"+a+"x"+(window.innerHeight||document.documentElement.clientHeight||document.body.clientHeight)};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `getResponsiveLayout` function gebruikt de volgende argumenten:

* **`ppw`** (vereist, geheel getal): De maximumbreedte van pixels die een browservenster kan hebben voordat de pagina overschakelt van de staande lay-out Telefoon naar een liggende lay-out voor de telefoon
* **`plw`** (vereist, geheel getal): De maximale breedte van pixels die een browservenster kan hebben voordat de pagina overschakelt van een liggende lay-out voor de telefoon naar een lay-out op basis van tablets
* **`tw`** (vereist, geheel getal): De maximale breedte van pixels die een browservenster kan hebben voordat de pagina overschakelt van een tabletlay-out naar een op het bureaublad gebaseerde lay-out

Als deze functie wordt aangeroepen, wordt een tekenreeks geretourneerd met twee delen die zijn gescheiden door een dubbele punt (`:`). Het eerste deel van de tekenreeks bevat een van de volgende waarden, afhankelijk van de breedte van de browser en de bovenstaande argumenten:

* `"phone portrait layout"`
* `"phone landscape layout"`
* `"phone layout"` (voor sites die niet zowel een staande als een liggende lay-out hebben)
* `"tablet layout"`
* `"desktop layout"`

Het tweede deel van de geretourneerde tekenreeks is de breedte en hoogte van de browser. Bijvoorbeeld, `"desktop layout:1243x700"`.

## Voorbeelden

```js
// A visitor accesses your site on their laptop. The browser window is maximized.
// * Your site switches from phone portrait mode to phone landscape mode when the browser width is greater than 500 pixels
// * Your site switches from phone landscape mode to tablet mode when the browser width is greater than 700 pixels
// * Your site switches from tablet mode to desktop mode when the browser width is greater than 1000 pixels
// Sets eVar10 to "desktop layout:1920x937".
s.eVar10 = getResponsiveLayout(500, 700, 1000);

// A visitor accesses your site on their phone.
// * Your site has only a phone mode, a tablet mode, and a desktop mode
// * Your site switches from phone mode to tablet mode when the browser width is greater than 800 pixels
// * Your site switches from tablet mode to desktop mode when the browser width is greater than 1,100 pixels
// Sets eVar10 to "phone portrait layout:720x1280"
s.eVar10 = getResponsiveLayout(800, 800, 1100);
```

## Versiehistorie

### 1.1 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 1.0 (2 mei 2018)

* Eerste release.
