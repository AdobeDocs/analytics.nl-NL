---
title: Prop
description: Een aangepaste dimensie die u kunt gebruiken in rapporten.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---


# Prop

*Deze Help-pagina beschrijft hoe props werken als een dimensie. Voor informatie over hoe te om steunen uit te voeren, zie[steunen](/help/implement/vars/page-vars/prop.md)in de de gebruikersgids van het Uitvoeren.*

Props zijn aangepaste variabelen die u op de gewenste manier kunt gebruiken. Ze blijven niet bestaan na de hit die ze zijn ingesteld.

>[!TIP]
>
>Adobe raadt u in de meeste gevallen aan [eVars](evar.md) te gebruiken. In eerdere versies van Adobe Analytics hadden props en eVars voor- en nadelen voor elkaar. Adobe heeft echter verbeteringen aangebracht in Vars waarin vrijwel alle gevallen van gebruik voor props zijn opgenomen.

Als u een document [van het](/help/implement/prepare/solution-design.md)oplossingsontwerp hebt, kunt u deze douanedimensies aan waarden toewijzen specifiek voor uw organisatie. Het aantal beschikbare proefdrukken is afhankelijk van uw contract met Adobe. Er zijn maximaal 75 props beschikbaar als uw contract met Adobe dit ondersteunt.

## Proefdrukken met gegevens vullen

Elke eigenschap verzamelt gegevens van de reeks [`c1` - `c75` queryreeks](/help/implement/validate/query-parameters.md) in afbeeldingsaanvragen. Bijvoorbeeld, verzamelt de parameter van het `c1` vraagkoord gegevens voor prop1, terwijl de parameter van het `c68` vraagkoord gegevens voor prop68 verzamelt.

AppMeasurement, waarmee JavaScript-variabelen worden gecompileerd in een afbeeldingsaanvraag voor gegevensverzameling, gebruikt de variabelen `prop1` - `prop75`. Zie [hulpmiddel](/help/implement/vars/page-vars/prop.md) in de de gebruikersgids van het Uitvoeren voor implementatierichtlijnen.

## Dimensie-items

Aangezien de steunen douanetekenreeksen in uw implementatie bevatten, bepaalt uw organisatie wat de afmetingspunten voor elke klem zijn. Zorg ervoor u het doel van elke steun en typische afmetingspunten in een document [van het](/help/implement/prepare/solution-design.md)oplossingsontwerp registreert.

## Waarde van props over eVars

Adobe raadt u in de meeste gevallen aan eVars te gebruiken. Uitzonderingen op deze verklaring zijn als volgt:

* U kunt profielen gebruiken in real-time rapporten. Het duurt ten minste 30 minuten om in de rapportage te verschijnen.
* Props kunnen lijsteigenschappen worden, die meerdere waarden in dezelfde hit accepteren. Lijstvariabelen zijn een afzonderlijke variabele en er zijn slechts drie lijstvariabelen beschikbaar.
* Wanneer u het plakken op een hulpmiddel toelaat, worden de [Ingang](entry-dimensions.md) en de afmetingen van de [Uitgang](exit-dimensions.md) onmiddellijk beschikbaar. Als u entry- en exit-afmetingen voor eVars wilt, kunt u handmatig een segment maken.

Zie [Var](evar.md) voor meer vergelijkingen tussen props en eVars.
