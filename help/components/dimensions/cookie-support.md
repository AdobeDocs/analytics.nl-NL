---
title: Cookie-ondersteuning
description: Hiermee bepaalt u of de browser cookies ondersteunt.
translation-type: tm+mt
source-git-commit: a8dc233e962a49674a30ff3c9f0b5d0d45b09f24
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---


# Cookie-ondersteuning

De dimensie &#39;Cookie support&#39; rapporteert als de browser cookies voor een bepaalde hit ondersteunt. Het is handig om de verhouding te bepalen tussen bezoekers die browsers gebruiken die cookies ondersteunen en bezoekers die deze opzettelijk uitschakelen.

## Deze dimensie vullen met gegevens

Deze dimensie verzamelt gegevens van het [`k` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken. AppMeasurement probeert een cookie met de naam in te stellen `s_cc`en detecteert vervolgens of het cookie bestaat. Het resultaat is de parameterwaarde van de queryreeks `Y` (als de browser cookies ondersteunt en ingeschakeld heeft) of `N` (als de browser cookies heeft uitgeschakeld). Als u AppMeasurement gebruikt (bijvoorbeeld via Adobe Experience Platform Launch), werkt deze dimensie buiten het vak. Als u een methode van de gegevensinzameling buiten AppMeasurement (zoals door API) gebruikt, zorg ervoor dat u de parameter van het `k` vraagkoord op elke slag met de waarde `Y` of `N`opneemt.

## Dimensiewaarden

De waarden van de afmeting omvatten `Enabled`, `Disabled`, en `Unknown`.

* **`Enabled`**: De browser ondersteunt cookies en heeft deze ingeschakeld.
* **`Disabled`**: De browser ondersteunt geen cookies of de bezoeker heeft deze uitgeschakeld.
* **`Unknown`**: AppMeasurement kon koekjessteun niet bepalen. De `k` queryreeks is niet aanwezig in de afbeeldingsaanvraag.
