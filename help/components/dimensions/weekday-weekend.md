---
title: Weekdag/Weekend
description: Hiermee bepaalt u of de treffer tijdens een weekdag of een weekend heeft plaatsgevonden.
feature: Dimensions
exl-id: c3111cdc-a5f9-4244-a725-b1bb1e72fcff
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---

# Weekdag/Weekend

De dimensie &#39;Weekday/Weekend&#39; geeft inzicht in de vraag of de aanslag heeft plaatsgevonden tijdens een weekdag (maandag - vrijdag) of weekend (zaterdag - zondag). De tijd van de treffer is gebaseerd op de [tijdzone van rapportsuite](/help/admin/admin/general-acct-settings-admin.md).

## Deze dimensie vullen met gegevens

Deze dimensie werkt uit de doos voor alle implementaties. Als een rapportsuite gegevens bevat, werkt deze dimensie.

## Dimension-items

Deze dimensie bevat altijd precies twee dimensieitems: `"Weekday"` en `"Weekend"`. Dimensie-item `"Weekday"` is van toepassing op alle hits op maandag t/m vrijdag, terwijl het dimensie-item `"Weekend"` van toepassing op alle hits op zaterdag en zondag.
