---
title: ActivityMap.linkExclusions
description: Filter Activity Map-gegevens op naam van koppeling.
role: Admin, Developer
feature: Appmeasurement Implementation
exl-id: 9fc95016-362d-4c21-806e-e23adce9b6f7
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---

# ActivityMap.linkExclusions

De `ActivityMap.linkExclusions` variabele laat u selectief de gegevens van Activity Map filtreren of uitsluiten die op de tekst in de [ worden gebaseerd van de Verbinding van Activity Map ](/help/components/dimensions/activity-map-link.md) afmeting.

## Uitsluitingen koppelen in de extensie Web SDK

Wanneer **[!UICONTROL Enable click data collection]** is ingeschakeld, gebruikt u het codeblok **[!UICONTROL Filter click properties]** callback. Binnen dit codeblok kunt u de waarde van `content.linkName` controleren en de waarde wijzigen of de verzameling van gegevens voor het bijhouden van koppelingen opgeven.

## Uitsluitingen koppelen in de Web SDK JavaScript-bibliotheek

Wanneer [`clickCollectionEnabled` ](https://experienceleague.adobe.com/nl/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled) wordt toegelaten, gebruik `filterClickDetails` callback in het `clickCollection` voorwerp. Binnen deze callback kunt u de waarde van `linkName` controleren en de waarde wijzigen of de verzameling van gegevens voor het bijhouden van koppelingen opgeven.

```js
alloy("configure", {
  clickCollectionEnabled: true,
  clickCollection: {
    filterClickDetails: function(content) {
      // If the link is a clickable telephone number, anonymize it
      if(content.linkUrl.includes("tel:")) {
        content.linkName = content.linkUrl = "Phone number";
      }
      // If the link is an email address, anonymize it
      if(content.linkUrl.includes("mailto:")) {
        content.linkName = content.linkUrl = "Email address";
      }
    }
  }
});
```

## Uitsluitingen koppelen met de Adobe Analytics-extensie

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de AppMeasurement-syntaxis.

## s.ActivityMap.linkExclusions gebruiken AppMeasurement

De variabele `s.ActivityMap.linkExclusions` is een tekenreeks met door komma&#39;s gescheiden waarden van zinnen die worden uitgesloten van het bijhouden van Activity Map. Als om het even welke uitdrukkingen de waarde aanpassen die in de [ dimensie van de Verbinding van Activity Map ](/help/components/dimensions/activity-map-link.md) wordt verzameld, worden alle gegevens van Activity Map verwijderd uit de slag. Deze variabele kijkt naar `linkName`, niet naar `linkUrl` .

```html
<script>
  var s = s_gi("examplersid");
  s.ActivityMap.linkExclusions = "Contact";
</script>

<!-- Clicking this link tracks normally -->
<a href="products.html">View our products</a>

<!-- Activity Map data is not tracked for this link -->
<a href="mailto:user@example.com">Contact this user</a>
```
