---
description: Verklaart hoe te om Report Builder-gepubliceerde activa in Power BI Desktop te trekken
title: Gepubliceerde assets opvragen in Power BI Desktop
uuid: ef47d5c7-31e0-44fc-a792-bc9d12bb089e
feature: Report Builder
role: User, Admin
exl-id: ce6020df-caf4-4cd2-8086-4357309e5bbb
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 10%

---

# Gepubliceerde assets opvragen in Power BI Desktop

Verklaart hoe te om Report Builder-gepubliceerde activa in Power BI Desktop te trekken

## Vereisten {#section_BDFDAE1E300B429FB6EBCB21AD1383A0}

* De nieuwste versie van Power BI Desktop moet zijn geïnstalleerd (release april 2017)
* Dit proces veronderstelt dat u reeds Report Builder geformatteerde lijsten of verzoeken aan de Dienst van de Power BI hebt gepubliceerd.

## Proces {#section_CB03E6E1B066457EA0F6FC08FFF5EFDD}

In de update van april 2017 van de Desktop van Power BI, vrijgegeven Microsoft de capaciteit om met datasets in de dienst van de Power BI te verbinden. Deze eigenschap staat u toe om nieuwe rapporten van bestaande datasets tot stand te brengen u reeds aan de wolk hebt gepubliceerd. U kunt deze functie gebruiken om beter samen te werken en dubbele inspanningen in uw team te verminderen.

1. Ga in Power BI Desktop naar **[!UICONTROL File]** > **[!UICONTROL Options and settings]** > **[!UICONTROL Options]** > **[!UICONTROL Preview features.]**
1. Schakel **[!UICONTROL Power BI Service Live Connection]** in en klik **[!UICONTROL OK]**. ![](assets/bi-preview-features.png)

1. Start Power BI Desktop opnieuw.
1. Als u het bureaublad opnieuw hebt gestart, gaat u naar **[!UICONTROL Home]** > **[!UICONTROL Get Data]** > **[!UICONTROL More...]**.
1. Zoek naar en selecteer **[!UICONTROL Power BI service]**.
1. Selecteer onder **[!UICONTROL Microsoft Power BI service]** > **[!UICONTROL My Workspace]** de dataset die u eerder van Report Builder had gepubliceerd.

Zie voor meer informatie deze [Microsoft-blogpost](https://powerbi.microsoft.com/en-us/blog/connecting-to-datasets-in-the-power-bi-service-from-desktop/).
