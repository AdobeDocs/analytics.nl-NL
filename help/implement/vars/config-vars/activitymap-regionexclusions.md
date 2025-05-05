---
title: ActivityMap.regionExclusions
description: Filter de gegevens van de Activity Map op gebied.
role: Admin, Developer
feature: Variables
source-git-commit: 05010d58ba2a3376473097e9d4543ee4415e83e1
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# ActivityMap.regionExclusions

De `ActivityMap.regionExclusions` variabele laat u selectief Activity Map gegevens filtreren of uitsluiten die op de afmetingspunten worden gebaseerd in de [ dimensie van het Gebied van de Activity Map ](/help/components/dimensions/activity-map-region.md) worden verzameld.

## Uitsluitingen van regio&#39;s in de Web SDK-extensie

Wanneer **[!UICONTROL Enable click data collection]** is ingeschakeld, gebruikt u het codeblok **[!UICONTROL Filter click properties]** callback. Binnen dit codeblok kunt u de waarde van `content.linkRegion` controleren en de waarde wijzigen of de verzameling van gegevens voor het bijhouden van koppelingen opgeven.

## Uitsluitingen voor regio&#39;s in de Web SDK JavaScript-bibliotheek

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

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de syntaxis van het AppMeasurement.

## s.ActivityMap.regionExclusions met AppMeasurement

De variabele `s.ActivityMap.regionExclusions` is een tekenreeks met kommagescheiden zinnen die worden uitgesloten van bijhouden van Activity Mappen. Als om het even welke uitdrukkingen de waarde aanpassen die in de [&#128279;](/help/components/dimensions/activity-map-region.md) dimensie van het Gebied van de Activity Map  wordt verzameld, worden alle gegevens van de Activity Map verwijderd uit de slag.

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
