---
description: Leer hoe u Microsoft Excel kunt gebruiken met functies voor Report Builder zonder de gebruikersinterface van de Report Builder te openen.
title: Meer informatie over het gebruik van Microsoft Excel met Report Builder-functies
uuid: 5342cc4f-085d-4a2d-a498-38b00a3ef4d3
feature: Report Builder
role: User, Admin
exl-id: b412f2b5-affe-4297-af4b-85e8c6dfd257
source-git-commit: 66b7de0b008364e47253d319785c204ca479ab26
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# Report Builder functies gebruiken met Microsoft Excel

U kunt functies van de Report Builder gebruiken om tot functionaliteit toegang te hebben zonder tot het gebruikersinterface van de Report Builder toegang te hebben.

Bijvoorbeeld, om Report Builder verzoeken met inputfilters automatisch te verfrissen die op gegevens worden gebaseerd die in Excel van andere bronnen worden getrokken, gebruik het koord RefreshRequestsInCellsRange (..) functie. Alle vraag is asynchroon en zij keren onmiddellijk terug en wachten niet om volledig uit te voeren.

**Vereisten**

* Report Builder 5.0 (of hoger) is vereist.

In de volgende tabel worden de belichte functies weergegeven.

| Functienaam | Type | Beschrijving |
|:---| --- | ---|
| AsyncRefreshAll() | string | Verfrist alle verzoeken van de Report Builder huidig in een werkboek. |
| AsyncRefreshRange(string rangeAddressInA1Format) | string | Verfrist alle verzoeken van de Report Builder aanwezig in het gespecificeerde adres van de celwaaier (een koorduitdrukking die een waaier van cel in A1 formaat vertegenwoordigt, bijvoorbeeld &quot;Blad1!A2:A10&quot;). |
| AsyncRefreshRangeAltTextParam() | string | Verfrist alle verzoeken van de Report Builder aanwezig in de gespecificeerde celwaaier die door de Alternatieve Tekst van de Controle van de Vorm MS wordt overgegaan. |
| AsyncRefreshActiveWorksheet() | string | Hiermee vernieuwt u alle verzoeken om Report Builder die aanwezig zijn in het actieve werkblad. |
| AsyncRefreshWorksheet(werkbladnaam tekenreeks) | string | Hiermee vernieuwt u alle aanvragen voor Report Builder die aanwezig zijn in het opgegeven werkblad (de naam van het werkblad zoals deze wordt weergegeven op het tabblad). |
| AsyncRefreshWorksheetAltTextParam(); | string | Hiermee vernieuwt u alle aanvragen voor Report Builder die aanwezig zijn in de specifieke werkbladnaam die is doorgegeven via de alternatieve tekst van MS Form Control |
| String GetLastRunStatus() | string | Retourneert een tekenreeks die de status van de laatste uitvoering beschrijft. |

Ga naar **[!UICONTROL Formulas]** > **[!UICONTROL Insert Function]**. Gebruik het zoekveld om naar een functie te zoeken of selecteer een categorie om de functies in die categorie weer te geven.

![Screenshot met het venster Functie invoegen waarin de categorielijst is uitgevouwen.](assets/arb_functions.png)

## Voorbeeld {#section_034311081C8D4D7AA9275C1435A087CD}

Het volgende voorbeeld toont *Als de waarde in cel P5 tekst is of leeg is, vernieuwt u het bereik in cel P9*.

```
=IF(OR(ISTEXT(P5),ISBLANK(P5)),AsyncRefreshRange("P9"),"")
```

## Report Builder-functies gebruiken met formaatcontrole {#section_26123090B5BD49748C8D8ED7A1C5ED84}

U kunt een macro aan een controle toewijzen u creeerde en die controle kan een functie zijn die een werkboekverzoek vernieuwt. De functie AsyncRefreshActiveWorksheet vernieuwt bijvoorbeeld alle aanvragen in een werkblad. Soms wilt u echter alleen bepaalde verzoeken vernieuwen.

1. Stel de macroparameter in.
1. Klik met de rechtermuisknop op het besturingselement en selecteer **[!UICONTROL Assign Macro]**.
1. Voer de naam van de functie Report Builder in (geen parameters of ronde haakjes).

![Screenshot met het venster Macro toewijzen.](assets/assign_macro.png)

## Parameters doorgeven aan Report Builder-functies met behulp van formaatbesturing {#section_ECCA1F4990D244619DFD79138064CEF0}

Twee functies die een parameter nemen kunnen met de Controle van het Formaat worden gebruikt. U moet de opdracht **Alternatieve tekst:** veld:

* AsyncRefreshRange(string rangeAddressInA1Format)
* AsyncRefreshWorksheet(werkbladnaam tekenreeks)

Parameters doorgeven aan Report Builder-functies met behulp van formaatbesturing

1. Klik met de rechtermuisknop op het besturingselement en selecteer **[!UICONTROL Format Control]**.

   ![Schermafbeelding met daarin de optie Besturingselement geselecteerd.](assets/format_control.png)

1. Klik op de knop **[!UICONTROL Alt Text]** tab.

   ![Screenshot met het tabblad Alt-tekst en het veld Alternatieve tekst:.](assets/alt_text.png)

1. Onder **[!UICONTROL Alternative text]**, voert u het celbereik in dat u wilt vernieuwen.
1. De lijst met parameters voor Report Builder openen onder **[!UICONTROL Formulas]** > **[!UICONTROL Insert Function]**> **[!UICONTROL Adobe.ReportBuilder.Bridge]**.

1. Kies een van de twee functies die eindigen met AltTextParam en klik op **[!UICONTROL OK]**.
