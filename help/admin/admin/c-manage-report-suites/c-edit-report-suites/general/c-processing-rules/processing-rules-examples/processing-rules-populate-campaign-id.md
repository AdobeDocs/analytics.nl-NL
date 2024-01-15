---
description: U kunt een variabele vullen met een parameter van een queryreeks.
subtopic: Processing rules
title: Een campagne-id vullen met een parameter voor een queryreeks
feature: Admin Tools
role: Admin
exl-id: 526d2727-b7f6-4b41-be86-e5f5bc5e6c2b
source-git-commit: 429aaa43fdae669350bdb5a5a54a7d4b9b1c65f2
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 1%

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
