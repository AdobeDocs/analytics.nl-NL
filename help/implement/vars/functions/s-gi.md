---
title: s_gi()
description: Creeer en spoor instanties van AppMeasurement.
exl-id: f87eff07-7e60-480b-8334-3db538c1030e
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 1%

---

# s_gi

De functie `s_gi()` concretiseert of vindt een geval van AppMeasurement door identiteitskaart van de rapportreeks. AppMeasurement houdt spoor van elke gemaakte instantie, en `s_gi()` keert de bestaande instantie voor een rapportreeks terug als één bestaat. Wanneer een instantie niet bestaat, wordt een nieuwe instantie gemaakt.

## s_gi() tags gebruiken in Adobe Experience Platform

De extensie Analytics instantieert en beheert het volgende object voor u. U kunt echter ook een algemeen traceringsobject instellen in de accordeon [!UICONTROL Library Management] wanneer u de Adobe Analytics-extensie configureert.

1. Meld u aan bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder Adobe Analytics.
4. Vouw de accordeon [!UICONTROL Library Management] uit en selecteer een ander keuzerondje dan [!UICONTROL Manage the library for me].

In het tekstveld voor algemene variabelen kunt u een aangepast tekstobject bijhouden instellen. De standaardwaarde is `s`.

## s_gi() in AppMeasurement en aangepaste code-editor

Roep de functie `s_gi()` aan om een volgende voorwerp te concretiseren. Zijn enige argument bevat een komma-afgebakende koord van rapportreeks IDs. Het argument van ID van de rapportsuite is vereist.

>[!TIP]
>
>Adobe raadt u aan de variabele `s` als een tekstspatiëringsobject te gebruiken. Adobe gebruikt `s` in zijn documentatie, implementatievoorbeelden, en stop-ins. U kunt echter elke variabele gebruiken zolang u op de hele site consistent bent.

```js
// Instantiate the tracking object with a single report suite
var s = s_gi("examplersid");

// Instantiate the tracking object to send to multiple report suites
var s = s_gi("examplersid1,examplersid2");
```

>[!CAUTION]
>
>De volgende secties en voorbeelden bevatten complexe implementatieonderwerpen. Test uw implementatie grondig en traceer belangrijke aanpassingen in het [document voor het ontwerp van oplossingen](../../prepare/solution-design.md) van uw organisatie.

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

Sommige gereedschappen van derden gebruiken mogelijk ook het JavaScript `s`-object. Als u per ongeluk het `s` voorwerp op uw plaats overschrijft, kunt u `s_gi` met het zelfde het koordargument van RSID roepen om alle beschreven variabelen en methodes te herstellen.

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

Als twee variabelen de zelfde `s_gi()` functie met de zelfde rapportreeks van verwijzingen voorzien, kunt u de variabelen onderling verwisselbaar gebruiken.

```js
// If the RSID is the same, any variables set in the 's' tracking object also get set in 'z' tracking object
var s = s_gi('examplersid');
var z = s_gi('examplersid');

s.eVar1 = "Shared tracking object value";

// This tracking call contains the above eVar1 value
z.t();
```
