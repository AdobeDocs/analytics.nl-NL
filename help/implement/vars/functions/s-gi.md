---
title: s_gi()
description: Creeer en spoor instanties van AppMeasurement.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# s_gi

De `s_gi()` functie instantieert of vindt een geval van AppMeasurement door rapportreeks ID. AppMeasurement houdt spoor van elke gemaakte instantie, en `s_gi()` keert de bestaande instantie voor een rapportreeks terug als één bestaat. Wanneer een instantie niet bestaat, wordt een nieuwe instantie gemaakt.

## s_gi() in Adobe Experience Platform Launch

De extensie Analytics instantieert en beheert het volgende object voor u. U kunt echter ook een algemeen traceringsobject in de [!UICONTROL Library Management] accordeon instellen wanneer u de extensie Adobe Analytics configureert.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] tabblad en klik vervolgens op de [!UICONTROL Configure] knop onder Adobe Analytics.
4. Vouw de [!UICONTROL Library Management] accordeon uit en selecteer een ander keuzerondje dan [!UICONTROL Manage the library for me].

In het tekstveld voor algemene variabelen kunt u een aangepast tekstobject bijhouden instellen. De standaardwaarde is `s`.

## s_gi() in de aangepaste code-editor van AppMeasurement en Launch

Roep de `s_gi()` functie aan om een volgend object te instantiëren. Zijn enige argument bevat een komma-afgebakende koord van rapportreeks IDs. Het argument van ID van de rapportsuite is vereist.

>[!TIP] Adobe raadt u aan de `s` variabele te gebruiken als een tekstspatiëringsobject. Adobe gebruikt `s` de documentatie, implementatievoorbeelden en plug-ins. U kunt echter elke variabele gebruiken zolang u op de hele site consistent bent.

```js
// Instantiate the tracking object with a single report suite
var s = s_gi("examplersid");

// Instantiate the tracking object to send to multiple report suites
var s = s_gi("examplersid1,examplersid2");
```

>[!CAUTION] De volgende secties en voorbeelden bevatten complexe implementatieonderwerpen. Test uw implementatie grondig en traceer belangrijke aanpassingen in het document [van het de](../../prepare/solution-design.md)oplossingsontwerp van uw organisatie.

## Meerdere implementaties beheren met verschillende trackingobjecten

U kunt verschillende gegevens naar verschillende rapportsuites verzenden als u veelvoudige het volgen voorwerpen concretiseert. Deze twee volgende objecten werken onafhankelijk van elkaar.

```js
// Instantiate two separate tracking objects to two different report suites
var s = s_gi('examplersid1');
var z = s_gi('examplersid2');

// The s object and z object contain their own independent Analytics variables simultaneously
s.pageName = "Example page name 1";
z.pageName = "Example page name 2";

// Send data to the examplersid1 report suite
s.t();

// Send data to the examplersid2 report suite
z.t();
```

## AppMeasurement-variabelen herstellen na het overschrijven van het s-object

Sommige gereedschappen van derden gebruiken mogelijk ook het JavaScript- `s` object. Als u per ongeluk het `s` object op uw site overschrijft, kunt u `s_gi` met hetzelfde RSID-tekenreeksargument aanroepen om alle overschreven variabelen en methoden te herstellen.

```js
// Step 1: Instantiate the tracking object
var s = s_gi("examplersid");

// Step 2: Set eVar1
s.eVar1 = "Example value";

// Step 3: Accidentally overwrite the tracking object
s = "3rd party tool";

// Step 4: If you attempt to send a tracking call, an error is returned. Instead, re-instantiate the tracking object
s = s_gi("examplersid");

// Step 5: The previous values of all variables are preserved. You can send a tracking call and eVar1 is correctly set
s.t();
```

## Verwijs naar hetzelfde volgende voorwerp met veelvoudige variabelen

Als twee variabelen met dezelfde `s_gi()` rapportsuite naar dezelfde functie verwijzen, kunt u de variabelen onderling uitwisselen.

```js
// If the RSID is the same, any variables set in the 's' tracking object also get set in 'z' tracking object
var s = s_gi('examplersid');
var z = s_gi('examplersid');

s.eVar1 = "Shared tracking object value";

// This tracking call contains the above eVar1 value
z.t();
```
