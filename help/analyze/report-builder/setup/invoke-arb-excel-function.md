---
description: Hierdoor wordt het gebruik van Report Builder verder geïntegreerd in de natuurlijke Excel-workflow, zonder dat u toegang hoeft te krijgen tot de gebruikersinterface van Report Builder.
title: De functie Report Builder oproepen vanuit Microsoft Excel-functies
uuid: 5342cc4f-085d-4a2d-a498-38b00a3ef4d3
feature: Report Builder
role: User, Admin
exl-id: b412f2b5-affe-4297-af4b-85e8c6dfd257
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 3%

---

# De functie Report Builder oproepen vanuit Microsoft Excel-functies

Hierdoor wordt het gebruik van Report Builder verder geïntegreerd in de natuurlijke Excel-workflow, zonder dat u toegang hoeft te krijgen tot de gebruikersinterface van Report Builder.

U kunt bijvoorbeeld automatisch Report Builder-aanvragen vernieuwen waarvan het invoerfilter is gebaseerd op gegevens die uit andere bronnen in Excel zijn opgehaald. U kunt dit nu doen met de tekenreeks RefreshRequestsInCellsRange(..) functie. Alle vraag is asynchroon. Zij keren onmiddellijk terug en wachten niet op een vraag volledig uit te voeren.

>[!NOTE]
>
>Deze functionaliteit werkt alleen als Report Builder 5.0 (of hoger) is geïnstalleerd.

Hier volgt een tabel met de lijst met belichte functies:

| Functienaam | Beschrijving |
|---|---|
| string AsyncRefreshAll() | Verfrist alle verzoeken van Report Builder aanwezig in een werkboek. |
| string AsyncRefreshRange(string rangeAddressInA1Format) | Hiermee worden alle Report Builder-aanvragen in het opgegeven celbereikadres vernieuwd (een tekenreeksexpressie die een celbereik in A1-indeling vertegenwoordigt, bijvoorbeeld &quot;Sheet1!A2:A10&quot;). |
| string AsyncRefreshRangeAltTextParam() | Hiermee vernieuwt u alle Report Builder-aanvragen in het opgegeven celbereik dat via de alternatieve tekst van MS Form Control wordt doorgegeven. |
| string AsyncRefreshActiveWorksheet() | Hiermee vernieuwt u alle Report Builder-aanvragen in het actieve werkblad. |
| tekenreeks AsyncRefreshWorksheet(werkbladnaam tekenreeks) | Hiermee vernieuwt u alle Report Builder-aanvragen in het opgegeven werkblad (de naam van het werkblad zoals deze wordt weergegeven op het tabblad). |
| string AsyncRefreshWorksheetAltTextParam(); | Hiermee vernieuwt u alle Report Builder-aanvragen in de specifieke werkbladnaam die via de alternatieve tekst van MS Form Control is doorgegeven |
| string GetLastRunStatus() | Retourneert een tekenreeks die de status van de laatste uitvoering beschrijft. |

Ga naar [!UICONTROL Formulas] > [!UICONTROL Insert Function]. Onder aan de lijst met categorieën vindt u Adobe.ReportBuilder.Bridge:

![](assets/arb_functions.png)

## Deze functies in een formule gebruiken {#section_034311081C8D4D7AA9275C1435A087CD}

De formule

```
=IF(OR(ISTEXT(P5),ISBLANK(P5)),AsyncRefreshRange("P9"),"")
```

Hiermee wordt &#39;&#39;Als de waarde in cel P5 tekst is of leeg is, vernieuwt u het bereik in cel P9.&#39;&#39;

## Report Builder-functies gebruiken met formaatcontrole {#section_26123090B5BD49748C8D8ED7A1C5ED84}

U kunt een macro aan een controle nu toewijzen u creeerde en die controle kan een functie zijn die een werkboekverzoek vernieuwt. De functie AsyncRefreshActiveWorksheet vernieuwt bijvoorbeeld alle aanvragen in een werkblad. Soms wilt u echter alleen bepaalde verzoeken vernieuwen, niet alle.

1. Stel de macroparameter in.
1. Klik met de rechtermuisknop op het besturingselement en selecteer **[!UICONTROL Assign Macro]**.
1. Ga de de functienaam van de rapportbouwer in (geen parameters of haakjes.)

![](assets/assign_macro.png)

## Parameters doorgeven aan Report Builder-functies via formaatbesturing {#section_ECCA1F4990D244619DFD79138064CEF0}

De twee functies die een parameter nemen, kunnen met de Controle van het Formaat worden gebruikt, maar slechts via het gebied van de Tekst van Alt:

* AsyncRefreshRange(string rangeAddressInA1Format)
* AsyncRefreshWorksheet(werkbladnaam tekenreeks)

1. Klik met de rechtermuisknop op het besturingselement en selecteer **[!UICONTROL Format Control]**.

   ![](assets/format_control.png)

1. Klik op de knop [!UICONTROL Alt Text] tab.

   ![](assets/alt_text.png)

1. Onder [!UICONTROL Alternative text], voert u het celbereik in dat u wilt vernieuwen.
1. Open de lijst van rapportbuilderparameters onder [!UICONTROL Formulas] > [!UICONTROL Insert Function]> [!UICONTROL Adobe.ReportBuilder.Bridge].

1. Kies een van de twee functies die eindigen met AltTextParam en klik op **[!UICONTROL OK]**.
