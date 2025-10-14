---
description: U kunt een complex datumbereik opgeven door een aangepaste expressie op te bouwen.
title: Aangepaste datumexpressies - overzicht
uuid: 7d6d7c03-a3f4-4dec-8343-de2e6478bf06
feature: Report Builder
role: User, Admin
exl-id: b3bdc07e-5c2d-4be3-86c9-b4b7380be0f6
source-git-commit: ae6ffed05f5a33f032d0c7471ccdb1029154ddbd
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# Aangepaste datumexpressies

{{legacy-arb}}

U kunt een complex datumbereik opgeven door een aangepaste expressie op te bouwen.

Wanneer u expressies maakt, raadpleegt u een kalender om het aantal weken en dagen correct op te geven. Excel beschikt over verschillende ingebouwde functies waarmee u het aantal dagen, werkdagen, maanden en jaren tussen datums kunt berekenen. U kunt deze functies in formules gebruiken om andere intervallen, zoals weken en kwarten te berekenen.

**om douaneuitdrukkingen** toe te laten

In het volgende voorbeeld wordt getoond hoe u een aangepaste expressie voor **[!UICONTROL Rolling Dates]** inschakelt.

1. Selecteer **[!UICONTROL Rolling Dates]** in het [!UICONTROL Request Wizard: Step 1] in plaats van **[!UICONTROL Preset Dates]** te gebruiken.

   ![&#x200B; Schermafbeelding die de Geselecteerde Data van het Draaien toont.](assets/rolldates1.png)

1. Schakel over naar wekelijks, maandelijks, driemaandelijks of jaarlijks rolbaar. U ziet hoe de opties hieronder veranderen.
1. Klik op **[!UICONTROL Show Advanced Options]** voor meer aanpassingsopties.

   ![&#x200B; Screenshot die de Show Geavanceerde Opties benadrukt.](assets/rolldates2.png)

1. Als u bijvoorbeeld de bovenstaande datums wijzigt in het verschuiven van de eerste dag drie maanden geleden naar de eerste dag van deze maand, worden de datums in het gedeelte met vooruitgangsopties automatisch bijgewerkt om aan te geven dat:

   ![&#x200B; Scherenshot die de het rollen data van de eerste dag drie maanden geleden aan de eerste dag van deze maand toont.](assets/rolldatesfor3.png)

1. Schakel **[!UICONTROL Customize Expression]** in. Door opties onder **[!UICONTROL Rolling Dates]** te selecteren, kunt u de syntaxis voor aangepaste datumexpressies gemakkelijk zien.

   ![&#x200B; Schermafbeelding tonen die Geselecteerde Uitdrukking van de Aanpassing tonen.](assets/rolldatesfor5.png)

   U kunt Geavanceerde opties gebruiken om aangepaste datumexpressies te combineren en aan te passen. Als u bijvoorbeeld gegevens wilt zien van het eerste van het jaar tot het einde van de laatste volledige maand, kunt u het volgende invoeren: `From: cy` `To: cm-1d` . In de wizard worden deze datums weergegeven als 1/1/2020-1/31/2020.
