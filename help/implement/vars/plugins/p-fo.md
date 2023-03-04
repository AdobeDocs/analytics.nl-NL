---
title: p_fo (alleen Pagina eerste)
description: Zorg ervoor dat bepaalde routines slechts één keer per pagina worden geactiveerd.
feature: Variables
exl-id: e82d77f9-2ea9-4b1b-b645-b12879c344ec
source-git-commit: c53f886d5329e2a3b5023f9396c3aa2360a86901
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---

# Adobe-plug-in: p_fo (alleen Pagina eerste)

{{plug-in}}

De `p_fo` insteekmodule is een hulpprogramma dat controleert of een specifiek JavaScript-object bestaat. Als het object niet bestaat, maakt de plug-in het object en wordt deze geretourneerd `true`. Als het JavaScript-object al op de pagina aanwezig is, wordt het geretourneerd `false`. Deze insteekmodule is handig als u code precies één keer op een pagina wilt uitvoeren. Verscheidene andere stop-ins baseren zich op deze code om te werken. Deze plug-in is niet nodig als u zich geen zorgen maakt over het aantal keren dat code op een pagina wordt uitgevoerd of als u geen afhankelijke plug-ins gebruikt.

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
    * Action Type: Initialize p_fo
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
/* Adobe Consulting Plugin: p_fo (pageFirstOnly) v3.0 (Requires AppMeasurement) */
function p_fo(c){if("-v"===c)return{plugin:"p_fo",version:"3.0"};a:{if("undefined"!==typeof window.s_c_il){var a=0;for(var b;a<window.s_c_il.length;a++)if(b=window.s_c_il[a],b._c&&"s_c"===b._c){a=b;break a}}a=void 0}"undefined"!==typeof a&&(a.contextData.p_fo="3.0");window.__fo||(window.__fo={});if(window.__fo[c])return!1;window.__fo[c]={};return!0};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `p_fo` function gebruikt de volgende argumenten:

* **op** (vereist, tekenreeks): De naam van het JavaScript-object dat door de insteekmodule wordt gemaakt als het object nog niet op de pagina bestaat.

Als het object nog niet bestaat, wordt deze functie geretourneerd `true` en maakt het object. Als het object al bestaat, wordt deze functie geretourneerd `false`.

## Voorbeelden van aanroepen

### Voorbeeld 1

De volgende code controleert of het object &quot;myobject&quot; op de pagina aanwezig is.  Als het object &quot;myobject&quot; niet bestaat, maakt de code het object &quot;myobject&quot; en retourneert deze de waarde true.  Het resultaat is dat de code binnen de voorwaardelijke instructie (Console.log(&#39;hello&#39;);) wordt uitgevoerd.

Als het object &quot;myobject&quot; echter al bestaat wanneer de p_fo-aanroep plaatsvindt, retourneert de p_fo-functie de waarde false en wordt de voorwaardelijke instructie dus als false beschouwd.  In dit geval wordt de code binnen de voorwaardelijke instructie niet uitgevoerd.

```js
if(p_fo("myobject"))
{
  console.log("hello");
}
```

**OPMERKING:** Telkens wanneer een nieuw paginaobject/DOM wordt geladen (of de huidige pagina opnieuw wordt geladen), bestaat het object dat is opgegeven in het argument on niet meer en retourneert de insteekmodule p_fo dus opnieuw de waarde wanneer de pagina volledig is geladen.

## Versiehistorie

### 3.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 2.0

* Puntrelease (opnieuw gecompileerd, kleiner codeformaat).
* Veranderd type geretourneerde waarde van geheel getal in Boolean

### 1.0

* Eerste release.
