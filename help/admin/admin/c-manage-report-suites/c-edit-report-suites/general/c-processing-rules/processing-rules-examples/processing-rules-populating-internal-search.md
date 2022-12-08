---
description: Als u een algemene variabele, zoals q, gebruikt om zoektermen te vullen, kunt u verwerkingsregels gebruiken om de eVar Interne zoektermen met deze waarden te vullen.
subtopic: Processing rules
title: Interne zoektermen invullen op basis van een queryreeksparameter
feature: Admin Tools
uuid: 05ae2b0a-8797-468c-8f59-643beac614c5
exl-id: bc7cc712-0f2a-4260-a82c-ad0e48149e73
source-git-commit: 71ff81a0ae67c6f4cc9a8df567e27223cc63f18c
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 17%

---

# Interne zoektermen invullen op basis van een queryreeksparameter

Als u een algemene variabele, zoals q, gebruikt om zoektermen te vullen, kunt u verwerkingsregels gebruiken om de eVar Interne zoektermen met deze waarden te vullen.

De het koordwaarden van de vraag moeten in Unicode of UTF-8 worden gecodeerd om door verwerkingsregels te worden gelezen.

| Regelset | Waarde |
|---|---|
| Voorwaarde | Als parameter q van queryreeks is ingesteld |
| Handeling | Waarde van interne zoektermen overschrijven naar parameter q van queryreeks |

Bijvoorbeeld:

![](assets/populate-internal-search-terms.png)
