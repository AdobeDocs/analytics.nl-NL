---
description: U kunt de waarde van een eVar naar een hulpmiddel kopiëren om het plakken toe te laten.
subtopic: Processing rules
title: Een pad bepalen door een eVar-waarde naar een profiel te kopiëren
feature: Admin Tools
role: Admin
exl-id: 23c978b9-a159-4364-9214-561a255d23e4
source-git-commit: 429aaa43fdae669350bdb5a5a54a7d4b9b1c65f2
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 1%

---

# Een pad bepalen door een eVar-waarde naar een profiel te kopiëren

U kunt de waarde van een eVar naar een hulpmiddel kopiëren om het plakken toe te laten.

Bij het instellen van waarden ontvangt de variabele aan de linkerkant de waarde (ook als deze leeg is) van de variabele aan de rechterkant.

| Regelset | Waarde |
|---|---|
| Voorwaarde | Geen (altijd uitvoeren) |
| Handeling | Waarde van Prop1 overschrijven met eVar1 |

U kunt deze regel wijzigen om de waarde van Prop1 slechts te plaatsen als het nog geen waarde bevat, gelijkend op het volgende:

| Regelset | Waarde |
|---|---|
| Voorwaarde | Als Prop1 niet is ingesteld |
| Handeling | Waarde van Prop1 overschrijven met eVar1 |

Bijvoorbeeld:

![](assets/overwrite-empty-prop.png)
