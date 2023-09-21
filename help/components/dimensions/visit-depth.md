---
title: Diepte bezoeken
description: Op bezoek-gebaseerde dimensie die de diepte van het bezoek meldt.
feature: Dimensions
exl-id: 3e9aca08-2255-46ca-9949-77334ee7120e
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# Diepte bezoeken

De &#39;diepte van bezoek&#39; [dimensie](overview.md) meldt het aantal paginaweergaven dat de bezoeker tijdens het volledige bezoek heeft gezien. De diepte van een bezoek neemt alleen toe als de treffer een paginaweergave is en de [Pagina](page.md) dimensie is niet het zelfde als het de afmetingspunt van de laatste paginamening. Het is een op bezoek-gebaseerde dimensie, die betekent dat het de zelfde waarde voor het volledige bezoek bevat. Deze variabele wordt ingesteld voor alle treffers tijdens een bezoek nadat dat bezoek is beëindigd.

## Deze dimensie vullen met gegevens

Deze dimensie werkt uit de doos voor alle implementaties. Als een rapportsuite gegevens bevat, werkt deze dimensie.

## Dimension-items

Items van het Dimension bevatten de tekenreeks `"Pages per visit"` gevolgd door een getal dat het aantal pagina&#39;s van het bezoek weergeeft. Het item Dimensie van `"Pages per visit: 1"` vertegenwoordigt een bezoek van één pagina, terwijl het afmetingspunt `"Pages per visit: 8"` vertegenwoordigt een bezoek met 8 paginameningen (en om het even welk aantal verbinding het volgen vraag).

## Vergelijking met raakdiepte

Zie [Hoogte](hit-depth.md) voor een vergelijking van de afmetingen.
