---
description: Implementeer de integratie ContactLab voor gebruik in Adobe Analytics.
title: De integratie implementeren
uuid: df3f24c9-d2e3-489e-b97e-e1af0d5dd1fa
translation-type: tm+mt
source-git-commit: 5d8032a9806836e7d0ecbd7fa3652ed1fd137e89
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 3%

---


# De integratie implementeren{#deploying-the-integration}

Deze integratie implementeren is een eenvoudig proces waarvoor de volgende acties nodig zijn:

## Voltooi de Tovenaar van de Integratie van de Adobe{#completing-the-adobe-integration-wizard}

Stappen om de integratietovenaar in de interface van Verbindingen van Gegevens te voltooien.

1. Navigeer naar het gebied Data Connectors (voorheen Genesis) in de Adobe Experience Cloud.
1. Start de wizard voor integratie van ContactLab.
1. Kies de gewenste rapportsuite en geef een naam op voor de integratie.
1. Configureer de volgende items:

   | Item | Beschrijving |
   |---|---|
   | E-mailadres | Het e-mailadres van de primaire contactpersoon |
   | Beschrijving | (Optioneel) Beschrijving voor deze integratie-instelling |

1. Vorm de volgende **[!UICONTROL Variable Mappings]** punten:

   | Item | Beschrijving |
   |---|---|
   | Koppelings-id | Selecteer een eVar voor het verzamelen van identiteitskaart van de Verbinding in echt - tijd. |
   | Bericht-id | Selecteer een eVar voor het verzamelen van identiteitskaart van het Bericht in echt - tijd. |
   | Ontvangers-id | Selecteer een eVar voor het verzamelen van ontvangers-id&#39;s in real-time. |
   | Bounces | Selecteer een numerieke gebeurtenis om dagelijkse grenzen van ContactLab te ontvangen. |
   | Verzonden | Selecteer een numerieke gebeurtenis om dagelijks te ontvangen verzendt van ContactLab. |
   | Geklikt | Selecteer een numerieke gebeurtenis om dagelijkse totale kliks van ContactLab te ontvangen. |
   | Geopend | Selecteer een numerieke gebeurtenis om dagelijks totaal te ontvangen opent van ContactLab. |
   | Abonnement opgezegd | Selecteer een numerieke gebeurtenis om dagelijks afmeldingsgegevens van ContactLab te ontvangen. |

1. Schakel gegevenstoegang in en configureer gegevensverzameling.
   1. Wijzig zo nodig de namen van classificaties.
   1. **[!UICONTROL Partner segments]** zijn standaard remarketing segmenten die in uw integratie inbegrepen zijn.
   1. Selecteer onder **[!UICONTROL Your Segments]** aangepaste segmenten die u in deze integratie wilt opnemen. U kunt extra aangepaste segmenten maken onder het deelvenster Beheer.
   1. Controleer onder **[!UICONTROL Access Requests]** het vakje om productinformatie toe te staan om naar ContactLab in dagelijkse remarketing segmenten worden uitgevoerd.
   1. Wijzig zo nodig de naam van berekende metriek.
   1. Vorm of u identiteitskaart door uw de inzamelingscode van Analytics manueel bij te werken of door de geautomatiseerde oplossing te gebruiken zult verzamelen. Als u **[!UICONTROL Automated Solution]** selecteert, moet u de parameters omvatten die in e-mailverbindingen worden gebruikt om identiteitskaart&#39;s over te gaan.
1. Herzie alle configuratiepunten en klik **[!UICONTROL Activate Now]**.

## De integratie verifiëren{#verifying-the-integration}

De integratie-instellingen van ContactLab weergeven in de Adobe Experience Cloud

1. Bekijk het logboek van de integratieactiviteit.
   1. Navigeer in de Adobe Experience Cloud naar **[!UICONTROL Support]** > **[!UICONTROL Integration Activity Log]**.

      ![](assets/integration_activity_log.png)

   1. Zoek naar ingangen zoals **[!UICONTROL Classification Data imported successfully]**, **[!UICONTROL Metrics Data imported successfully]**, en **[!UICONTROL Metric Data exported successfully]**. Deze ingangen zouden binnen 1 dag van succesvolle plaatsing moeten verschijnen.
1. Je rapportgegevens bekijken in Adobe Analytics.
   1. Ga naar **[!UICONTROL Custom Conversion]** > **[!UICONTROL Custom Conversion 1-10]** > **[!UICONTROL Message ID Reports]**.

      ![](assets/reporting.png)

   1. Zoek ContactLab rapportering. Deze gegevens moeten binnen 24-48 uur na een geslaagde implementatie worden weergegeven.
