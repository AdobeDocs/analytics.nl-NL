---
title: Create annotations
description: How to create annotations in Workspace.
role: User, Admin
feature: Annotations
exl-id: 3cf9a0fd-11c9-4375-8bbe-9551ba86f86d
source-git-commit: 6a63c480220fa963cf1dc00acdd5e482dc2bab38
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# Create annotations

>[!NOTE]
>
>Gradual rollout of this feature starts March 23, 2022. General Availability: April 11, 2022.

1. To create annotations, you have several ways to get started:

| Creation method | Details |
| --- | --- |
| **[!UICONTROL Analytics][!UICONTROL Components][!UICONTROL Annotation]** | The Annotations Manager page opens. [!UICONTROL Create New Annotation][!UICONTROL Annotation builder] |
| **** | [!UICONTROL The Annotation builder] Note that, by default, annotations created this way are visible only in the project where they were created. But you can make them available to all projects. Also notice that the date/s and any metric, etc., have already been populated.<p>![](assets/annotate-table.png) |
| **[!UICONTROL Line]** | [!UICONTROL Annotation builder] Note that, by default, annotations created this way are visible only in the project where they were created. But you can make them available to all projects. Also notice that the date/s and any metric, etc., have already been populated.<p>![](assets/annotate-line.png) |
| **[!UICONTROL Components][!UICONTROL Create annotation]** | [!UICONTROL Annotation builder] |
| ****`ctrl``shift``shift``command` | Note that by using the hotkey to create an annotation, you create a single-day annotation for the current date, without any pre-selected scope (metrics or dimensions). |
| **[](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/annotations/)** | The Analytics 2.0 Annotations APIs allow you to create, update, or retrieve annotations programmatically through Adobe I/O. These APIs use the same data and methods that Adobe uses inside the product UI. |

1. [!UICONTROL Annotation builder]

   ![](assets/ann-builder.png)

   | Element | Beschrijving |
   | --- | --- |
   | [!UICONTROL Project-only Annotation] | By default, the annotation applies to the current project. By checking this box, you can make the annotation available to all projects that you own.<p> ![](assets/project-only.png) |
   | [!UICONTROL Title] | Name the annotation, e.g. &quot;Memorial Day&quot; |
   | [!UICONTROL Description] | (Optional) Provide a description for the annotation, e.g. &quot;Public holiday observed in the US&quot;. |
   | [!UICONTROL Tags] | (Optional) Organize annotations by creating or applying a tag. |
   | [!UICONTROL Applied date] | Select the date or date range that needs to be present for the annotation to be visible. |
   | [!UICONTROL Color] | Apply a color to the annotation. The annotation appears in the project with the selected color. Color can be used to categorize annotations, such as public holidays, external events, tracking issues, etc. |
   | [!UICONTROL Scope] | (Optional) Drag and drop the metrics that trigger the annotation. Then drag and drop any dimensions or segments that act as as filters (i.e., that the annotation will be visible with). If you don&#39;t specify a scope, the annotation will apply to all your data.<ul><li>**[!UICONTROL Any of these metrics are present]**</li><li>**[!UICONTROL With all of these filters]**</li></ul><p>Use cases: An eVar has stopped collecting data for a specific date range. **[!UICONTROL Any of these metrics are present]** [!UICONTROL Visits]<p>**** The desired calculated metric must also be added to the scope section to display the annotation. However, a new annotation should be created for any segment that you wish to annotate with the same information.<p>[!UICONTROL Orders] [!UICONTROL Orders] The new calculated metric will not automatically display the annotation for orders; the calculated metric must be also be added to the scope section for the annotation to be displayed. |
   | [!UICONTROL Apply to all report suites] | By default, the annotation applies to the originating report suite. By checking this box, you can make the annotation apply to all report suites in the company. |

   {style=&quot;table-layout:auto&quot;}

1. Klik op **[!UICONTROL Save]**.
