---
title: Nummers Suite
description: Cijfers maken en manipuleren voor gebruik in andere JavaScript-variabelen.
feature: Variables
exl-id: 7af88dce-baf3-4581-b5b6-0d6e41922266
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 0%

---

# Adobe plug-in: Numbers Suite

{{plug-in}}

De Numbers Suite bevat een aantal JavaScript-functies. Deze bevat de volgende plug-ins:

* **`zeroPad`**: Voeg een specifiek aantal nullen toe aan het begin van een getal. Deze insteekmodule is handig als een variabele een bepaald aantal cijfers vereist, bijvoorbeeld als u werkt met JavaScript-datumobjecten en de maand en dag van een datum wilt opmaken met twee cijfers in plaats van slechts één cijfer. Bijvoorbeeld: `01/09/2020` in plaats van `1/9/2020`.
* **`randomNumber`**: Genereer een willekeurig getal met een specifiek aantal cijfers. Deze plug-in is handig als u tags van derden implementeert en een willekeurig nummer voor het opbouwen van cache wilt.
* **`twoDecimals`**: Rond een getal af op het honderdste van de kast. Deze insteekmodule is handig voor valutadoeleinden, zodat u een getal kunt afronden naar een geldige valutawaarde.

## De insteekmodule installeren met de extensie Web SDK of Web SDK

Deze plug-in wordt nog niet ondersteund voor gebruik in de Web SDK.

## De insteekmodule installeren met de Adobe Analytics-extensie

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken met Adobe Analytics.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop [!UICONTROL Catalog] knop
1. Installeer de [!UICONTROL Common Analytics Plugins] extension
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: geen
   * Event: Core - bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: veelgebruikte plug-ins voor Analytics
   * Type handeling: Numbers Suite initialiseren
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met aangepaste code-editor

Als u niet de Gemeenschappelijke Insteekmodule van Analytics wilt gebruiken, kunt u de redacteur van de douanecode gebruiken.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder de extensie Adobe Analytics.
1. Breid uit [!UICONTROL Configure tracking using custom code] accordion, die de [!UICONTROL Open Editor] knop.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

## Plug-in installeren met AppMeasurement

Kopieer en plak de volgende code ergens in het bestand AppMeasurement nadat het object Analytics tracking is geïnstantieerd (met [`s_gi`](../functions/s-gi.md)). Door opmerkingen en versienummers van de code in uw implementatie te behouden, kunt u Adoben met het oplossen van mogelijke problemen.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: zeroPad v1.0 */
function zeroPad(num,nod){num=parseInt(num);nod=parseInt(nod);if(isNaN(num)||isNaN(nod))return"";var c=nod-num.toString().length+ 1;return Array(+(0<c&&c)).join("0")+num};

/* Adobe Consulting Plugin: randomNumber v2.0 (zeroPad plug-in optional)*/
function randomNumber(nod){nod="number"===typeof nod?17>Math.abs(nod)?Math.round(Math.abs(nod)):17:10;for(var a="1",c=0;c<nod;c++) a+="0";a=Number(a);a=Math.floor(Math.random().toFixed(nod)*a)+"";a.length!==nod&&"undefined"!==typeof zeroPad&&(a=zeroPad(a,nod)); return a};

/* Adobe Consulting Plugin: twoDecimals v1.0 */
function twoDecimals(v){return"undefined"===typeof v||void 0===v||isNaN(v)?0:Number(Number(v).toFixed(2))};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-ins gebruiken

De `zeroPad` function gebruikt de volgende argumenten:

* **num** (required, integer): Het getal dat moet worden gecompileerd. De functie rondt de waarde van dit argument af als het decimalen bevat.
* **knip** (vereist, geheel getal): Het aantal cijfers in de uiteindelijke geretourneerde waarde. Als het aantal cijfers dat moet worden gecomprimeerd kleiner is dan het aantal cijfers dat moet worden gedraaid, worden er door de plug-in nullen aan het begin van het blok toegevoegd `num` argument.

De `randomNumber` function gebruikt de volgende argumenten:

* **knip** (optioneel, geheel getal): Het aantal cijfers in het willekeurige getal dat u wilt genereren. De maximumwaarde is 17 cijfers. De standaardwaarde is 10 cijfers.

De `twoDecimals` function gebruikt de volgende argumenten:

* **val** (vereist, getal): Een getal (vertegenwoordigd door een tekenreeks of een object Number) dat u naar het dichtstbijzijnde honderdste wilt afronden.

## Retourneert

* De **zeroPad** functie retourneert een tekenreeks die gelijk is aan de `num` argument maar met een specifiek aantal nullen toegevoegd aan het begin van zijn waarde, die ervoor zorgt dat de terugkeerwaarde het correcte aantal cijfers heeft.
* De **randomNumber** Deze functie retourneert een tekenreeks die gelijk is aan een willekeurig getal met het gewenste aantal cijfers.
* De **tweeDecimals** function retourneert een Number-object afgerond naar het dichtstbijzijnde honderdste.

## Voorbeelden van aanroepen

### voorbeelden van zeroPad

```js
s.eVar25 = zeroPad(25.5562, 5) //sets eVar25 equal to "00025"

s.prop1 = zeroPad(25, 1) //sets prop1 equal to "25"

s.prop1 = zeroPad(232425235,23) //sets prop1 equal to "00000000000000232425235"
```

### randomNumber-voorbeelden

```js
s.eVar65 = randomNumber(15) //sets eVar65 equal to "721759731750342" or some other random 15-digit number

randomNumber() //returns a random 10-digit number but is useless since this isn't used in an expression

var j = randomNumber(35) //sets a variable named j equal to "15476068651810060" or another random 17-digit number
```

### twee decimale voorbeelden

```js
s.events = "event10=" + twoDecimals("85.4827128694") //sets s.events="event10=85.48"

var fivehundredthirtytwo = twoDecimals(532.000000001) //sets the variable fivehundredthirtytwo equal to 532

s.eVar65 = twoDecimals("672132.9699736457") //sets s.eVar65 equal to 672132.97
```

## Versiehistorie

### 1.0 (25 mei 2019)

* Eerste release.
