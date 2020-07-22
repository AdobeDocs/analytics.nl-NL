---
title: Categorie
description: De productcategorie van de hit.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---


# Categorie

De dimensie &#39;Categorie&#39; rapporteert de productcategorie van de hit. Het is handig voor implementaties die gebruikmaken van de `products` variabele en die meetgegevens willen zien rond de productcategorie, zoals topverkopers of de meeste weergegeven gebruikers. Deze dimensie kan opzettelijk leeg zijn als u geen producten op uw site hebt.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar het eerste deel van de tekenreeks in de [`products`](/help/implement/vars/page-vars/products.md) variabele. Alles vóór de eerste puntkomma (`;`) vult deze dimensie.

## Dimensie-items

Aangezien deze variabele op een douanekoord in uw implementatie gebaseerd is, bepaalt uw organisatie wat de afmetingspunten zijn. Adobe raadt u aan afzonderlijke producten te groeperen in betekenisvolle categorieën, waarbij zowel de afmetingen &#39;Product&#39; als &#39;Categorie&#39; worden gebruikt.

>[!TIP]
>
>In eerdere versies van Adobe Analytics zijn enkele beperkingen opgelegd aan de dimensie &#39;Categorie&#39; vanwege de verwerkingsarchitectuur. Deze beperkingen zijn sindsdien opgeheven, toelatend u om het even welke metrisch en om het even welke onderbreking te gebruiken.
