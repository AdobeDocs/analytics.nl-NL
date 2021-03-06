---
title: Data analyseren die door gebeurtenissen worden beïnvloed
description: Begrijp hoe de gegevens die door een gebeurtenis worden beïnvloed tot algemene gegevenskwaliteit bijdragen.
translation-type: tm+mt
source-git-commit: 178e372e63c436268a1f7028d986504983430b2f
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 2%

---


# Data analyseren die door gebeurtenissen worden beïnvloed

Soms kan een gebeurtenis de gegevenskwaliteit in uw organisatie beïnvloeden. Voorbeelden zijn:

* Een bot die uitstraalgegevens verzendt, zoals miljoenen dollars aan inkomsten
* Uw organisatie heeft een update naar uw website uitgevoerd die een negatief effect heeft op uw Analytics-implementatie
* Andere kwesties die de gegevenskwaliteit of volledigheid beïnvloeden

Als uw site een probleem met de gegevenskwaliteit heeft ondervonden, kunt u het beter uitsluiten van rapportage om te voorkomen dat er zakelijke beslissingen over worden genomen. Gebruik deze secties om het effect van de gebeurtenis op uw gegevens te meten, en te bepalen hoe u wilt te werk gaan.

## De oorzaak van een gebeurtenis bepalen

Als u niet zeker weet waarom u een piek of daling in gegevens ziet, zie [Problemen met spikes/dalingen in gegevens](spikes-drops.md)oplossen.

## Gegevens analyseren en uitsluiten met behulp van segmentatie

Adobe Analytics biedt een eenvoudige en robuuste manier om zich op gegevens te concentreren of uit te sluiten gebruikend segmentatie. U kunt de dimensies van het datumbereik binnen segmenten gebruiken om uit te filteren of op die specifieke datums te concentreren. See [Exclude specific dates in analysis](segments.md).

## Een gebeurtenis vergelijken met vorige datumbereiken

Als u meer wilt weten over de invloed die een gebeurtenis op uw gegevens heeft gehad, kunt u datumvergelijking gebruiken in Analysis Workspace. Met deze functie kunt u gegevens dag voor dag, week voor week of maand vergelijken om te zien hoe deze zich verhoudt tot vorige bereiken. Vervolgens kunt u met deze vergelijking bepalen in hoeverre een gebeurtenis trends beïnvloedt. Zie Datums [vergelijken die door een gebeurtenis aan vorige waaiers](compare-dates.md)worden beïnvloed.

## Gegevens op basis van berekende meetwaarden

Nadat u segmenten hebt gemaakt en datumvergelijking hebt gebruikt, kunt u beide concepten combineren om trendgegevens te corrigeren aan de hand van berekende meetwaarden. Neem de segmenten op in een berekende metrische waarde en vermenigvuldig de betrokken dagen met de verschuiving die wordt gevonden bij het vergelijken van datums. See [Derive data impacted by events](calcmetrics.md).

## Communiceer gevolgen aan gebruikers in uw organisatie

Zodra u bent voorbereid met hoe u van plan bent om een gebeurtenis te behandelen, kunt u aan gebruikers in uw organisatie [](communicate.md)communiceren. Adobe biedt verschillende plaatsen in Analytics aan waar u tekst kunt plaatsen om met gebruikers te communiceren wat er is gebeurd en welke componenten zij kunnen gebruiken.

## Video

Deze video doorloopt elk van de bovenstaande stappen.

>[!VIDEO](https://video.tv.adobe.com/v/33316?quality=12)

* **0:27**: Gegevens uitsluiten met behulp van segmentatie
* **2:55**: Een gebeurtenis vergelijken met vorige bereiken
* **8:42**: Gegevens op basis van berekende meetwaarden
* **11:46**: Communiceren met gevolgen voor gebruikers
