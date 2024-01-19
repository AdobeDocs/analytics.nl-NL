---
description: Het pakhuis van gegevens verstrekt een flexibele interface om douanerapporten in werking te stellen. Als u deze richtlijnen volgt, kunt u de tijd die nodig is om gegevens op te halen, verkorten.
keywords: tips en trucs;fout;timeout;problemen oplossen
title: Aanbevolen werkwijzen voor Data Warehouse
feature: Data Warehouse
uuid: d71c9138-22d9-4f92-885e-593f83f2bb59
exl-id: 7e21534b-a7ec-4231-89f1-0ad5013e70cf
source-git-commit: 93099d36a65ca2bf16fbd6342f01bfecdc8c798e
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# Aanbevolen werkwijzen voor Data Warehouse

Data Warehouse biedt een flexibele interface voor het uitvoeren van aangepaste rapporten. Gebruik de volgende richtlijnen om de tijd die nodig is om gegevens op te halen te verminderen:

| Richtsnoer | Beschrijving |
|--- |--- |
| Begrijp de hoeveelheid gegevens die u vraagt | Een meerjarenrapport over een grote rapportsuite kan tientallen miljarden gegevensrijen bevatten. Het verwerken en evalueren van deze gegevens kan dagen of zelfs weken in beslag nemen. Evalueer hoe het rapport wordt gebruikt om te bepalen als sommige gegevens over meerdere jaren beschikbaar zijn, of als u het rapport in veelvoudige verzoeken kunt breken. |
| Pas de rapportperiode aan de granulariteit aan | Het melden van granulariteit vereist extra verwerkingstijd. Als u maandelijks granulariteit voor een volledig jaar rapporteert, verwerkt uw rapporten veel sneller als u een rapportverzoek voor elke maand indient. |
| Rapport over voltooide gegevensbereiken | De rapporten van de Data Warehouse worden geproduceerd wanneer de gevraagde datumwaaier volledig is. Bijvoorbeeld, als u om een rapport voor de huidige week op Woensdag verzoekt, wordt het rapport niet geproduceerd tot Zondag van de volgende week. |
| Tekenrapporten genereren in Data Warehouse | Metrische waarden (items, uitgangen, grenzen, enz.) niet beschikbaar zijn in het gegevenspakhuis. |
| Virtuele rapportsuites | Data Warehouse die over virtuele rapportreeksen rapporteert steunt de alternatieve tijdzone die op de virtuele rapportreeks wordt gevormd. |

