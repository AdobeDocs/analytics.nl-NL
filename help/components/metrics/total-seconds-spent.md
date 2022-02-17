---
title: Totaal aantal bestede seconden
description: Het geaggregeerde totale aantal seconden dat aan het dimensie-item wordt besteed.
feature: Metrics
exl-id: 02302982-ce8c-44e9-9967-0a4f226f5e9e
source-git-commit: 7d5383e1ee3bee189d3dd48bc6b899f4108f7ba8
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# Totaal aantal bestede seconden

De metrische waarde &#39;Totaal aantal bestede seconden&#39; toont het geaggregeerde aantal seconden dat een bezoeker heeft doorgebracht aan een bepaald afmetingsitem. Deze metrisch is nuttig wanneer u de ruwe hoeveelheid tijd wilt doorbrengen aan een bepaald afmetingspunt, en niet gemiddelden zoals andere tijd doorgebrachte metriekaanbieding.

In Report Builder, wordt dit metrisch genoemd &quot;Totale bestede tijd&quot;.

## Hoe deze metrische waarde wordt berekend

Deze metrisch gebruikt de volgende stappen om berekening te meten:

1. Kijk voor een bepaalde hit naar de tijdstempel.
2. Vergelijk deze hit met de tijdstempel van de volgende hit in het bezoek. In zowel de paginaweergave als het bijhouden van koppelingen wordt het aantal treffers weergegeven.
3. De hoeveelheid seconden die tussen de twee hits is verstreken, dragen bij aan het dimensie-item.

Blijvende variabelen, zoals [eVars](../dimensions/evar.md), tel naar totale gebruikte seconden. Verkeersvariabelen, zoals [props](../dimensions/prop.md), omvat seconden doorgebracht over verdere verbinding het volgen vraag.

>[!TIP]
>
>De tijd die wordt besteed wordt niet gemeten voor de laatste hit van het bezoek aangezien er geen volgende beeldverzoek is om verstreken tijd te meten. Dit concept geldt ook voor bezoeken die bestaan uit één enkele hit (een stuit).

Zie [Overzicht van de tijd](time-spent.md) voor meer algemene informatie over de bestede tijd.
