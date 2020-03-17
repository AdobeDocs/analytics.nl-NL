---
title: Overzicht van variabelen, functies, methoden en plug-ins
description: Leer welke variabelen u kunt opnemen in de gegevens die u naar Adobe verzendt om de rapportage te verbeteren.
keywords: appmeasurement,variables,vars,configuration,page,implementation
translation-type: tm+mt
source-git-commit: 7a1c3c7ed0e509969e281e865e8ff2c969a18bcb

---


# Overzicht van variabelen, functies, methoden en plug-ins

Analytics biedt een aantal variabelen voor het verzamelen van analysegegevens. Variabelen in deze sectie worden in verschillende secties gesplitst:

* **Paginabariabelen** zijn waarden die doorgaans rechtstreeks worden gebruikt voor de rapportage. Veelvoorkomende paginariabelen zijn `props`, `eVars`en `events`.
* **Configuratievariabelen** zijn instellingswaarden die ervoor zorgen dat de juiste gegevens bij Adobe terechtkomen. Veelvoorkomende configuratievariabelen zijn `trackingServerSecure`, `charSet`en `linkTrackVars`. In configuratievariabelen worden gewoonlijk geen waarden voor dimensies gevuld.
* **Functies en methoden** zijn stukken code die een specifieke taak uitvoeren wanneer ernaar wordt verwezen. Veelvoorkomende functies zijn `t()`, `tl()`en `clearVars()`.

## Variabelen en uitvoeringsmethoden

Adobe biedt meerdere manieren om Adobe Analytics te implementeren. Elke pagina bevat een sectie over het implementeren van de variabele met behulp van Launch en AppMeasurement voor JavaScript.

## Volgorde van de verrichtingen

AppMeasurement-bibliotheken die door Adobe Analytics worden gepubliceerd, hebben een specifieke volgorde wanneer ze gegevens naar Adobe verzenden. Als u deze taken uit orde uitvoert, kunnen de gegevens onvolledig zijn.

1. Als uw site een gegevenslaag gebruikt, moet u ervoor zorgen dat eerst alle toepasselijke variabelen worden ingevuld. Zie [Gegevenslaag](../prepare/data-layer.md) voor meer informatie.
2. Gebruik de gegevenslaag om analytische variabelen te vullen. Als u Lancering gebruikt, wordt deze taak gemakkelijk verwezenlijkt door gegevenselementen te gebruiken, dan toewijzend het gegevenselement aan een variabele. Zie [Gegevenselementen](https://docs.adobe.com/content/help/en/launch/using/reference/manage-resources/data-elements.html) in de gebruikershandleiding bij Starten.
3. Roep de functie tracking aan. De meeste AppMeasurement-bibliotheken gebruiken de `t()` functie, maar het gebruik van sommige mobiele SDK&#39;s `track()`. Wanneer de functie voor bijhouden wordt aangeroepen, worden alle ondersteunde variabelen die in het object Analytics zijn gedefinieerd, naar Adobe verzonden in de vorm van een afbeeldingsaanvraag.

## Ongeldige tekens

De volgende tekens en tekenreeksen zijn nooit toegestaan in JavaScript-variabelen.

* Tab (`0x09`)
* Regeleinde (`0x0D`)
* Newline (`0x0A`)
* HTML-tags (bijvoorbeeld `<b></b>` of `&#153`)

Sommige variabelen hebben extra beperkingen of syntaxisvereisten. Met de variabele worden bijvoorbeeld puntkomma&#39;s en komma&#39;s `products` gereserveerd om afzonderlijke producten en categorieën te scheiden.
