---
title: contextData
description: Met contextgegevensvariabelen kunt u aangepaste variabelen definiëren op elke pagina die door verwerkingsregels kan worden gelezen.
feature: Appmeasurement Implementation
exl-id: f2c747a9-1a03-4f9f-8025-9f4745403a81
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '570'
ht-degree: 0%

---

# contextData

Met contextgegevensvariabelen kunt u aangepaste variabelen definiëren op elke pagina die door verwerkingsregels kan worden gelezen. In plaats van expliciet waarden toe te wijzen aan analytische variabelen in uw code, kunt u gegevens verzenden in contextgegevensvariabelen. De verwerkingsregels nemen dan de veranderlijke waarden van contextgegevens en gaan hen in respectieve variabelen van de Analyse over. Zie [ Regels van de Verwerking ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.md) in de Admin gebruikersgids.

Contextgegevensvariabelen zijn handig voor ontwikkelingsteams om gegevens te verzamelen in benoemde elementen in plaats van genummerde variabelen. In plaats van ontwikkelingsteams bijvoorbeeld te vragen de auteur van de pagina aan `eVar10` toe te wijzen, kunt u deze laten toewijzen aan `s.contextData["author"]` . Een beheerder van Analytics in uw organisatie kan dan verwerkingsregels tot stand brengen om de variabelen van de contextgegevens in analytische variabelen voor het melden in kaart te brengen. Ontwikkelingsteams zouden zich uiteindelijk alleen zorgen maken over de variabelen van contextgegevens in plaats van over de vele paginariabelen die Adobe aanbiedt.

## Contextgegevensvariabelen die de Web SDK gebruiken

Als het gebruiken van het [**voorwerp XDM**](/help/implement/aep-edge/xdm-var-mapping.md), zijn alle gebieden die niet aan een variabele van Adobe Analytics in kaart brengen automatisch inbegrepen als variabele van contextgegevens. U kunt ook expliciet contextgegevens instellen met het XDM-object. U kunt [ Regels van de Verwerking ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules.md) dan gebruiken om de variabele van contextgegevens aan de gewenste variabele van Analytics toe te wijzen.  Zie [ Toewijzing andere gebieden XDM aan de variabelen van Analytics ](../../aep-edge/xdm-var-mapping.md#mapping-other-xdm-fields-to-analytics-variables) voor meer informatie.

Als het gebruiken van het [**gegevensvoorwerp**](/help/implement/aep-edge/data-var-mapping.md), verblijven alle variabelen van contextgegevens binnen `data.__adobe.analytics.contextData` als zeer belangrijk-waardeparen:

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

De [ interface van de Regels van de Verwerking ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules.md) zou `example_variable` en `second_example` in toepasselijke drop-down menu&#39;s tonen.

## Contextgegevensvariabelen die de extensie Adobe Analytics gebruiken

Adobe Experience Platform-gegevensverzameling heeft geen specifieke locatie voor het instellen van contextgegevensvariabelen. Gebruik de aangepaste code-editor volgens de AppMeasurement-syntaxis.

## s.contextData in AppMeasurement en de de coderedacteur van de uitbreiding van de Analyse

De variabele `s.contextData` neemt niet rechtstreeks een waarde. Stel in plaats daarvan de eigenschappen van deze variabele in op een tekenreeks.

```js
// Assign the example_variable property a value
s.contextData["example_variable"] = "Example value";
```

* Geldige contextgegevensvariabelen bevatten alleen alfanumerieke tekens, onderstrepingstekens en punten. Adobe garandeert geen gegevensverzameling in verwerkingsregels als u andere tekens, zoals afbreekstreepjes, opneemt.
* Begin geen variabelen van contextgegevens met `"a."`. Dit voorvoegsel is gereserveerd en wordt gebruikt door Adobe. Gebruik bijvoorbeeld niet `s.contextData["a.InstallEvent"]` .
* Contextgegevensvariabelen zijn niet hoofdlettergevoelig. De variabelen `s.contextData["example"]` en `s.contextData["EXAMPLE"]` zijn identiek.
* Een enkele toets mag niet meer dan één waarde bevatten. Als u de variabelen van contextgegevens voor multi-waardevariabelen wilt gebruiken, schakelt alle waarden aaneen gebruikend een scheidingsteken (typisch a komma) en gaat het in of a [ lijst prop ](prop.md#list-props) of a [ lijstvariabele ](list.md) gebruikend verwerkingsregels over.

## De verwerkingsregels van het gebruik om analysevariabelen te bevolken

>[!WARNING]
>
>Contextgegevensvariabelen worden verwijderd nadat de verwerkingsregels zijn uitgevoerd. Als u geen verwerkingsregels hebt die waarden in variabelen plaatsen, worden die gegevens permanent verloren!

1. Werk uw implementatie bij om namen en waarden van variabelen voor de contextgegevens in te stellen.
2. Meld u aan bij Adobe Analytics en ga naar **[!UICONTROL Admin]** > **[!UICONTROL Report]** Suites.
3. Selecteer de gewenste rapportsuite en ga naar **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Processing Rules]** .
4. Creeer een verwerkingsregel die een variabele Analytics aan de veranderlijke waarde van contextgegevens plaatst.
5. Wijzigingen opslaan.

De verwerkingsregels worden onmiddellijk van kracht nadat ze zijn opgeslagen. Zij zijn niet van toepassing op historische gegevens.

## Contextgegevens verzenden in een koppelingsvraag

Neem de variabele met contextgegevens op als een eigenschap van `contextData` in [`s.linkTrackVars`](../config-vars/linktrackvars.md) :

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
