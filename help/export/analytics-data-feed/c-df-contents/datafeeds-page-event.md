---
description: Opzoektabel om het type hit te bepalen op basis van paginagebeurtenis.
keywords: pagina;gebeurtenis;pagina_gebeurtenis;post_page_event
title: Opzoeken van paginagebeurtenissen
feature: Data Feeds
exl-id: ef0467df-b94b-4cec-b312-96d8f42c23b0
source-git-commit: e16b0d7b3fe585dc8e9274a77833ad5af3c63124
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Opzoeken van paginagebeurtenissen

Opzoektabel om het type van een hit te bepalen op basis van de waarde `page_event` . Zoals vermeld in de [ de kolomverwijzing van Gegevens ](datafeeds-reference.md), zijn de `page_event` en `post_page_event` kolommen tinyint ongetekend.

* Zie [`t()`](/help/implement/vars/functions/t-method.md) voor meer informatie over het implementeren van paginaweergaveoproepen voor AppMeasurement en de Web SDK.
* Zie [`tl()`](/help/implement/vars/functions/tl-method.md) voor meer informatie over het implementeren van aanroepen voor het bijhouden van koppelingen voor AppMeasurement en de Web SDK.
* Zie [ Adobe Analytics met Adobe Experience Platform Edge Network ](/help/implement/aep-edge/overview.md) uitvoeren om te begrijpen hoe Adobe Analytics XDM nuttige ladingen aan de types van paginagebeurtenis vertaalt.

| `page_event` value | `post_page_event` value | Beschrijving |
| --- | --- | --- |
| `0` | `0` | Alle standaardaanroepen voor paginaweergave. Dit is de standaardwaarde voor de meeste treffers. |
| `10` | `100` | Aangepaste koppelingen. Stel het koppelingstype in op `o` (AppMeasurement) of `xdm.web.webInteraction.type` op `other` (Web SDK of Mobile SDK). |
| `11` | `101` | Download koppelingen. Stel het koppelingstype in op `d` (AppMeasurement) of `xdm.web.webInteraction.type` op `download` (Web SDK of Mobile SDK). |
| `12` | `102` | Koppelingen afsluiten. Stel het koppelingstype in op `e` (AppMeasurement) of `xdm.web.webInteraction.type` op `exit` (Web SDK of Mobile SDK). |
| `31` | `76` | Start media |
| `32` | `77` | Media-updates (zonder andere variabele-verwerking) |
| `33` | `78` | Media-updates (met andere variabele-verwerking) |
| `40` | `80` | Enquête |
| `50` | `50` | Start streaming media |
| `51` | `51` | Streaming media sluiten |
| `52` | `52` | Streaming media scrubben |
| `53` | `53` | Streaming media in leven houden |
| `54` | `54` | Streaming media en begin |
| `55` | `55` | Streaming media en close |
| `56` | `56` | Streaming media en scrubben |
| `60` | `60` | Start media primetime |
| `61` | `61` | Premimetime-media sluiten |
| `62` | `62` | Primetime media scrubben |
| `63` | `63` | Primetime-media in leven houden |
| `64` | `64` | Primetime-media en begin |
| `65` | `65` | Primetime-media en sluiten |
| `66` | `66` | Primetime media en scrubben |
| `70` | `70` | Inclusief gegevens over doelactiviteit |
