---
title: Problemen met gegevensaanwezigheid oplossen
description: Leer welke stappen u kunt nemen wanneer u geen gegevens in rapporten ziet.
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 0%

---


# Problemen met gegevensaanwezigheid oplossen

In Analysis Workspace retourneren sommige projectinstellingen nul rijen. In Rapporten &amp; Analytics, terugkeert het bekijken van bepaalde rapporten het volgende bericht:

**&quot;Er zijn geen gegevens voor de geselecteerde criteria.&quot;**

Gebruik de volgende stappen om te bepalen waarom een rapport geen gegevens toont.

## Gegevens bestaan maar worden uitgefilterd

Uw rapportsuite bevat gegevens, maar de specifieke componenten die in het rapport worden gebruikt, filteren alle gegevens.

* **Segmenten**: De segmenten kunnen gemakkelijk verhinderen alle gegevens in een rapport verschijnen. Controleer alle segmentdefinities en verwijder alle segmenten om te zien of een segment uw gegevens veroorzaakt om niet te verschijnen.
* **Metrisch**: Controleer of de juiste meetgegevens worden gebruikt. Verander metrisch in [Voorkomen](/help/components/metrics/occurrences.md) om ervoor te zorgen dat metrisch niet de medewerker aan een rapport zonder gegevens is.
* **Datumbereiken**: Datumbereiken in het verleden of op enig moment in de toekomst leveren geen gegevens op. Het [beleid voor gegevensbewaring](data-retention.md) van uw organisatie bepaalt hoe ver de achtergegevens worden bewaard.
* **Filters**: Verwijder alle zoekfilters uit het rapport.

## Gegevens bestaan niet

Als er geen segmenten zijn, metrisch is Voorkomen, is de datumwaaier de huidige maand, en er zijn geen onderzoeksfilters, controleer het volgende:

* **Verifieer de rapportsuite**: Zorg ervoor dat u in een rapportreeks bent die gegevens bevat. Vele organisaties hebben nieuwe, test, of de reeksen van het ontwikkelingsrapport die typisch niet veel gegevens bevatten.
* **Latentie**: Als u recente gegevens weergeeft, kunnen deze gegevens worden vertraagd. Zie [Latentie](latency.md) voor meer informatie.
* **Gegevensverzameling** valideren: Navigeer aan het Webbezit dat uw rapportreeks wordt verondersteld te volgen, en open debugger [ van ](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html)Adobe. Zorg ervoor dat er een verzoek voor een analyseafbeelding aanwezig is wanneer u een pagina laadt. Als u een beeldverzoek ziet, zorg ervoor dat het de correcte rapportreeks identiteitskaart gebruikt, dat het geldige [currencyCode](/help/implement/vars/config-vars/currencycode.md) omvat, en dat [timestamp steun](/help/implement/vars/page-vars/timestamp.md) tussen de beeldverzoek en rapportreeks aanpast.
