---
title: Hoofdstukafmetingen van streamingmedia
description: Beschikbare afmetingen wanneer u [!UICONTROL Media Chapters] inschakelt voor een rapportsuite.
feature: Dimensions
exl-id: cac66a0b-3f83-46a9-b35c-ba08e0eafb92
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---

# Hoofdstukdimensies voor streaming-mediaservices

*Deze pagina beschrijft de beschikbare afmetingen wanneer u [!UICONTROL Media Chapters] voor een rapportreeks toelaat. Zie [ Streaming media de hoofdstukmetriek van de diensten ](../metrics/sm-chapters.md) voor beschikbare metriek.*

De het hoofdstukdimensies van de de media van het stromen de diensten verstrekken extra rapporteringsfunctionaliteit aan gegevensinzameling door de bibliotheken van de stromende media van de diensten. Voor het gebruik van deze afmetingen is de instructie **[!UICONTROL Adobe Analytics for Streaming Media Ad-on]** vereist. Neem contact op met uw Adobe-accountteam voor meer informatie.

Wanneer u **[!UICONTROL Media Chapters]** onder [ Media die ](/help/admin/tools/manage-rs/edit-settings/media-management.md) melden toelaat, is de volgende afmeting beschikbaar:

| Dimension-naam | Beschrijving | Verzonden met | Variabele van contextgegevens |
| --- | --- | --- | --- |
| Hoofdstuk | De automatisch gegenereerde hoofdstuk-id. | Hoofdstuk sluiten | `a.media.chapter.name` |

{style="table-layout:auto"}

Naast de bovenstaande afmetingen maakt Adobe automatisch de volgende classificatieafmetingen. U moet classificatiegegevens uploaden om rapporten te bekijken die deze afmetingen gebruiken.

| Classificatienaam | Bovenliggende dimensie | Beschrijving |
| --- | --- | --- |
| Maker | [ Inhoud ](sm-core.md) | De maker van de inhoud. |
| Lengte van hoofdstuk | Hoofdstuk | De lengte van het hoofdstuk, in seconden. |
| Hoofdstuknaam | Hoofdstuk | De vriendelijke naam van het hoofdstuk. |
| Verschuiving hoofdstuk | Hoofdstuk | De verschuiving van het hoofdstuk binnen de inhoud vanaf het begin, in seconden. |
| Hoofdstukpositie | Hoofdstuk | De indexpositie van het hoofdstuk in de inhoud. |

{style="table-layout:auto"}
