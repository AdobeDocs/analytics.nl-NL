---
description: Hiermee verschaft u algemene instellingen voor een website die artikelen en video's met productondersteuning biedt.
title: Ondersteuningsmedia
feature: Report Suite Settings
exl-id: f522173a-8f58-4fa4-868b-251158a71e26
source-git-commit: 9057cc83881a72fa039e9398ed3daaf4259ef2bf
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 21%

---

# Ondersteuningsmedia

Hiermee verschaft u algemene instellingen voor een website die artikelen en video&#39;s met productondersteuning biedt.

| Conversievariabelen | Type | Subrelaties | Toewijzing | Verlopen | `s_code` variabele |
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
