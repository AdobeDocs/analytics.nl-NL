---
title: Nummers Suite
description: Cijfers maken en manipuleren voor gebruik in andere JavaScript-variabelen.
feature: Appmeasurement Implementation
exl-id: 7af88dce-baf3-4581-b5b6-0d6e41922266
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 0%

---

# Adobe-insteekmodule: Numbers Suite

{{plug-in}}

De Numbers Suite bevat een aantal JavaScript-functies. Deze bevat de volgende plug-ins:

* **`zeroPad`**: voeg een specifiek aantal nullen aan het begin van een getal toe. Deze insteekmodule is handig als een variabele een bepaald aantal cijfers nodig heeft, bijvoorbeeld als u werkt met JavaScript-datumobjecten en de maand en dag van een datum wilt opmaken met twee cijfers in plaats van slechts één cijfer. Bijvoorbeeld `01/09/2020` in plaats van `1/9/2020` .
* **`randomNumber`**: Genereer een willekeurig getal met een specifiek aantal cijfers. Deze plug-in is handig als u tags van derden implementeert en een willekeurig nummer voor het opbouwen van cache wilt.
* **`twoDecimals`**: Rond een getal af op de dichtstbijzijnde honderdste. Deze insteekmodule is handig voor valutadoeleinden, zodat u een getal kunt afronden naar een geldige valutawaarde.

## De insteekmodule installeren met de extensie Web SDK of Web SDK

Deze insteekmodule wordt nog niet ondersteund voor gebruik in de Web SDK.

## De insteekmodule installeren met de Adobe Analytics-extensie

Adobe biedt een extensie waarmee u veelgebruikte plug-ins kunt gebruiken in Adobe Analytics.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop [!UICONTROL Catalog]
1. De extensie [!UICONTROL Common Analytics Plugins] installeren en publiceren
1. Als u niet reeds hebt, creeer een regel geëtiketteerd &quot;Initialize stop-ins&quot;met de volgende configuratie:
   * Voorwaarde: geen
   * Event: Core - bibliotheek geladen (pagina boven)
1. Voeg een actie aan de bovengenoemde regel met de volgende configuratie toe:
   * Extensie: veelgebruikte plug-ins voor Analytics
   * Type handeling: Numbers Suite initialiseren
1. Sla de wijzigingen in de regel op en publiceer deze.

## Plug-in installeren met aangepaste code-editor

Als u niet de Gemeenschappelijke Insteekmodule van Analytics wilt gebruiken, kunt u de redacteur van de douanecode gebruiken.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste eigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder de extensie Adobe Analytics.
1. Vouw de accordeon [!UICONTROL Configure tracking using custom code] uit, zodat de knop [!UICONTROL Open Editor] zichtbaar wordt.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

## Plug-in installeren met AppMeasurement

Kopieer en plak de volgende code ergens in het AppMeasurement-bestand nadat het object Analytics tracking is geïnstantieerd (met [`s_gi`](../functions/s-gi.md) ). Door opmerkingen en versienummers van de code in uw implementatie te behouden, helpt Adobe bij het oplossen van mogelijke problemen.

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

De functie `zeroPad` gebruikt de volgende argumenten:

* **num** (vereist, geheel): Het aantal aan stootkussen. De functie rondt de waarde van dit argument af als het decimalen bevat.
* **knoop** (vereist, geheel): Het aantal cijfers in de definitieve terugkeerwaarde. Als het aantal cijfers dat moet worden gecompileerd minder is dan het aantal cijfers dat moet worden weergegeven, voegt de plug-in nullen toe aan het begin van het argument `num` .

De functie `randomNumber` gebruikt de volgende argumenten:

* **knoop** (facultatief, geheel): Het aantal cijfers in het willekeurige aantal dat u wilt produceren. De maximumwaarde is 17 cijfers. De standaardwaarde is 10 cijfers.

De functie `twoDecimals` gebruikt de volgende argumenten:

* **val** (vereist, aantal): Een aantal (dat door of een koord of aantalvoorwerp wordt vertegenwoordigd) dat u aan de dichtstbijzijnde honderdste wilt afronden.

## Retourneert

* De **zeroPad** functie keert een koord gelijk aan het `num` argument maar met een specifiek aantal nul terug aan het begin van zijn waarde wordt toegevoegd, die ervoor zorgt dat de terugkeerwaarde het correcte aantal cijfers heeft.
* De **randomNumber** functie keert een koord gelijk aan een willekeurig aantal met het gewenste aantal cijfers terug.
* De **twoDecimals** functie keert een aantalvoorwerp terug dat aan de dichtste honderdste wordt afgerond.

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
