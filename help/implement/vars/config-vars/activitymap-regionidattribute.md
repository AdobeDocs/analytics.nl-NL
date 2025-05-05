---
title: ActivityMap.regionIDAttribute
description: Wijzig het kenmerk waarnaar de Activity Map zoekt om het gebied te bepalen.
feature: Variables
role: Admin, Developer
source-git-commit: 05010d58ba2a3376473097e9d4543ee4415e83e1
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# ActivityMap.regionIDAttribute

De `ActivityMap.regionIDAttribute` variabele laat u de attributen veranderen die de Activity Map zoekt wanneer het bepalen van de [ dimensie van het Gebied van de Activity Map ](/help/components/dimensions/activity-map-region.md). Als uw site zodanig is gestructureerd dat het kenmerk `id` minder handig is voor het gebied van de Activity Map, kunt u deze variabele zo instellen dat deze naar een ander kenmerk kijkt.

## Het attribuut van identiteitskaart van het gebied in de uitbreiding van SDK van het Web

Wanneer **[!UICONTROL Enable click data collection]** is ingeschakeld, gebruikt u het codeblok **[!UICONTROL Filter click properties]** callback. Binnen dit codeblok kunt u de waarde van `content.clickedElement` controleren en de waarde wijzigen of de verzameling van gegevens voor het bijhouden van koppelingen opgeven.

## Het kenmerk Region ID in de Web SDK JavaScript-bibliotheek

Wanneer [`clickCollectionEnabled` ](https://experienceleague.adobe.com/nl/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled) wordt toegelaten, gebruik `filterClickDetails` callback in het `clickCollection` voorwerp. Binnen deze callback kunt u de waarde van `clickedElement` controleren en de logica van het verzamelde gebied aanpassen.

```js
alloy("configure", {
  clickCollectionEnabled: true,
  clickCollection: {
    filterClickDetails: function(content) {
      // If the clicked element was in a table, set the region to the contents of the data-custom attribute
      // If the clicked element was not in a table, or if the data-custom attribute doesn't exist, leave region as-is
      content.region = content.clickedElement.closest('table')?.getAttribute('data-custom') || content.region;
    }
  }
});
```

## Gebied ID-kenmerk met Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de syntaxis van het AppMeasurement.

## s.ActivityMap.regionIDAttribute gebruiken AppMeasurement

De `s.ActivityMap.regionIDAttribute` variabele is een koord dat de attributen vertegenwoordigt om de [ dimensie van het Gebied van de Activity Map ](/help/components/dimensions/activity-map-region.md) te bepalen. Deze variabele wordt standaard ingesteld op `id` . Als u deze variabele wijzigt, zoekt de Activity Map niet langer naar het kenmerk `id` , maar naar andere criteria om het gebied te bepalen (zoals semantische elementen).

```html
<script>
  var s = s_gi("examplersid");
  s.ActivityMap.regionIDAttribute = "data-custom";
</script>

<!-- Clicking any of these links populates the region dimension with 'left-nav' -->
<div id="676967617A656C6C65" data-custom="left-nav">
  <a href="index.html">Home</a>
  <a href="products.html">View our products</a>
  <a href="contact.html">Contact us</a>
</div>
```
