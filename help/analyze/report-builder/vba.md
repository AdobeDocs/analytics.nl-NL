---
title: Visual Basic-macro's in Report Builder
description: Breid de functionaliteit van de werkboeken van Excel en Report Builder uit gebruikend VBA.
feature: Report Builder
role: User, Admin
exl-id: 0d92bce2-22ae-4b0c-af1d-3d12f2041ddf
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 1%

---

# Visual Basic-macro&#39;s in Report Builder

De macro&#39;s van VBA, die ook als Macro&#39;s van Visual Basic worden bekend, staan u toe om werkboeken op manieren te manipuleren alleen Microsoft Excel niet kan. Visual Basic heeft toegang tot het werkboek, Excel, en zelfs Vensters.

Adobe ondersteunt drie Report Builder API-methoden. Zorg ervoor dat de recentste versie van rapportbouwer geïnstalleerd is, en login alvorens om het even welke macro&#39;s in werking te stellen.

>[!IMPORTANT]
>
>Om veiligheidsredenen, kunt u geen werkboek plannen dat een macro bevat.

## `RefreshAllReportBuilderRequests()`

De macro `RefreshAllReportBuilderRequests()` vernieuwt alle verzoeken van Report Builder in het actieve werkboek. Het begint door Report Builder Com toe:voegen-binnen door zijn identiteitskaart van het Product te roepen, dan roept `RefreshAllRequests()` API bevel:

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

Met de macro `RefreshAllReportBuilderRequestsInActiveWorksheet()` worden alle Report Builder-aanvragen in het actieve werkblad vernieuwd. De `RefreshWorksheetRequests()` API vraag neemt een aantekenvelvoorwerp als argument. U kunt deze vraag voor om het even welk aantekenvel gebruiken dat Report Builder verzoeken bevat:

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

Met de macro `RefreshAllReportBuilderRequestsInCellsRange()` worden alle Report Builder-aanvragen vernieuwd waarvan de celuitvoer het opgegeven celbereik doorsnijdt. De celwaaier die in dit voorbeeld wordt gebruikt richt aan de waaier `B1:B54` van het aantekenvel van &quot;Gegevens&quot;binnen het actieve werkboek. De bereikexpressie ondersteunt alle ondersteunde Excel-bereikexpressies:

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
