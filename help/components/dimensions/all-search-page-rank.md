---
title: Alle zoekpaginanummers
description: Bepaal welke pagina op een zoekmachine een bezoeker door aan uw site heeft geklikt.
feature: Dimensions
exl-id: 58ce54c3-cc45-4e84-a14d-5fec0b70f50f
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Alle zoekpaginanummers

De &#39;Alle rang van zoekpagina&#39; [dimensie](overview.md) biedt inzicht in de pagina met zoekresultaten die een bezoeker heeft doorgeklikt op uw site. Als uw site bijvoorbeeld op de tweede pagina van de zoekresultaten van een zoekmachine wordt weergegeven, is het item voor de dimensie van deze variabele &quot;Zoekpagina 2&quot;.

## Deze dimensie vullen met gegevens

Om deze dimensie te laten werken is het alleen nodig dat uw rapportenpakket [Interne URL-filters](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/internal-url-filter-admin.md) correct is ingesteld. AppMeasurement vult deze dimensie automatisch in zonder wijzigingen in de implementatiecode.

## Dimension-items

Als een bezoeker vanaf een zoekprogramma naar uw site klikt, is de waarde van deze dimensie &quot;Pagina zoeken&quot;, gevolgd door het paginanummer waarop de bezoeker heeft geklikt. Als een hit niet afkomstig is van een zoekmachine, is de waarde van deze dimensie &quot;Niet gespecificeerd&quot;.
