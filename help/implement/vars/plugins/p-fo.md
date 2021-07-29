---
title: p_fo (alleen Pagina eerste)
description: Zorg ervoor dat bepaalde routines slechts één keer per pagina worden geactiveerd.
exl-id: e82d77f9-2ea9-4b1b-b645-b12879c344ec
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 0%

---

# Adobe-plug-in: p_fo (alleen Pagina eerste)

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

De `p_fo` plug-in is een hulpprogramma dat controleert of een specifiek JavaScript-object bestaat. Als het object niet bestaat, maakt de plug-in het object en wordt `true` geretourneerd. Als het JavaScript-object al op de pagina aanwezig is, wordt `false` geretourneerd. Deze insteekmodule is handig als u code precies één keer op een pagina wilt uitvoeren. Verscheidene andere stop-ins baseren zich op deze code om te werken. Deze plug-in is niet nodig als u zich geen zorgen maakt over het aantal keren dat code op een pagina wordt uitgevoerd of als u geen afhankelijke plug-ins gebruikt.

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
   * Type handeling: p_fo initialiseren
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
/* Adobe Consulting Plugin: p_fo (pageFirstOnly) v3.0 (Requires AppMeasurement) */
function p_fo(c){if("-v"===c)return{plugin:"p_fo",version:"3.0"};a:{if("undefined"!==typeof window.s_c_il){var a=0;for(var b;a<window.s_c_il.length;a++)if(b=window.s_c_il[a],b._c&&"s_c"===b._c){a=b;break a}}a=void 0}"undefined"!==typeof a&&(a.contextData.p_fo="3.0");window.__fo||(window.__fo={});if(window.__fo[c])return!1;window.__fo[c]={};return!0};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De methode `p_fo` gebruikt de volgende argumenten:

* **on** (required, string): De naam van het JavaScript-object dat door de insteekmodule wordt gemaakt als het object nog niet op de pagina bestaat.

Als het object nog niet bestaat, retourneert deze methode `true` en wordt het object gemaakt. Als het object al bestaat, retourneert deze methode `false`.

## Voorbeelden van aanroepen

### Voorbeeld 1

De volgende code controleert of het object &quot;myobject&quot; op de pagina aanwezig is.  Als het object &quot;myobject&quot; niet bestaat, maakt de code het object &quot;myobject&quot; en retourneert deze de waarde true.  Het resultaat is dat de code binnen de voorwaardelijke instructie (Console.log(&#39;hello&#39;);) wordt uitgevoerd.

Als het object &quot;myobject&quot; echter al bestaat wanneer de p_fo-aanroep plaatsvindt, retourneert de p_fo-functie de waarde false en wordt de voorwaardelijke instructie dus als false beschouwd.  In dit geval wordt de code binnen de voorwaardelijke instructie niet uitgevoerd.

```javascript
if(s.p_fo("myobject"))
{
  console.log("hello");
}
```

**OPMERKING:** Telkens wanneer een nieuw paginaobject/DOM wordt geladen (of de huidige pagina opnieuw wordt geladen), bestaat het object dat in het argument on is opgegeven, niet meer en retourneert de insteekmodule p_fo dus opnieuw true wanneer de pagina volledig is geladen.

## Versiehistorie

### 3.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 2,0

* Puntrelease (opnieuw gecompileerd, kleiner codeformaat).
* Veranderd type geretourneerde waarde van geheel getal in Boolean

### 1,0

* Eerste release.
