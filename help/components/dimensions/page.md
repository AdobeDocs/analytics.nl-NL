---
title: Pagina
description: De naam van de pagina.
feature: Dimensions
exl-id: 579963c8-8460-425f-b716-3b30d7a259af
source-git-commit: 72b38970e573b928e4dc4a8c8efdbfb753be0f4e
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---

# Pagina

De &quot;pagina&quot;[&#x200B; afmeting &#x200B;](overview.md) maakt een lijst van de namen van pagina&#39;s op uw plaats. Het is een van de meest gebruikte afmetingen in Adobe Analytics, omdat het inzicht biedt in welke pagina&#39;s op uw site het beste presteren.

Deze afmeting is verwant met de [&#x200B; sectie van de Plaats &#x200B;](site-section.md) en [&#x200B; de dimensies van de Server &#x200B;](server.md). De pagina is korrelig, de Server is het minst korrelig, en de sectie van de Plaats is tussen twee.

## Deze dimensie vullen met gegevens

Deze afmeting wint gegevens van het [`pageName` vraagkoord &#x200B;](/help/implement/validate/query-parameters.md) in [&#x200B; vraag van de de meningsmening van de Pagina terug (`t()`) &#x200B;](/help/implement/vars/functions/t-method.md). [&#x200B; het volgen van verbinding vraag (`tl()`) &#x200B;](/help/implement/vars/functions/tl-method.md) ontdoet altijd deze afmeting, zelfs als het `pageName` vraagkoord bestaat.

AppMeasurement verzamelt deze gegevens met behulp van de variabele [`pageName`](/help/implement/vars/page-vars/pagename.md) . Wanneer de variabele `pageName` niet is ingesteld, wordt deze dimensie teruggezet naar het gebruik van de variabele [`pageURL`](/help/implement/vars/page-vars/pageurl.md) .

## Dimension-items

Items van Dimensionen bevatten de namen van pagina&#39;s op uw site. Uw organisatie bepaalt welke specifieke afmetingspunten die u wilt gebruiken. Sommige organisaties gebruiken `document.title` rechtstreeks, terwijl andere een aangepaste breadcrumb maken. Wat methode u gebruikt, zorg ervoor het verenigbaar is en dat u het in het document van het a [&#x200B; oplossingsontwerp &#x200B;](/help/implement/prepare/solution-design.md) registreert.

>[!NOTE]
>
>Analysis Workspace gebruikt standaard de laatste toewijzing, met de optie om een willekeurig toewijzingsmodel te gebruiken.
