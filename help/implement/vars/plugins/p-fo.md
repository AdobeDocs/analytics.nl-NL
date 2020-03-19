---
title: p_fo (alleen Pagina eerste)
description: Zorg ervoor dat bepaalde routines slechts één keer per pagina worden geactiveerd.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe-insteekmodule: p_fo (alleen Pagina eerste)

> [!IMPORTANT] Deze plug-in wordt geleverd door Adobe Consulting als een hoffelijkheid om u te helpen meer waarde te krijgen van Adobe Analytics. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

De `p_fo` insteekmodule is een hulpprogramma dat controleert of een specifiek JavaScript-object bestaat. Als het object niet bestaat, maakt de plug-in het object en wordt deze geretourneerd `true`. Als het JavaScript-object al op de pagina aanwezig is, wordt het geretourneerd `false`. Deze insteekmodule is handig als u code precies één keer op een pagina wilt uitvoeren. Verscheidene andere stop-ins baseren zich op deze code om te werken. Deze plug-in is niet nodig als u zich geen zorgen maakt over het aantal keren dat code op een pagina wordt uitgevoerd of als u geen afhankelijke plug-ins gebruikt.

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
   * Type handeling: p_fo initialiseren
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

Kopieer en plak de volgende code ergens in het AppMeasurement-bestand nadat het analytics tracking-object is geïnstantieerd (met [`s_gi`](../functions/s-gi.md)). Door opmerkingen en versienummers van de code in uw implementatie te behouden, kan Adobe eventuele problemen oplossen.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: p_fo (pageFirstOnly) v2.0 */
s.p_fo=function(on){var s=this;s.__fo||(s.__fo={});if(s.__fo[on])return!1;s.__fo[on]={};return!0};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `p_fo` methode gebruikt de volgende argumenten:

* **on** (required, string): De naam van het JavaScript-object dat door de insteekmodule wordt gemaakt als het object nog niet op de pagina bestaat.

Als het object nog niet bestaat, retourneert deze methode het object `true` en wordt het gemaakt. Als het object al bestaat, wordt deze methode geretourneerd `false`.

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

**OPMERKING:** Telkens wanneer een nieuw paginaobject/DOM wordt geladen (of de huidige pagina opnieuw wordt geladen), bestaat het object dat is opgegeven in het argument on niet meer en retourneert de insteekmodule p_fo dus opnieuw de waarde wanneer de pagina volledig is geladen.

## Versiehistorie

### 2.0

* Puntrelease (opnieuw gecompileerd, kleiner codeformaat).
* Veranderd type geretourneerde waarde van geheel getal in Boolean

### 1.0

* Eerste release.
