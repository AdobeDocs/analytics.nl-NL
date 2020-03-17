---
description: 'null'
title: Voorbeeld van labeling
uuid: a9a5b937-dbde-4f0f-a171-005ef4c79df9
translation-type: tm+mt
source-git-commit: ''

---


# Voorbeeld van labeling

## Bemonster met gegevens

Stel dat u de volgende raakgegevens hebt:

* De eerste rij bevat de labels voor elke variabele.
* De tweede rij is de naam van de variabele. Als het een etiket van identiteitskaart heeft, bevat het toegewezen namespace tussen haakjes.
* De gegevens van de aanraking beginnen in de derde rij.

| Labels | I2<br>ID-<br>PERSONDEL-<br>PERSONACC-PERSON | I2<br>ID-<br>DEVICEDEL-<br>DEVICEACC-ALL | I2<br>DEL-<br>PERSONACC-PERSON | I2<br>DEL-<br>DEVICEDEL-<br>PERSONACC-ALL | I2<br>ID-<br>DEVICEDEL-<br>DEVICEACC-ALL |
|---|---|---|---|---|---|
| **Naam **<br>**variabele (naamruimte)** | **MyProp1 **<br>**(gebruiker)** | **Bezoeker-id **<br>**(HULP)** | **MyEvar1** | **MyEvar2** | **MyEvar3 **<br>**(xyz)** |
| Gegevens aanpassen | Mary | 77 | A | M | X |
|  | Mary | 88 | B | N | Y |
|  | Mary | 99 | C | O | Z |
|  | John | 77 | D | P | W |
|  | John | 88 | E | N | U |
|  | John | 44 | F | Q | V |
|  | John | 55 | G | R | X |
|  | Alice | 66 | A | N | Z |

## Voorbeeld van toegangsaanvraag

Als ik een toegangsverzoek indient, bevat het samenvattingsbestand de waarden die in de onderstaande tabel worden vermeld. Een verzoek kan slechts een apparatendossier, slechts een persoondossier of één van elk terugkeren. Twee samenvattingsbestanden worden alleen geretourneerd als een persoon-id wordt gebruikt en expandIds waar is.

| API-waarden | API-waarden | Type geretourneerd bestand | Gegevens in <br>samenvattingstoegangsbestand | Gegevens in <br>samenvattingstoegangsbestand | Gegevens in <br>samenvattingstoegangsbestand | Gegevens in <br>samenvattingstoegangsbestand | Gegevens in <br>samenvattingstoegangsbestand |
|--- |--- |--- |---|---|---|---|---|
| **Naamruimte/id** | **expandIDs** |  | **MyProp1** | **Bezoeker-id** | **MyEvar1** | **MyEvar2** | **MyEvar3** |
| AID=77 | false | apparaat | Variabele niet aanwezig | 77 | Variabele niet aanwezig | M, P | X, W |
| AID=77 | true | apparaat | Variabele niet aanwezig | 77 | Variabele niet aanwezig | M, P | X, W |
| user=Mary | false | persoon | Mary | 77, 88, 99 | A, B, C | M, N, O | X, Y, Z |
| user=Mary | true | persoon | Mary | 77, 88, 99 | A, B, C | M, N, O | X, Y, Z |
| user=Mary | true | apparaat | niet aanwezig | 77, 88 | niet aanwezig | N, P | U, W |
| user=Mary AID=66 | true | persoon | Mary | 77, 88, 99 | A, B, C | M, N, O | X, Y, Z |
| user=Mary AID=66 | true | apparaat | niet aanwezig | 66, 77, 88 | niet aanwezig | N, P | U, W, Z |
| xyz=X | false | apparaat | niet aanwezig | 55, 77 | niet aanwezig | M, R | X |
| xyz=X | true | apparaat | niet aanwezig | 55, 77 | niet aanwezig | M, P, R | B, X |

De instelling voor expandID&#39;s heeft geen invloed op de uitvoer wanneer een cookie-id wordt gebruikt.

## Voorbeeld verzoek verwijderen

Met een verwijderaanvraag waarbij de API-waarden in de eerste rij van de tabel worden gebruikt, wordt de aanraaktabel zo bijgewerkt dat deze er ongeveer als volgt uitziet:

