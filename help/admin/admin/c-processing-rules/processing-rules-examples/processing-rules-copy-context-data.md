---
description: Verwerkingsregels worden gebruikt om waarden van variabelen van de Gegevens van de Context naar steunen en eVars te bewegen.
subtopic: Processing rules
title: Kopieer een variabele van contextgegevens naar een eVar
topic: Admin tools
uuid: 1beaec4c-71e9-49ce-b154-78408cc532a3
translation-type: tm+mt
source-git-commit: 984d6034d14cc4256d93bd4f7d1a7f01b63b71e9

---


# Kopieer een variabele van contextgegevens naar een eVar

De verwerkingsregels worden gebruikt om waarden van de variabelen van contextgegevens naar steunen en eVars te bewegen. Zonder verwerkingsregels hebben contextgegevensvariabelen geen betekenis en vullen ze geen rapporten in Analytics.

De [!UICONTROL Context Variables] lijst bevat alle variabelen die de afgelopen 30 dagen naar de rapportsuite zijn verzonden. Als u de naam van de variabele van contextgegevens kent maar niet het in de huidige rapportreeks hebt verzonden, kunt u een waarde toevoegen door de veranderlijke naam te typen en te klikken **[!UICONTROL Add variable name context data]**:

![Toevoegen](assets/add-context-variable.png)

In het volgende voorbeeld wordt de variabele `search_term` met contextgegevens geplaatst in `eVar3`:

![Set](assets/set-context-data.png)

Het bovenstaande voorbeeld werkt prima als er slechts een paar eVars zijn om te vullen. Als uw organisatie honderden variabelen van contextgegevens heeft die elk hun eigen eVar nodig hebben, kunt u voorwaardelijke verklaringen gebruiken. Tientallen voorwaardelijke instructies passen binnen één verwerkingsregel, zodat uw organisatie alle eVars in een rapportsuite kan vullen zonder dat de verwerkingsregellimiet van 150 regels wordt overschreden.

In het volgende voorbeeld wordt `prop7` de variabele contextgegevens ingevuld, maar alleen als `testhierarchy``testhierarchy` deze is ingesteld:

![Voorwaardelijk](assets/add-conditional.png)

Voor meer informatie over het uitvoeren van de variabelen van contextgegevens, zie de variabelen [van](/help/implement/vars/page-vars/contextdata.md) de Context- gegevens in de de gebruikersgids van het Uitvoeren.
