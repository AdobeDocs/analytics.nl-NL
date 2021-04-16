---
description: U kunt de waarde van een eVar naar een hulpmiddel kopiëren om het plakken toe te laten.
subtopic: Processing rules
title: Een pad bepalen door een eVar-waarde naar een prop te kopiëren
feature: Admin Tools
uuid: 8d7647c7-aa91-466b-8d31-fb4dce83f04a
exl-id: 23c978b9-a159-4364-9214-561a255d23e4
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 20%

---

# Een pad bepalen door een eVar-waarde naar een prop te kopiëren

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
