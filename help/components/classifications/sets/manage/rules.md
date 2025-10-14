---
title: Classificatieregels
description: Regels voor een afzonderlijke classificatieset weergeven en bewerken.
exl-id: 1ccb6a20-1993-4fd3-90eb-9154d12d0ec7
feature: Classifications
source-git-commit: de12253f6db798f49d0cae34bf9cb6b7a3de17db
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---

# Classificatieregels

Met indelingssetregels kunt u waarden automatisch classificeren op basis van de waarde waarop de variabele is ingesteld. Deze regels zijn van toepassing op alle binnenkomende variabelewaarden voor alle abonnementen van de classificatieset.

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Sets]** > Klik op de gewenste naam van de classificatieset > **[!UICONTROL Rules]**

![&#x200B; classificatie vastgestelde regels UI &#x200B;](../../assets/csets-rules.png)

## Regelinstellingen

Instellingen die van toepassing zijn op de gehele set regels.

* **[!UICONTROL Rules overwrite]** - Bepaalt het gedrag van alle regels in gevallen waarin een classificatiewaarde bestaat.
   * **[!UICONTROL Apply to all values]**: als een regel overeenkomt, overschrijft u altijd de classificatiewaarde.
   * **[!UICONTROL Apply only to unset values]**: als een regel overeenkomt, noteert u alleen de classificatiewaarde als deze leeg is. Als er een classificatiewaarde bestaat, doet u niets.
* **[!UICONTROL Lookback window]**: Wanneer deze regel wordt geactiveerd, worden alle regels uitgevoerd tegen alle unieke waarden die worden weergegeven in het terugzoekvenster dat hier wordt ingesteld.

## Regels

Een lijst met regels die voor elke unieke waarde worden uitgevoerd.

* **[!UICONTROL Search]**: Een zoekvak waarmee u regels kunt filteren op criteria die overeenkomen.
* **[!UICONTROL Add rule]** - Voegt een lege rij aan de regellijst toe.
* **[!UICONTROL Test rule set]**: Brings up a test UI that allows you to validate your rules. Links kunt u handmatig sleutelwaarden typen of een classificatiebestand slepen en neerzetten om veel waarden te importeren die u wilt testen. Rechts is een tabel met voorlopige resultaten van hoe geclassificeerde waarden eruit zouden zien als de regelset zou worden geactiveerd. Aangezien deze interface alleen voor validatie is, worden geen waarden geclassificeerd.

Selecteer een of meer regels door op het selectievakje naast de gewenste regel te klikken. Als u een regel selecteert, worden de volgende opties weergegeven:

* **[!UICONTROL Delete]** - Hiermee verwijdert u de rij uit de regeltabel.
* **[!UICONTROL Duplicate]**: kopieert de geselecteerde rijen naar nieuwe rijen in de regeltabel.

## Regeltabel

De regeltabel wordt verticaal gescheiden in twee hoofdonderdelen: overeenkomende voorwaarde en indelingsactie. Elke rij (een afzonderlijke regel) bevat een overeenkomende voorwaarde en een classificatiehandeling.

* **aantal van de Regel**: De regels lopen in de zelfde orde dat u de regellijst vormt. Als [!UICONTROL Rules overwrite] is ingesteld op [!UICONTROL Apply to all values] , overschrijft de laatste overeenkomende regel eventuele vorige regels voor dezelfde classificatiedimensie. Als [!UICONTROL Rules overwrite] is ingesteld op [!UICONTROL Apply to only unset values] , wordt de eerste regel die een classificatiewaarde instelt, toegepast.
* **[!UICONTROL Select rule type]**: De regelcriteria. De opties zijn [!UICONTROL Contains] , [!UICONTROL Ends with] , [!UICONTROL Regular expression] , [!UICONTROL Regular expression] en [!UICONTROL Starts with] .
* **[!UICONTROL Enter match criteria]**: De tekenreeks die moet overeenkomen. Als u [!UICONTROL Regular expression] als regeltype selecteert, wordt een bedekking weergegeven waarmee u de waarde kunt invoeren, de reguliere expressie kunt testen en een voorbeeldsyntaxis kunt opgeven.
* **[!UICONTROL Set classification]**: Een vervolgkeuzelijst met de indelingsdimensie waaraan u een waarde wilt toewijzen. De geldige opties omvatten elementen in uw [&#x200B; schema &#x200B;](schema.md).
* **[!UICONTROL To]**: de tekenreeks waarop de geclassificeerde waarde moet worden ingesteld. Als het regeltype [!UICONTROL Regular expression] is, kunt u een combinatie van tekst en overeenkomende groepen opnemen.
