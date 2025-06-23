---
title: ActivityMap.region
description: Aanpassen hoe Activity Map het aangeklikte gebied verzamelt.
feature: Appmeasurement Implementation
role: Admin, Developer
exl-id: 9bbdb124-b865-4431-8a98-9814c3f2e65c
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# ActivityMap.region

Met de variabele `ActivityMap.region` kunt u de logica negeren die Activity Map gebruikt om gebiedswaarden in te stellen. Deze variabele is nuttig in gebieden waar u meer controle wilt hebben dan wat [`ActivityMap.regionExclusions`](../config-vars/activitymap-regionexclusions.md) verstrekt.

>[!CAUTION]
>Deze variabele heeft volledig voorrang op Activity Map-logica. Als u hier een overschrijvingsfunctie instelt die onjuiste waarden retourneert, kunnen er problemen optreden bij het verzamelen van gegevens met Activity Map-afmetingen en de Activity Map-overlay.

## Waarden voor gebieden overschrijven met de Web SDK

U kunt [`OnBeforeLinkClickSend` gebruiken ](https://experienceleague.adobe.com/nl/docs/experience-platform/web-sdk/commands/configure/onbeforelinkclicksend) callback om de nuttige lading van SDK van het Web te veranderen of het verzenden van gegevens te aborteren.

## Regio overschrijven met Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de AppMeasurement-syntaxis.

## ActivityMap.region in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

Wijs deze variabele een functie toe die:

* Ontvangt het HTML-element waarop is geklikt; en
* Retourneert een tekenreekswaarde. Deze koordwaarde is de definitieve waarde die voor de [&#128279;](/help/components/dimensions/activity-map-region.md) dimensie van het Gebied van Activity Map wordt gebruikt.

Als de terugkeerwaarde [ vals ](https://developer.mozilla.org/en-US/docs/Glossary/Falsy) is, worden alle de contextgegevensvariabelen van Activity Map ontruimd en geen verbindingsgegevens worden gevolgd.

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
