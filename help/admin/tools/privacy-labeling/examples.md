---
description: Toont voorbeelden op hoe te om gegevens voor raakgegevens, toegangsverzoeken, schrappingsverzoeken te etiketteren
title: Voorbeelden van labels
feature: Data Governance
role: Admin
exl-id: 9bea8636-c79c-4998-8952-7c66d31226e3
source-git-commit: 0b8b9d0067c183bfeb13816f942b3726ac66d08c
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 57%

---

# Voorbeelden van labels

## Bemonsteringstreffers {#hit}

Stel dat u de volgende treffersdata hebt:

* De eerste rij bevat de labels voor elke variabele.
* De tweede rij is de naam van de variabele. Als er een id-label is, bevat deze de toegewezen naamruimte tussen haakjes.
* De treffersdata beginnen op de derde rij.

| Labels | I2 <br> ID-PERSON <br> DEL-PERSON <br> ACC-PERSON | I2 <br> ID-DEVICE <br> DEL-DEVICE <br> ACC-ALL | I2 <br> DEL-PERSON <br> ACC-PERSON | I2 <br> DEL-DEVICE <br> DEL-PERSON <br> ACC-ALL | I2 <br> ID-DEVICE <br> DEL-DEVICE <br> ACC-ALL |
|---|---|---|---|---|---|
| **Veranderlijke Naam** <br> **(Namespace)** | **MyProp1** <br> **(user)** | **identiteitskaart van de Bezoeker** <br> **(AID)** | **MyEvar1** | **MyEvar2** | **MyEvar3** <br> **(xyz)** |
| Treffersdata | Moniek | 77 | A | M | X |
| | Moniek | 88 | B | N | Y |
| | Moniek | 99 | C | O | Z |
| | John | 77 | D | P | W |
| | John | 88 | E | N | U |
| | John | 44 | F | Q | V |
| | John | 55 | G | R | X |
| | Alice | 66 | A | N | Z |

## Voorbeeld van toegangsaanvraag {#access}

Als u een toegangsverzoek indient, ontvangt u twee bestanden die u naar de betrokkene kunt terugsturen. Eén bestand is een CSV-bestand dat één rij bevat voor elke treffer die voor de betrokkene is ontvangen en een kolom voor elke variabele met het juiste toegangslabel. Het andere bestand is een samenvattend HTML-bestand met elke variabele, gevolgd door alle unieke waarden die voor die variabele voor de betrokkene worden gezien en het aantal keren dat elke unieke waarde werd gezien.

Het samenvattingsbestand bevat bijvoorbeeld de waarden die in de onderstaande tabel worden aangegeven. Een aanvraag kan alleen een apparaatbestand, alleen een persoonsbestand, of één van beide retourneren. Twee samenvattingsbestanden worden alleen geretourneerd als een persoon-id wordt gebruikt en `expandIds` true is.

<table>
  <tr>
    <th colspan="2" style="text-align:center">API-waarden</th>
    <th>Samenvatting <br/> teruggekeerd dossiertype <br/></th>
    <th colspan="5" style="text-align:center">Gegevens in toegangsbestand overzicht</th>
  </tr>
  <tr>
    <th>Naamruimte/id</th>
    <th>expandIDs</th>
    <th></th>
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
    <td>AAID=77</td>
    <td>true</td>
    <td>device</td>
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
    <td>person</td>
    <td>Moniek</td>
    <td>77, 88, 99</td>
    <td>A, B, C</td>
    <td>M, N, O</td>
    <td>X, Y, Z</td>
  </tr>
  <tr>
    <td>device</td>
    <td>niet aanwezig</td>
    <td>77, 88</td>
    <td>A, B, C</td>
    <td>N, P</td>
    <td>U, W</td>
  </tr>
  <tr>
    <td rowspan="2">user=Mary <br> AID=66</td>
    <td rowspan="2">true</td>
    <td>person</td>
    <td>Moniek</td>
    <td>77, 88, 99</td>
    <td>A, B, C</td>
    <td>M, N, O</td>
    <td>X, Y, Z</td>
  </tr>
  <tr>
    <td>device</td>
    <td>niet aanwezig</td>
    <td>66, 77, 88</td>
    <td>A, B, C</td>
    <td>N, P</td>
    <td>U, W, Z</td>
  </tr>
  <tr>
    <td>xyz=X</td>
    <td>false</td>
    <td>device</td>
    <td>niet aanwezig</td>
    <td>55, 77</td>
    <td>niet aanwezig</td>
    <td>M, R</td>
    <td>X</td>
  </tr>
  <tr>
    <td>xyz=X</td>
    <td>true</td>
    <td>device</td>
    <td>niet aanwezig</td>
    <td>55, 77</td>
    <td>niet aanwezig</td>
    <td>M, P, R</td>
    <td>B, X</td>
  </tr>
</table>

De instelling voor `expandIDs` heeft geen invloed op de uitvoer wanneer een cookie-id wordt gebruikt.

## Voorbeeld verzoeken verwijderen {#delete}

Met een verwijderingsaanvraag waarbij de API-waarden in de eerste rij van de tabel staan, wordt de tabel met treffers zodanig bijgewerkt dat deze er ongeveer als volgt uitziet:

<table>
  <tr>
    <th colspan="5" style="text-align:center">AID=77 <br> (waarde voor expandIDs is niet van belang)</th>
  </tr>
  <tr>
    <th>MyProp1</th>
    <th>STEUN</th>
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
>Alleen kolommen op rijen met `AAID=77` en een label `DEL-DEVICE` worden beïnvloed.

<table>
  <tr>
    <th colspan="5" style="text-align:center">user=Mary <br> expandIDs=false</th>
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
>Alleen celkolommen op rijen met `user=Mary` en een label `DEL-PERSON` worden beïnvloed. In de praktijk zou de variabele die `A_ID` bevat waarschijnlijk ook een proxy of een eVar zijn. Zijn vervangingswaarde zou een koord zijn dat met `Privacy-` begint, door een willekeurig aantal (GUID) wordt gevolgd, eerder dan het vervangen van de numerieke waarde met een verschillende, willekeurige numerieke waarde die.

<table>
  <tr>
    <th colspan="5" style="text-align:center">user=Mary <br> expandIDs=true</th>
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

* Cellen op rijen met `user=Mary` en een label `DEL-PERSON` worden beïnvloed.

