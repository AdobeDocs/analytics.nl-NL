---
description: Toont voorbeelden op hoe te om gegevens voor raakgegevens, toegangsverzoeken, schrappingsverzoeken te etiketteren
title: Voorbeeld van labeling
uuid: a9a5b937-dbde-4f0f-a171-005ef4c79df9
exl-id: 9bea8636-c79c-4998-8952-7c66d31226e3
source-git-commit: 3ff221b8715ecde6923310b6818904c697a2b003
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 84%

---

# Voorbeeld van labeling

## Voorbeelden van treffersdata

Stel dat u de volgende treffersdata hebt:

* De eerste rij bevat de labels voor elke variabele.
* De tweede rij is de naam van de variabele. Als er een id-label is, bevat deze de toegewezen naamruimte tussen haakjes.
* De treffersdata beginnen op de derde rij.

| Labels | I2<br>ID-PERSON<br>DEL-PERSON<br>ACC-PERSON | I2<br>ID-DEVICE<br>DEL-DEVICE<br>ACC-ALL | I2<br>DEL-PERSON<br>ACC-PERSON | I2<br>DEL-DEVICE<br>DEL-PERSON<br>ACC-ALL | I2<br>ID-DEVICE<br>DEL-DEVICE<br>ACC-ALL |
|---|---|---|---|---|---|
| **Naam variabele** <br> **(Namespace)** | **MyProp1** <br> **(gebruiker)** | **Bezoekers-id** <br> **(AAID)** | **MyEvar1** | **MyEvar2** | **MyEvar3** <br> **(xyz)** |
| Treffersdata | Moniek | 77 | A | M | X |
|  | Moniek | 88 | B | N | Y |
|  | Moniek | 99 | C | O | Z |
|  | John | 77 | D | P | W |
|  | John | 88 | E | N | U |
|  | John | 44 | F | Q | V |
|  | John | 55 | G | R | X |
|  | Alice | 66 | A | N | Z |

## Voorbeeld van toegangsaanvraag

Als ik een toegangsverzoek indient, bevat het samenvattingsbestand de waarden die in de onderstaande tabel worden vermeld. Een aanvraag kan alleen een apparaatbestand, alleen een persoonsbestand, of één van beide retourneren. Twee overzichtsbestanden worden alleen geretourneerd als een persoons-id wordt gebruikt en expandIds waar is.

<table>
  <tr>
    <th colspan="2" style="text-align:center">API-waarden</th>
    <th rowspan="2">Geretourneerd<br>Bestandstype</th>
    <th colspan="5" style="text-align:center">Data in Overzichtstoegangsbestand</th>
  </tr>
  <tr>
    <th>Naamruimte/id</th>
    <th>expandIDs</th>
    <th>MyProp1</th>
    <th>Bezoekers-id</th>
    <th>MyEvar1</th>
    <th>MyEvar2</th>
    <th>MyEvar3</th>
  </tr>
  <tr>
    <td>AAID=77</td>
    <td>false</td>
    <td>device</td>
    <td>niet aanwezig</td>
    <td>77</td>
    <td>niet aanwezig</td>
    <td>M, P</td>
    <td>X, W</td>
  </tr>
  <tr>
    <td>AID=77</td>
    <td>true</td>
    <td>apparaat</td>
    <td>niet aanwezig</td>
    <td>77</td>
    <td>niet aanwezig</td>
    <td>M, P</td>
    <td>X, W</td>
  </tr>
  <tr>
    <td>user=Moniek</td>
    <td>false</td>
    <td>person</td>
    <td>Moniek</td>
    <td>77, 88, 99</td>
    <td>A, B, C</td>
    <td>M, N, O</td>
    <td>X, Y, Z</td>
  </tr>
  <tr>
    <td rowspan="2">user=Moniek</td>
    <td rowspan="2">true</td>
    <td>persoon</td>
    <td>Moniek</td>
    <td>77 88 99</td>
    <td>A, B, C</td>
    <td>M, N, O</td>
    <td>X, Y, Z</td>
  </tr>
  <tr>
    <td>apparaat</td>
    <td>niet aanwezig</td>
    <td>77, 88</td>
    <td>A, B, C</td>
    <td>N, P</td>
    <td>U, W</td>
  </tr>
  <tr>
    <td rowspan="2">user=Mary<br>AID=66</td>
    <td rowspan="2">true</td>
    <td>persoon</td>
    <td>Moniek</td>
    <td>77 88 99</td>
    <td>A, B, C</td>
    <td>M, N, O</td>
    <td>X, Y, Z</td>
  </tr>
  <tr>
    <td>apparaat</td>
    <td>niet aanwezig</td>
    <td>66, 77, 88</td>
    <td>A, B, C</td>
    <td>N, P</td>
    <td>U, W, Z</td>
  </tr>
  <tr>
    <td>xyz=X</td>
    <td>false</td>
    <td>apparaat</td>
    <td>niet aanwezig</td>
    <td>55, 77</td>
    <td>niet aanwezig</td>
    <td>M, R</td>
    <td>X</td>
  </tr>
  <tr>
    <td>xyz=X</td>
    <td>true</td>
    <td>apparaat</td>
    <td>niet aanwezig</td>
    <td>55 77</td>
    <td>niet aanwezig</td>
    <td>M, P, R</td>
    <td>B, X</td>
  </tr>
