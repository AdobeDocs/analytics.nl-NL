---
title: Pagina's niet gevonden
description: Het aantal treffers dat een fout bevat.
translation-type: tm+mt
source-git-commit: 54aeaa35fea8f725c87030936fa24f415064e333
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# Pagina&#39;s niet gevonden

*Deze Help-pagina beschrijft hoe &#39;Pagina&#39;s niet gevonden&#39; werkt als metrisch. Zie de[Pagina&#39;s niet gevonden](../dimensions/pages-not-found.md)dimensie voor meer informatie.*

De metrische waarde &#39;Pagina&#39;s niet gevonden&#39; geeft het aantal treffers aan waar de pagina een fout bevatte. Deze metrische waarde is nuttig wanneer u wilt zien welke pagina&#39;s of URL&#39;s foutberichten bevatten (zoals 404), zodat u de oorzaak van de fout kunt bepalen en deze kunt corrigeren.

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde telt alle klappen waar de [`pageType`](/help/implement/vars/page-vars/pagetype.md) variabele de waarde van `"errorPage"`evenaart. Het is het metrische equivalent van de niet gevonden [](../dimensions/pages-not-found.md) Pagina&#39;s dimensie.