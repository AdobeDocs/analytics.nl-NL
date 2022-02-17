---
title: abort
description: De abortvariabele is een booleaanse waarde die voorkomt dat een hit wordt verzonden naar Adobe-gegevensverzamelingsservers.
feature: Variables
exl-id: e4e25a89-272b-4444-b52b-c7fe2478ff30
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---

# afbreken

De `abort` De variabele is een booleaanse waarde die kan verhinderen dat de volgende volgende volgvraag naar Adobe wordt verzonden.

## De abortvariabele gebruiken in de gebruikersinterface voor gegevensverzameling in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## De syntaxis van de Meting van de app en de douanecode redacteur in de UI van de Inzameling van Gegevens

De `abort` variable is a boolean. De standaardwaarde is `false`.

* Indien ingesteld op `true`, de volgende volgende volgende volgende volgvraag ([`t()`](../functions/t-method.md) of [`tl()`](../functions/tl-method.md)) verzendt geen gegevens naar Adobe.
* Indien ingesteld op `false` of niet gedefinieerd, heeft deze variabele geen effect.

```js
s.abort = true;
```

>[!NOTE]
>
>De `abort` variabele herstelt naar `false` na elke volgende vraag. Als u volgende het volgen vraag op de zelfde pagina moet afbreken, plaats `abort` tot `true` opnieuw.

## Voorbeeld

De `abort` kan worden ingesteld in het dialoogvenster [`doPlugins()`](../functions/doplugins.md) -functie. Dit is de laatste functie die wordt uitgevoerd voordat een afbeeldingsaanvraag naar Adobe wordt verzonden.

```js
s.doPlugins = function(s) {
     s.campaign = s.Util.getQueryParam("cid");
     if ((!s.campaign) && (!s.events)) {
          s.abort = true;
     }
};
```

U kunt de logica centraliseren die u gebruikt om activiteit te identificeren die u niet wilt volgen, zoals sommige douaneverbindingen of externe verbindingen in vertoningsadvertenties.
