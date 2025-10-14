---
title: Betaalde zoekopdracht
description: Hiermee onderscheidt u metriek van betaald en natuurlijk zoeken.
feature: Dimensions
exl-id: b12665a3-e92f-4fc1-acd3-ea17a316e5e5
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# Betaalde zoekopdracht

De &quot;Betaalde onderzoek&quot;[&#x200B; dimensie &#x200B;](overview.md) laat u om het even welke metrisch bekijken en het tussen betaald onderzoek en natuurlijk onderzoek vergelijken. Alle andere treffers buiten zoekmachines worden weggelaten. Deze dimensie is handig om te begrijpen hoe uw betaalde zoekopdracht zich verhoudt tot biologisch zoeken.

## Deze dimensie vullen met gegevens

Het enige vereiste voor deze dimensie om behoorlijk te werken is [&#x200B; Betaalde onderzoeksopsporing &#x200B;](/help/admin/tools/manage-rs/edit-settings/general/paid-search-detection/paid-search-detection.md) te hebben die correct in de montages van de rapportreeks wordt gevormd. Als de betaalde onderzoeksopsporing correct wordt gevormd en een rapportreeks gegevens heeft, werkt deze dimensie altijd.

## Dimension-objecten

Dimension-items bevatten twee statische waarden: `"Natural"` en `"Paid"` . Als een bezoek criteria voor een onderzoeksmotor aanpast en ook betaalde onderzoeksopsporing aanpast, behoort het tot het `"Paid"` dimensie punt. Als een bezoek criteria voor een onderzoeksmotor aanpast en *niet* betaalde onderzoeksopsporing aanpast, behoort het tot het `"Natural"` afmetingspunt.
