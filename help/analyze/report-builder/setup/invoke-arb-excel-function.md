---
description: Deze capaciteit integreert verder het gebruik van de Bouwer van het Rapport binnen het natuurlijke werkschema van Excel, zonder u te vereisen om tot het gebruikersinterface van de Bouwer van het Rapport toegang te hebben.
title: De functie Report Builder aanroepen vanuit Microsoft Excel-functies
topic: Report builder
uuid: 5342cc4f-085d-4a2d-a498-38b00a3ef4d3
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# De functie Report Builder aanroepen vanuit Microsoft Excel-functies

Deze capaciteit integreert verder het gebruik van de Bouwer van het Rapport binnen het natuurlijke werkschema van Excel, zonder u te vereisen om tot het gebruikersinterface van de Bouwer van het Rapport toegang te hebben.

Bijvoorbeeld, kunt u verzoeken van de Bouwer van het Rapport automatisch willen verfrissen de waarvan inputfilter op gegevens gebaseerd is die in Excel uit andere bronnen worden getrokken. U kunt dit nu doen met de tekenreeks RefreshRequestsInCellsRange(..) functie. Alle vraag is asynchroon. Zij keren onmiddellijk terug en wachten niet op een vraag volledig uit te voeren.

> [!NOTE] Deze functionaliteit werkt alleen als Report Builder 5.0 (of hoger) is geïnstalleerd.

Hier volgt een tabel met de lijst met belichte functies:

| Functienaam | Beschrijving |
|---|---|
| string AsyncRefreshAll() | Verfrist alle verzoeken van de Bouwer van het Rapport huidig in een werkboek. |
| string AsyncRefreshRange(string rangeAddressInA1Format) | Verfrist alle verzoeken van de Bouwer van het Rapport huidig in het gespecificeerde adres van de celwaaier (een koorduitdrukking die een waaier van cel in A1 formaat vertegenwoordigt, bijvoorbeeld &quot;Sheet1!A2:A10&quot;). |
| string AsyncRefreshRangeAltTextParam() | Verfrist alle verzoeken van de Bouwer van het Rapport huidig in de gespecificeerde celwaaier die door de Alternatieve Tekst van de Controle van de Vorm MS wordt overgegaan. |
| string AsyncRefreshActiveWorksheet() | Verfrist alle verzoeken van de Bouwer van het Rapport huidig in het actieve aantekenvel. |
| tekenreeks AsyncRefreshWorksheet(werkbladnaam tekenreeks) | Verfrist alle verzoeken van de Bouwer van het Rapport aanwezig in het gespecificeerde aantekenvel (de aantekenvelnaam zoals het op het lusje verschijnt.) |
| string AsyncRefreshWorksheetAltTextParam(); | Verfrist alle verzoeken van de Bouwer van het Rapport huidig in de specifieke aantekenvelnaam die door de Alternatieve Tekst van de Controle van de Vorm MS werd overgegaan |
| string GetLastRunStatus() | Retourneert een tekenreeks die de status van de laatste uitvoering beschrijft. |

Ga naar [!UICONTROL Formulas] > [!UICONTROL Insert Function]. Onder aan de lijst met categorieën vindt u Adobe.ReportBuilder.Bridge:

![](assets/arb_functions.png)

## Deze functies in een formule gebruiken {#section_034311081C8D4D7AA9275C1435A087CD}

De formule

```
=IF(OR(ISTEXT(P5),ISBLANK(P5)),AsyncRefreshRange("P9"),"")
```

Hiermee wordt &#39;&#39;Als de waarde in cel P5 tekst is of leeg is, vernieuwt u het bereik in cel P9.&#39;&#39;

## De functies van de Bouwer van het Rapport van het gebruik met formaatcontrole {#section_26123090B5BD49748C8D8ED7A1C5ED84}

U kunt een macro aan een controle nu toewijzen u creeerde en die controle kan een functie zijn die een werkboekverzoek vernieuwt. De functie AsyncRefreshActiveWorksheet vernieuwt bijvoorbeeld alle aanvragen in een werkblad. Soms wilt u echter alleen bepaalde verzoeken vernieuwen, niet alle.

1. Stel de macroparameter in.
1. Klik met de rechtermuisknop op het besturingselement en selecteer **[!UICONTROL Assign Macro]**.
1. Ga de de functienaam van de rapportbouwer in (geen parameters of haakjes.)

![](assets/assign_macro.png)

## Parameters doorgeven aan de functies van de Bouwer van het Rapport via formaatcontrole {#section_ECCA1F4990D244619DFD79138064CEF0}

De twee functies die een parameter nemen, kunnen met de Controle van het Formaat worden gebruikt, maar slechts via het gebied van de Tekst van Alt:

* AsyncRefreshRange(string rangeAddressInA1Format)
* AsyncRefreshWorksheet(werkbladnaam tekenreeks)

1. Klik met de rechtermuisknop op het besturingselement en selecteer **[!UICONTROL Format Control]**.

   ![](assets/format_control.png)

1. Klik op het [!UICONTROL Alt Text] tabblad.

   ![](assets/alt_text.png)

1. Voer onder [!UICONTROL Alternative text]het celbereik in dat u wilt vernieuwen.
1. Open de lijst met parameters voor het samenstellen van rapporten onder [!UICONTROL Formulas] > [!UICONTROL Insert Function]> [!UICONTROL Adobe.ReportBuilder.Bridge].

1. Kies een van de twee functies die eindigen met AltTextParam en klik **[!UICONTROL OK]**.

