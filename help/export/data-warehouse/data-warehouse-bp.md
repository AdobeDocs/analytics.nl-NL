---
description: Leer de richtlijnen die helpen de tijd verminderen het duurt om gegevens van Data Warehouse terug te winnen.
keywords: tips en trucs;fout;timeout;problemen oplossen
title: Aanbevolen werkwijzen voor Data Warehouse
feature: Data Warehouse
uuid: d71c9138-22d9-4f92-885e-593f83f2bb59
exl-id: 7e21534b-a7ec-4231-89f1-0ad5013e70cf
source-git-commit: d929e97a9d9623a8255f16729177d812d59cec05
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# Aanbevolen werkwijzen voor Data Warehouse

Data Warehouse biedt een flexibele interface voor het uitvoeren van aangepaste rapporten. Gebruik de volgende richtlijnen om de tijd die nodig is om gegevens op te halen te verminderen:

| Richtsnoer | Beschrijving |
|--- |--- |
| Begrijp de hoeveelheid gegevens die u vraagt | Een meerjarenrapport over een grote rapportsuite kan tientallen miljarden gegevensrijen bevatten. Het verwerken en evalueren van deze gegevens kan dagen of zelfs weken in beslag nemen. Evalueer hoe het rapport wordt gebruikt om te bepalen als sommige gegevens over meerdere jaren beschikbaar zijn, of als u het rapport in veelvoudige verzoeken kunt breken. |
| Pas de rapportperiode aan de granulariteit aan | Het melden van granulariteit vereist extra verwerkingstijd. Als u maandelijks granulariteit voor een volledig jaar rapporteert, verwerkt uw rapporten veel sneller als u een rapportverzoek voor elke maand indient. |
| Rapport over voltooide gegevensbereiken | De rapporten van de Data Warehouse worden geproduceerd wanneer de gevraagde datumwaaier volledig is. Bijvoorbeeld, als u om een rapport voor de huidige week op Woensdag verzoekt, wordt het rapport niet geproduceerd tot Zondag van de volgende week. |
| Tekenrapporten genereren in Data Warehouse | De metriek van de verf (ingangen, uitgang, grenzen, enz.) zijn niet beschikbaar in gegevenspakhuis. |
| Virtuele rapportsuites | Data Warehouse die over virtuele rapportreeksen rapporteert steunt de alternatieve tijdzone die op de virtuele rapportreeks wordt gevormd. |

