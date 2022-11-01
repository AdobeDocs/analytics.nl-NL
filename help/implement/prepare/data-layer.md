---
title: Een datalaag maken
description: Leer wat een gegevenslaag in uw implementatie Analytics is, en hoe het kan worden gebruikt om variabelen in Adobe Analytics in kaart te brengen.
feature: Implementation Basics
exl-id: 271dd8fa-3ba1-4a7f-b16a-c48a736a5bb5
source-git-commit: 571192e27972f2bc15912481f9a578427e1c1cfb
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Een datalaag maken

Een gegevenslaag is een raamwerk van JavaScript-objecten op uw site die de variabelenwaarden bevatten die worden gebruikt in uw analytische implementatie. Het staat grotere controle en gemakkelijker onderhoud toe wanneer het toewijzen van waarden aan de variabelen van de Analyse.

## Vereisten

[Een document voor het ontwerp van een oplossing maken](solution-design.md) - Het is belangrijk dat uw organisatie zich aanpast aan de traceervereisten. Zorg ervoor dat u met een document van het oplossingsontwerp alvorens ontwikkelingsteams in uw organisatie wordt voorbereid te benaderen.

## Workflow

Bij het implementeren van Adobe Analytics met een gegevenslaag worden doorgaans de volgende stappen uitgevoerd:

1. **Werk met uw team van de plaatsontwikkeling om een gegevenslaag uit te voeren**: Uw team van de plaatsontwikkeling is hoofdzakelijk verantwoordelijk voor het ervoor zorgen van het voorwerp van de gegevenslaag bevolkt met correcte waarden. Controleer deze pagina met uw team van de plaatsontwikkeling om ervoor te zorgen de verwachtingen tussen teams worden gericht.

   >[!NOTE]
   >
   >De volgende Adobe aanbevolen gegevenslaagspecificaties is optioneel. Als u reeds een gegevenslaag hebt, of anders verkiest om Adobe geen specificaties te volgen, zorg ervoor dat uw organisatie zich op welke specificatie richt te volgen.

1. **Valideer uw gegevenslaag met een browserconsole**: Zodra een gegevenslaag wordt gecreeerd, kunt u bevestigen dat het gebruikend om het even welke browser ontwikkelaarsconsole werkt. U kunt de ontwikkelaarsconsole in de meeste browsers openen gebruikend `F12` toets. Een waarde van een voorbeeldvariabele zou `adobeDataLayer.page.title`.
1. **Adobe Experience Platform-gegevensverzameling gebruiken om gegevenslaagobjecten toe te wijzen aan gegevenselementen**: Deze stap is afhankelijk van de implementatiemethode van uw organisatie:
   * **Als het gebruiken van SDK van het Web**: Wijs de gewenste gegevenslaagobjecten toe aan de gewenste XDM-velden in Adobe Experience Platform Edge. Zie [Variabeletoewijzing Analyse](../aep-edge/variable-mapping.md) om de gewenste afbeelding van de gegevenslaag te bepalen.
   * **Indien de extensie Analytics wordt gebruikt**: Maak gegevenselementen onder Tags in de gegevensverzameling van Adobe Experience Platform en wijs deze toe aan de gewenste gegevenslaagobjecten. Wijs vervolgens binnen de extensie Analytics elk gegevenselement toe aan de juiste variabele Analytics.

## Specificaties

Adobe raadt u aan de [Gegevenslaag Adobe-client](https://github.com/adobe/adobe-client-data-layer/wiki) voor nieuwe of geherstructureerde implementaties.

Uw organisatie is vrij om andere specificaties van de gegevenslaag te gebruiken, zoals [Klantenervaring met digitale gegevenslaag](https://www.w3.org/2013/12/ceddl-201312.pdf)of een andere aangepaste specificatie. Het is van het grootste belang dat de lagen worden uitgelijnd op een consistente gegevenslaag die voldoet aan de behoeften van uw organisatie.

Gegevenslagen zijn uitbreidbaar; als u specifieke vereisten voor uw organisatie hebt, kunt u voorwerpen in uw gegevenslaag omvatten om die behoeften aan te passen.

## Waarden voor gegevenslagen instellen

Gegevenslagen genereren doorgaans aan de serverzijde, waarbij wordt verwezen naar dezelfde objecten die worden gebruikt om de site-inhoud samen te stellen. Stel de gegevenslaag van de site in op basis van de traceervereisten die zijn ingesteld in de [document ontwerp oplossing](solution-design.md).

## Volgende stappen

[Gegevenslaagobjecten toewijzen aan gegevenselementen](../launch/layer-to-elements.md): Gebruik de gegevenslaag van uw site in Adobe Experience Platform.
