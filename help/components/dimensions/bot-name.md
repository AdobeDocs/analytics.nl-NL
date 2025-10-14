---
title: Bot-naam
description: De naam van beide die aan de regels van de Bot voldeed.
exl-id: 034dce46-e83c-4053-a062-3998231f8d6b
feature: Dimensions
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---

# Bot-naam

De &quot;Bot naam&quot;[&#x200B; dimensie &#x200B;](overview.md) toont de namen van bots die gebruikend [&#x200B; Bot regels &#x200B;](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/bot-rules.md) werden ontdekt. Deze regels kunnen standaardIAB regels, of de regels van de douanebot zijn die uw organisatie vormt. Het is handig als u meer wilt weten over welke bots uw site bezoeken of welke bots het meeste verkeer genereren.

Hits die [!UICONTROL Bot rules] aanpassen wordt automatisch gefilterd uit alle Analytics die met uitzondering op deze afmeting, [&#x200B; verschijnen Bot &#x200B;](../metrics/bot-occurrences.md), en [&#x200B; Bot paginameningen &#x200B;](../metrics/bot-page-views.md) melden. U kunt deze dimensie en deze twee meeteenheden gebruiken om te zien welke beide gegevens van de rest van uw rapporten worden uitgesloten.

Aangezien beide rapportages van de rest van uw gegevens van de rapportreeks worden gescheiden, slechts worden de volgende dimensies en metriek gesteund met deze dimensie:

* [Pagina](page.md)
* Op tijd-gebaseerde afmetingen (bijvoorbeeld, [&#x200B; Dag &#x200B;](day.md), [&#x200B; Week &#x200B;](week.md), of [&#x200B; Maand &#x200B;](month.md))
* [Beide voorvallen](../metrics/bot-occurrences.md)
* [Boven pagina weergeven](../metrics/bot-page-views.md)

Het gebruiken van een andere afmeting of metrisch met deze afmeting keert geen gegevens terug.

## Deze dimensie vullen met gegevens

Als u [&#x200B; Bot regels &#x200B;](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/bot-rules.md) hebt toegelaten, verzamelt deze dimensie automatisch gegevens. Als u [!UICONTROL Bot rules] nog niet hebt ingeschakeld, wordt deze dimensie niet weergegeven in Analysis Workspace.

## Dimension-objecten

Elk dimensie-item bevat de naam van de beide elementen die overeenkomen met IAB- of aangepaste beide regelcriteria.
