---
title: Overzicht van classificaties
description: Pas de groepering van dimensie-items aan.
feature: Classifications
exl-id: 0d2c77ea-610f-48e0-b6a2-6e91794783b1
source-git-commit: 2e07f1b9495801383b030b2396e5468c39299f50
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---

# Overzicht van classificaties

Een classificatie is een manier om de veranderlijke gegevens van Analytics te categoriseren, dan tonend de gegevens op verschillende manieren wanneer u rapporten produceert. U brengt een relatie tot stand tussen een variabele waarde en metagegevens die betrekking hebben op die waarde. De classificaties kunnen op de meeste douanedimensies, zoals [&#x200B; het Volgen code &#x200B;](/help/components/dimensions/tracking-code.md), [&#x200B; steunen &#x200B;](/help/components/dimensions/prop.md), en [&#x200B; eVars &#x200B;](/help/components/dimensions/evar.md) worden gebruikt.

* **de reeksen van de Classificatie** zijn de primaire componenten om gegevens te classificeren. [&#x200B; de reeksen van de Classificatie &#x200B;](/help/components/classifications/sets/overview.md) staan u toe om classificaties in één enkele, vereenvoudigde interface tot stand te brengen en te beheren.

* **Verouderde classificaties** documenteert de methodes van de erfenisclassificatie om gegevens te classificeren. Deze methoden zullen in de nabije toekomst verouderd zijn en zullen niet langer toegankelijk zijn.

   * [&#x200B; de regels van de Classificatie &#x200B;](/help/components/classifications/crb/classification-rule-builder.md): Creeer regels die een bepaald afmetingspunt aan een punt van de classificatiedimensie toewijzen. Deze methode voor het classificeren van gegevens is het best wanneer een dimensie vaak nieuwe unieke waarden aantreft of wanneer handmatige classificaties frequent en belastend zouden zijn. Deze functionaliteit wordt na 28 februari 2027 vervangen.

   * [&#x200B; de invoerder van de Classificatie &#x200B;](/help/components/classifications/importer/c-working-with-saint.md): Exporteer een malplaatjespreadsheet met afmetingspunten in elke rij. Kolommen geven elke classificatie voor een dimensie aan. Deze methode voor het classificeren van gegevens is het best wanneer alle dimensie-items bekend zijn en niet regelmatig hoeven te worden bijgewerkt. Deze functionaliteit wordt na 31 augustus 2026 vervangen. Met de afschrijving kunt u geen classificaties meer importeren met standaard-FTP.

Eén dimensie kan meerdere classificatiedimensies hebben. U kunt [!UICONTROL Product IDs] bijvoorbeeld indelen met aanvullende productkenmerken, zoals productnaam, kleur, grootte, beschrijving en SKU. Elk van deze kenmerken zou een afzonderlijke classificatiedimensie zijn die tot dezelfde bovenliggende dimensie behoort. Het uitbreiden van rapporten met deze kenmerken biedt diepere en complexere rapportagemogelijkheden. Zodra een dimensie classificatiegegevens bevat, is de classificatiedimensie beschikbaar in rapportage die alleen classificatiedimensies bevat. Om het even welk punt van de ouderdimensie dat geen classificatiewaarde bevat wordt gegroepeerd onder [&#x200B; Niet gespecificeerd &#x200B;](/help/technotes/unspecified.md)
