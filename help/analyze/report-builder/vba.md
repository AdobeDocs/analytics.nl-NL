---
title: Hoe te om de macro's van Visual Basic in Report Builder te gebruiken
description: Leer hoe u de functionaliteit van Excel-werkboeken en -Report Builder kunt uitbreiden met VBA-macro's.
feature: Report Builder
role: User, Admin
exl-id: 0d92bce2-22ae-4b0c-af1d-3d12f2041ddf
source-git-commit: 66b7de0b008364e47253d319785c204ca479ab26
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# Visual Basic-macro&#39;s in Report Builder

De macro&#39;s van Visual Basic (VBA) verstrekken eigenschappen die u helpen de werkboeken van Excel verfrissen. Visual Basic heeft toegang tot het werkboek, Excel, en Vensters.

U moet de nieuwste versie van Report Builder uitvoeren en u aanmelden voordat u VBA-macro&#39;s kunt uitvoeren.

>[!IMPORTANT]
>
>Om veiligheidsredenen, kunt u geen werkboek plannen dat een macro bevat.

Adobe ondersteunt drie Report Builder API-methoden.

## `RefreshAllReportBuilderRequests()`

De `RefreshAllReportBuilderRequests()` macro verfrist alle verzoeken van de Report Builder in het actieve werkboek. Het begint door Report Builder toe:voegen-binnen Com door zijn identiteitskaart van het Product te roepen, dan roept `RefreshAllRequests()` API-opdracht:

```vba
Sub RefreshAllReportBuilderRequests()
 
 Dim addIn As COMAddIn
 Dim automationObject As Object
 Dim success As String
 Set addIn = Application.COMAddIns("ReportBuilderAddIn.Connect")
 Set automationObject = addIn.Object
 success = automationObject.RefreshAllRequests(ActiveWorkbook)
 
End Sub
```

## `RefreshAllReportBuilderRequestsInActiveWorksheet()`

De `RefreshAllReportBuilderRequestsInActiveWorksheet()` macro vernieuwt alle verzoeken van de Report Builder in het actieve aantekenvel. De `RefreshWorksheetRequests()` API-aanroep neemt een werkbladobject als argument. U kunt deze vraag voor om het even welk aantekenvel gebruiken dat Report Builder verzoeken bevat:

```vba
Sub RefreshAllReportBuilderRequestsInActiveWorksheet()
 
 Dim addIn As COMAddIn
 Dim automationObject As Object
 Dim success As String
 Set addIn = Application.COMAddIns("ReportBuilderAddIn.Connect")
 Set automationObject = addIn.Object
 success = automationObject.RefreshWorksheetRequests(ActiveWorkbook.ActiveSheet)
 
End Sub
```

## `RefreshAllReportBuilderRequestsInCellsRange()`

De `RefreshAllReportBuilderRequestsInCellsRange()` macro vernieuwt alle verzoeken van de Report Builder de waarvan celoutput de gespecificeerde waaier van cellen snijdt. Het in dit voorbeeld gebruikte celbereik verwijst naar het bereik `B1:B54` van het &quot;aantekenvel van Gegevens&quot;binnen het actieve werkboek. De bereikexpressie ondersteunt alle ondersteunde Excel-bereikexpressies:

```vba
Sub RefreshAllReportBuilderRequestsInCellsRange()
 
 Dim addIn As COMAddIn
 Dim automationObject As Object
 Dim success As String
 Set addIn = Application.COMAddIns("ReportBuilderAddIn.Connect")
 Set automationObject = addIn.Object
 success = automationObject.RefreshRequestsInCellsRange("'Data'!B1:B54")
  
End Sub
```
