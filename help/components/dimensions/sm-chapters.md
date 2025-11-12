---
title: Hoofdstukafmetingen van streamingmedia
description: Beschikbare afmetingen wanneer u [!UICONTROL Media Chapters] inschakelt voor een rapportsuite.
feature: Dimensions
exl-id: cac66a0b-3f83-46a9-b35c-ba08e0eafb92
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 1%

---

# Hoofdstukdimensies voor streaming-mediaservices

*Deze pagina beschrijft de beschikbare afmetingen wanneer u [!UICONTROL Media Chapters] voor een rapportreeks toelaat. Zie [ Streaming media de hoofdstukmetriek van de diensten ](../metrics/sm-chapters.md) voor beschikbare metriek.*

De het hoofdstukdimensies van de de media van het stromen de diensten verstrekken extra rapporteringsfunctionaliteit aan gegevensinzameling door de bibliotheken van de stromende media van de diensten. Voor het gebruik van deze afmetingen is de instructie **[!UICONTROL Adobe Analytics for Streaming Media Add-on]** vereist. Neem contact op met uw Adobe-accountteam voor meer informatie.

Wanneer u **[!UICONTROL Media Chapters]** onder [ Media die ](/help/admin/tools/manage-rs/edit-settings/media-management.md) melden toelaat, is de volgende afmeting beschikbaar:

| Dimension-naam | Beschrijving | Verzonden met | Variabele van contextgegevens | XDM-veld |
| --- | --- | --- | --- | --- |
| **[!UICONTROL Chapter]** | De automatisch gegenereerde hoofdstuk-id. | Hoofdstuk sluiten | `a.media.chapter.name` | `xdm.mediaReporting.`<br>`chapterDetails.ID` |

Naast de bovenstaande afmetingen maakt Adobe automatisch de volgende classificatieafmetingen. U moet classificatiegegevens uploaden om rapporten te bekijken die deze afmetingen gebruiken.

| Classificatienaam | Bovenliggende dimensie | Beschrijving |
| --- | --- | --- |
| **[!UICONTROL Originator]** | [[!UICONTROL Content]](sm-core.md) | De maker van de inhoud. |
| **[!UICONTROL Chapter length]** | [!UICONTROL Chapter] | De lengte van het hoofdstuk, in seconden. |
| **[!UICONTROL Chapter name]** | [!UICONTROL Chapter] | De vriendelijke naam van het hoofdstuk. |
| **[!UICONTROL Chapter offset]** | [!UICONTROL Chapter] | De verschuiving van het hoofdstuk binnen de inhoud vanaf het begin, in seconden. |
| **[!UICONTROL Chapter position]** | [!UICONTROL Chapter] | De indexpositie van het hoofdstuk in de inhoud. |
