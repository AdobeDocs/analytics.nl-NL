---
title: Gebruikersinterface voor gegevensinvoer
description: Leer hoe te om de interface van de gegevensvoer te navigeren.
translation-type: tm+mt
source-git-commit: c9b3471b138c2e056a5abadb4ace6bb4eccd1d72

---


# Gegevensfeeds beheren

Met de gegevensvoedermanager kunt u gegevensfeeds voor uw organisatie maken, bewerken en verwijderen. Als u toestemmingen hebt om tot de manager van de gegevensvoer toegang te hebben, kunt u gegevensvoer voor alle rapportreeksen beheren zichtbaar aan u.

Voer de volgende stappen uit om toegang te krijgen tot gegevensbeheer:

1. Meld u aan bij [ExperienceCloud.adobe.com](https://experiencecloud.adobe.com).
2. Klik in de rechterbovenhoek op het menu met 9-rasters en klik vervolgens op [!UICONTROL Analytics].
3. Klik in het bovenste menu op [!UICONTROL Admin] > [!UICONTROL Data Feeds].

![Menu Gegevensinvoer](assets/AdminMenu.png)

## Navigeren door de interface

Wanneer het aankomen aan de pagina van de gegevensvoedermanager, kijkt de interface gelijkaardig aan het volgende:

![Gegevensfeeds](assets/feeds.png)

Als er geen feeds zijn ingesteld, wordt op de pagina een [!UICONTROL Create New Data Feed] knop weergegeven.

### Filters en zoeken

Gebruik filters en zoek naar de exacte feed die u zoekt.

Klik helemaal links op het filterpictogram om filteropties weer te geven of te verbergen. Filters zijn ingedeeld in categorieën. Klik op het chevron om filtercategorieën samen te vouwen of uit te vouwen. Klik op het selectievakje om dat filter toe te passen.

![Filter](assets/filters.jpg)

Gebruik Zoeken om een feed op naam te zoeken.

![Zoeken](assets/search.jpg)

### Feeds en taken

Klik op het tabblad Taken om afzonderlijke taken weer te geven die door elk van uw feeds worden gemaakt. Zie Taken voor [gegevensinvoer](df-manage-jobs.md)beheren.

### Toevoegen

Klik bij de tabbladen feeds en jobs op + [!UICONTROL Add] om een nieuwe feed te maken. Zie Een feed [](create-feed.md) toevoegen voor meer informatie.

### Kolommen

Elk gecreeerd voer toont verscheidene kolommen die informatie over het verstrekken. Klik op een kolomkop om deze in oplopende volgorde te sorteren. Klik nogmaals op een kolomkop om deze in aflopende volgorde te sorteren. Als een bepaalde kolom niet zichtbaar is, klikt u op het kolompictogram rechtsboven.

![Kolompictogram](assets/cols.jpg)

* **Naam** van feed: Vereiste kolom. Geeft de naam van de feed weer.
* **ID** feed: Hiermee geeft u de feed-id weer, een unieke id.
* **Rapportsuite**: De rapportsuite waarin de feed verwijst naar gegevens van.
* **ID** rapportsuite: De unieke id van de rapportsuite.
* **Gegevenskolommen**: Welke gegevenskolommen actief zijn voor het voer. In de meeste gevallen zijn er te veel kolommen om in deze indeling weer te geven.
* **Interval**: Vermeld of het diervoeder per uur of per dag is.
* **Doeltype**: Het doeltype voor de feed. Bijvoorbeeld FTP, Amazon S3 of Azure.
* **Host** bestemming: De locatie waar het bestand wordt geplaatst. Bijvoorbeeld, `ftp.example.com`.
* **Eigenaar**: De gebruikersaccount waarmee de feed is gemaakt.
* **Status**: De status van het diervoeder.
   * Actief: Het voer is operationeel.
   * Goedkeuring in behandeling: In sommige gevallen is goedkeuring van Adobe vereist voor een feed voordat taken kunnen worden gegenereerd.
   * Verwijderd: Het voer wordt verwijderd.
   * Voltooid: Het voer is verwerkt. Een voltooide feed kan worden bewerkt, in de wachtstand worden gezet of worden geannuleerd.
   * In behandeling: De feed is gemaakt, maar nog niet actief. Feeds blijven in deze toestand voor een korte overgangsperiode.
   * Inactief: Gelijk aan de staat &#39;gepauzeerd&#39; of &#39;in wachtstand&#39;. Wanneer het voer opnieuw wordt geactiveerd, wordt het opnieuw om banen te leveren vanaf het moment dat het wordt gestopt.
* **Laatst gewijzigd**: De datum waarop het diervoeder voor het laatst is gewijzigd. Datum en tijd worden getoond in de de tijdzone van de rapportreeks met GMT compensatie.
* **Begindatum**: De datum van de eerste taak voor deze feed. Datum en tijd worden getoond in de de tijdzone van de rapportreeks met GMT compensatie.
* **Einddatum**: De datum van de laatste taak voor deze feed. Doorlopende gegevensfeeds hebben geen einddatum.

## Handelingen voor gegevensinvoer

Klik op het selectievakje naast een gegevensfeed om beschikbare acties weer te geven.

* **Taakgeschiedenis**: Alle taken weergeven die aan deze gegevensfeeds zijn gekoppeld. Hiermee gaat u automatisch naar de interface [voor het](df-manage-jobs.md)beheren van taken.
* **Verwijderen**: Hiermee verwijdert u de gegevensfeed en stelt u de status in op [!UICONTROL Deleted].
* **Kopiëren**: Hiermee [maakt u een nieuwe feed](create-feed.md) met alle instellingen van de huidige feed. U kunt een gegevensfeed niet kopiëren als er meerdere zijn geselecteerd.
* **Pauzeren**: Stopt de verwerking voor de feed en stelt de status in op [!UICONTROL Inactive].
* **Activeren**: Alleen beschikbaar voor inactieve feeds. Hiermee worden verwerkingsgegevens opgehaald waar deze zijn weggelaten, en worden zo nodig datums teruggezet.
