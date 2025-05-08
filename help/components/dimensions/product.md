---
title: Product
description: De naam van het product.
feature: Dimensions
exl-id: 2649c200-4b0a-49a9-8592-9b9af72b91cf
source-git-commit: a40f30bbe8fdbf98862c4c9a05341fb63962cdd1
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 1%

---

# Product

De &quot;dimensie van het Product&quot;[&#128279;](overview.md) meldt de naam van het product in de slag. Dit is handig voor implementaties die de variabele `products` gebruiken en die meetgegevens willen zien rond producten, zoals topverkopers of de meeste weergegeven. Deze dimensie kan opzettelijk leeg zijn als u geen producten op uw site hebt.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar het tweede deel van de tekenreeks in de variabele [`products`](/help/implement/vars/page-vars/products.md) . De karakters tussen eerste en tweede puntkomma (`;`) bevolkt deze afmeting.

## Dimension-objecten

Aangezien deze variabele op een douanekoord in uw implementatie gebaseerd is, bepaalt uw organisatie wat de afmetingspunten zijn. Adobe raadt u aan een consistente naamgevingsconventie voor producten vast te stellen. [ classificaties ](../classifications/classifications-overview.md) zijn beschikbaar als u producten verschillend wilt groeperen of een vriendelijkere naam verstrekken. Adobe raadt aan zowel de afmetingen &#39;Product&#39; als &#39;Categorie&#39; te gebruiken.
