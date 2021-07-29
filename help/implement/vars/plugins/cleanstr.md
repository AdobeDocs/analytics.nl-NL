---
title: cleanStr
description: Alle overbodige tekens uit een tekenreeks verwijderen of vervangen.
exl-id: d699dcd4-5e0a-40d3-b345-e5b1a077d393
source-git-commit: 9a70d79a83d8274e17407229bab0273abbe80649
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---

# Adobe-plug-in: cleanStr

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `cleanStr`-plug-in verwijdert of vervangt u alle overbodige tekens uit een tekenreeks, zoals HTML-labeltekens, extra witruimten, tabs en geretourneerde nieuwe regels/onderkomens. Het vervangt ook linker/juiste enkele citaten (`‘` en `’`) met rechte enige citaten (`'`). Adobe raadt u aan deze plug-in te gebruiken als u overbodige tekens wilt verwijderen uit variabele waarden en de functie &#39;Tekst opschonen&#39; in Adobe Experience Platform voldoet niet aan de implementatievereisten. Deze insteekmodule is niet nodig als de verzamelde gegevens geen overbodige tekens bevatten of als de functie &#39;Tekst opschonen&#39; in de gebruikersinterface voor gegevensverzameling voldoende is.

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
   * Type handeling: CleanStr initialiseren
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
/* Adobe Consulting Plugin: cleanStr v2.0 (No Prerequisites Required) */
function cleanStr(str){var a=str;if("-v"===a)return{plugin:"cleanStr",version:"2.0"};a:{if("undefined"!==typeof window.s_c_il){var b=0;for(var c;b<window.s_c_il.length;b++)if(c=window.s_c_il[b],c._c&&"s_c"===c._c){b=c;break a}}b=void 0}"undefined"!==typeof b&&(b.contextData.cleanStr="2.0");if("string"===typeof a){a=a.replace(/<\/?[^>]+(>|$)/g,"");a=a.trim();a=a.replace(/[\u2018\u2019\u201A]/g,"'");a=a.replace(/\t+/g,"");for(a=a.replace(/[\n\r]/g," ");-1<a.indexOf("  ");)a=a.replace(/\s\s/g," ");return a}return""}
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De methode `cleanStr` gebruikt de volgende argumenten:

* **`str`** (vereist, tekenreeks): De waarde die u wilt verwijderen voor HTML-codering, extra witruimte, tabs of andere overbodige tekens.

De methode retourneert de waarde van het argument `str`, waarbij alle overbodige tekens zijn verwijderd.

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

### Voorbeeld 3

Indien...

```js
s.eVar1 = "»∙∙this∙∙is∙a∙∙»∙messy»string∙∙∙∙"
```

...en de volgende code wordt uitgevoerd...

```js
cleanStr(s.eVar1)
```

...de uiteindelijke waarde van s.eVar1 blijft :

```js
"»∙∙this∙∙is∙a∙∙»∙messy»string∙∙∙∙"
```

Als u de plug-in helemaal zelf uitvoert (zonder de geretourneerde waarde aan een variabele toe te wijzen), wordt de variabele die door het str-argument is doorgegeven, niet opnieuw ingesteld.

## Versiehistorie

### 2.0 (19 maart 2021)

* Versienummer toegevoegd als contextgegevens.

### 1.0 (15 april 2018)

* Eerste release.
