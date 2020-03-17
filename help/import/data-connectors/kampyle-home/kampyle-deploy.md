---
description: 'null'
title: De integratie implementeren
uuid: ebb385ca-7bfb-4cd3-9ff6-a5f5a52db5c9
translation-type: tm+mt
source-git-commit: a02fb674ea71a05e085c8e9b2dc4460f62f2cd51

---


# De integratie implementeren{#deploying-the-integration}

Het implementeren van deze integratie is een eenvoudig proces waarbij de wizard Adobe Integration wordt voltooid, de insteekmodulecode (javascript) wordt geïmplementeerd en de integratie wordt gecontroleerd.

## De wizard Adobe Integration voltooien{#complete-the-adobe-integration-wizard}

Om de integratie te activeren, moet u de configuratietovenaar binnen de interface van Verbindingen van Gegevens voltooien.

1. Meld u aan bij Adobe Experience Cloud.
1. Navigeer naar **[!UICONTROL Data Connectors]** (voorheen Genesis).
1. Start de integratiewizard van Kampyle.
1. Selecteer de gewenste rapportsuite en geef een naam op voor de integratie.
1. Configureer de volgende items:
   1. **[!UICONTROL Email address]** - het e-mailadres van de primaire contactpersoon.
   1. **[!UICONTROL Description]** - (facultatief) beschrijving voor deze integratieopstelling.
   1. **[!UICONTROL Kampyle Key]** - Zoek deze sleutel in de Kampyle-toepassing onder **[!UICONTROL Feedback Form]** > **[!UICONTROL Feedback Form Customization]**.
   1. **[!UICONTROL Tracking Server]** - de instelling voor de trackingserver (domein) waarmee u de gegevens van Adobe Analytics kunt bijhouden.
   1. **[!UICONTROL Tracking Server Secure]** - Als uw trackingserver anders is voor beveiligd/https-verkeer, moet u die instelling hier opgeven.
1. Configureer de volgende **[!UICONTROL Variable Mappings]** items:
   1. **[!UICONTROL Kampyle Feedback ID]** -Selecteer een beschikbare eVar variabele van uw rapportreeks
   1. **[!UICONTROL Feedback Grade]** - Selecteer een beschikbare succesgebeurtenis (type &quot;teller&quot;) in uw rapportsuite.
   1. **[!UICONTROL Feedback Items]** - Selecteer een beschikbare succesgebeurtenis (type &quot;teller&quot;) in uw rapportsuite.
   1. **[!UICONTROL Feedback with Grade]** - Selecteer een beschikbare succesgebeurtenis (type &quot;teller&quot;) in uw rapportsuite.
1. Schakel het selectievakje in om het Kampyle Integration-dashboard automatisch voor u te maken (aanbevolen).
1. Controleer alle configuratiepunten en klik **[!UICONTROL Activate Now]**.

## Implementeer het Configuration-object Integratie{#deploy-the-integration-configuration-object}

Na de voltooiing van de integratietovenaar, moet u het voorwerp van de integratieconfiguratie aan uw Webbezit opstellen.

In veel gevallen is het opnemen van het integratieconfiguratieobject in de implementatiecode van Adobe Analytics de eenvoudigste manier om dit te implementeren.

> [!NOTE] Als u Adobe TagManager of Dynamic Tag Management gebruikt om Adobe Analytics te implementeren, kunt u het integratieconfiguratieobject eenvoudig toevoegen met dat hulpprogramma.

1. Navigeer naar het tabblad **[!UICONTROL Resources]** **[!UICONTROL Support]** > van de integratie.
1. Download en sla de **[!UICONTROL Kampyle Integration Code (JS)]** bron op. De code ziet er ongeveer als volgt uit:

   ```
   /* Kampyle:  Integration configuration settings */
     window.k_sc_param = { "version":1.1 }
   ```

1. Implementeer de code met een van de volgende methoden:
| **U gebruikt Adobe TagManager of Dynamisch tagbeheer.** | Gebruik de interface voor tagbeheer om de code toe te voegen. ||—|—|| **In alle andere gevallen** | Lever de code aan de organisatiebron die verantwoordelijk is voor het bijwerken van de implementatiecode van Adobe Analytics.  |

## De integratie controleren{#verify-the-integration}

Valideer dat de integratie gegevens overbrengt door een paar controles te voltooien.

### Integratieactiviteitenlog {#section-0472df9180db4f218db5f6040cab07af}

Ga naar **[!UICONTROL Support]** > **[!UICONTROL Integration Activity Log]**. Onder het **[!UICONTROL Data In]** tabblad ziet u vermeldingen die aangeven dat classificatiegegevens zijn geïmporteerd.

> [!NOTE] Logboekinvoer moet binnen 24 uur na de succesvolle implementatie worden weergegeven.

![](assets/integration_activity_log.png)

### Adobe-rapportgegevens {#section-1ae9f0a5e6bc40988478ff55aefd56ac}

Bekijk uw Kampyle-feedbackrapporten met Adobe Analytics door naar de Kampyle-rapportage te navigeren binnen de juiste menustructuur.

> [!NOTE] Gegevens moeten binnen 24-48 uur na een geslaagde implementatie worden gerapporteerd, ervan uitgaande dat de geïntegreerde feedbackformulieren actief inzendingen ontvangen.

![](assets/adobe_reporting_data.png)

