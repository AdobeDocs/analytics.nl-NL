---
title: Algorithmic, toewijzing
description: Details over het algoritmische attributiemodel.
feature: Attribution
role: User, Admin
exl-id: dd2b2a5b-9c36-4534-999f-f96604f29eab
source-git-commit: d7a6867796f97f8a14cd8a3cfad115923b329c7c
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Algorithmic, toewijzing

Het de attributenmodel van het Algorithmic [ ](models.md) in Analysis Workspace verschilt van andere modellen in die zin dat het statistische technieken gebruikt om krediet over de afmetingspunten in uw rapport of vrije vormlijst toe te wijzen. Zoals alle andere attributiemodellen in Analysis Workspace, kan het op om het even welke afmeting of metrisch worden gebruikt en steunt onbeperkte segmentatie en onderverdelingen en verdeelt 100% van omzettingen aan de afmeting(en) in de lijst (ook genoemd geworden &quot;fractionele&quot;attributie).


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Algorithmic attributie ](https://video.tv.adobe.com/v/36205?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


Het algoritme dat wordt gebruikt voor attributie is gebaseerd op de Harsanyi Dividend van coöperatieve speltheorie. Het dividend van Harsanyi is een generalisering van de Shapley-waardeoplossing (genoemd naar Lloyd Shapley, een Nobelprijswinnaar) voor het verdelen van krediet onder spelers in een spel met ongelijke bijdragen aan de uitkomst.

Op hoog niveau wordt bij de berekening van de conversiekrediet voor elk aanraakpunt elk van de marketingaanraakpunten binnen een terugkijkvenster beschouwd als een coalitie van spelers waaraan een overschot op billijke wijze moet worden verdeeld. De overtollige verdeling van elke coalitie wordt bepaald volgens het overschot dat eerder door elke subcoalitie (of eerder deelnemende dimensie-items) recursief werd gecreeerd. Raadpleeg voor meer informatie de originele documenten van John Harsanyi en Lloyd Shapley:

* Shapley, Lloyd S.1953. Een waarde voor spelletjes van één persoon. *bijdragen aan de Theorie van Spelen, 2 (28)*, 307-317.
* Harsanyi, John C. (1963) Een vereenvoudigd onderhandelingsmodel voor het on-person coöperatieve spel. *Internationale Economische Controle 4 (2)*, 194-220.

>[!NOTE]
>
>Het resultaat van Algorithmic-toewijzing verschilt alleen van andere modellen wanneer er meerdere aanraakpunten bestaan binnen het opgegeven terugzoekvenster. Conversies met één aanraakpunt krijgen 100% krediet ongeacht het attributiemodel.
