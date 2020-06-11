---
title: Betaalde zoekopdracht
description: Hiermee onderscheidt u metriek van betaald en natuurlijk zoeken.
translation-type: tm+mt
source-git-commit: d71edc74644907b47bfb6492e7a6c47c06d5984f
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---


# Betaalde zoekopdracht

Met de dimensie &#39;Betaald zoeken&#39; kunt u naar elke meting kijken en deze vergelijken tussen betaalde zoekopdrachten en natuurlijk zoeken. Alle andere treffers buiten zoekmachines worden weggelaten. Deze dimensie is handig om te begrijpen hoe uw betaalde zoekopdracht zich verhoudt tot biologisch zoeken.

## Deze dimensie vullen met gegevens

De enige vereiste voor deze dimensie om behoorlijk te werken moet [Betaalde onderzoeksopsporing](/help/admin/admin/paid-search-detection/paid-search-detection.md) hebben correct in de montages van de rapportreeks wordt gevormd. Als de betaalde onderzoeksopsporing correct wordt gevormd en een rapportreeks gegevens heeft, werkt deze dimensie altijd.

## Dimensiewaarden

Dimensiewaarden zijn twee statische waarden: `"Natural"` en `"Paid"`. Als een bezoek criteria voor een onderzoeksmotor aanpast en ook betaalde onderzoeksopsporing aanpast, behoort het tot de `"Paid"` afmetingswaarde. Als een bezoek criteria voor een onderzoeksmotor aanpast en betaalde onderzoeksopsporing *niet* aanpast, behoort het tot de `"Natural"` afmetingswaarde.
