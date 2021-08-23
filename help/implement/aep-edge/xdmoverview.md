---
title: XDM-gegevens gebruiken met Analytics
description: Overzicht van het gebruik van XDM-gegevens van Experience Platform in Adobe Analytics
exl-id: 6f1282fb-8d4a-4d88-9be0-1c939c22cb92
source-git-commit: 3def20b348713b580429e342ad3319963cae6549
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 2%

---

# Adobe Experience Platform Edge-gegevens gebruiken met Analytics

U kunt de [Adobe Experience Platform (AEP) Web SDK](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/sdk/overview.html) gebruiken om gegevens naar Adobe Analytics te verzenden. Dit werkt door het [Gegevensmodel van de Ervaring (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl) in een formaat te vertalen dat door Analytics wordt gebruikt.

Analytics verzamelt XDM-gegevens via twee methoden:

* Automatische toewijzing van XDM-schema&#39;s
* Handmatige toewijzing aan contextgegevens

## Automatische toewijzing

Automatische toewijzing is afhankelijk van een standaardschema [schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html) in XDM dat JSON-objecten automatisch vult die zijn opgenomen in de standaardgegevensverzameling Analytics. De variabelen van Analytics die automatisch van XDM aan uw gevormde rapportreeksen worden in kaart gebracht vereisen geen ontwikkelaarssteun om op te nemen. Zie [Variabelen die automatisch in Analytics](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/adobe-analytics/automatically-mapped-vars.html) in de de gebruikersgids van SDK van het Web van het Platform worden in kaart gebracht.

## Handmatige toewijzing

[Handmatige toewijzing van XDM-gegevens aan ](xdm-manual.md) Analytics is afhankelijk van  [Analytics-](../vars/page-vars/contextdata.md) contextgegevens. Deze variabelen worden in JSON-objecten geplaatst die overeenkomen met de toepasselijke schema&#39;s. Typisch, voegt uw ontwikkelingsteam contextgegevens bij implementatie toe en dan Admins plaatste [verwerkingsregels](/help/admin/admin/c-processing-rules/c-processing-rules-configuration/t-processing-rules.md) om die gegevens op gespecificeerde rapportreeksen toe te passen.

## Instellen

Analytics instellen voor het ontvangen van XDM-gegevens:

1. Installeer en [configureer](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html) de [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html).

2. Controleer of de toepasselijke rapportsuites zijn toegewezen aan de gewenste gegevens. XDM-gegevens worden automatisch vanuit het Adobe Experience-platform naar de rapportsuite verzonden.
