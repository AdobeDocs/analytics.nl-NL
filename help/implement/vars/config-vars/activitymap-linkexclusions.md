---
title: ActivityMap.linkExclusions
description: Filter de gegevens van de Activity Map op verbindingsnaam.
role: Admin, Developer
feature: Variables
source-git-commit: 05010d58ba2a3376473097e9d4543ee4415e83e1
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---

# ActivityMap.linkExclusions

De `ActivityMap.linkExclusions` variabele laat u selectief Activity Map gegevens filtreren of uitsluiten die op de tekst in de [ worden gebaseerd van de Verbinding van de Activity Map ](/help/components/dimensions/activity-map-link.md) afmeting.

## Uitsluitingen koppelen in de Web SDK-extensie

Wanneer **[!UICONTROL Enable click data collection]** is ingeschakeld, gebruikt u het codeblok **[!UICONTROL Filter click properties]** callback. Binnen dit codeblok kunt u de waarde van `content.linkName` controleren en de waarde wijzigen of de verzameling van gegevens voor het bijhouden van koppelingen opgeven.

## Uitsluitingen koppelen in de Web SDK JavaScript-bibliotheek

Wanneer [`clickCollectionEnabled` ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled) wordt toegelaten, gebruik `filterClickDetails` callback in het `clickCollection` voorwerp. Binnen deze callback kunt u de waarde van `linkName` controleren en de waarde wijzigen of de verzameling van gegevens voor het bijhouden van koppelingen opgeven.

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

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de syntaxis van het AppMeasurement.

## s.ActivityMap.linkExclusions gebruiken AppMeasurement

De variabele `s.ActivityMap.linkExclusions` is een tekenreeks met kommagescheiden waarden van zinnen die worden uitgesloten van bijhouden van Activity Mappen. Als om het even welke uitdrukkingen de waarde aanpassen die in de [ dimensie van de Verbinding van de Activity Map ](/help/components/dimensions/activity-map-link.md) wordt verzameld, worden alle gegevens van de Activity Map verwijderd uit de slag. Deze variabele kijkt naar `linkName`, niet naar `linkUrl` .

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
