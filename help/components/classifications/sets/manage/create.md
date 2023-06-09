---
title: Een classificatieset maken
description: Beschikbare velden en beschrijvingen bij het maken van een classificatieset.
exl-id: 6d692d90-8cc7-4306-a780-58d03db45be8
source-git-commit: d0e3b28590b24d630a192ee857a7d84c115dc8c1
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---

# Een classificatieset maken

U kunt de functie voor classificatiesets gebruiken om een classificatieset te maken.

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Sets]** > **[!UICONTROL Add]**

Wanneer u een classificatieset maakt, zijn de volgende velden beschikbaar.

* **[!UICONTROL Name]**: Een tekstveld dat wordt gebruikt om de classificatieset te identificeren. Dit veld kan niet worden bewerkt tijdens het maken, maar u kunt de naam later wijzigen.
* **[!UICONTROL Column Name]**: De naam van de eerste classificatiedimensie die u wilt maken. Dit veld is de naam van de dimensie die in Analysis Workspace wordt gebruikt en de kolomnaam bij het exporteren van classificatiegegevens. U kunt meer kolomnamen toevoegen nadat de classificatieset is gemaakt.
* **[!UICONTROL Type]**: Keuzerondjes die het type classificatie aangeven. Primaire classificaties worden doorgaans gebruikt; Opzoekclassificaties worden weergegeven [Subclassificaties](../../c-sub-classifications.md).
* **[!UICONTROL Subscriptions]** De rapporteereeksen en -afmetingen waarop deze classificatieset van toepassing is. U kunt veelvoudige rapportreeks en afmetingscombinaties aan een classificatiereeks toevoegen.

![Een classificatieset maken](../../assets/classification-set-create.png)

Als een classificatieset voor een bepaalde rapportreeks + variabele bestaat, wordt de classificatie toegevoegd aan het schema. Een bepaalde rapportsuite + variabele combinatie kan niet tot meerdere classificatiesets behoren.
