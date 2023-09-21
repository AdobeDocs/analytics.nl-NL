---
title: Pagina
description: De naam van de pagina.
feature: Dimensions
exl-id: 579963c8-8460-425f-b716-3b30d7a259af
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Pagina

De &#39;pagina&#39; [dimensie](overview.md) geeft de namen van pagina&#39;s op uw site weer. Het is een van de meest gebruikte afmetingen in Adobe Analytics, omdat het inzicht biedt in welke pagina&#39;s op uw site het beste presteren.

Deze dimensie houdt verband met de [Sectie Site](site-section.md) en [Server](server.md) afmetingen. De pagina is korrelig, de Server is het minst korrelig, en de sectie van de Plaats is tussen twee.

## Deze dimensie vullen met gegevens

Deze dimensie haalt gegevens van terug [`pageName` querytekenreeks](/help/implement/validate/query-parameters.md) in [Aanroepen in de paginaweergave (`t()`)](/help/implement/vars/functions/t-method.md). [Aanroepen voor het bijhouden van koppelingen (`tl()`)](/help/implement/vars/functions/tl-method.md) verwijdert deze dimensie altijd, zelfs als de `pageName` queryreeks bestaat.

AppMeasurement verzamelt deze gegevens met de [`pageName`](/help/implement/vars/page-vars/pagename.md) variabele. Als de `pageName` variabele is niet gedefinieerd, maar wordt gebruikt voor de [`pageURL`](/help/implement/vars/page-vars/pageurl.md) variabele.

## Dimension-items

Items van Dimensionen bevatten de namen van pagina&#39;s op uw site. Uw organisatie bepaalt welke specifieke afmetingspunten u wilt gebruiken. Sommige organisaties gebruiken rechtstreeks `document.title`, terwijl anderen een aangepaste breadcrumb maken. Welke methode u ook gebruikt, zorg ervoor het verenigbaar is en dat u het in een registreert [document ontwerp oplossing](/help/implement/prepare/solution-design.md).

>[!NOTE]
>
>In Rapporten &amp; Analytics, gebruiken de omzettingsmetriek lineaire attributie voor deze afmeting. De inkomsten worden bijvoorbeeld gesplitst tussen alle pagina&#39;s die vóór een bezoek worden weergegeven `purchase` gebeurtenis. Analysis Workspace gebruikt standaard de laatste toewijzing, met de optie om een willekeurig toewijzingsmodel te gebruiken.
