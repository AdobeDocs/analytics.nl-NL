---
title: getTimeSinceLastVisit
description: Meet de hoeveelheid tijd die tussen twee bezoeken is verstreken.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Adobe-insteekmodule: getTimeSinceLastVisit

>[!IMPORTANT] Deze plug-in wordt geleverd door Adobe Consulting als een hoffelijkheid om u te helpen meer waarde te krijgen van Adobe Analytics. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `getTimeSinceLastVisit` insteekmodule kunt u bijhouden hoelang een bezoeker na zijn laatste bezoek naar uw site is teruggekeerd.

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
   * Type handeling: getTimeSinceLastVisit initialiseren
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
/* Adobe Consulting Plugin: getTimeSinceLastVisit v1.0 (Requires formatTime and inList plug-ins) */
s.getTimeSinceLastVisit=function(){var s=this,a=new Date,b=a.getTime(),c=s.c_r("s_tslv")||0,d=Math.round((b-c)/1E3);a.setTime(b+63072E6);s.c_w("s_tslv",b,a);return c?1800<d&&s.formatTime?s.formatTime(d):"":"New Visitor"};

/* Adobe Consulting Plugin: formatTime v1.1 (Requires inList plug-in) */
s.formatTime=function(ns,tf,bml){var s=this;if(!("undefined"===typeof ns||isNaN(ns)||0>Number(ns))){if("string"===typeof tf&&"d"===tf||("string"!==typeof tf||!s.inList("h,m,s",tf))&&86400<=ns){tf=86400;var d="days";bml=isNaN(bml)?1:tf/(bml*tf)} else"string"===typeof tf&&"h"===tf||("string"!==typeof tf||!s.inList("m,s",tf))&&3600<=ns?(tf=3600,d="hours", bml=isNaN(bml)?4: tf/(bml*tf)):"string"===typeof tf&&"m"===tf||("string"!==typeof tf||!s.inList("s",tf))&&60<=ns?(tf=60,d="minutes",bml=isNaN(bml)?2: tf/(bml*tf)):(tf=1,d="seconds",bml=isNaN(bml)?.2:tf/bml);ns=Math.round(ns*bml/tf)/bml+" "+d;0===ns.indexOf("1 ")&&(ns=ns.substring(0, ns.length-1));return ns}};

/* Adobe Consulting Plugin: inList v2.1 */
s.inList=function(lv,vtc,d,cc){if("string"!==typeof vtc)return!1;if("string"===typeof lv)lv=lv.split(d||",");else if("object"!== typeof lv)return!1;d=0;for(var e=lv.length;d<e;d++)if(1==cc&&vtc===lv[d]||vtc.toLowerCase()===lv[d].toLowerCase())return!0;return!1};
 /******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `getTimeSinceLastVisit` methode gebruikt geen argumenten. Het retourneert de hoeveelheid tijd die is verstreken sinds de bezoeker voor het laatst naar de site is gekomen. Deze tijd wordt als volgt geplakt:

* De tijd tussen 30 minuten en een uur sinds het laatste bezoek is ingesteld op de dichtstbijzijnde halftijdse benchmark. Bijvoorbeeld, `"30.5 minutes"`, `"53 minutes"`
* De tijd tussen een uur en een dag wordt afgerond aan de dichtstbijzijnde benchmark van kwartier. Bijvoorbeeld, `"2.25 hours"`, `"7.5 hours"`
* Tijd langer dan een dag wordt afgerond naar de dichtstbijzijnde dagbenchmark. Bijvoorbeeld, `"1 day"`, `"3 days"`, `"9 days"`, `"372 days"`
* Als een bezoeker niet eerder is bezocht of de verstreken tijd langer is dan twee jaar, wordt de waarde ingesteld op `"New Visitor"`.

>[!NOTE] Deze insteekmodule retourneert alleen een waarde bij de eerste aanraking van een bezoek.

Deze plug-in maakt een cookie van de eerste partij die wordt aangeroepen `"s_tslv"` op een Unix-tijdstempel van de huidige tijd. Het cookie verloopt na twee jaar inactiviteit.

## Voorbeelden van aanroepen

### Voorbeeld 1

Als een gloednieuwe bezoeker naar de site komt en de volgende code op de eerste pagina van het bezoek wordt uitgevoerd...

```javascript
s.prop1 = s.getTimeSinceLastVisit();
s.linkTrackVars = s.apl(s.linkTrackVars, "prop1") //ensures that prop1 will be included on the first hit of the visit
```

...de waarde van s.prop1 zal aan &quot;Nieuwe Bezoeker&quot;worden geplaatst.

Als dezelfde code op hetzelfde domein wordt uitgevoerd na 35 minuten inactiviteit, wordt de waarde van s.prop1 ingesteld op &quot;35 minuten&quot;.

Als dezelfde code op hetzelfde domein wordt uitgevoerd na 4 dagen van verdere inactiviteit, wordt de waarde van s.prop1 ingesteld op &quot;4 dagen&quot;.

## Versiehistorie

### 1.0 (16 april 2018)

* Puntrelease (opnieuw gecompileerde code en kleinere grootte).
* Code die is afgeleid van de `getDaysSinceLastVisit` plug-in (nu afgekeurd en hernoemd).
* Gebruikt nu `formatTime` en `inList` stop-ins voor de terugkeerwaarde.
