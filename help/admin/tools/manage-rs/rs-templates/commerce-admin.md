---
description: Hiermee definieert u algemene instellingen voor een e-commercewebsite.
title: Commerce
feature: Report Suite Settings
exl-id: 90e5d446-10b8-4d40-8bd0-8b13e1c2f603
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 11%

---

# Commerce

Hiermee definieert u algemene instellingen voor een e-commercewebsite.

| Conversievariabelen | Type | Subrelaties | Toewijzing | Verlopen | `s_code` variable |
|---|---|---|---|---|---|
| Interne aanbiedingen | String | Basis | Recentste (laatste) | Bezoek | `evar1` |
| Algemene zoektermen | String | Basis | Recentste (laatste) | Bezoek | `evar2` |
| Categorie Merchandising | String | Basis | Recentste (laatste) | Bezoek | `evar3` |
| Commerce-variabele 4 | String | Basis | Recentste (laatste) | Bezoek | `evar4` |
| Commerce-variabele 5 | String | Basis | Recentste (laatste) | Bezoek | `evar5` |

| Gebeurtenissen geslaagd | Type | `s_code` variable |
|---|---|---|
| Registraties | Teller (geen subrelaties) | `event1` |
| Aangepaste gebeurtenissen 1-5 | Teller (geen subrelaties) | `event1, event2, event3, event4, event5` |

| Custom Insight-variabelen | `s_code` variable |
|---|---|
| Verkeerseigenschap 1 - 5 | `prop1, prop2, prop3, prop4, prop5` |

De volgende lijst bevat een lijst van de standaardhandelgebeurtenissen. De aanvankelijke configuratie voor deze gebeurtenissen is identiek in alle malplaatjes van de rapportreeks. Gebeurtenissen met een s_code-variabele van N.v.t. hoeven niet te worden ingesteld, ze worden automatisch verschaft.

| Standaard Commerce-gebeurtenissen | Type | `s_code` variable |
|---|---|---|
| Ontvangsten | Teller | `purchase` |
| Orders | Teller | `purchase` |
| Eenheden | Teller | `purchase` |
| Houtskaarten | Teller | `scOpen` |
| Kleuraweergaven | Teller | `scView` |
| Instanties | Teller | N.v.t. |
| Afbeeldingen | Teller | `scCheckout` |
| Extra winkelwagentjes | Teller | `scAdd` |
| Winkelwagentjes | Teller | `scRemove` |
| Bezoeken | Teller (geen subrelaties) | N.v.t. |
| Paginaweergaven | Teller (geen subrelaties) | N.v.t. |
| Dagelijkse unieke bezoekers | Teller (geen subrelaties) | N.v.t. |
| Unieke bezoekers | Teller (geen subrelaties) | N.v.t. |
