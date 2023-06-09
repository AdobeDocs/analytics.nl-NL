---
title: Schema voor classificatieset
description: Het schema voor een afzonderlijke classificatieset weergeven en bewerken.
source-git-commit: d0e3b28590b24d630a192ee857a7d84c115dc8c1
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# Schema

Bekijk momenteel gevormde classificatiedimensies voor deze classificatieset.

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Sets]** > Klik op de gewenste naam van de classificatieset > **[!UICONTROL Schema]**

De volgende knoppen zijn beschikbaar:

<!--* **[!UICONTROL Add]**: Adds an empty row so that you can add a classification dimension to the schema.-->
* **[!UICONTROL Upload]**: Upload classificatiegegevens handmatig voor een of meer classificatiedimensies. `JSON`, `CSV`, `TSV`, en `TAB` worden ondersteund. Wanneer u een geldig bestand uploadt, wordt een tabelvoorbeeld weergegeven met gegevens die u wilt classificeren.
   * **[!UICONTROL File encoding]**: Selecteer de juiste bestandscodering in deze vervolgkeuzelijst. Geldige opties zijn [!UICONTROL UTF-8] en [!UICONTROL Latin1].
   * **[!UICONTROL List delimiter]**: Selecteer het juiste lijstscheidingsteken. Als u een gedownload bestand of sjabloonbestand gebruikt, moet u ervoor zorgen dat de [!UICONTROL List delimiter] hier komt overeen met [!UICONTROL List delimiter] wanneer het bestand is gedownload.
   * **[!UICONTROL Apply]**: Sla de geüploade classificatiegegevens op in de classificatieset.

  ![Uploaden van classificatieset](../../assets/classification-set-upload.png)

* **[!UICONTROL Download]**: Download sleutelwaarden en hun classificatiekolommen.
   * **[!UICONTROL Rows]**: Het maximumaantal rijen dat in het downloadbestand moet worden opgenomen.
   * **[!UICONTROL Download rows received between]**: Een kalenderdatumkiezer waarmee u sleutelwaarden kunt filteren op het moment dat ze in de rapportage worden weergegeven. Als er geen sleutelwaarde is verzameld in dit datumbereik, wordt deze niet weergegeven in het gedownloade bestand.
   * **[!UICONTROL Data returned]**: Een vervolgkeuzelijst waarmee u sleutelwaarden in het gedownloade bestand kunt filteren op basis van de bijbehorende classificatiegegevens.
      * **[!UICONTROL All classified values]**: Hiermee worden rijen opgenomen waarvan de classificatiegegevens in ten minste één kolom zijn opgenomen.
      * **[!UICONTROL All unclassified values]**: Hier vindt u rijen waarin classificatiegegevens ontbreken in ten minste één kolom.
   * **[!UICONTROL File format]**: Een vervolgkeuzelijst die de bestandsindeling bepaalt waarin het downloadbestand zich bevindt. Opties omvatten [!UICONTROL JSON], [!UICONTROL Comma separated values], en [!UICONTROL Excel tab separated values].
   * **[!UICONTROL File encoding]**: Een vervolgkeuzelijst die de bestandencodering bepaalt. Opties omvatten [!UICONTROL UTF-8] en [!UICONTROL Latin1]. UTF-8 wordt aanbevolen.

  ![Downloaden van classificatieset](../../assets/classification-set-download.png)

* **[!UICONTROL Template]**: Download een sjabloonbestand. Dit bestand lijkt op het [!UICONTROL Download] , behalve dat het classificatiegegevens of sleutelwaarden bevat.
   * **[!UICONTROL File format]**: Een vervolgkeuzelijst die de bestandsindeling bepaalt waarin het sjabloonbestand zich bevindt. Opties omvatten [!UICONTROL Comma separated values], en [!UICONTROL Excel tab separated values].
   * **[!UICONTROL File encoding]**: Een vervolgkeuzelijst die de bestandencodering bepaalt. Opties omvatten [!UICONTROL UTF-8] en [!UICONTROL Latin1]. UTF-8 wordt aanbevolen.
   * **[!UICONTROL List delimiters]**: Een vervolgkeuzelijst die het lijstscheidingsteken bepaalt dat classificatiekolommen op elke rij scheidt.

  ![Classificatiesetjabloon](../../assets/classification-set-template.png)

* **[!UICONTROL Job history]**: Een snelkoppeling die u naar de [Taakbeheer](../job-manager.md), waarbij alleen banen worden getoond voor deze classificatie.
* **[!UICONTROL Automate]**: Automatisch gegevens van externe opslaglocaties opnemen.
   * **[!UICONTROL Location account]**: Een vervolgkeuzelijst met bestaande locatierekeningen die uw organisatie heeft geconfigureerd. Er is een knop beschikbaar om een locatieaccount te maken.
   * **[!UICONTROL Location]**: Een vervolgkeuzelijst met bestaande locaties die door uw organisatie zijn geconfigureerd. Er is een knop beschikbaar om een locatie te maken.
   * **[!UICONTROL Delimiter]**: Het kolomscheidingsteken voor geüploade bestanden. Opties omvatten [!UICONTROL Comma], [!UICONTROL Semicolon], [!UICONTROL Colon], [!UICONTROL Vertical bar], [!UICONTROL Space], [!UICONTROL Forward slash], [!UICONTROL Backward slash], [!UICONTROL Dash], of [!UICONTROL Underscore].
   * **[!UICONTROL Encoding]**: Een vervolgkeuzelijst die de bestandencodering bepaalt. Opties omvatten [!UICONTROL UTF-8] en [!UICONTROL Latin1]. UTF-8 wordt aanbevolen.
