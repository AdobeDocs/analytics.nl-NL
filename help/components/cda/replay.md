---
title: Hoe herspeelt u
description: Begrijp het concept "replay"in Cross-Device Analytics
translation-type: tm+mt
source-git-commit: 2230fa2c48358346d1d449f2db335ff75c6b1631
workflow-type: tm+mt
source-wordcount: '624'
ht-degree: 0%

---


# Hoe herspeelt u

Analytics maakt twee gegevenscontroles op verschillende apparaten in een virtuele rapportsuite:

* **Levend stitching**: CDA probeert elke hit te stikken terwijl hij binnenkomt. Netto nieuwe apparaten aan de rapportreeks die nooit het programma hebben geopend worden typisch niet vastgemaakt op dit niveau. Apparaten die al zijn herkend, worden direct vastgezet.
* **Opnieuw afspelen**: Ongeveer eens per week, &quot;herspeelt&quot;CDA gegevens die op unieke herkenningstekens worden gebaseerd het heeft geleerd. In dit stadium worden nieuwe apparaten aan de rapportsuite vastgezet.

## Voorbeeldtabel

In de volgende tabellen ziet u hoe beide CDA-methoden ([veldgebaseerde stitching](field-based-stitching.md) en [apparaatgrafiek](device-graph.md)) het aantal unieke personen berekenen:

### Levend stitching

Zodra een treffer is verzameld, probeert de CDA deze aan bekende apparaten te hechten. Overweeg het volgende voorbeeld, waar het Loodje twee apparaten gebruikt.

*Gegevens zoals deze worden weergegeven op de dag waarop ze worden verzameld:*

| Tijdstempel | ECID | eVar1 of CustomerID | Toelichting bij treffer | Metrische personen (cumulatief) die de Grafiek van het Apparaat gebruiken | Metrische personen (cumulatief) die op veld gebaseerde stitching gebruiken |
| --- | --- | --- | --- | --- | --- |
| `1` | `246` | - | Bob op zijn desktopcomputer, niet geverifieerd | `1` (246) | `1` (246) |
| `2` | `246` | `Bob` | Bob meldt zich aan op zijn bureaublad | `1` (246) | `2` (246 en Bob) |
| `3` | `3579` | - | Bob op zijn mobiele apparaat, niet geverifieerd | `2` (246 en 3579) | `3` (246, Bob en 3579) |
| `4` | `3579` | `Bob` | Bob meldt zich aan op mobile | `2` (246 en 3579) | `3` (246, Bob en 3579) |
| `5` | `246` | - | Bob benadert uw site opnieuw op het bureaublad, zonder verificatie | `2` (246 en 3579) | `3` (246, Bob en 3579) |
| `6` | `246` | `Bob` | Bob meldt zich opnieuw aan via desktop | `2` (246 en 3579) | `3` (246, Bob en 3579) |
| `7` | `3579` | - | Bob benadert uw site opnieuw op mobile | `2` (246 en 3579) | `3` (246, Bob en 3579) |
| `8` | `3579` | `Bob` | Bob meldt zich opnieuw aan via mobile | `2` (246 en 3579) | `3` (246, Bob en 3579) |

Zowel niet-geverifieerde als geverifieerde hits op nieuwe apparaten worden als afzonderlijke personen geteld (tijdelijk).

* **Als u de apparaatgrafiek gebruikt,** worden niet-geverifieerde treffers op herkende apparaten live-gezet zodra een cluster door de apparaatgrafiek wordt gepubliceerd. Het publiceren van clusters duurt van drie uur tot twee weken.

   Een derde cumulatieve persoon wordt ook toegevoegd wanneer een cluster wordt gepubliceerd. Deze derde persoon vertegenwoordigt de cluster zelf, naast de individuele apparaten. Deze derde &quot;persoon&quot; blijft bestaan totdat de gegevens worden weergegeven.

   De attributie werkt pas over apparaten nadat een cluster wordt gepubliceerd, en zelfs dan slechts leven-hetches van dat punt voorwaarts. In het bovenstaande voorbeeld worden nog geen van de hits op verschillende apparaten geplaatst. De attributie van het dwars-apparaat op bestaande klusjes werkt pas na het opnieuw spelen stitching.
* **Als u stitching op basis van velden gebruikt,** worden niet-geverifieerde treffers op herkende apparaten vanaf dat punt live-stitched.

   Attributie werkt zodra de identificerende douanevariabele aan een apparaat bindt. In het bovenstaande voorbeeld worden alle treffers, behalve hits 1 en 3, in een live-stitched weergegeven (ze gebruiken allemaal de `Bob` id). Attributie werkt bij hits 1 en 3 na het opnieuw afspelen van stitching.

### Replay stitching

Ongeveer eens per week herberekent CDA historische gegevens op basis van de apparaten die het nu herkent. Als een apparaat aanvankelijk gegevens verzendt terwijl niet voor authentiek verklaard en dan login, CDA die niet voor authentiek verklaarde klappen aan de correcte persoon bindt. In de volgende tabel worden dezelfde gegevens weergegeven als hierboven, maar worden verschillende getallen weergegeven op basis van het opnieuw afspelen van de gegevens.

*Dezelfde gegevens na afspelen:*

| Tijdstempel | ECID | eVar1 of CustomerID | Toelichting bij treffer | Metrische personen (cumulatief) die de Grafiek van het Apparaat gebruiken | Metrische personen (cumulatief) die op veld gebaseerde stitching gebruiken |
| --- | --- | --- | --- | --- | --- |
| `1` | `246` | - | Bob op zijn desktopcomputer, niet geverifieerd | `1` (Cluster1) | `1` (Bob) |
| `2` | `246` | `Bob` | Bob meldt zich aan op zijn bureaublad | `1` (Cluster1) | `1` (Bob) |
| `3` | `3579` | - | Bob op zijn mobiele apparaat, niet geverifieerd | `1` (Cluster1) | `1` (Bob) |
| `4` | `3579` | `Bob` | Bob meldt zich aan op mobile | `1` (Cluster1) | `1` (Bob) |
| `5` | `246` | - | Bob benadert uw site opnieuw op het bureaublad, zonder verificatie | `1` (Cluster1) | `1` (Bob) |
| `6` | `246` | `Bob` | Bob meldt zich opnieuw aan via desktop | `1` (Cluster1) | `1` (Bob) |
| `7` | `3579` | - | Bob benadert uw site opnieuw op mobile | `1` (Cluster1) | `1` (Bob) |
| `8` | `3579` | `Bob` | Bob meldt zich opnieuw aan via mobile | `1` (Cluster1) | `1` (Bob) |

## Opnieuw

* **Als u een apparaatgrafiek gebruikt,** worden gegevens vastgezet wanneer een cluster wordt gepubliceerd (doorgaans 3 uur tot 2 weken).
* **Als u op velden gebaseerde stitching gebruikt,** worden bekende apparaten onmiddellijk vastgezet door gegevens die minder dan een week oud zijn, maar worden nieuwe of niet-herkende apparaten niet onmiddellijk vastgezet.
* De gegevens worden één keer per week herhaald, en verandert historische gegevens in de virtuele rapportreeks die op apparaten wordt gebaseerd het heeft geleerd om zich te identificeren.
