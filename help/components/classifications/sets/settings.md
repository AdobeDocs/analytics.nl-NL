---
title: Classificatieset-instellingen
description: Een classificatieset maken of bewerken.
exl-id: abf00508-5dde-4669-bf94-5eb4754888cc
source-git-commit: b8640d1387a475e2a9dd082759f0514bd18c1b6e
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# Classificatieset-instellingen

Configureer een classificatieset, upload gegevens of download gegevens.

>[!NOTE]
>
>Deze functie is beschikbaar voor alle klanten die hun rapportagesets hebben gemigreerd naar de nieuwe classificatiearchitectuur. Neem voor meer informatie contact op met de klantenservice van Adobe of uw accountmanager.

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Sets]** > Klik op de gewenste naam van de classificatieset

Bij het bewerken van een classificatieset zijn twee tabbladen beschikbaar. **[!UICONTROL Schema]** en **[!UICONTROL Settings]**.

## Instellingen

De volgende velden zijn beschikbaar in het dialoogvenster [!UICONTROL Settings] en kan worden bewerkt:

* **[!UICONTROL Name]**: De naam van de classificatieset.
* **[!UICONTROL Description]**: De beschrijving voor de classificatieset.
* **[!UICONTROL Owner name]**: De naam van de eigenaar.
* **[!UICONTROL Owner email]**: Het e-mailadres van de eigenaar.
* **[!UICONTROL Notify of issues]**: Een door komma&#39;s gescheiden lijst met e-mailadressen die op de hoogte worden gesteld van problemen met deze classificatieset.
* **[!UICONTROL Tags]**: Voeg een of meer tags toe aan de geselecteerde classificatieset(s), zodat u classificatiesets kunt ordenen of groeperen om deze in de toekomst gemakkelijker te vinden.

Aanvullende velden zijn ter informatie beschikbaar en kunnen niet worden bewerkt:

* **[!UICONTROL Type]**: Het type indeling tussen [!UICONTROL Primary] en [!UICONTROL Lookup]. Primaire classificaties worden doorgaans gebruikt.
* **[!UICONTROL Subscriptions]**: The Report Suite and variable that the Classification Set is apply to. Er wordt momenteel slechts één rapportsuite ondersteund voor een bepaalde classificatieset. De steun voor veelvoudige Reeksen van het Rapport wordt gepland.

## Schema

Momenteel geconfigureerde classificatieafmetingen voor dit abonnement weergeven. De volgende knoppen zijn beschikbaar:

* **[!UICONTROL Upload]**: Upload classificatiegegevens handmatig voor een of meer classificatiedimensies. JSON-, CSV-, TSV- en TAB-bestanden worden ondersteund. Wanneer u een geldig bestand uploadt, wordt een tabelvoorbeeld weergegeven met gegevens die u wilt classificeren.
   * **[!UICONTROL File encoding]**: Selecteer de juiste bestandencodering met deze vervolgkeuzelijst. Geldige opties zijn [!UICONTROL UTF-8] en [!UICONTROL Latin1].
   * **[!UICONTROL List delimiter]**: Selecteer het juiste lijstscheidingsteken. Als u een gedownload bestand of sjabloonbestand gebruikt, moet u ervoor zorgen dat de [!UICONTROL List delimiter] hier komt overeen met [!UICONTROL List delimiter] wanneer het bestand is gedownload.
   * **[!UICONTROL Apply]**: Sla de geüploade classificatiegegevens op in de classificatieset.

   ![Uploaden van classificatieset](../assets/classification-set-upload.png)

* **[!UICONTROL Download]**: Download sleutelwaarden en hun classificatiekolommen.
   * **[!UICONTROL Rows]**: Het maximumaantal rijen dat in het downloadbestand moet worden opgenomen.
   * **[!UICONTROL Download rows received between]**: Een kalenderdatumkiezer waarmee u sleutelwaarden kunt filteren op het moment dat ze in de rapportage worden weergegeven. Als er geen sleutelwaarde is verzameld in dit datumbereik, wordt deze niet weergegeven in het gedownloade bestand.
   * **[!UICONTROL Data returned]**: Een vervolgkeuzelijst waarmee u sleutelwaarden kunt filteren die in het gedownloade bestand zijn opgenomen op basis van de bijbehorende classificatiegegevens.
      * **[!UICONTROL All classified values]**: Hiermee worden rijen opgenomen waarvan de classificatiegegevens in ten minste één kolom zijn opgenomen.
      * **[!UICONTROL All unclassified values]**: Hier vindt u rijen waarin classificatiegegevens ontbreken in ten minste één kolom.
   * **[!UICONTROL File format]**: Vervolgkeuzelijst die de bestandsindeling bepaalt waarin het downloadbestand zich bevindt. Opties omvatten [!UICONTROL JSON], [!UICONTROL Comma separated values], en [!UICONTROL Excel tab separated values].
   * **[!UICONTROL File encoding]**: Vervolgkeuzelijst die de bestandencodering bepaalt. Opties omvatten [!UICONTROL UTF-8] en [!UICONTROL Latin1]. UTF-8 wordt aanbevolen.
   * **[!UICONTROL List delimiters]**: Vervolgkeuzelijst die het lijstscheidingsteken bepaalt dat classificatiekolommen op elke rij scheidt.

   ![Downloaden van classificatieset](../assets/classification-set-download.png)

* **[!UICONTROL Template]**: Download een sjabloonbestand. Dit bestand lijkt op het [!UICONTROL Download] , behalve dat het classificatiegegevens of sleutelwaarden bevat.
   * **[!UICONTROL File format]**: Vervolgkeuzelijst die de bestandsindeling bepaalt waarin het sjabloonbestand zich bevindt. Opties omvatten [!UICONTROL Comma separated values], en [!UICONTROL Excel tab separated values].
   * **[!UICONTROL File encoding]**: Vervolgkeuzelijst die de bestandencodering bepaalt. Opties omvatten [!UICONTROL UTF-8] en [!UICONTROL Latin1]. UTF-8 wordt aanbevolen.
   * **[!UICONTROL List delimiters]**: Vervolgkeuzelijst die het lijstscheidingsteken bepaalt dat classificatiekolommen op elke rij scheidt.
* **[!UICONTROL Job history]**: Een snelkoppeling die u naar de [Taakbeheer](job-manager.md), waarin alleen de banen voor deze classificatieset worden weergegeven.

   ![Classificatieset-sjabloon](../assets/classification-set-template.png)
