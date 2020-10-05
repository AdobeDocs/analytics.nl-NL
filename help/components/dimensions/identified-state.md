---
title: Status geïdentificeerd
description: Een markering die de herkenning door de apparaatgrafiek bepaalt.
translation-type: tm+mt
source-git-commit: 60fe85adaebee8ca390e59727dda949c12c1ee26
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# Status geïdentificeerd

De dimensie &#39;Identified state&#39; is specifiek voor [cross-device Analytics](../cda/overview.md) virtuele rapportsuites. Het meldt of Experience Cloud-id wordt herkend door de apparaatgrafiek op het moment dat het rapport wordt uitgevoerd. Deze dimensie is handig om te begrijpen hoe goed CDA gegevens heft of comprimeert.

## Deze dimensie vullen met gegevens

Zolang u Analytics [van](../cda/overview.md) het apparaat voor een virtuele rapportreeks wordt gevormd, werkt deze afmeting uit de doos.

## Dimension-items

Dimension-items zijn onder andere `"Identified"` en `"Unidentified"`.

* **`"Identified"`**: De apparaatgrafiek herkent de Experience Cloud-id die aan de treffer is gekoppeld.
* **`"Unidentified"`**: De apparaatgrafiek herkent de Experience Cloud-id niet of de treffer heeft geen Experience Cloud-id.
