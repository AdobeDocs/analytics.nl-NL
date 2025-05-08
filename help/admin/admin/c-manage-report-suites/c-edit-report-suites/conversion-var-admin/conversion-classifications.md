---
description: Classificaties worden gebruikt om waarden in groepen te categoriseren en op groepsniveau te rapporteren. U kunt bijvoorbeeld alle campagnes voor betaalde zoekopdrachten classificeren in een categorie zoals pop-muziektermen en rapporteren over het succes van die categorie ten opzichte van metriek zoals Instanties (doorklikken) en conversie naar succesgebeurtenissen.
title: Conversieclassificaties
feature: Classifications
role: Admin
exl-id: b4855000-adf3-4e3b-af36-f4803383126d
source-git-commit: a40f30bbe8fdbf98862c4c9a05341fb63962cdd1
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 1%

---

# Conversieclassificaties

Classificaties worden gebruikt om waarden in groepen te categoriseren en op groepsniveau te rapporteren. Bijvoorbeeld, kunt u alle [!UICONTROL Paid Search] campagnes in een categorie als *pop muziektermijnen* classificeren en over het succes van die categorie met betrekking tot metriek zoals Instanties (klik-door), en omzetting aan succesgebeurtenissen rapporteren. U kunt maximaal 255 classificaties toevoegen aan een variabele.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Conversion]** > **[!UICONTROL Conversion Classifications]**

Met conversieclassificaties kunt u conversievariabelen classificeren. Zodra geclassificeerd, kan om het even welk rapport dat u het gebruiken van de zeer belangrijke gegevens kunt produceren ook worden geproduceerd gebruikend de bijbehorende gegevenseigenschappen.

>[!WARNING]
>
>Het anders noemen van een classificatie kan kwesties met bestaande die regels veroorzaken in de [ de regelbouwer van de Classificatie ](/help/components/classifications/crb/classification-rule-builder.md) worden gecreeerd. Als u een classificatie anders noemt die classificatieregels heeft, zorg ervoor dat u elke regel verbetert zodat richt het aan de anders genoemde classificatie.

## Omzettingsclassificatiebeschrijvingen

| Element | Beschrijving |
| --- | --- |
| Naam | De indelingsnaam |
| Datum ingeschakeld (alleen tekst) | Geeft aan of de tekstclassificatie een datumbereik voor campagnevariabelen is. |
| Opties (alleen tekst) | Hiermee maakt u een lijst met classificatiewaarden die beschikbaar zijn voor deze classificatie. Gebruik Opties met campagnevariabelen om gebruikers een lijst met ondersteunde waarden voor de classificatie in Campagnebeheer te bieden. |
| Type nummer (alleen numeriek) | Geeft het type getal in de numerieke classificatie aan. U kunt onder andere de opties Numeriek, Percentage en Valuta kiezen. |

## Conversieclassificaties toevoegen

Conversieclassificaties toevoegen in Admin:

1. Klik op **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** .
1. Selecteer een rapportsuite.
1. Klik op **[!UICONTROL Edit Settings]** > **[!UICONTROL Conversion]** > **[!UICONTROL Conversion Classifications]**.
1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Select Classification Type]** de variabele waaraan u een classificatie wilt toevoegen.

   ![ Info van de Stap ](/help/admin/admin/assets/sub_class_create.png)

1. Plaats de muis boven het pictogram **[!UICONTROL Edit Classification]** en selecteer vervolgens **[!UICONTROL Add Classification]** .
1. Configureer de classificatie naar wens in het dialoogvenster **[!UICONTROL Text Classifications]** .

1. Opties toevoegen aan of verwijderen uit het dialoogvenster Vervolgkeuzelijst.

   Met Opties toevoegen maakt u een lijst met classificatiewaarden die beschikbaar zijn voor deze classificatie. U kunt deze optie gebruiken met campagnevariabelen om gebruikers een lijst van gesteunde waarden voor de classificatie in de Manager van de Campagne te voorzien. Gebruik dit voor classificatiedimensies als u een klein aantal toegestane waarden hebt die zelden of nooit veranderen. U kunt bijvoorbeeld verschillende campagnes voeren die gericht zijn op verschillende niveaus van klantenloyaliteit: Zilver, Goud en Platinum. Vervolgens kunt u de vervolgkeuzelijst gebruiken om er zeker van te zijn dat alleen de waarden worden geaccepteerd die overeenkomen met de drie niveaus. Als iemand een andere waarde probeert te gebruiken, wordt deze genegeerd.

1. Klik op **[!UICONTROL Save]**.

## Een conversieclassificatie verwijderen

Een conversieclassificatie verwijderen wanneer deze niet meer nodig is.

1. Open Report Suite Manager door op **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** in de koptekst van de Suite te klikken.
1. Selecteer een rapportsuite.
1. Klik op **[!UICONTROL Edit Settings]** > **[!UICONTROL Conversion]** > **[!UICONTROL Conversion Classifications]**.
1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Select Classification Type]** de variabele waar u een classificatie wilt verwijderen.
1. Plaats de muis boven het pictogram **[!UICONTROL Edit Classification]** en selecteer vervolgens **[!UICONTROL Delete Classification]** .
1. Klik in het dialoogvenster Classificatie verwijderen op **[!UICONTROL Delete]** .
