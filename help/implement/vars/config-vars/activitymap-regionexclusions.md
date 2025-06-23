---
title: ActivityMap.regionExclusions
description: Filter Activity Map-gegevens op gebied.
role: Admin, Developer
feature: Appmeasurement Implementation
exl-id: 353282aa-860c-45dc-a6b0-8d9f1fa09f13
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# ActivityMap.regionExclusions

De `ActivityMap.regionExclusions` variabele laat u Activity Map gegevens selectief filtreren of uitsluiten die op de afmetingspunten worden gebaseerd in de [ 2} afmeting van het Gebied van Activity Map worden verzameld {.](/help/components/dimensions/activity-map-region.md)

## Uitsluitingen van regio&#39;s in de extensie Web SDK

Wanneer **[!UICONTROL Enable click data collection]** is ingeschakeld, gebruikt u het codeblok **[!UICONTROL Filter click properties]** callback. Binnen dit codeblok kunt u de waarde van `content.linkRegion` controleren en de waarde wijzigen of de verzameling van gegevens voor het bijhouden van koppelingen opgeven.

## Uitsluitingen van regio&#39;s in de Web SDK JavaScript-bibliotheek

Wanneer [`clickCollectionEnabled` ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled) wordt toegelaten, gebruik `filterClickDetails` callback in het `clickCollection` voorwerp. Binnen deze callback kunt u de waarde van `linkRegion` controleren en de waarde wijzigen of de verzameling van gegevens voor het bijhouden van koppelingen opgeven.

```js
alloy("configure", {
  clickCollectionEnabled: true,
  clickCollection: {
    filterClickDetails: function(content) {
      // If the clicked region has personal links in it, don't send click data
      if(content.linkRegion.includes("personal")) {
        return false;
      }
    }
  }
});
```

## Uitsluitingen van gebieden die de extensie Adobe Analytics gebruiken

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de AppMeasurement-syntaxis.

## s.ActivityMap.regionExclusions met AppMeasurement

De variabele `s.ActivityMap.regionExclusions` is een tekenreeks met door komma&#39;s gescheiden zinnen die worden uitgesloten van het bijhouden van Activity Map. Als om het even welke uitdrukkingen de waarde aanpassen die in de [ dimensie van het Gebied van Activity Map ](/help/components/dimensions/activity-map-region.md) wordt verzameld, worden alle gegevens van Activity Map verwijderd uit de slag.

```html
<script>
  var s = s_gi("examplersid");
  s.ActivityMap.regionExclusions = "contact";
</script>

<!-- Clicking any of these links tracks normally. -->
<!-- While "contact" is present, it is not tracked in region. The region is "nav" -->
<nav>
  <a href="index.html">Home</a>
  <a href="products.html">View our products</a>
  <a href="contact.html">Contact us</a>
</nav>

<!-- Activity Map data is not tracked for any of these links. -->
<!-- All these links belong to the region "Personal contact information" -->
<div id="personal-contact-information">
 <a href="mailto:user@example.com">Example user</a>
 <a href="mailto:user2@example.com">Example user 2</a>
 <a href="mailto:user3@example.com">Example user 3</a>
</div>
```
