---
title: Data analyseren die door gebeurtenissen worden beïnvloed
description: Begrijp hoe de gegevens die door een gebeurtenis worden beïnvloed tot algemene gegevenskwaliteit bijdragen.
exl-id: 8d81a432-42d6-4f5d-b66a-bb3af7fc4857
feature: Event
source-git-commit: 811e321ce96aaefaeff691ed5969981a048d2c31
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 2%

---

# Data analyseren die door gebeurtenissen worden beïnvloed

Soms kan een gebeurtenis de gegevenskwaliteit in uw organisatie beïnvloeden. Voorbeelden zijn:

* Een bot die uitstraalgegevens verzendt, zoals miljoenen dollars aan inkomsten
* Uw organisatie heeft een update naar uw website uitgevoerd die een negatief effect heeft op uw analytische implementatie
* Andere kwesties die de gegevenskwaliteit of volledigheid beïnvloeden

Als uw site een probleem met de gegevenskwaliteit heeft ondervonden, kunt u het beter uitsluiten van rapportage om te voorkomen dat er zakelijke beslissingen over worden genomen. Gebruik deze secties om het effect van de gebeurtenis op uw gegevens te meten, en te bepalen hoe u wilt te werk gaan.

## De oorzaak van een gebeurtenis bepalen

Als u niet zeker weet waarom u een piek of daling in gegevens ziet, zie [Problemen met spikes/druppels in gegevens oplossen](spikes-drops.md).

## Gegevens analyseren en uitsluiten met behulp van segmentatie

Adobe Analytics biedt een eenvoudige en robuuste manier om zich op gegevens te concentreren of uit te sluiten gebruikend segmentatie. U kunt de dimensies van het datumbereik binnen segmenten gebruiken om uit te filteren of op die specifieke datums te concentreren. Zie [Specifieke data in de analyse uitsluiten](segments.md).

## Een gebeurtenis vergelijken met vorige datumbereiken

Als u meer wilt weten over de invloed die een gebeurtenis op uw gegevens heeft gehad, kunt u datumvergelijking gebruiken in Analysis Workspace. Met deze functie kunt u gegevens dag voor dag, week voor week of maand vergelijken om te zien hoe deze zich verhoudt tot vorige bereiken. Vervolgens kunt u met deze vergelijking bepalen in hoeverre een gebeurtenis trends beïnvloedt. Zie [Datums vergelijken die door een gebeurtenis worden beïnvloed met vorige bereiken](compare-dates.md).

## Gegevens op basis van berekende meetwaarden

Nadat u segmenten hebt gemaakt en datumvergelijking hebt gebruikt, kunt u beide concepten combineren om trendgegevens te corrigeren aan de hand van berekende meetwaarden. Neem de segmenten op in een berekende metrische waarde en vermenigvuldig de betrokken dagen met de verschuiving die wordt gevonden bij het vergelijken van datums. Zie [Afleiden van gegevens die door gebeurtenissen worden beïnvloed](calcmetrics.md).

## Communiceer gevolgen aan gebruikers in uw organisatie

Als u klaar bent met de manier waarop u een gebeurtenis wilt afhandelen, kunt u [communiceren met gebruikers in uw organisatie](communicate.md). Adobe biedt verschillende locaties in Analytics waar u tekst kunt plaatsen om met gebruikers te communiceren wat er is gebeurd en welke componenten zij kunnen gebruiken.

## Video

Deze video doorloopt elk van de bovenstaande stappen.

>[!VIDEO](https://video.tv.adobe.com/v/33316?quality=12)

* **0:27**: Gegevens uitsluiten met behulp van segmentatie
* **02:55**: Een gebeurtenis vergelijken met vorige bereiken
* **8:42**: Gegevens op basis van berekende meetwaarden
* **11:46**: Communiceren met gevolgen voor gebruikers
