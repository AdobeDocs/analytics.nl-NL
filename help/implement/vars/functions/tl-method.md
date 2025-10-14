---
title: tl
description: Stuur een koppelingenvolgvraag naar Adobe.
feature: Appmeasurement Implementation
exl-id: 470662b2-ce07-4432-b2d5-a670fbb77771
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 0%

---

# tl

De methode `tl()` is een belangrijke kerncomponent voor Adobe Analytics. Alle analysevariabelen die op de pagina zijn gedefinieerd, worden gecompileerd tot een verzoek om een afbeelding en die gegevens worden naar Adobe-servers voor gegevensverzameling verzonden. Deze methode werkt op ongeveer dezelfde manier als de methode [`t()`](t-method.md) , maar bij deze methode worden de paginaweergaven niet vergroot. Het is handig voor het bijhouden van koppelingen en andere elementen die niet als een volledige pagina worden geladen.

Als [`trackDownloadLinks`](../config-vars/trackdownloadlinks.md) of [`trackExternalLinks`](../config-vars/trackexternallinks.md) is ingeschakeld, roept AppMeasurement automatisch de methode `tl()` aan om de downloadkoppeling te verzenden en de volggegevens van de koppeling af te sluiten. Als uw organisatie liever meer controle heeft over de koppelingen en het gedrag ervan, kunt u de methode `tl()` handmatig aanroepen. U kunt aangepaste koppelingen alleen handmatig bijhouden.

## Koppelingen bijhouden met de Web SDK

Het Web SDK maakt geen onderscheid tussen de vraag van de paginamening en verbinding het volgen vraag; allebei gebruiken het `sendEvent` bevel.

Als u een XDM-object gebruikt en Adobe Analytics een bepaalde gebeurtenis wilt tellen als een aanroep voor het bijhouden van koppelingen, moet u ervoor zorgen dat uw XDM-gegevens:

* Koppelingsnaam: toegewezen aan `xdm.web.webInteraction.name` .
* URL van koppeling: toegewezen aan `xdm.web.webInteraction.URL` .
* Koppelingstype: toegewezen aan `xdm.web.webInteraction.type` . Geldige waarden zijn `other` (Aangepaste koppelingen), `download` (Koppelingen downloaden) en `exit` (Koppelingen afsluiten).

```js
alloy("sendEvent", {
  "xdm": {
    "web": {
      "webInteraction": {
        "name": "My Custom Link",
        "URL": "https://example.com",
        "type": "other"
      }
    }
  }
});
```

Als u een gegevensobject gebruikt en Adobe Analytics een bepaalde gebeurtenis wilt laten tellen als een aanroep voor het bijhouden van koppelingen, moet u ervoor zorgen dat het gegevensobject de volgende gegevens bevat:

* Koppelingsnaam: toegewezen aan `data.__adobe.analytics.linkName` .
* URL van koppeling: toegewezen aan `data.__adobe.analytics.linkURL` .
* Koppelingstype: toegewezen aan `data.__adobe.analytics.linkType` . Geldige waarden zijn `o` (Aangepaste koppelingen), `d` (Koppelingen downloaden) en `e` (Koppelingen afsluiten).

```js
alloy("sendEvent", {
  "data": {
    "__adobe": {
      "analytics": {
        "linkName": "My custom link",
        "linkURL": "https://example.com",
        "linkType": "o"
      }
    }
  }
});
```

## Koppelingen bijhouden met de Adobe Analytics-extensie

De extensie Adobe Analytics heeft een specifieke locatie om een aanroep voor het bijhouden van koppelingen in te stellen.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Ga naar het tabblad [!UICONTROL Rules] en klik vervolgens op de gewenste regel (of maak een regel).
1. Klik onder [!UICONTROL Actions] op de gewenste actie of klik op het pictogram **&#39;+&#39;** om een actie toe te voegen.
1. Stel de vervolgkeuzelijst [!UICONTROL Extension] in op **[!UICONTROL Adobe Analytics]** en de vervolgkeuzelijst op [!UICONTROL Action Type] op **[!UICONTROL Send Beacon]** .
1. Klik op het keuzerondje `s.tl()` .

U kunt geen optionele argumenten instellen in de extensie Analytics.

## s.tl()-methode in AppMeasurement en de aangepaste code-editor van de extensie Analytics

Roep de methode `s.tl()` aan wanneer u een volgende aanroep naar Adobe wilt verzenden.

```js
s.tl([Link object],[Link type],[Link name],[Override variable]);
```

### Koppelingsobject (vereist)

Het argument voor het koppelingsobject bepaalt of de browser tot 500 ms wacht voordat er vanaf de pagina wordt genavigeerd. Als een verzoek om een afbeelding eerder dan 500 ms wordt verzonden, navigeert de pagina direct naar de aangeklikte koppeling.

>[!NOTE]
>
>AppMeasurement schakelt de variabele [`useBeacon`](../config-vars/usebeacon.md) automatisch in voor afsluitkoppelingen, waardoor dit argument niet langer nodig is in moderne browsers. Dit argument werd vaker gebruikt in eerdere versies van AppMeasurement.

