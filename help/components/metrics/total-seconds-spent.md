---
title: Totaal aantal bestede seconden
description: Het geaggregeerde totale aantal seconden dat aan het dimensie-item wordt besteed.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# Totaal aantal bestede seconden

De metrische waarde &#39;Totaal aantal bestede seconden&#39; toont het geaggregeerde aantal seconden dat een bezoeker heeft doorgebracht aan een bepaald afmetingsitem. Deze metrisch is nuttig wanneer u de ruwe hoeveelheid tijd wilt doorbrengen aan een bepaald afmetingspunt, en niet gemiddelden zoals andere tijd doorgebrachte metriekaanbieding.

In de Bouwer van het Rapport, wordt dit metrisch genoemd &quot;Totale bestede tijd&quot;.

## Hoe deze metrische waarde wordt berekend

Deze metrisch gebruikt de volgende stappen om berekening te meten:

1. Kijk voor een bepaalde hit naar de tijdstempel.
2. Vergelijk deze hit met de tijdstempel van de volgende hit in het bezoek. In zowel de paginaweergave als het bijhouden van koppelingen wordt het aantal treffers weergegeven.
3. De hoeveelheid seconden die tussen de twee hits is verstreken, dragen bij aan het dimensie-item.

Persisted variabelen, zoals [eVars](../dimensions/evar.md), tellen naar het totale aantal seconden dat wordt doorgebracht. De variabelen van het verkeer, zoals [steunen](../dimensions/prop.md), omvatten seconden besteed over verdere verbinding het volgen vraag.

>[!TIP]
>
>De tijd die wordt besteed wordt niet gemeten voor de laatste hit van het bezoek aangezien er geen volgende beeldverzoek is om verstreken tijd te meten. Dit concept geldt ook voor bezoeken die bestaan uit één enkele hit (een stuit).

Zie [Tijd besteed overzicht](time-spent.md) voor meer algemene informatie over bestede tijd.
