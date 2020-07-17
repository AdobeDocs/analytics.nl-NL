---
description: 'null'
title: Voorbeeld van labeling
uuid: a9a5b937-dbde-4f0f-a171-005ef4c79df9
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 100%

---


# Voorbeeld van labeling

## Voorbeelden van treffersdata

Stel dat u de volgende treffersdata hebt:

* De eerste rij bevat de labels voor elke variabele.
* De tweede rij is de naam van de variabele. Als er een id-label is, bevat deze de toegewezen naamruimte tussen haakjes.
* De treffersdata beginnen op de derde rij.

| Labels | I2<br>ID-PERSON<br>DEL-PERSON<br>ACC-PERSON | I2<br>ID-DEVICE<br>DEL-DEVICE<br>ACC-ALL | I2<br>DEL-PERSON<br>ACC-PERSON | I2<br>DEL-DEVICE<br>DEL-PERSON<br>ACC-ALL | I2<br>ID-DEVICE<br>DEL-DEVICE<br>ACC-ALL |
|---|---|---|---|---|---|
| **Naam variabele**<br>**(Naamruimte)** | **MyProp1**<br>**(gebruiker)** | **Bezoekers-id**<br>**(AAID)** | **MyEvar1** | **MyEvar2** | **MyEvar3**<br>**(xyz)** |
| Treffersdata | Moniek | 77 | A | M | X |
|  | Moniek | 88 | B | N | Y |
|  | Moniek | 99 | C | O | Z |
|  | John | 77 | D | P | W |
|  | John | 88 | E | N | U |
|  | John | 44 | F | Q | V |
|  | John | 55 | G | R | X |
|  | Alice | 66 | A | N | Z |

## Voorbeeld van toegangsaanvraag

Als ik een toegangsaanvraag verzend, bevat het overzichtsbestand de waarden die in de onderstaande tabel worden vermeld. Een aanvraag kan alleen een apparaatbestand, alleen een persoonsbestand, of één van beide retourneren. Twee overzichtsbestanden worden alleen geretourneerd als een persoons-id wordt gebruikt en expandIds waar is.

| API-waarden | API-waarden | Type geretourneerd bestand | Data in <br>Overzichtstoegangsbestand | Data in <br>Overzichtstoegangsbestand | Data in <br>Overzichtstoegangsbestand | Data in <br>Overzichtstoegangsbestand | Data in <br>Overzichtstoegangsbestand |
|--- |--- |--- |---|---|---|---|---|
| **Naamruimte/id** | **expandIDs** |  | **MyProp1** | **Bezoekers-id** | **MyEvar1** | **MyEvar2** | **MyEvar3** |
| AAID=77 | false | device | Variabele niet aanwezig | 77 | Variabele niet aanwezig | M, P | X, W |
| AAID=77 | true | device | Variabele niet aanwezig | 77 | Variabele niet aanwezig | M, P | X, W |
| user=Moniek | false | person | Moniek | 77, 88, 99 | A, B, C | M, N, O | X, Y, Z |
| user=Moniek | true | person | Moniek | 77, 88, 99 | A, B, C | M, N, O | X, Y, Z |
| user=Moniek | true | device | niet aanwezig | 77, 88 | niet aanwezig | N, P | U, W |
| user=Moniek AAID=66 | true | person | Moniek | 77, 88, 99 | A, B, C | M, N, O | X, Y, Z |
| user=Moniek AAID=66 | true | device | niet aanwezig | 66, 77, 88 | niet aanwezig | N, P | U, W, Z |
| xyz=X | false | device | niet aanwezig | 55, 77 | niet aanwezig | M, R | X |
| xyz=X | true | device | niet aanwezig | 55, 77 | niet aanwezig | M, P, R | B, X |

Bedenk dat de instelling voor expandIDs niet uitmaakt voor de uitvoer wanneer een cookie-id wordt gebruikt.

## Voorbeeld van verwijderingsaanvraag

Met een verwijderingsaanvraag waarbij de API-waarden in de eerste rij van de tabel staan, wordt de tabel met treffers zodanig bijgewerkt dat deze er ongeveer als volgt uitziet:

