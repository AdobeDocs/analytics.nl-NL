---
description: 'null'
title: De integratie implementeren
uuid: 1a0770a7-c61b-4eec-a9b3-983def842ad8
translation-type: tm+mt
source-git-commit: ''

---


# De integratie implementeren{#deploying-the-integration}

Deze integratie implementeren is een eenvoudig proces dat bestaat uit het voltooien van de Adobe Integration Wizard en het controleren van de integratie.

## De wizard Adobe Integration voltooien{#completing-the-adobe-integration-wizard}

Stappen om de integratietovenaar in de interface van Verbindingen van Gegevens te voltooien.

1. Navigeer naar het gebied Gegevensverbindingen (voorheen Genesis) in de Adobe Experience Cloud.
1. Start de integratiewizard Dynamisch signaal.
1. Kies de gewenste rapportsuite en geef een naam op voor de integratie.
1. Configureer de volgende items:

   | Item | Beschrijving |
   |---|---|
   | E-mailadres | Het e-mailadres van de primaire contactpersoon. |
   | Beschrijving | (Optioneel) Beschrijving voor deze integratie-instelling. |
   | Community-id | U kunt deze id verkrijgen van uw vertegenwoordiger voor dynamisch signaal. |

1. Configureer de volgende **[!UICONTROL Variable Mappings]** items:

   | Item | Beschrijving |
   |---|---|
   | Trackingcode | Selecteer een beschikbare eVar variabele van uw rapportreeks. |

1. Herzie de classificaties die voor deze integratie zullen worden gecreeerd.
1. Schakel het selectievakje in om het dashboard voor dynamische signaalintegratie te maken (optioneel, maar sterk aanbevolen).
1. Controleer alle configuratiepunten en klik **[!UICONTROL Activate Now]**.
1. **Belangrijk**: Zodra u de tovenaar hebt voltooid, moet u uw Dynamische Vertegenwoordiger van het Signaal op de hoogte brengen zodat zij de integratie op het platform kunnen activeren VoiceStorm.

## Integratie controleren{#verifying-the-integration}

Stappen om uw instellingen voor de integratie van Dynamic Signal VoiceStorm in de Adobe Experience Cloud weer te geven

1. Bekijk uw Dynamic Signal-integratie-instelling in het logboek voor integratieactiviteiten.
   1. Ga in de Adobe Experience Cloud naar **[!UICONTROL Support]** > **[!UICONTROL Integration Activity Log]** .

      ![](assets/integration_activity_log.png)

   1. Zoek naar ingangen als **[!UICONTROL Classification Data imported successfully]**. Deze ingangen zouden binnen 24 uren na succesvolle plaatsing moeten verschijnen.
1. Controleer uw Dynamic Signal-rapporten in Adobe Analytics met het dashboard dat automatisch voor u is gemaakt met de wizard Adobe Integration (Stap 7). U kunt ook naar het Dynamic Signal-rapport navigeren in de menustructuur van Adobe Analytics. Raadpleeg hiervoor de volgende schermafbeeldingen.

   **Opmerking**: Deze gegevens moeten binnen 24-48 uur na een geslaagde implementatie worden weergegeven.

   ![](assets/reporting.png)

   ![](assets/reporting2.png)
