---
description: Hiermee definieert u algemene instellingen voor een e-commercewebsite.
title: Commerce
feature: Report Suite Settings
exl-id: 90e5d446-10b8-4d40-8bd0-8b13e1c2f603
source-git-commit: 9057cc83881a72fa039e9398ed3daaf4259ef2bf
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 22%

---

# Commerce

Hiermee definieert u algemene instellingen voor een e-commercewebsite.

| Conversievariabelen | Type | Subrelaties | Toewijzing | Verlopen | `s_code` variabele |
|---|---|---|---|---|---|
| Interne aanbiedingen | String | Basis | Recentste (laatste) | Bezoek | `evar1` |
| Algemene zoektermen | String | Basis | Recentste (laatste) | Bezoek | `evar2` |
| Categorie Merchandising | String | Basis | Recentste (laatste) | Bezoek | `evar3` |
| Handelsvariabele 4 | String | Basis | Recentste (laatste) | Bezoek | `evar4` |
| Handelsvariabele 5 | String | Basis | Recentste (laatste) | Bezoek | `evar5` |

| Gebeurtenissen geslaagd | Type | `s_code` variabele |
|---|---|---|
| Registraties | Teller (geen subrelaties) | `event1` |
| Aangepaste gebeurtenissen 1-5 | Teller (geen subrelaties) | `event1, event2, event3, event4, event5` |

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
