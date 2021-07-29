---
title: contextData
description: Met contextgegevensvariabelen kunt u aangepaste variabelen definiëren op elke pagina die door verwerkingsregels kan worden gelezen.
exl-id: f2c747a9-1a03-4f9f-8025-9f4745403a81
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%

---

# contextData

Met contextgegevensvariabelen kunt u aangepaste variabelen definiëren op elke pagina die door verwerkingsregels kan worden gelezen. In plaats van expliciet waarden toe te wijzen aan analytische variabelen in uw code, kunt u gegevens verzenden in contextgegevensvariabelen. De verwerkingsregels nemen dan de veranderlijke waarden van contextgegevens en gaan hen in respectieve variabelen van de Analyse over. Zie [Verwerkingsregels](/help/admin/admin/c-processing-rules/c-processing-rules-configuration/t-processing-rules.md) in de Admin gebruikershandleiding.

Contextgegevensvariabelen zijn handig voor ontwikkelingsteams om gegevens te verzamelen in benoemde elementen in plaats van genummerde variabelen. In plaats van ontwikkelingsteams bijvoorbeeld te vragen de auteur van de pagina aan `eVar10` toe te wijzen, kunt u vragen dat deze de pagina toewijst aan `s.contextData["author"]`. Een beheerder van Analytics in uw organisatie kan dan verwerkingsregels tot stand brengen om de variabelen van de contextgegevens in analytische variabelen voor het melden in kaart te brengen. Ontwikkelingsteams zouden zich uiteindelijk alleen zorgen maken over de variabelen van contextgegevens in plaats van over de vele Adobe-aanbiedingen voor paginabereiken.

## Contextgegevensvariabelen die tags gebruiken in Adobe Experience Platform

De UI van de Inzameling van Gegevens heeft geen specifieke plaats om de variabelen van contextgegevens te plaatsen. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.contextData in AppMeasurement en aangepaste code-editor

De variabele `s.contextData` neemt niet direct een waarde. Stel in plaats daarvan de eigenschappen van deze variabele in op een tekenreeks.

```js
// Assign the example_variable property a value
s.contextData["example_variable"] = "Example value";
```

* Geldige contextgegevensvariabelen bevatten alleen alfanumerieke tekens, onderstrepingstekens en punten. Adobe garandeert geen gegevensverzameling in verwerkingsregels als u andere tekens, zoals afbreekstreepjes, opneemt.
* Begin geen variabelen van contextgegevens met `"a."`. Dit voorvoegsel is gereserveerd en wordt gebruikt door Adobe. Gebruik bijvoorbeeld `s.contextData["a.InstallEvent"]` niet.
* Contextgegevensvariabelen zijn niet hoofdlettergevoelig. De variabelen `s.contextData["example"]` en `s.contextData["EXAMPLE"]` zijn identiek.

## De verwerkingsregels van het gebruik om analysevariabelen te bevolken

>[!IMPORTANT]
>
>Contextgegevensvariabelen worden verwijderd nadat de verwerkingsregels zijn uitgevoerd. Als u geen verwerkingsregels hebt die waarden in variabelen plaatsen, worden die gegevens permanent verloren!

1. Werk uw implementatie bij om namen en waarden voor de variabele van de contextgegevens in te stellen.
2. Meld u aan bij Adobe Analytics en ga naar Beheer > Suites rapporteren.
3. Selecteer de gewenste rapportsuite en ga naar Instellingen > Algemeen > Verwerkingsregels bewerken.
4. Creeer een verwerkingsregel die een variabele Analytics aan de veranderlijke waarde van contextgegevens plaatst.
5. Wijzigingen opslaan.

De verwerkingsregels worden onmiddellijk van kracht nadat ze zijn opgeslagen. Zij zijn niet van toepassing op historische gegevens.

## Contextgegevens verzenden in een koppelingsvraag

Neem de variabele met contextgegevens op als een eigenschap van `contextData` in [`s.linkTrackVars`](../config-vars/linktrackvars.md):

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
