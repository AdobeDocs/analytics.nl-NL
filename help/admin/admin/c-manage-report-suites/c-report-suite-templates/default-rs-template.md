---
description: Vormt verscheidene gemeenschappelijke variabelen en succesgebeurtenissen voor een typische website.
title: Standaardsjabloon
feature: Report Suite Settings
uuid: edcf1b97-4ff2-4e98-b84c-199af2181d68
exl-id: 36aaded4-5c46-41af-a5c6-216bd2fcadb2
source-git-commit: 9057cc83881a72fa039e9398ed3daaf4259ef2bf
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 21%

---

# Standaardsjabloon

Vormt verscheidene gemeenschappelijke variabelen en succesgebeurtenissen voor een typische website.

| Conversievariabelen | Type | Subrelaties | Toewijzing | Verlopen | `s_code` variabele |
|---|---|---|---|---|---|
| Interne campagne | String | Basis | Recentste (laatste) | Bezoek | `evar1` |
| Algemene zoektermen | String | Basis | Recentste (laatste) | Bezoek | `evar2` |
| Handelsvariabele 3 | String | Basis | Recentste (laatste) | Bezoek | `evar3` |
| Handelsvariabele 4 | String | Basis | Recentste (laatste) | Bezoek | `evar4` |

| Gebeurtenissen geslaagd | Type | `s_code` variabele |
|---|---|---|
| Registraties | Teller (geen subrelaties) | `event1` |
| E-mailregistratie | Teller (geen subrelaties) | `event2` |
| Abonnementen | Teller (geen subrelaties) | `event3` |
| Paginaweergaven | Teller (geen subrelaties) | `event4` |
| Advertentie-impressies | Teller (geen subrelaties) | `event5` |
| Advertentieklikken | Teller (geen subrelaties) | `event6` |

| Custom Insight-variabelen | `s_code` variabele |
|---|---|
| Verkeerseigenschap 1 - 5 | `prop1, prop2, prop3, prop4, prop5` |

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
