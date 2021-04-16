---
description: U kunt een variabele vullen met een parameter van een queryreeks.
subtopic: Processing rules
title: Een campagne-id invullen op basis van een queryreeksparameter
feature: Admin Tools
uuid: 2bc61f9f-d8d2-41b7-bd39-4a9df30ff013
exl-id: 526d2727-b7f6-4b41-be86-e5f5bc5e6c2b
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 19%

---

# Een campagne-id invullen op basis van een queryreeksparameter

U kunt een variabele vullen met een parameter van een queryreeks.

In de meeste gevallen gebruikt u een plug-in om variabelen van de queryreeks te vullen. Als een typefout of een vergelijkbare uitgave voorkomt dat de waarde wordt gevuld, kunt u de variabele vullen met verwerkingsregels.

Controleer altijd of een waarde leeg is of de verwachte waarde bevat voordat u deze overschrijft.

| Regelset | Waarde |
|---|---|
| Voorwaarde | Campagne is niet ingesteld |
| Handeling | Overschrijf de waarde van cpid voor parameter van campagne naar query-tekenreeks |

Bijvoorbeeld:

![](assets/set-campaign-conditionally.png)
