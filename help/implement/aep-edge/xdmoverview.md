---
title: XDM-gegevens gebruiken met Analytics
description: 'Overzicht van het gebruik van XDM-gegevens van Experience Platform in Adobe Analytics '
translation-type: tm+mt
source-git-commit: a28a05047e95d12343fd94f7b11e5cabf7fac070
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---


# Adobe Experience Platform Edge-gegevens gebruiken met Analytics

U kunt de SDK [van het Web van](https://docs.adobe.com/content/help/en/launch/using/extensions-ref/adobe-extension/aep-extension/overview.html) Adobe Experience Platform (AEP) gebruiken om gegevens naar de Analytics van Adobe te verzenden. Dit werkt door het Model van de Gegevens van de [Ervaring (XDM)](https://docs.adobe.com/content/help/en/experience-platform/xdm/home.html) in een formaat te vertalen dat door Analytics wordt gebruikt.

Analytics verzamelt XDM-gegevens via twee methoden:

* Automatische toewijzing van XDM-schema&#39;s
* Handmatige toewijzing aan contextgegevens

## Automatische toewijzing

[Automatische toewijzing](xdm-manual.md) vertrouwt op een standaardschema [](https://docs.adobe.com/content/help/en/experience-platform/xdm/schema/composition.html) in XDM dat automatisch JSON voorwerpen bevolkt die in typische de gegevensinzameling van de Analyse inbegrepen zijn. De variabelen van Analytics die automatisch van XDM aan uw gevormde rapportreeksen worden in kaart gebracht vereisen geen ontwikkelaarssteun om op te nemen.

## Handmatige toewijzing

Handmatige toewijzing van XDM-gegevens aan Analytics is afhankelijk van [analytics-contextgegevensvariabelen](../vars/page-vars/contextdata.md) . Deze variabelen worden in JSON-objecten geplaatst die overeenkomen met de toepasselijke schema&#39;s. Typisch, voegt uw ontwikkelingsteam contextgegevens bij implementatie toe en dan Admins vastgestelde [verwerkingsregels](/help/admin/admin/c-processing-rules/c-processing-rules-configuration/t-processing-rules.md) om die gegevens op gespecificeerde rapportreeksen toe te passen.

## Instellen

Analtyics instellen om XDM-gegevens te ontvangen:

1. Installeer en [configureer](https://docs.adobe.com/content/help/en/experience-platform/edge/fundamentals/configuring-the-sdk.html) de [Adobe Experience Platform Web SDK](https://docs.adobe.com/content/help/en/experience-platform/edge/fundamentals/installing-the-sdk.html).

2. Controleer of de toepasselijke rapportsuites zijn toegewezen aan de gewenste gegevens. XDM-gegevens worden automatisch vanuit het Adobe Experience-platform naar de rapportsuite verzonden.
