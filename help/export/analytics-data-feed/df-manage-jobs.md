---
title: Taken voor gegevensfeed beheren
description: Leer hoe u afzonderlijke taken in gegevensfeeds beheert. Navigeer de interface, gebruik filters en onderzoek, en vind kolomdefinities.
feature: Data Feeds
exl-id: b17e333e-290f-42e4-b304-1e34282237a7
source-git-commit: d042bdb680504fdbf0ba346e5829713e529bd543
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 2%

---

# Taken voor gegevensinvoer beheren

Taken zijn individuele taken die een gecomprimeerd bestand uitvoeren. Ze worden gecreëerd en bestuurd door feeds.

U kunt de taakgeschiedenis weergeven voor elke gegevensfeed, taken opnieuw verzenden of taken opnieuw verwerken.

## Taakgeschiedenis weergeven voor een gegevensfeed

U kunt een lijst weergeven met taken voor het doorvoeren van gegevens voor een bepaalde gegevensfeed, samen met informatie over elke taak.

De taakgeschiedenis voor een gegevensfeed weergeven:

1. Meld u met uw Adobe ID aan bij [experiencecloud.adobe.com](https://experiencecloud.adobe.com).

1. Selecteer het 9-vierkante pictogram in hoger-recht, dan uitgezochte [!UICONTROL **Analytics**].

1. In de hoogste navigatiebar, ga [!UICONTROL **Admin**] > [!UICONTROL **het voer van Gegevens**].

   De voer van gegevens voor alle rapportreeksen die u hebt toegang tot wordt getoond. Of als er geen feeds zijn geconfigureerd, wordt op de pagina een knop **[!UICONTROL Create data feed]** weergegeven.

   ![&#x200B; de voedermanager van Gegevens &#x200B;](assets/data-feed-manager.png)

1. Selecteer checkbox naast de gegevensvoer die de banen bevat die u wilt bekijken, dan selecteren de [!UICONTROL **geschiedenis van de Baan**].

   De historie van de gegevensfeed wordt weergegeven met informatie over elke taak in de beschikbare kolommen.

1. (Facultatief) om de zichtbare kolommen in de lijst aan te passen selecteer het kolompictogram ![&#x200B; pictogram van de Kolom &#x200B;](assets/customize-columns-icon.png) in het hoogste recht, dan in de Customize lijstdialoog, selecteer elke kolom u elke kolom bekijken en wilt schrappen u wilt verbergen.

   De volgende kolommen zijn beschikbaar:

   * **[!UICONTROL Request period begin]**

   * **[!UICONTROL Request period end]**

   * **[!UICONTROL Scheduled]**

   * **[!UICONTROL Started]**

   * **[!UICONTROL Finished]**

   * **[!UICONTROL Run #]**

   * **[!UICONTROL Status]**

   * **[!UICONTROL Error code]**

   * **[!UICONTROL Error message]**

## Taak voor gegevensinvoer opnieuw verzenden

Wanneer u een gegevenfeed-taak opnieuw verzendt, worden de gegevens opnieuw met dezelfde gegevens en verwerking verzonden als toen het bestand oorspronkelijk werd verzonden. Alternatief, kunt u [&#x200B; een baan van de gegevensvoer &#x200B;](#reprocess-data-feed-jobs) opnieuw verwerken.

Een of meer taken voor gegevensinvoer opnieuw verzenden:

1. In Adobe Analytics, uitgezochte [!UICONTROL **Admin**] > [!UICONTROL **het voer van Gegevens**].

1. Selecteer checkbox naast de gegevensvoer die de banen bevat die u wilt opnieuw sturen, dan selecteren de [!UICONTROL **geschiedenis van de Baan**].

1. Schakel het selectievakje naast een of meer taken voor gegevensinvoer in en selecteer vervolgens **[!UICONTROL Resend]** . <!-- What does the status need to be? Error, ... -->

   ![&#x200B; het voer van gegevens opnieuw verwerken baan &#x200B;](assets/data-feed-job-resend.png)

## Taak voor gegevensinvoer opnieuw verwerken

Wanneer u een gegevenfeed-taak opnieuw verwerkt, worden de brongegevens van een gegevenfeed-taak opnieuw verwerkt en met de opnieuw verwerkte gegevens opnieuw verzonden. Alternatief, kunt u [&#x200B; opnieuw sturen een baan van de gegevensvoer &#x200B;](#resend-data-feed-jobs).

Een of meer taken voor het doorvoeren van gegevens opnieuw verwerken:

1. In Adobe Analytics, uitgezochte [!UICONTROL **Admin**] > [!UICONTROL **het voer van Gegevens**].

1. Selecteer checkbox naast de gegevensvoer die de banen bevat die u wilt opnieuw verwerken, dan de uitgezochte [!UICONTROL **geschiedenis van de Baan**].

1. Schakel het selectievakje naast een of meer taken voor gegevensinvoer in en selecteer vervolgens **[!UICONTROL Reprocess]** . <!-- What does the status need to be? Error, ... -->

   ![&#x200B; het voer van gegevens opnieuw verwerken baan &#x200B;](assets/data-feed-job-reprocess.png)
