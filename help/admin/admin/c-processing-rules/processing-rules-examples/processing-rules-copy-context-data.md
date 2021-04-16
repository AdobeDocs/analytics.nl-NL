---
description: Verwerkingsregels worden gebruikt om waarden van variabelen van de Gegevens van de Context naar steunen en eVars te bewegen.
subtopic: Processing rules
title: Een contextdatavariabele kopiëren naar een eVar
feature: Admin Tools
uuid: 1beaec4c-71e9-49ce-b154-78408cc532a3
exl-id: f52c2c6c-da3d-43d6-be13-92d0820c93b4
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 8%

---

# Een contextdatavariabele kopiëren naar een eVar

De verwerkingsregels worden gebruikt om waarden van de variabelen van contextgegevens naar steunen en eVars te bewegen. Zonder verwerkingsregels hebben contextgegevensvariabelen geen betekenis en vullen ze geen rapporten in Analytics.

De lijst [!UICONTROL Context Variables] bevat alle variabelen die in de voorafgaande 30 dagen naar de rapportreeks zijn verzonden. Als u de naam van de variabele van contextgegevens kent maar niet het in de huidige rapportreeks hebt verzonden, kunt u een waarde toevoegen door de variabelenaam te typen en **[!UICONTROL Add variable name context data]** te klikken:

![Toevoegen](assets/add-context-variable.png)

In het volgende voorbeeld wordt de contextgegevensvariabele `search_term` geplaatst en wordt de waarde ervan in `eVar3` geplaatst:

![Set](assets/set-context-data.png)

Het bovenstaande voorbeeld werkt prima als er slechts een paar eVars zijn om te vullen. Als uw organisatie honderden variabelen van contextgegevens heeft die elk hun eigen eVar nodig hebben, kunt u voorwaardelijke verklaringen gebruiken. Tientallen voorwaardelijke instructies passen binnen één verwerkingsregel, zodat uw organisatie alle eVars in een rapportsuite kan vullen zonder dat de verwerkingsregellimiet van 150 regels wordt overschreden.

In het volgende voorbeeld wordt `prop7` gevuld met de contextgegevensvariabele `testhierarchy`, maar alleen als `testhierarchy` is ingesteld:

![Voorwaardelijk](assets/add-conditional.png)

Zie [Contextgegevensvariabelen](/help/implement/vars/page-vars/contextdata.md) in de gebruikershandleiding Implementeren voor meer informatie over het implementeren van contextgegevensvariabelen.
