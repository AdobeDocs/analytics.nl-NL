---
title: Weekdag/Weekend
description: Hiermee bepaalt u of de treffer tijdens een weekdag of een weekend heeft plaatsgevonden.
feature: Dimensions
exl-id: c3111cdc-a5f9-4244-a725-b1bb1e72fcff
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---

# Weekdag/Weekend

De &quot;weekdag/week&quot; [dimensie](overview.md) geeft inzicht in de vraag of de aanslag heeft plaatsgevonden tijdens een weekdag (maandag - vrijdag) of weekend (zaterdag - zondag). De tijd van de treffer is gebaseerd op de [tijdzone van rapportsuite](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md).

## Deze dimensie vullen met gegevens

Deze dimensie werkt uit de doos voor alle implementaties. Als een rapportsuite gegevens bevat, werkt deze dimensie.

## Dimension-items

Deze dimensie bevat altijd precies twee dimensieitems: `"Weekday"` en `"Weekend"`. Dimensie-item `"Weekday"` is van toepassing op alle treffers Maandag door Vrijdag, terwijl het afmetingspunt `"Weekend"` van toepassing op alle hits op zaterdag en zondag.
