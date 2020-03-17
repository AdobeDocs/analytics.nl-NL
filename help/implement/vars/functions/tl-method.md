---
title: tl
description: Stuur een koppelingenvolgvraag naar Adobe.
translation-type: tm+mt
source-git-commit: 8494e8bb08b45006b357dd114e6bf9507f0cd54a

---


# tl

De `tl` methode is een belangrijk basisonderdeel van Adobe Analytics. Alle analytische variabelen die op de pagina zijn gedefinieerd, worden gecompileerd tot een verzoek om een afbeelding en die gegevens worden naar Adobe-servers voor gegevensverzameling verzonden. De methode werkt op dezelfde manier als de `t` methode, maar met deze methode worden de paginaweergaven niet vergroot. Het is handig voor het bijhouden van koppelingen en andere elementen die niet als een volledige pagina worden geladen.

Als `trackDownloadLinks` of `trackExternalLinks` worden toegelaten, roept AppMeasurement automatisch de `tl` methode om downloadverbinding te verzenden en verbinding het volgen gegevens weg te gaan. Als uw organisatie er de voorkeur aan geeft meer controle te hebben over de koppelingen en hun gedrag, kunt u de `tl` methode handmatig aanroepen. Aangepaste koppelingen kunnen alleen handmatig worden bijgehouden.

## Aanroep voor het bijhouden van koppelingen in Adobe Experience Platform Starten

De lancering heeft een specifieke plaats plaatste een verbinding volgende vraag.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
1. Klik onder [!UICONTROL Actions]op het pictogram ‘+’
1. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op Adobe Analytics en de knop [!UICONTROL Action Type] To Send Beacon.
1. Klik op het `s.tl()` keuzerondje.

U kunt geen optionele argumenten instellen in Launch.

## s.tl()-methode in de aangepaste code-editor van AppMeasurement en Launch

Roep de `s.tl()` methode aan wanneer u een volgende vraag naar Adobe wilt verzenden.

```js
s.tl();
```

Optioneel accepteert deze methode verschillende argumenten:

```js
s.tl([Link object],[Link type],[Link name],[Override variable]);
```

### Object Koppelen

Het argument voor het koppelingsobject bepaalt of de browser tot 500 ms wacht voordat er vanaf de pagina wordt genavigeerd. Als een verzoek om een afbeelding eerder dan 500 ms wordt verzonden, navigeert de pagina direct naar de aangeklikte koppeling.

> [!NOTE] AppMeasurement laat automatisch de `useBeacon` variabele voor uitgangsverbindingen toe, die dit argument maken niet meer nodig in moderne browsers. Dit argument werd vaker gebruikt in vorige versies van AppMeasurement.

* `this`: Wacht tot maximaal 500 ms om AppMeasurement tijd te geven om een verzoek om een afbeelding te verzenden. Standaardwaarde.
* `true`: Wacht niet.

```JavaScript
// Include a 500ms delay
s.tl(this);

// Do not include a 500ms delay
s.tl(true);
```

### Type koppeling

Het koppelingstype argument is een single-letter koord dat het type van verbinding het volgen vraag bepaalt. Dit is hetzelfde als het instellen van de `linkType` variabele.

```js
// Send a custom link
s.tl(true,"o");

// Send a download link
s.tl(true,"d");

// Send an exit link
s.tl(true,"e");
```

### Koppelingsnaam

Het argument van de verbindingsnaam is een koord dat de de afmetingswaarde van de verbinding het volgen bepaalt. Dit is hetzelfde als het instellen van de `linkName` variabele.

```js
s.tl(true,"d","Example download link");
```

### Variabele overschrijvingen

Laat u veranderlijke waarden voor één enkele vraag veranderen. Zie [variabele overschrijvingen](../../js/overrides.md) voor meer informatie.

```js
var y = new Object();
y.eVar1 = "Override value";
y.linkTrackVars = "eVar1";
s.tl(true,"o","Example custom link",y);
```

## Voorbeelden en gebruiksgevallen

Verzend een basisvraag van het verbinden direct binnen een verbinding van HTML:

```HTML
<a href="example.html" onClick="s.tl(true,'o','Example link');">Click here</a>
```

Gebruik JavaScript om een basisvraag van het verbinden het volgen te maken gebruikend methodeargumenten:

```JavaScript
s.tl(true,"o","Example link");
```

Gebruik JavaScript om dezelfde basisaanroep voor het bijhouden van koppelingen te maken met behulp van afzonderlijke variabelen:

```js
s.linkType = "o";
s.linkName = "Example link";
s.tl();
```

### Koppelingen bijhouden aanroepen maken binnen een aangepaste functie

U kunt koppelingsvolgcode verenigen in een zelfstandige JavaScript-functie die op de pagina of in een gekoppeld JavaScript-bestand is gedefinieerd. De vraag kan dan in de onClick functie van elke verbinding worden gemaakt. Stel het volgende in een JavaScript-bestand in:

```JavaScript
function trackClickInteraction(name){
  s.linkTrackVars = "eVar1,eVar2";
  s.eVar1 = name;
  s.eVar2 = s.pageName;
  s.tl(true,"o",name);
}
```

Vervolgens kunt u de functie aanroepen wanneer u een bepaalde koppeling wilt bijhouden:

```HTML
<!-- Use wherever you want to track links -->
<a href="example.html" onClick="trackClickInteraction('Example link');">Click here</a>
```

### Dubbele koppelingen niet bijhouden

Als `trackDownloadLinks` of `trackExternalLinks` worden toegelaten, maakt AppMeasurement automatisch een verbinding volgende vraag als de correcte filters aanpassen. Als u ook handmatig `s.tl()` voor deze koppeling klikt, kunt u dubbele gegevens naar Adobe verzenden. Met dubbele gegevens worden de rapportnummers opgevoerd en minder nauwkeurig gemaakt.

De volgende functie verzendt bijvoorbeeld twee aanroepen voor het bijhouden van koppelingen naar dezelfde link (handmatige en automatische downloadkoppelingen):

```JavaScript
function trackDownload(obj) {
  s.tl(obj,"d","Example PDF download");
}
```

U kunt helpen dubbele verbinding het volgen vraag verhinderen door de volgende gewijzigde functie te gebruiken. Het controleert eerst of een verbindingsvoorwerp bestaat, en verzendt slechts een handvraag van het verbinden het volgen als het verbindingsvoorwerp een lege koord is.

```JavaScript
function linkCode(obj) {
  var lt = obj.href != null ? s.lt(obj.href) : "";
  if (lt=="") {
    s.tl(obj,"d","Example PDF download");
  }
}
```
