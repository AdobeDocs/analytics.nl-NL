---
title: Weekdag/Weekend
description: Hiermee bepaalt u of de treffer tijdens een weekdag of een weekend heeft plaatsgevonden.
feature: Dimensions
exl-id: c3111cdc-a5f9-4244-a725-b1bb1e72fcff
source-git-commit: 71ff81a0ae67c6f4cc9a8df567e27223cc63f18c
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---

# Weekdag/Weekend

De dimensie &#39;Weekday/Weekend&#39; geeft inzicht in de vraag of de aanslag heeft plaatsgevonden tijdens een weekdag (maandag - vrijdag) of weekend (zaterdag - zondag). De tijd van de treffer is gebaseerd op de [tijdzone van rapportsuite](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md).

## Deze dimensie vullen met gegevens

Deze dimensie werkt uit de doos voor alle implementaties. Als een rapportsuite gegevens bevat, werkt deze dimensie.

## Dimension-items

Deze dimensie bevat altijd precies twee dimensieitems: `"Weekday"` en `"Weekend"`. Dimensie-item `"Weekday"` is van toepassing op alle hits op maandag t/m vrijdag, terwijl het dimensie-item `"Weekend"` van toepassing op alle hits op zaterdag en zondag.
