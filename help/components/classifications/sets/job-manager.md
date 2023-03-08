---
title: Taakbeheer voor classificatieset
description: Huidige en voltooide classificatietaken weergeven die zijn gegenereerd uit classificatiesets.
exl-id: 0470e131-79c6-4906-85f0-530d360ac227
source-git-commit: b8640d1387a475e2a9dd082759f0514bd18c1b6e
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Indelingsset taakbeheer

Met de Classificatieset Taakbeheer kunt u huidige en voltooide classificatietaken zien die zijn gegenereerd op basis van classificatiesets. U kunt deze interface ook gebruiken om classificatiegegevens of sjablonen voor een bepaalde taak te downloaden of aanvullende gegevens te uploaden naar een taak.

>[!NOTE]
>
>Deze functie is beschikbaar voor alle klanten die hun rapportagesets hebben gemigreerd naar de nieuwe classificatiearchitectuur. Neem voor meer informatie contact op met de klantenservice van Adobe of uw accountmanager.

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Jobs]**

U kunt geen taken maken van deze interface. In plaats daarvan kunt u taken maken door gegevens te uploaden naar een classificatieset, een downloadbestand aan te vragen of een sjabloonbestand aan te vragen.

## Filterclassificatiesets

De linkerkant van het Manager van de Baan van de Reeks van de Classificatie verstrekt filtermontages om van de gewenste Baan de plaats te bepalen. Door op het filterpictogram te klikken schakelt u de zichtbaarheid van de filterinstellingen in of uit. U kunt classificatiesets filteren op **[!UICONTROL Classification Set]**, **[!UICONTROL Completion time]**, of **[!UICONTROL Status]**.

![Classificatieset taakfilters](../assets/classification-set-job-filters.png)

Er zijn aanvullende filteropties beschikbaar boven de kolommen Taakbeheer classificatieset:

* **[!UICONTROL Search by title]**: Zoeken naar taken op bestandsnaam.
* **[!UICONTROL Load more]**: In eerste instantie worden maximaal 1000 taken weergegeven in de classificatieset Taakbeheer. Klik op deze knop om 1000 extra taken te laden.
* **Kolommen tonen/verbergen**: Zichtbaarheid van elke kolom in-/uitschakelen [!UICONTROL Filename] en [!UICONTROL Completion time].

## Taakbeheerkolommen voor classificatieset

De volgende kolommen zijn beschikbaar in het Manager van de Baan van de Reeks van de Classificatie:

* **[!UICONTROL Filename]**: De naam van het geüploade of gedownloade bestand.
* **[!UICONTROL Classification Set]**: De naam van de classificatieset waarop het bestand van toepassing is. U kunt op de naam van de classificatieset klikken om de classificatieset te bereiken [Instellingen](settings.md).
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
* **[!UICONTROL Type]**: Het type taak.
* **[!UICONTROL File download]**: Alleen van toepassing op downloadtaken, zoals het downloaden van classificatiegegevens of het downloaden van sjablonen. Als een download gereed is, wordt in deze kolom een downloadkoppeling weergegeven.
* **[!UICONTROL Completion time]**: De datum en tijd waarop de taak is voltooid (of mislukt).