| De<br>waarde van AID=77 expandIDs is niet van belang | De<br>waarde van AID=77 expandIDs is niet van belang | De<br>waarde van AID=77 expandIDs is niet van belang | De<br>waarde van AID=77 expandIDs is niet van belang | De<br>waarde van AID=77 expandIDs is niet van belang |
|---|---|---|---|---|
| **MyProp1** | **STEUN** | **MyEvar1** | **MyEvar2** | **MyEvar3** |
| Mary | 42 | A | Privacy-7398 | Privacy-9152 |
| Mary | 88 | B | N | Y |
| Mary | 99 | C | O | Z |
| John | 42 | D | Privacy-1866 | Privacy-8216 |
| John | 88 | E | N | U |
| John | 44 | F | Q | V |
| John | 55 | G | R | X |
| Alice | 66 | A | N | W |

> [!NOTE] Alleen cellen op rijen met AID = 77 en een DEL-DEVICE-label worden beïnvloed.

| user=<br>MaryexpandIDs=false | user=<br>MaryexpandIDs=false | user=<br>MaryexpandIDs=false | user=<br>MaryexpandIDs=false | user=<br>MaryexpandIDs=false |
|--- |---|---|---|---|
| **MyProp1** | **STEUN** | **MyEvar1** | **MyEvar2** | **MyEvar3** |
| Privacy-0523 | 77 | Privacy-1866 | Privacy-3681 | X |
| Privacy-0523 | 88 | Privacy-2178 | Privacy-1975 | Y |
| Privacy-0523 | 99 | Privacy-9045 | Privacy-2864 | Z |
| John | 77 | D | P | W |
| John | 88 | E | N | U |
| John | 44 | F | Q | V |
| John | 55 | G | R | X |
| Alice | 66 | A | N | W |

> [!NOTE] Alleen cellen op rijen met user=Mary en een DEL-PERSON-label worden beïnvloed. Ook, in de praktijk zou de variabele die A_ID bevat waarschijnlijk een steun of eVar zijn en zijn vervangingswaarde zou een koord zijn dat met &quot;Privacy-&quot;begint, door een willekeurig aantal (GUID) wordt gevolgd, eerder dan het vervangen van de numerieke waarde met een verschillende, willekeurige numerieke waarde die.

| user=<br>MaryexpandIDs=true | user=<br>MaryexpandIDs=true | user=<br>MaryexpandIDs=true | user=<br>MaryexpandIDs=true | user=<br>MaryexpandIDs=true |
|--- |---|---|---|---|
| **MyProp1** | **STEUN** | **MyEvar1** | **MyEvar2** | **MyEvar3** |
| Privacy-5782 | 09 | Privacy-0859 | Privacy-8183 | Privacy-9152 |
| Privacy-5782 | 16 | Privacy-6104 | Privacy-2911 | Privacy-6821 |
| Privacy-5782 | 83 | Privacy-2714 | Privacy-0219 | Privacy-4395 |
| John | 09 | D | Privacy-8454 | Privacy-8216 |
| John | 16 | E | Privacy-2911 | Privacy-2930 |
| John | 44 | F | Q | V |
| John | 55 | G | R | X |
| Alice | 66 | A | N | W |

Let op het volgende:

* De cellen op rijen die `user=Mary` en een `DEL-DEVICE` of `DEL-PERSON` etiket bevatten worden beïnvloed, evenals cellen met een `DEL-DEVICE` etiket op rijen die om het even welke identiteitskaart van de Bezoeker bevatten die op een rij die `user=Mary`voorkwam.
* `MyEvar2` in de vierde en vijfde rij wordt bijgewerkt omdat deze rijen de zelfde waarden van identiteitskaart van de Bezoeker zoals die op de eerste en tweede rijen bevatten, zodat omvat de uitbreiding van identiteitskaart hen voor apparaat-vlakke schrapping.
* De waarden van `MyEvar2` in rijen 2 en 5 komen zowel vóór als na schrapping overeen, maar na schrapping niet meer de waarde N aanpast die in de laatste rij voorkomt, omdat die rij niet als deel van het schrappingsverzoek werd bijgewerkt.
* `MyEvar3` gedraagt zich heel anders dan zonder de uitbreiding van identiteitskaart, omdat zonder de uitbreiding van identiteitskaart, geen `ID-DEVICES` gelijke. Komt nu `AAID` overeen met de eerste vijf rijen.
