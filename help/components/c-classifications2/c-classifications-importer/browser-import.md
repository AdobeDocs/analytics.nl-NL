---
description: U kunt classificatiegegevens importeren (uploaden) via de browser. Deze methode beperkt het uploaden van classificatiegegevens tot één rapportsuite
subtopic: Classifications
title: Browserimport
topic: Admin tools
uuid: 56dfbf4c-36e6-49f4-b5cb-8ab714432825
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Browserimport

U kunt classificatiegegevens importeren (uploaden) via de browser. Deze methode beperkt het uploaden van classificatiegegevens tot één rapportsuite

## Browserimport {#concept_314FB3D5FD5A439B9CFEDE37A3337BA7}

U kunt classificatiegegevens importeren (uploaden) via de browser. Deze methode beperkt het uploaden van classificatiegegevens tot één rapportsuite

**[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**

## Browser voor classificaties importeren - Veldbeschrijvingen {#section_F628C47081DA4026A4D30E3D3454B1DA}

<table id="table_7FC7E510E7E74C2D9E8F316C5C6B66DB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Rapportsuite selecteren </td> 
   <td colname="col2"> <p>De rapportsuite waar u de classificatiegegevens wilt importeren. Het bestand met importgegevens moet overeenkomen met de indeling van de gegevensset in de rapportsuite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Te classificeren gegevensset </td> 
   <td colname="col2"> <p>De gegevensset die de classificaties ontvangt. De drop-down lijst omvat alle rapporten in uw rapportreeksen die voor classificaties worden gevormd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Te importeren bestand selecteren </td> 
   <td colname="col2"> <p>Hiermee kunt u het bestand met importgegevens zoeken dat u wilt uploaden. </p> <p>Opmerking:  De maximale bestandsgrootte voor uploaden is 1 MB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gegevens bij conflicten overschrijven </td> 
   <td colname="col2"> <p>Overschrijft automatisch bestaande gegevens die conflicteren met de geïmporteerde gegevens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Classificatiebestand automatisch downloaden nadat het importeren is voltooid </td> 
   <td colname="col2"> <p>Hiermee wordt automatisch een door tabs gescheiden bestand gedownload dat de gegevensset vertegenwoordigt met de nieuw geüploade classificatiegegevens. Adobe genereert dit bestand automatisch voor u als bij het importeren unieke id's worden gemaakt of als er fouten optreden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Classificaties importeren via de browser {#task_D7D51CB6FB35437AB68599B1B23FEAC1}

<!-- 

t_upload_a_saint_data_file_via_web_browser.xml

 -->

1. Klik op **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. Klik op **[!UICONTROL Import File]**.
1. Configureer de **[!UICONTROL Browser Import]** velden.
1. Klik op **[!UICONTROL Import File]**.
1. Bekijk het statusvenster voor het verwerken van berichten.
1. (Voorwaardelijk) Als u selecteerde **[!UICONTROL Automatically Download Classification File After Upload is Complete]**, specificeer waar u het resulterende dossier wilt opslaan wanneer de verwerking voltooit.
>Wanneer het importeren is gelukt, worden onmiddellijk de juiste wijzigingen in een exportbewerking weergegeven. Gegevenswijzigingen in rapporten duren echter maximaal vier uur wanneer u een browser importeert en maximaal 24 uur wanneer u een FTP-import gebruikt.

