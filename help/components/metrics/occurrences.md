---
title: Voorvallen
description: Het aantal treffers dat een variabele is ingesteld of geduurd.
feature: Metrics
exl-id: 8428e813-0fb4-4620-884e-1aa92fe33209
source-git-commit: 7d5383e1ee3bee189d3dd48bc6b899f4108f7ba8
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---

# Voorvallen

De metrische waarde &#39;Voorkomt&#39; toont het aantal treffers waar een bepaalde dimensie is ingesteld of geduurd. Wanneer u een dimensie in Workspace naar een leeg canvas sleept, past Adobe deze metrische waarde automatisch toe op het project.

## Hoe deze metrische waarde wordt berekend

Van alle klare resultaten in een rapportreeks, omvat klappen waar een afmetingspunt wordt bepaald of voortgeduurd. Sommige afmetingen, zoals [eVars](../dimensions/evar.md)blijven staan na de hit waarop ze zijn ingesteld. Deze metrische tellingen zowel aanvankelijke als persistelde waarden.

## Vergelijken met vergelijkbare cijfers

* **Voorvallen vs. [Instanties](instances.md)**: Komt tellingsklappen voor waar een afmetingspunt werd geplaatst of voortgeduurd. Exemplaren bevatten geen treffers op plaatsen waar een dimensie-item aanwezig blijft.
* **Voorvallen vs. [Paginaweergaven](page-views.md)**: Voorvallen omvatten alle raaktypen, inclusief aanroepen voor het bijhouden van paginaweergaven ([`t()`](/help/implement/vars/functions/t-method.md)) en koppelings volgende vraag ([`tl()`](/help/implement/vars/functions/tl-method.md)). De metrische paginamening omvat slechts de volgende vraag van de paginamening, en sluit verbinding het volgen vraag uit.
