---
title: Voorvallen
description: Het aantal treffers dat een variabele is ingesteld of geduurd.
feature: Metrics
exl-id: 8428e813-0fb4-4620-884e-1aa92fe33209
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 1%

---

# Voorvallen

De &#39;voorvallen&#39; [metrisch](overview.md) toont het aantal treffers waar een bepaalde afmeting werd geplaatst of voortgeduurd. Wanneer u een afmeting in Workspace naar een leeg canvas sleept, past de Adobe deze metrische waarde automatisch toe op het project.

## Hoe deze metrische waarde wordt berekend

Van alle klare resultaten in een rapportreeks, omvat klappen waar een afmetingspunt wordt bepaald of voortgeduurd. Sommige afmetingen, zoals [eVars](../dimensions/evar.md)blijven staan na de hit waarop ze zijn ingesteld. Deze metrische tellingen zowel aanvankelijke als persistelde waarden.

## Vergelijken met vergelijkbare cijfers

* **Voorvallen vs. [Instanties](instances.md)**: Komt tellingen klappen voor waar een afmetingspunt werd geplaatst of voortgeduurd. Exemplaren bevatten geen treffers op plaatsen waar een dimensie-item aanwezig blijft.
* **Voorvallen vs. [Paginaweergaven](page-views.md)**: De instanties omvatten alle raaktypen, inclusief aanroepen voor het bijhouden van paginaweergaven ([`t()`](/help/implement/vars/functions/t-method.md)), verbinding het volgen vraag ([`tl()`](/help/implement/vars/functions/tl-method.md)) en gegevens uit samenvatting [Gegevensbronnen](/help/import/data-sources/overview.md). Metrische paginaweergaven bevatten alleen aanroepen voor het bijhouden van paginaweergaven, exclusief aanroepen voor het bijhouden van koppelingen en samenvattingsgegevensbronnen.
