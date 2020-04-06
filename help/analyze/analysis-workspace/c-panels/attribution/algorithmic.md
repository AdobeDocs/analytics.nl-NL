---
title: Algorithmic, toewijzing
description: Details over het algoritmische attributiemodel in Adobe Analytics.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Algorithmic, toewijzing

>[!NOTE] Algorithmic-toewijzing is momenteel alleen beschikbaar via [Adobe Analytics Labs](https://docs.adobe.com/content/help/en/analytics/analyze/tech-previews/overview.html). De functie zal uiteindelijk onderdeel zijn van een algemene release.

Het Algorithmic [attribution model](attribution.md) in Analysis Workspace verschilt van andere modellen in die zin dat het gebruik maakt van statistische technieken om krediet toe te wijzen over de waarden van de dimensies in uw rapport of vrije-vormtabel. Zoals alle andere attributiemodellen in de Werkruimte van de Analyse, kan het op om het even welke afmeting of metrisch worden gebruikt en steunt onbeperkte segmentatie en onderverdelingen en verdeelt 100% van omzettingen aan de afmeting(en) in de lijst (ook genoemd geworden &quot;fractionele&quot;attributie).

Het algoritme dat wordt gebruikt voor attributie is gebaseerd op de Harsanyi Dividend van coöperatieve speltheorie. Het dividend van Harsanyi is een generalisering van de Shapley-waardeoplossing (genoemd naar Lloyd Shapley, een Nobelprijswinnaar) voor het verdelen van krediet onder spelers in een spel met ongelijke bijdragen aan de uitkomst.

Op hoog niveau wordt bij de berekening van de conversiekrediet voor elk aanraakpunt elk van de marketingaanraakpunten binnen een terugkijkvenster beschouwd als een coalitie van spelers waaraan een overschot op billijke wijze moet worden verdeeld. De overtollige verdeling van elke coalitie wordt bepaald op basis van het overschot dat eerder door elke subcoalitie (of eerder participerende dimensiewaarden) recursief werd gecreëerd. Raadpleeg voor meer informatie de originele documenten van John Harsanyi en Lloyd Shapley:

* Shapley, Lloyd S. (1953). Een waarde voor spelletjes van één persoon. *Bijdragen aan de Theory of Games, 2(28)*, 307-317.
* Harsanyi, John C. (1963). Een vereenvoudigd onderhandelingsmodel voor het on-person coöperatieve spel. *International Economic Review 4(2)*, 194-220.

>[!NOTE] Het resultaat van Algorithmic-toewijzing verschilt alleen van andere modellen wanneer er meerdere aanraakpunten bestaan binnen het opgegeven terugzoekvenster. Conversies met één aanraakpunt krijgen 100% krediet ongeacht het attributiemodel.
