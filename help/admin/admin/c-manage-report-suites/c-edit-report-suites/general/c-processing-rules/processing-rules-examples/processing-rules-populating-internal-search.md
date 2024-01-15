---
description: Als u een algemene variabele, zoals q, gebruikt om zoektermen te vullen, kunt u verwerkingsregels gebruiken om de eVar Interne zoektermen met deze waarden te vullen.
subtopic: Processing rules
title: Interne zoektermen vullen met een parameter voor een queryreeks
feature: Admin Tools
role: Admin
exl-id: bc7cc712-0f2a-4260-a82c-ad0e48149e73
source-git-commit: 429aaa43fdae669350bdb5a5a54a7d4b9b1c65f2
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 1%

---

# Interne zoektermen vullen met een parameter voor een queryreeks

Als u een algemene variabele, zoals q, gebruikt om zoektermen te vullen, kunt u verwerkingsregels gebruiken om de eVar Interne zoektermen met deze waarden te vullen.

De het koordwaarden van de vraag moeten in Unicode of UTF-8 worden gecodeerd om door verwerkingsregels te worden gelezen.

| Regelset | Waarde |
|---|---|
| Voorwaarde | Als parameter q van queryreeks is ingesteld |
| Handeling | Waarde van interne zoektermen overschrijven naar parameter q van queryreeks |

Bijvoorbeeld:

![](assets/populate-internal-search-terms.png)
