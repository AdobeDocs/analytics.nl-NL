---
title: Weekdag/Weekend
description: Hiermee bepaalt u of de treffer tijdens een weekdag of een weekend heeft plaatsgevonden.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# Weekdag/Weekend

De dimensie &#39;Weekday/Weekend&#39; geeft inzicht in de vraag of de aanslag heeft plaatsgevonden tijdens een weekdag (maandag - vrijdag) of weekend (zaterdag - zondag). De tijd van de treffer is gebaseerd op de tijdzone [van de](/help/admin/admin/general-acct-settings-admin.md)rapportreeks.

## Deze dimensie vullen met gegevens

Deze dimensie werkt uit de doos voor alle implementaties. Als een rapportsuite gegevens bevat, werkt deze dimensie.

## Dimensie-items

Deze dimensie bevat altijd precies twee dimensieitems: `"Weekday"` en `"Weekend"`. Het dimensie-item `"Weekday"` is van toepassing op alle treffers van maandag tot en met vrijdag, terwijl het dimensie-item van toepassing `"Weekend"` is op alle treffers op zaterdag en zondag.
