---
title: ActivityMap.regionIDAttribute
description: Wijzig het kenmerk waarnaar Activity Map zoekt om het gebied te bepalen.
feature: Appmeasurement Implementation
role: Admin, Developer
exl-id: 4aec045e-1a86-412f-bd37-777ac49ccc7d
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# ActivityMap.regionIDAttribute

De `ActivityMap.regionIDAttribute` variabele laat u de attributen veranderen die Activity Map wanneer het bepalen van de [ 2} dimensie van het Gebied van Activity Map zoekt. ](/help/components/dimensions/activity-map-region.md) Als uw site zodanig is gestructureerd dat het kenmerk `id` minder nuttig is voor het Activity Map-gebied, kunt u deze variabele zo instellen dat deze naar een ander kenmerk kijkt.

## Het attribuut van identiteitskaart van het gebied in de uitbreiding van SDK van het Web

Wanneer **[!UICONTROL Enable click data collection]** is ingeschakeld, gebruikt u het codeblok **[!UICONTROL Filter click properties]** callback. Binnen dit codeblok kunt u de waarde van `content.clickedElement` controleren en de waarde wijzigen of de verzameling van gegevens voor het bijhouden van koppelingen opgeven.

## Het kenmerk Region ID in de Web SDK JavaScript-bibliotheek

Wanneer [`clickCollectionEnabled` ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled) wordt toegelaten, gebruik `filterClickDetails` callback in het `clickCollection` voorwerp. Binnen deze callback kunt u de waarde van `clickedElement` controleren en de logica van het verzamelde gebied aanpassen.

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

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de AppMeasurement-syntaxis.

## s.ActivityMap.regionIDAttribute gebruiken met AppMeasurement

De `s.ActivityMap.regionIDAttribute` variabele is een koord dat de attributen vertegenwoordigt om de [ dimensie van het Gebied van Activity Map ](/help/components/dimensions/activity-map-region.md) te bepalen. Deze variabele wordt standaard ingesteld op `id` . Als u deze variabele wijzigt, zoekt Activity Map niet langer naar het kenmerk `id` , maar zoekt het nog steeds naar andere criteria om het gebied te bepalen (zoals semantische elementen).

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
