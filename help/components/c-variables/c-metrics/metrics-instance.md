---
description: Het aantal keren dat een waarde voor een variabele is ingesteld.
keywords: instances
title: Instanties
topic: Metrics
uuid: fec94bdd-a1dc-4cb0-8983-ea575b69589f
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Instanties

Het aantal keren dat een waarde voor een variabele is ingesteld.

Instanties worden voor alle raaktypen geteld, maar worden niet geteld wanneer een waarde wordt opgenomen voor een variabele op een volgende hit vanwege persistentie.

Als een gebruiker bijvoorbeeld via [!DNL example.com]uw site arriveert, bevat de eerste aanvraag voor een afbeelding op uw site de referentie van [!DNL example.com]. Wanneer deze waarde is ingesteld, wordt aan één instantie toegewezen, [!DNL example.com] ook al wordt deze referentie opgenomen voor alle pagina&#39;s die tijdens dat bezoek worden weergegeven.

De instanties voor omzettingsvariabelen in gegevenspakhuis werden toegevoegd medio-2011, toestaand de verzoeken van het gegevenspakhuis om een specifieke veranderlijke instantie van de omzettingsvariabele als metrisch te behandelen. Deze metriek is niet beschikbaar voor rapportering voorafgaand aan de tijd zij werden geïntroduceerd.
