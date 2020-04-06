---
title: cleanStr
description: Alle overbodige tekens uit een tekenreeks verwijderen of vervangen.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Adobe-insteekmodule: cleanStr

>[!IMPORTANT] Deze plug-in wordt geleverd door Adobe Consulting als een hoffelijkheid om u te helpen meer waarde te krijgen van Adobe Analytics. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `cleanStr` insteekmodule verwijdert of vervangt u alle overbodige tekens uit een tekenreeks, zoals tekens van HTML-tags, extra witruimten, tabs en regeleinden. Het vervangt ook enkele aanhalingstekens links/rechts (`‘` en `’`) door rechte enkele aanhalingstekens (`'`). Adobe raadt u aan deze plug-in te gebruiken als u overbodige tekens wilt verwijderen uit variabele waarden en de functie &#39;Tekst opschonen&#39; in Launch voldoet niet aan de implementatievereisten. Deze plug-in is niet nodig als de verzamelde gegevens geen overbodige tekens bevatten of als de functie &#39;Tekst opschonen&#39; in Launch voldoende is.

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
   * Type handeling: CleanStr initialiseren
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
/* Adobe Consulting Plugin: cleanStr v1.0 */
function cleanStr(str){if("string"===typeof str){str=str.replace(/<\/?[^>]+(>|$)/g,"");str=str.trim(); str=str.replace(/[\u2018\u2019\u201A]/g,"'");str=str.replace(/\t+/g,"");for(str=str.replace(/[\n\r]/g," ");-1<str.indexOf("  ");)str=str.replace(/\s\s/g," ");return str}return""};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De `cleanStr` methode gebruikt de volgende argumenten:

* **`str`** (vereist, tekenreeks): De waarde die u wilt verwijderen voor HTML-codering, extra witruimte, tabs of andere overbodige tekens.

De methode retourneert de waarde van het `str` argument, waarbij alle overbodige tekens zijn verwijderd.

## Voorbeelden

### Voorbeeld 1

Stel het volgende in (waar de punten spaties vertegenwoordigen en de pijlen tabtekens zijn

```js
s.eVar1 = "»∙∙this∙∙is∙a∙∙»∙messy»string∙∙∙∙"
```

Wanneer u de volgende code uitvoert...

```js
s.eVar1 = cleanStr(s.eVar1)
```

...eVar1 wordt ingesteld op gelijk aan &quot;this is a message string&quot; (met alle extra spaties en alle tabtekens verwijderd)

### Voorbeeld 2

Indien...

```js
s.eVar1 = "»∙∙this∙∙is∙a∙∙»∙messy»string∙∙∙∙"
```

...en de volgende code wordt uitgevoerd...

```js
cleanStr(s.eVar1)
```

...de uiteindelijke waarde van s.eVar1 blijft:

```js
"»∙∙this∙∙is∙a∙∙»∙messy»string∙∙∙∙"
```

Als u de plug-in helemaal zelf uitvoert (zonder de geretourneerde waarde aan een variabele toe te wijzen), wordt de variabele die door het str-argument is doorgegeven, niet opnieuw ingesteld.

## Versiehistorie

### 1.0 (15 april 2018)

* Eerste release.