* `this`: wacht tot 500 ms om AppMeasurement tijd te geven om een afbeeldingsaanvraag te verzenden. Standaardwaarde.
* `true`: wacht niet.

```JavaScript
// Include a 500ms delay with an exit link
s.tl(this,"e","Example exit link");

// Do not include a 500ms delay with an exit link
s.tl(true,"e","Example exit link");
```

### Koppelingstype (vereist)

Het koppelingstype argument is een enig-karakterkoord dat het type van verbinding het volgen vraag bepaalt. Er zijn drie geldige waarden.

* `o`: De verbinding is de verbinding van de a [&#x200B; Douane &#x200B;](/help/components/dimensions/custom-link.md).
* `d`: De verbinding is de verbinding van de a [&#x200B; Download &#x200B;](/help/components/dimensions/download-link.md).
* `e`: De verbinding is een [&#x200B; verbinding van de Uitgang &#x200B;](/help/components/dimensions/exit-link.md).

```js
// Send a custom link
s.tl(true,"o","Example custom link");

// Send a download link
s.tl(true,"d","Example download link");

// Send an exit link
s.tl(true,"e","Example exit link");
```

### Koppelingsnaam (aanbevolen)

Het argument van de verbindingsnaam is een koord dat het verbinding volgende afmetingspunt bepaalt. Wanneer het gebruiken van de [&#x200B; Verbinding van de Douane &#x200B;](/help/components/dimensions/custom-link.md), [&#x200B; Verbinding van de Download &#x200B;](/help/components/dimensions/download-link.md), of [&#x200B; Verbinding van de Uitgang &#x200B;](/help/components/dimensions/exit-link.md) dimensies in het melden, bevat dit koord het afmetingspunt. Als dit argument niet wordt geplaatst, wordt de [&#x200B; linkURL &#x200B;](../config-vars/linkurl.md) variabele gebruikt.

```js
// When using the Download link dimension, this method call increases the occurrences metric for "Sea turtle PDF report" by 1.
s.tl(true,"d","Sea turtle PDF report");
```

### Variabele overschrijvingen (optioneel)

Laat u veranderlijke waarden voor één enkele vraag veranderen. Zie [&#x200B; veranderlijke met voeten treedt &#x200B;](../../js/overrides.md) voor meer informatie.

```js
var y = new Object();
y.eVar1 = "Override value";
y.linkTrackVars = "eVar1";
s.tl(true,"o","Example custom link",y);
```

## Voorbeelden en gebruiksgevallen

Verzend een basisvraag het volgen van verbindingen direct binnen een verbinding van HTML:

```HTML
<a href="example.html" onClick="s.tl(true,'o','Example link');">Click here</a>
```

JavaScript gebruiken om een eenvoudige aanroep voor het bijhouden van koppelingen te maken met behulp van methodeargumenten:

```JavaScript
s.tl(true,"o","Example link");
```

### Koppelingen bijhouden aanroepen maken binnen een aangepaste functie

U kunt code voor het bijhouden van koppelingen consolideren in een zelfstandige JavaScript-functie. Aanroepen kunnen vervolgens worden uitgevoerd in de functie `onClick` van elke koppeling. Stel het volgende in een JavaScript-bestand in:

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

>[!NOTE]
>Door de methode `tl()` indirect aan te roepen, kunt u Activity Map-overlayrapportage minder handig maken. U moet op elke koppeling klikken om de functie te registreren bij het koppelingselement. Activity Map-afmetingen in Workspace worden echter op dezelfde manier bijgehouden.

### Dubbele koppelingen niet bijhouden

Als `trackDownloadLinks` of `trackExternalLinks` zijn ingeschakeld, roept AppMeasurement automatisch een koppeling bij te houden op als de juiste filters overeenkomen. Als u ook handmatig `s.tl()` voor deze koppeling aanroept, kunt u dubbele gegevens naar Adobe verzenden. Met dubbele gegevens worden de rapportnummers opgevoerd en minder nauwkeurig gemaakt.

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

### De methode `tl()` gebruiken met Activity Map

Met de methode `tl()` kunt u aangepaste elementen bijhouden en de rendering van bedekkingen configureren voor dynamische inhoud. De `linkName` parameter wordt ook gebruikt om de [&#x200B; 2&rbrace; dimensie van de Verbinding van Activity Map &lbrace;te plaatsen.](/help/components/dimensions/activity-map-link.md)

Wanneer de methode `tl()` rechtstreeks wordt aangeroepen vanuit de klikgebeurtenis van het HTML-element, kan Activity Map een bedekking voor dat element weergeven wanneer de webpagina wordt geladen. Bijvoorbeeld:

```html
<a href="index.html" onclick="s.tl(this,'o','Example custom link');">Example link text</a>
```

Wanneer de methode `tl()` niet rechtstreeks wordt aangeroepen vanuit de klikgebeurtenis van het HTML-element, kan Activity Map alleen een bedekking weergeven nadat op dat element is geklikt. Bijvoorbeeld:

```html
<a href="index.html" onclick="someFn(event);">Example link text</a>
<script>
  function someFn (event) {
    s.tl(event.srcElement,'o','Example custom link');
  }
</script>
```
