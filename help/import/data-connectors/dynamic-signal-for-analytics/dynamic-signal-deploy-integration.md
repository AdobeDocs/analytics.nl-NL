---
description: Implementeer de Dynamic Signal-gegevensconnector voor gebruik in Adobe Analytics.
title: De integratie implementeren
uuid: 1a0770a7-c61b-4eec-a9b3-983def842ad8
translation-type: tm+mt
source-git-commit: 5d8032a9806836e7d0ecbd7fa3652ed1fd137e89
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 4%

---


# De integratie implementeren{#deploying-the-integration}

Het opstellen van deze integratie is een eenvoudig proces dat bestaat uit de voltooiing van de Tovenaar van de Integratie van de Adobe en het verifiëren van de integratie.

## Voltooiing van de Tovenaar van de Integratie van Adobe{#completing-the-adobe-integration-wizard}

Stappen om de integratietovenaar in de interface van Verbindingen van Gegevens te voltooien.

1. Navigeer naar het gebied Data Connectors (voorheen Genesis) in de Adobe Experience Cloud.
1. Start de integratiewizard Dynamisch signaal.
1. Kies de gewenste rapportsuite en geef een naam op voor de integratie.
1. Configureer de volgende items:

   | Item | Beschrijving |
   |---|---|
   | E-mailadres | Het e-mailadres van de primaire contactpersoon. |
   | Beschrijving | (Optioneel) Beschrijving voor deze integratie-instelling. |
   | Community-id | U kunt deze id verkrijgen van uw vertegenwoordiger voor dynamisch signaal. |

1. Vorm de volgende **[!UICONTROL Variable Mappings]** punten:

   | Item | Beschrijving |
   |---|---|
   | Trackingcode | Selecteer een beschikbare eVar variabele van uw rapportreeks. |

1. Herzie de classificaties die voor deze integratie zullen worden gecreeerd.
1. Schakel het selectievakje in om het dashboard voor dynamische signaalintegratie te maken (optioneel, maar sterk aanbevolen).
1. Herzie alle configuratiepunten en klik **[!UICONTROL Activate Now]**.
1. **Belangrijk**: Zodra u de tovenaar hebt voltooid, moet u uw Dynamische Vertegenwoordiger van het Signaal op de hoogte brengen zodat zij de integratie op het platform kunnen activeren VoiceStorm.

## Integratie controleren{#verifying-the-integration}

Stappen om uw Dynamic Signal VoiceStorm-integratie-instellingen in de Adobe Experience Cloud weer te geven

1. Bekijk uw Dynamic Signal-integratie-instelling in het logboek voor integratieactiviteiten.
   1. Navigeer in de Adobe Experience Cloud naar **[!UICONTROL Support]** > **[!UICONTROL Integration Activity Log]**.

      ![](assets/integration_activity_log.png)

   1. Zoek naar ingangen zoals **[!UICONTROL Classification Data imported successfully]**. Deze ingangen zouden binnen 24 uren na succesvolle plaatsing moeten verschijnen.
1. Controleer uw Dynamic Signal-rapporten in Adobe Analytics met behulp van het dashboard dat automatisch voor u is gemaakt met de wizard Adobe integreren (Stap 7). U kunt ook naar de Dynamic Signal-rapportage navigeren in de menustructuur van Adobe Analytics. Raadpleeg de volgende schermafbeeldingen.

   **Opmerking**: Deze gegevens moeten binnen 24-48 uur na een geslaagde implementatie worden weergegeven.

   ![](assets/reporting.png)

   ![](assets/reporting2.png)
