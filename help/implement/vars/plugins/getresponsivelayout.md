---
title: getResponsiveLayout
description: Bepaal welke lay-out van een website momenteel wordt weergegeven.
translation-type: tm+mt
source-git-commit: ''

---


# Adobe-insteekmodule: getResponsiveLayout

> [!IMPORTANT] Deze plug-in wordt geleverd door Adobe Consulting als een hoffelijkheid om u te helpen meer waarde te krijgen van Adobe Analytics. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `getResponsiveLayout` insteekmodule kunt u bijhouden naar welke versie van uw responsieve, op ontwerpen gebaseerde website een bezoeker momenteel kijkt. Adobe raadt u aan deze plug-in te gebruiken als uw site gebruikmaakt van een responsief ontwerp en u de versie van de site wilt bijhouden die door een bezoeker wordt weergegeven. Deze insteekmodule is niet nodig als uw site geen responsief ontwerp gebruikt.

## De plug-in installeren met de Adobe Experience Platform Launch-extensie

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Go to the [!UICONTROL Extensions] tab, then click on the [!UICONTROL Catalog] button
1. De [!UICONTROL Common Analytics Plugins] extensie installeren en publiceren
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: Geen
   * Gebeurtenis: Kern - Bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: Gebruikelijke plug-ins voor Analytics
   * Type handeling: getResponsiveLayout initialiseren
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met de aangepaste code-editor van Launch

Als u de extensie van de plug-in niet wilt gebruiken, kunt u de aangepaste code-editor gebruiken.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar het [!UICONTROL Extensions] tabblad en klik vervolgens op de [!UICONTROL Configure] knop onder de extensie Adobe Analytics.
1. Vouw de [!UICONTROL Configure tracking using custom code] accordeon uit, zodat de [!UICONTROL Open Editor] knop zichtbaar wordt.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

## De plug-in installeren met AppMeturement

Kopieer en plak de volgende code ergens in het AppMeasurement-bestand nadat het analytics tracking-object is geïnstantieerd (met `s_gi`). Door opmerkingen en versienummers van de code in uw implementatie te behouden, kan Adobe eventuele problemen oplossen.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getResponsiveLayout v1.0 */
var getResponsiveLayout=function(ppw,plw,tw){if(!(isNaN(ppw)||isNaN(plw)||isNaN(tw)||plw<ppw||tw<plw)){var b=window.innerWidth|| document.documentElement.clientWidth||document.body.clientWidth;return(ppw<plw&&b<=plw?b<=ppw?"phone portrait layout":"phone landscape layout":b<=plw?"phone layout":b<=tw?"tablet layout":"desktop layout")+":"+b+"x"+(window.innerHeight|| document.documentElement.clientHeight||document.body.clientHeight)}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `getResponsiveLayout` methode gebruikt de volgende argumenten:

* **`ppw`** (vereist, geheel getal): De maximumbreedte van pixels die een browservenster kan hebben voordat de pagina overschakelt van de staande lay-out Telefoon naar een liggende lay-out voor de telefoon
* **`plw`** (vereist, geheel getal): De maximale breedte van pixels die een browservenster kan hebben voordat de pagina overschakelt van een liggende lay-out voor de telefoon naar een lay-out op basis van tablets
* **`tw`** (vereist, Booleaans): De maximale breedte van pixels die een browservenster kan hebben voordat de pagina overschakelt van een tabletlay-out naar een op het bureaublad gebaseerde lay-out

Wanneer deze methode wordt aangeroepen, wordt een tekenreeks met twee delen geretourneerd. Het eerste deel gebruikt van de volgende waarden, afhankelijk van de breedte van de browser en de bovenstaande argumenten:

* `"phone portrait layout"`
* `"phone landscape layout"`
* `"phone layout"` (voor sites die niet zowel een staande als een liggende lay-out hebben)
* `"tablet layout"`
* `"desktop layout"`

Het tweede deel van de geretourneerde tekenreeks is de breedte en hoogte van de browser. Bijvoorbeeld, `"desktop layout:1243x700"`.

## Voorbeelden van aanroepen

### Voorbeeld 1

Indien...

* Uw site schakelt over van de modus Staand telefoon naar de modus Liggend, wanneer de breedte van de browser groter is dan 500 pixels
* Uw site schakelt over van de modus Liggend voor de telefoon naar de tabletmodus als de breedte van de browser groter is dan 700 pixels
* Uw site schakelt over van tabletmodus naar bureaubladmodus als de breedte van de browser groter is dan 1000 pixels

...met de volgende code wordt eVar10 ingesteld op de huidige responsieve ontwerplay-out, zoals de bezoeker die ervaart, en de breedte en afmetingen van de browser

```js
s.eVar10 = getResponsiveLayout(500, 700, 1000);
```

### Voorbeeld 2

Indien...

* Uw site heeft alleen een telefoonmodus, een tabletmodus en een desktopmodus
* Uw site schakelt over van de telefoonmodus naar de tabletmodus als de breedte van de browser groter is dan 500 pixels
* Uw site schakelt over van de tabletmodus naar de bureaubladmodus als de breedte van de browser groter is dan 1100 pixels

...met de volgende code wordt eVar10 ingesteld op de huidige responsieve ontwerplay-out, zoals de bezoeker die ervaart, en de breedte en afmetingen van de browser

```js
s.eVar10 = getResponsiveLayout(500, 500, 1100);
```

## Versiehistorie

### 1.0 (2 mei 2018)

* Eerste release.
