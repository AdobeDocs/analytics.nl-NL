---
title: tl
description: Verzend een verbinding het volgen vraag aan Adobe.
feature: Variables
exl-id: 470662b2-ce07-4432-b2d5-a670fbb77771
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 0%

---

# tl

De `tl()` Deze methode is een belangrijk kernonderdeel van Adobe Analytics. Het neemt alle variabelen die van Analytics op de pagina worden bepaald, compileert hen in een beeldverzoek, en verzendt die gegevens naar de servers van de Adobe- gegevensinzameling. Het werkt op dezelfde manier als de [`t()`](t-method.md) Deze methode verhoogt de paginaweergaven echter niet. Het is handig voor het bijhouden van koppelingen en andere elementen die niet als een volledige pagina worden geladen.

Indien [`trackDownloadLinks`](../config-vars/trackdownloadlinks.md) of [`trackExternalLinks`](../config-vars/trackexternallinks.md) worden ingeschakeld, roept AppMeturement automatisch de `tl()` methode voor het verzenden van de downloadkoppeling en het afsluiten van koppelingsvolggegevens. Als uw organisatie liever meer controle heeft over de koppelingen en het gedrag ervan, kunt u de `tl()` handmatig. Aangepaste koppelingen kunnen alleen handmatig worden bijgehouden.

## Aanroep voor bijhouden van koppelingen met tags in Adobe Experience Platform

De UI van de Inzameling van Gegevens heeft een specifieke plaats reeks een verbinding het volgen vraag.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste eigenschap.
1. Ga naar de [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
1. Onder [!UICONTROL Actions], klikt u op het pictogram &#39;+&#39;
1. Stel de [!UICONTROL Extension] en de [!UICONTROL Action Type] om baken te verzenden.
1. Klik op de knop `s.tl()` keuzerondje.

U kunt geen optionele argumenten instellen in de gebruikersinterface voor gegevensverzameling.

## s.tl()-methode in AppMeturement en aangepaste code-editor

Roep de `s.tl()` methode wanneer u een volgende vraag naar Adobe wilt verzenden.

```js
s.tl([Link object],[Link type],[Link name],[Override variable]);
```

### Koppelingsobject (vereist)

Het argument voor het koppelingsobject bepaalt of de browser tot 500 ms wacht voordat er vanaf de pagina wordt genavigeerd. Als een verzoek om een afbeelding eerder dan 500 ms wordt verzonden, navigeert de pagina direct naar de aangeklikte koppeling.

>[!NOTE]
>
>AppMeasurement schakelt automatisch het [`useBeacon`](../config-vars/usebeacon.md) variabele voor exit links, waardoor dit argument niet langer nodig is in moderne browsers. Dit argument werd vaker gebruikt in vorige versies van AppMeasurement.

* `this`: Wacht tot maximaal 500 ms om AppMeasurement tijd te geven om een verzoek om een afbeelding te verzenden. Standaardwaarde.
* `true`: Wacht niet.

```JavaScript
// Include a 500ms delay with an exit link
s.tl(this,"e","Example exit link");

// Do not include a 500ms delay with an exit link
s.tl(true,"e","Example exit link");
```

### Koppelingstype (vereist)

Het koppelingstype argument is een enig-karakterkoord dat het type van verbinding het volgen vraag bepaalt. Er zijn drie geldige waarden.

* `o`: De koppeling is een [Aangepaste koppeling](/help/components/dimensions/custom-link.md).
* `d`: De koppeling is een [Koppeling downloaden](/help/components/dimensions/download-link.md).
* `e`: De koppeling is een [Koppeling afsluiten](/help/components/dimensions/exit-link.md).

```js
// Send a custom link
s.tl(true,"o","Example custom link");

// Send a download link
s.tl(true,"d","Example download link");

// Send an exit link
s.tl(true,"e","Example exit link");
```

### Koppelingsnaam (aanbevolen)

Het argument van de verbindingsnaam is een koord dat het verbinding volgende afmetingspunt bepaalt. Wanneer u de [Aangepaste koppeling](/help/components/dimensions/custom-link.md), [Koppeling downloaden](/help/components/dimensions/download-link.md), of [Koppeling afsluiten](/help/components/dimensions/exit-link.md) afmetingen in het rapporteren, bevat dit koord het afmetingspunt. Als dit argument niet is ingesteld, wordt [linkURL](../config-vars/linkurl.md) variable wordt gebruikt.

```js
// When using the Download link dimension, this method call increases the occurrences metric for "Sea turtle PDF report" by 1.
s.tl(true,"d","Sea turtle PDF report");
```

### Variabele overschrijvingen (optioneel)

Laat u veranderlijke waarden voor één enkele vraag veranderen. Zie [variabele overschrijvingen](../../js/overrides.md) voor meer informatie .

```js
var y = new Object();
y.eVar1 = "Override value";
y.linkTrackVars = "eVar1";
s.tl(true,"o","Example custom link",y);
```

## Voorbeelden en gebruiksgevallen

Verzend een basisverbinding het volgen vraag direct binnen een verbinding van HTML:

```HTML
<a href="example.html" onClick="s.tl(true,'o','Example link');">Click here</a>
```

Gebruik JavaScript om een basisvraag van het verbinden het volgen te maken gebruikend methodeargumenten:

```JavaScript
s.tl(true,"o","Example link");
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

Indien `trackDownloadLinks` of `trackExternalLinks` wordt toegelaten, maakt AppMeturement automatisch een verbinding volgende vraag als de correcte filters aanpassen. Als u ook handmatig `s.tl()` voor deze koppeling kunt u dubbele gegevens naar Adobe verzenden. Met dubbele gegevens worden de rapportnummers opgevoerd en minder nauwkeurig gemaakt.

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
