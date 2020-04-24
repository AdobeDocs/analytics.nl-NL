---
title: Taken voor gegevensinvoer beheren
description: Leer hoe u afzonderlijke taken in gegevensfeeds beheert.
translation-type: tm+mt
source-git-commit: 7db88bce7b3d0f90fa5b50664d7c0c23904348c0

---


# Taken voor gegevensinvoer beheren

Taken zijn afzonderlijke taken die een gecomprimeerd bestand als uitvoer geven. Ze worden gecreëerd en bestuurd door feeds.

Voer het taakbeheer van de Gegevens van de toegang door deze stappen te volgen:

1. Meld u aan bij [ExperienceCloud.adobe.com](https://experiencecloud.adobe.com).
2. Klik in de rechterbovenhoek op het menu met 9-rasters en klik vervolgens op [!UICONTROL Analytics].
3. Klik in het bovenste menu op [!UICONTROL Admin] > [!UICONTROL Data Feeds].
4. Klik boven aan het tabblad Taken.

![Menu Gegevensinvoer](assets/AdminMenu.png)

## Navigeren door de interface

Een gegevensinvoertaak is één instantie waarbij Adobe een gecomprimeerd bestand voor een bepaald rapportagevenster verwerkt en uitvoert. De taakmanager geeft een verfijnde weergave om de status van individuele taken te zien.

![Taken](assets/jobs.jpg)

### Filters en zoeken

Gebruik filters en zoek naar de exacte taak die u zoekt.

Klik helemaal links op het filterpictogram om filteropties weer te geven of te verbergen. Filters zijn ingedeeld in categorieën. Klik op het chevron om filtercategorieën samen te vouwen of uit te vouwen. Klik op het selectievakje om dat filter toe te passen.

![Filter](assets/jobs-filter.jpg)

Gebruik Zoeken om een taak op naam te zoeken.

![Zoeken](assets/search.jpg)

### Feeds en taken

Klik op het tabblad feeds om overkoepelende feeds weer te geven die deze taken maken. Zie Gegevensfeeds [beheren](df-manage-feeds.md).

### Kolommen

Elke baan toont verscheidene kolommen die informatie over het verstrekken. Klik op een kolomkop om deze in oplopende volgorde te sorteren. Klik nogmaals op een kolomkop om deze in aflopende volgorde te sorteren. Als een bepaalde kolom niet zichtbaar is, klikt u op het kolompictogram rechtsboven.

![Kolompictogram](assets/job-cols.jpg)

* **ID** feed: Hiermee geeft u de feed-id weer, een unieke id. Taken die door dezelfde feed worden gemaakt, hebben dezelfde feed-id.
* **Taak-id**: Een unieke id voor de taak. Alle taken hebben een andere taak-id.
* **Naam** van feed: Vereiste kolom. Geeft de naam van de feed weer. Taken die door dezelfde feed worden gemaakt, hebben dezelfde voedernaam.
* **Rapportsuite**: De rapportsuite verwijst naar gegevens van de taak.
* **ID** rapportsuite: De unieke id van de rapportsuite.
* **Begintijd**: De tijd waarop de taak is gestart. Datum en tijd worden getoond in de de tijdzone van de rapportreeks met GMT compensatie. De dagelijkse voer begint typisch dichtbij middernacht in de tijdzone van de rapportreeks.
* **Status**: De status van het diervoeder.
   * Wachten op gegevens: De taak is operationeel en de gegevens voor het rapportvenster worden verzameld.
   * Verwerking: De taak maakt de gegevensbestanden en bereidt zich voor op het verzenden ervan.
   * Voltooid: De taak is voltooid zonder problemen.
   * Mislukt: De taak is niet voltooid. Zie [Problemen met taken](jobs-troubleshooting.md) oplossen om de oorzaak van fouten te achterhalen.
   * Wachten op exporteren: De gegevens voor het rapportagevenster zijn nog niet volledig verwerkt.
   * Geen gegevens: Er zijn geen gegevens in de rapportsuite voor het gevraagde rapportvenster.
* **Voltooiingstijd**: De tijd waarop de taak is voltooid. Datum en tijd worden getoond in de de tijdzone van de rapportreeks met GMT compensatie.
* **Aangevraagde datum**: Het rapportvenster van het bestand. De dagelijkse voer toont typisch 00:00 - 23:59 met een compensatie van GMT, die op een volledige dag wijst die op de tijdzone van de rapportreeks wordt gebaseerd. Uurfeeds laten het individuele uur zien waarvoor de baan is bedoeld.
