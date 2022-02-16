---
description: Definieert gemeenschappelijke instellingen voor banken en andere instellingen die toegang verlenen tot onlineservices.
title: Financiële diensten
feature: Report Suite Settings
exl-id: 2ab435e2-3fc7-46f9-aee9-961f6730f3e8
source-git-commit: 72bd67179e003b70233d863d34153fec77548256
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 21%

---

# Financiële diensten

Definieert gemeenschappelijke instellingen voor banken en andere instellingen die toegang verlenen tot onlineservices.

| Conversievariabelen (eVars) | Type | Subrelaties | Toewijzing | Verlopen | `s_code` variabele |
|---|---|---|---|---|---|
| Interne promotie | String | Basis | Recentste (laatste) | Bezoek | `evar1` |
| Algemene zoektermen | String | Basis | Recentste (laatste) | Bezoek | `evar2` |
| Self-Service-gebeurtenistype | String | Basis | Recentste (laatste) | Bezoek | `evar3` |

Geen succesgebeurtenissen worden gevormd door dit malplaatje van de rapportreeks.

| Custom Insight-variabelen | `s_code` variabele |
|---|---|
| Beveiligen/niet-beveiligen | `prop1` |
| Verkeerseigenschap 2 - 5 | `prop2, prop3, prop4, prop5` |

De volgende lijst bevat een lijst van de standaardhandelgebeurtenissen. De aanvankelijke configuratie voor deze gebeurtenissen is identiek in alle malplaatjes van de rapportreeks. Gebeurtenissen met een s_code-variabele van N.v.t. hoeven niet te worden ingesteld, ze worden automatisch verschaft.

| Standard Commerce-gebeurtenissen | Type | `s_code` variabele |
|---|---|---|
| Omzet | Teller | `purchase` |
| Orders | Teller | `purchase` |
| Eenheden | Teller | `purchase` |
| Houtskaarten | Teller | `scOpen` |
| Weergaven winkelwagen | Teller | `scView` |
| Instanties | Teller | N.v.t. |
| Betalingen | Teller | `scCheckout` |
| Toevoegingen aan winkelwagen | Teller | `scAdd` |
| Verwijderingen uit winkelwagen | Teller | `scRemove` |
| Bezoeken | Teller (geen subrelaties) | N.v.t. |
| Paginaweergaven | Teller (geen subrelaties) | N.v.t. |
| Dagelijkse unieke bezoekers | Teller (geen subrelaties) | N.v.t. |
| Unieke bezoekers | Teller (geen subrelaties) | N.v.t. |
