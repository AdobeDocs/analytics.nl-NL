---
description: U kunt een complex datumbereik opgeven door een aangepaste expressie op te bouwen.
title: Aangepaste datumexpressies - overzicht
topic: Report builder
uuid: 7d6d7c03-a3f4-4dec-8343-de2e6478bf06
translation-type: tm+mt
source-git-commit: ''

---


# Aangepaste datumexpressies - overzicht

U kunt een complex datumbereik opgeven door een aangepaste expressie op te bouwen.

We raden u aan naar een kalender te verwijzen wanneer u expressies maakt om het aantal weken en dagen correct op te geven. Excel beschikt over verschillende ingebouwde functies waarmee u het aantal dagen, werkdagen, maanden en jaren tussen datums kunt berekenen. U kunt deze functies in formules gebruiken om andere intervallen, zoals weken en kwarten te berekenen.

**Aangepaste expressies inschakelen**

Dit is een voorbeeld **[!UICONTROL Rolling Dates]**.

1. Selecteer op het [!UICONTROL Request Wizard: Step 1]scherm in plaats van **[!UICONTROL Preset Dates]** te gebruiken **[!UICONTROL Rolling Dates]**.

   ![](assets/rolldates1.png)

1. Schakel over naar wekelijks, maandelijks, driemaandelijks of jaarlijks rolbaar. U ziet hoe de opties hieronder veranderen.
1. Klik op **[!UICONTROL Show Advanced Options]** voor meer aanpassingsopties.

   ![](assets/rolldates2.png)

1. Als u bijvoorbeeld de bovenstaande datums wijzigt in het verschuiven van de eerste dag drie maanden geleden naar de eerste dag van deze maand, worden de datums in het gedeelte met vooruitgangsopties automatisch bijgewerkt om aan te geven dat:

   ![](assets/rolldatesfor3.png)

1. Inschakelen **[!UICONTROL Customize Expression]**. Door opties onder te selecteren, kunt u gemakkelijk de syntaxis voor de uitdrukkingen van de douanedatum zien. **[!UICONTROL Rolling Dates]**

   ![](assets/rolldatesfor5.png)

   U kunt Geavanceerde opties gebruiken om aangepaste datumexpressies te combineren en aan te passen. Als u bijvoorbeeld gegevens wilt zien van het eerste van het jaar tot het einde van de laatste volledige maand, kunt u het volgende invoeren: `From: cy` . `To: cm-1d`. In de wizard worden deze datums weergegeven als 1/1/2020-1/31/2020.
