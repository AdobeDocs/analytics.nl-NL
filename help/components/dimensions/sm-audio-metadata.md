---
title: Metagegevens voor streaming mediaservices
description: Beschikbare afmetingen wanneer u [!UICONTROL Audio Metadata] inschakelt voor een rapportsuite.
feature: Dimensions
exl-id: 2e4dc1e9-267b-47a2-b791-23d1e754a2c1
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Metagegevens voor streaming mediaservices

Streaming-mediaservices en -dimensies bieden extra rapportagefunctionaliteit voor gegevensverzameling via Streaming-mediaservices-bibliotheken. Voor het gebruik van deze afmetingen is de instructie **[!UICONTROL Adobe Analytics for Streaming Media Add-on]** vereist. Neem contact op met uw Adobe-accountteam voor meer informatie.

Wanneer u **[!UICONTROL Audio Metadata]** onder [ Media die ](/help/admin/tools/manage-rs/edit-settings/media-management.md) melden toelaat, zijn de volgende afmetingen beschikbaar:

| Dimension-naam | Beschrijving | Verzonden met | Variabele van contextgegevens | XDM-veld |
| --- | --- | --- | --- | --- |
| **[!UICONTROL Album]** | De naam van het album. | Media starten, Media sluiten | `a.media.album` | `xdm.mediaCollection.`<br>`sessionDetails.album`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.album` |
| **[!UICONTROL Artist]** | De naam van de artiest. | Media starten, Media sluiten | `a.media.artist` | `xdm.mediaCollection.`<br>`sessionDetails.artist`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.artist` |
| **[!UICONTROL Author]** | De naam van de auteur van het audioboek. | Media starten, Media sluiten | `a.media.author` | `xdm.mediaCollection.`<br>`sessionDetails.author`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.author` |
| **[!UICONTROL Label]** | De naam van het recordlabel. | Media starten, Media sluiten | `a.media.label` | `xdm.mediaCollection.`<br>`sessionDetails.label`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.label` |
| **[!UICONTROL Publisher]** | De naam van de uitgever van de audio-inhoud. | Media starten, Media sluiten | `a.media.publisher` | `xdm.mediaCollection.`<br>`sessionDetails.publisher`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.publisher` |
| **[!UICONTROL Station]** | De naam of id van het radiostation. | Media starten, Media sluiten | `a.media.station` | `xdm.mediaCollection.`<br>`sessionDetails.station`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.station` |
