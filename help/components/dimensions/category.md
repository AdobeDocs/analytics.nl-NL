---
title: Categorie
description: De productcategorie van de hit.
feature: Dimensions
exl-id: 3517b417-1a44-4d3e-ac16-93fdc5f36404
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# Categorie

De dimensie &#39;Categorie&#39; rapporteert de productcategorie van de hit. Het is handig voor implementaties die de opdracht `products` en wil meetgegevens zien rond de productcategorie, zoals topverkopers of de meeste weergegeven. Deze dimensie kan opzettelijk leeg zijn als u geen producten op uw site hebt.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar het eerste deel van de tekenreeks in de [`products`](/help/implement/vars/page-vars/products.md) variabele. Alles vóór de eerste puntkomma (`;`) vult deze dimensie.

## Dimension-items

Aangezien deze variabele op een douanekoord in uw implementatie gebaseerd is, bepaalt uw organisatie wat de afmetingspunten zijn. Adobe raadt u aan afzonderlijke producten te groeperen in betekenisvolle categorieën, waarbij zowel de afmetingen &#39;Product&#39; als &#39;Categorie&#39; worden gebruikt.

>[!TIP]
>
>In eerdere versies van Adobe Analytics werden enkele beperkingen opgelegd aan de &#39;Categorie&#39;-dimensie vanwege de verwerkingsarchitectuur. Deze beperkingen zijn sindsdien opgeheven, toelatend u om het even welke metrisch en om het even welke onderbreking te gebruiken.
