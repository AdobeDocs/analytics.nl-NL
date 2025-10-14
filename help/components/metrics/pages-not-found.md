---
title: Pagina's niet gevonden (cijfers)
description: Het aantal treffers dat een fout bevat.
feature: Metrics
exl-id: 71e138b5-69bb-41b0-852c-ca4af22be1f3
source-git-commit: a15d2b596c1e8b70e91efb49dd607fdbb0ceec3c
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---

# Pagina&#39;s niet gevonden

*Deze hulppagina beschrijft hoe de &quot;Pagina&#39;s niet gevonden&quot;werken metrisch. Zie de [&#x200B; Pagina&#39;s niet gevonden &#x200B;](../dimensions/pages-not-found.md) afmetingspagina voor meer informatie over hoe het als afmeting werkt.*

De &quot;Pagina&#39;s niet gevonden&quot;[&#x200B; metrische &#x200B;](overview.md) toont het aantal treffers waar een afmeting werd geplaatst of werd voortgeduurd op het tijdstip dat een bezoeker een fout ontmoette. Deze metrische waarde is handig wanneer u wilt zien welke pagina&#39;s of URL&#39;s foutberichten bevatten (zoals 404). U kunt deze informatie vervolgens doorgeven aan uw webontwikkelingsteam, dat de oorzaak van de fout kan vaststellen en deze kan verhelpen.

## Hoe deze metrische waarde wordt berekend

Deze metrische waarde telt alle treffers waar de [`pageType`](/help/implement/vars/page-vars/pagetype.md) variabele de waarde van `"errorPage"` evenaart. Het is het metrische equivalent van de [&#x200B; Pagina&#39;s niet gevonden &#x200B;](../dimensions/pages-not-found.md) dimensie.
