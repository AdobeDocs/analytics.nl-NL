---
description: Gegevens die worden verzameld op websites, mobiele apps of die worden geüpload met behulp van webservice-API's of gegevensbronnen, worden verwerkt en opgeslagen in Adobe Data Warehouse. Deze onbewerkte klikstreamgegevens vormen de gegevensset die door Adobe Analytics wordt gebruikt.
keywords: clickStream;data feed;datafeed;Data Feed
title: Overzicht van gegevensinvoer voor analyse
feature: Data Feeds
exl-id: 2cfff9ad-cdb5-4ae9-a266-4f3d3d046f0c
source-git-commit: 84bdeb5d502e46c922fc5123fcdd5b6819426c0e
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# Overzicht van gegevensinvoer voor analyse

Gegevensfeeds zijn een krachtige manier om onbewerkte gegevens uit Adobe Analytics te halen. Deze onbewerkte gegevens kunnen worden gebruikt op andere platformen buiten de Adobe om naar eigen goeddunken van uw organisatie te worden gebruikt. De gegevens worden aan het einde van elk uur in partijen per uur of aan het einde van elke dag in partijen per uur verstrekt.

## Vereisten

Zorg ervoor dat u aan alle volgende vereisten voldoet voordat u gegevensfeeds gebruikt.

* Een werkende implementatie die gegevens naar de servers van de Adobe- gegevensinzameling verzendt. Zie [Een implementatie valideren en publiceren](/help/implement/launch/validate-publish-prod.md) in de handleiding voor de implementatie.
* Uw account is een productbeheerder voor Analytics of uw account behoort tot een productprofiel met toegang tot gegevensfeeds.
* Een emmertje geconfigureerd op Amazon S3, Google Cloud Platform, Azure RBAC of Azure SAS.
* (Verouderd: Alleen vereist voor verouderde FTP- en SFTP-doeltypen) Heb een FTP-site en aanmeldingsgegevens (FTP-gegevens verstrekt door uw organisatie).

## Volgende stappen

Met de volgende bronnen krijgt u inzicht in de basisworkflow voor het verkrijgen van gegevensfeeds. Nadat u de basisworkflow hebt begrepen, kunt u met teams binnen uw organisatie werken om onbewerkte gegevens in een database op te slaan of in te voeren.

* [Aanbevolen werkwijzen voor gegevensinvoer](/help/export/analytics-data-feed/data-feeds-best-practices.md): Aanbevolen procedures voor het maken en beheren van gegevensfeeds.
* [Een gegevensfeed maken](create-feed.md): Technische details voor het maken van een gegevensfeed, waarbij afzonderlijke velden gedetailleerder worden uitgelegd
* [Gegevensfeeds beheren](df-manage-feeds.md): Meer informatie over navigeren in de interface voor gegevensinvoer
* [Inhoud gegevensfeed](c-df-contents/datafeeds-contents.md): Begrijp wat binnen het samengeperste dossier is <!-- Is this still the output users can download from the destination? I aske Jun. -->
* [Definities gegevenskolom](c-df-contents/datafeeds-reference.md): Een uitgebreide lijst van alle beschikbare kolommen.
* Video navigating the data feed interface:

  >[!VIDEO](https://video.tv.adobe.com/v/25452/?quality=12)

* Video over het zoeken naar de id van uw gegevensfeed:

  >[!VIDEO](https://video.tv.adobe.com/v/335747/?quality=12)