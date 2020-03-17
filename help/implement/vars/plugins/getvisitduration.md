---
title: getVisitDuration
description: Houd bij hoeveel tijd een bezoeker tot dusver op de site is geweest.
translation-type: tm+mt
source-git-commit: 180ad544541f25d02b3a257559bc045abed7387b

---


# Adobe-insteekmodule: getVisitDuration

> [!IMPORTANT] Deze plug-in wordt geleverd door Adobe Consulting als een hoffelijkheid om u te helpen meer waarde te krijgen van Adobe Analytics. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

De `getVisitDuration` insteekmodule houdt de hoeveelheid tijd in minuten bij die de bezoeker tot dat moment op de site is geweest. Adobe raadt u aan deze plug-in te gebruiken als u de cumulatieve tijd op de site tot dat moment wilt bijhouden of als u de tijd wilt bijhouden die nodig is om een activiteit uit te voeren. Deze plug-in houdt de hoeveelheid tijd tussen gebeurtenissen niet bij; Als u deze functionaliteit wilt gebruiken, gebruikt u de `getTimeBetweenEvents` insteekmodule.

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
   * Type handeling: getVisitDuration initialiseren
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
/* Adobe Consulting Plugin: getVisitDuration v2.0 */
s.getVisitDuration=function(){var d=new Date,c=d.getTime(),b=this.c_r("s_dur");if(isNaN(b)||18E5<c-b)b=c;var a=c-b;d.setTime(c+18E5); this.c_w("s_dur",b+"",d);if(0===a)return"first hit of visit";a=Math.floor(a/6E4);return 0===a?"less than a minute":1===a?"1 minute": a+" minutes"};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `getVisitDuration` methode gebruikt geen argumenten. Deze geeft een van de volgende waarden:

* `"first hit of visit"`
* `"less than a minute"`
* `"1 minute"`
* `"[x] minutes"` (waarbij `[x]` het aantal minuten is verstreken sinds de bezoeker op de locatie is aangeland)

Deze plug-in maakt een cookie van de eerste partij met de naam `"s_dur"`, dat wil zeggen het aantal milliseconden dat is verstreken sinds de bezoeker de site heeft aangeland. Het cookie verloopt na 30 minuten inactiviteit.

## Voorbeelden van aanroepen

### Voorbeeld 1

De volgende code...

```js
s.eVar10 = s.getVisitDuration();
```

...zal eVar10 altijd gelijk stellen aan het aantal minuten dat is verstreken sinds de bezoeker op de site is aangeland

### Voorbeeld 2

De volgende code...

```js
if(s.inList(s.events, "purchase")) s.eVar10 = s.getVisitDuration();
```

...gebruikt de insteekmodule inList om te controleren of de variabele events de aankoopgebeurtenis bevat.  In dat geval wordt eVar10 ingesteld op het aantal minuten tussen het begin van het bezoek van de bezoeker en het tijdstip van aankoop.

### Voorbeeld 3

De volgende code...

```js
s.prop10 = s.getVisitDuration();
```

...stelt prop10 altijd in op het aantal minuten dat is verstreken sinds de bezoeker de site heeft aangeland.  Dit is handig als voor prop10 het plakken is ingeschakeld.  Als u de metrische waarde ‘exits’ toevoegt aan het rapport prop10, wordt een korrelig, ‘scatterplot’ weergegeven met de melding hoe lang een bezoek duurde in minuten voordat een bezoeker de site verliet.

## Versiehistorie

### 2.0 (2 mei 2018)

* Puntrelease (volledige heranalyse/herschrijven van plug-in).
