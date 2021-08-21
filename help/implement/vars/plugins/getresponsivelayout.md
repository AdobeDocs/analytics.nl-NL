---
title: getResponsiveLayout
description: Bepaal welke lay-out van een website momenteel wordt weergegeven.
exl-id: 5b192d02-fc3c-4b82-acb4-42902202ab5f
source-git-commit: ab078c5da7e0e38ab9f0f941b407cad0b42dd4d1
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# Adobe-plug-in: getResponsiveLayout

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de insteekmodule `getResponsiveLayout` kunt u bijhouden naar welke versie van uw responsieve, op ontwerpen gebaseerde website een bezoeker momenteel kijkt. Adobe raadt u aan deze plug-in te gebruiken als uw site gebruikmaakt van een responsief ontwerp en u de versie van de site wilt bijhouden die door een bezoeker wordt weergegeven. Deze insteekmodule is niet nodig als uw site geen responsief ontwerp gebruikt.

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
   * Type handeling: getResponsiveLayout initialiseren
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
/* Adobe Consulting Plugin: getResponsiveLayout v1.1 (Requires AppMeasurement) */
var getResponsiveLayout=function(ppw,plw,tw){var c=ppw,b=plw,e=tw;if("-v"===c)return{plugin:"getResponsiveLayout",version:"1.1"};a:{if("undefined"!==typeof window.s_c_il){var a=0;for(var d;a<window.s_c_il.length;a++)if(d=window.s_c_il[a],d._c&&"s_c"===d._c){a=d;break a}}a=void 0}"undefined"!==typeof a&&(a.contextData.getResponsiveLayout="1.1");if(!(isNaN(c)||isNaN(b)||isNaN(e)||b<c||e<b))return a=window.innerWidth||document.documentElement.clientWidth||document.body.clientWidth,(c<b&&a<=b?a<=c?"phone portrait layout":"phone landscape layout":a<=b?"phone layout":a<=e?"tablet layout":"desktop layout")+":"+a+"x"+(window.innerHeight||document.documentElement.clientHeight||document.body.clientHeight)};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De functie `getResponsiveLayout` gebruikt de volgende argumenten:

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
