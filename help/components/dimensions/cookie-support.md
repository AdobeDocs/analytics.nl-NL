---
title: Cookie-ondersteuning
description: Hiermee bepaalt u of de browser cookies ondersteunt.
exl-id: 07d4fe12-0d60-469d-98b1-e93ce5a0fd21
source-git-commit: e6f3beadfba340cea07f5fd2694105ad31de9751
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---

# Cookie-ondersteuning

De dimensie &#39;Cookie support&#39; rapporteert als de browser cookies voor een bepaalde hit ondersteunt. Het is handig om de verhouding te bepalen tussen bezoekers die browsers gebruiken die cookies ondersteunen en bezoekers die deze opzettelijk uitschakelen.

## Deze dimensie vullen met gegevens

Deze afmeting verzamelt gegevens van [`k` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken. AppMeasurement probeert om een koekje te plaatsen genoemd `s_cc`, dan ontdekt als het koekje bestaat. Het resultaat is de parameterwaarde `Y` voor de querytekenreeks (als de browser cookies ondersteunt en ingeschakeld heeft) of `N` (als de browser cookies heeft uitgeschakeld). Als u AppMeasurement gebruikt (zoals door markeringen in Adobe Experience Platform), werkt deze afmeting uit de doos. Als u een methode van de gegevensinzameling buiten AppMeasurement (zoals door API) gebruikt, zorg ervoor dat u `k` vraagkoordparameter op elke slag met de waarde `Y` of `N` omvat.

## Dimension-items

Dimension-items zijn onder andere `Enabled`, `Disabled` en `Unknown`.

* **`Enabled`**: De browser ondersteunt cookies en heeft deze ingeschakeld.
* **`Disabled`**: De browser ondersteunt geen cookies of de bezoeker heeft deze uitgeschakeld.
* **`Unknown`**: AppMeasurement kon koekjessteun niet bepalen. De query-tekenreeks `k` is niet aanwezig in de afbeeldingsaanvraag.
