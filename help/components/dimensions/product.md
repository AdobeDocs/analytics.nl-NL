---
title: Product
description: De naam van het product.
feature: Dimensions
exl-id: 2649c200-4b0a-49a9-8592-9b9af72b91cf
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 1%

---

# Product

De dimensie &#39;Product&#39; rapporteert de naam van het product in de hit. Het is handig voor implementaties die de opdracht `products` variabele en wil meetgegevens zien rond producten, zoals topverkopers of de meeste weergegeven. Deze dimensie kan opzettelijk leeg zijn als u geen producten op uw site hebt.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar het tweede deel van de tekenreeks in de [`products`](/help/implement/vars/page-vars/products.md) variabele. Teken tussen de eerste en de tweede puntkomma (`;`) vult deze dimensie.

## Dimension-items

Aangezien deze variabele op een douanekoord in uw implementatie gebaseerd is, bepaalt uw organisatie wat de afmetingspunten zijn. Adobe raadt u aan een consistente naamgevingsconventie voor producten vast te stellen. [Classificaties](../classifications/c-classifications.md) zijn beschikbaar als u producten anders wilt groeperen of een vriendelijkere naam wilt geven. Adobe beveelt aan zowel de afmetingen &#39;Product&#39; als &#39;Categorie&#39; te gebruiken.
