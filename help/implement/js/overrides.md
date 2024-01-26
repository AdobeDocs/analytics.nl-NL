---
title: Variabele overschrijvingen
description: Met overschrijvingen van variabelen kunt u een variabele waarde wijzigen voor één track of koppeling.
feature: Implementation Basics
exl-id: e297ef94-c5f7-42b1-a9d0-57e073f0d1a9
role: Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---

# Variabele overschrijvingen

Met overschrijvingen van variabelen kunt u de analysewaarden voor een enkele hit wijzigen zonder dat dit van invloed is op bestaande variabelen op de pagina.

## Workflow

1. Maak een nieuw JavaScript-object. De objectnaam kan alles zijn wat u wilt.

   ```js
   var y = new Object();
   ```

2. Wijs geldige eigenschappen voor Analytics toe aan dit object:

   ```js
   y.eVar1 = "New value";
   y.events = "event2";
   ```

3. Gebruik het object als een argument binnen de juiste volgende aanroep:

   ```js
   // Use the override object in a standard page view call
   s.t(y);
   
   // Use the override object in a link tracking call
   s.tl(this,'o','Example override link',y);
   ```

Wanneer een volgende vraag een voorwerp in de met voeten getreden parameter ontvangt, overschrijven alle geldige waarden in het met voeten getreden voorwerp waarden in het standaard voorwerp Analytics. Variabelen die al in het bestaande object Analytics zijn gedefinieerd, worden niet beïnvloed.
