---
title: XDM-gegevens gebruiken met Analytics
description: 'Overzicht van het gebruik van XDM-gegevens van Experience Platform in Adobe Analytics '
translation-type: tm+mt
source-git-commit: 3526d9f98b545e5f720a0cb127857e7fd5d5388e
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---


# Adobe Experience Platform Edge-gegevens gebruiken met Analyse

Met de SDK [van het](https://docs.adobe.com/content/help/en/launch/using/extensions-ref/adobe-extension/aep-extension/overview.html) Adobe Experience Platform (AEP) kunt u gegevens verzenden naar Adobe Analytics. Dit werkt door het Model van de Gegevens van de [Ervaring (XDM)](https://docs.adobe.com/content/help/en/experience-platform/xdm/home.html) in een formaat te vertalen dat door Analytics wordt gebruikt.

Analytics verzamelt XDM-gegevens via twee methoden:

* Automatische toewijzing van XDM-schema&#39;s

* Handmatige toewijzing aan contextgegevens

## Automatische toewijzing

[Automatische toewijzing](https://git.corp.adobe.com/AdobeDocs/analytics.en/blob/master/help/implement/aep-edge/xdm-manual.md) vertrouwt op een standaardschema [](https://docs.adobe.com/content/help/en/experience-platform/xdm/schema/composition.html) in XDM dat automatisch JSON voorwerpen bevolkt die in typische de gegevensinzameling van de Analyse inbegrepen zijn. De variabelen van de [Analytics die automatisch van XDM](https://git.corp.adobe.com/analytics-data-collection/anedge/blob/master/XDM_Translator.md) aan uw gevormde rapportreeksen worden in kaart gebracht vereisen geen ontwikkelaarssteun om op te nemen.

## Handmatige toewijzing

Handmatige toewijzing van XDM-gegevens aan Analytics is afhankelijk van [analytics-contextgegevensvariabelen](https://docs.adobe.com/content/help/en/analytics/implementation/vars/page-vars/contextdata.html) . Deze variabelen worden in JSON-objecten geplaatst die overeenkomen met de toepasselijke schema&#39;s. Typisch, voegt uw ontwikkelingsteam contextgegevens bij implementatie toe en dan Admins vastgestelde [verwerkingsregels](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/processing-rules/processing-rules-configuration/t-processing-rules.html) om die gegevens op gespecificeerde rapportreeksen toe te passen.


## Instellen

Analtyics instellen om XDM-gegevens te ontvangen:

1. Installeer en [configureer](https://docs.adobe.com/content/help/en/experience-platform/edge/fundamentals/configuring-the-sdk.html) de [Adobe Experience Platform Web SDK](https://docs.adobe.com/content/help/en/experience-platform/edge/fundamentals/installing-the-sdk.html).

2. Controleer of de toepasselijke rapportsuites zijn toegewezen aan de gewenste gegevens. XDM-gegevens worden automatisch vanuit het Adobe Experience-platform naar de rapportsuite verzonden.

