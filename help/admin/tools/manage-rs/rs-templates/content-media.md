---
description: Definieert algemene instellingen voor een website die originele inhoud ontwikkelt en artikelen en video's weergeeft.
title: Inhoud en media
feature: Report Suite Settings
exl-id: 9983ff86-9341-4b01-b4f3-41042874a9fb
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 9%

---

# Inhoud en media

Definieert algemene instellingen voor een website die originele inhoud ontwikkelt en artikelen en video&#39;s weergeeft.

| Conversievariabelen | Type | Subrelaties | Toewijzing | Verlopen | `s_code` variable |
|---|---|---|---|---|---|
| Interne campagne | String | Basis | Recentste (laatste) | Bezoek | `evar1` |
| Algemene zoektermen | String | Basis | Recentste (laatste) | Bezoek | `evar2` |
| Commerce-variabele 3 | String | Basis | Recentste (laatste) | Bezoek | `evar3` |
| Commerce-variabele 4 | String | Basis | Recentste (laatste) | Bezoek | `evar4` |

| Gebeurtenissen geslaagd | Type | `s_code` variable |
|---|---|---|
| Registraties | Teller (geen subrelaties) | `event1` |
| E-mailregistratie | Teller (geen subrelaties) | `event2` |
| Abonnementen | Teller (geen subrelaties) | `event3` |
| Paginaweergaven | Teller (geen subrelaties) | `event4` |
| Advertentie-impressies | Teller (geen subrelaties) | `event5` |
| Advertentieklikken | Teller (geen subrelaties) | `event6` |

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
