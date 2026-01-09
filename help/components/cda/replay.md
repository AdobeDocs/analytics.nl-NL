---
title: Hoe herspeelt u?
description: Begrijp het concept "replay"in Cross-Device Analytics
exl-id: 0b7252ff-3986-4fcf-810a-438d9a51e01f
feature: CDA
role: Admin
source-git-commit: f75a1f6d9f08f422595c24760796abf0f8332ddb
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# Hoe herspeelt u?

{{available-existing-customers}}

Analytics voor verschillende apparaten maakt twee gegevenscontroles in een virtuele rapportsuite:

* **Levend-stitching**: CDA probeert om elke hit te stikken aangezien het binnen komt. Netto nieuwe apparaten aan de rapportreeks die nooit het programma hebben geopend worden typisch niet vastgemaakt op dit niveau. Apparaten die al zijn herkend, worden direct vastgezet.
* **Replay**: Ongeveer eens per week, &quot;replay&quot;CDA gegevens die op unieke herkenningstekens worden gebaseerd het heeft geleerd. In dit stadium worden nieuwe apparaten aan de rapportsuite vastgezet.

## Voorbeeldtabel

De volgende lijsten illustreren hoe ([&#x200B; Op gebied-gebaseerd het stitching &#x200B;](field-based-stitching.md) het aantal unieke mensen berekent:

### Levend stitching

Zodra een treffer is verzameld, probeert de CDA deze aan bekende apparaten te hechten. Overweeg het volgende voorbeeld, waar het Loodje twee apparaten gebruikt.

*Gegevens aangezien het lijkt de dag het wordt verzameld:*

| Tijdstempel | ECID | eVar1 of CustomerID | Toelichting bij treffer | Mensen (cumulatief) die op het veld gebaseerde stitching gebruiken |
| --- | --- | --- | --- | --- | 
| `1` | `246` | - | Bob op zijn desktopcomputer, niet geverifieerd | `1` (246) |
| `2` | `246` | `Bob` | Bob meldt zich aan op zijn bureaublad | `2` (246 en Bob) |
| `3` | `3579` | - | Bob op zijn mobiele apparaat, niet geverifieerd | `2` (246 en 3579) | `3` (246, Bob en 3579) |
| `4` | `3579` | `Bob` | Bob meldt zich aan op mobile | `3` (246, Bob en 3579) |
| `5` | `246` | - | Bob benadert uw site opnieuw op het bureaublad, zonder verificatie | | `3` (246, Bob en 3579) |
| `6` | `246` | `Bob` | Bob meldt zich opnieuw aan via desktop | `3` (246, Bob en 3579) |
| `7` | `3579` | - | Bob benadert uw site opnieuw op mobile | `3` (246, Bob en 3579) |
| `8` | `3579` | `Bob` | Bob meldt zich opnieuw aan via mobile | `3` (246, Bob en 3579) |

Zowel niet-geverifieerde als geverifieerde hits op nieuwe apparaten worden als afzonderlijke personen geteld (tijdelijk).
Niet-geverifieerde treffers op herkende apparaten worden vanaf dat punt live-gezet. Attributie werkt zodra de identificerende douanevariabele aan een apparaat bindt. In het bovenstaande voorbeeld worden alle treffers, behalve hits 1 en 3, in een live-stitched weergegeven (ze gebruiken allemaal de id `Bob` ). Attributie werkt bij hits 1 en 3 na het opnieuw afspelen van stitching.

>[!NOTE]
>
>Tijdgestempelde hits ouder dan 12 uur worden niet in de live flow vastgezet. Deze hits worden echter wel opgenomen in de optie voor opnieuw afspelen, zolang ze maar in het terugkijkvenster voor opnieuw afspelen vallen.

### Replay stitching

Replay komt of dagelijks of wekelijks voor, afhankelijk van hoe u CDA om vroeg te worden gevormd. Tijdens replay, probeert CDA historische gegevens binnen een bepaald terugkijkvenster opnieuw te verklaren:

* Dagelijks opnieuw afspelen gebruikt een terugkijkvenster van 1 dag
* Wekelijks opnieuw afspelen gebruikt een terugkijkvenster van 7 dagen.

Als een apparaat aanvankelijk gegevens verzendt terwijl niet voor authentiek verklaard en dan login, CDA die niet voor authentiek verklaarde klappen aan de correcte persoon bindt. In de volgende tabel worden dezelfde gegevens weergegeven als hierboven, maar worden verschillende getallen weergegeven op basis van het opnieuw afspelen van de gegevens.

*De zelfde gegevens na replay:*

| Tijdstempel | ECID | eVar1 of CustomerID | Toelichting bij treffer | Mensen (cumulatief) die op het veld gebaseerde stitching gebruiken |
| --- | --- | --- | --- | --- |
| `1` | `246` | - | Bob op zijn desktopcomputer, niet geverifieerd | `1` (Bob) |
| `2` | `246` | `Bob` | Bob meldt zich aan op zijn bureaublad | `1` (Bob) |
| `3` | `3579` | - | Bob op zijn mobiele apparaat, niet geverifieerd | `1` (Bob) |
| `4` | `3579` | `Bob` | Bob meldt zich aan op mobile | `1` (Bob) |
| `5` | `246` | - | Bob benadert uw site opnieuw op het bureaublad, zonder verificatie | `1` (Bob) |
| `6` | `246` | `Bob` | Bob meldt zich opnieuw aan via desktop | `1` (Bob) |
| `7` | `3579` | - | Bob benadert uw site opnieuw op mobile | `1` (Bob) |
| `8` | `3579` | `Bob` | Bob meldt zich opnieuw aan via mobile | `1` (Bob) |
