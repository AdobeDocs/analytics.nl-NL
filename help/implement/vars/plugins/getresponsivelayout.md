---
title: getResponsiveLayout
description: Bepaal welke lay-out van een website momenteel wordt weergegeven.
feature: Variables
exl-id: 5b192d02-fc3c-4b82-acb4-42902202ab5f
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# Adobe-insteekmodule: getResponsiveLayout

{{plug-in}}

De `getResponsiveLayout` Met de insteekmodule kunt u bijhouden naar welke versie van uw responsieve, op ontwerpen gebaseerde website een bezoeker momenteel kijkt. Adobe raadt u aan deze plug-in te gebruiken als uw site gebruikmaakt van een responsief ontwerp en u de versie van de site wilt bijhouden die door een bezoeker wordt weergegeven. Deze insteekmodule is niet nodig als uw site geen responsief ontwerp gebruikt.

## De insteekmodule installeren met de extensie Web SDK of Web SDK

Deze plug-in wordt nog niet ondersteund voor gebruik in de Web SDK.

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
   * Type handeling: getResponsiveLayout initialiseren
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
/* Adobe Consulting Plugin: getResponsiveLayout v1.1 (Requires AppMeasurement) */
var getResponsiveLayout=function(ppw,plw,tw){var c=ppw,b=plw,e=tw;if("-v"===c)return{plugin:"getResponsiveLayout",version:"1.1"};a:{if("undefined"!==typeof window.s_c_il){var a=0;for(var d;a<window.s_c_il.length;a++)if(d=window.s_c_il[a],d._c&&"s_c"===d._c){a=d;break a}}a=void 0}"undefined"!==typeof a&&(a.contextData.getResponsiveLayout="1.1");if(!(isNaN(c)||isNaN(b)||isNaN(e)||b<c||e<b))return a=window.innerWidth||document.documentElement.clientWidth||document.body.clientWidth,(c<b&&a<=b?a<=c?"phone portrait layout":"phone landscape layout":a<=b?"phone layout":a<=e?"tablet layout":"desktop layout")+":"+a+"x"+(window.innerHeight||document.documentElement.clientHeight||document.body.clientHeight)};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `getResponsiveLayout` function gebruikt de volgende argumenten:

* **`ppw`** (vereist, geheel getal): de maximale breedte van pixels die een browservenster kan hebben voordat de pagina overschakelt van een staande lay-out Telefoon naar een liggende lay-out Telefoon
* **`plw`** (vereist, geheel getal): de maximale breedte van pixels die een browservenster kan hebben voordat de pagina overschakelt van een liggende lay-out voor de telefoon naar een op tablets gebaseerde lay-out
* **`tw`** (vereist, geheel getal): de maximale breedte van pixels die een browservenster kan hebben voordat de pagina overschakelt van een tabletlay-out naar een op het bureaublad gebaseerde lay-out

Als deze functie wordt aangeroepen, wordt een tekenreeks geretourneerd met twee delen die zijn gescheiden door een dubbele punt (`:`). Het eerste deel van de tekenreeks bevat een van de volgende waarden, afhankelijk van de breedte van de browser en de bovenstaande argumenten:

* `"phone portrait layout"`
* `"phone landscape layout"`
* `"phone layout"` (voor sites die niet zowel een staande als een liggende lay-out hebben)
* `"tablet layout"`
* `"desktop layout"`

Het tweede deel van de geretourneerde tekenreeks is de breedte en hoogte van de browser. Bijvoorbeeld: `"desktop layout:1243x700"`.

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
