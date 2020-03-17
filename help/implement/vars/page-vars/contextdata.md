---
title: contextData
description: Met contextgegevensvariabelen kunt u aangepaste variabelen definiëren op elke pagina die door verwerkingsregels kan worden gelezen.
translation-type: tm+mt
source-git-commit: ''

---


# contextData

Met contextgegevensvariabelen kunt u aangepaste variabelen definiëren op elke pagina die door verwerkingsregels kan worden gelezen. In plaats van expliciet waarden toe te wijzen aan analytische variabelen in uw code, kunt u gegevens verzenden in contextgegevensvariabelen. De verwerkingsregels nemen dan de veranderlijke waarden van contextgegevens en gaan hen in respectieve variabelen van de Analyse over. Zie [Verwerkingsregels](/help/admin/admin/c-processing-rules/c-processing-rules-configuration/t-processing-rules.md) in de gebruikershandleiding voor Admin.

Contextgegevensvariabelen zijn handig voor ontwikkelingsteams om gegevens te verzamelen in benoemde elementen in plaats van genummerde variabelen. In plaats van ontwikkelingsteams bijvoorbeeld te vragen de auteur van de pagina aan toe te wijzen, kunt u `eVar10`ze vragen deze `s.contextData["author"]` toe te wijzen. Een beheerder van Analytics in uw organisatie kan dan verwerkingsregels tot stand brengen om de variabelen van de contextgegevens in analytische variabelen voor het melden in kaart te brengen. Ontwikkelingsteams zouden zich uiteindelijk alleen zorgen maken over de variabelen van de contextgegevens in plaats van over de vele paginariabelen die Adobe aanbiedt.

## Contextgegevensvariabelen in Adobe Experience Platform Launch

Starten heeft geen specifieke locatie voor het instellen van contextgegevensvariabelen. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.contextData in AppMeasurement en Launch, aangepaste code-editor

De `s.contextData` variabele neemt niet direct een waarde. Stel in plaats daarvan de eigenschappen van deze variabele in op een tekenreeks.

```js
// Assign the example_variable property a value
s.contextData["example_variable"] = "Example value";
```

* Geldige contextgegevensvariabelen bevatten alleen alfanumerieke tekens, onderstrepingstekens en punten. Adobe garandeert geen gegevensverzameling in de verwerkingsregels als u andere tekens, zoals afbreekstreepjes, opneemt.
* Begin geen variabelen van contextgegevens met `"a."`. Dit voorvoegsel is gereserveerd en wordt gebruikt door Adobe. Gebruik dit bijvoorbeeld niet `s.contextData["a.InstallEvent"]`.
* Contextgegevensvariabelen zijn niet hoofdlettergevoelig. De variabelen `s.contextData["example"]` en `s.contextData["EXAMPLE"]` zijn identiek.

## De verwerkingsregels van het gebruik om analysevariabelen te bevolken

> [!IMPORTANT] Contextgegevensvariabelen worden verwijderd nadat de verwerkingsregels zijn uitgevoerd. Als u geen verwerkingsregels hebt die waarden in variabelen plaatsen, worden die gegevens permanent verloren!

1. Werk uw implementatie bij om namen en waarden voor de variabele van de contextgegevens in te stellen.
2. Meld u aan bij Adobe Analytics en ga naar Admin > Report Suites.
3. Selecteer de gewenste rapportsuite en ga naar Instellingen > Algemeen > Verwerkingsregels bewerken.
4. Creeer een verwerkingsregel die een variabele Analytics aan de veranderlijke waarde van contextgegevens plaatst.
5. Wijzigingen opslaan.

De verwerkingsregels worden onmiddellijk van kracht nadat ze zijn opgeslagen. Zij zijn niet van toepassing op historische gegevens.

## Contextgegevens verzenden in een koppelingsvraag

De variabele met contextgegevens opnemen als een eigenschap van `contextData` in `s.linkTrackVars`:

```js
s.contextData["example_variable"] = "Example value";
s.linkTrackVars = "contextData.example_variable";
s.tl(true,"o","Example context data link");
```
