---
title: Variabele overschrijvingen
description: Met overschrijvingen van variabelen kunt u een variabele waarde wijzigen voor één track- of trackkoppelingsaanroep.
translation-type: tm+mt
source-git-commit: 1f0fd2dcb0454ad9bc2e0c2141b5e17470c6a5de

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
