---
title: Algoritmische attributie
description: Details over het algoritmische attributiemodel.
translation-type: tm+mt
source-git-commit: d12ea12ffbf54e1af091ceff6ec671e6a09d0db3
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 1%

---


# Algoritmische attributie

>[!NOTE] **[!UICONTROL Algorithmic attribution]** wordt momenteel beperkt getest. Zie de [Adobe Analytics-functiereleases](/help/landing/an-releases.md) voor meer informatie.

Het Algorithmic [attribution model](models.md) in Analysis Workspace verschilt van andere modellen in die zin dat het gebruik maakt van statistische technieken om krediet toe te wijzen over de waarden van de dimensies in uw rapport of vrije-vormtabel. Zoals alle andere attributiemodellen in de Werkruimte van de Analyse, kan het op om het even welke afmeting of metrisch worden gebruikt en steunt onbeperkte segmentatie en onderverdelingen en verdeelt 100% van omzettingen aan de afmeting(en) in de lijst (ook genoemd geworden &quot;fractionele&quot;attributie).

Het algoritme dat wordt gebruikt voor attributie is gebaseerd op de Harsanyi Dividend van coöperatieve speltheorie. Het dividend van Harsanyi is een generalisering van de Shapley-waardeoplossing (genoemd naar Lloyd Shapley, een Nobelprijswinnaar) voor het verdelen van krediet onder spelers in een spel met ongelijke bijdragen aan de uitkomst.

Op hoog niveau wordt bij de berekening van de conversiekrediet voor elk aanraakpunt elk van de marketingaanraakpunten binnen een terugkijkvenster beschouwd als een coalitie van spelers waaraan een overschot op billijke wijze moet worden verdeeld. De overtollige verdeling van elke coalitie wordt bepaald op basis van het overschot dat eerder door elke subcoalitie (of eerder participerende dimensiewaarden) recursief werd gecreëerd. Raadpleeg voor meer informatie de originele documenten van John Harsanyi en Lloyd Shapley:

* Shapley, Lloyd S. (1953). Een waarde voor spelletjes van één persoon. *Bijdragen aan de Theory of Games, 2(28)*, 307-317.
* Harsanyi, John C. (1963). Een vereenvoudigd onderhandelingsmodel voor het on-person coöperatieve spel. *International Economic Review 4(2)*, 194-220.

>[!NOTE] Het resultaat van Algorithmic-toewijzing verschilt alleen van andere modellen wanneer er meerdere aanraakpunten bestaan binnen het opgegeven terugzoekvenster. Conversies met één aanraakpunt krijgen 100% krediet ongeacht het attributiemodel.
