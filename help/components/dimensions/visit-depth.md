---
title: Diepte bezoeken
description: Op bezoek-gebaseerde dimensie die de diepte van het bezoek meldt.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---


# Diepte bezoeken

De dimensie &#39;Visit depth&#39; rapporteert het aantal paginaweergaven dat de bezoeker tijdens het volledige bezoek heeft gezien. De diepte van een bezoek neemt alleen toe als de hit een paginaweergave is en de afmetingen van de [pagina](page.md) niet gelijk zijn aan het item met de afmetingen van de laatste paginaweergave. Het is een op bezoek-gebaseerde dimensie, die betekent dat het de zelfde waarde voor het volledige bezoek bevat. Deze variabele wordt ingesteld voor alle treffers tijdens een bezoek nadat dat bezoek is beëindigd.

## Deze dimensie vullen met gegevens

Deze dimensie werkt uit de doos voor alle implementaties. Als een rapportsuite gegevens bevat, werkt deze dimensie.

## Dimensie-items

Dimensie-items bevatten de tekenreeks `"Pages per visit"` gevolgd door een getal dat het aantal pagina&#39;s in het bezoek vertegenwoordigt. Het afmetingspunt van `"Pages per visit: 1"` vertegenwoordigt een enig-paginabezoek, terwijl het afmetingspunt een bezoek met 8 paginameningen (en om het even welk aantal verbinding het volgen vraag) `"Pages per visit: 8"` vertegenwoordigt.

## Vergelijking met raakdiepte

Zie [Piepdiepte](hit-depth.md) voor een vergelijking tussen de afmetingen.