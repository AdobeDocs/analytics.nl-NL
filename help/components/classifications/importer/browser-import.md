---
description: U kunt classificatiegegevens importeren (uploaden) via de browser. Deze methode beperkt het uploaden van classificatiegegevens tot één rapportsuite
title: Browserimport
feature: Classifications
exl-id: 5bef1f6d-9b27-464d-8343-472f300a7437
source-git-commit: a40f30bbe8fdbf98862c4c9a05341fb63962cdd1
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 1%

---

# Browserimport (verouderd)

U kunt classificatiegegevens importeren (uploaden) via de browser. Deze methode beperkt het uploaden van classificatiegegevens tot één rapportsuite

## Browserimport {#concept_314FB3D5FD5A439B9CFEDE37A3337BA7}

U kunt classificatiegegevens importeren (uploaden) via de browser. Deze methode beperkt het uploaden van classificatiegegevens tot één rapportsuite

**[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**

## Browser voor classificaties importeren - Veldbeschrijvingen {#section_F628C47081DA4026A4D30E3D3454B1DA}

| Element | Beschrijving |
| --- | --- |
| Rapportsuite selecteren | De rapportsuite waar u de classificatiegegevens wilt importeren. Het bestand met importgegevens moet overeenkomen met de indeling van de gegevensset in de rapportsuite. |
| Te classificeren gegevensset | De gegevensset die de classificaties ontvangt. De drop-down lijst omvat alle rapporten in uw rapportreeksen die voor classificaties worden gevormd. |
| Te importeren bestand selecteren | Hiermee kunt u het bestand met importgegevens zoeken dat u wilt uploaden.  Opmerking: de maximale bestandsgrootte voor uploaden is 1 MB. |
| Gegevens bij conflicten overschrijven | Overschrijft automatisch bestaande gegevens die conflicteren met de geïmporteerde gegevens.<br>**Belangrijk**: Deze optie is niet beschikbaar voor rapportreeksen die voor de Nieuwe Architectuur van de Classificatie worden toegelaten. |
| Classificatiebestand automatisch downloaden nadat het importeren is voltooid | Hiermee wordt automatisch een door tabs gescheiden bestand gedownload dat de gegevensset vertegenwoordigt met de nieuw geüploade classificatiegegevens. Adobe genereert dit bestand automatisch voor u als bij het importeren unieke id&#39;s worden gemaakt of als er fouten optreden.<br>**Belangrijk**: Deze optie is niet beschikbaar voor rapportreeksen die voor de Nieuwe Architectuur van de Classificatie worden toegelaten. |


## Classificaties importeren via de browser {#task_D7D51CB6FB35437AB68599B1B23FEAC1}

1. Klik op **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]** .
1. Klik op **[!UICONTROL Import File]**.
1. Configureer de **[!UICONTROL Browser Import]** -velden.
1. Klik op **[!UICONTROL Import File]**.
1. Bekijk het statusvenster voor het verwerken van berichten.
1. (Voorwaardelijk) Als u **[!UICONTROL Automatically Download Classification File After Upload is Complete]** hebt geselecteerd, geeft u aan waar u het resulterende bestand wilt opslaan wanneer de verwerking is voltooid. Merk op dat deze optie niet beschikbaar is voor rapportsuites die voor de Nieuwe Architectuur van de Classificatie worden toegelaten.

>Wanneer het importeren is gelukt, worden onmiddellijk de juiste wijzigingen in een exportbewerking weergegeven. Gegevenswijzigingen in rapporten duren echter maximaal vier uur wanneer u een browser importeert en maximaal 24 uur wanneer u een FTP-import gebruikt.
