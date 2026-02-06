---
title: Taken voor gegevensfeed beheren
description: Leer hoe u afzonderlijke taken in gegevensfeeds beheert. Navigeer de interface, gebruik filters en onderzoek, en vind kolomdefinities.
feature: Data Feeds
exl-id: b17e333e-290f-42e4-b304-1e34282237a7
source-git-commit: 728e807764901ad2bd6834339e5e75348dd5a988
workflow-type: tm+mt
source-wordcount: '801'
ht-degree: 1%

---

# Taken voor gegevensinvoer beheren

Taken zijn individuele taken die een gecomprimeerd bestand uitvoeren. Ze worden gecreëerd en bestuurd door feeds.

Taken voor het beheren van gegevenfeed:

1. Meld u met uw Adobe ID aan bij [experiencecloud.adobe.com](https://experiencecloud.adobe.com).

1. Selecteer het 9-vierkante pictogram in hoger-recht, dan uitgezochte [!UICONTROL **Analytics**].

1. In de hoogste navigatiebar, ga [!UICONTROL **Admin**] > [!UICONTROL **het voer van Gegevens**].

   De voer van gegevens voor alle rapportreeksen die u hebt toegang tot wordt getoond. Of als er geen feeds zijn geconfigureerd, wordt op de pagina een knop [!UICONTROL Create New Data Feed] weergegeven.

   ![&#x200B; de voedermanager van Gegevens &#x200B;](assets/data-feed-manager.png)

1. (Facultatief) selecteer checkbox naast de gegevensvoer die de banen bevat die u wilt bekijken, dan de uitgezochte [!UICONTROL **geschiedenis van de Baan**].

   Voor meer informatie, zie [&#x200B; de baangeschiedenis van de Mening voor een gegevensvoer &#x200B;](#view-job-history-for-a-data-feed).

## Filteren en zoeken

U kunt filteren en zoeken om de exacte taak te zoeken die u zoekt.

Klik helemaal links op het filterpictogram om filteropties weer te geven of te verbergen. Filters zijn ingedeeld in categorieën. Klik op het pictogram om filtercategorieën samen te vouwen of uit te vouwen. Klik op het selectievakje om een filter toe te passen.

![&#x200B; Filter &#x200B;](assets/jobs-filter.png)

Gebruik Zoeken om een taak op naam te zoeken.

![&#x200B; Onderzoek &#x200B;](assets/search.png)

## Kolommen sorteren en aanpassen

Elke taak bevat meerdere kolommen die informatie over de taak bevatten. U kunt informatie in elke kolom sorteren en de kolommen aanpassen die worden getoond.

### Kolommen sorteren

Selecteer een kolomkop om deze in oplopende volgorde te sorteren. Selecteer nogmaals een kolomkop om deze in aflopende volgorde te sorteren.

### Kolommen aanpassen

De zichtbare kolommen in de tabel aanpassen:

1. Selecteer het kolompictogram ![&#x200B; pictogram van de Kolom &#x200B;](assets/customize-columns-icon.png) in het top-right.

1. Selecteer in het dialoogvenster Tabel aanpassen elke kolom die u wilt weergeven en hef de selectie van elke kolom op die u wilt verbergen.

   De volgende kolommen zijn beschikbaar:

* **naam van het voer**: Vereiste kolom. Geeft de naam van de feed weer. Taken die door dezelfde feed worden gemaakt, hebben dezelfde voedernaam.
* **identiteitskaart van het Gevoer**: Vertoningen identiteitskaart van het Gevoer, een uniek herkenningsteken. Taken die door dezelfde feed worden gemaakt, hebben dezelfde feed-id.
* **Reeks van het Rapport**: De rapportsuite de gegevens van baanverwijzingen van.
* **Reeks identiteitskaart van het Rapport**: Het unieke herkenningsteken van de rapportreeks.
* **Interval**: Het interval van het voer.
* **type van Bestemming**: Het bestemmingstype van het voer.
* **Bestemming**: De bestemming van het voer.
* **Eigenaar**: De eigenaar van het voer.
* **Status**: De status van het voer.
   * Wachten op gegevens: de taak is operationeel en er worden gegevens voor het rapportagevenster verzameld.
   * Verwerking: de taak maakt de gegevensbestanden en bereidt zich voor op het verzenden ervan.
   * Voltooid: de taak is voltooid zonder problemen.
   * Mislukt: de taak is niet voltooid. Zie [&#x200B; problemen oplossen gegevensvoer &#x200B;](troubleshooting.md) helpen de oorzaak van mislukking bepalen.
   * Wachten op exporteren: de gegevens voor het rapportagevenster zijn nog niet volledig verwerkt.
   * Geen gegevens: de rapportsuite bevat geen gegevens voor het aangevraagde rapportvenster.
* **Laatste veranderde**: De tijd de voer werd het laatst gewijzigd.
* **de datum van het Begin**: De tijd de baan begon. Datum en tijd worden getoond in de de tijdzone van de rapportreeks met GMT compensatie. De dagelijkse voer begint typisch dichtbij middernacht in de tijdzone van de rapportreeks.
* **einddatum**: De tijd de baan beëindigde. Datum en tijd worden getoond in de de tijdzone van de rapportreeks met GMT compensatie.

## Taakgeschiedenis weergeven voor een gegevensfeed

U kunt een lijst weergeven met taken voor gegevensinvoer uit het verleden voor een bepaalde gegevensfeed, samen met informatie over elke taak.

De taakgeschiedenis voor een gegevensfeed weergeven:

1. In Adobe Analytics, uitgezochte [!UICONTROL **Admin**] > [!UICONTROL **het voer van Gegevens**].

   ![&#x200B; de voedermanager van Gegevens &#x200B;](assets/data-feed-manager.png)

1. Selecteer checkbox naast de gegevensvoer de waarvan baangeschiedenis u wilt bekijken, dan selecteren [!UICONTROL **de geschiedenis van de Baan**].

   De historie van de gegevensfeed-taak wordt weergegeven, waarbij de volgende informatie beschikbaar is over elke taak (selecteer het kolompictogram om kolommen toe te voegen die standaard niet zichtbaar zijn):

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

U kunt een gegevenfeed-taak opnieuw verzenden als u het gegevensbestand opnieuw wilt verzenden met exact dezelfde gegevens en verwerking als toen het oorspronkelijk werd verzonden. Alternatief, kunt u [&#x200B; een baan van de gegevensvoer &#x200B;](#reprocess-data-feed-jobs) opnieuw verwerken.

Een of meer taken voor gegevensinvoer opnieuw verzenden:

1. In Adobe Analytics, uitgezochte [!UICONTROL **Admin**] > [!UICONTROL **het voer van Gegevens**].

1. Selecteer checkbox naast de gegevensvoer die de banen bevat die u wilt opnieuw sturen, dan selecteren de [!UICONTROL **geschiedenis van de Baan**].

1. Schakel het selectievakje naast een of meer taken voor gegevensinvoer in en selecteer vervolgens **[!UICONTROL Resend]** . <!-- What does the status need to be? Error, ... -->

   ![&#x200B; het voer van gegevens opnieuw verwerken baan &#x200B;](assets/data-feed-job-resend.png)

## Taak voor gegevensinvoer opnieuw verwerken

U kunt de brongegevens van een gegevensinvoertaak opnieuw verwerken en deze opnieuw met de opnieuw verwerkte gegevens verzenden. Alternatief, kunt u [&#x200B; opnieuw sturen een baan van de gegevensvoer &#x200B;](#resend-data-feed-jobs).

Een of meer taken voor het doorvoeren van gegevens opnieuw verwerken:

1. In Adobe Analytics, uitgezochte [!UICONTROL **Admin**] > [!UICONTROL **het voer van Gegevens**].

1. Selecteer checkbox naast de gegevensvoer die de banen bevat die u wilt opnieuw verwerken, dan de uitgezochte [!UICONTROL **geschiedenis van de Baan**].

1. Schakel het selectievakje naast een of meer taken voor gegevensinvoer in en selecteer vervolgens **[!UICONTROL Reprocess]** . <!-- What does the status need to be? Error, ... -->

   ![&#x200B; het voer van gegevens opnieuw verwerken baan &#x200B;](assets/data-feed-job-reprocess.png)
