---
description: Hiermee definieert u algemene instellingen voor een website die inhoud samenvoegt, zoals een nieuwsportaal.
title: Verzamel-portal
feature: Admin Tools
uuid: d227c209-4d88-4eff-b126-994b2a179c51
exl-id: 48f57f27-289c-4e26-9fb2-e34d48c1f2e6
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 22%

---

# Verzamel-portal

Hiermee definieert u algemene instellingen voor een website die inhoud samenvoegt, zoals een nieuwsportaal.

| Conversievariabelen | Type | Subrelaties | Toewijzing | Verlopen | `s_code` variabele |
|---|---|---|---|---|---|
| Interne campagne | String | Basis | Recentste (laatste) | Bezoek | `evar1` |
| Algemene zoektermen | String | Basis | Recentste (laatste) | Bezoek | `evar2` |
| Referentiecategorie | String | Basis | Recentste (laatste) | Bezoek | `evar3` |

| Gebeurtenissen geslaagd | Type | `s_code` variabele |
|---|---|---|
| Aanmelden | Teller (geen subrelaties) | `event1` |
| Referentieweergave | Teller (geen subrelaties) | `event2` |
| Verwijzing klikt | Teller (geen subrelaties) | `event3` |

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
