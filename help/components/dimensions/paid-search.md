---
title: Betaalde zoekopdracht
description: Hiermee onderscheidt u metriek van betaald en natuurlijk zoeken.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---


# Betaalde zoekopdracht

Met de dimensie &#39;Betaald zoeken&#39; kunt u naar elke meting kijken en deze vergelijken tussen betaalde zoekopdrachten en natuurlijk zoeken. Alle andere treffers buiten zoekmachines worden weggelaten. Deze dimensie is handig om te begrijpen hoe uw betaalde zoekopdracht zich verhoudt tot biologisch zoeken.

## Deze dimensie vullen met gegevens

De enige vereiste voor deze dimensie om behoorlijk te werken moet [Betaalde onderzoeksopsporing](/help/admin/admin/paid-search-detection/paid-search-detection.md) hebben correct in de montages van de rapportreeks wordt gevormd. Als de betaalde onderzoeksopsporing correct wordt gevormd en een rapportreeks gegevens heeft, werkt deze dimensie altijd.

## Dimensie-items

Dimensie-items bevatten twee statische waarden: `"Natural"` en `"Paid"`. Als een bezoek criteria voor een onderzoeksmotor aanpast en ook betaalde onderzoeksopsporing aanpast, behoort het tot het `"Paid"` afmetingspunt. Als een bezoek criteria voor een onderzoeksmotor aanpast en betaalde onderzoeksopsporing *niet* aanpast, behoort het tot het `"Natural"` afmetingspunt.
