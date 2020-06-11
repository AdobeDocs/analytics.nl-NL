---
title: AM/PM
description: Hiermee wordt bepaald of de treffer heeft plaatsgevonden tijdens uur 's ochtends of 's middags.
translation-type: tm+mt
source-git-commit: 05ea2778cd5cd324c660fd0f1d2ac02373829f0f
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---


# AM/PM

De dimensie &#39;AM/PM&#39; geeft inzicht in of de hit heeft plaatsgevonden tijdens de uren &#39;AM&#39; of &#39;PM&#39;. De tijd van de treffer is gebaseerd op de tijdzone [van de](/help/admin/admin/general-acct-settings-admin.md)rapportreeks.

## Deze dimensie vullen met gegevens

Deze dimensie werkt buiten de doos. Er zijn geen instellingen om te wijzigen. Zijn enige afhankelijkheid is op de tijdzone van de rapportreeks, die bepaalt welke uren AM zijn en PM zijn.

## Dimensiewaarden

Deze dimensie bevat altijd precies twee afmetingswaarden: `"AM"` en `"PM"`. De waarde Dimensie `"AM"` is van toepassing op alle treffers van 12:00 tot 11:59 AM, terwijl de waarde van de afmeting op alle treffers van 12:00 tot 11:59 PM van toepassing `"PM"` is.
