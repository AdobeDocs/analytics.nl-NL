---
title: Cookie-ondersteuning
description: Hiermee bepaalt u of de browser cookies ondersteunt.
feature: Dimensions
exl-id: 07d4fe12-0d60-469d-98b1-e93ce5a0fd21
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---

# Cookie-ondersteuning

De &#39;Cookie-ondersteuning&#39; [dimensie](overview.md) meldt of browser cookies voor een bepaalde hit ondersteunt. Het is handig om de verhouding te bepalen tussen bezoekers die browsers gebruiken die cookies ondersteunen en bezoekers die deze opzettelijk uitschakelen.

## Deze dimensie vullen met gegevens

Deze dimensie verzamelt gegevens van de [`k` querytekenreeks](/help/implement/validate/query-parameters.md) in afbeeldingsaanvragen. AppMeasurement probeert een cookie met de naam `s_cc`, dan ontdekt of het koekje bestaat. Het resultaat is de parameterwaarde van het vraagkoord `Y` (als de browser cookies ondersteunt en ingeschakeld heeft) of `N` (als cookies zijn uitgeschakeld in de browser). Als u AppMeasurement gebruikt (zoals door markeringen in Adobe Experience Platform), werkt deze afmeting uit de doos. Als u een methode voor gegevensverzameling buiten het AppMeasurement gebruikt (bijvoorbeeld via de API), moet u de opdracht `k` de parameter van het vraagkoord op elke slag met de waarde `Y` of `N`.

## Dimension-items

Tot Dimension-items behoren `Enabled`, `Disabled`, en `Unknown`.

* **`Enabled`**: De browser ondersteunt cookies en heeft deze ingeschakeld.
* **`Disabled`**: De browser ondersteunt geen cookies of de bezoeker heeft deze uitgeschakeld.
* **`Unknown`**: AppMeasurement kan ondersteuning voor cookies niet bepalen. De `k` queryreeks is niet aanwezig in de afbeeldingsaanvraag.
