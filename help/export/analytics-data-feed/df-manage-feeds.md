---
title: Gebruikersinterface voor gegevensinvoer
description: Leer hoe te om de interface van de gegevensvoer te navigeren.
feature: Data Feeds
exl-id: 4d4f0062-e079-48ff-9464-940c6425ad54
source-git-commit: 0916ef4ddc2ca65f01721f4d79d7af825dcf50e3
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 0%

---

# Gegevensfeeds beheren

Met de gegevensvoedermanager kunt u gegevensfeeds voor uw organisatie maken, bewerken en verwijderen. Als u toestemmingen hebt om tot de manager van de gegevensvoer toegang te hebben, kunt u gegevensvoer voor alle rapportreeksen beheren zichtbaar aan u.

Hier volgt een video over de interface van Data Feeds Management:

>[!VIDEO](https://video.tv.adobe.com/v/25452/?quality=12)

Voer de volgende stappen uit om toegang te krijgen tot gegevensbeheer:

1. Aanmelden bij [ExperienceCloud.adobe.com](https://experiencecloud.adobe.com).
2. Klik in het menu met 9-rasters rechtsboven en klik vervolgens op [!UICONTROL Analytics].
3. Klik in het bovenste menu op [!UICONTROL Admin] > [!UICONTROL Data Feeds].

![Menu Gegevensinvoer](assets/AdminMenu.png)

## Navigeren door de interface

Wanneer het aankomen aan de pagina van de gegevensvoedermanager, kijkt de interface gelijkaardig aan het volgende:

![Gegevensfeeds](assets/feeds.png)

Als er geen feeds zijn ingesteld, wordt op de pagina een [!UICONTROL Create New Data Feed] knop.

### Filters en zoeken

Gebruik filters en zoek naar de exacte feed die u zoekt.

Klik helemaal links op het filterpictogram om filteropties weer te geven of te verbergen. Filters zijn ingedeeld in categorieën. Klik op het chevron om filtercategorieën samen te vouwen of uit te vouwen. Klik op het selectievakje om dat filter toe te passen.

![Filter](assets/filters.jpg)

Gebruik Zoeken om een feed op naam te zoeken.

![Zoeken](assets/search.jpg)

### Feeds en taken

Klik op het tabblad Taken om afzonderlijke taken weer te geven die door elk van uw feeds worden gemaakt. Zie [Taken voor gegevensinvoer beheren](df-manage-jobs.md).

### Toevoegen

Klik op + bij de tabbladen feeds en taken [!UICONTROL Add] om een nieuwe feed te maken. Zie [Een gegevensfeed maken](create-feed.md) voor meer informatie .

### Kolommen

Elk gecreeerd voer toont verscheidene kolommen die informatie over het verstrekken. Klik op een kolomkop om deze in oplopende volgorde te sorteren. Klik nogmaals op een kolomkop om deze in aflopende volgorde te sorteren. Als een bepaalde kolom niet zichtbaar is, klikt u op het kolompictogram rechtsboven.

![Kolompictogram](assets/cols.jpg)

* **Naam van feed**: Vereiste kolom. Geeft de naam van de feed weer.
* **Feed-id**: Hiermee geeft u de feed-id weer, een unieke id.
* **Rapportsuite**: De rapportsuite waarin de feed verwijst naar gegevens van.
* **ID van rapportsuite**: De unieke id van de rapportsuite.
* **Gegevenskolommen**: Welke gegevenskolommen actief zijn voor het voer. In de meeste gevallen zijn er te veel kolommen om in deze indeling weer te geven.
* **Interval**: Vermeld of het diervoeder per uur of per dag is.
* **Doeltype**: Het doeltype voor de feed. Bijvoorbeeld Amazon S3, GCP of Azure.
* **Host bestemming**: De locatie waar het bestand wordt geplaatst.
* **Eigenaar**: De gebruikersaccount waarmee de feed is gemaakt.
* **Status**: De status van het diervoeder.
   * Actief: Het voer is operationeel.
   * Goedkeuring in behandeling: In sommige gevallen is goedkeuring van een diervoeder door Adobe vereist voordat het kan beginnen met het genereren van banen.
   * Verwijderd: Het voer wordt verwijderd.
   * Voltooid: Het voer is verwerkt. Een voltooide feed kan worden bewerkt, in de wachtstand worden gezet of worden geannuleerd.
   * In behandeling: De feed is gemaakt, maar nog niet actief. Feeds blijven in deze toestand voor een korte overgangsperiode.
   * Inactief: Gelijk aan de staat &#39;gepauzeerd&#39; of &#39;in wachtstand&#39;. Wanneer het voer opnieuw wordt geactiveerd, wordt het opnieuw om banen te leveren vanaf het moment dat het wordt gestopt.
* **Laatst gewijzigd**: De datum waarop het diervoeder voor het laatst is gewijzigd. Datum en tijd worden getoond in de de tijdzone van de rapportreeks met GMT compensatie.
* **Begindatum**: De datum van de eerste taak voor deze feed. Datum en tijd worden getoond in de de tijdzone van de rapportreeks met GMT compensatie.
* **Einddatum**: De datum van de laatste taak voor deze feed. Doorlopende gegevensfeeds hebben geen einddatum.

## Handelingen voor gegevensinvoer

Klik op het selectievakje naast een gegevensfeed om beschikbare acties weer te geven.

* **Taakgeschiedenis**: Alle taken weergeven die aan deze gegevensfeeds zijn gekoppeld. Hiermee gaat u automatisch naar de [interface voor beheer van taken](df-manage-jobs.md).
* **Verwijderen**: Hiermee verwijdert u de gegevensfeed en stelt u de status in op [!UICONTROL Deleted].
* **Kopiëren**: Neemt u [een nieuwe feed maken](create-feed.md) met alle instellingen van de huidige feed. U kunt een gegevensfeed niet kopiëren als er meerdere zijn geselecteerd.
* **Pauzeren**: Stopt de verwerking van de feed en stelt de status in op [!UICONTROL Inactive].
* **Activeren**: Alleen beschikbaar voor inactieve feeds. Hiermee worden verwerkingsgegevens opgehaald waar deze zijn weggelaten, en worden zo nodig datums teruggezet.