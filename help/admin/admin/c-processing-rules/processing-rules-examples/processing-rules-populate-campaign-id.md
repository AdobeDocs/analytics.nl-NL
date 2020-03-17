---
description: U kunt een variabele vullen met een parameter van een queryreeks.
subtopic: Processing rules
title: Een campagne-id vullen met een parameter voor een queryreeks
topic: Admin tools
uuid: 2bc61f9f-d8d2-41b7-bd39-4a9df30ff013
translation-type: tm+mt
source-git-commit: 2ffa989156dd9bc4f6ef9a216e8c06425cc39440

---


# Een campagne-id vullen met een parameter voor een queryreeks

U kunt een variabele vullen met een parameter van een queryreeks.

In de meeste gevallen gebruikt u een plug-in om variabelen van de queryreeks te vullen. Als een typefout of een vergelijkbare uitgave voorkomt dat de waarde wordt gevuld, kunt u de variabele vullen met verwerkingsregels.

Controleer altijd of een waarde leeg is of de verwachte waarde bevat voordat u deze overschrijft.

| Regelset | Waarde |
|---|---|
| Voorwaarde | Campagne is niet ingesteld |
| Handeling | Overschrijf de waarde van cpid voor parameter van campagne naar query-tekenreeks |

Bijvoorbeeld:

![](assets/set-campaign-conditionally.png)

