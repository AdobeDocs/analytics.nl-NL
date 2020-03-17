---
title: afbreken
description: De variabele Afbreken is een Booleaanse waarde die voorkomt dat een hit wordt verzonden naar Adobe-servers voor gegevensverzameling.
translation-type: tm+mt
source-git-commit: f769da139d9890fd736a9b277934b11aa131e166

---


# afbreken

De `abort` variabele is een Booleaanse waarde die kan voorkomen dat de volgende volgaanroep naar Adobe wordt verzonden.

## De abortvariabele gebruiken in Adobe Experience Platform Launch

Er is geen specifiek veld in Launch om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## Syntaxis en aangepaste code-editor voor appMeturement in Launch

De `abort` variabele is een booleaanse waarde. De standaardwaarde is `false`.

* Indien ingesteld op `true`, worden bij de volgende aanroep (`t()` of `tl()`) geen gegevens naar Adobe verzonden.
* Indien ingesteld op `false` of niet gedefinieerd, heeft deze variabele geen effect.

```js
s.abort = true;
```

> [!NOTE] De `abort` variabele herstelt aan `false` na elke volgende vraag. Als u verdere het volgen vraag op de zelfde pagina moet afbreken, reeks `abort` aan `true` opnieuw.

## Voorbeeld

De `abort` variabele kan in de `doPlugins()` functie worden ingesteld. Dit is de laatste functie die moet worden uitgevoerd voordat een afbeeldingsaanvraag naar Adobe wordt verzonden.

```js
s.doPlugins = function(s) {
     s.campaign = s.Util.getQueryParam("cid");
     if ((!s.campaign) && (!s.events)) {
          s.abort = true;
     }
};
```

U kunt de logica centraliseren die u gebruikt om activiteit te identificeren die u niet wilt volgen, zoals sommige douaneverbindingen of externe verbindingen in vertoningsadvertenties.
