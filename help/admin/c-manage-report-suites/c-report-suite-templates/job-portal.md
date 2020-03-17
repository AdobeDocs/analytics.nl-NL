---
description: Hiermee definieert u algemene instellingen voor een zoekwebsite voor een vacature of een carrière.
title: Job Portal
topic: Admin tools
uuid: c33a8e30-eea6-45f5-9568-d64c6753855e
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Job Portal

Hiermee definieert u algemene instellingen voor een zoekwebsite voor een vacature of een carrière.

| Conversievariabelen | Type | Subrelaties | Toewijzing | Verlopen | `s_code` variabele |
|---|---|---|---|---|---|
| Interne promotie | String | Basis | Recentste (laatste) | Bezoek | `evar1` |
| Algemene zoektermen | String | Basis | Recentste (laatste) | Bezoek | `evar2` |
| Self-Service-gebeurtenistype | String | Basis | Recentste (laatste) | Bezoek | `evar3` |

Geen succesgebeurtenissen worden gevormd door dit malplaatje van de rapportreeks.

| Aangepaste inzichtvariabelen | `s_code` variabele |
|---|---|
| Beveiligen/niet-beveiligen | `prop1` |
| Verkeerseigenschap 2 - 5 | `prop2, prop3, prop4, prop5` |

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

