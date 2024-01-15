---
description: Verwerkingsregels worden gebruikt om waarden van variabelen van de Gegevens van de Context naar steunen en eVars te bewegen.
subtopic: Processing rules
title: Een variabele met contextgegevens kopiëren naar een eVar
feature: Admin Tools
role: Admin
exl-id: f52c2c6c-da3d-43d6-be13-92d0820c93b4
source-git-commit: 429aaa43fdae669350bdb5a5a54a7d4b9b1c65f2
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# Een variabele met contextgegevens kopiëren naar een eVar

De verwerkingsregels worden gebruikt om waarden van de variabelen van contextgegevens naar steunen en eVars te bewegen. Zonder verwerkingsregels hebben contextgegevensvariabelen geen betekenis en vullen ze geen rapporten in Analytics.

De [!UICONTROL Context Variables] lijst bevat alle variabelen die in de afgelopen 30 dagen naar de rapportsuite zijn verzonden. Als u de naam van de variabele van de contextgegevens kent maar het niet naar de huidige rapportreeks hebt verzonden, kunt u een waarde toevoegen door de veranderlijke naam te typen en te klikken **[!UICONTROL Add variable name context data]**:

![Toevoegen](assets/add-context-variable.png)

In het volgende voorbeeld wordt het `search_term` context gegevensvariabele en plaatst zijn waarde in `eVar3`:

![Set](assets/set-context-data.png)

Het bovenstaande voorbeeld werkt prima als er slechts een paar eVars zijn om te vullen. Als uw organisatie honderden variabelen van contextgegevens heeft die elk hun eigen eVar nodig hebben, kunt u voorwaardelijke verklaringen gebruiken. Tientallen voorwaardelijke instructies passen binnen één verwerkingsregel, zodat uw organisatie alle eVars in een rapportsuite kan vullen zonder dat de verwerkingsregellimiet van 150 regels wordt overschreden.

In het volgende voorbeeld wordt het bestand gevuld `prop7` met de variabele contextgegevens `testhierarchy`, maar alleen als `testhierarchy` is ingesteld:

![Voorwaardelijk](assets/add-conditional.png)

Zie voor meer informatie over het implementeren van contextgegevensvariabelen [Contextgegevensvariabelen](/help/implement/vars/page-vars/contextdata.md) in de gebruikershandleiding Implementeren.
