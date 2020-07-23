---
title: Voorvallen
description: Het aantal treffers dat een variabele is ingesteld of geduurd.
translation-type: tm+mt
source-git-commit: 422e99d9ea70f0192443d7ebc3631c6bf99e7591
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---


# Voorvallen

De metrische waarde &#39;Voorkomt&#39; toont het aantal treffers waar een bepaalde dimensie is ingesteld of geduurd. Wanneer u een dimensie in Workspace naar een leeg canvas sleept, past Adobe deze metrische waarde automatisch toe op het project.

## Hoe deze metrische waarde wordt berekend

Van alle klare resultaten in een rapportreeks, omvat klappen waar een afmetingspunt wordt bepaald of voortgeduurd. Bepaalde afmetingen, zoals [eVars](../dimensions/evar.md), blijven bestaan na de hit waarop ze zijn ingesteld. Metriek zoals de [paginaweergaven](page-views.md) en [Voorvallen](occurrences.md) tellen zowel initiële als permanente waarden.

## Vergelijken met vergelijkbare cijfers

* **Voorvallen vs.[instanties](instances.md)**: Komt tellingsklappen voor waar een afmetingspunt werd geplaatst of voortgeduurd. Exemplaren bevatten geen treffers op plaatsen waar een dimensie-item aanwezig blijft.
* **Voorvallen versus[paginaweergaven](page-views.md)**: Voorvallen omvatten alle raaktypen, waaronder oproepen voor het bijhouden van paginaweergaven ([`t()`](/help/implement/vars/functions/t-method.md)) en aanroepen voor het bijhouden van koppelingen ([`tl()`](/help/implement/vars/functions/tl-method.md)). De metrische paginaweergaven omvatten slechts de volgende vraag van de paginamening, en sluit verbinding het volgen vraag uit.
