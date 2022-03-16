---
title: Bezoeken op één pagina (afmetingen)
description: Een vlag die aangeeft dat het bezoek uit één pagina bestond.
feature: Dimensions
exl-id: f7b58941-add4-4e7b-8645-a64280fd9dcb
source-git-commit: 10ff98f7ca4697afe5c2dae66be415c0d68c4aac
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# Eén pagina bezoeken

*In deze Help-pagina wordt beschreven hoe &#39;Bezoeken van één pagina&#39; werkt als een dimensie. Zie de [Eén pagina bezoeken](../metrics/single-page-visits.md) metrisch voor meer informatie.*

De dimensie &quot;Bezoeken van één pagina&quot; geeft het aantal bezoeken weer dat uit één unieke [Pagina](page.md) dimensie-item. Het is de dimensie van de [Eén pagina bezoeken](../metrics/single-page-visits.md) metrisch.

Deze dimensie wordt meestal gebruikt als een component binnen [segmentatie](../segmentation/seg-home.md). Het wordt typisch niet gebruikt als dimensie in rapporten.

## Deze dimensie vullen met gegevens

Deze dimensie werkt uit de doos voor alle implementaties. Als een rapportsuite gegevens bevat, werkt deze dimensie.

## Dimension-items

Het enige dimensie-item is `"Enabled"`. Als een bezoek uit één pagina bestaat, wordt de hit ingesteld op deze waarde. Alle andere treffers worden uit dit verslag weggelaten.
