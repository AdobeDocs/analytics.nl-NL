---
title: Prop
description: Een aangepaste dimensie die u kunt gebruiken in rapporten.
feature: Dimensions
exl-id: cf8ad65b-bc54-473e-bcfc-9c981d23e782
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# Prop

*Deze Help-pagina beschrijft hoe props werken als een dimensie. Voor informatie over het implementeren van profielen raadpleegt u [props](/help/implement/vars/page-vars/prop.md) in de gebruikershandleiding Implementeren.*

Props zijn aangepaste variabelen die u op de gewenste manier kunt gebruiken. Ze blijven niet bestaan na de hit die ze zijn ingesteld.

>[!TIP]
>
>Adobe raadt u aan [eVars](evar.md) in de meeste gevallen. In vorige versies van Adobe Analytics hadden props en eVars voor- en nadelen. Adobe heeft echter verbeteringen doorgevoerd in de mate waarin ze bijna alle gevallen van gebruik voor props naleven.

Als u een [document ontwerp oplossing](/help/implement/prepare/solution-design.md)kunt u deze aangepaste afmetingen toewijzen aan waarden die specifiek zijn voor uw organisatie. Het aantal beschikbare props is afhankelijk van uw contract met Adobe. Er zijn maximaal 75 props beschikbaar als uw contract met Adobe dit ondersteunt.

## Proefdrukken met gegevens vullen

Elke eigenschap verzamelt gegevens uit de [`c1` - `c75` querytekenreeks](/help/implement/validate/query-parameters.md) in afbeeldingsaanvragen. De `c1` de parameter van het vraagkoord verzamelt gegevens voor prop1, terwijl `c68` de parameter van het vraagkoord verzamelt gegevens voor prop68.

AppMeasurement, waarmee JavaScript-variabelen worden gecompileerd in een afbeeldingsaanvraag voor gegevensverzameling, gebruikt de variabelen `prop1` - `prop75`. Zie [prop](/help/implement/vars/page-vars/prop.md) in de gebruikershandleiding Implementeren voor implementatierichtlijnen.

## Dimension-items

Aangezien de steunen douanetekenreeksen in uw implementatie bevatten, bepaalt uw organisatie wat de afmetingspunten voor elke klem zijn. Zorg ervoor u het doel van elke steun en typische afmetingspunten in a registreert [document ontwerp oplossing](/help/implement/prepare/solution-design.md).

## Hoofdlettergevoeligheid

Props zijn standaard niet hoofdlettergevoelig. Als u dezelfde waarde in verschillende gevallen verzendt (bijvoorbeeld `"DOG"` en `"Dog"`), groepeert Analysis Workspace deze in hetzelfde dimensie-item. Het geval van de eerste waarde aan het begin van de rapportagemaand wordt gebruikt. De Data Warehouse toont de eerste waarde die tijdens de verzoekperiode wordt ontmoet.

U kunt hoofdlettergevoelig maken. U kunt hoofdlettergevoeligheid ook uitschakelen voor elke aanwijzing nadat deze is ingeschakeld. Neem contact op met de klantenservice van Adobe met de id van de rapportsuite en de gewenste variabelen om hoofdlettergevoeligheid in/uit te schakelen.

>[!IMPORTANT]
>
>Als u de gevoeligheid van hoofdletters/kleine letters in-/uitschakelen, leidt dit tot onverwachte resultaten met segmenten en tot problemen met filters. Adobe beveelt ten zeerste aan deze instelling te schakelen tussen twee belangrijke tijdsperiodes, zoals het begin van een maand of jaar.

## Waarde van props over eVars

Adobe raadt in de meeste gevallen het gebruik van eVars aan. Uitzonderingen op deze verklaring zijn als volgt:

* U kunt profielen gebruiken in real-time rapporten. Het duurt ten minste 30 minuten om in de rapportage te verschijnen.
* Props kunnen lijsteigenschappen worden, die meerdere waarden in dezelfde hit accepteren. Lijstvariabelen zijn een afzonderlijke variabele en er zijn slechts drie lijstvariabelen beschikbaar.
* Wanneer u het plakken op een steun toelaat, [Invoer](entry-dimensions.md) en [Afsluiten](exit-dimensions.md) de afmetingen zijn onmiddellijk beschikbaar. Als u entry- en exit-afmetingen voor eVars wilt, kunt u handmatig een segment maken.

Zie [eVar](evar.md) voor meer vergelijkingen tussen props en eVars.
