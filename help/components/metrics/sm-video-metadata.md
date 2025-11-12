---
title: Metrische gegevens voor videometagegevens voor streaming mediaservices
description: De beschikbare metriek wanneer u [!UICONTROL Video Metadata] voor een rapportreeks toelaat.
feature: Metrics
exl-id: b2f60a34-e139-4498-bf71-74d291759ef2
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# Metrische gegevens voor videometagegevens voor streaming mediaservices

*Deze pagina beschrijft de beschikbare metriek wanneer u [!UICONTROL Video metadata] voor een rapportreeks toelaat. Zie [ Streaming media diensten videometadimensies ](../dimensions/sm-video-metadata.md) voor beschikbare afmetingen.*

Metrische gegevens over videometagegevens voor streaming mediaservices bieden aanvullende rapportagefunctionaliteit voor gegevensverzameling via bibliotheken met streaming-mediaservices. Voor het gebruik van deze metriek is **[!UICONTROL Adobe Analytics for Streaming Media Add-on]** vereist. Neem contact op met uw Adobe-accountteam voor meer informatie.

Wanneer u **[!UICONTROL Video Metadata]** onder [ Media die ](/help/admin/tools/manage-rs/edit-settings/media-management.md) melden toelaat, is volgende metrisch beschikbaar:

| Metrische naam | Beschrijving | Verzonden met | Variabele van contextgegevens | XDM-veld |
| --- | --- | --- | --- | --- |
| **[!UICONTROL Authorized]** | Een Booleaanse waarde die wordt geactiveerd wanneer de gebruiker via Adobe-verificatie is geautoriseerd. | Media starten, Media sluiten | `a.media.pass.auth` | `xdm.mediaCollection.`<br>`sessionDetails.authorized`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.authorized` |
