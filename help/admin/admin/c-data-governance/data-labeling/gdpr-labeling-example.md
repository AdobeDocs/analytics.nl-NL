---
description: Toont voorbeelden op hoe te om gegevens voor raakgegevens, toegangsverzoeken, schrappingsverzoeken te etiketteren
title: Voorbeelden van labels
feature: Data Governance
role: Admin
exl-id: 9bea8636-c79c-4998-8952-7c66d31226e3
source-git-commit: 48f1974a0c379a4e619d9a04ae80e43cce9527c1
workflow-type: tm+mt
source-wordcount: '932'
ht-degree: 46%

---

# Voorbeelden van labels

## Bemonsteringstreffers {#hit}

Stel dat u de volgende treffersdata hebt:

* De eerste rij bevat de labels voor elke variabele.
* De tweede rij is de naam van de variabele. Als er een id-label is, bevat deze de toegewezen naamruimte tussen haakjes.
* De treffersdata beginnen op de derde rij.

| Labels | I2 <br> ID-PERSON <br> DEL-PERSON <br> ACC-PERSON | I2 <br> ID-APPARAAT <br> DEL-APPARAAT <br> ACC-ALL | I2 <br> DEL-PERSON <br> ACC-PERSON | I2 <br> DEL-APPARAAT <br> DEL-PERSON <br> ACC-ALL | I2 <br> ID-APPARAAT <br> DEL-APPARAAT <br> ACC-ALL |
|---|---|---|---|---|---|
| **Naam variabele** <br> **(Namespace)** | **MyProp1** <br> **(gebruiker)** | **Bezoeker-id** <br> **(STEUN)** | **MyEvar1** | **MyEvar2** | **MyEvar3** <br> **(xyz)** |
| Treffersdata | Moniek | 77 | A | M | X |
| | Moniek | 88 | B | N | Y |
| | Moniek | 99 | C | O | Z |
| | John | 77 | D | P | W |
| | John | 88 | E | N | U |
| | John | 44 | F | Q | V |
| | John | 55 | G | R | X |
| | Alice | 66 | A | N | Z |

## Voorbeeld van toegangsaanvraag {#access}

Als u een toegangsverzoek indient, ontvangt u twee bestanden die u naar de betrokkene kunt terugsturen. Eén bestand is een CSV-bestand dat één rij bevat voor elke treffer die voor de betrokkene is ontvangen en een kolom voor elke variabele met het juiste toegangslabel. Het andere bestand is een summiere HTML-bestand waarin elke variabele wordt vermeld, gevolgd door alle unieke waarden die voor die variabele voor de betrokkene worden gezien en het aantal keren dat elke unieke waarde werd gezien.

Het samenvattingsbestand bevat bijvoorbeeld de waarden die in de onderstaande tabel worden aangegeven. Een aanvraag kan alleen een apparaatbestand, alleen een persoonsbestand, of één van beide retourneren. Twee samenvattingsbestanden worden alleen geretourneerd als een persoon-id wordt gebruikt en `expandIds` is waar.

<table>
  <tr>
    <th colspan="2" style="text-align:center">API-waarden</th>
    <th rowspan="2">Samenvatting<br/>bestandstype<br/>geretourneerd</th>
    <th colspan="5" style="text-align:center">Gegevens in toegangsbestand overzicht</th>
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
    <td rowspan="2">user=Mary<br>AID=66</td>
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
    <th colspan="5" style="text-align:center">AID=77 <br>(Waarde van expandIDs is niet van belang)</th>
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
>Alleen kolommen op rijen die `AAID=77` en `DEL-DEVICE` het label wordt beïnvloed.

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
>Alleen celcolumnslets op rijen die `user=Mary` en `DEL-PERSON` het label wordt beïnvloed. In de praktijk bevat de variabele `A_ID` zou waarschijnlijk een prop of een eVar zijn. De vervangingswaarde zou een tekenreeks zijn die begint met `Privacy-`gevolgd door een willekeurig getal (GUID) in plaats van de numerieke waarde te vervangen door een andere willekeurige numerieke waarde.

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

* Cellen op rijen die `user=Mary` en `DEL-PERSON` het label wordt beïnvloed.
* Vanwege ID-uitbreiding bevatten cellen op rijen die `AAID=77`, `AAID=88` of `AAID=99` (Dit zijn de waarden van de STEUN op rijen die `user=Mary`) en `DEL-DEVICE` het label wordt beïnvloed. Dit omvat cellen met een `DEL-DEVICE` label op rijen waar `user=Mary`. Dit veroorzaakt cellen in rijen 4 en 5 (evenals rijen 1-3) met `DEL-DEVICE` labels (AID, MyEvar2 en MyEvar3) die u wilt verduisteren.
* De instelling expandIDs wordt niet uitgebreid naar de aanroep om waarden op te nemen die zich in MyEvar3 (`X`, `Y` en `Z`), dat een ID-DEVICE-label heeft, wanneer `user=Mary`. ExpandIDs breidt zich slechts uit om Bezoeker IDs (HULPs in dit voorbeeld, maar ook ECID) op rijen te omvatten waar `user=Mary`. De laatste twee rijen die MyEvar3-waarden bevatten van `X` en `Z` geen invloed hebben.
* `MyEvar2` in de vierde en vijfde rij worden bijgewerkt omdat deze rijen dezelfde waarden voor de bezoeker-id bevatten (`77` en `88`) als op de eerste en de tweede rij. Dientengevolge, omvat de uitbreiding van identiteitskaart hen voor apparaat-vlakke schrappingen.
* De waarden van `MyEvar2` in de rijen twee en vijf komen zowel voor als na de schrapping overeen. Na het verwijderen komen ze echter niet meer overeen met de waarde `N` die in de laatste rij voorkomt, omdat die rij niet als deel van het schrappingsverzoek werd bijgewerkt.
* `MyEvar3` gedraagt zich heel anders dan zonder de id-uitbreiding, omdat zonder id-uitbreiding geen `ID-DEVICES` overeenkwam. Nu, `AAID` komt overeen met de eerste vijf rijen.
