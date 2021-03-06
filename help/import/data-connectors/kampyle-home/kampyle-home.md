---
description: Gebruik de gegevensconnector van Kampyle met Adobe Analytics.
title: Kampyle Data Connector voor Adobe Analytics
uuid: f7733c81-93f5-4c50-b83a-721a6fbd4e8e
translation-type: tm+mt
source-git-commit: 5d8032a9806836e7d0ecbd7fa3652ed1fd137e89
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 5%

---


# Kampyle Data Connector voor Adobe Analytics{#kampyle-data-connector-for-adobe-analytics}

>[!IMPORTANT]
>
>Op 1 augustus 2021 zullen we de Adobe Data Connector-technologie aan het einde van de levensduur hebben. [Meer informatie...](/help/import/data-connectors/data-connectors-eol.md)

De Kampyle Data Connector voor Adobe Analytics combineert het geïntegreerde feedbacksysteem van Kampyle en de gedragsrapportage van Adobe Analytics® om krachtige analysemogelijkheden en optimaliseringsmogelijkheden voor uw organisatie te creëren.

De online marketeers realiseren zich steeds meer de relevantie van klantenfeedback in het opbouwen van merken en het aansturen van bedrijfsresultaten. Met de Kampyle Data Connector voor Adobe Analytics® krijgt Adobe Analytics feedback van bezoekers. Het laat u bezoekersgedrag in de context van hun houding en meningen analyseren. Op deze manier kunt u optimaliseren op basis van feedback en de conversiesnelheden verbeteren.

## Integratievereisten{#integration-prerequisites}

Vereisten om te overwegen alvorens u de gegevensschakelaar kunt activeren.

### Vereisten voor Adobe-klanten: {#section-d9c2e266931249e596de5f4406b5b6f0}

* U moet een huidige Adobe Analytics-klant zijn.
* U moet een Admin-gebruiker zijn.
* U moet 1 beschikbare en toegelaten variabele van de eVar binnen uw rapportreeks hebben.
* U moet 3 beschikbare en toegelaten douanegebeurtenissen binnen uw rapportreeks hebben (type: teller).

### Vereisten voor Kampyle-klanten: {#section-4bbbca50e74d4f218414ae0cc535b8e9}

* U moet een huidige klant van Kampyle voor Websites zijn.
* U moet een Adobe Experience Cloud-beheerder met machtigingen zijn om gegevensconnectors in te schakelen.
* U moet de persoonlijke sleutel van Kampyle van de het beheersinterface van het Vorm van de Terugkoppeling van Kampyle kunnen terugwinnen.

## De persoonlijke sleutel van Kampyle ophalen{#retrieve-the-kampyle-private-key}

Stappen om de sleutel binnen de interface van Kampyle terug te winnen.

1. Meld u aan bij uw Kampyle-account op [https://www.kampyle.com/login](https://www.kampyle.com/login).
1. Ga in de linkernavigatie naar **[!UICONTROL Feedback Form]** > **[!UICONTROL Feedback Form Customization]**.

   ![](assets/retrieve_key1.png)

1. Zoek naar Privé Sleutel die op het lagere gedeelte van de belangrijkste inhoudruit wordt vermeld.

   ![](assets/retrieve_key2.png)
