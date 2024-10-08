---
title: Hoe herspeelt u?
description: Begrijp het concept "replay"in Cross-Device Analytics
exl-id: 0b7252ff-3986-4fcf-810a-438d9a51e01f
feature: CDA
role: Admin
source-git-commit: cfa5cc02ba3a7349b51a904f29bab533c0f1c603
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 0%

---

# Hoe herspeelt u?

{{available-existing-customers}}

Analytics voor verschillende apparaten maakt twee gegevenscontroles in een virtuele rapportsuite:

* **Levend-stitching**: CDA probeert om elke hit te stikken aangezien het binnen komt. Netto nieuwe apparaten aan de rapportreeks die nooit het programma hebben geopend worden typisch niet vastgemaakt op dit niveau. Apparaten die al zijn herkend, worden direct vastgezet.
* **Replay**: Ongeveer eens per week, &quot;replay&quot;CDA gegevens die op unieke herkenningstekens worden gebaseerd het heeft geleerd. In dit stadium worden nieuwe apparaten aan de rapportsuite vastgezet.

## Voorbeeldtabel

De volgende lijsten illustreren hoe zowel CDA methodes ([ op gebied-gebaseerde het stitching ](field-based-stitching.md) en [ grafiek van het Apparaat ](device-graph.md)) het aantal unieke mensen berekenen:

### Levend stitching

Zodra een treffer is verzameld, probeert de CDA deze aan bekende apparaten te hechten. Overweeg het volgende voorbeeld, waar het Loodje twee apparaten gebruikt.

*Gegevens aangezien het lijkt de dag het wordt verzameld:*

| Tijdstempel | ECID | eVar1 of CustomerID | Toelichting bij treffer | Metrische personen (cumulatief) met apparaatgrafiek | Metrische personen (cumulatief) die op veld gebaseerde stitching gebruiken |
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

* **als het gebruiken van de apparatengrafiek,** niet voor authentiek verklaarde hits op erkende apparaten levend-gestikt zijn zodra een cluster door de apparatengrafiek wordt gepubliceerd. Het publiceren van clusters duurt van drie uur tot twee weken.

  Een derde cumulatieve persoon wordt ook toegevoegd wanneer een cluster wordt gepubliceerd. Deze derde persoon vertegenwoordigt de cluster zelf, naast de individuele apparaten. Deze derde &quot;persoon&quot; blijft bestaan totdat de gegevens worden weergegeven.

  De attributie werkt pas over apparaten nadat een cluster wordt gepubliceerd, en zelfs dan slechts leven-hetches van dat punt voorwaarts. In het bovenstaande voorbeeld worden nog geen van de hits op verschillende apparaten geplaatst. De attributie van het dwars-apparaat op bestaande klusjes werkt pas na het opnieuw spelen stitching.
* **als het gebruiken van op gebied-gebaseerde het stitching,** niet voor authentiek verklaarde hits op erkende apparaten van dat punt voorwaarts wordt vastgezet.

  Attributie werkt zodra de identificerende douanevariabele aan een apparaat bindt. In het bovenstaande voorbeeld worden alle treffers, behalve hits 1 en 3, in een live-stitched weergegeven (ze gebruiken allemaal de id `Bob` ). Attributie werkt bij hits 1 en 3 na het opnieuw afspelen van stitching.

>[!NOTE]
>
>Tijdgestempelde hits ouder dan 12 uur worden niet in de live flow vastgezet. Deze hits worden echter wel opgenomen in de optie voor opnieuw afspelen, zolang ze maar in het terugkijkvenster voor opnieuw afspelen vallen.

### Replay stitching

Replay komt of dagelijks of wekelijks voor, afhankelijk van hoe u CDA om vroeg te worden gevormd. Tijdens replay, probeert CDA historische gegevens binnen een bepaald terugkijkvenster opnieuw te verklaren:

* Dagelijks opnieuw afspelen gebruikt een terugkijkvenster van 1 dag
* Wekelijks opnieuw afspelen gebruikt een terugkijkvenster van 7 dagen.

Als een apparaat aanvankelijk gegevens verzendt terwijl niet voor authentiek verklaard en dan login, CDA die niet voor authentiek verklaarde klappen aan de correcte persoon bindt. In de volgende tabel worden dezelfde gegevens weergegeven als hierboven, maar worden verschillende getallen weergegeven op basis van het opnieuw afspelen van de gegevens.

*De zelfde gegevens na replay:*

| Tijdstempel | ECID | eVar1 of CustomerID | Toelichting bij treffer | Metrische personen (cumulatief) met apparaatgrafiek | Metrische personen (cumulatief) die op veld gebaseerde stitching gebruiken |
| --- | --- | --- | --- | --- | --- |
| `1` | `246` | - | Bob op zijn desktopcomputer, niet geverifieerd | `1` (Cluster1) | `1` (Bob) |
| `2` | `246` | `Bob` | Bob meldt zich aan op zijn bureaublad | `1` (Cluster1) | `1` (Bob) |
| `3` | `3579` | - | Bob op zijn mobiele apparaat, niet geverifieerd | `1` (Cluster1) | `1` (Bob) |
| `4` | `3579` | `Bob` | Bob meldt zich aan op mobile | `1` (Cluster1) | `1` (Bob) |
| `5` | `246` | - | Bob benadert uw site opnieuw op het bureaublad, zonder verificatie | `1` (Cluster1) | `1` (Bob) |
| `6` | `246` | `Bob` | Bob meldt zich opnieuw aan via desktop | `1` (Cluster1) | `1` (Bob) |
| `7` | `3579` | - | Bob benadert uw site opnieuw op mobile | `1` (Cluster1) | `1` (Bob) |
| `8` | `3579` | `Bob` | Bob meldt zich opnieuw aan via mobile | `1` (Cluster1) | `1` (Bob) |
