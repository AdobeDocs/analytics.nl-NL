---
title: ActivityMap.link
description: Aanpassen hoe Activity Map de aangeklikte koppeling verzamelt.
feature: Appmeasurement Implementation
role: Admin, Developer
exl-id: 3a31f80b-dbee-4a45-ac3c-0b8ca198c95a
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---

# ActivityMap.link

Met de variabele `ActivityMap.link` kunt u de logica negeren die Activity Map gebruikt om koppelingswaarden in te stellen. Deze variabele is nuttig in gebieden waar u meer controle wilt hebben dan wat [`ActivityMap.linkExclusions`](../config-vars/activitymap-linkexclusions.md) verstrekt.

>[!CAUTION]
>Deze variabele heeft volledig voorrang op Activity Map-logica. Als u hier een overschrijvingsfunctie instelt die onjuiste waarden retourneert, kunnen er problemen optreden bij het verzamelen van gegevens met Activity Map-afmetingen en de Activity Map-overlay.

## Koppelingswaarden overschrijven met de Web SDK

U kunt [`OnBeforeLinkClickSend` gebruiken &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/web-sdk/commands/configure/onbeforelinkclicksend) callback om de nuttige lading van SDK van het Web te veranderen of het verzenden van gegevens te aborteren.

## Koppelingsoverschrijving met de Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de AppMeasurement-syntaxis.

## ActivityMap.link in AppMeasurement en de aangepaste code-editor voor de extensie Analytics

Wijs deze variabele een functie toe die:

* Ontvangt het HTML-element waarop is geklikt; en
* Retourneert een tekenreekswaarde. Deze koordwaarde is de definitieve waarde die voor de [&#x200B; dimensie van de Verbinding van Activity Map &#x200B;](/help/components/dimensions/activity-map-link.md) wordt gebruikt.

Als de terugkeerwaarde [&#x200B; vals &#x200B;](https://developer.mozilla.org/en-US/docs/Glossary/Falsy) is, worden alle de contextgegevensvariabelen van Activity Map ontruimd en geen verbindingsgegevens worden gevolgd.

## Voorbeelden

Gebruik alleen het titelkenmerk van `<a>` -tags. Als het titelkenmerk niet aanwezig is, wordt geen koppeling bijgehouden.

```js
s.ActivityMap.link = function(clickedElement) {
  var linkId;
  if (clickedElement && clickedElement.tagName.toUpperCase() === 'A') {
    linkId = clickedElement.getAttribute('title');
  }
  return linkId;
}
```

Retourneer de handmatig ingestelde naam van de koppeling in `s.tl` als deze bestaat, anders retourneert u de URL van de koppeling.

```js
s.ActivityMap.link = function(ele, linkName) {
  if (linkName) {
    return linkName;
  }
  if (ele && ele.tagName == 'A' && ele.href) {
    return ele.href;
  }
}
```

In plaats van de standaardkoppelingslogica volledig te vervangen, kunt u deze voorwaardelijk wijzigen.

```html
<script>
  // Copy the original link function
  var originalLinkFunction = s.ActivityMap.link;
  // Return the link name from s.tl, a modified activity map value, or the original activity map value
  s.ActivityMap.link = function(element,linkName)
  {
    return linkName || customFunction(element) || originalLinkFunction(element,linkName);
  };
</script>

<button type="button" onclick="s.tl(this,'o',customFunction(this)">Add To Cart</button>
```

1. Als `linkName` wordt doorgegeven, is de methode aangeroepen door `tl()` . Retourneer wat `tl()` heeft doorgegeven als `linkName` .
2. Als een `linkName` -element wordt aangeroepen door Activity Map, wordt dit nooit doorgegeven. Roep `customFunction()` dus aan met het koppelingselement. U kunt elke aangepaste functie gebruiken die u wilt retourneren.
3. Als geen van beide bovengenoemde terugkeerwaarden, gebruik de verbindingsnaam normaal verzameld als reserve.
