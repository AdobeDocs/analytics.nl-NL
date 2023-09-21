---
title: Bot-naam
description: De naam van beide die aan de regels van de Bot voldeed.
exl-id: 668c1dce-c603-477a-9df7-dacb649bbf63
feature: Dimensions
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---

# Bot-naam

De naam van de &#39;Bot&#39; [dimensie](overview.md) toont de namen van de bots die zijn gedetecteerd met [Bot-regels](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md). Deze regels kunnen standaardIAB regels, of de regels van de douanebot zijn die uw organisatie vormt. Het is handig als u meer wilt weten over welke bots uw site bezoeken of welke bots het meeste verkeer genereren.

Komt overeen met [!UICONTROL Bot rules] automatisch uit alle analytische rapportage worden gefilterd, met uitzondering van deze dimensie; [Beide voorvallen](../metrics/bot-occurrences.md), en [Boven pagina weergeven](../metrics/bot-page-views.md). U kunt deze dimensie en deze twee meeteenheden gebruiken om te zien welke beide gegevens van de rest van uw rapporten worden uitgesloten.

Aangezien beide rapportages van de rest van uw gegevens van de rapportreeks worden gescheiden, slechts worden de volgende dimensies en metriek gesteund met deze dimensie:

* [Pagina](page.md)
* Op tijd gebaseerde afmetingen (bijvoorbeeld [Dag](day.md), [Week](week.md), of [Maand](month.md))
* [Beide voorvallen](../metrics/bot-occurrences.md)
* [Boven pagina weergeven](../metrics/bot-page-views.md)

Het gebruiken van een andere afmeting of metrisch met deze afmeting keert geen gegevens terug.

## Deze dimensie vullen met gegevens

Als u [Bot-regels](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md)Deze dimensie verzamelt automatisch gegevens. Als u dit nog niet hebt gedaan [!UICONTROL Bot rules], komt deze dimensie niet voor in Analysis Workspace.

## Dimension-items

Elk dimensie-item bevat de naam van de beide elementen die overeenkomen met IAB- of aangepaste beide regelcriteria.
