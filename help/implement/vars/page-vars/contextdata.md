---
title: contextData
description: Met contextgegevensvariabelen kunt u aangepaste variabelen definiëren op elke pagina die door verwerkingsregels kan worden gelezen.
feature: Variables
exl-id: f2c747a9-1a03-4f9f-8025-9f4745403a81
role: Admin, Developer
source-git-commit: 12347957a7a51dc1f8dfb46d489b59a450c2745a
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# contextData

Met contextgegevensvariabelen kunt u aangepaste variabelen definiëren op elke pagina die door verwerkingsregels kan worden gelezen. In plaats van expliciet waarden toe te wijzen aan analytische variabelen in uw code, kunt u gegevens verzenden in contextgegevensvariabelen. De verwerkingsregels nemen dan de veranderlijke waarden van contextgegevens en gaan hen in respectieve variabelen van de Analyse over. Zie [Verwerkingsregels](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.md) in de handleiding voor Admin-gebruikers.

Contextgegevensvariabelen zijn handig voor ontwikkelingsteams om gegevens te verzamelen in benoemde elementen in plaats van genummerde variabelen. In plaats van ontwikkelingsteams bijvoorbeeld te vragen, wijst u de auteur van de pagina toe aan `eVar10`, kunt u vragen dat ze deze toewijzen aan `s.contextData["author"]` in plaats daarvan. Een beheerder van Analytics in uw organisatie kan dan verwerkingsregels tot stand brengen om de variabelen van de contextgegevens in analytische variabelen voor het melden in kaart te brengen. Ontwikkelingsteams zouden zich uiteindelijk alleen zorgen maken over de variabelen van de contextgegevens in plaats van over de vele Adoben die de pagina aanbiedt.

## Contextgegevensvariabelen die de SDK van het Web gebruiken

Als u de [**XDM-object**](/help/implement/aep-edge/xdm-var-mapping.md) Alle velden die niet zijn toegewezen aan een Adobe Analytics-variabele worden automatisch opgenomen als een contextgegevensvariabele. U kunt vervolgens [Verwerkingsregels](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules.md) om de variabele van contextgegevens aan de gewenste variabele Analytics toe te wijzen.

Als u de [**gegevensobject**](/help/implement/aep-edge/data-var-mapping.md) alle variabelen van de contextgegevens zich binnen `data.__adobe.analytics.contextData` als sleutel-waardeparen:

```js
alloy("sendEvent", {
  "data": {
    "__adobe": {
      "analytics": {
        "contextData": {
          "example_variable": "Example value",
          "second_example": "Another value"
        }
      }
    }
  }
});
```

De [Verwerkingsregels](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules.md) interface zou tonen `c.example_variable` en `c.second_example` in de toepasselijke vervolgkeuzemenu&#39;s.

## Contextgegevensvariabelen die de extensie Adobe Analytics gebruiken

Adobe Experience Platform-gegevensverzameling heeft geen specifieke locatie voor het instellen van contextgegevensvariabelen. Gebruik de aangepaste code-editor volgens de syntaxis van het AppMeasurement.

## s.contextData in AppMeasurement en de de uitbreidingsredacteur van de douanecode van de Analyse

De `s.contextData` De variabele neemt niet direct een waarde. Stel in plaats daarvan de eigenschappen van deze variabele in op een tekenreeks.

```js
// Assign the example_variable property a value
s.contextData["example_variable"] = "Example value";
```

* Geldige contextgegevensvariabelen bevatten alleen alfanumerieke tekens, onderstrepingstekens en punten. Adobe garandeert geen gegevensverzameling in verwerkingsregels als u andere tekens, zoals afbreekstreepjes, opneemt.
* Geen variabelen voor contextgegevens starten met `"a."`. Dit voorvoegsel is gereserveerd en wordt gebruikt door Adobe. Gebruik bijvoorbeeld niet `s.contextData["a.InstallEvent"]`.
* Contextgegevensvariabelen zijn niet hoofdlettergevoelig. De variabelen `s.contextData["example"]` en `s.contextData["EXAMPLE"]` identiek zijn.

## De verwerkingsregels van het gebruik om analysevariabelen te bevolken

>[!WARNING]
>
>Contextgegevensvariabelen worden verwijderd nadat de verwerkingsregels zijn uitgevoerd. Als u geen verwerkingsregels hebt die waarden in variabelen plaatsen, worden die gegevens permanent verloren!

1. Werk uw implementatie bij om namen en waarden van variabelen voor de contextgegevens in te stellen.
2. Meld u aan bij Adobe Analytics en ga naar Beheer > Suites rapporteren.
3. Selecteer de gewenste rapportsuite en ga naar Instellingen > Algemeen > Verwerkingsregels bewerken.
4. Creeer een verwerkingsregel die een variabele Analytics aan de veranderlijke waarde van contextgegevens plaatst.
5. Wijzigingen opslaan.

De verwerkingsregels worden onmiddellijk van kracht nadat ze zijn opgeslagen. Zij zijn niet van toepassing op historische gegevens.

## Contextgegevens verzenden in een koppelingsvraag

De variabele met contextgegevens opnemen als een eigenschap van `contextData` in [`s.linkTrackVars`](../config-vars/linktrackvars.md):

```js
s.contextData["example_variable"] = "Example value";
s.linkTrackVars = "contextData.example_variable";
s.tl(true,"o","Example context data link");
```

## Incrementele gebeurtenissen met gebruik van contextgegevensvariabelen

Wanneer u verwerkingsregels maakt, kunt u contextgegevensvariabelen aan gebeurtenissen toewijzen.

* Als een contextgegevensvariabele tekst bevat, wordt de gebeurtenis met één verhoogd.
* Als een contextgegevensvariabele een geheel getal bevat, wordt de waarde van het gehele getal verhoogd.

```js
// Assigning this context data variable to an event increments it by one
s.contextData["example_text"] = "Text value";

// Assigning this context data variable to an event increments it by four
s.contextData["example_number"] = "4";
```
