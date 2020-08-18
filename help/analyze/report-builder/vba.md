---
title: Visual Basic-macro's in Report Builder
description: Breid de functionaliteit van de werkboeken van Excel en Report Builder uit gebruikend VBA.
translation-type: tm+mt
source-git-commit: b569f87dde3b9a8b323e0664d6c4d1578d410bb7
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---


# Visual Basic-macro&#39;s in Report Builder

De macro&#39;s van VBA, die ook als Macro&#39;s van Visual Basic worden bekend, staan u toe om werkboeken op manieren te manipuleren alleen Microsoft Excel niet kan. Visual Basic heeft toegang tot het werkboek, Excel, en zelfs Vensters.

Adobe ondersteunt drie Report Builder API-methoden. Zorg ervoor dat de recentste versie van rapportbouwer geïnstalleerd is, en login alvorens om het even welke macro&#39;s in werking te stellen.

>[!IMPORTANT]
>
>Om veiligheidsredenen, kunt u geen werkboek plannen dat een macro bevat.

## `RefreshAllReportBuilderRequests()`

De `RefreshAllReportBuilderRequests()` macro verfrist alle verzoeken van Report Builder in het actieve werkboek. Het begint door Report Builder Com toe:voegen-binnen door zijn identiteitskaart van het Product te roepen, dan roept het `RefreshAllRequests()` API bevel:

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

De `RefreshAllReportBuilderRequestsInCellsRange()` macro vernieuwt alle Report Builder-aanvragen waarvan de celuitvoer het opgegeven celbereik doorsnijdt. De celwaaier die in dit voorbeeld wordt gebruikt richt aan de waaier `B1:B54` van het &quot;aantekenvel van Gegevens&quot;binnen het actieve werkboek. De bereikexpressie ondersteunt alle ondersteunde Excel-bereikexpressies:

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