</table>

Bedenk dat de instelling voor expandIDs niet uitmaakt voor de uitvoer wanneer een cookie-id wordt gebruikt.

## Voorbeeld verzoeken verwijderen

Met een verwijderingsaanvraag waarbij de API-waarden in de eerste rij van de tabel staan, wordt de tabel met treffers zodanig bijgewerkt dat deze er ongeveer als volgt uitziet:

<table>
  <tr>
    <th colspan="5" style="text-align:center">AID=77 <br>(waarde expandIDs is niet van belang)</th>
  </tr>
  <tr>
    <th>MyProp1</th>
    <th>AAID</th>
    <th>MyEvar1</th>
    <th>MyEvar2</th>
    <th>MyEvar3</th>
  </tr>
  <tr>
    <td>Moniek</td>
    <td>42</td>
    <td>A</td>
    <td>Privacy-7398</td>
    <td>Privacy-9152</td>
  </tr>
  <tr>
    <td>Moniek</td>
    <td>88</td>
    <td>B</td>
    <td>N</td>
    <td>Y</td>
  </tr>
  <tr>
    <td>Moniek</td>
    <td>99</td>
    <td>C</td>
    <td>O</td>
    <td>Z</td>
  </tr>
  <tr>
    <td>John</td>
    <td>42</td>
    <td>D</td>
    <td>Privacy-1866</td>
    <td>Privacy-8216</td>
  </tr>
  <tr>
    <td>John</td>
    <td>88</td>
    <td>E</td>
    <td>N</td>
    <td>U</td>
  </tr>
  <tr>
    <td>John</td>
    <td>44</td>
    <td>F</td>
    <td>Q</td>
    <td>V</td>
  </tr>
  <tr>
    <td>John</td>
    <td>55</td>
    <td>G</td>
    <td>R</td>
    <td>X</td>
  </tr>
  <tr>
    <td>Alice</td>
    <td>66</td>
    <td>A</td>
    <td>N</td>
    <td>Z</td>
  </tr>
</table>

>[!NOTE]
>
>Alleen cellen op rijen met AAID=77 en een DEL-DEVICE-label worden beïnvloed.

<table>
  <tr>
    <th colspan="5" style="text-align:center">user=Moniek<br>expandIDs=false</th>
  </tr>
  <tr>
    <th>MyProp1</th>
    <th>STEUN</th>
    <th>MyEvar1</th>
    <th>MyEvar2</th>
    <th>MyEvar3</th>
  </tr>
  <tr>
    <td>Privacy-0523</td>
    <td>77</td>
    <td>Privacy-1866</td>
    <td>Privacy-3681</td>
    <td>X</td>
  </tr>
  <tr>
    <td>Privacy-0523</td>
    <td>88</td>
    <td>Privacy-2178</td>
    <td>Privacy-1975</td>
    <td>Y</td>
  </tr>
  <tr>
    <td>Privacy-0523</td>
    <td>99</td>
    <td>Privacy-9045</td>
    <td>Privacy-2864</td>
    <td>Z</td>
  </tr>
  <tr>
    <td>John</td>
    <td>77</td>
    <td>D</td>
    <td>P</td>
    <td>W</td>
  </tr>
  <tr>
    <td>John</td>
    <td>88</td>
    <td>E</td>
    <td>N</td>
    <td>U</td>
  </tr>
  <tr>
    <td>John</td>
    <td>44</td>
    <td>F</td>
    <td>Q</td>
    <td>V</td>
  </tr>
  <tr>
    <td>John</td>
    <td>55</td>
    <td>G</td>
    <td>R</td>
    <td>X</td>
  </tr>
  <tr>
    <td>Alice</td>
    <td>66</td>
    <td>A</td>
    <td>N</td>
    <td>Z</td>
  </tr>
