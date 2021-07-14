---
description: Classificaties worden gebruikt om waarden in groepen te categoriseren en op groepsniveau te rapporteren. U kunt bijvoorbeeld alle campagnes voor betaalde zoekopdrachten classificeren in een categorie zoals pop-muziektermen en rapporteren over het succes van die categorie ten opzichte van metriek zoals Instanties (doorklikken) en conversie naar succesgebeurtenissen.
title: Conversieclassificaties
exl-id: b4855000-adf3-4e3b-af36-f4803383126d
source-git-commit: fa12c51be5d0f788dbdaacfbd36504d1cda92a58
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 3%

---

# Conversieclassificaties

Classificaties worden gebruikt om waarden in groepen te categoriseren en op groepsniveau te rapporteren. Bijvoorbeeld, kunt u alle [!UICONTROL Paid Search] campagnes in een categorie zoals *pop muziektermijnen* classificeren en over het succes van die categorie met betrekking tot metriek zoals Instanties (klik-door), en omzetting in succesgebeurtenissen rapporteren. U kunt maximaal 255 classificaties toevoegen aan een variabele.

Met conversieclassificaties kunt u conversievariabelen classificeren. Zodra geclassificeerd, kan om het even welk rapport dat u het gebruiken van de zeer belangrijke gegevens kunt produceren ook worden geproduceerd gebruikend de bijbehorende gegevenseigenschappen.

Na het toelaten van classificaties, gebruik [Indelingsimporteur](/help/components/classifications/importer/c-working-with-saint.md) om specifieke waarden aan de aangewezen classificatie toe te wijzen.

>[!WARNING]
>
>Het anders noemen van een classificatie kan kwesties met bestaande regels veroorzaken die in [de bouwer van de classificatieregel](/help/components/classifications/crb/classification-rule-builder.md) worden gecreeerd. Als u een classificatie anders noemt die classificatieregels heeft, zorg ervoor dat u elke regel verbetert zodat richt het aan de anders genoemde classificatie.

## Omzettingsclassificatiebeschrijvingen

| Element | Beschrijving |
| --- | --- |
| Naam | De indelingsnaam |
| Datum ingeschakeld (alleen tekst) | Geeft aan of de tekstclassificatie een datumbereik voor campagnevariabelen is. |
| Opties (alleen tekst) | Hiermee maakt u een lijst met classificatiewaarden die beschikbaar zijn voor deze classificatie. Gebruik Opties met campagnevariabelen om gebruikers een lijst met ondersteunde waarden voor de classificatie in Campagnebeheer te bieden. |
| Type nummer (alleen numeriek) | Geeft het type getal in de numerieke classificatie aan. U kunt onder andere de opties Numeriek, Percentage en Valuta kiezen. |

## Conversieclassificaties toevoegen

Stappen die beschrijven hoe u conversieclassificaties in Admin kunt toevoegen.

1. Klik op **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. Een rapportsuite selecteren.
1. Klik op **[!UICONTROL Edit Settings]** > **[!UICONTROL Conversion]** > **[!UICONTROL Conversion Classifications]**.
1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Select Classification Type]** de variabele waar u een classificatie wilt toevoegen.

   ![Stapinfo](../assets/sub_class_create.png)

1. Plaats de muis boven het pictogram **[!UICONTROL Edit Classification]** en selecteer **[!UICONTROL Add Classification]**.
1. Selecteer in het veld **[!UICONTROL Select Type]** het type classificatie dat u aan de variabele wilt toevoegen.

   U kunt onder andere **[!UICONTROL Text]** en **[!UICONTROL Numeric]** kiezen. Zie [Informatie over classificaties](/help/components/classifications/c-classifications.md) voor meer informatie over classificatietypen.
1. Configureer in het dialoogvenster **[!UICONTROL Text Classifications]** de classificatie naar wens.

1. Voeg opties toe of verwijder opties in het dialoogvenster **[!UICONTROL Dropdown List]**.

   Met Opties toevoegen maakt u een lijst met classificatiewaarden die beschikbaar zijn voor deze classificatie. U kunt deze optie gebruiken met campagnevariabelen om gebruikers een lijst van gesteunde waarden voor de classificatie in de Manager van de Campagne te voorzien. Gebruik dit voor classificatiedimensies als u een klein aantal toegestane waarden hebt die zelden of nooit veranderen. Bijvoorbeeld, zou u verschillende campagnes kunnen in werking stellen die op verschillende niveaus van klantenloyaliteit worden gericht: Zilver, Goud en Platinum. Vervolgens kunt u de vervolgkeuzelijst gebruiken om er zeker van te zijn dat alleen de waarden worden geaccepteerd die overeenkomen met de drie niveaus. Als iemand een andere waarde probeert te gebruiken, wordt deze genegeerd.

1. Klik op **[!UICONTROL Save]**.

## Een conversieclassificatie verwijderen

Een conversieclassificatie verwijderen wanneer deze niet meer nodig is.

1. Open Report Suite Manager door op **[!UICONTROL Admin]** **[!UICONTROL Report Suites]** in de koptekst van de Suite te klikken.
1. Een rapportsuite selecteren.
1. Klik op **[!UICONTROL Edit Settings]** > **[!UICONTROL Conversion]** > **[!UICONTROL Conversion Classifications]**.
1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Select Classification Type]** de variabele waar u een classificatie wilt verwijderen.
1. Plaats de muis boven het pictogram **[!UICONTROL Edit Classification]** en selecteer **[!UICONTROL Delete Classification]**.
1. Klik in het dialoogvenster Classificatie verwijderen op **[!UICONTROL Delete]**.
