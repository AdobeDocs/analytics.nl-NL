---
title: Koppeling Activity Mappen per regio
description: Een samengevoegde waarde van de koppeling en het gebied.
feature: Dimensions
role: User, Admin
source-git-commit: 65e75a1c2b39823e72abfb0e5b61122c62f1f013
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---

# Koppeling Activity Mappen per regio

De &quot;Verbinding van de Activity Map door Gebied&quot;[ dimensie ](overview.md) toont een aaneenschakeling van [ de Verbinding van de Activity Map ](activity-map-link.md) en [ Gebied van de Activity Map ](activity-map-link-by-region.md). Deze dimensie is handig wanneer u koppelingen hebt met dezelfde naam, maar in verschillende gebieden van uw site. Als u bijvoorbeeld meerdere koppelingen naar uw homepage hebt met het label &#39;Home&#39;, kunt u deze dimensie gebruiken om die koppelingen in elk sitegebied te onderscheiden.

## Deze dimensie vullen met gegevens

Deze afmeting wint gegevens van de [ variabelen van de Contextgegevens ](/help/implement/vars/page-vars/contextdata.md) terug `c.a.activitymap.link` en `c.a.activitymap.region`. Deze twee waarden worden aaneengeschakeld en door een pijp (`|`) gescheiden. Als uw implementatie [ Activity Map ](/help/analyze/activity-map/overview.md) gebruikt, verzamelen deze variabelen van contextgegevens automatisch gegevens wanneer de verbindingen worden geklikt.

## Dimension-items

De punten van het Dimension omvatten waarden van [ Verbinding van de Activity Map ](activity-map-link.md) en [ Gebied van de Activity Map ](activity-map-link-by-region.md). De sitestructuur en -implementatie van uw organisatie bepalen de exacte verzamelde waarden.
