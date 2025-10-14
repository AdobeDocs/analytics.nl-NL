---
title: Taken voor gegevensfeed beheren
description: Leer hoe u afzonderlijke taken in gegevensfeeds beheert. Navigeer de interface, gebruik filters en onderzoek, en vind kolomdefinities.
feature: Data Feeds
exl-id: b17e333e-290f-42e4-b304-1e34282237a7
source-git-commit: 0eef1b1269dcfbc7648127602bdfe24d4789f4b7
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 0%

---

# Taken voor gegevensinvoer beheren

Taken zijn individuele taken die een gecomprimeerd bestand uitvoeren. Ze worden gecreëerd en bestuurd door feeds.

Voer het taakbeheer van de Gegevens van de toegang door deze stappen te volgen:

1. Login aan [&#x200B; experience.adobe.com &#x200B;](https://experiencecloud.adobe.com).
2. Klik op het 9-rastermenu rechtsboven en klik op [!UICONTROL Analytics] .
3. Klik in het bovenste menu op [!UICONTROL Admin] > [!UICONTROL Data Feeds] .
4. Klik boven aan het tabblad Taken.

![&#x200B; het voedermenu van Gegevens &#x200B;](assets/AdminMenu.png)

## Navigeren door de interface

Een gegevenfeed-taak is één instantie waarbij Adobe een gecomprimeerd bestand voor een bepaald rapportagevenster verwerkt en uitvoert. De taakmanager geeft een verfijnde weergave om de status van individuele taken te zien.

![&#x200B; Banen &#x200B;](assets/jobs.jpg)

### Filters en zoeken

Gebruik filters en zoek naar de exacte taak die u zoekt.

Klik helemaal links op het filterpictogram om filteropties weer te geven of te verbergen. Filters zijn ingedeeld in categorieën. Klik op het pictogram om filtercategorieën samen te vouwen of uit te vouwen. Klik op het selectievakje om dat filter toe te passen.

![&#x200B; Filter &#x200B;](assets/jobs-filter.jpg)

Gebruik Zoeken om een taak op naam te zoeken.

![&#x200B; Onderzoek &#x200B;](assets/search.jpg)

### Feeds en banen

Klik op het tabblad feeds om overkoepelende feeds weer te geven die deze taken maken. Zie [&#x200B; gegevensvoer beheren &#x200B;](df-manage-feeds.md).

### Kolommen

Elke baan toont verscheidene kolommen die informatie over het verstrekken. Klik op een kolomkop om deze in oplopende volgorde te sorteren. Klik nogmaals op een kolomkop om deze in aflopende volgorde te sorteren. Als een bepaalde kolom niet zichtbaar is, klikt u op het kolompictogram rechtsboven.

![&#x200B; pictogram van de Kolom &#x200B;](assets/job-cols.jpg)

* **identiteitskaart van het Gevoer**: Vertoningen identiteitskaart van het Gevoer, een uniek herkenningsteken. Taken die door dezelfde feed worden gemaakt, hebben dezelfde feed-id.
* **identiteitskaart van de Baan**: Een uniek herkenningsteken voor de baan. Alle taken hebben een andere taak-id.
* **Naam van het voer**: Vereiste kolom. Geeft de naam van de feed weer. Taken die door dezelfde feed worden gemaakt, hebben dezelfde voedernaam.
* **Reeks van het Rapport**: De rapportreeks de gegevens van baanverwijzingen van.
* **identiteitskaart van de Reeks van het Rapport**: Het unieke herkenningsteken van de rapportreeks.
* **Tijd van het Begin**: De tijd de baan begon. Datum en tijd worden getoond in de de tijdzone van de rapportreeks met GMT compensatie. De dagelijkse voer begint typisch dichtbij middernacht in de tijdzone van de rapportreeks.
* **Status**: De status van het voer.
   * Wachten op gegevens: de taak is operationeel en er worden gegevens voor het rapportagevenster verzameld.
   * Verwerking: de taak maakt de gegevensbestanden en bereidt zich voor op het verzenden ervan.
   * Voltooid: de taak is voltooid zonder problemen.
   * Mislukt: de taak is niet voltooid. Zie [&#x200B; problemen oplossen gegevensvoer &#x200B;](troubleshooting.md) helpen de oorzaak van mislukking bepalen.
   * Wachten op exporteren: de gegevens voor het rapportagevenster zijn nog niet volledig verwerkt.
   * Geen gegevens: de rapportsuite bevat geen gegevens voor het aangevraagde rapportvenster.
* **Tijd van de Voltooiing**: De tijd de baan eindigde. Datum en tijd worden getoond in de de tijdzone van de rapportreeks met GMT compensatie.
* **Gevraagde Datum**: Het rapporteringsvenster van het dossier. De dagelijkse voer toont typisch 00:00 - 23:59 met een compensatie van GMT, die op een volledige dag wijst die op de tijdzone van de rapportreeks wordt gebaseerd. Uurfeeds laten het individuele uur zien waarvoor de baan is bedoeld.