| Waarde AAID=77 expandIDs<br> is niet van belang | Waarde AAID=77 expandIDs<br> is niet van belang | Waarde AAID=77 expandIDs<br> is niet van belang | Waarde AAID=77 expandIDs<br> is niet van belang | Waarde AAID=77 expandIDs<br> is niet van belang |
|---|---|---|---|---|
| **MyProp1** | **AAID** | **MyEvar1** | **MyEvar2** | **MyEvar3** |
| Moniek | 42 | A | Privacy-7398 | Privacy-9152 |
| Moniek | 88 | B | N | Y |
| Moniek | 99 | C | O | Z |
| John | 42 | D | Privacy-1866 | Privacy-8216 |
| John | 88 | E | N | U |
| John | 44 | F | Q | V |
| John | 55 | G | R | X |
| Alice | 66 | A | N | W |

>[!NOTE]
>
>Alleen cellen op rijen met AAID=77 en een DEL-DEVICE-label worden beïnvloed.

| user=Moniek<br>expandIDs=false | user=Moniek<br>expandIDs=false | user=Moniek<br>expandIDs=false | user=Moniek<br>expandIDs=false | user=Moniek<br>expandIDs=false |
|--- |---|---|---|---|
| **MyProp1** | **AAID** | **MyEvar1** | **MyEvar2** | **MyEvar3** |
| Privacy-0523 | 77 | Privacy-1866 | Privacy-3681 | X |
| Privacy-0523 | 88 | Privacy-2178 | Privacy-1975 | Y |
| Privacy-0523 | 99 | Privacy-9045 | Privacy-2864 | Z |
| John | 77 | D | P | W |
| John | 88 | E | N | U |
| John | 44 | F | Q | V |
| John | 55 | G | R | X |
| Alice | 66 | A | N | W |

>[!NOTE]
>
>Alleen cellen op rijen met user=Moniek en een DEL-PERSON-label worden beïnvloed. Bovendien zou in de praktijk de variabele met A_ID waarschijnlijk een prop of eVar zijn, en de vervangende waarde zou een tekenreeks zijn die begint met “Privacy-”, gevolgd door een willekeurig getald (GUID), in plaats van de numerieke waarde te vervangen door een andere, willekeurige numerieke waarde.

| user=Moniek<br>expandIDs=true | user=Moniek<br>expandIDs=true | user=Moniek<br>expandIDs=true | user=Moniek<br>expandIDs=true | user=Moniek<br>expandIDs=true |
|--- |---|---|---|---|
| **MyProp1** | **AAID** | **MyEvar1** | **MyEvar2** | **MyEvar3** |
| Privacy-5782 | 09 | Privacy-0859 | Privacy-8183 | Privacy-9152 |
| Privacy-5782 | 16 | Privacy-6104 | Privacy-2911 | Privacy-6821 |
| Privacy-5782 | 83 | Privacy-2714 | Privacy-0219 | Privacy-4395 |
| John | 09 | D | Privacy-8454 | Privacy-8216 |
| John | 16 | E | Privacy-2911 | Privacy-2930 |
| John | 44 | F | Q | V |
| John | 55 | G | R | X |
| Alice | 66 | A | N | W |

Let op het volgende:

* De cellen in rijen die `user=Mary` en een `DEL-DEVICE`- of `DEL-PERSON`-label bevatten, worden beïnvloed, evenals cellen met een `DEL-DEVICE`-label op rijen die een bezoekers-id bevatten die voorkwam op een rij met `user=Mary`.
* `MyEvar2` in de vierde en vijfde rij wordt bijgewerkt omdat deze rijen dezelfde waarden voor bezoekers-id bevatten als die op de eerste en tweede rij, zodat id-uitbreiding deze opneemt bij verwijderingen op apparaatniveau.
* De waarden van `MyEvar2` in rij 2 en 5 komen zowel vóór als na de verwijdering overeen, maar komen na de verwijdering niet meer overeen met de waarde N die in de laatste rij voorkomt, omdat deze rij niet is bijgewerkt als deel van de verwijderingsaanvraag.
* `MyEvar3` gedraagt zich heel anders dan zonder de id-uitbreiding, omdat zonder id-uitbreiding geen `ID-DEVICES` overeenkwam. Nu komt `AAID` overeen met de eerste vijf rijen.
