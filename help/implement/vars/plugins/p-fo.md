---
title: p_fo (alleen Pagina eerste)
description: Zorg ervoor dat bepaalde routines slechts één keer per pagina worden geactiveerd.
feature: Variables
exl-id: e82d77f9-2ea9-4b1b-b645-b12879c344ec
source-git-commit: bbb138d979968ec2536e53ff07001b43156df095
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---

# Adobe-plug-in: p_fo (alleen Pagina eerste)

{{plug-in}}

De `p_fo` insteekmodule is een hulpprogramma dat controleert of een specifiek JavaScript-object bestaat. Als het object niet bestaat, maakt de plug-in het object en wordt deze geretourneerd `true`. Als het JavaScript-object al op de pagina aanwezig is, wordt het geretourneerd `false`. Deze insteekmodule is handig als u code precies één keer op een pagina wilt uitvoeren. Verscheidene andere stop-ins baseren zich op deze code om te werken. Deze plug-in is niet nodig als u zich geen zorgen maakt over het aantal keren dat code op een pagina wordt uitgevoerd of als u geen afhankelijke plug-ins gebruikt.

## De plug-in installeren met de extensie Web SDK

Adobe biedt een uitbreiding aan die u toestaat om het meest algemeen gebruikte stop-ins met het Web SDK te gebruiken.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klikken **[!UICONTROL Tags]** klikt u links op de gewenste eigenschap tag.
1. Klikken **[!UICONTROL Extensions]** klikt u links op de knop **[!UICONTROL Catalog]** tab
1. Zoek en installeer de **[!UICONTROL Common Web SDK Plugins]** extensie.
1. Klikken **[!UICONTROL Data Elements]** klikt u links op het gewenste gegevenselement.
1. Stel de gewenste naam van het gegevenselement in met de volgende configuratie:
   * Extensie: Algemene insteekmodules voor Web SDK
   * Gegevenselement: `p_fo`
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
   * Type handeling: p_fo initialiseren
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
