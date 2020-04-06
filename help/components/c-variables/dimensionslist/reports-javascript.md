---
description: Hiermee worden metrische gegevens weergegeven op basis van het feit of JavaScript voor het apparaat is ingeschakeld, uitgeschakeld of als "niet-geïdentificeerd" wordt geteld.
title: JavaScript-ondersteuning
topic: Reports
uuid: 7b95001a-cd35-478a-8b24-54d30666110d
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# JavaScript-ondersteuning

Hiermee worden metrische gegevens weergegeven op basis van het feit of JavaScript voor het apparaat is ingeschakeld, uitgeschakeld of als &quot;niet-geïdentificeerd&quot; wordt geteld.

>[!NOTE] Begin november 2016 zijn we van plan de beperking te verwijderen, waarbij JavaScript altijd wordt vermeld als *`disabled / unidentified`* voor mobiele apparaten.

Het JavaScript-rapport komt overeen met de kolom javascript in de onbewerkte gegevens.

javascript is een bezoek-vlakke gebied, zodat blijft het de waarde van eerste treffer in het bezoek. De kolom javascript is gebaseerd op de eerste waarde aanwezig in de j_jscript kolom (als een visit_reference slechts de eerste verwijzer van het bezoek zal voortzetten).

j_jscript wordt gevuld met parameter j uit de Adobe Analytics-afbeeldingsaanvraag.

Hier volgt een voorbeeld:

| Actief | j_jscript | javascript |
|---|---|---|
| 1 |  | 0 |
| 2 | 1.6 | 0 |
| 3 | 1.6 | 0 |

Dientengevolge, maakt het niet uit als u een versie javascript had die op één of ander punt in het bezoek wordt gespecificeerd - het zal altijd als niet Javascript worden getoond omdat de eerste treffer geen waarde voor j_jscript bevatte.
