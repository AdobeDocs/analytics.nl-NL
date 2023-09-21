---
title: Betaalde zoekopdracht
description: Hiermee onderscheidt u metriek van betaald en natuurlijk zoeken.
feature: Dimensions
exl-id: b12665a3-e92f-4fc1-acd3-ea17a316e5e5
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# Betaalde zoekopdracht

De &#39;betaalde zoekopdracht&#39; [dimensie](overview.md) laat u naar om het even welke metrisch kijken en het vergelijken tussen betaalde onderzoek en natuurlijk onderzoek. Alle andere treffers buiten zoekmachines worden weggelaten. Deze dimensie is handig om te begrijpen hoe uw betaalde zoekopdracht zich verhoudt tot biologisch zoeken.

## Deze dimensie vullen met gegevens

Alleen voor een goede werking van deze dimensie is een [Betaalde zoekdetectie](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/paid-search-detection/paid-search-detection.md) correct geconfigureerd in de instellingen van de rapportsuite. Als de betaalde onderzoeksopsporing correct wordt gevormd en een rapportreeks gegevens heeft, werkt deze dimensie altijd.

## Dimension-items

Items van het Dimension bevatten twee statische waarden: `"Natural"` en `"Paid"`. Als een bezoek criteria voor een onderzoeksmotor aanpast en ook betaalde onderzoeksopsporing aanpast, behoort het tot `"Paid"` dimensie-item. Als een bezoek voldoet aan de criteria voor een zoekmachine en *niet* zoeken met betaald zoeken, hoort bij de `"Natural"` dimensie-item.
