---
description: Hiermee definieert u algemene instellingen voor een e-commercewebsite.
title: Handel
topic: Admin tools
uuid: 85fc235d-0180-4245-b831-0243ebe3c40c
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Handel

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

| Aangepaste inzichtvariabelen | `s_code` variabele |
|---|---|
| Verkeerseigenschap 1 - 5 | `prop1, prop2, prop3, prop4, prop5` |

De volgende lijst bevat een lijst van de standaardhandelgebeurtenissen. De aanvankelijke configuratie voor deze gebeurtenissen is identiek in alle malplaatjes van de rapportreeks. Gebeurtenissen met een s_code-variabele van N.v.t. hoeven niet te worden ingesteld, ze worden automatisch verschaft.

| Standard Commerce-gebeurtenissen | Type | `s_code` variabele |
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

