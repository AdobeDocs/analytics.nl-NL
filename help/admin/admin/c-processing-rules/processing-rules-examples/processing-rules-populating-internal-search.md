---
description: Als u een algemene variabele, zoals q, gebruikt om zoektermen te vullen, kunt u verwerkingsregels gebruiken om de interne zoektermen Var met deze waarden te vullen.
subtopic: Processing rules
title: Interne zoektermen vullen met een parameter voor een queryreeks
topic: Admin tools
uuid: 05ae2b0a-8797-468c-8f59-643beac614c5
translation-type: tm+mt
source-git-commit: ''

---


# Interne zoektermen vullen met een parameter voor een queryreeks

Als u een algemene variabele, zoals q, gebruikt om zoektermen te vullen, kunt u verwerkingsregels gebruiken om de interne zoektermen Var met deze waarden te vullen.

De het koordwaarden van de vraag moeten in Unicode of UTF-8 worden gecodeerd om door verwerkingsregels te worden gelezen.

| Regelset | Waarde |
|---|---|
| Voorwaarde | Als parameter q van queryreeks is ingesteld |
| Handeling | Waarde van interne zoektermen overschrijven naar parameter q van queryreeks |

Bijvoorbeeld:

![](assets/populate-internal-search-terms.png)

