---
description: Classificaties worden gebruikt om waarden in groepen te categoriseren en op groepsniveau te rapporteren. U kunt bijvoorbeeld alle campagnes voor betaalde zoekopdrachten classificeren in een categorie zoals pop-muziektermen en rapporteren over het succes van die categorie ten opzichte van metriek zoals Instanties (doorklikken) en conversie naar succesgebeurtenissen.
title: Conversieclassificaties
feature: Classifications
role: Admin
exl-id: b4855000-adf3-4e3b-af36-f4803383126d
source-git-commit: 429aaa43fdae669350bdb5a5a54a7d4b9b1c65f2
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 1%

---

# Conversieclassificaties

Classificaties worden gebruikt om waarden in groepen te categoriseren en op groepsniveau te rapporteren. U kunt bijvoorbeeld alles classificeren [!UICONTROL Paid Search] campagnes in een soort categorie *pop-muzieknoten* en rapporteren over het succes van die categorie ten opzichte van metriek zoals Instanties (klik-door), en omzetting in succesgebeurtenissen. U kunt maximaal 255 classificaties toevoegen aan een variabele.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Conversion]** > **[!UICONTROL Conversion Classifications]**

Met conversieclassificaties kunt u conversievariabelen classificeren. Zodra geclassificeerd, kan om het even welk rapport dat u het gebruiken van de zeer belangrijke gegevens kunt produceren ook worden geproduceerd gebruikend de bijbehorende gegevenseigenschappen.

Gebruik na het inschakelen van classificaties de opdracht [Classificatieimportmodule](/help/components/classifications/importer/c-working-with-saint.md) specifieke waarden aan de juiste classificatie toe te wijzen.

>[!WARNING]
>
>Als u de naam van een classificatie wijzigt, kunnen er problemen ontstaan met bestaande regels die zijn gemaakt in het dialoogvenster [Bouwer van classificatieregel](/help/components/classifications/crb/classification-rule-builder.md). Als u een classificatie anders noemt die classificatieregels heeft, zorg ervoor dat u elke regel verbetert zodat richt het aan de anders genoemde classificatie.

## Omzettingsclassificatiebeschrijvingen

| Element | Beschrijving |
| --- | --- |
| Naam | De indelingsnaam |
| Datum ingeschakeld (alleen tekst) | Geeft aan of de tekstclassificatie een datumbereik voor campagnevariabelen is. |
| Opties (alleen tekst) | Hiermee maakt u een lijst met classificatiewaarden die beschikbaar zijn voor deze classificatie. Gebruik Opties met campagnevariabelen om gebruikers een lijst met ondersteunde waarden voor de classificatie in Campagnebeheer te bieden. |
| Type nummer (alleen numeriek) | Geeft het type getal in de numerieke classificatie aan. U kunt onder andere de opties Numeriek, Percentage en Valuta kiezen. |

## Conversieclassificaties toevoegen

Conversieclassificaties toevoegen in Admin:

1. Klikken **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. Selecteer een rapportsuite.
1. Klik op **[!UICONTROL Edit Settings]** > **[!UICONTROL Conversion]** > **[!UICONTROL Conversion Classifications]**.
1. Van de **[!UICONTROL Select Classification Type]** vervolgkeuzelijst, selecteert u de variabele waaraan u een classificatie wilt toevoegen.

   ![Stapinfo](/help/admin/admin/assets/sub_class_create.png)

1. Muis over de **[!UICONTROL Edit Classification]** pictogram, dan selecteren **[!UICONTROL Add Classification]**.
1. In de **[!UICONTROL Select Type]** selecteert u het type classificatie dat u aan de variabele wilt toevoegen.

   Opties omvatten **[!UICONTROL Text]** en **[!UICONTROL Numeric]**. Zie voor meer informatie over classificatietypen [Over classificaties](/help/components/classifications/c-classifications.md).
1. In de **[!UICONTROL Text Classifications]** de classificatie naar wens configureren.

1. Opties toevoegen aan of verwijderen uit het dialoogvenster Vervolgkeuzelijst.

   Met Opties toevoegen maakt u een lijst met classificatiewaarden die beschikbaar zijn voor deze classificatie. U kunt deze optie gebruiken met campagnevariabelen om gebruikers een lijst van gesteunde waarden voor de classificatie in de Manager van de Campagne te voorzien. Gebruik dit voor classificatiedimensies als u een klein aantal toegestane waarden hebt die zelden of nooit veranderen. U kunt bijvoorbeeld verschillende campagnes voeren die gericht zijn op verschillende niveaus van klantenloyaliteit: Zilver, Goud en Platinum. Vervolgens kunt u de vervolgkeuzelijst gebruiken om er zeker van te zijn dat alleen de waarden worden geaccepteerd die overeenkomen met de drie niveaus. Als iemand een andere waarde probeert te gebruiken, wordt deze genegeerd.

1. Klik op **[!UICONTROL Save]**.

## Een conversieclassificatie verwijderen

Een conversieclassificatie verwijderen wanneer deze niet meer nodig is.

1. Open Report Suite Manager door op **[!UICONTROL Admin]**> **[!UICONTROL Report Suites]** in de koptekst van de Suite.
1. Selecteer een rapportsuite.
1. Klik op **[!UICONTROL Edit Settings]** > **[!UICONTROL Conversion]** > **[!UICONTROL Conversion Classifications]**.
1. Van de **[!UICONTROL Select Classification Type]** vervolgkeuzelijst, selecteert u de variabele waar u een classificatie wilt verwijderen.
1. Muis over de **[!UICONTROL Edit Classification]** pictogram, dan selecteren **[!UICONTROL Delete Classification]**.
1. Klik in het dialoogvenster Classificatie verwijderen op **[!UICONTROL Delete]**.
