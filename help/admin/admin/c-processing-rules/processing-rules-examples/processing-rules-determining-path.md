---
description: U kunt de waarde van een eVar aan een steun kopiëren om het kleven toe te laten.
subtopic: Processing rules
title: Een pad bepalen door een eVar-waarde naar een pop-up te kopiëren
topic: Admin tools
uuid: 8d7647c7-aa91-466b-8d31-fb4dce83f04a
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Een pad bepalen door een eVar-waarde naar een pop-up te kopiëren

U kunt de waarde van een eVar aan een steun kopiëren om het kleven toe te laten.

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

