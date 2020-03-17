---
title: dynamicAccountList
description: Bepaal logica op hoe uw implementatie zijn rapportreeks bepaalt.
translation-type: tm+mt
source-git-commit: ''

---


# s.dynamicAccountList

> [!IMPORTANT] Dynamische accounts worden alleen ondersteund met behulp van verouderde JavaScript-implementaties (H Code). Deze variabelen worden niet ondersteund in de huidige AppMeasurement-bibliotheken of Adobe Experience Platform Launch.

De `s.dynamicAccountList` variabele bepaalt dynamisch de waarde van `s_account`. Wanneer `dynamicAccountSelection` deze is ingesteld op `true`, wordt de `dynamicAccountMatch` variabele vergeleken met `dynamicAccountList`. Als een gelijke wordt gevonden, wordt de passende identiteitskaart van de rapportreeks gebruikt.

## Syntaxis

Deze variabele is een tekenreeks die automatisch door het JavaScript-bestand wordt geparseerd.

```JavaScript
s.dynamicAccountList = "[rsid]=[valuetomatch],[rsid2]=[valuetomatch]";
```

Geldige invoer is een door puntkomma&#39;s gescheiden lijst met raster- en waardeparen. Elke lijst bevat de volgende items:

* Een of meer rapportsuite-id&#39;s (gescheiden door komma&#39;s)
* Een gelijkteken
* Een of meer tekenreeksen die moeten overeenkomen (gescheiden door komma&#39;s)

Alleen standaard ASCII-tekens mogen in de tekenreeks worden gebruikt. Neem geen spaties op.

## Voorbeelden

Voor alle volgende voorbeelden is de pagina-URL `https://example.com/path2/?prod_id=12345`, wordt de `dynamicAccountSelection` variabele ingesteld op `true`, en wordt de `s_account` variabele ingesteld op `examplersid`.

```js
// In this example, the report suite that receives data is examplersid1.
s.dynamicAccountMatch = "window.location.hostname";
s.dynamicAccountList = "examplersid2=www2.example.com;examplersid1=example.com";

// In this example, the report suite that receives data is examplersid2.
s.dynamicAccountMatch = "window.location.pathname";
s.dynamicAccountList = "examplersid2=path2;examplersid3=path3";

// In this example, no rules match so it resorts to the default rsid in s_account, examplersid.
s.dynamicAccountMatch = "window.location.pathname";
s.dynamicAccountList = "examplersid4=path4;examplersid5=path5";
```

## Punten, vragen en tips

* De regels in deze variabele worden vermeld worden toegepast in een orde van links naar rechts. Als de `dynamicAccountMatch` variabele meer dan één regel aanpast, wordt de uiterst linkse regel gebruikt om de rapportreeks te bepalen. Dientengevolge, plaats meer generische regels aan het recht van de lijst.
* Als er geen regels overeenkomen, wordt de standaard rapportsuite in `s_account` gebruikt.
* Als uw pagina wordt opgeslagen op de vaste schijf van iemand of wordt vertaald via een vertaalprogramma op internet (zoals vertaalde pagina&#39;s van Google), werkt de dynamische accountselectie waarschijnlijk niet.
* De `dynamicAccountSelection` regels gelden alleen voor het gedeelte van de URL dat is opgegeven in `dynamicAccountMatch`.
* Gebruik het [!DNL Adobe Experience Cloud Debugger] om de reeks van het bestemmingsrapport te testen.
