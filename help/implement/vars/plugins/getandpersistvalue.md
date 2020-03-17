---
title: getAndPersistValue
description: Sla een waarde op die later kan worden opgehaald.
translation-type: tm+mt
source-git-commit: 180ad544541f25d02b3a257559bc045abed7387b

---


# Adobe-insteekmodule: getAndPersistValue

> [!IMPORTANT] Deze plug-in wordt geleverd door Adobe Consulting als een hoffelijkheid om u te helpen meer waarde te krijgen van Adobe Analytics. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `getAndPersistValue` insteekmodule kunt u een waarde opslaan in een cookie die later tijdens een bezoek kan worden opgehaald. Deze rol komt overeen met de functie [!UICONTROL Storage duration] in Adobe Experience Platform Launch. Adobe raadt u aan deze plug-in te gebruiken als u na het instellen van de variabele automatisch een analysevariabele tot dezelfde waarde wilt behouden. Deze insteekmodule is niet nodig als de [!UICONTROL Storage duration] functie Starten voldoende is of als u variabelen niet op dezelfde waarde hoeft in te stellen en te behouden bij volgende treffers. Voor de ingebouwde persistentie van eVars is het gebruik van deze plug-in niet vereist, aangezien deze variabelen door Adobe op de server blijven staan.

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
   * Type handeling: getAndPersistValue initialiseren
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
/* Adobe Consulting Plugin: getAndPersistValue v2.0 */
s.getAndPersistValue=function(vtp,cn,ex){var b=new Date;cn=cn?cn:"s_gapv";(ex=ex?ex:0)?b.setTime(b.getTime()+864E5*ex): b.setTime(b.getTime()+18E5);vtp||(vtp=this.c_r(cn));this.c_w(cn,vtp,b);return vtp};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `getAndPersist` methode gebruikt de volgende argumenten:

* **`vtp`** (vereist): De waarde die van pagina tot pagina moet worden behouden
* **`cn`** (optioneel): De naam van het cookie waarin de waarde wordt opgeslagen. Als dit argument niet is ingesteld, krijgt het cookie de naam `"s_gapv"`
* **`ex`** (optioneel): Het aantal dagen voordat de cookie vervalt. Als dit argument is `0` of niet is ingesteld, verloopt het cookie aan het einde van het bezoek (30 minuten inactiviteit).

Als de variabele in het `vtp` argument is ingesteld, stelt de plug-in het cookie in en retourneert deze de waarde van het cookie. Als de variabele in het `vtp` argument niet is ingesteld, retourneert de plug-in alleen de waarde van het cookie.

## Voorbeelden

### Voorbeeld 1

Met de volgende code wordt eVar21 ingesteld op de waarde &quot;hello&quot;.  De code zal dan ev21gapv koekje, dat over 28 dagen zal verlopen, aan de waarde van eVar21 (d.w.z. &quot;hallo&quot;).  De code stelt vervolgens (re)Var21 in op de waarde van het ev21gapv-cookie.

```js
s.eVar21 = "hello";
s.eVar21 = s.getAndPersistValue(s.eVar21,"ev21gapv",28);
```

### Voorbeeld 2

Stel dat eVar21 nog niet is ingesteld op de huidige pagina, maar in de afgelopen 28 dagen gelijk was aan &quot;hello&quot; op een vorige pagina.   Met de volgende code wordt eVar21 alleen ingesteld op de waarde van het ev21gapv-cookie (d.w.z. &quot;hallo&quot;).  De ev21gapv-cookie wordt niet opnieuw ingesteld omdat eVar21 niet op de huidige pagina is ingesteld voordat de functie werd aangeroepen.

```js
s.eVar21 = s.getAndPersistValue(s.eVar21,"ev21gapv",28);
```

### Voorbeeld 3

Stel dat eVar21 nog niet is ingesteld op de huidige pagina, maar in de afgelopen 28 dagen gelijk was aan &quot;hello&quot; op een vorige pagina.  Met de volgende code wordt alleen prop35 ingesteld op de waarde van het ev21gapv-cookie (d.w.z. &quot;hallo&quot;).  eVar21 wordt niet ingesteld.

```js
s.prop35 = s.getAndPersistValue(s.eVar21,"ev21gapv",28);
```

### Voorbeeld 4

Met de volgende code wordt eVar21 ingesteld op de waarde &quot;howdy&quot;.  De code stelt vervolgens de ev21gapv-cookie, die over 28 dagen verloopt, in (of herstelt deze) op de waarde van eVar21 (d.w.z. &quot;howdy&quot;).  De code stelt dan prop35 in op de waarde van het ev21gapv-cookie (dat wil zeggen &quot;howdy&quot;).

```js
s.eVar21 = "howdy";
s.prop35 = s.getAndPersistValue(s.eVar21,"ev21gapv",28);
```

### Voorbeeld 5

Stel dat s.eVar21 de laatste 28 dagen op geen enkele pagina is ingesteld.  De volgende code stelt s.eVar21 gelijk aan niets omdat het ev21gapv-cookie 28 dagen na de laatste set zou zijn verlopen.

```js
s.eVar21 = s.getAndPersistValue(s.eVar21,"ev21gapv",28);
```

### Voorbeeld 6

Met de volgende code wordt eVar30 gelijk gesteld aan &quot;shopping&quot;.  Vervolgens wordt het s_gapv-cookie, dat aan het einde van de browsersessie vervalt, ingesteld op de waarde van s.eVar30 (dus &quot;winkelen&quot;).  Vervolgens wordt s.eVar30 ingesteld op de waarde van het s_gapv-cookie (de aanroep getAndPersistValue retourneert de waarde van het s_gapv-cookie, die in dit geval winkelen is).

```js
s.eVar30 = "shopping";
s.eVar30 = s.getAndPersistValue(s.eVar30);
```

Als s.eVar30 niet aan een expliciete waarde op om het even welke extra pagina&#39;s wordt geplaatst die tijdens de zitting worden gezien maar (in doPlugins) via de volgende code wordt geplaatst..

```js
s.eVar30 = s.getAndPersistValue(s.eVar30);
```

...s.eVar30 wordt ingesteld op &quot;shopping&quot; (d.w.z. de persistentie van de s_gapv cookie)

## Versiehistorie

### 2.0 (16 april 2018)

* Puntrelease (kleinere codegrootte)
* Als u 0 in het `ex` argument doorgeeft, verloopt de bewerking nu na 30 minuten inactiviteit in plaats van na afloop van de browsersessie.

### 1.0 (18 januari 2016)

* Eerste release.
