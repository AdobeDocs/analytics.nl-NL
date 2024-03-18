---
title: Een gegevenslaag maken
description: Leer wat een gegevenslaag in uw implementatie Analytics is, en hoe het kan worden gebruikt om variabelen in Adobe Analytics in kaart te brengen.
feature: Implementation Basics
exl-id: 271dd8fa-3ba1-4a7f-b16a-c48a736a5bb5
role: Admin, Developer, Leader
source-git-commit: 5ef8ba686a13f8b4ab592c0b48a9c074b0477fcf
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Een gegevenslaag maken

Een gegevenslaag is een raamwerk van JavaScript-objecten op uw site die de variabelenwaarden bevatten die worden gebruikt in uw analytische implementatie. Het staat grotere controle en gemakkelijker onderhoud toe wanneer het toewijzen van waarden aan de variabelen van de Analyse.

## Vereisten

[Een document voor het ontwerp van een oplossing maken](solution-design.md) - Het is belangrijk dat uw organisatie zich aanpast aan de traceervereisten. Zorg ervoor dat u met een document van het oplossingsontwerp alvorens ontwikkelingsteams in uw organisatie wordt voorbereid te benaderen.

## Workflow

Bij het implementeren van Adobe Analytics met een gegevenslaag worden doorgaans de volgende stappen uitgevoerd:

1. **Werk met uw team voor siteontwikkeling om een gegevenslaag te implementeren**: Het ontwikkelingsteam van uw site is primair verantwoordelijk voor het controleren of het gegevenslaagobject correct wordt gevuld. Controleer deze pagina met uw team van de plaatsontwikkeling om ervoor te zorgen de verwachtingen tussen teams worden gericht.

   >[!NOTE]
   >
   >Aanbevolen specificaties voor gegevenslagen van Adobe zijn optioneel. Als u reeds een gegevenslaag hebt, of anders verkiest om de specificaties van de Adobe niet te volgen, zorg ervoor dat uw organisatie zich op welke te volgen specificatie richt.

1. **Valideer uw gegevenslaag met een browserconsole**: Nadat een gegevenslaag is gemaakt, kunt u controleren of deze werkt met de ontwikkelaarsconsole van een browser. U kunt de ontwikkelaarsconsole in de meeste browsers openen gebruikend `F12` toets. Een waarde van een voorbeeldvariabele zou `adobeDataLayer.page.title`.
1. **Adobe Experience Platform-gegevensverzameling gebruiken om gegevenslaagobjecten toe te wijzen aan gegevenselementen**: Deze stap is afhankelijk van de implementatiemethode van uw organisatie:
   * **Als het gebruiken van SDK van het Web**: Wijs de gewenste gegevenslaagobjecten toe aan de gewenste XDM-velden in Adobe Experience Platform Edge. Zie [Analytics XDM variable mapping](../aep-edge/xdm-var-mapping.md) om de gewenste afbeelding van de gegevenslaag te bepalen.
   * **Indien de extensie Analytics wordt gebruikt**: Maak gegevenselementen onder Tags in Adobe Experience Platform-gegevensverzameling en wijs deze toe aan de gewenste gegevenslaagobjecten. Wijs vervolgens binnen de extensie Analytics elk gegevenselement toe aan de juiste variabele Analytics.

## Specificaties

Adobe raadt u aan de [Gegevenslaag client-Adobe](https://github.com/adobe/adobe-client-data-layer/wiki) voor nieuwe of geherstructureerde implementaties.

Uw organisatie is vrij om andere specificaties van de gegevenslaag te gebruiken, zoals [Klantenervaring met digitale gegevenslaag](https://www.w3.org/2013/12/ceddl-201312.pdf)of een andere aangepaste specificatie. Het is van het grootste belang dat de lagen worden uitgelijnd op een consistente gegevenslaag die voldoet aan de behoeften van uw organisatie.

Gegevenslagen zijn uitbreidbaar; als u specifieke vereisten voor uw organisatie hebt, kunt u objecten in uw gegevenslaag opnemen om aan die behoeften te voldoen.

## Waarden voor gegevenslagen instellen

Gegevenslagen genereren doorgaans aan de serverzijde, waarbij wordt verwezen naar dezelfde objecten die worden gebruikt om de site-inhoud samen te stellen. Stel de gegevenslaag van de site in op basis van de traceervereisten die zijn ingesteld in de [document ontwerp oplossing](solution-design.md).

## Volgende stappen

[Gegevenslaagobjecten toewijzen aan gegevenselementen](../launch/layer-to-elements.md): Gebruik de gegevenslaag van uw site in Adobe Experience Platform.
