---
title: XDM-gegevens gebruiken met Analytics
description: 'Overzicht van het gebruik van XDM-gegevens van Experience Platform in Adobe Analytics '
translation-type: tm+mt
source-git-commit: 31efa43043120b68de90e817a7980addbe2ded39

---




# Adobe Experience Platform Edge-gegevens gebruiken met Analyse

>[!IMPORTANT]
>
>Adobe Experience Edge Web SDK wordt niet vrijgegeven en is alleen beschikbaar voor bètatests onder uitgenodigde klanten. Deze documentatie is alleen bedoeld voor bètagebruikers en vertegenwoordigt niet de volledige functionaliteit van de functie. Neem contact op met de [klantenservice](https://helpx.adobe.com/nl/contact/enterprise-support.ec.html)van Adobe als u een bètagebruiker voor deze functie wilt worden.


Met de SDK [van het](https://docs.adobe.com/content/help/en/launch/using/extensions-ref/adobe-extension/aep-extension/overview.html) Adobe Experience Platform (AEP) kunt u gegevens verzenden naar Adobe Analytics. Dit werkt door het Model van de Gegevens van de [Ervaring (XDM)](https://docs.adobe.com/content/help/en/experience-platform/xdm/home.html) in een formaat te vertalen dat door Analytics wordt gebruikt.

Analytics verzamelt XDM-gegevens via twee methoden:

* Automatische toewijzing van XDM-schema&#39;s

* Handmatige toewijzing aan contextgegevens

## Automatische toewijzing

Automatische toewijzing is afhankelijk van een standaardschema [](https://docs.adobe.com/content/help/en/experience-platform/xdm/schema/composition.html) in de XDM dat JSON-objecten automatisch vult die zijn opgenomen in de gegevensverzameling Analytics. De variabelen van de [Analytics die automatisch van XDM](https://git.corp.adobe.com/analytics-data-collection/anedge/blob/master/XDM_Translator.md) aan uw gevormde rapportreeksen worden in kaart gebracht vereisen geen ontwikkelaarssteun om op te nemen.

## Handmatige toewijzing

Handmatige toewijzing van XDM-gegevens aan Analytics is afhankelijk van [analytics-contextgegevensvariabelen](https://docs.adobe.com/content/help/en/analytics/implementation/vars/page-vars/contextdata.html) . Deze variabelen worden in JSON-objecten geplaatst die overeenkomen met de toepasselijke schema&#39;s. Typisch, voegt uw ontwikkelingsteam contextgegevens bij implementatie toe en dan Admins vastgestelde [verwerkingsregels](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/processing-rules/processing-rules-configuration/t-processing-rules.html) om die gegevens op gespecificeerde rapportreeksen toe te passen.


## Instellen

Analtyics instellen om XDM-gegevens te ontvangen:

1. Installeer en [configureer](https://docs.adobe.com/content/help/en/experience-platform/edge/fundamentals/configuring-the-sdk.html) de [Adobe Experience Platform Web SDK](https://docs.adobe.com/content/help/en/experience-platform/edge/fundamentals/installing-the-sdk.html).

2. Controleer of de toepasselijke rapportsuites zijn toegewezen aan de gewenste gegevens. XDM-gegevens worden automatisch vanuit het Adobe Experience-platform naar de rapportsuite verzonden.

