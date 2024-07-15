---
title: Gebruikersinterface voor gegevensinvoer
description: Leer hoe te om de interface van de gegevensvoer te navigeren.
feature: Data Feeds
exl-id: 4d4f0062-e079-48ff-9464-940c6425ad54
source-git-commit: 3916115169f526bb91442d251e6159496efd547f
workflow-type: tm+mt
source-wordcount: '1135'
ht-degree: 0%

---

# Gegevensfeeds beheren

Met de gegevensvoedermanager kunt u gegevensfeeds voor uw organisatie maken, bewerken en verwijderen. Als u toestemmingen hebt om tot de manager van de gegevensvoer toegang te hebben, kunt u gegevensvoer voor alle rapportreeksen beheren zichtbaar aan u.

+++Bekijk een video over gegevensvoederbeheer.

>[!VIDEO](https://video.tv.adobe.com/v/25452/?quality=12)

+++

## Gegevensfeeds weergeven

1. Meld u met uw Adobe ID aan bij [experiencecloud.adobe.com](https://experiencecloud.adobe.com).
1. Selecteer het 9-vierkante pictogram in hoger-recht, dan uitgezochte [!UICONTROL **Analytics**].
1. In de hoogste navigatiebar, ga [!UICONTROL **Admin**] > [!UICONTROL **het voer van Gegevens**].

   De voer van gegevens voor alle rapportreeksen die u hebt toegang tot wordt getoond. Of als er geen feeds zijn geconfigureerd, wordt op de pagina een knop [!UICONTROL Create New Data Feed] weergegeven.

   ![ het voer van Gegevens ](assets/feeds.png)

## Een gegevensfeed maken

Met de knop [!UICONTROL Add] kunt u een nieuwe feed maken. Zie [ een gegevensvoer ](create-feed.md) voor meer informatie creëren.

## Een gegevensfeed bewerken

1. In Adobe Analytics, uitgezochte [!UICONTROL **Admin**] > [!UICONTROL **het voer van Gegevens**].

1. Zoek de gegevensfeed die u wilt bewerken. Om van een gegevensvoer de plaats te bepalen, kunt u [ filter en de lijst van gegevensvoer ](#filter-and-search-the-list-of-data-feeds) zoeken.

1. Selecteer de gegevensvoer in de [!UICONTROL **naam van het Gegeven**] kolom.

1. Breng de gewenste wijzigingen aan in de gegevensinvoer.

   Wanneer het bijwerken van de [!UICONTROL **sectie van de Bestemming**] voor een gegevensvoer die u uitgeeft, kunt u een verschillende rekening en een plaats kiezen voor de nieuwe gegevensvoer in de [!UICONTROL **Rekening**] en [!UICONTROL **plaats**] drop-down gebieden te gebruiken.

   De rekeningen en de plaatsen kunnen worden uitgegeven zoals die in [ wordt beschreven vormen de invoer en de uitvoerrekeningen van de wolk ](/help/components/locations/configure-import-accounts.md) en [ vormen wolkeninvoer en de uitvoerplaatsen ](/help/components/locations/configure-import-locations.md). Het bewerken van een account of locatie heeft invloed op alle items die aan dat account of die locatie zijn gekoppeld.

   Met eerdere versies van de gegevensfeeds Manager kon u FTP-, SFTP-, S3- en Azure-blokdoelen maken. Doelen die in deze eerdere versies van het gegevensfeeds-beheer zijn gemaakt, kunnen niet worden bewerkt of gekopieerd.

1. Selecteer [!UICONTROL **sparen**].

## De lijst met gegevensfeeds filteren en doorzoeken

1. In Adobe Analytics, uitgezochte [!UICONTROL **Admin**] > [!UICONTROL **het voer van Gegevens**].

1. Gebruik zoekopdrachten of filters om een specifieke feed te zoeken.

   * Typ in het zoekveld de naam van een feed. Alleen de overeenkomende feeds worden weergegeven in de lijst met beschikbare feeds.

   * Klik helemaal links op het filterpictogram om filteropties weer te geven of te verbergen. Filters zijn ingedeeld in categorieën. U kunt filtercategorieën samenvouwen of uitbreiden. Schakel het selectievakje naast een filter dat u wilt toepassen in.

![ Filter ](assets/filters.png)

## Taak voor gegevensinvoer weergeven

1. In Adobe Analytics, uitgezochte [!UICONTROL **Admin**] > [!UICONTROL **het voer van Gegevens**].

1. Selecteer het [!UICONTROL **lusje van Banen**] om individuele banen te bekijken die elk van uw voer creeert.

   of

   Om banen voor specifieke gegevensvoer te bekijken, selecteer checkbox naast één of meerdere gegevensvoer, dan de uitgezochte [!UICONTROL **geschiedenis van de Baan**].

   Voor meer informatie, zie [ leiden de banen van de gegevensvoer ](df-manage-jobs.md).

## Een gegevensfeed kopiëren

1. In Adobe Analytics, uitgezochte [!UICONTROL **Admin**] > [!UICONTROL **het voer van Gegevens**].

1. Selecteer checkbox naast de gegevensvoer die u wilt kopiëren, dan selecteren [!UICONTROL **Exemplaar**].

   Neemt u [ om een nieuwe voer ](create-feed.md) met alle montages van het huidige voer tot stand te brengen. Deze optie is niet zichtbaar als er meer dan één gegevensfeed is geselecteerd.

   Wanneer het bijwerken van de [!UICONTROL **sectie van de Bestemming**] voor een gegevensvoer die u kopieert, kunt u een verschillende rekening en een plaats kiezen voor de nieuwe gegevensvoer in de [!UICONTROL **Rekening**] en [!UICONTROL **drop-down gebieden van de Plaats**] te gebruiken.

   De rekeningen en de plaatsen kunnen worden uitgegeven zoals die in [ wordt beschreven vormen de invoer en de uitvoerrekeningen van de wolk ](/help/components/locations/configure-import-accounts.md) en [ vormen wolkeninvoer en de uitvoerplaatsen ](/help/components/locations/configure-import-locations.md). Het bewerken van een account of locatie heeft invloed op alle items die aan dat account of die locatie zijn gekoppeld.

   Met eerdere versies van de gegevensfeeds Manager kon u FTP-, SFTP-, S3- en Azure-blokdoelen maken. Doelen die in deze eerdere versies van het gegevensfeeds-beheer zijn gemaakt, kunnen niet worden bewerkt of gekopieerd.

## Een gegevensfeed pauzeren

U kunt de verwerking van de feed stoppen en de status ervan instellen op [!UICONTROL Inactive] .

1. In Adobe Analytics, uitgezochte [!UICONTROL **Admin**] > [!UICONTROL **het voer van Gegevens**].

1. Selecteer checkbox naast de gegevensvoer die u wilt pauzeren, dan selecteren [!UICONTROL **Pauzeren**].

## Een gegevensfeed activeren

U kunt inactieve feeds activeren.

Als u een back-up maakt van feeds (feeds die alleen historische gegevens verwerken), worden de verwerkingsgegevens hervat vanaf het punt waarop ze zijn gestopt. Zo nodig worden de datums opnieuw ingevuld. Met Live feeds worden ook verwerkingsgegevens hervat vanaf het punt waar ze zijn gestopt.

>[!AVAILABILITY]
>
>De volgende wijziging in de manier waarop live feeds verwerkingsgegevens hervat, bevindt zich in de Beperkte testfase van de release:
> 
>**Levende voer hervat verwerkingsgegevens van de huidige tijd.**
>
>Deze wijziging is mogelijk nog niet beschikbaar in uw omgeving.
>
>Deze opmerking wordt verwijderd wanneer deze wijziging over het algemeen beschikbaar is. Voor informatie over het de versieproces van de Analyse, zie [ de eigenschapversies van Adobe Analytics ](/help/release-notes/releases.md).

Een gegevensfeed activeren:

1. In Adobe Analytics, uitgezochte [!UICONTROL **Admin**] > [!UICONTROL **het voer van Gegevens**].

1. Selecteer checkbox naast de inactieve gegevensvoer die u wilt activeren, dan selecteren [!UICONTROL **activeert**].

## Een gegevensfeed verwijderen

Wanneer u een gegevensfeed verwijdert, wordt de status ingesteld op [!UICONTROL Deleted] .

1. In Adobe Analytics, uitgezochte [!UICONTROL **Admin**] > [!UICONTROL **het voer van Gegevens**].

1. Selecteer checkbox naast de gegevensvoer die u wilt schrappen, dan selecteren [!UICONTROL **Schrapping**].

## Kolommen configureren in de gegevensvoedermanager

Elk gecreeerd voer toont verscheidene kolommen die informatie over het verstrekken. Selecteer een kolomkop om deze in oplopende volgorde te sorteren. Selecteer nogmaals een kolomkop om deze in aflopende volgorde te sorteren. Als een bepaalde kolom niet zichtbaar is, klikt u op het kolompictogram rechtsboven.

![ pictogram van de Kolom ](assets/cols.jpg)

De volgende kolommen zijn beschikbaar:

* **naam van het voer**: Vereiste kolom. Geeft de naam van de feed weer.
* **identiteitskaart van het Gevoer**: Vertoningen identiteitskaart van het Gevoer, een uniek herkenningsteken.
* **Reeks van het Rapport**: De rapportsuite de gegevens van voederverwijzingen van.
* **Reeks identiteitskaart van het Rapport**: Het unieke herkenningsteken van de rapportreeks.
* **Kolommen van Gegevens**: Welke gegevenskolommen actief zijn voor het voer. In de meeste gevallen zijn er te veel kolommen om in deze indeling weer te geven.
* **Interval**: Indicator of het voer uur of dag is.
* **Type van Bestemming**: Het bestemmingstype voor het voer. Amazon S3, GCP of Azure.
* **Gastheer van de Bestemming**: De plaats het dossier wordt geplaatst.
* **Eigenaar**: De gebruikersrekening die tot het voer leidde.
* **Status**: De status van het voer.
   * Actief: Het voer is operationeel.
   * Goedkeuring in behandeling: in sommige gevallen moet een diervoeder worden goedgekeurd door de Adobe voordat het kan beginnen met het genereren van banen.
   * Verwijderd: de feed wordt verwijderd.
   * Voltooid: De verwerking van de feed is voltooid. Een volledig ingevuld diervoeder kan worden bewerkt, in de wachtstand worden gezet of worden geannuleerd.
   * In behandeling: de feed is gemaakt, maar nog niet actief. Feeds blijven in deze toestand voor een korte overgangsperiode.
   * Inactief: gelijk aan de status &#39;gepauzeerd&#39; of &#39;in wachtstand&#39;. Voor informatie over wat met backfill voer en levende voer gebeurt wanneer een inactief voer wordt opnieuw geactiveerd, zie [ een gegevensvoer ](#activate-a-data-feed) activeren.
* **Laatste Gewijzigd**: De datum het voer werd het laatst gewijzigd. Datum en tijd worden getoond in de de tijdzone van de rapportreeks met GMT compensatie.
* **Datum van het Begin**: De datum van de eerste baan voor dit voer. Datum en tijd worden getoond in de de tijdzone van de rapportreeks met GMT compensatie.
* **Datum van het Eind**: De datum van de laatste baan voor dit voer. Doorlopende gegevensfeeds hebben geen einddatum.

