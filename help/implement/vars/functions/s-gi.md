---
title: s_gi()
description: Instanties van AppMeasurement maken en bijhouden.
feature: Appmeasurement Implementation
exl-id: f87eff07-7e60-480b-8334-3db538c1030e
role: Admin, Developer
source-git-commit: 2d5348a4a6377313f5aab229214d97a02c826939
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# s_gi

De functie `s_gi()` instantieert of zoekt een instantie van AppMeasurement door rapportsuite-id. AppMeasurement houdt elke gemaakte instantie bij en `s_gi()` retourneert de bestaande instantie voor een rapportsuite als deze bestaat. Wanneer een instantie niet bestaat, wordt een nieuwe instantie gemaakt.

## Een trackingobject instantiëren met de extensie Web SDK

De extensie Web SDK instantieert en beheert het volgende object voor u. U kunt de naam van het volgende object echter aanpassen in de extensie-instellingen:

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Ga naar het tabblad [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder Adobe Experience Platform Web SDK.
1. Wijzig het veld [!UICONTROL Name] in de gewenste waarde. De standaardwaarde is `alloy` .

## Instantieer een volgende voorwerp manueel uitvoerend het Web SDK

De volgende code laadt het Web SDK en concretiseert een volgend voorwerp. U kunt de naam van het volgende object aanpassen door de tekenreeks `"alloy"` aan het einde van het inlinescript in te stellen op de gewenste waarde.

```js
<script>
  !function(n,o){o.forEach(function(o){n[o]||((n.__alloyNS=n.__alloyNS||
  []).push(o),n[o]=function(){var u=arguments;return new Promise(
  function(i,l){n[o].q.push([i,l,u])})},n[o].q=[])})}
  (window,["alloy"]);
</script>
<script src="https://cdn1.adoberesources.net/alloy/2.6.4/alloy.min.js" async></script>
```

Zie [&#x200B; de SDK &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=nl-NL) in de documentatie van SDK van het Web voor meer informatie installeren.

## Een trackingobject instantiëren met de Adobe Analytics-extensie

De extensie Analytics instantieert en beheert het volgende object voor u. U kunt echter ook een algemeen traceringsobject instellen in de accordeon [!UICONTROL Library Management] wanneer u de Adobe Analytics-extensie configureert.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de gewenste tageigenschap.
1. Ga naar de tab [!UICONTROL Extensions] en klik vervolgens op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
1. Vouw de accordeon [!UICONTROL Library Management] uit en selecteer een ander keuzerondje dan [!UICONTROL Manage the library for me] .

In het tekstveld voor algemene variabelen kunt u een aangepast tekstobject bijhouden instellen. De standaardwaarde is `s` .

## s_gi() in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

Roep de functie `s_gi()` aan om een volgend object te instantiëren. Zijn enige argument bevat een komma-afgebakende koord van rapportreeks IDs. Het argument van ID van de rapportsuite is vereist.

>[!TIP]
>
>Adobe raadt u aan de variabele `s` als een tekstspatiëringsobject te gebruiken. Adobe gebruikt `s` in de documentatie, implementatievoorbeelden en plug-ins. U kunt echter elke variabele gebruiken zolang u op de hele site consistent bent.

```js
// Instantiate the tracking object with a single report suite
var s = s_gi("examplersid");

// Instantiate the tracking object to send to multiple report suites
var s = s_gi("examplersid1,examplersid2");
```

>[!CAUTION]
>
>De volgende secties en voorbeelden bevatten complexe implementatieonderwerpen. Test uw implementatie grondig en volg belangrijke aanpassingen in het document van het de oplossingsontwerp van uw organisatie [&#128279;](../../prepare/solution-design.md).

## Meerdere implementaties beheren met verschillende trackingobjecten

U kunt verschillende gegevens naar verschillende rapportsuites verzenden als u veelvoudige het volgen voorwerpen concretiseert. Deze twee volgende objecten werken onafhankelijk van elkaar.

```js
// Instantiate two separate tracking objects to two different report suites
var s = s_gi('examplersid1');
var z = s_gi('examplersid2');

// The s object and z object contain their own independent Analytics variables simultaneously
s.pageName = "Example page name";
z.pageName = "An alternate page name";

// Send data to the examplersid1 report suite
s.t();

// Send data to the examplersid2 report suite
z.t();
```

## AppMeasurement-variabelen herstellen nadat het s-object is overschreven

Sommige gereedschappen van derden gebruiken mogelijk ook het JavaScript `s` -object. Als u per ongeluk het `s` -object op uw site overschrijft, kunt u `s_gi` aanroepen met hetzelfde RSID-tekenreeksargument om alle overschreven variabelen en methoden te herstellen.

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

Als twee variabelen met dezelfde rapportsuite naar dezelfde `s_gi()` functie verwijzen, kunt u de variabelen door elkaar gebruiken.

```js
// If the RSID is the same, any variables set in the 's' tracking object also get set in 'z' tracking object
var s = s_gi('examplersid');
var z = s_gi('examplersid');

s.eVar1 = "Shared tracking object value";

// This tracking call contains the above eVar1 value
z.t();
```
