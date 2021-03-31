---
description: U kunt een complex datumbereik opgeven door een aangepaste expressie op te bouwen.
title: Aangepaste datumexpressies - overzicht
uuid: 7d6d7c03-a3f4-4dec-8343-de2e6478bf06
feature: Report Builder
role: Bedrijfs Praktijk, Beheerder
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 4%

---


# Aangepaste datumexpressies - overzicht

U kunt een complex datumbereik opgeven door een aangepaste expressie op te bouwen.

We raden u aan naar een kalender te verwijzen wanneer u expressies maakt om het aantal weken en dagen correct op te geven. Excel beschikt over verschillende ingebouwde functies waarmee u het aantal dagen, werkdagen, maanden en jaren tussen datums kunt berekenen. U kunt deze functies in formules gebruiken om andere intervallen, zoals weken en kwarten te berekenen.

**Aangepaste expressies inschakelen**

Dit is een voorbeeld met **[!UICONTROL Rolling Dates]**.

1. Selecteer **[!UICONTROL Rolling Dates]** in [!UICONTROL Request Wizard: Step 1] in plaats van **[!UICONTROL Preset Dates]** te gebruiken.

   ![](assets/rolldates1.png)

1. Schakel over naar wekelijks, maandelijks, driemaandelijks of jaarlijks rolbaar. U ziet hoe de opties hieronder veranderen.
1. Klik op **[!UICONTROL Show Advanced Options]** voor meer aanpassingsopties.

   ![](assets/rolldates2.png)

1. Als u bijvoorbeeld de bovenstaande datums wijzigt in het verschuiven van de eerste dag drie maanden geleden naar de eerste dag van deze maand, worden de datums in het gedeelte met vooruitgangsopties automatisch bijgewerkt om aan te geven dat:

   ![](assets/rolldatesfor3.png)

1. **[!UICONTROL Customize Expression]** inschakelen. Door opties te selecteren onder **[!UICONTROL Rolling Dates]**, kunt u de syntaxis voor de uitdrukkingen van de douanedatum gemakkelijk zien.

   ![](assets/rolldatesfor5.png)

   U kunt Geavanceerde opties gebruiken om aangepaste datumexpressies te combineren en aan te passen. Als u bijvoorbeeld gegevens wilt zien van het eerste van het jaar tot het einde van de laatste volledige maand, kunt u het volgende invoeren: `From: cy` `To: cm-1d`. In de wizard worden deze datums weergegeven als 1/1/2020-1/31/2020.
