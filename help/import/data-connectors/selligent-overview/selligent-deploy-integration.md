---
description: Het implementeren van deze integratie is een eenvoudig proces in drie stappen.
title: De integratie implementeren
uuid: c578bf26-34c2-44ea-8e60-2990273f8659
translation-type: tm+mt
source-git-commit: a02fb674ea71a05e085c8e9b2dc4460f62f2cd51

---


# De integratie implementeren{#deploying-the-integration}

Het implementeren van deze integratie is een eenvoudig proces in drie stappen.

## Voltooiend de Tovenaar van de Integratie{#completing-the-integration-wizard}

Als u de integratie wilt activeren, moet u de wizard voor zorgvuldige integratie voltooien in de interface voor gegevensverbindingen.

1. Navigeer naar het gebied Gegevensverbindingen in de Adobe Experience Cloud.

   ![](assets/selligent-data_connectors.png)

1. Sleep de plug-in Selective onder **[!UICONTROL Add Integrations]** en neer naar Adobe Experience Cloud.

   ![](assets/selligent-add_integration.png)

   Hierdoor wordt de &#39;selligent Data Connector Integration&#39; geopend.

1. **Integratie-instellingen**: Kies de gewenste rapportsuite en geef een naam op voor de integratie onder **[!UICONTROL Integration Settings]**.

1. Vul onder **[!UICONTROL Custom Values]** al uw gegevens over de account die u hebt geselecteerd in.

   ![](assets/selligent-general_settings.png)

1. **Variabele toewijzen**: Kies de juiste gereserveerde eVars en gebeurtenissen in de vervolgkeuzemenu&#39;s:

   ![](assets/selligent-variables.png)

1. **Gegevensinstellingen**: U kunt uw eigen segmenten kiezen onder **[!UICONTROL Your Segments]** uitzondering van de drie geautomatiseerde **[!UICONTROL Partner]** segmenten.

1. Voor deze integratie is mogelijk het downloaden van een paar gegevenspunten naar uw account met de optie &#39;Suite&#39; vereist. U kunt ervoor kiezen om dezelfde toegang te verlenen onder **[!UICONTROL Access Request]**.
1. Kies onder **[!UICONTROL Data Collection]**, een geautomatiseerde of handmatige oplossing (JavaScript-plug-in) om parameters van de queryreeks te verzamelen van de bestemmingspagina-URL. Als u een geautomatiseerde oplossing kiest, ga uw parameter van het vraagkoord voor identiteitskaart van het Bericht en Ontvangersidentiteitskaart in die MID en RID respectievelijk is. Neem voor JavaScript-plug-in contact op met uw Adobe Consultant.
1. **Rapportinstellingen**: Schakel onder **[!UICONTROL Dashboard Generation]** het selectievakje in als u het dashboard Selectief automatisch voor u wilt laten genereren.

   ![](assets/selligent-report_settings.png)

1. Bekijk het overzicht van de integratie en klik op **[!UICONTROL Activate]**.

## Configuratie binnen selligent{#configuration-within-selligent}

Zodra de Integratie binnen de Analytics van Adobe wordt toegelaten, wordt een automatische configuratie toegelaten op de Te kiezen kant.

Er is een tracker gemaakt die elke e-mail bijhoudt. Voor het geval u het tot een bepaald domein wilt beperken, gelieve de spoorstaafconfiguratie bij te werken.

We raden u aan de trackingparameter voor Adobe Analytics in de URL naar voren te verplaatsen. Zo zorgt u ervoor dat de Adobe-verwerkingsregels de parameters ophalen van de URL van de bestemmingspagina. Schakel het bijhouden van wijzigingen in door het selectievakje in te schakelen zoals hieronder wordt weergegeven.

![](assets/selligent-tracker.png)

## Integratie controleren{#verifying-the-integration}

Zodra alle plaatsingsstappen zijn voltooid kunt u bevestigen dat de integratie met succes gegevens overbrengt.

Het duurt een paar dagen voordat de gegevensuitwisseling begint. Zorg ervoor dat u contact opneemt met de optie Selectief nadat u de integratie hebt geactiveerd.

### Integratieactiviteitenlog {#section-927e270495db479fba9578915d9ae9c9}

Navigeer naar de gewenste integratie in de gegevensconnectors. Onder het **[!UICONTROL Support]** tabblad ziet u gebeurtenissen zoals Metrische gegevens die zijn geïmporteerd en/of Classificatiegegevens die zijn geïmporteerd:

![](assets/selligent-verifying.png)

### Rapportgegevens {#section-ebd481a162324e66bd6dc8cb4b8d2424}

Geef de juiste maatstaven op voor uw rapporten over het vertrouwelijke bericht.

1. Ga naar Rapport en Analyse onder Adobe Experience Cloud.
1. Selecteer de juiste rapportsuite.
1. Selecteer onder **[!UICONTROL Custom Conversion]**, de **[!UICONTROL Message ID Reports]** en kies **[!UICONTROL Message ID/Message Name]**.
