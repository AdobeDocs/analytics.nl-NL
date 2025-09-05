---
title: Weekdag/Weekend
description: Hiermee bepaalt u of de treffer tijdens een weekdag of een weekend heeft plaatsgevonden.
feature: Dimensions
exl-id: c3111cdc-a5f9-4244-a725-b1bb1e72fcff
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---

# Weekdag/Weekend

De dimensie &quot;Weekday/Weekend&quot;[ ](overview.md) verstrekt insight op als de slag tijdens een weekdag (maandag - vrijdag) of weekend (zaterdag - zondag) gebeurde. De tijd van de klap is gebaseerd op de [ tijdzone van de rapportreeks ](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md).

## Deze dimensie vullen met gegevens

Deze dimensie werkt uit de doos voor alle implementaties. Als een rapportsuite gegevens bevat, werkt deze dimensie.

## Dimension-objecten

Deze dimensie bevat altijd precies twee afmetingsitems: `"Weekday"` en `"Weekend"` . Het dimensie-item `"Weekday"` is van toepassing op alle treffers van maandag tot en met vrijdag, terwijl het dimensie-item `"Weekend"` van toepassing is op alle treffers op zaterdag en zondag.
