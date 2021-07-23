---
title: Implementeren met tags in Adobe Experience Platform
description: Leer hoe u Adobe Analytics implementeert met tags
exl-id: 52990731-8a68-4779-ad42-6ec94b0aabd1
source-git-commit: 562ed0e190954b7687fa79efaf5c5c54eb202af8
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 0%

---

# Implementeren met tags in Adobe Experience Platform

>[!NOTE]
>Adobe Experience Platform Launch is omgedoopt tot een reeks technologieën voor gegevensverzameling in Experience Platform. Diverse terminologische wijzigingen zijn als gevolg hiervan in de productdocumentatie doorgevoerd. Raadpleeg het volgende [document](https://experienceleague.adobe.com/docs/experience-platform/tags/term-updates.html?lang=en) voor een geconsolideerde referentie van de terminologische wijzigingen.

Tijdens de levensduur van Adobe Analytics heeft Adobe verschillende methoden aangeboden om code op uw site te implementeren voor gegevensverzameling. Aanbevolen Adobe is via tags in Adobe Experience Platform.

De markeringen in de Inzameling van Gegevens van Adobe Experience Platform zijn een oplossing van het markeringsbeheer die u de code van de Analyse naast andere het etiketteren vereisten laat opstellen. Adobe biedt integratie met andere oplossingen en producten aan, en laat u douanecode opstellen. Al deze taken kunnen worden uitgevoerd zonder dat ontwikkelingsteams in uw organisatie code op uw site hoeven bij te werken.

Alle klanten met een actief Adobe Experience Cloud-contract kunnen tags gebruiken. Als u niet zeker bent als u toegang hebt, contacteer één van de het systeembeheerders van Experience Cloud van uw organisatie.

## Algemene workflow

De volgende stappen volgen voor het uitvoeren van een implementatie met tags:

1. **Toegang tot tags** verkrijgen: U kunt toegang tot Platforms tags verkrijgen via een systeembeheerder in uw organisatie.
2. **Een eigenschap** voor tags maken: Eigenschappen zijn overkoepelende containers die worden gebruikt om te verwijzen naar tagbeheergegevens.
3. **Distribueren naar een ontwikkelomgeving**: Zorg voor een omgeving waarin u de ontwikkeling van tags kunt doorlopen.
4. **Valideren en publiceren naar productie**: Zorg ervoor dat alles werkt en publiceer het live.

Zie [Een eigenschap voor de tag Analytics maken](create-analytics-property.md) om aan de slag te gaan.

## Aanvullende bronnen

Tags kunnen in hoge mate worden aangepast. Meer informatie over hoe u optimaal kunt profiteren van Adobe Analytics door de juiste gegevens op te nemen in uw implementatie.

* [Documentatie](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=en#) over tags: Leer hoe de interface werkt en welke extensies beschikbaar zijn.
* [Adobe Analytics-extensie](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html?lang=en): Gebruik de extensie Analytics om gegevens naar Adobe Analytics te verzenden.
* [Implementatievariabelen](../vars/overview.md): Bepaal welke variabelen u naar de servers van de gegevensinzameling wilt verzenden.
