---
title: ActivityMap.region
description: Pas aan hoe de Activity Map het aangeklikte gebied verzamelt.
feature: Variables
role: Admin, Developer
source-git-commit: 1fb57590714ad2412323416289dee967eef07fad
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# ActivityMap.region

Met de variabele `ActivityMap.region` kunt u de logica negeren waarmee de Activity Map gebiedswaarden instelt. Deze variabele is nuttig in gebieden waar u meer controle wilt hebben dan wat [`ActivityMap.regionExclusions`](../config-vars/activitymap-regionexclusions.md) verstrekt.

>[!CAUTION]
>Deze variabele negeert volledig de logica van de Activity Map. Als u hier een overschrijvingsfunctie instelt die onjuiste waarden retourneert, kunnen er problemen ontstaan met de gegevensverzameling en de Activity Map-overlay.

## Waarde van gebieden overschrijven met de SDK van het web

U kunt [`OnBeforeLinkClickSend` gebruiken ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/onbeforelinkclicksend) callback om de nuttige lading van SDK van het Web te veranderen of het verzenden van gegevens te aborteren.

## Regio overschrijven met Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de syntaxis van het AppMeasurement.

## ActivityMap.region in AppMeasurement en de de coderedacteur van de uitbreiding van de Analyse

Wijs deze variabele een functie toe die:

* Ontvangt het HTML-element waarop is geklikt; en
* Retourneert een tekenreekswaarde. Deze koordwaarde is de definitieve waarde die voor de [&#128279;](/help/components/dimensions/activity-map-region.md) dimensie van het Gebied van de Activity Map wordt gebruikt 0&rbrace;.

Als de terugkeerwaarde [ vals ](https://developer.mozilla.org/en-US/docs/Glossary/Falsy) is, worden alle variabelen van de de context van de Activity Map ontruimd en geen verbindingsgegevens worden gevolgd.

## Voorbeelden

Gebruik een naam van een tag in kleine letters als gebied:

```js
s.ActivityMap.region = function(clickedElement) {
  while (clickedElement && (clickedElement = clickedElement.parentNode)) {
    var regionId = clickedElement.tagName;
    if (regionId) {
      return regionId.toLowerCase();
    }
  }
}
```

Gebruik specifieke gewenste klassenamen als gebied:

```js
s.ActivityMap.region = function(ele) {
  var className,
  classNames = {
    'header': 1,
    'navbar': 1,
    'left-content': 1,
    'main-content': 1,
    'footer': 1,
  };
  while ((ele && (ele = ele.parentNode))) {
    if ((className = ele.className)) {
      let classes = className.split(' ');
      for (let i = 0; i < classes.length; i++) {
        if (classNames[classes[i]]) {
          return classes[i];
        }
      }
    }
  }
  return "BODY";
}
```
