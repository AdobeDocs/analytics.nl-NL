---
title: AM/PM
description: Hiermee wordt bepaald of de treffer heeft plaatsgevonden tijdens uur 's ochtends of 's middags.
feature: Dimensions
exl-id: 93fcdb9f-2ba3-402c-a389-b02ed8c990d2
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---

# AM/PM

De &quot;AM/PM&quot;dimensie [ ](overview.md) verstrekt insight op als de slag tijdens AM of PM uren gebeurde. De tijd van de klap is gebaseerd op de [ tijdzone van de rapportreeks ](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md).

## Deze dimensie vullen met gegevens

Deze dimensie werkt buiten de doos. Er zijn geen instellingen om te wijzigen. Zijn enige afhankelijkheid is op de tijdzone van de rapportreeks, die bepaalt welke uren AM zijn en PM zijn.

## Dimension-objecten

Deze dimensie bevat altijd precies twee afmetingsitems: `"AM"` en `"PM"` . Het afmetingspunt `"AM"` is op alle treffers van 12 :00 AM aan 11 :59 AM van toepassing, terwijl het afmetingspunt `"PM"` op alle treffers van 12 :00 PM tot 11 :59 PM van toepassing is.
