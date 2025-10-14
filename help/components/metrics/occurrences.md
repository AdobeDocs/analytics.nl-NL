---
title: Voorvallen
description: Het aantal treffers dat een variabele is ingesteld of geduurd.
feature: Metrics
exl-id: 8428e813-0fb4-4620-884e-1aa92fe33209
source-git-commit: 0c5062363e10d9b545a3209ebaefcc6fa5d02c8b
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---

# Voorvallen

De metrische &quot;Voorvallen&quot; [&#128279;](overview.md) toont het aantal treffers waar een bepaalde afmeting werd geplaatst of voortgeduurd. Wanneer u een afmeting in Workspace naar een leeg canvas sleept, past de Adobe deze metrische waarde automatisch toe op het project.

## Hoe deze metrische waarde wordt berekend

Van alle klare resultaten in een rapportreeks, omvat klappen waar een afmetingspunt wordt bepaald of voortgeduurd. Sommige dimensies, zoals [&#x200B; eVars &#x200B;](../dimensions/evar.md), blijven voorbij de slag zij worden geplaatst. Deze metrische tellingen zowel aanvankelijke als persistelde waarden.

## Vergelijken met vergelijkbare cijfers

* **Voorkomen vs. [&#x200B; Instanties](instances.md)**: De tellingen van voorkomen raken waar een afmetingspunt werd geplaatst of voortgeduurd. Exemplaren bevatten geen treffers op plaatsen waar een dimensie-item aanwezig blijft.
* **Voorkomen vs. [&#x200B; de meningen van de Pagina](page-views.md)**: De voorvallen omvatten alle raaktypes, met inbegrip van pagina mening het volgen vraag ([`t()`](/help/implement/vars/functions/t-method.md)), verbinding het volgen vraag ([`tl()`](/help/implement/vars/functions/tl-method.md)), en gegevens van summiere [&#x200B; Gegevensbronnen &#x200B;](/help/import/data-sources/overview.md). Metrische paginaweergaven bevatten alleen aanroepen voor het bijhouden van paginaweergaven, exclusief aanroepen voor het bijhouden van koppelingen en samenvattingsgegevensbronnen.

## Persistentie

Persistentie is de capaciteit voor een bepaalde afmetingswaarde om op metrisch voorbij de gebeurtenis betrekking te hebben het wordt geplaatst. Er wordt een combinatie van toewijzing en vervaldatum gebruikt. Met Toewijzing kunt u bepalen welke waarde wordt behouden wanneer meerdere dimensies-items tegelijk in één kolom kunnen blijven staan. Met Vervaldatum kunt u bepalen hoe lang een dimensie-item zich na de gebeurtenis blijft bevinden waarop het is ingesteld.

Persistentie is alleen beschikbaar voor dimensies en is retroactief voor de gegevens waarop deze wordt toegepast. Het is een directe gegevenstransformatie die gebeurt alvorens het filtreren of andere analyseverrichtingen worden toegepast. Als persistentie niet is ingeschakeld, heeft de dimensie alleen betrekking op metriek die in dezelfde gebeurtenis bestaan.