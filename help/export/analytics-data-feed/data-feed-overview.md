---
description: Leer hoe u gegevensfeeds kunt gebruiken om onbewerkte gegevens uit Adobe Analytics te halen. Kom de eerste vereisten voor het gebruiken van gegevensvoer te weten wat te doen daarna.
keywords: clickStream;data feed;datafeed;Data Feed
title: Overzicht van gegevensfeed voor analyse
feature: Data Feeds
exl-id: 2cfff9ad-cdb5-4ae9-a266-4f3d3d046f0c
source-git-commit: 08e29da4847e8ef70bd4435949e26265d770f557
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Overzicht van gegevensinvoer voor analyse

Gegevensfeeds zijn een krachtige manier om onbewerkte gegevens uit Adobe Analytics te halen. Deze onbewerkte gegevens kunnen worden gebruikt op andere platformen buiten de Adobe om naar eigen goeddunken van uw organisatie te worden gebruikt. De gegevens worden aan het einde van elk uur in partijen per uur of aan het einde van elke dag in partijen per uur verstrekt.

## Vereisten

Zorg ervoor dat u aan alle volgende vereisten voldoet voordat u gegevensfeeds gebruikt.

* Een werkende implementatie die gegevens naar de servers van de de gegevensinzameling van de Adobe verzendt. Zie [ bevestigen en een implementatie ](/help/implement/launch/validate-publish-prod.md) in de gids van de Implementatie publiceren.
* Uw account is een productbeheerder voor Analytics of uw account behoort tot een productprofiel met toegang tot gegevensfeeds.
* Een emmertje geconfigureerd op Amazon S3, Google Cloud Platform, Azure RBAC of Azure SAS.
* (Verouderd: alleen vereist voor verouderde FTP- en SFTP-doeltypen) U kunt kiezen voor een FTP-site en gebruikersgegevens (FTP-referenties die door uw organisatie worden geleverd).

## Volgende stappen

Met de volgende bronnen krijgt u inzicht in de basisworkflow voor het verkrijgen van gegevensfeeds. Nadat u de basisworkflow hebt begrepen, kunt u met teams binnen uw organisatie werken om onbewerkte gegevens in een database op te slaan of in te voeren.

* [ voer van Gegevens beste praktijken ](/help/export/analytics-data-feed/data-feeds-best-practices.md): Beste praktijken voor het creëren van en het beheren van gegevensvoer.
* [ creeer een gegevensvoer ](create-feed.md): De technische details voor het creëren van een gegevensvoer, die individuele gebieden in meer detail verklaren
* [ beheert gegevensvoer ](df-manage-feeds.md): Leer meer over het navigeren van de interface van de gegevensvoer
* [ de voederinhoud van Gegevens ](c-df-contents/datafeeds-contents.md): Begrijp wat binnen het samengedrukte dossier <!-- Is this still the output users can download from the destination? I aske Jun. --> is
* [ de kolomdefinities van Gegevens ](c-df-contents/datafeeds-reference.md): Een uitvoerige lijst van alle beschikbare kolommen.

>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ de interface van de gegevensvoer ](https://video.tv.adobe.com/v/25452?quality=12&learn=on){target="_blank"} voor een demo video navigeren.

>[!ENDSHADEBOX]



>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ uw gegevens voer identiteitskaart ](https://video.tv.adobe.com/v/335747?quality=12&learn=on){target="_blank"} voor een demo video vinden.

>[!ENDSHADEBOX]
