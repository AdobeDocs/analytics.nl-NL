---
title: Product
description: De naam van het product.
translation-type: tm+mt
source-git-commit: 6778dd290424651dc959224daa0eef8ebd8196e5
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 1%

---


# Product

De dimensie &#39;Product&#39; rapporteert de naam van het product in de hit. Het is handig voor implementaties die gebruikmaken van de `products` variabele en die meetgegevens willen zien rond producten, zoals topverkopers of de meeste weergegeven. Deze dimensie kan opzettelijk leeg zijn als u geen producten op uw site hebt.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar het tweede deel van de tekenreeks in de [`products`](/help/implement/vars/page-vars/products.md) variabele. Deze dimensie wordt gevuld door tekens tussen de eerste en de tweede puntkomma (`;`).

## Dimension-items

Aangezien deze variabele op een douanekoord in uw implementatie gebaseerd is, bepaalt uw organisatie wat de afmetingspunten zijn. Adobe raadt u aan een consistente naamgevingsconventie voor producten vast te stellen. [Classificaties](../classifications/c-classifications.md) zijn beschikbaar als u producten anders wilt groeperen of een vriendelijkere naam wilt opgeven. Adobe beveelt aan zowel de afmetingen &#39;Product&#39; als &#39;Categorie&#39; te gebruiken.
