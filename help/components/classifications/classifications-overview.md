---
title: Overzicht van classificaties
description: Pas de groepering van dimensie-items aan.
feature: Classifications
exl-id: 0d2c77ea-610f-48e0-b6a2-6e91794783b1
source-git-commit: 1e209d4313c3d9d67f15a0c3a0939ceeb7a1ed31
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Overzicht van classificaties

Een classificatie is een manier om de veranderlijke gegevens van Analytics te categoriseren, dan tonend de gegevens op verschillende manieren wanneer u rapporten produceert. U brengt een relatie tot stand tussen een variabele waarde en metagegevens die betrekking hebben op die waarde. De classificaties kunnen op de meeste douanedimensies, zoals [ het Volgen code ](/help/components/dimensions/tracking-code.md), [ steunen ](/help/components/dimensions/prop.md), en [ eVars ](/help/components/dimensions/evar.md) worden gebruikt.

* **de reeksen van de Classificatie** zijn de primaire componenten om gegevens te classificeren. [ de reeksen van de Classificatie ](/help/components/classifications/sets/overview.md) staan u toe om classificaties in één enkele, vereenvoudigde interface tot stand te brengen en te beheren.

* **Verouderde classificaties** documenteert de methodes van de erfenisclassificatie om gegevens te classificeren. Deze methoden zijn verouderd en zijn na 31 augustus 2026 niet meer toegankelijk.

   * [ de regels van de Classificatie ](/help/components/classifications/crb/classification-rule-builder.md): Creeer regels die een bepaald afmetingspunt aan een punt van de classificatiedimensie toewijzen. Deze methode voor het classificeren van gegevens is het best wanneer een dimensie vaak nieuwe unieke waarden aantreft of wanneer handmatige classificaties frequent en belastend zouden zijn.
   * [ de invoerder van de Classificatie ](/help/components/classifications/importer/c-working-with-saint.md): Exporteer een malplaatjespreadsheet met afmetingspunten in elke rij. Kolommen geven elke classificatie voor een dimensie aan. Deze methode voor het classificeren van gegevens is het best wanneer alle dimensie-items bekend zijn en niet regelmatig hoeven te worden bijgewerkt.

Eén dimensie kan meerdere classificatiedimensies hebben. U kunt [!UICONTROL Product IDs] bijvoorbeeld indelen met aanvullende productkenmerken, zoals productnaam, kleur, grootte, beschrijving en SKU. Elk van deze kenmerken zou een afzonderlijke classificatiedimensie zijn die tot dezelfde bovenliggende dimensie behoort. Het uitbreiden van rapporten met deze kenmerken biedt diepere en complexere rapportagemogelijkheden. Zodra een dimensie classificatiegegevens bevat, is de classificatiedimensie beschikbaar in rapportage die alleen classificatiedimensies bevat. Om het even welk punt van de ouderdimensie dat geen classificatiewaarde bevat wordt gegroepeerd onder [ Niet gespecificeerd ](/help/technotes/unspecified.md)
