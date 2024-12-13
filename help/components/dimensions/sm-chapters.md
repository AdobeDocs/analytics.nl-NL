---
title: Hoofdstukafmetingen van streamingmedia
description: Beschikbare afmetingen wanneer u [!UICONTROL Media Chapters] inschakelt voor een rapportsuite.
feature: Dimensions
exl-id: cac66a0b-3f83-46a9-b35c-ba08e0eafb92
source-git-commit: fdd66c9558f070cd760f37a39e5911f0dac22612
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 1%

---

# Hoofdstukafmetingen van streamingmedia

*Deze pagina beschrijft de beschikbare afmetingen wanneer u [!UICONTROL Media Chapters] voor een rapportreeks toelaat. Zie [ het stromen het hoofdstukmetriek van Media ](../metrics/sm-chapters.md) voor beschikbare metriek.*

De het hoofdstukdimensies van Media van het stromen verstrekken extra rapporteringsfunctionaliteit aan gegevensinzameling door de bibliotheken van de de inzamelingsmedia van het stromen. Voor het gebruik van deze afmetingen is de instructie **[!UICONTROL Adobe Streaming Media Collection]** vereist. Neem contact op met het accountteam van de Adobe voor meer informatie.

Wanneer u **[!UICONTROL Media Chapters]** onder [ Media die ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) melden toelaat, is de volgende afmeting beschikbaar:

| Naam Dimension | Beschrijving | Verzonden met | Variabele van contextgegevens |
| --- | --- | --- | --- |
| Hoofdstuk | De automatisch gegenereerde hoofdstuk-id. | Hoofdstuk sluiten | `a.media.chapter.name` |

{style="table-layout:auto"}

Naast de bovenstaande afmetingen worden met Adobe automatisch de volgende indelingsafmetingen gemaakt. U moet classificatiegegevens uploaden om rapporten te bekijken die deze afmetingen gebruiken.

| Classificatienaam | Bovenliggende dimensie | Beschrijving |
| --- | --- | --- |
| Maker | [ Inhoud ](sm-core.md) | De maker van de inhoud. |
| Lengte van hoofdstuk | Hoofdstuk | De lengte van het hoofdstuk, in seconden. |
| Hoofdstuknaam | Hoofdstuk | De vriendelijke naam van het hoofdstuk. |
| Verschuiving hoofdstuk | Hoofdstuk | De verschuiving van het hoofdstuk binnen de inhoud vanaf het begin, in seconden. |
| Hoofdstukpositie | Hoofdstuk | De indexpositie van het hoofdstuk in de inhoud. |

{style="table-layout:auto"}