</table>

>[!NOTE]
>
>Alleen cellen op rijen met user=Moniek en een DEL-PERSON-label worden beïnvloed. Bovendien zou in de praktijk de variabele met A_ID waarschijnlijk een prop of eVar zijn, en de vervangende waarde zou een tekenreeks zijn die begint met “Privacy-”, gevolgd door een willekeurig getald (GUID), in plaats van de numerieke waarde te vervangen door een andere, willekeurige numerieke waarde.

<table>
  <tr>
    <th colspan="5" style="text-align:center">user=Moniek<br>expandIDs=true</th>
  </tr>
  <tr>
    <th>MyProp1</th>
    <th>STEUN</th>
    <th>MyEvar1</th>
    <th>MyEvar2</th>
    <th>MyEvar3</th>
  </tr>
  <tr>
    <td>Privacy-5782</td>
    <td>09</td>
    <td>Privacy-0859</td>
    <td>Privacy-8183</td>
    <td>Privacy-9152</td>
  </tr>
  <tr>
    <td>Privacy-5782</td>
    <td>16</td>
    <td>Privacy-6104</td>
    <td>Privacy-2911</td>
    <td>Privacy-6821</td>
  </tr>
  <tr>
    <td>Privacy-5782</td>
    <td>83</td>
    <td>Privacy-2714</td>
    <td>Privacy-0219</td>
    <td>Privacy-4395</td>
  </tr>
  <tr>
    <td>John</td>
    <td>09</td>
    <td>D</td>
    <td>Privacy-8454</td>
    <td>Privacy-8216</td>
  </tr>
  <tr>
    <td>John</td>
    <td>16</td>
    <td>E</td>
    <td>Privacy-2911</td>
    <td>Privacy-2930</td>
  </tr>
  <tr>
    <td>John</td>
    <td>44</td>
    <td>F</td>
    <td>Q</td>
    <td>V</td>
  </tr>
  <tr>
    <td>John</td>
    <td>55</td>
    <td>G</td>
    <td>R</td>
    <td>X</td>
  </tr>
  <tr>
    <td>Alice</td>
    <td>66</td>
    <td>A</td>
    <td>N</td>
    <td>Z</td>
  </tr>
</table>

Let op het volgende:

* Cellen op rijen die `user=Mary` en een `DEL-DEVICE` of `DEL-PERSON` etiket bevatten worden beïnvloed, evenals cellen met een `DEL-DEVICE` etiket op rijen die om het even welke identiteitskaart van de Bezoeker bevatten (AID) die op een rij die `user=Mary` bevatten voorkwamen.
* ExpexpandIDs het plaatsen breidt zich niet aan de vraag uit om waarden in MyEvar3 te omvatten, die een identiteitskaart-APPARAAT etiket heeft, wanneer `user=Mary`. ExpandIDs breidt zich slechts uit om bezoeker IDs (HULPs in dit voorbeeld, maar ook ECID) op rijen te omvatten waar `user=Mary`.
* `MyEvar2` in de vierde en vijfde rij wordt bijgewerkt omdat deze rijen dezelfde waarden voor bezoekers-id bevatten als die op de eerste en tweede rij, zodat id-uitbreiding deze opneemt bij verwijderingen op apparaatniveau.
* De waarden van `MyEvar2` in rij 2 en 5 komen zowel vóór als na de verwijdering overeen, maar komen na de verwijdering niet meer overeen met de waarde N die in de laatste rij voorkomt, omdat deze rij niet is bijgewerkt als deel van de verwijderingsaanvraag.
* `MyEvar3` gedraagt zich heel anders dan zonder de id-uitbreiding, omdat zonder id-uitbreiding geen `ID-DEVICES` overeenkwam. Nu komt `AAID` overeen met de eerste vijf rijen.
