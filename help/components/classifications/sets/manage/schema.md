---
title: Schema voor classificatieset
description: Het schema voor een afzonderlijke classificatieset weergeven en bewerken.
exl-id: 4a7c5bfe-ff2b-4380-af46-435801d73c1e
feature: Classifications
source-git-commit: a2a5e29eee46840d894ebf8d6184f8d6af9eee29
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Schema

Bekijk momenteel gevormde classificatiedimensies voor deze classificatieset.

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Sets]** > Klik op de gewenste naam van de classificatieset > **[!UICONTROL Schema]**

![ het schema UI van de classificatieset ](../../assets/classification-set-schema.png)

De volgende knoppen zijn beschikbaar:

<!--* **[!UICONTROL Add]**: Adds an empty row so that you can add a classification dimension to the schema.-->
* **[!UICONTROL Upload]**: upload classificatiegegevens handmatig voor een classificatieafmetingen. `JSON` -, `CSV` -, `TSV` - en `TAB` -bestanden worden ondersteund. Wanneer u een geldig bestand uploadt, wordt een tabelvoorbeeld weergegeven met gegevens die u wilt classificeren.
   * **[!UICONTROL File encoding]**: selecteer de juiste bestandencodering in deze vervolgkeuzelijst. Geldige opties zijn [!UICONTROL UTF-8] en [!UICONTROL Latin1] .
   * **[!UICONTROL List delimiter]**: selecteer het juiste lijstscheidingsteken. Als u een gedownload bestand of sjabloonbestand gebruikt, moet u ervoor zorgen dat [!UICONTROL List delimiter] hier overeenkomt met [!UICONTROL List delimiter] toen het bestand werd gedownload.
   * **[!UICONTROL Apply]**: sla de geüploade classificatiegegevens op in de classificatieset.

  ![ de vastgestelde classificatie uploadt ](../../assets/classification-set-upload.png)

* **[!UICONTROL Download]**: Download sleutelwaarden en hun classificatiekolommen.
   * **[!UICONTROL Rows]**: Het maximum aantal rijen dat in het downloadbestand moet worden opgenomen.
   * **[!UICONTROL Download rows received between]**: Een kalenderdatumkiezer waarmee u sleutelwaarden kunt filteren op het moment dat ze in de rapportage worden weergegeven. Als er geen sleutelwaarde is verzameld in dit datumbereik, wordt deze niet weergegeven in het gedownloade bestand.
   * **[!UICONTROL Data returned]**: Een vervolgkeuzelijst waarmee u sleutelwaarden kunt filteren die in het gedownloade bestand zijn opgenomen op basis van de bijbehorende classificatiegegevens.
      * **[!UICONTROL All classified values]**: bevat rijen waarin classificatiegegevens in ten minste één kolom zijn opgenomen.
      * **[!UICONTROL All unclassified values]**: hiermee worden rijen opgenomen waarin classificatiegegevens ontbreken in ten minste één kolom.
   * **[!UICONTROL File format]**: Een vervolgkeuzelijst die de bestandsindeling bepaalt waarin het downloadbestand zich bevindt. De opties zijn [!UICONTROL JSON] , [!UICONTROL Comma separated values] en [!UICONTROL Excel tab separated values] .
   * **[!UICONTROL File encoding]**: Een vervolgkeuzelijst die de bestandencodering bepaalt. De opties zijn [!UICONTROL UTF-8] en [!UICONTROL Latin1] . UTF-8 wordt aanbevolen.

  ![ Vastgestelde download van de Classificatie ](../../assets/classification-set-download.png)

* **[!UICONTROL Template]**: Download een sjabloonbestand. Dit bestand lijkt op de knop [!UICONTROL Download] , maar bevat geen classificatiegegevens of sleutelwaarden.
   * **[!UICONTROL File format]**: Een vervolgkeuzelijst die de bestandsindeling bepaalt waarin het sjabloonbestand zich bevindt. De opties zijn [!UICONTROL Comma separated values] en [!UICONTROL Excel tab separated values] .
   * **[!UICONTROL File encoding]**: Een vervolgkeuzelijst die de bestandencodering bepaalt. De opties zijn [!UICONTROL UTF-8] en [!UICONTROL Latin1] . UTF-8 wordt aanbevolen.
   * **[!UICONTROL List delimiters]**: Een vervolgkeuzelijst waarmee het scheidingsteken voor de lijsten wordt bepaald tussen classificatiekolommen op elke rij.

  ![ plaatste malplaatje van de Classificatie ](../../assets/classification-set-template.png)

* **[!UICONTROL Job history]**: Een kortere wegverbinding die u aan [ manager van de Baan ](../job-manager.md) neemt, tonend banen slechts voor deze classificatiereeks.
* **[!UICONTROL Automate]**: gegevens worden automatisch ingevoerd vanaf externe opslaglocaties.
   * **[!UICONTROL Location account]**: Een vervolgkeuzelijst met bestaande locatierekeningen die uw organisatie heeft geconfigureerd. Als uw organisatie reeds geen plaatsrekening heeft gevormd, kunt u één vormen door [!UICONTROL **te selecteren creeer een nieuwe rekening**].

     Voor informatie over het vormen van de plaatsrekening, zie [ de invoer en de uitvoerrekeningen van de wolk vormen ](/help/components/locations/configure-import-accounts.md).

   * **[!UICONTROL Location]**: Een vervolgkeuzelijst met bestaande locaties die uw organisatie heeft geconfigureerd. Als uw organisatie reeds geen plaats heeft gevormd, kunt u één vormen door [!UICONTROL **te selecteren creeer een nieuwe plaats**].

     Voor informatie over het vormen van een plaats, zie [ de invoer van de wolk en de uitvoerplaatsen ](/help/components/locations/configure-import-locations.md) vormen.

   * **[!UICONTROL Delimiter]**: Het kolomscheidingsteken voor geüploade bestanden. U kunt onder andere de volgende opties kiezen: [!UICONTROL Comma] , [!UICONTROL Semicolon] , [!UICONTROL Colon] , [!UICONTROL Vertical bar] , [!UICONTROL Space] , [!UICONTROL Forward slash] , [!UICONTROL Backward slash] , [!UICONTROL Dash] of [!UICONTROL Underscore] .

   * **[!UICONTROL Encoding]**: Een vervolgkeuzelijst die de bestandencodering bepaalt. De opties zijn [!UICONTROL UTF-8] en [!UICONTROL Latin1] . UTF-8 wordt aanbevolen.

De volgende acties zijn alleen beschikbaar nadat u een classificatie hebt geselecteerd.

* **voeg raadpleging** toe: Een raadplegingslijst is een classificatie van een classificatie. Het zijn metagegevens over een classificatiewaarde in plaats van de variabele zelf. De variabele Product kan bijvoorbeeld een classificatie van &quot;kleurcode&quot; hebben. Een opzoektabel met &quot;kleurnaam&quot; kan aan &quot;kleurcode&quot; worden gekoppeld om uit te leggen wat de kleuren zijn.

  ![ de raadplegingslijst van de Band ](../../assets/lookup.png)

* **noem** anders: Laat u de classificatie anders noemen.

* **Schrapping**: Laat u de classificatie schrappen.
