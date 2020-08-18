---
title: Voorvallen
description: Het aantal treffers dat een variabele is ingesteld of geduurd.
translation-type: tm+mt
source-git-commit: b569f87dde3b9a8b323e0664d6c4d1578d410bb7
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---


# Voorvallen

De metrische waarde &#39;Voorkomt&#39; toont het aantal treffers waar een bepaalde dimensie is ingesteld of geduurd. Wanneer u een dimensie in Workspace naar een leeg canvas sleept, past Adobe deze metrische waarde automatisch toe op het project.

## Hoe deze metrische waarde wordt berekend

Van alle klare resultaten in een rapportreeks, omvat klappen waar een afmetingspunt wordt bepaald of voortgeduurd. Bepaalde afmetingen, zoals [eVars](../dimensions/evar.md), blijven bestaan na de hit waarop ze zijn ingesteld. Deze metrische tellingen zowel aanvankelijke als persistelde waarden.

## Vergelijken met vergelijkbare cijfers

* **Voorvallen vs.[instanties](instances.md)**: Komt tellingsklappen voor waar een afmetingspunt werd geplaatst of voortgeduurd. Exemplaren bevatten geen treffers op plaatsen waar een dimensie-item aanwezig blijft.
* **Voorvallen versus[paginaweergaven](page-views.md)**: Voorvallen omvatten alle raaktypen, waaronder oproepen voor het bijhouden van paginaweergaven ([`t()`](/help/implement/vars/functions/t-method.md)) en aanroepen voor het bijhouden van koppelingen ([`tl()`](/help/implement/vars/functions/tl-method.md)). De metrische paginaweergaven omvatten slechts de volgende vraag van de paginamening, en sluit verbinding het volgen vraag uit.
