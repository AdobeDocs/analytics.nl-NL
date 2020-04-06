---
title: getValOnce
description: Voorkomen dat een variabele Analytics tweemaal achter elkaar op dezelfde waarde wordt ingesteld.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Adobe-insteekmodule: getValOnce

>[!IMPORTANT] Deze plug-in wordt geleverd door Adobe Consulting als een hoffelijkheid om u te helpen meer waarde te krijgen van Adobe Analytics. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `getValOnce` insteekmodule voorkomt u dat een variabele meerdere keren op dezelfde waarde wordt ingesteld. Adobe raadt u aan deze plug-in te gebruiken als u gevallen wilt dedupliceren waarin een bezoeker een pagina vernieuwt of een bepaalde pagina meerdere keren bezoekt. Deze insteekmodule is niet nodig als u zich geen zorgen maakt over de metrische waarde &#39;Voorvallen&#39; in de analysewerkruimte.

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
   * Type handeling: getValOnce initialiseren
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
/* Adobe Consulting Plugin: getValOnce v2.0 */
s.getValOnce=function(vtc,cn,et,ep){if(vtc&&(cn=cn||"s_gvo",et=et||0,ep="m"===ep?6E4:864E5,vtc!==this.c_r(cn))){var e=new Date;e.setTime(e.getTime()+et*ep);this.c_w(cn,vtc,0===et?0:ep);return vtc}return""};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `getValOnce` methode gebruikt de volgende argumenten:

* **`vtc`** (vereist, tekenreeks): De variabele die moet worden gecontroleerd en gecontroleerd of deze eerder is ingesteld op een identieke waarde
* **`cn`** (optioneel, tekenreeks): De naam van het cookie dat de te controleren waarde bevat. Standaardwaarden: `"s_gvo"`
* **`et`** (optioneel, geheel getal): De vervaldatum van de cookie in dagen (of minuten, afhankelijk van het `ep` argument). De standaardwaarde is `0`, die aan het einde van de browsersessie vervalt
* **`ep`** (optioneel, tekenreeks): Stel dit argument alleen in als het `et` argument ook is ingesteld. Stel dit argument in op `"m"` als u wilt dat het `et` argument in minuten verloopt in plaats van dagen. Wordt standaard ingesteld op `"d"`, waardoor het `et` argument wordt ingesteld in dagen.

Als het `vtc` argument en de koekjeswaarde aanpassen, keert deze methode een lege koord terug. Als het `vtc` argument en de koekjeswaarde niet aanpassen, keert de methode het `vtc` argument als koord terug.

## Voorbeelden van aanroepen

### Voorbeeld 1

Gebruik deze vraag om de zelfde waarde te verhinderen binnen aan s.campagne meer dan eens in een rij voor volgende 30 dagen wordt overgegaan:

```js
s.campaign=s.getValOnce(s.campaign,"s_campaign",30);
```

In de bovengenoemde vraag, zal het elektrische toestel eerst de waarde reeds in het s_campagne koekje met de waarde vergelijken die uit de huidige s.campagne variabele komt.   Als een gelijke niet wordt gemaakt, zal de stop-binnen het s_campagne koekje gelijk aan de nieuwe waarde plaatsen die uit s.campagne komt en dan de nieuwe waarde terugkeren.   Deze vergelijking vindt plaats in de komende 30 dagen

### Voorbeeld 2

Gebruik deze aanroep om te voorkomen dat dezelfde waarde tijdens de gehele sessie wordt ingesteld:

```js
s.eVar2=s.getValOnce(s.eVar2,"s_ev2",0,"m");
```

Met deze code wordt voorkomen dat dezelfde waarde meerdere keren achter een gebruikerssessie in s.eVar2 wordt doorgegeven.  Het negeert ook de &quot;m&quot;waarde in het argument (aan het eind van de vraag) aangezien de vervaltijd aan 0 wordt geplaatst.   De code slaat ook de vergelijkingswaarde in het s_ev2 koekje op.

## Versiehistorie

### 2.0

* Puntrelease (opnieuw gecompileerd, kleiner codeformaat).

### 1.1

* De optie voor het kiezen van minuten of dagen voor het verlopen via de `t` parameter toegevoegd.
* Correctie van het bereik van de `k` variabele die wordt gebruikt om het tot stop-binnen slechts te beperken. Deze wijziging voorkomt mogelijke interferentie met andere code op de pagina.
