---
title: abort
description: De abortvariabele is een booleaanse waarde die voorkomt dat een hit wordt verzonden naar Adobe-gegevensverzamelingsservers.
exl-id: e4e25a89-272b-4444-b52b-c7fe2478ff30
source-git-commit: 3986084eaab81842b6ea0dbabc7bdb78e39f887a
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---

# afbreken

De `abort` variabele is een booleaanse waarde die kan verhinderen dat de volgende volgende volgende volgende vraag wordt verzonden naar Adobe.

## De abortvariabele gebruiken in de gebruikersinterface voor gegevensverzameling in Adobe Experience Platform

Er is geen specifiek gebied in de Inzameling van Gegevens UI om deze variabele te gebruiken. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## De syntaxis van de Meting van de app en de douanecode redacteur in de UI van de Inzameling van Gegevens

De variabele `abort` is een booleaanse waarde. De standaardwaarde is `false`.

* Indien ingesteld op `true`, verzendt de volgende volgende volgende volgende aanroep ([`t()`](../functions/t-method.md) of [`tl()`](../functions/tl-method.md)) geen gegevens naar Adobe.
* Indien ingesteld op `false` of niet gedefinieerd, heeft deze variabele geen effect.

```js
s.abort = true;
```

>[!NOTE]
>
>De `abort` variabele stelt aan `false` na elke volgende vraag terug. Als u verdere het volgen vraag op de zelfde pagina moet afbreken, plaats `abort` aan `true` opnieuw.

## Voorbeeld

De variabele `abort` kan in de functie [`doPlugins()`](../functions/doplugins.md) worden geplaatst, die de laatste functie is die moet lopen alvorens een beeldverzoek wordt verzonden naar Adobe.

```js
s.doPlugins = function(s) {
     s.campaign = s.Util.getQueryParam("cid");
     if ((!s.campaign) && (!s.events)) {
          s.abort = true;
     }
};
```

U kunt de logica centraliseren die u gebruikt om activiteit te identificeren die u niet wilt volgen, zoals sommige douaneverbindingen of externe verbindingen in vertoningsadvertenties.
