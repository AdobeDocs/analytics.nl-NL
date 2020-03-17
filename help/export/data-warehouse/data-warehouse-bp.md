---
description: Het pakhuis van gegevens verstrekt een flexibele interface om douanerapporten in werking te stellen. Als u deze richtlijnen volgt, kunt u de tijd die nodig is om gegevens op te halen, verkorten.
keywords: best practices;failure;timeout;troubleshooting
title: Best practices voor Data Warehouse
topic: Data warehouse
uuid: d71c9138-22d9-4f92-885e-593f83f2bb59
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Best practices voor Data Warehouse

Het Pakhuis van gegevens verstrekt een flexibele interface om douanerapporten in werking te stellen. Als u deze richtlijnen volgt, kunt u de tijd die nodig is om gegevens op te halen, verkorten.



| Richtsnoer | Beschrijving |
|--- |--- |
| Paginaweergaven, bezoeken, bezoekers en andere standaardrapporten uitvoeren in Rapporten en Analytics | Alvorens een rapport van het Pakhuis van Gegevens te creëren, zie of is de informatie u zoekt reeds beschikbaar in rapporten. Als dat het geval is, zal het rapport veel sneller worden afgeleverd vanwege de voorbehandeling die wordt uitgevoerd door Rapporten &amp; Analytics voor algemene meetgegevens. |
| Begrijp de hoeveelheid gegevens die u vraagt | Een meerjarenrapport over een grote rapportsuite kan tientallen miljarden gegevensrijen bevatten. Het verwerken en evalueren van deze gegevens kan dagen of zelfs weken in beslag nemen. Evalueer hoe het rapport wordt gebruikt om te bepalen als sommige gegevens over meerdere jaren beschikbaar zijn, of als u het rapport in veelvoudige verzoeken kunt breken. |
| Pas de rapportperiode aan de granulariteit aan | Het melden van granulariteit vereist extra verwerkingstijd. Als u maandelijks granulariteit voor een volledig jaar rapporteert, verwerkt uw rapporten veel sneller als u een rapportverzoek voor elke maand indient. |
| Rapport over voltooide gegevensbereiken | De rapporten van het Pakhuis van gegevens worden geproduceerd wanneer de gevraagde datumwaaier volledig is. Bijvoorbeeld, als u om een rapport voor de huidige week op Woensdag verzoekt, wordt het rapport niet geproduceerd tot Zondag van de volgende week. |
| Tekenrapporten genereren in Data Warehouse | De metriek van de verf (ingangen, uitgang, grenzen, enz.) zijn niet beschikbaar in gegevenspakhuis. |
| Virtuele rapportsuites | De rapportering van het Pakhuis van gegevens over virtuele rapportreeksen steunt de alternatieve tijdzone die op de virtuele rapportreeks wordt gevormd. |
