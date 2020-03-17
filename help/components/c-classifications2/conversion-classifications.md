---
description: Classificaties worden gebruikt om waarden in groepen te categoriseren en op groepsniveau te rapporteren. U kunt bijvoorbeeld alle campagnes voor betaalde zoekopdrachten classificeren in een categorie zoals pop-muziektermen en rapporteren over het succes van die categorie ten opzichte van metriek zoals Instanties (doorklikken) en conversie naar succesgebeurtenissen.
subtopic: Classifications
title: Conversieclassificaties
topic: Admin tools
uuid: 4c8726c9-f527-44e1-be01-8c7b3b5c20f0
translation-type: tm+mt
source-git-commit: ''

---


# Conversieclassificaties

Classificaties worden gebruikt om waarden in groepen te categoriseren en op groepsniveau te rapporteren. U kunt bijvoorbeeld alle campagnes voor betaalde zoekopdrachten classificeren in een categorie zoals pop-muziektermen en rapporteren over het succes van die categorie ten opzichte van metriek zoals Instanties (doorklikken) en conversie naar succesgebeurtenissen.

## Conversieclassificaties {#concept_B4B1478A8CB540599AC9D4A58CA4B6FE}

Classificaties worden gebruikt om waarden in groepen te categoriseren en op groepsniveau te rapporteren. U kunt bijvoorbeeld alle campagnes voor betaald zoeken classificeren in een categorie zoals *pop-muziektermen* en rapporteren over het succes van die categorie ten opzichte van metriek zoals Instanties (doorklikken) en conversie naar succesgebeurtenissen.

Met conversieclassificaties kunt u conversievariabelen classificeren. Zodra geclassificeerd, kan om het even welk rapport dat u het gebruiken van de zeer belangrijke gegevens kunt produceren ook worden geproduceerd gebruikend de bijbehorende gegevenseigenschappen.

Nadat classificaties zijn ingeschakeld, gebruikt u de [Classificatieimportmodule](/help/components/c-classifications2/c-classifications-importer/c-working-with-saint.md) om specifieke waarden aan de juiste classificatie toe te wijzen.

## Omzettingsclassificatiebeschrijvingen {#section_4A98DD5F5C314B9DAEE710AEE4EE51D4}

<table id="table_0B72C485467348E2A34BF913441F4AF5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Naam</span> </td> 
   <td colname="col2"> De classificatienaam. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Datum ingeschakeld (alleen tekst)</span> </td> 
   <td colname="col2"> <p>Geeft aan of de tekstclassificatie een datumbereik voor campagnevariabelen is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Opties (alleen tekst)</span> </td> 
   <td colname="col2">Hiermee maakt u een lijst met classificatiewaarden die beschikbaar zijn voor deze classificatie. Gebruik <span class="wintitle"> Opties</span> met campagnevariabelen om gebruikers een lijst van gesteunde waarden voor de classificatie in de Manager <span class="wintitle"> van de</span>Campagne te voorzien. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Type nummer (alleen numeriek)</span> </td> 
   <td colname="col2">Geeft het type getal in de numerieke classificatie aan. U kunt kiezen uit <span class="wintitle"> Numeriek</span>, <span class="wintitle"> Percentage</span>en <span class="wintitle"> Valuta</span>. </td> 
  </tr> 
 </tbody> 
</table>

## Conversieclassificaties toevoegen {#task_D535D09E3EAF4CD1A15A6B93C0BB1BB5}

<!-- 

t_classification_conversion.xml

 -->

Stappen die beschrijven hoe u conversieclassificaties in Admin kunt toevoegen.

1. Klik op **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. Selecteer een rapportsuite.
1. Klik op **[!UICONTROL Edit Settings]** > **[!UICONTROL Conversion]** > **[!UICONTROL Conversion Classifications]**.
1. Selecteer in de **[!UICONTROL Select Classification Type]** vervolgkeuzelijst de variabele waaraan u een classificatie wilt toevoegen.

   ![Stapinfo](assets/sub_class_create.png)

1. Plaats de muis boven het **[!UICONTROL Edit Classification]** pictogram en selecteer vervolgens **[!UICONTROL Add Classification]**.
1. Selecteer in het **[!UICONTROL Select Type]** veld het type classificatie dat u aan de variabele wilt toevoegen.

   De opties omvatten **[!UICONTROL Text]** en **[!UICONTROL Numeric]**. Zie [Informatie over classificaties](/help/components/c-classifications2/c-classifications.md)voor meer informatie over classificatietypen.
1. Configureer de classificatie naar wens in het **[!UICONTROL Text Classifications]** dialoogvenster.

   Zie Beschrijving van [conversieclassificaties](/help/components/c-classifications2/conversion-classifications.md#section_4A98DD5F5C314B9DAEE710AEE4EE51D4) voor informatie over deze elementen.

1. Voeg opties toe of verwijder opties in het **[!UICONTROL Dropdown List]** dialoogvenster.

   Met Opties toevoegen maakt u een lijst met classificatiewaarden die beschikbaar zijn voor deze classificatie. U kunt deze optie gebruiken met campagnevariabelen om gebruikers een lijst van gesteunde waarden voor de classificatie in de Manager van de Campagne te voorzien. Gebruik dit voor classificatiedimensies als u een klein aantal toegestane waarden hebt die zelden of nooit veranderen. Bijvoorbeeld, zou u verschillende campagnes kunnen in werking stellen die op verschillende niveaus van klantenloyaliteit worden gericht: Zilver, Goud en Platinum. Vervolgens kunt u de vervolgkeuzelijst gebruiken om er zeker van te zijn dat alleen de waarden worden geaccepteerd die overeenkomen met de drie niveaus. Als iemand een andere waarde probeert te gebruiken, wordt deze genegeerd.
1. Klik op **[!UICONTROL Save]**.

## Een conversieclassificatie verwijderen {#task_566651BC245944618A6A833E58211FDE}

<!-- 

t_classification_delete_conversion.xml

 -->

Een conversieclassificatie verwijderen wanneer deze niet meer nodig is.

1. Open Report Suite Manager door op **[!UICONTROL Admin]**> **[!UICONTROL Report Suites]** in de koptekst van de Intel Health Care Management Suite te klikken.
1. Selecteer een rapportsuite.
1. Klik op **[!UICONTROL Edit Settings]** > **[!UICONTROL Conversion]** > **[!UICONTROL Conversion Classifications]**.
1. Selecteer in de **[!UICONTROL Select Classification Type]** vervolgkeuzelijst de variabele waar u een classificatie wilt verwijderen.
1. Plaats de muis boven het **[!UICONTROL Edit Classification]** pictogram en selecteer vervolgens **[!UICONTROL Delete Classification]**.
1. Klik in het dialoogvenster Classificatie verwijderen op **[!UICONTROL Delete]**.
