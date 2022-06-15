---
title: Classificatieset-instellingen
description: Een classificatieset maken of bewerken.
source-git-commit: c9465ea0524225494aa5067d00ca5e7aba4bca92
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Classificatieset-instellingen

Configureer een classificatieset, upload gegevens of download gegevens.

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
   * **[!UICONTROL List delimiter]**: Selecteer het juiste lijstscheidingsteken. Als u een gedownload bestand of sjabloonbestand gebruikt, controleert u of [!UICONTROL List delimiter] hier komt overeen met [!UICONTROL List delimiter] wanneer het bestand is gedownload.
   * **[!UICONTROL Apply]**: Sla de geüploade classificatiegegevens op in de classificatieset.
