---
title: AM/PM
description: Hiermee wordt bepaald of de treffer heeft plaatsgevonden tijdens uur 's ochtends of 's middags.
feature: Dimensions
exl-id: 93fcdb9f-2ba3-402c-a389-b02ed8c990d2
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---

# AM/PM

De &#39;AM/PM&#39; [dimensie](overview.md) geeft inzicht in of de hit heeft plaatsgevonden tijdens de uren &#39;s ochtends of &#39;s ochtends. De tijd van de treffer is gebaseerd op de [tijdzone van rapportsuite](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md).

## Deze dimensie vullen met gegevens

Deze dimensie werkt buiten de doos. Er zijn geen instellingen om te wijzigen. Zijn enige afhankelijkheid is op de tijdzone van de rapportreeks, die bepaalt welke uren AM zijn en PM zijn.

## Dimension-items

Deze dimensie bevat altijd precies twee dimensieitems: `"AM"` en `"PM"`. Dimensie-item `"AM"` van toepassing op alle treffers van 12:00 tot 11:59 AM, terwijl het afmetingspunt `"PM"` van toepassing op alle hits van 12.00 tot 23.59 uur.
