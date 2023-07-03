---
title: Classificatieregels
description: Regels voor een afzonderlijke classificatieset weergeven en bewerken.
exl-id: b3518aaa-382f-47ad-860f-b6af6ddb3cbc
feature: Classifications
source-git-commit: 811e321ce96aaefaeff691ed5969981a048d2c31
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---

# Classificatieregels

Met indelingssetregels kunt u waarden automatisch classificeren op basis van de waarde waarop de variabele is ingesteld. Deze regels zijn van toepassing op alle binnenkomende variabelewaarden voor alle abonnementen van de classificatieset.

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Sets]** > Klik op de gewenste naam van de classificatieset > **[!UICONTROL Rules]**

## Regelinstellingen

Instellingen die van toepassing zijn op de gehele set regels.

* **[!UICONTROL Rules overwrite]**: Bepaalt het gedrag van alle regels in gevallen waar een classificatiewaarde bestaat.
   * **[!UICONTROL Apply to all values]**: Als een regel overeenkomt, overschrijft u altijd de classificatiewaarde.
   * **[!UICONTROL Apply only to unset values]**: Als een regel overeenkomt, schrijft u alleen de classificatiewaarde als deze leeg is. Als er een classificatiewaarde bestaat, doet u niets.
* **[!UICONTROL Lookback window]**: Wanneer deze regel wordt geactiveerd, lopen alle regels tegen alle unieke waarden die binnen het terugkijkvenster worden gezien dat hier wordt geplaatst.

## Regels

Een lijst met regels die voor elke unieke waarde worden uitgevoerd.

* **[!UICONTROL Search]**: Een zoekvak waarmee u regels kunt filteren op criteria die overeenkomen.
* **[!UICONTROL Add rule]**: Hiermee voegt u een lege rij toe aan de regeltabel.
* **[!UICONTROL Test rule set]**: Brings up a test UI die u toestaat om uw regels te bevestigen. Links kunt u handmatig sleutelwaarden typen of een classificatiebestand slepen en neerzetten om veel waarden te importeren die u wilt testen. Rechts is een tabel met voorlopige resultaten van hoe geclassificeerde waarden eruit zouden zien als de regelset zou worden geactiveerd. Aangezien deze interface alleen voor validatie is, worden geen waarden geclassificeerd.

Selecteer een of meer regels door op het selectievakje naast de gewenste regel te klikken. Als u een regel selecteert, worden de volgende opties weergegeven:

* **[!UICONTROL Delete]**: Hiermee verwijdert u de rij uit de regeltabel.
* **[!UICONTROL Duplicate]**: Hiermee kopieert u de geselecteerde rijen naar nieuwe rijen in de regeltabel.

## Regeltabel

De regeltabel wordt verticaal gescheiden in twee hoofdonderdelen: overeenstemmende voorwaarde en indelingsactie. Elke rij (een afzonderlijke regel) bevat een overeenkomende voorwaarde en een classificatiehandeling.

* **Regelnummer**: De regels lopen in de zelfde orde dat u de regellijst vormt. Indien [!UICONTROL Rules overwrite] is ingesteld op [!UICONTROL Apply to all values], vervangt de laatste passende regel om het even welke vorige regels voor de zelfde classificatiedimensie. Indien [!UICONTROL Rules overwrite] is ingesteld op [!UICONTROL Apply to only unset values]De eerste regel die een classificatiewaarde instelt, is van toepassing.
* **[!UICONTROL Select rule type]**: De regelcriteria. Opties omvatten [!UICONTROL Contains], [!UICONTROL Ends with], [!UICONTROL Regular expression], [!UICONTROL Regular expression], en [!UICONTROL Starts with].
* **[!UICONTROL Enter match criteria]**: De tekenreeks die moet overeenkomen. Als u [!UICONTROL Regular expression] als regeltype wordt een bedekking weergegeven waarmee u de waarde kunt invoeren, de reguliere expressie kunt testen en een voorbeeldsyntaxis kunt opgeven.
* **[!UICONTROL Set classification]**: Een vervolgkeuzelijst die de classificatiedimensie instelt waaraan u een waarde wilt toewijzen. Geldige opties zijn elementen in uw [schema](schema.md).
* **[!UICONTROL To]**: De tekstreeks waarop de geclassificeerde waarde moet worden ingesteld. Als het regeltype [!UICONTROL Regular expression]kunt u een combinatie van tekst en overeenkomende groepen opnemen.
