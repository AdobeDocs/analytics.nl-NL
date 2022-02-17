---
title: Betaalde zoekopdracht
description: Hiermee onderscheidt u metriek van betaald en natuurlijk zoeken.
feature: Dimensions
exl-id: b12665a3-e92f-4fc1-acd3-ea17a316e5e5
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# Betaalde zoekopdracht

Met de dimensie &#39;Betaald zoeken&#39; kunt u naar elke meting kijken en deze vergelijken tussen betaalde zoekopdrachten en natuurlijk zoeken. Alle andere treffers buiten zoekmachines worden weggelaten. Deze dimensie is handig om te begrijpen hoe uw betaalde zoekopdracht zich verhoudt tot biologisch zoeken.

## Deze dimensie vullen met gegevens

Deze dimensie kan alleen goed functioneren als [Betaalde zoekdetectie](/help/admin/admin/paid-search-detection/paid-search-detection.md) correct geconfigureerd in de instellingen van de rapportsuite. Als de betaalde onderzoeksopsporing correct wordt gevormd en een rapportreeks gegevens heeft, werkt deze dimensie altijd.

## Dimension-items

Dimension-items bevatten twee statische waarden: `"Natural"` en `"Paid"`. Als een bezoek criteria voor een onderzoeksmotor aanpast en ook betaalde onderzoeksopsporing aanpast, behoort het tot `"Paid"` dimensie-item. Als een bezoek voldoet aan de criteria voor een zoekmachine en *niet* zoeken met betaald zoeken, hoort bij de `"Natural"` dimensie-item.
