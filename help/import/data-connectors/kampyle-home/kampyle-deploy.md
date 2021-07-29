---
description: Implementeer de gegevensconnector van Kampyle in Adobe Analytics.
title: De integratie implementeren
uuid: ebb385ca-7bfb-4cd3-9ff6-a5f5a52db5c9
exl-id: ac8e1f30-cefe-448a-bec6-cda58ee51025
source-git-commit: 9a70d79a83d8274e17407229bab0273abbe80649
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 1%

---

# De integratie implementeren{#deploying-the-integration}

Het implementeren van deze integratie is een eenvoudig proces waarbij de wizard Adobe Integration wordt voltooid, de insteekmodule code (JavaScript) wordt geïmplementeerd en de integratie wordt gecontroleerd.

## Voltooi de wizard Adobe Integration{#complete-the-adobe-integration-wizard}

Om de integratie te activeren, voltooi de configuratietovenaar in de interface van Verbindingen van Gegevens.

1. Meld u aan bij [!DNL Adobe Experience Cloud].
1. Klik op **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL All admin]** > **[!UICONTROL Data connectors]**.
1. Start de integratiewizard van Kampyle.
1. Selecteer de gewenste rapportsuite en geef een naam op voor de integratie.
1. Configureer de volgende items:
   1. **[!UICONTROL Email address]**: Het e-mailadres van de primaire contactpersoon.
   1. **[!UICONTROL Description]** (optioneel): Beschrijving voor deze integratie-instelling.
   1. **[!UICONTROL Kampyle Key]**: Zoek deze sleutel in de Kampyle-toepassing onder  **[!UICONTROL Feedback Form]** >  **[!UICONTROL Feedback Form Customization]**.
   1. **[!UICONTROL Tracking Server]**: De waarde van de trackingserver die u gebruikt om Adobe Analytics-gegevens bij te houden.
   1. **[!UICONTROL Tracking Server Secure]**: Als uw volgende server voor veilig/https verkeer verschillend is, dan verstrek die het plaatsen hier.
1. Vorm de volgende **[!UICONTROL Variable Mappings]** punten:
   1. **[!UICONTROL Kampyle Feedback ID]**: Selecteer een beschikbare eVar-variabele uit uw rapportsuite
   1. **[!UICONTROL Feedback Grade]**: Selecteer een beschikbare succesgebeurtenis (type &quot;teller&quot;) in uw rapportsuite.
   1. **[!UICONTROL Feedback Items]**: Selecteer een beschikbare succesgebeurtenis (type &quot;teller&quot;) in uw rapportsuite.
   1. **[!UICONTROL Feedback with Grade]**: Selecteer een beschikbare succesgebeurtenis (type &quot;teller&quot;) in uw rapportsuite.
1. Schakel het selectievakje in om het Kampyle Integration-dashboard automatisch voor u te maken (aanbevolen).
1. Herzie alle configuratiepunten en klik **[!UICONTROL Activate Now]**.

## Implementeer het Configuration-object Integratie{#deploy-the-integration-configuration-object}

Nadat u de integratietovenaar hebt voltooid, implementeert u het integratieconfiguratieobject in uw webeigenschap. In veel gevallen, is de gemakkelijkste manier om het voorwerp van de integratieconfiguratie op te stellen het met uw de plaatsingscode van Adobe Analytics te omvatten.

>[!NOTE]
>
>Als u tags gebruikt in Adobe Experience Platform, kunt u het integratieconfiguratieobject eenvoudig toevoegen met dat gereedschap.

1. Navigeer naar het tabblad **[!UICONTROL Resources]** > **[!UICONTROL Support]** van de integratie.
2. Download en sla de **[!UICONTROL Kampyle Integration Code (JS)]**-bron op. De code ziet er ongeveer als volgt uit:

   ```
   /* Kampyle:  Integration configuration settings */
     window.k_sc_param = { "version":1.1 }
   ```

3. Implementeer de code met een van de volgende methoden:

   * Gebruik tags in Adobe Experience Platform.
   * Lever de code aan het organisatorische middel dat uw plaatsing van Adobe Analytics handhaaft.

## De integratie controleren{#verify-the-integration}

Valideer dat de integratie gegevens met succes overbrengt door een paar controles te voltooien.

### Integratieactiviteitenlog {#section-0472df9180db4f218db5f6040cab07af}

Bekijk uw integratie-instellingen voor Kampyle in de Adobe Experience Cloud door naar **[!UICONTROL Support]** > **[!UICONTROL Integration Activity Log]** te navigeren. Onder het tabblad **[!UICONTROL Data In]** ziet u vermeldingen die aangeven dat classificatiegegevens correct zijn geïmporteerd.

>[!NOTE]
>
>Logboekinvoer wordt meestal binnen 24 uur na een geslaagde implementatie weergegeven.

![Logboek voor integratieactiviteiten](assets/integration_activity_log.png)

### Adobe Rapportgegevens {#section-1ae9f0a5e6bc40988478ff55aefd56ac}

Bekijk uw Kampyle-feedbackrapporten met Adobe Analytics door naar de Kampyle-rapportage te navigeren binnen de juiste menustructuur.

>[!NOTE]
>
>Gegevens moeten binnen 24-48 uur na een geslaagde implementatie worden gerapporteerd, ervan uitgaande dat de geïntegreerde feedbackformulieren actief inzendingen ontvangen.

![Adobe-rapportagegegevens](assets/adobe_reporting_data.png)
