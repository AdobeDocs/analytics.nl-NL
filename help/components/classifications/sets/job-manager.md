---
title: Taakmanager voor classificatie
description: Huidige en voltooide classificatietaken weergeven die zijn gegenereerd uit classificatiesets.
exl-id: 0470e131-79c6-4906-85f0-530d360ac227
feature: Classifications
source-git-commit: 811e321ce96aaefaeff691ed5969981a048d2c31
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 0%

---

# Taakmanager voor classificatie

Met de indelingsset kunt u huidige en voltooide classificatietaken weergeven die zijn gegenereerd op basis van classificatiesets. U kunt deze interface ook gebruiken om classificatiegegevens of sjablonen voor een bepaalde taak te downloaden of aanvullende gegevens te uploaden naar een taak.

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Jobs]**

U kunt geen banen van deze interface creëren. U kunt taken maken door gegevens naar een classificatieset te uploaden (handmatig of via een geconfigureerde externe locatie), een downloadbestand aan te vragen of een sjabloonbestand aan te vragen.

## Filterclassificatiesets

De linkerkant van het taakbeheer van de classificatieset biedt filterinstellingen om de gewenste taak te vinden. Door op het filterpictogram te klikken schakelt u de zichtbaarheid van de filterinstellingen in of uit. U kunt classificatiesets filteren op **[!UICONTROL Classification set]**, **[!UICONTROL Completion time]**, **[!UICONTROL Status]**, **[!UICONTROL Job Type]**, of **[!UICONTROL Source]**.

![Indelingsset taakfilters](../assets/classification-set-job-filters.png)

Er zijn aanvullende filteropties beschikbaar boven de taakbeheerkolommen van de classificatieset:

* **[!UICONTROL Search by title]**: Zoeken naar taken op bestandsnaam.
* **[!UICONTROL Load more]**: In de indelingsset worden aanvankelijk maximaal 1000 taken weergegeven. Als er meer taken zijn, klikt u op deze knop om 1000 extra taken te laden.
* **Kolommen tonen/verbergen**: Zichtbaarheid van elke kolom in-/uitschakelen [!UICONTROL Filename] en [!UICONTROL Completion time].

## Kolommen met indelingssets voor taakmanager

De volgende kolommen zijn beschikbaar in de het geplaatste baanmanager van de Classificatie:

* **[!UICONTROL Filename]**: De naam van het geüploade of gedownloade bestand.
* **[!UICONTROL Classification set]**: De naam van de classificatieset waarop het bestand van toepassing is. U kunt op de naam van de classificatieset klikken om de indelingsset te bereiken [Instellingen](manage/settings.md).
* **[!UICONTROL Size]**: De grootte van het bestand.
* **[!UICONTROL Status]**: De status van de taak die het bestand verwerkt.
   * **[!UICONTROL Created]**: De taak is verzonden.
   * **[!UICONTROL Queued]**: Het bestand is klaar om te worden verwerkt en wacht op een classificatieserver om het bestand te verwerken.
   * **[!UICONTROL Validated]**: Het bestand is geldig en wacht op verwerking.
   * **[!UICONTROL Failed validation]**: Het bestand is onjuist opgemaakt of anderszins ongeldig. Het bestand wordt niet verwerkt.
   * **[!UICONTROL Processing]**: Het bestand wordt actief verwerkt door Adobe.
   * **[!UICONTROL Failed processing]**: Het bestand is niet verwerkt.
   * **[!UICONTROL Complete]**: De verwerking is voltooid. Indelingsgegevens zijn zichtbaar in de rapportage.
   * **[!UICONTROL Failed]**: Algemene fout heeft geen betrekking op validatie of verwerking.
* **[!UICONTROL Job type]**: Het type taak.
* **[!UICONTROL Source]**: De taakbron.
* **[!UICONTROL File download]**: Alleen van toepassing op downloadtaken, zoals het downloaden van classificatiegegevens of het downloaden van sjablonen. Als een download gereed is, wordt in deze kolom een downloadkoppeling weergegeven.
* **[!UICONTROL Modified lines]**: Het aantal gewijzigde regels.
* **[!UICONTROL Completed lines]**: Het aantal voltooide regels.
* **[!UICONTROL Completion time]**: De datum en tijd waarop de taak is voltooid (of mislukt).
