---
title: AM/PM
description: Hiermee wordt bepaald of de treffer heeft plaatsgevonden tijdens uur 's ochtends of 's middags.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---


# AM/PM

De dimensie &#39;AM/PM&#39; geeft inzicht in of de hit heeft plaatsgevonden tijdens de uren &#39;AM&#39; of &#39;PM&#39;. De tijd van de treffer is gebaseerd op de tijdzone [van de](/help/admin/admin/general-acct-settings-admin.md)rapportreeks.

## Deze dimensie vullen met gegevens

Deze dimensie werkt buiten de doos. Er zijn geen instellingen om te wijzigen. Zijn enige afhankelijkheid is op de tijdzone van de rapportreeks, die bepaalt welke uren AM zijn en PM zijn.

## Dimensie-items

Deze dimensie bevat altijd precies twee dimensieitems: `"AM"` en `"PM"`. Het item Dimensie `"AM"` is van toepassing op alle hits van 12.00 tot 11.59 uur &#39;s middags, terwijl het item Dimensie van `"PM"` toepassing is op alle hits van 12.00 tot 23.59 uur.
