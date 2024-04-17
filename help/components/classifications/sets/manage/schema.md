---
title: Schema voor classificatieset
description: Het schema voor een afzonderlijke classificatieset weergeven en bewerken.
exl-id: 4a7c5bfe-ff2b-4380-af46-435801d73c1e
feature: Classifications
source-git-commit: 95767d10f63e20d5943fa95be3f2fe8f88e67e97
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# Schema

Bekijk momenteel gevormde classificatiedimensies voor deze classificatieset.

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Sets]** > Klik op de gewenste naam van de classificatieset > **[!UICONTROL Schema]**

De volgende knoppen zijn beschikbaar:

<!--* **[!UICONTROL Add]**: Adds an empty row so that you can add a classification dimension to the schema.-->
* **[!UICONTROL Upload]**: upload handmatig classificatiegegevens voor een of meer classificatiedimensies. `JSON`, `CSV`, `TSV`, en `TAB` worden ondersteund. Wanneer u een geldig bestand uploadt, wordt een tabelvoorbeeld weergegeven met gegevens die u wilt classificeren.
   * **[!UICONTROL File encoding]**: Selecteer de juiste bestandscodering met deze vervolgkeuzelijst. Geldige opties zijn [!UICONTROL UTF-8] en [!UICONTROL Latin1].
   * **[!UICONTROL List delimiter]**: Selecteer het juiste lijstscheidingsteken. Als u een gedownload bestand of sjabloonbestand gebruikt, moet u ervoor zorgen dat [!UICONTROL List delimiter] hier komt overeen met [!UICONTROL List delimiter] wanneer het bestand is gedownload.
   * **[!UICONTROL Apply]**: Sla de geüploade classificatiegegevens op in de classificatieset.

  ![Uploaden van classificatieset](../../assets/classification-set-upload.png)

* **[!UICONTROL Download]**: Download sleutelwaarden en hun classificatiekolommen.
   * **[!UICONTROL Rows]**: Het maximum aantal rijen dat in het downloadbestand moet worden opgenomen.
   * **[!UICONTROL Download rows received between]**: Een kalenderdatumkiezer waarmee u sleutelwaarden kunt filteren wanneer deze in de rapportage worden weergegeven. Als er geen sleutelwaarde is verzameld in dit datumbereik, wordt deze niet weergegeven in het gedownloade bestand.
   * **[!UICONTROL Data returned]**: Een vervolgkeuzelijst waarmee u sleutelwaarden kunt filteren die in het gedownloade bestand zijn opgenomen op basis van de bijbehorende classificatiegegevens.
      * **[!UICONTROL All classified values]**: Hiermee worden rijen opgenomen waarvan de indelingsgegevens in ten minste één kolom zijn opgenomen.
      * **[!UICONTROL All unclassified values]**: Bevat rijen waarin classificatiegegevens ontbreken in ten minste één kolom.
   * **[!UICONTROL File format]**: Een vervolgkeuzelijst die de bestandsindeling bepaalt waarin het downloadbestand zich bevindt. Opties omvatten [!UICONTROL JSON], [!UICONTROL Comma separated values], en [!UICONTROL Excel tab separated values].
   * **[!UICONTROL File encoding]**: Een vervolgkeuzelijst die de bestandencodering bepaalt. Opties omvatten [!UICONTROL UTF-8] en [!UICONTROL Latin1]. UTF-8 wordt aanbevolen.

  ![Downloaden van classificatieset](../../assets/classification-set-download.png)

* **[!UICONTROL Template]**: Download een sjabloonbestand. Dit bestand lijkt op het [!UICONTROL Download] , behalve dat het classificatiegegevens of sleutelwaarden bevat.
   * **[!UICONTROL File format]**: Een vervolgkeuzelijst die de bestandsindeling bepaalt waarin het sjabloonbestand zich bevindt. Opties omvatten [!UICONTROL Comma separated values], en [!UICONTROL Excel tab separated values].
   * **[!UICONTROL File encoding]**: Een vervolgkeuzelijst die de bestandencodering bepaalt. Opties omvatten [!UICONTROL UTF-8] en [!UICONTROL Latin1]. UTF-8 wordt aanbevolen.
   * **[!UICONTROL List delimiters]**: Een vervolgkeuzelijst die het scheidingsteken bepaalt voor de classificatiekolommen op elke rij.

  ![Classificatiesetjabloon](../../assets/classification-set-template.png)

* **[!UICONTROL Job history]**: Een snelkoppeling waarmee u naar de [Taakbeheer](../job-manager.md), waarbij alleen banen worden getoond voor deze classificatie.
* **[!UICONTROL Automate]**: Gegevens worden automatisch van externe opslaglocaties opgehaald.
   * **[!UICONTROL Location account]**: Een vervolgkeuzelijst met bestaande locatierekeningen die uw organisatie heeft geconfigureerd. Als uw organisatie nog geen locatieaccount heeft geconfigureerd, kunt u een account configureren door [!UICONTROL **Een nieuwe account maken**].

     Zie voor informatie over het configureren van de locatieaccount [Cloud-import- en exportaccounts configureren](/help/components/locations/configure-import-accounts.md).

   * **[!UICONTROL Location]**: Een vervolgkeuzelijst met bestaande locaties die door uw organisatie zijn geconfigureerd. Als uw organisatie nog geen locatie heeft geconfigureerd, kunt u een locatie configureren door [!UICONTROL **Een nieuwe locatie maken**].

     Voor informatie over het vormen van een plaats, zie [Locaties voor het importeren en exporteren van cloud configureren](/help/components/locations/configure-import-locations.md).

   * **[!UICONTROL Delimiter]**: Het kolomscheidingsteken voor geüploade bestanden. Opties omvatten [!UICONTROL Comma], [!UICONTROL Semicolon], [!UICONTROL Colon], [!UICONTROL Vertical bar], [!UICONTROL Space], [!UICONTROL Forward slash], [!UICONTROL Backward slash], [!UICONTROL Dash], of [!UICONTROL Underscore].

   * **[!UICONTROL Encoding]**: Een vervolgkeuzelijst die de bestandencodering bepaalt. Opties omvatten [!UICONTROL UTF-8] en [!UICONTROL Latin1]. UTF-8 wordt aanbevolen.
